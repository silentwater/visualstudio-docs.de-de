---
title: IDebugBreakpointResolution2::GetResolutionInfo | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugBreakpointResolution2::GetResolutionInfo
helpviewer_keywords:
- IDebugBreakpointResolution2::GetResolutionInfo
ms.assetid: 828cbdf6-b87d-4c45-be87-d87087b04a60
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d1b82921c2d08ed74ba05bb2ccf8ecfb642fa9cc
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56701108"
---
# <a name="idebugbreakpointresolution2getresolutioninfo"></a>IDebugBreakpointResolution2::GetResolutionInfo
Ruft die Informationen der Haltepunkt-Lösung, die diesem Breakpoint beschreibt.

## <a name="syntax"></a>Syntax

```cpp
HRESULT GetResolutionInfo( 
   BPRESI_FIELDS       dwFields,
   BP_RESOLUTION_INFO* pBPResolutionInfo
);
```

```csharp
int GetResolutionInfo( 
   enum BPRESI_FIELDS   dwFields,
   BP_RESOLUTION_INFO[] pBPResolutionInfo
);
```

#### <a name="parameters"></a>Parameter
 `dwFields`

 [in] Eine Kombination von Flags aus der [BPRESI_FIELDS](../../../extensibility/debugger/reference/bpresi-fields.md) Enumeration, die bestimmen, welche Felder von der `pBPResolutionInfo` sind, dass Parameter ausgefüllt werden müssen.

 `pBPResolutionInfo`

 [out] Die [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md) Struktur mit Informationen zu diesem Haltepunkt gefüllt werden soll.

## <a name="return-value"></a>Rückgabewert
 Wenn erfolgreich, wird `S_OK`; gibt andernfalls einen Fehlercode zurück.

## <a name="example"></a>Beispiel
 Das folgende Beispiel implementiert diese Methode für eine einfache `CDebugBreakpointResolution` -Objekt, das macht die [IDebugBreakpointResolution2](../../../extensibility/debugger/reference/idebugbreakpointresolution2.md) Schnittstelle.

```
HRESULT CDebugBreakpointResolution::GetResolutionInfo(
   BPRESI_FIELDS dwFields,
   BP_RESOLUTION_INFO* pBPResolutionInfo)
{
   HRESULT hr;

   if (pBPResolutionInfo)
   {
      // Copy the specified fields of the request information from the class
      // member variable to the local BP_RESOLUTION_INFO variable.
      hr = CopyBP_RESOLUTION_INFO(m_bpResolutionInfo,
                                  *pBPResolutionInfo,
                                  dwFields);
   }
   else
   {
      hr = E_INVALIDARG;
   }

   return hr;
}

HRESULT CDebugBreakpointResolution::CopyBP_RESOLUTION_INFO(
   BP_RESOLUTION_INFO& bpResSrc,
   BP_RESOLUTION_INFO& bpResDest,
   DWORD dwFields)
{
   HRESULT hr = S_OK;

   // Start with a raw copy.
   memcpy(&bpResDest, &bpResSrc, sizeof(BP_RESOLUTION_INFO));

   // The fields in the destination is the result of the AND of
   //  bpInfoSrc.dwFields and dwFields.
   bpResDest.dwFields = dwFields & bpResSrc.dwFields;

   // Fill in the bp location information if the BPRESI_BPRESLOCATION
   //  flag is set in BPRESI_FIELDS.
   if (IsFlagSet(bpResDest.dwFields, BPRESI_BPRESLOCATION))
   {
      // Switch based on the BP_TYPE.
      switch (bpResSrc.bpResLocation.bpType)
      {
         case BPT_CODE:
         {
            // AddRef the IDebugCodeContext2 of the BP_RESOLUTION_CODE structure.
            bpResDest.bpResLocation.bpResLocation.bpresCode.pCodeContext->AddRef();
            break;
         }
         case BPT_DATA:
         {
            // Copy the bstrDataExpr, bstrFunc, and bstrImage of the
            // BP_RESOLUTION_DATA structure.
            bpResDest.bpResLocation.bpResLocation.bpresData.bstrDataExpr =
               SysAllocString(bpResSrc.bpResLocation.bpResLocation.bpresData.bstrDataExpr);
            bpResDest.bpResLocation.bpResLocation.bpresData.bstrFunc =
               SysAllocString(bpResSrc.bpResLocation.bpResLocation.bpresData.bstrFunc);
            bpResSrc.bpResLocation.bpResLocation.bpresData.bstrImage =
               SysAllocString(bpResSrc.bpResLocation.bpResLocation.bpresData.bstrImage);
            break;
         }
         default:
         {
            assert(FALSE);
            // Clear the BPRESI_BPRESLOCATION flag in the BPRESI_FIELDS
            // of the destination BP_RESOLUTION_INFO.
            ClearFlag(bpResDest.dwFields, BPRESI_BPRESLOCATION);
            break;
         }
      }
   }
   // AddRef the IDebugProgram2 if the BPRESI_PROGRAM flag is set in BPRESI_FIELDS.
   if (IsFlagSet(bpResDest.dwFields, BPRESI_PROGRAM))
   {
      bpResDest.pProgram->AddRef();
   }
   // AddRef the IDebugThread2 if the BPRESI_THREAD flag is set in BPRESI_FIELDS.
   if (IsFlagSet(bpResDest.dwFields, BPRESI_THREAD))
   {
      bpResDest.pThread->AddRef();
   }

   return hr;
}
```

## <a name="see-also"></a>Siehe auch
- [IDebugBreakpointResolution2](../../../extensibility/debugger/reference/idebugbreakpointresolution2.md)
- [BPRESI_FIELDS](../../../extensibility/debugger/reference/bpresi-fields.md)
- [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md)