---
title: IMetaDataTables2::GetMetaDataStorage-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataTables2.GetMetaDataStorage
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataTables2::GetMetaDataStorage
helpviewer_keywords:
- GetMetaDataStorage method [.NET Framework metadata]
- IMetaDataTables2::GetMetaDataStorage method [.NET Framework metadata]
ms.assetid: 667a6d1e-753d-4ea2-8fd8-a8337d1bb9cd
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 8b86542a55c0b4e778dfd956961f5a14a1c9d6f4
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="imetadatatables2getmetadatastorage-method"></a><span data-ttu-id="487d8-102">IMetaDataTables2::GetMetaDataStorage-Methode</span><span class="sxs-lookup"><span data-stu-id="487d8-102">IMetaDataTables2::GetMetaDataStorage Method</span></span>
<span data-ttu-id="487d8-103">Ruft die Größe und den Inhalt der Metadaten in den angegebenen Abschnitt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="487d8-103">Gets the size and contents of the metadata stored in the specified section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="487d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="487d8-104">Syntax</span></span>  
  
```  
HRESULT GetMetaDataStorage (  
   [in, out] const void   **ppvMd,  
   [out] ULONG   *pcbMd  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="487d8-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="487d8-105">Parameters</span></span>  
 `ppvMd`  
 <span data-ttu-id="487d8-106">[in, out] Ein Zeiger auf einen Metadatenabschnitt.</span><span class="sxs-lookup"><span data-stu-id="487d8-106">[in, out] A pointer to a metadata section.</span></span>  
  
 `pcbMd`  
 <span data-ttu-id="487d8-107">[out] Die Größe des Datenstroms Metadaten.</span><span class="sxs-lookup"><span data-stu-id="487d8-107">[out] The size of the metadata stream.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="487d8-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="487d8-108">Requirements</span></span>  
 <span data-ttu-id="487d8-109">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="487d8-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="487d8-110">**Header:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="487d8-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="487d8-111">**Bibliothek:** als Ressource in MsCorEE.dll verwendet</span><span class="sxs-lookup"><span data-stu-id="487d8-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="487d8-112">**.NET Framework-Versionen:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="487d8-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="487d8-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="487d8-113">See Also</span></span>  
 [<span data-ttu-id="487d8-114">IMetaDataTables2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="487d8-114">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)  
 [<span data-ttu-id="487d8-115">IMetaDataTables-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="487d8-115">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)