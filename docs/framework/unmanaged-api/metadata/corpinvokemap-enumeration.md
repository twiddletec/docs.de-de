---
title: CorPinvokeMap-Enumeration
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorPinvokeMap
api_location: mscoree.dll
api_type: COM
f1_keywords: CorPinvokeMap
helpviewer_keywords: CorPinvokeMap enumeration [.NET Framework metadata]
ms.assetid: f14f986e-f6ce-42bc-aa23-18150c46d28c
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 9c6e1a49d18cde768884ab3d92eaa6593e2955c0
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2017
---
# <a name="corpinvokemap-enumeration"></a><span data-ttu-id="8b660-102">CorPinvokeMap-Enumeration</span><span class="sxs-lookup"><span data-stu-id="8b660-102">CorPinvokeMap Enumeration</span></span>
<span data-ttu-id="8b660-103">Gibt Optionen für PInvoke-Aufrufs.</span><span class="sxs-lookup"><span data-stu-id="8b660-103">Specifies options for a PInvoke call.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8b660-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b660-104">Syntax</span></span>  
  
```  
typedef enum  CorPinvokeMap {  
  
    pmNoMangle          = 0x0001,  
  
    pmCharSetMask       = 0x0006,  
    pmCharSetNotSpec    = 0x0000,  
    pmCharSetAnsi       = 0x0002,  
    pmCharSetUnicode    = 0x0004,  
    pmCharSetAuto       = 0x0006,  
  
    pmBestFitUseAssem   = 0x0000,  
    pmBestFitEnabled    = 0x0010,  
    pmBestFitDisabled   = 0x0020,  
    pmBestFitMask       = 0x0030,  
  
    pmThrowOnUnmappableCharUseAssem   = 0x0000,  
    pmThrowOnUnmappableCharEnabled    = 0x1000,  
    pmThrowOnUnmappableCharDisabled   = 0x2000,  
    pmThrowOnUnmappableCharMask       = 0x3000,  
  
    pmSupportsLastError = 0x0040,   
  
    pmCallConvMask      = 0x0700,  
    pmCallConvWinapi    = 0x0100,  
    pmCallConvCdecl     = 0x0200,  
    pmCallConvStdcall   = 0x0300,  
    pmCallConvThiscall  = 0x0400,  
    pmCallConvFastcall  = 0x0500,  
  
    pmMaxValue          = 0xFFFF  
  
} CorPinvokeMap;  
```  
  
## <a name="members"></a><span data-ttu-id="8b660-105">Member</span><span class="sxs-lookup"><span data-stu-id="8b660-105">Members</span></span>  
  
|<span data-ttu-id="8b660-106">Member</span><span class="sxs-lookup"><span data-stu-id="8b660-106">Member</span></span>|<span data-ttu-id="8b660-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b660-107">Description</span></span>|  
|------------|-----------------|  
|`pmNoMangle`|<span data-ttu-id="8b660-108">Verwenden Sie alle Elementnamen, wie angegeben.</span><span class="sxs-lookup"><span data-stu-id="8b660-108">Use each member name as specified.</span></span>|  
|`pmCharSetMask`|<span data-ttu-id="8b660-109">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="8b660-109">Reserved.</span></span>|  
|`pmCharSetNotSpec`|<span data-ttu-id="8b660-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="8b660-110">Reserved.</span></span>|  
|`pmCharSetAnsi`|<span data-ttu-id="8b660-111">Marshallen von Zeichenfolgen als Zeichenfolgen mit mehreren Byte-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8b660-111">Marshal strings as multiple-byte character strings.</span></span>|  
|`pmCharSetUnicode`|<span data-ttu-id="8b660-112">Marshallen von Zeichenfolgen als Unicode-2-Byte-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8b660-112">Marshal strings as Unicode 2-byte characters.</span></span>|  
|`pmCharSetAuto`|<span data-ttu-id="8b660-113">Zeichenfolgen für DSA zielbetriebsystem entsprechend automatisch zu marshallen.</span><span class="sxs-lookup"><span data-stu-id="8b660-113">Automatically marshal strings appropriately for the target operating system.</span></span> <span data-ttu-id="8b660-114">Der Standardwert ist Unicode unter Windows NT, Windows 2000, Windows XP und Windows Server 2003-Produktfamilie. Die Standardeinstellung ist, d. h. ANSI unter Windows 98 und Windows Me.</span><span class="sxs-lookup"><span data-stu-id="8b660-114">The default is Unicode on Windows NT, Windows 2000, Windows XP, and the Windows Server 2003 family; the default is ANSI on Windows 98 and Windows Me.</span></span>|  
|`pmBestFitUseAssem`|<span data-ttu-id="8b660-115">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="8b660-115">Reserved.</span></span>|  
|`pmBestFitEnabled`|<span data-ttu-id="8b660-116">Führen Sie die Zuordnung mit ähnlichen Zeichen von Unicode-Zeichen, die eine genaue Übereinstimmung in der ANSI-Zeichensatz hat.</span><span class="sxs-lookup"><span data-stu-id="8b660-116">Perform best-fit mapping of Unicode characters that lack an exact match in the ANSI character set.</span></span>|  
|`pmBestFitDisabled`|<span data-ttu-id="8b660-117">Führen Sie keine Zuordnung mit ähnlichen Zeichen von Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8b660-117">Do not perform best-fit mapping of Unicode characters.</span></span> <span data-ttu-id="8b660-118">In diesem Fall werden alle zuzuordnenden Zeichen durch ersetzt ein "?".</span><span class="sxs-lookup"><span data-stu-id="8b660-118">In this case, all unmappable characters will be replaced by a ‘?’.</span></span>|  
|`pmBestFitMask`|<span data-ttu-id="8b660-119">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="8b660-119">Reserved.</span></span>|  
|`pmThrowOnUnmappableCharUseAssem`|<span data-ttu-id="8b660-120">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="8b660-120">Reserved.</span></span>|  
|`pmThrowOnUnmappableCharEnabled`|<span data-ttu-id="8b660-121">Eine Ausnahme stößt der Interop-Marshaller ein Zeichen nicht zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8b660-121">Throw an exception when the interop marshaler encounters an unmappable character.</span></span>|  
|`pmThrowOnUnmappableCharDisabled`|<span data-ttu-id="8b660-122">Stößt der Interop-Marshaller ein zuzuordnendes Zeichen keine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8b660-122">Do not throw an exception when the interop marshaler encounters an unmappable character.</span></span>|  
|`pmThrowOnUnmappableCharMask`|<span data-ttu-id="8b660-123">Reserviert</span><span class="sxs-lookup"><span data-stu-id="8b660-123">Reserved</span></span>|  
|`pmSupportsLastError`|<span data-ttu-id="8b660-124">Ermöglicht es dem aufgerufenen zum Aufrufen von Win32 `SetLastError` Funktion vor der Rückgabe von die attributierte Methode.</span><span class="sxs-lookup"><span data-stu-id="8b660-124">Allow the callee to call the Win32 `SetLastError` function before returning from the attributed method.</span></span>|  
|`pmCallConvMask`|<span data-ttu-id="8b660-125">Reserviert</span><span class="sxs-lookup"><span data-stu-id="8b660-125">Reserved</span></span>|  
|`pmCallConvWinapi`|<span data-ttu-id="8b660-126">Verwenden Sie die Standardplattform Aufrufkonvention.</span><span class="sxs-lookup"><span data-stu-id="8b660-126">Use the default platform calling convention.</span></span> <span data-ttu-id="8b660-127">Unter Windows ist die Standardeinstellung `StdCall` und auf Windows CE .NET ist `Cdecl`.</span><span class="sxs-lookup"><span data-stu-id="8b660-127">For example, on Windows the default is `StdCall` and on Windows CE .NET it is `Cdecl`.</span></span>|  
|`pmCallConvCdecl`|<span data-ttu-id="8b660-128">Verwenden der `Cdecl` Aufrufkonvention.</span><span class="sxs-lookup"><span data-stu-id="8b660-128">Use the `Cdecl` calling convention.</span></span> <span data-ttu-id="8b660-129">In diesem Fall löscht der Aufrufer den Stapel.</span><span class="sxs-lookup"><span data-stu-id="8b660-129">In this case, the caller cleans the stack.</span></span> <span data-ttu-id="8b660-130">Aufrufende von Funktionen mit dadurch `varargs` (d. h. Funktionen, die eine Variable Anzahl von Parametern akzeptieren).</span><span class="sxs-lookup"><span data-stu-id="8b660-130">This enables calling functions with `varargs` (that is, functions that accept a variable number of parameters).</span></span>|  
|`pmCallConvStdcall`|<span data-ttu-id="8b660-131">Verwenden der `StdCall` Aufrufkonvention.</span><span class="sxs-lookup"><span data-stu-id="8b660-131">Use the `StdCall` calling convention.</span></span> <span data-ttu-id="8b660-132">In diesem Fall entleert der aufgerufene den Stapel.</span><span class="sxs-lookup"><span data-stu-id="8b660-132">In this case, the callee cleans the stack.</span></span> <span data-ttu-id="8b660-133">Dies ist die Standardkonvention für das Aufrufen von nicht verwalteten Funktionen mit Plattformaufruf.</span><span class="sxs-lookup"><span data-stu-id="8b660-133">This is the default convention for calling unmanaged functions with platform invoke.</span></span>|  
|`pmCallConvThiscall`|<span data-ttu-id="8b660-134">Verwenden der `ThisCall` Aufrufkonvention.</span><span class="sxs-lookup"><span data-stu-id="8b660-134">Use the `ThisCall` calling convention.</span></span> <span data-ttu-id="8b660-135">Der erste Parameter in diesem Fall ist die `this` Zeiger und in ECX-Register gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="8b660-135">In this case, the first parameter is the `this` pointer and is stored in register ECX.</span></span> <span data-ttu-id="8b660-136">Andere Parameter werden auf dem Stapel abgelegt.</span><span class="sxs-lookup"><span data-stu-id="8b660-136">Other parameters are pushed on the stack.</span></span> <span data-ttu-id="8b660-137">Die `ThisCall` -Aufrufkonvention wird zum Aufrufen von Methoden für Klassen, die aus einer nicht verwalteten DLL exportiert.</span><span class="sxs-lookup"><span data-stu-id="8b660-137">The `ThisCall` calling convention is used to call methods on classes exported from an unmanaged DLL.</span></span>|  
|`pmCallConvFastcall`|<span data-ttu-id="8b660-138">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="8b660-138">Reserved.</span></span>|  
|`pmMaxValue`|<span data-ttu-id="8b660-139">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="8b660-139">Reserved.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="8b660-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b660-140">Requirements</span></span>  
 <span data-ttu-id="8b660-141">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8b660-141">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8b660-142">**Header:** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="8b660-142">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="8b660-143">**.NET Framework-Versionen:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8b660-143">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b660-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b660-144">See Also</span></span>  
 [<span data-ttu-id="8b660-145">Metadatenenumerationen</span><span class="sxs-lookup"><span data-stu-id="8b660-145">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)