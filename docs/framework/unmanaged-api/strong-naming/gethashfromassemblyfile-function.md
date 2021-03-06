---
title: GetHashFromAssemblyFile-Funktion
ms.date: 03/30/2017
api_name:
- GetHashFromAssemblyFile
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromAssemblyFile
helpviewer_keywords:
- GetHashFromAssemblyFile function [.NET Framework strong naming]
ms.assetid: 751ed69f-b7ab-4e07-80de-e17ca9319b0c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5e9c0abcd395caf09ebe11e060a4b922e78ad1e6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33457931"
---
# <a name="gethashfromassemblyfile-function"></a>GetHashFromAssemblyFile-Funktion
Ruft einen Hash der angegebenen Assemblydatei, die mithilfe des angegebenen Hashalgorithmus ab.  
  
 Diese Funktion ist veraltet. Verwenden der [ICLRStrongName:: GetHashFromAssemblyFile](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfile-method.md) Methode stattdessen.  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT GetHashFromAssemblyFile (  
    [in]  LPCSTR   szFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE     *pbHash,  
    [in]  DWORD    cchHash,  
    [out] DWORD    *pchHash  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `szFilePath`  
 [in] Der Pfad zu der Datei, der Hashwert berechnet werden soll.  
  
 `piHashAlg`  
 [in, out] Eine Konstante, die den Hashalgorithmus angibt. Verwenden Sie 0 (null), für die Standard-Hash-Algorithmus.  
  
 `pbHash`  
 [out] Der zurückgegebene Hashpuffer.  
  
 `cchHash`  
 [in] Die angeforderte maximale Größe der `pbHash`.  
  
 `pchHash`  
 [out] Die Größe in Bytes, der zurückgegebenen `pbHash`.  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** StrongName.h  
  
 **Bibliothek:** als Ressource in MsCorEE.dll enthalten  
  
 **.NET Framework-Versionen:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch  
 [GetHashFromAssemblyFile-Methode](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfile-method.md)  
 [GetHashFromAssemblyFileW-Methode](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfilew-method.md)  
 [ICLRStrongName-Schnittstelle](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
