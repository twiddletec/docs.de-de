---
title: StrongNameGetPublicKeyEx-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRStrongName2.StrongNameGetPublicKeyEx
api_location: mscoree.dll
api_type: COM
f1_keywords: StrongNameGetPublicKeyEx
helpviewer_keywords:
- StrongNameGetPublicKeyEx method, ICLRStrongName2 interface [.NET Framework hosting]
- ICLRStrongName2::StrongNameGetPublicKeyEx method [.NET Framework hosting]
ms.assetid: 63d8260c-fb32-4f8f-a357-768afd570f68
topic_type: apiref
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: f39c5c948d43fd0e9387c1cc0319a46d25ec86ec
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="strongnamegetpublickeyex-method"></a><span data-ttu-id="c8fe3-102">StrongNameGetPublicKeyEx-Methode</span><span class="sxs-lookup"><span data-stu-id="c8fe3-102">StrongNameGetPublicKeyEx Method</span></span>
<span data-ttu-id="c8fe3-103">Ruft den öffentlichen Schlüssel aus einem öffentlichen/privaten Schlüsselpaar und gibt einen Hashalgorithmus und eines Signaturalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-103">Gets the public key from a public/private key pair, and specifies a hash algorithm and a signature algorithm.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c8fe3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8fe3-104">Syntax</span></span>  
  
```  
HRESULT StrongNameGetPublicKey (   
    [in]  LPCWSTR   pwzKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob,  
    [out] BYTE      **ppbPublicKeyBlob,  
    [out] ULONG     *pcbPublicKeyBlob  
    [in]  ULONG     uHashAlgId,  
    [in]  ULONG     uReserved,  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c8fe3-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8fe3-105">Parameters</span></span>  
 `pwzKeyContainer`  
 <span data-ttu-id="c8fe3-106">[in] Der Name des Schlüsselcontainers an, die das öffentlich/privat-Schlüsselpaar enthält.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-106">[in] The name of the key container that contains the public/private key pair.</span></span> <span data-ttu-id="c8fe3-107">Wenn `pbKeyBlob` ist null, `szKeyContainer` müssen einen gültigen Container innerhalb der Kryptografiedienstanbieter (CSP) angeben.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-107">If `pbKeyBlob` is null, `szKeyContainer` must specify a valid container within the cryptographic service provider (CSP).</span></span> <span data-ttu-id="c8fe3-108">In diesem Fall die `StrongNameGetPublicKeyEx` Methode extrahiert den öffentlichen Schlüssel aus dem Schlüsselpaar in dem Container gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-108">In this case, the `StrongNameGetPublicKeyEx` method extracts the public key from the key pair stored in the container.</span></span>  
  
 <span data-ttu-id="c8fe3-109">Wenn `pbKeyBlob` ist ungleich null, das Schlüsselpaar wird davon ausgegangen, dass im Schlüssel binary large Object (BLOB) enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-109">If `pbKeyBlob` is not null, the key pair is assumed to be contained in the key binary large object (BLOB).</span></span>  
  
 <span data-ttu-id="c8fe3-110">Die Schlüssel müssen 1024-Bit-Rivest-Shamir-Adleman (RSA) Signaturschlüssel sein.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-110">The keys must be 1024-bit Rivest-Shamir-Adleman (RSA) signing keys.</span></span> <span data-ttu-id="c8fe3-111">Zu diesem Zeitpunkt werden keine anderen Arten von Schlüsseln unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-111">No other types of keys are supported at this time.</span></span>  
  
 `pbKeyBlob`  
 <span data-ttu-id="c8fe3-112">[in] Ein Zeiger auf das öffentlich/privat-Schlüsselpaar.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-112">[in] A pointer to the public/private key pair.</span></span> <span data-ttu-id="c8fe3-113">Dieses Paar weist das Format, das erstellt wird, durch die Win32- `CryptExportKey` Funktion.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-113">This pair is in the format created by the Win32 `CryptExportKey` function.</span></span> <span data-ttu-id="c8fe3-114">Wenn `pbKeyBlob` null ist, die vom angegebenen Schlüsselcontainer `szKeyContainer` wird davon ausgegangen, dass das Schlüsselpaar enthält.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-114">If `pbKeyBlob` is null, the key container specified by `szKeyContainer` is assumed to contain the key pair.</span></span>  
  
 `cbKeyBlob`  
 <span data-ttu-id="c8fe3-115">[in] Die Größe in Bytes, der `pbKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-115">[in] The size, in bytes, of `pbKeyBlob`.</span></span>  
  
 `ppbPublicKeyBlob`  
 <span data-ttu-id="c8fe3-116">[out] Der zurückgegebene öffentliche Schlüssel BLOB.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-116">[out] The returned public key BLOB.</span></span> <span data-ttu-id="c8fe3-117">Die `ppbPublicKeyBlob` Parameter von der common Language Runtime zugeordnet ist und an den Aufrufer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-117">The `ppbPublicKeyBlob` parameter is allocated by the common language runtime and returned to the caller.</span></span> <span data-ttu-id="c8fe3-118">Der Aufrufer muss den Arbeitsspeicher freigeben, mithilfe der [ICLRStrongName:: StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-118">The caller must free the memory by using the [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) method.</span></span>  
  
 `pcbPublicKeyBlob`  
 <span data-ttu-id="c8fe3-119">[out] Die Größe des BLOB zurückgegebenen öffentlichen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-119">[out] The size of the returned public key BLOB.</span></span>  
  
 `uHashAlgId`  
 <span data-ttu-id="c8fe3-120">[in] Der Hashalgorithmus für die Assembly.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-120">[in] The assembly hash algorithm.</span></span> <span data-ttu-id="c8fe3-121">Finden Sie im Abschnitt "Hinweise" eine Liste der zulässigen Werte.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-121">See the Remarks section for a list of accepted values.</span></span>  
  
 `uReserved`  
 <span data-ttu-id="c8fe3-122">[in] Für die zukünftige Verwendung reserviert. Der Standardwert ist null.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-122">[in] Reserved for future use; defaults to null.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c8fe3-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8fe3-123">Return Value</span></span>  
 <span data-ttu-id="c8fe3-124">`S_OK`Wenn die Methode erfolgreich abgeschlossen. andernfalls ein HRESULT-Wert, der Fehler weist darauf hin (finden Sie unter [häufig auftretende HRESULT-Werte](http://go.microsoft.com/fwlink/?LinkId=213878) eine Liste).</span><span class="sxs-lookup"><span data-stu-id="c8fe3-124">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](http://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c8fe3-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c8fe3-125">Remarks</span></span>  
 <span data-ttu-id="c8fe3-126">Der öffentliche Schlüssel ist Bestandteil einer [PublicKeyBlob](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-126">The public key is contained in a [PublicKeyBlob](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md) structure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c8fe3-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c8fe3-127">Remarks</span></span>  
 <span data-ttu-id="c8fe3-128">Die folgende Tabelle zeigt die Menge der zulässigen Werte für die `uHashAlgId` Parameter.</span><span class="sxs-lookup"><span data-stu-id="c8fe3-128">The following table shows the set of accepted values for the `uHashAlgId` parameter.</span></span>  
  
|<span data-ttu-id="c8fe3-129">Name</span><span class="sxs-lookup"><span data-stu-id="c8fe3-129">Name</span></span>|<span data-ttu-id="c8fe3-130">Wert</span><span class="sxs-lookup"><span data-stu-id="c8fe3-130">Value</span></span>|  
|----------|-----------|  
|<span data-ttu-id="c8fe3-131">Keine</span><span class="sxs-lookup"><span data-stu-id="c8fe3-131">None</span></span>|<span data-ttu-id="c8fe3-132">0</span><span class="sxs-lookup"><span data-stu-id="c8fe3-132">0</span></span>|  
|<span data-ttu-id="c8fe3-133">SHA-1</span><span class="sxs-lookup"><span data-stu-id="c8fe3-133">SHA-1</span></span>|<span data-ttu-id="c8fe3-134">0x8004</span><span class="sxs-lookup"><span data-stu-id="c8fe3-134">0x8004</span></span>|  
|<span data-ttu-id="c8fe3-135">SHA-256</span><span class="sxs-lookup"><span data-stu-id="c8fe3-135">SHA-256</span></span>|<span data-ttu-id="c8fe3-136">0x800c</span><span class="sxs-lookup"><span data-stu-id="c8fe3-136">0x800c</span></span>|  
|<span data-ttu-id="c8fe3-137">SHA-384</span><span class="sxs-lookup"><span data-stu-id="c8fe3-137">SHA-384</span></span>|<span data-ttu-id="c8fe3-138">0x800d</span><span class="sxs-lookup"><span data-stu-id="c8fe3-138">0x800d</span></span>|  
|<span data-ttu-id="c8fe3-139">SHA-512</span><span class="sxs-lookup"><span data-stu-id="c8fe3-139">SHA-512</span></span>|<span data-ttu-id="c8fe3-140">0x800e</span><span class="sxs-lookup"><span data-stu-id="c8fe3-140">0x800e</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c8fe3-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8fe3-141">Requirements</span></span>  
 <span data-ttu-id="c8fe3-142">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c8fe3-142">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c8fe3-143">**Header:** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="c8fe3-143">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="c8fe3-144">**Bibliothek:** als Ressource in MSCorEE.dll enthalten</span><span class="sxs-lookup"><span data-stu-id="c8fe3-144">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c8fe3-145">**.NET Framework-Versionen:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c8fe3-145">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c8fe3-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8fe3-146">See Also</span></span>  
 [<span data-ttu-id="c8fe3-147">StrongNameTokenFromPublicKey-Methode</span><span class="sxs-lookup"><span data-stu-id="c8fe3-147">StrongNameTokenFromPublicKey Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfrompublickey-method.md)  
 [<span data-ttu-id="c8fe3-148">PublicKeyBlob-Struktur</span><span class="sxs-lookup"><span data-stu-id="c8fe3-148">PublicKeyBlob Structure</span></span>](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md)  
 [<span data-ttu-id="c8fe3-149">ICLRStrongName-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c8fe3-149">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)  
 [<span data-ttu-id="c8fe3-150">StrongNameGetPublicKey-Methode</span><span class="sxs-lookup"><span data-stu-id="c8fe3-150">StrongNameGetPublicKey Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetpublickey-method.md)