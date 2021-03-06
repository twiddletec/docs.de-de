---
title: '&#39;&lt;Membername&gt; &#39; kann nicht verfügbar machen &#39; &lt;Typename&gt; &#39; außerhalb des Projekts durch &lt;Containertype&gt; &#39; &lt;Containertypename&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- bc30909
- vbc30909
helpviewer_keywords:
- BC30909
ms.assetid: ffa7395d-e182-4087-8ce8-079810fdae54
ms.openlocfilehash: 36add48ebee2d1804921eeeec0b59cdd4cbafecc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33588092"
---
# <a name="39ltmembernamegt39-cannot-expose-type-39lttypenamegt39-outside-the-project-through-ltcontainertypegt-39ltcontainertypenamegt39"></a>&#39;&lt;Membername&gt; &#39; kann nicht verfügbar machen &#39; &lt;Typename&gt; &#39; außerhalb des Projekts durch &lt;Containertype&gt; &#39; &lt;Containertypename&gt;&#39;
Eine Variable, Prozedurparameter oder Funktionsrückgabe wird außerhalb des zugehörigen Containers verfügbar gemacht, aber es ist deklariert, als ein Typ, der außerhalb des Containers nicht verfügbar gemacht werden muss.  
  
 Die folgenden Codegerüst zeigt eine Situation, die diesen Fehler generiert.  
  
```  
Private Class privateClass  
End Class  
Public Class mainClass  
    Public exposedVar As New privateClass  
End Class  
```  
  
 Ein Typ, der deklariert wird `Protected`, `Friend`, `Protected Friend`, oder `Private` soll beschränkten Zugriff außerhalb seines Deklarationskontexts haben. Die Daten unter widerspricht Typ einer Variablen mit weniger eingeschränktem Zugriff diesen Zweck. Im vorangehenden Code Skelett `exposedVar` ist `Public` und Verfügbarmachen von würde `privateClass` an Code, der keinen Zugriff darauf haben sollten.  
  
 **Fehler-ID:** BC30909  
  
## <a name="to-correct-this-error"></a>So beheben Sie diesen Fehler  
  
-   Ändern Sie die Zugriffsebene der Variablen, Parameter der Prozedur oder Funktion zurück, um mindestens so restriktiv wie die Zugriffsebene für die Angabe des Datentyps werden.  
  
## <a name="see-also"></a>Siehe auch  
 [Zugriffsebenen in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
