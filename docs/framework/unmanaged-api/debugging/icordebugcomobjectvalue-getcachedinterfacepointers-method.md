---
title: ICorDebugComObjectValue::GetCachedInterfacePointers-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugComObjectValue::GetCachedInterfacePointers
api_location: mscordbi.dll
f1_keywords: ICorDebugComObjectValue::GetCachedInterfacePointers
helpviewer_keywords:
- ICorDebugComObjectValue::GetCachedInterfacePointers method [.NET Framework debugging]
- GetCachedInterfacePointers method, ICorDebugComObjectValue interface [.NET Framework debugging]
ms.assetid: 08dbd558-bd39-4263-94c2-71e70687aaf0
topic_type: apiref
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 607300d6b46f3ee20545c50872b99df483b1614c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugcomobjectvaluegetcachedinterfacepointers-method"></a><span data-ttu-id="5bbd2-102">ICorDebugComObjectValue::GetCachedInterfacePointers-Methode</span><span class="sxs-lookup"><span data-stu-id="5bbd2-102">ICorDebugComObjectValue::GetCachedInterfacePointers Method</span></span>
<span data-ttu-id="5bbd2-103">Ruft den unformatierten Schnittstellenzeiger, der auf den aktuellen Runtime callable Wrapper (RCW) zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="5bbd2-103">Gets the raw interface pointers cached on the current runtime callable wrapper (RCW).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5bbd2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bbd2-104">Syntax</span></span>  
  
```  
HRESULT GetCachedInterfacePointers(  
    [in] BOOL bIInspectableOnly,  
    [in] ULONG32 celt,  
    [out] ULONG32 *pceltFetched,  
    [out, size_is(celt), length_is(*pceltFetched) CORDB_ADDRESS *ptrs);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5bbd2-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bbd2-105">Parameters</span></span>  
 `bIInspectableOnly`  
 <span data-ttu-id="5bbd2-106">[in] Ein Wert, der angibt, ob die Methode nur zurückliefert [!INCLUDE[wrt](../../../../includes/wrt-md.md)] Schnittstellen (`IInspectable` Schnittstellen) oder alle COM-Schnittstellen, die von den Runtime callable Wrapper (RCW) zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="5bbd2-106">[in] A value that indicates whether the method will return only [!INCLUDE[wrt](../../../../includes/wrt-md.md)] interfaces (`IInspectable` interfaces) or all COM interfaces that are cached by the runtime callable wrapper (RCW).</span></span>  
  
 `celt`  
 <span data-ttu-id="5bbd2-107">[in] Die Anzahl der Objekte, deren Adressen sind abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5bbd2-107">[in] The number of objects whose addresses are to be retrieved.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="5bbd2-108">[out] Ein Zeiger auf die Anzahl der `CORDB_ADDRESS` Rückgabewerte, die tatsächlich `ptrs`.</span><span class="sxs-lookup"><span data-stu-id="5bbd2-108">[out] A pointer to the number of `CORDB_ADDRESS` values actually returned in `ptrs`.</span></span>  
  
 `ptrs`  
 <span data-ttu-id="5bbd2-109">Ein Zeiger auf die Startadresse eines Arrays von `CORDB_ADDRESS` zwischengespeicherte Benutzeroberflächenobjekte Werte, die die Adressen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5bbd2-109">A pointer to the starting address of an array of `CORDB_ADDRESS` values that contain the addresses of cached interface objects.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5bbd2-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5bbd2-110">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5bbd2-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bbd2-111">Requirements</span></span>  
 <span data-ttu-id="5bbd2-112">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5bbd2-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5bbd2-113">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5bbd2-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5bbd2-114">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5bbd2-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5bbd2-115">**.NET Framework-Versionen:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5bbd2-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5bbd2-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bbd2-116">See Also</span></span>  
 [<span data-ttu-id="5bbd2-117">ICorDebugComObjectValue-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5bbd2-117">ICorDebugComObjectValue Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcomobjectvalue-interface.md)  
 [<span data-ttu-id="5bbd2-118">Debugschnittstellen</span><span class="sxs-lookup"><span data-stu-id="5bbd2-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)