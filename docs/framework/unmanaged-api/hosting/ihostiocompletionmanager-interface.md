---
title: IHostIoCompletionManager-Schnittstelle
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager
helpviewer_keywords:
- IHostIoCompletionManager interface [.NET Framework hosting]
ms.assetid: c28d1983-83f7-46e2-990f-dbb9dc07c818
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 194dcec6ea484e9cd2d3a17093c1eceb16c8f6c9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33440215"
---
# <a name="ihostiocompletionmanager-interface"></a>IHostIoCompletionManager-Schnittstelle
Enthält Methoden, die die common Language Runtime (CLR) für die Interaktion mit e/a-Abschlussports vom Host zu ermöglichen.  
  
## <a name="methods"></a>Methoden  
  
|Methode|Beschreibung|  
|------------|-----------------|  
|[Bind-Methode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-bind-method.md)|Bindet ein Handle eines e/a-Abschlussanschlusses an.|  
|[CloseIoCompletionPort-Methode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-closeiocompletionport-method.md)|Schließt einen Port, der durch einen früheren Aufruf erstellten `CreateIoCompletionPort`.|  
|[CreateIoCompletionPort-Methode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-createiocompletionport-method.md)|Fordert an, dass der Host eine neue e/a-Abschlussport erstellen.|  
|[GetAvailableThreads-Methode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-getavailablethreads-method.md)|Ruft die Anzahl der e/a-Abschlussthreads, die derzeit keine Anforderungen verarbeiten.|  
|[GetHostOverlappedSize-Methode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-gethostoverlappedsize-method.md)|Ruft die Größe der benutzerdefinierten Daten, die der Host beabsichtigt, um e/a-Anforderungen angefügt werden soll.|  
|[GetMaxThreads-Methode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-getmaxthreads-method.md)|Ruft die maximale Anzahl von Threads, die der Host reserviert werden soll, kann e/a-Anforderungen.|  
|[GetMinThreads-Methode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-getminthreads-method.md)|Ruft die minimale Anzahl von Threads, die vom Host bereitgestellten e/a-Anforderungen.|  
|[InitializeHostOverlapped-Methode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-initializehostoverlapped-method.md)|Stellt den Host eine Möglichkeit, benutzerdefinierte Daten über eine e/a-Anforderung zu initialisieren.|  
|[SetCLRIoCompletionManager-Methode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-setclriocompletionmanager-method.md)|Ermöglicht den Host einen Schnittstellenzeiger auf eine [ICLRIoCompletionManager](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-interface.md) Instanz, die von der CLR implementiert.|  
|[SetMaxThreads-Methode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-setmaxthreads-method.md)|Legt die maximale Anzahl von Threads, die der Host-Bereitstellung für e/a-Anforderungen fest.|  
|[SetMinThreads-Methode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-setminthreads-method.md)|Legt die Mindestanzahl von Threads, die der Host reserviert werden soll, sollte auf e/a-Abschluss fest.|  
  
## <a name="remarks"></a>Hinweise  
 `IHostIoCompletionManager` entspricht der `ICLRIoCompletionManager` Schnittstelle, die von der CLR implementiert. Die CLR ruft die Methoden der `IHostIoCompletionManager` Handles an den Ports binden, die der Host bietet, und der Host Ruft die Methoden der `ICLRIoCompletionManager` um den Abschluss von e/a-Anforderungen zu melden.  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** MSCorEE.h  
  
 **Bibliothek:** als Ressource in MSCorEE.dll enthalten  
  
 **.NET Framework-Versionen:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch  
 [Hosten von Schnittstellen](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
