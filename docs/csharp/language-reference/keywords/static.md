---
title: static (C#-Referenz)
ms.date: 07/20/2015
f1_keywords:
- static
- static_CSharpKeyword
helpviewer_keywords:
- static keyword [C#]
ms.assetid: 5509e215-2183-4da3-bab4-6b7e607a4fdf
ms.openlocfilehash: b7e2981c8832d6ac1744c102d5bde55bbe25c256
ms.sourcegitcommit: 60645077dc4b62178403145f8ef691b13ffec28e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/10/2018
ms.locfileid: "37959984"
---
# <a name="static-c-reference"></a>static (C#-Referenz)
Verwenden Sie den Modifizierer `static`, um einen statischen Member zu deklarieren, der zum Typ selbst gehört, anstatt zu einem bestimmten Objekt. Der Modifizierer `static` kann mit Klassen, Feldern, Methoden, Eigenschaften, Operatoren, Ereignissen und Konstruktoren verwendet werden, jedoch nicht mit Indexern, Finalizern oder Typen außer Klassen. Weitere Informationen finden Sie unter [Statische Klassen und statische Klassenmember](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md).  
  
## <a name="example"></a>Beispiel  
 Die folgende Klasse wird als `static` deklariert und enthält nur `static`-Methoden:  
  
 [!code-csharp[csrefKeywordsModifiers#18](../../../csharp/language-reference/keywords/codesnippet/CSharp/static_1.cs)]  
  
 Die Deklaration einer Konstante oder eines Typs ist implizit ein statischer Member.  
  
 Ein statischer Member kann nicht über eine Instanz verwiesen werden. Stattdessen wird er über den Namen verwiesen. Betrachten Sie beispielsweise die folgende Klasse:  
  
 [!code-csharp[csrefKeywordsModifiers#19](../../../csharp/language-reference/keywords/codesnippet/CSharp/static_2.cs)]  
  
 Verwenden Sie zum Verweisen auf ein statischen Member `x` den vollqualifizierten Namen `MyBaseC.MyStruct.x`, außer es kann auf den Member vom selben Geltungsbereich zugegriffen werden:  
  
```csharp  
Console.WriteLine(MyBaseC.MyStruct.x);  
```  
  
 Während die Instanz einer Klasse eine separate Kopie aller Instanzfelder der Klasse enthält, gibt es nur eine Kopie von jedem statischen Feld.  
  
 Es ist nicht möglich, [this](../../../csharp/language-reference/keywords/this.md) zum Verweis auf statische Methoden oder Eigenschaftenaccessoren zu verwenden.  
  
 Wenn das Schlüsselwort `static` auf eine Klasse angewandt wird, müssen alle Member der Klasse statisch sein.  
  
 Klassen und statische Klassen können über statische Konstruktoren verfügen. Statische Konstruktoren werden irgendwann zwischen Programmstart und Klasseninstanziierung aufgerufen.  
  
> [!NOTE]
>  Die Verwendung des Schlüsselworts `static` ist in C# eingeschränkter als in C++. Vergleiche mit dem C++-Schlüsselwort finden Sie unter [Speicherklassen (C++)](/cpp/cpp/storage-classes-cpp#static).
  
 Stellen Sie sich zur Veranschaulichung von statischen Membern eine Klasse vor, die einen Angestellten eines Unternehmens darstellt. Es wird angenommen, dass die Klasse eine Methode zum Zählen von Angestellten sowie ein Feld enthält, in dem die Anzahl von Angestellten gespeichert wird. Sowohl die Methode als auch das Feld gehören nicht zu einem Instanzangestellten. Sie gehören stattdessen zur Unternehmensklasse. Daher sollten sie als statische Member der Klasse deklariert werden.  
  
## <a name="example"></a>Beispiel  
 In diesem Beispiel wird der Name und die ID eines neuen Angestellten gelesen, der Angestelltenzähler wird um 1 erhöht, und die Informationen zum neuen Angestellten sowie die neue Anzahl von Angestellten wird angezeigt. Der Einfachheit halber liest das Programm die aktuelle Anzahl von Angestellten von der Tastatur. Bei einer realen Anwendung sollten diese Informationen aus einer Datei gelesen werden.  
  
 [!code-csharp[csrefKeywordsModifiers#20](../../../csharp/language-reference/keywords/codesnippet/CSharp/static_3.cs)]  
  
## <a name="example"></a>Beispiel  
 Dieses Beispiel zeigt, dass, obwohl Sie ein statisches Feld mit einem anderen noch nicht deklarierte, statischen Feld initialisieren können, die Ergebnisse undefiniert bleiben, bis Sie dem statischen Feld explizit einen Wert zuweisen.  
  
 [!code-csharp[csrefKeywordsModifiers#21](../../../csharp/language-reference/keywords/codesnippet/CSharp/static_4.cs)]  
  
## <a name="c-language-specification"></a>C#-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Siehe auch  
 [C#-Referenz](../../../csharp/language-reference/index.md)  
 [C#-Programmierhandbuch](../../../csharp/programming-guide/index.md)  
 [C#-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)  
 [Modifizierer](../../../csharp/language-reference/keywords/modifiers.md)  
 [Statische Klassen und statische Klassenmember](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md)
