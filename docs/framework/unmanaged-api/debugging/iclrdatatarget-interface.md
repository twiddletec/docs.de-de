---
title: ICLRDataTarget-Schnittstelle
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRDataTarget
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICLRDataTarget
helpviewer_keywords: ICLRDataTarget interface [.NET Framework debugging]
ms.assetid: e2f05155-9bef-4e11-b703-7f05890665ca
topic_type: apiref
caps.latest.revision: "14"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 6a40276b28f3d20428f0d7eb0556a762fdb56801
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="iclrdatatarget-interface"></a><span data-ttu-id="56872-102">ICLRDataTarget-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="56872-102">ICLRDataTarget Interface</span></span>
<span data-ttu-id="56872-103">Stellt Methoden für die Interaktion mit einem Zielelement der common Language Runtime (CLR) bereit.</span><span class="sxs-lookup"><span data-stu-id="56872-103">Provides methods for interaction with a target item of the common language runtime (CLR).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="56872-104">Methoden</span><span class="sxs-lookup"><span data-stu-id="56872-104">Methods</span></span>  
  
|<span data-ttu-id="56872-105">Methode</span><span class="sxs-lookup"><span data-stu-id="56872-105">Method</span></span>|<span data-ttu-id="56872-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56872-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="56872-107">GetCurrentThreadID-Methode</span><span class="sxs-lookup"><span data-stu-id="56872-107">GetCurrentThreadID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-getcurrentthreadid-method.md)|<span data-ttu-id="56872-108">Ruft den Bezeichner des Betriebssystems für den aktuellen Thread ab.</span><span class="sxs-lookup"><span data-stu-id="56872-108">Gets the operating system identifier for the current thread.</span></span>|  
|[<span data-ttu-id="56872-109">GetImageBase-Methode</span><span class="sxs-lookup"><span data-stu-id="56872-109">GetImageBase Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-getimagebase-method.md)|<span data-ttu-id="56872-110">Ruft die Basis Speicheradresse für das angegebene Bild ab.</span><span class="sxs-lookup"><span data-stu-id="56872-110">Gets the base memory address for the specified image.</span></span>|  
|[<span data-ttu-id="56872-111">GetMachineType-Methode</span><span class="sxs-lookup"><span data-stu-id="56872-111">GetMachineType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-getmachinetype-method.md)|<span data-ttu-id="56872-112">Ruft einen Bezeichner für die Art der Anweisungssatz, der der Zielprozess verwendet.</span><span class="sxs-lookup"><span data-stu-id="56872-112">Gets an identifier for the kind of instruction set that the target process is using.</span></span>|  
|[<span data-ttu-id="56872-113">GetPointerSize-Methode</span><span class="sxs-lookup"><span data-stu-id="56872-113">GetPointerSize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-getpointersize-method.md)|<span data-ttu-id="56872-114">Ruft die Größe in Bytes, der einen Zeiger auf das aktuelle Ziel an.</span><span class="sxs-lookup"><span data-stu-id="56872-114">Gets the size, in bytes, of a pointer to the current target.</span></span>|  
|[<span data-ttu-id="56872-115">GetThreadContext-Methode</span><span class="sxs-lookup"><span data-stu-id="56872-115">GetThreadContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-getthreadcontext-method.md)|<span data-ttu-id="56872-116">Ruft einen Zeiger auf den Kontext des Threads mit dem angegebenen Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="56872-116">Gets a pointer to the context of the thread with the specified identifier.</span></span>|  
|[<span data-ttu-id="56872-117">GetTLSValue-Methode</span><span class="sxs-lookup"><span data-stu-id="56872-117">GetTLSValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-gettlsvalue-method.md)|<span data-ttu-id="56872-118">Ruft einen Wert im lokalen Threadspeicher (TLS) am angegebenen Index für den angegebenen Thread ab.</span><span class="sxs-lookup"><span data-stu-id="56872-118">Gets a value in thread local storage (TLS) at the specified index for the specified thread.</span></span>|  
|[<span data-ttu-id="56872-119">ReadVirtual-Methode</span><span class="sxs-lookup"><span data-stu-id="56872-119">ReadVirtual Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-readvirtual-method.md)|<span data-ttu-id="56872-120">Liest Daten aus der angegebenen virtuellen Speicheradresse in den angegebenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="56872-120">Reads data from the specified virtual memory address into the specified buffer.</span></span>|  
|[<span data-ttu-id="56872-121">Request-Methode</span><span class="sxs-lookup"><span data-stu-id="56872-121">Request Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-request-method.md)|<span data-ttu-id="56872-122">Wird von der common Language Runtime (CLR) Daten Access Services zum Anfordern eines Vorgangs aufgerufen, wie durch die Implementierung definiert.</span><span class="sxs-lookup"><span data-stu-id="56872-122">Called by the common language runtime (CLR) data access services to request an operation, as defined by the implementation.</span></span>|  
|[<span data-ttu-id="56872-123">SetThreadContext-Methode</span><span class="sxs-lookup"><span data-stu-id="56872-123">SetThreadContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-setthreadcontext-method.md)|<span data-ttu-id="56872-124">Legt den aktuellen Kontext des angegebenen Threads im Zielprozess.</span><span class="sxs-lookup"><span data-stu-id="56872-124">Sets the current context of the specified thread in the target process.</span></span>|  
|[<span data-ttu-id="56872-125">SetTLSValue-Methode</span><span class="sxs-lookup"><span data-stu-id="56872-125">SetTLSValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-settlsvalue-method.md)|<span data-ttu-id="56872-126">Legt einen Wert in den lokalen Threadspeicher (TLS) des angegebenen Threads im Zielprozess.</span><span class="sxs-lookup"><span data-stu-id="56872-126">Sets a value in the thread local storage (TLS) of the specified thread in the target process.</span></span>|  
|[<span data-ttu-id="56872-127">WriteVirtual-Methode</span><span class="sxs-lookup"><span data-stu-id="56872-127">WriteVirtual Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-writevirtual-method.md)|<span data-ttu-id="56872-128">Schreibt Daten aus dem angegebenen Puffer auf die angegebene virtuelle Speicheradresse.</span><span class="sxs-lookup"><span data-stu-id="56872-128">Writes data from the specified buffer to the specified virtual memory address.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="56872-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="56872-129">Remarks</span></span>  
 <span data-ttu-id="56872-130">Der API-Client (d. h. der Debugger) muss diese Schnittstelle für die jeweiligen Zielelement geeigneten Form implementieren.</span><span class="sxs-lookup"><span data-stu-id="56872-130">The API client (that is, the debugger) must implement this interface as appropriate for the particular target item.</span></span> <span data-ttu-id="56872-131">So hätte ein Liveprozess z. B. eine andere Implementierung als ein Speicherabbild.</span><span class="sxs-lookup"><span data-stu-id="56872-131">For example, a live process would have an implementation different from that of a memory dump.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="56872-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56872-132">Requirements</span></span>  
 <span data-ttu-id="56872-133">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="56872-133">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="56872-134">**Header:** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="56872-134">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="56872-135">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="56872-135">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="56872-136">**.NET Framework-Versionen:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="56872-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="56872-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56872-137">See Also</span></span>  
 [<span data-ttu-id="56872-138">ICLRDataTarget2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="56872-138">ICLRDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md)  
 [<span data-ttu-id="56872-139">Debugschnittstellen</span><span class="sxs-lookup"><span data-stu-id="56872-139">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)