---
title: ICorDebugThread4::GetBlockingObjects-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugThread4.GetBlockingObjects Method
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugThread4::GetBlockingObjects
helpviewer_keywords:
- GetBlockingObjects method [.NET Framework debugging]
- ICorDebugThread4::GetBlockingObjects method [.NET Framework debugging]
ms.assetid: a7e6c54e-7be9-4e52-bbb4-95f52458e8e4
topic_type: apiref
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 6783d7f9af67acdff147cc46ea4f856f9b10bf3a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugthread4getblockingobjects-method"></a><span data-ttu-id="ad174-102">ICorDebugThread4::GetBlockingObjects-Methode</span><span class="sxs-lookup"><span data-stu-id="ad174-102">ICorDebugThread4::GetBlockingObjects Method</span></span>
<span data-ttu-id="ad174-103">Stellt eine geordnete Enumeration von [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) thread Blockierungsinformationen-Strukturen, die bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ad174-103">Provides an ordered enumeration of [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structures that provide thread blocking information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ad174-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad174-104">Syntax</span></span>  
  
```  
HRESULT GetBlockingObjects (  
    [out] ICorDebugBlockingObjectEnum **ppBlockingObjectEnum  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ad174-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad174-105">Parameters</span></span>  
 `ppBlockingObjectEnum`  
 <span data-ttu-id="ad174-106">[out] Ein Zeiger auf eine geordnete Enumeration von [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="ad174-106">[out] A pointer to an ordered enumeration of [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structures.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ad174-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad174-107">Remarks</span></span>  
 <span data-ttu-id="ad174-108">Das erste Element in der zurückgegebenen Enumeration entspricht der ersten Struktur, die den Thread blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="ad174-108">The first element in the returned enumeration corresponds to the first structure that is blocking the thread.</span></span> <span data-ttu-id="ad174-109">Das zweite Element entspricht einem blockierenden Element, das gefunden wird, während der Ausführung eines asynchronen Prozeduraufrufs (APC), wenn auf der ersten und so weiter blockiert.</span><span class="sxs-lookup"><span data-stu-id="ad174-109">The second element corresponds to a blocking item that is encountered while running an asynchronous procedure call (APC) when blocked on the first, and so on.</span></span>  
  
 <span data-ttu-id="ad174-110">Die Enumeration ist nur für die Dauer des aktuellen Status "synchronisiert" gültig.</span><span class="sxs-lookup"><span data-stu-id="ad174-110">The enumeration is valid only for the duration of the current synchronized state.</span></span>  
  
 <span data-ttu-id="ad174-111">Diese Methode muss aufgerufen werden, während die zu debuggende Komponente in einem synchronisierten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="ad174-111">This method must be called while the debuggee is in a synchronized state.</span></span>  
  
 <span data-ttu-id="ad174-112">Wenn `ppBlockingObjectEnum` ist kein gültiger Zeiger ist, das Ergebnis nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ad174-112">If `ppBlockingObjectEnum` is not a valid pointer, the result is undefined.</span></span>  
  
 <span data-ttu-id="ad174-113">Wenn ein Thread blockiert ist und der Fehler kann nicht bestimmt werden, die Methode gibt ein HRESULT zurück, der Fehler weist darauf hin. Andernfalls wird S_OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ad174-113">If a thread is blocked and the error cannot be determined, the method returns an HRESULT that indicates failure; otherwise, it returns S_OK.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ad174-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad174-114">Requirements</span></span>  
 <span data-ttu-id="ad174-115">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ad174-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ad174-116">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ad174-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ad174-117">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ad174-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ad174-118">**.NET Framework-Versionen:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ad174-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad174-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad174-119">See Also</span></span>  
 [<span data-ttu-id="ad174-120">ICorDebugThread4-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ad174-120">ICorDebugThread4 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread4-interface.md)  
 [<span data-ttu-id="ad174-121">Debugschnittstellen</span><span class="sxs-lookup"><span data-stu-id="ad174-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="ad174-122">Debuggen</span><span class="sxs-lookup"><span data-stu-id="ad174-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)