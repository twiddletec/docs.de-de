---
title: -nowarn (C#-Compileroptionen)
ms.date: 07/20/2015
f1_keywords:
- /nowarn
helpviewer_keywords:
- nowarn compiler option [C#]
- /nowarn compiler option [C#]
- -nowarn compiler option [C#]
ms.assetid: 6dcbc5e8-ae67-4566-9df3-f63cfdd9c4e4
ms.openlocfilehash: 1c5e8bc7ad065c4662cd489930b2226e8a4b8962
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33215484"
---
# <a name="-nowarn-c-compiler-options"></a>-nowarn (C#-Compileroptionen)
Mit der Option **-nowarn** können Sie unterdrücken, dass der Compiler eine oder mehrere Warnungen anzeigt. Trennen Sie mehrere Warnnummern durch ein Komma.  
  
## <a name="syntax"></a>Syntax  
  
```console  
-nowarn:number1[,number2,...]  
```  
  
## <a name="arguments"></a>Argumente  
 `number1`, `number2`  
 Warnnummer(n), die der Compiler unterdrücken soll.  
  
## <a name="remarks"></a>Hinweise  
 Sie sollten lediglich den numerischen Teil des Warnungsbezeichners angeben. Wenn Sie z.B. CS0028 unterdrücken wollen, könnten Sie `-nowarn:28` angeben.  
  
 Der Compiler wird automatisch die Warnnummern ignorieren, die an `-nowarn` übergeben wurden und in einer früheren Version gültig waren, jedoch aus dem Compiler entfernt worden sind. CS0679 war z.B. im Compiler in Visual Studio .NET 2002 gültig, wurde aber später entfernt.  
  
 Die folgenden Warnungen können nicht durch die Option `-nowarn` unterdrückt werden.  
  
-   Compilerwarnung (Stufe 1) CS2002  
  
-   Compilerwarnung (Stufe 1) CS2023  
  
-   Compilerwarnung (Stufe 1) CS2029  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Compileroption in der Visual Studio-Entwicklungsumgebung fest  
  
1.  Öffnen Sie die Seite **Eigenschaften** für das Projekt. Informationen finden Sie auf der [Seite „Erstellen“, Projekt-Designer (C#)](/visualstudio/ide/reference/build-page-project-designer-csharp).  
  
2.  Klicken Sie auf die Eigenschaftenseite **Build** .  
  
3.  Ändern Sie die Eigenschaft **Warnungen unterdrücken**.  
  
 Informationen zum programmgesteuerten Festlegen dieser Compileroption finden Sie unter <xref:VSLangProj80.ProjectProperties3.DelaySign%2A>.  
  
## <a name="see-also"></a>Siehe auch  
 [C#-Compileroptionen](../../../csharp/language-reference/compiler-options/index.md)  
 [Verwalten von Projekt- und Projektmappeneigenschaften](/visualstudio/ide/managing-project-and-solution-properties)  
 [C#-Compilerfehler](../../../csharp/language-reference/compiler-messages/index.md)
