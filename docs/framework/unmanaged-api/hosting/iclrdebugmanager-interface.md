---
title: ICLRDebugManager-Schnittstelle
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRDebugManager
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRDebugManager
helpviewer_keywords: ICLRDebugManager interface [.NET Framework hosting]
ms.assetid: e835062c-c7d6-4945-8a44-2de7ebf3928e
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 0e537b955524f2721868ddf5da9fccf68f9d4efd
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2017
---
# <a name="iclrdebugmanager-interface"></a><span data-ttu-id="f79be-102">ICLRDebugManager-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f79be-102">ICLRDebugManager Interface</span></span>
<span data-ttu-id="f79be-103">Enthält Methoden, mit die einen Host eine Reihe von Aufgaben mit einem Bezeichner und einen Anzeigenamen zuordnen können.</span><span class="sxs-lookup"><span data-stu-id="f79be-103">Provides methods that allow a host to associate a set of tasks with an identifier and a friendly name.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f79be-104">Methoden</span><span class="sxs-lookup"><span data-stu-id="f79be-104">Methods</span></span>  
  
|<span data-ttu-id="f79be-105">Methode</span><span class="sxs-lookup"><span data-stu-id="f79be-105">Method</span></span>|<span data-ttu-id="f79be-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f79be-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f79be-107">BeginConnection-Methode</span><span class="sxs-lookup"><span data-stu-id="f79be-107">BeginConnection Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-beginconnection-method.md)|<span data-ttu-id="f79be-108">Wird eine neue Verbindung zwischen dem Host und den Debugger, einen Bezeichner und einen Anzeigenamen Aufgaben zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f79be-108">Establishes a new connection between the host and the debugger to associate tasks with an identifier and a friendly name.</span></span>|  
|[<span data-ttu-id="f79be-109">EndConnection-Methode</span><span class="sxs-lookup"><span data-stu-id="f79be-109">EndConnection Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-endconnection-method.md)|<span data-ttu-id="f79be-110">Entfernt die Zuordnung zwischen einer Liste von Aufgaben und einen Bezeichner und einen Anzeigenamen ein.</span><span class="sxs-lookup"><span data-stu-id="f79be-110">Removes the association between a list of tasks and an identifier and a friendly name.</span></span>|  
|[<span data-ttu-id="f79be-111">GetDacl-Methode</span><span class="sxs-lookup"><span data-stu-id="f79be-111">GetDacl Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-getdacl-method.md)|<span data-ttu-id="f79be-112">Diese Methode ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f79be-112">This method is not implemented.</span></span>|  
|[<span data-ttu-id="f79be-113">IsDebuggerAttached-Methode</span><span class="sxs-lookup"><span data-stu-id="f79be-113">IsDebuggerAttached Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-isdebuggerattached-method.md)|<span data-ttu-id="f79be-114">Ruft einen Wert ab, der angibt, ob ein Debugger an den Prozess angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="f79be-114">Gets a value that indicates whether a debugger is attached to the process.</span></span>|  
|[<span data-ttu-id="f79be-115">SetConnectionTasks-Methode</span><span class="sxs-lookup"><span data-stu-id="f79be-115">SetConnectionTasks Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setconnectiontasks-method.md)|<span data-ttu-id="f79be-116">Ordnet eine Liste der [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) Instanzen einen Bezeichner und einen Anzeigenamen ein.</span><span class="sxs-lookup"><span data-stu-id="f79be-116">Associates a list of [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instances with an identifier and a friendly name.</span></span>|  
|[<span data-ttu-id="f79be-117">SetDacl-Methode</span><span class="sxs-lookup"><span data-stu-id="f79be-117">SetDacl Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setdacl-method.md)|<span data-ttu-id="f79be-118">Diese Methode ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f79be-118">This method is not implemented.</span></span>|  
|[<span data-ttu-id="f79be-119">SetSymbolReadingPolicy-Methode</span><span class="sxs-lookup"><span data-stu-id="f79be-119">SetSymbolReadingPolicy Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setsymbolreadingpolicy-method.md)|<span data-ttu-id="f79be-120">Legt die Richtlinie zum Lesen der Programmdatenbankdateien (PDB).</span><span class="sxs-lookup"><span data-stu-id="f79be-120">Sets the policy for reading program database (PDB) files.</span></span> <span data-ttu-id="f79be-121">Die Richtlinie bestimmt, ob Informationen zu Zeilennummern und Dateien in Aufruflisten enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f79be-121">The policy determines whether information about line numbers and files is included in call stacks.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f79be-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f79be-122">Remarks</span></span>  
 <span data-ttu-id="f79be-123">Debugszenarios beschrieben, kann ein Host zum Gruppieren von Aufgaben gemäß seiner eigenen Programmierlogik möchte.</span><span class="sxs-lookup"><span data-stu-id="f79be-123">In debugging scenarios, a host might want to group tasks according to its own programming logic.</span></span> <span data-ttu-id="f79be-124">Eine Gruppierung erlauben zum Beispiel ein Entwickler sehen nur die Aufgaben der Entwickler-APIs anstelle jede Aufgabe, die im Prozess ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f79be-124">For example, a grouping would allow a developer to see only the tasks required by the developer's APIs, instead of seeing every task running in the process.</span></span> <span data-ttu-id="f79be-125">`ICLRDebugManager`ermöglicht dem Host, um diese Art der Gruppierung zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="f79be-125">`ICLRDebugManager` allows the host to implement this kind of grouping.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="f79be-126">Drei `ICLRDebugManager` Methoden `BeginConnection`, `SetConnectionTasks` und `EndConnection`, voneinander abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="f79be-126">Three `ICLRDebugManager` methods, `BeginConnection`, `SetConnectionTasks` and `EndConnection`, are dependent upon each other.</span></span> <span data-ttu-id="f79be-127">Sie müssen in der angegebenen Reihenfolge erwartungsgemäßen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f79be-127">They must be called in the given order to work as expected.</span></span>  
  
 <span data-ttu-id="f79be-128">Haben die Gruppierung und die Bezeichner und den Anzeigenamen, die mit der Gruppierung der Host weist keine Bedeutung für die common Language Runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="f79be-128">The grouping, and the identifiers and friendly names that the host assigns to the grouping, have no meaning for the common language runtime (CLR).</span></span> <span data-ttu-id="f79be-129">Die CLR übergibt lediglich die Informationen an dem Debugger.</span><span class="sxs-lookup"><span data-stu-id="f79be-129">The CLR merely passes the information along to the debugger.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f79be-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f79be-130">Requirements</span></span>  
 <span data-ttu-id="f79be-131">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f79be-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f79be-132">**Header:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f79be-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f79be-133">**Bibliothek:** als Ressource in MSCorEE.dll enthalten</span><span class="sxs-lookup"><span data-stu-id="f79be-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f79be-134">**.NET Framework-Versionen:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f79be-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f79be-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f79be-135">See Also</span></span>  
 [<span data-ttu-id="f79be-136">Hosten von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f79be-136">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)