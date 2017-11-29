---
title: ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugAppDomain3.GetCachedWinRTTypesForIIDs
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs
helpviewer_keywords:
- ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs method, [.NET Framework debugging]
- GetCachedWinRTTypesForIIDs method, ICorDebugAppDomain3 interface [.NET Framework debugging]
ms.assetid: 23682ca0-1bcf-48e6-996e-69f7ba337682
topic_type: apiref
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 84b58e3a016431eba10710ea384338cb388404ff
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugappdomain3getcachedwinrttypesforiids-method"></a><span data-ttu-id="6c994-102">ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs-Methode</span><span class="sxs-lookup"><span data-stu-id="6c994-102">ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs Method</span></span>
<span data-ttu-id="6c994-103">Ruft einen Enumerator ab, für die zwischengespeicherten [!INCLUDE[wrt](../../../../includes/wrt-md.md)] Typen in einer Anwendungsdomäne basierend auf deren Schnittstellenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="6c994-103">Gets an enumerator for cached [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types in an application domain based on their interface identifiers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c994-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c994-104">Syntax</span></span>  
  
```  
HRESULT GetCachedWinRTTypesForIIDs (   
    [in]  ULONG32            cReqTypes,  
    [in]  GUID                *iidsToResolve,  
    [out] ICorDebugTypeEnum   **ppTypesEnum  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6c994-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c994-105">Parameters</span></span>  
 `cReqTypes`  
 <span data-ttu-id="6c994-106">[in] Die Anzahl der erforderlichen Typen.</span><span class="sxs-lookup"><span data-stu-id="6c994-106">[in] The number of required types.</span></span>  
  
 `iidsToResolve`  
 <span data-ttu-id="6c994-107">[in] Ein Zeiger auf ein Array, das die verwalteten Darstellungen der entsprechenden Schnittstellenbezeichner enthält die [!INCLUDE[wrt](../../../../includes/wrt-md.md)] Typen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c994-107">[in] A pointer to an array that contains the interface identifiers corresponding to the managed representations of the [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types to be retrieved.</span></span>  
  
 `ppTypesEnum`  
 <span data-ttu-id="6c994-108">[out] Ein Zeiger auf die Adresse eines Schnittstellenobjekts "ICorDebugTypeEnum", die die zwischengespeicherten Enumeration ermöglicht verwaltete Darstellungen der [!INCLUDE[wrt](../../../../includes/wrt-md.md)] Typen abgerufen, basierend auf den Schnittstellenbezeichner in `iidsToResolve`.</span><span class="sxs-lookup"><span data-stu-id="6c994-108">[out] A pointer to the address of an "ICorDebugTypeEnum" interface object that allows enumeration of the cached managed representations of the [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types retrieved, based on the interface identifiers in `iidsToResolve`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6c994-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6c994-109">Remarks</span></span>  
 <span data-ttu-id="6c994-110">Wenn die Methode, zum Abrufen von Informationen für eine bestimmte Schnittstelle-ID fehlschlägt, weist der zugehörige Eintrag in der Auflistung "ICorDebugTypeEnum" einen Typ von `ELEMENT_TYPE_END` nach Fehlern aufgrund von Problemen für Daten abrufen, oder `ELEMENT_TYPE_VOID` für unbekannte-Schnittstelle Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="6c994-110">If the method fails to retrieve information for a specific interface identifier, the corresponding entry in the "ICorDebugTypeEnum" collection will have a type of `ELEMENT_TYPE_END` for errors due to data retrieval issues, or `ELEMENT_TYPE_VOID` for unknown interface identifiers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6c994-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c994-111">Requirements</span></span>  
 <span data-ttu-id="6c994-112">**Plattformen:**[!INCLUDE[wrt](../../../../includes/wrt-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6c994-112">**Platforms:** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]</span></span>  
  
 <span data-ttu-id="6c994-113">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6c994-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6c994-114">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6c994-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6c994-115">**.NET Framework-Versionen:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6c994-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c994-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c994-116">See Also</span></span>  
 [<span data-ttu-id="6c994-117">ICorDebugAppDomain3-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6c994-117">ICorDebugAppDomain3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain3-interface.md)