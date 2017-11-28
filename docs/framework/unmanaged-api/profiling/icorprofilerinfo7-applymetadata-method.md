---
title: ICorProfilerInfo7::ApplyMetaData-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: cpp
api_name: ICorProfilerInfo7.ApplyMetaData
api_location: mscorwks.dll
api_type: COM
ms.assetid: a1bfb649-4584-4d35-b3e6-8fe59b53992a
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: e3724555df58392e5ab59ccb4f52dd2de860b8d4
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilerinfo7applymetadata-method"></a><span data-ttu-id="fdf1b-102">ICorProfilerInfo7::ApplyMetaData-Methode</span><span class="sxs-lookup"><span data-stu-id="fdf1b-102">ICorProfilerInfo7::ApplyMetaData Method</span></span>
<span data-ttu-id="fdf1b-103">[Wird nur in .NET Framework 4.6.1 und höheren Versionen unterstützt]</span><span class="sxs-lookup"><span data-stu-id="fdf1b-103">[Supported in the .NET Framework 4.6.1 and later versions]</span></span>  
  
 <span data-ttu-id="fdf1b-104">Wendet die neu definierte von Metadaten der `IMetadataEmit::Define*` Methoden, um ein angegebenes Modul.</span><span class="sxs-lookup"><span data-stu-id="fdf1b-104">Applies the metadata newly defined by the `IMetadataEmit::Define*` methods to a specified module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fdf1b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdf1b-105">Syntax</span></span>  
  
```cpp
HRESULT ApplyMetaData(  
        [in] ModuleID moduleID  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fdf1b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdf1b-106">Parameters</span></span>  
 `moduleID`  
 <span data-ttu-id="fdf1b-107">[in] Der Bezeichner des Moduls, dessen Metadaten geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="fdf1b-107">[in] The identifier of the module whose metadata was changed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fdf1b-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fdf1b-108">Remarks</span></span>  
 <span data-ttu-id="fdf1b-109">Wenn Metadaten-Änderungen vorgenommen werden, nach der [ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) Rückruf, müssen Sie diese Methode aufrufen, bevor Sie die neue Metadaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="fdf1b-109">If metadata changes are made after the [ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) callback, you must call this method before using the new metadata.</span></span>  
  
 <span data-ttu-id="fdf1b-110">`ApplyMetaData`unterstützt nur die folgenden Arten von Metadaten hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="fdf1b-110">`ApplyMetaData` only supports adding the following types of metadata:</span></span>  
  
-   <span data-ttu-id="fdf1b-111">`AssemblyRef`Datensätze, die Sie, durch Aufrufen Erstellen der [IMetaDataAssemblyEmit:: DefineAssemblyRef](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineassemblyref-method.md).</span><span class="sxs-lookup"><span data-stu-id="fdf1b-111">`AssemblyRef` records, which you create by calling the [IMetaDataAssemblyEmit::DefineAssemblyRef](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineassemblyref-method.md).</span></span> <span data-ttu-id="fdf1b-112">-Methode.</span><span class="sxs-lookup"><span data-stu-id="fdf1b-112">method.</span></span>  
  
-   <span data-ttu-id="fdf1b-113">`TypeRef`Datensätze, die Sie, durch Aufrufen Erstellen der [IMetaDataEmit:: DefineTypeRefByName](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definetyperefbyname-method.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="fdf1b-113">`TypeRef` records, which you create by calling the [IMetaDataEmit::DefineTypeRefByName](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definetyperefbyname-method.md) method.</span></span>  
  
-   <span data-ttu-id="fdf1b-114">`TypeSpec`Datensätze, die Sie, durch Aufrufen Erstellen der [IMetaDataEmit:: GetTokenFromTypeSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-gettokenfromtypespec-method.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="fdf1b-114">`TypeSpec` records, which you create by calling the [IMetaDataEmit::GetTokenFromTypeSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-gettokenfromtypespec-method.md) method.</span></span>  
  
-   <span data-ttu-id="fdf1b-115">`MemberRef`Datensätze, die Sie, durch Aufrufen Erstellen der [DefineMemberRef](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definememberref-method.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="fdf1b-115">`MemberRef` records, which you create by calling the [IMetaDataEmit::DefineMemberRef](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definememberref-method.md) method.</span></span>  
  
-   <span data-ttu-id="fdf1b-116">`MemberSpec`Datensätze, die Sie, durch Aufrufen Erstellen der [IMetaDataEmit2:: DefineMethodSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definemethodspec-method.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="fdf1b-116">`MemberSpec` records, which you create by calling the [IMetaDataEmit2::DefineMethodSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definemethodspec-method.md) method.</span></span>  
  
-   <span data-ttu-id="fdf1b-117">`UserString`Datensätze, die Sie, durch Aufrufen Erstellen der [IMetaDataEmit:: DefineUserString](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineuserstring-method.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="fdf1b-117">`UserString` records, which you create by calling the [IMetaDataEmit::DefineUserString](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineuserstring-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fdf1b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fdf1b-118">Requirements</span></span>  
 <span data-ttu-id="fdf1b-119">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fdf1b-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fdf1b-120">**Header:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fdf1b-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fdf1b-121">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fdf1b-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fdf1b-122">**.NET Framework-Versionen:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fdf1b-122">**.NET Framework Versions:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fdf1b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fdf1b-123">See Also</span></span>  
 [<span data-ttu-id="fdf1b-124">ICorProfilerInfo7-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fdf1b-124">ICorProfilerInfo7 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-interface.md)