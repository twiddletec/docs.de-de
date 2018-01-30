---
title: 'Vorgehensweise: Verketten mehrerer Zeichenfolgen (C#-Handbuch)'
description: "Es gibt mehrere Möglichkeiten zum Verketten von Zeichenfolgen in C#. Lernen Sie die Optionen und Gründe für verschiedene Auswahlmöglichkeiten kennen."
ms.date: 01/11/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
helpviewer_keywords:
- joining strings [C#]
- concatenating strings [C#]
- strings [C#], concatenation
ms.assetid: 8e16736f-4096-4f3f-be0f-9d4c3ff63520
caps.latest.revision: 
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: a4bc5e04edba48065746b96841b628ec5843c5e9
ms.sourcegitcommit: f28752eab00d2bd97e971542c0f49ce63cfbc239
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2018
---
# <a name="how-to-concatenate-multiple-strings-c-guide"></a><span data-ttu-id="0119f-104">Vorgehensweise: Verketten mehrerer Zeichenfolgen (C#-Handbuch)</span><span class="sxs-lookup"><span data-stu-id="0119f-104">How to: Concatenate Multiple Strings (C# Guide)</span></span>

<span data-ttu-id="0119f-105">*Verkettung* ist der Prozess, eine Zeichenfolge ans Ende einer anderen Zeichenfolge anzufügen.</span><span class="sxs-lookup"><span data-stu-id="0119f-105">*Concatenation* is the process of appending one string to the end of another string.</span></span> <span data-ttu-id="0119f-106">Sie können Zeichenfolgen mithilfe des +-Operators verketten.</span><span class="sxs-lookup"><span data-stu-id="0119f-106">You concatenate strings by using the + operator.</span></span> <span data-ttu-id="0119f-107">Bei Zeichenfolgenliteralen und Zeichenfolgenkonstanten erfolgt die Verkettung beim Kompilieren. Es erfolgt keine Verkettung zur Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="0119f-107">For string literals and string constants, concatenation occurs at compile time; no run-time concatenation occurs.</span></span> <span data-ttu-id="0119f-108">Bei Zeichenfolgenvariablen erfolgt die Verkettung nur zur Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="0119f-108">For string variables, concatenation occurs only at run time.</span></span>

[!INCLUDE[interactive-note](~/includes/csharp-interactive-note.md)]

<span data-ttu-id="0119f-109">Im folgenden Beispiel wird die Verkettung genutzt, um ein langes Zeichenfolgenliteral in kleinere Zeichenfolgen aufzuteilen, wodurch die Lesbarkeit im Quellcode verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="0119f-109">The following example uses concatenation to split a long string literal into smaller strings in order to improve readability in the source code.</span></span> <span data-ttu-id="0119f-110">Diese Teile werden zur Kompilierzeit in eine einzelne Zeichenfolge verkettet.</span><span class="sxs-lookup"><span data-stu-id="0119f-110">These parts will be concatenated into a single string at compile time.</span></span> <span data-ttu-id="0119f-111">Es entstehen unabhängig von der Anzahl an Zeichenfolgen keine Leistungseinbußen zur Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="0119f-111">There is no run-time performance cost regardless of the number of strings involved.</span></span>  
  
 [!code-csharp-interactive[Combining strings at compile time](../../../samples/snippets/csharp/how-to/strings/Concatenate.cs#1)]  
  

<span data-ttu-id="0119f-112">Zum Verketten von Zeichenfolgenvariablen können Sie die Operatoren `+` bzw. `+=`, die [Zeichenfolgeninterpolation](../tutorials/string-interpolation.md) oder die Methoden <xref:System.String.Concat%2A?displayProperty=nameWithType>, <xref:System.String.Format%2A?displayProperty=nameWithType> oder <xref:System.Text.StringBuilder.Append%2A?displayProperty=nameWithType> verwenden.</span><span class="sxs-lookup"><span data-stu-id="0119f-112">To concatenate string variables, you can use the `+` or `+=` operators, [string interpolation](../tutorials/string-interpolation.md) or the <xref:System.String.Concat%2A?displayProperty=nameWithType>, <xref:System.String.Format%2A?displayProperty=nameWithType> or <xref:System.Text.StringBuilder.Append%2A?displayProperty=nameWithType> methods.</span></span> <span data-ttu-id="0119f-113">Der Operator `+` ist einfach zu verwenden und gut für intuitiv verständlichen Code geeignet.</span><span class="sxs-lookup"><span data-stu-id="0119f-113">The `+` operator is easy to use and makes for intuitive code.</span></span> <span data-ttu-id="0119f-114">Auch wenn Sie mehrere +-Operatoren in einer Anweisung verwenden, wird der Inhalt der Zeichenfolge nur einmal kopiert.</span><span class="sxs-lookup"><span data-stu-id="0119f-114">Even if you use several + operators in one statement, the string content is copied only once.</span></span> <span data-ttu-id="0119f-115">Der folgende Code zeigt zwei Beispiele zur Verwendung des `+`-Operators zum Verketten von Zeichenfolgen:</span><span class="sxs-lookup"><span data-stu-id="0119f-115">The following code shows two examples of using the `+` operator to concatenate strings:</span></span>

[!code-csharp-interactive[combining strings using +](../../../samples/snippets/csharp/how-to/strings/Concatenate.cs#2)]  

<span data-ttu-id="0119f-116">In einigen Ausdrücken ist es einfacher, Zeichenfolgen mithilfe der Zeichenfolgeninterpolation zu verketten, wie in folgendem Beispiel gezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="0119f-116">In some expressions, it is easier to concatenate strings using string interpolation, as the following code shows:</span></span>
  
[!code-csharp-interactive[building strings using string interpolation](../../../samples/snippets/csharp/how-to/strings/Concatenate.cs#3)]  
  
> [!NOTE]
>  <span data-ttu-id="0119f-117">Bei der Zeichenfolgenverkettung behandelt der C#-Compiler eine NULL-Zeichenfolge wie eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0119f-117">In string concatenation operations, the C# compiler treats a null string the same as an empty string.</span></span>

<span data-ttu-id="0119f-118">Andere Methoden zum Verketten von Zeichenfolgen sind <xref:System.String.Concat%2A?displayProperty=nameWithType> und <xref:System.String.Format%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="0119f-118">Other methods to concatenate strings are <xref:System.String.Concat%2A?displayProperty=nameWithType> and <xref:System.String.Format%2A?displayProperty=nameWithType>.</span></span> <span data-ttu-id="0119f-119">Diese Methoden funktionieren gut, wenn Sie eine Zeichenfolge mit einer kleinen Anzahl von Zeichenfolgenkomponenten erstellen.</span><span class="sxs-lookup"><span data-stu-id="0119f-119">These methods work well when you are building a string from a small number of component strings.</span></span> <span data-ttu-id="0119f-120">Diese Methoden sind auch gut geeignet, wenn Sie die Anzahl der Zeichenfolgen, die Ihre verkettete Zeichenfolge ergeben, kennen.</span><span class="sxs-lookup"><span data-stu-id="0119f-120">These methdos are also a great choice when you know the number of strings that make up your concatenated string.</span></span>

<span data-ttu-id="0119f-121">In anderen Fällen kann es passieren, dass Sie Zeichenfolgen in einer Schleife kombinieren, bei der Sie nicht wissen, wie viele Quellzeichenfolgen Sie kombinieren, und die tatsächliche Anzahl an Quellzeichenfolgen kann in solchen Fällen sehr groß sein.</span><span class="sxs-lookup"><span data-stu-id="0119f-121">In other cases you may be combining strings in a loop, where you don't know how many source strings you are combining, and the actual number of source strings may be quite large.</span></span> <span data-ttu-id="0119f-122">Für solche Szenarios wurde die Klasse <xref:System.Text.StringBuilder> entwickelt.</span><span class="sxs-lookup"><span data-stu-id="0119f-122">The <xref:System.Text.StringBuilder> class was designed for these scenarios.</span></span> <span data-ttu-id="0119f-123">Im folgenden Code werden Zeichenfolgen mit der Methode <xref:System.Text.StringBuilder.Append%2A> der Klasse <xref:System.Text.StringBuilder> verkettet.</span><span class="sxs-lookup"><span data-stu-id="0119f-123">The following code uses the <xref:System.Text.StringBuilder.Append%2A> method of the <xref:System.Text.StringBuilder> class to concatenate strings.</span></span>  
  
[!code-csharp-interactive[string concatenation using string builder](../../../samples/snippets/csharp/how-to/strings/Concatenate.cs#4)]  

<span data-ttu-id="0119f-124">Erfahren Sie mehr über die [Gründe für das Verketten von Zeichenfolgen oder die `StringBuilder`-Klasse](xref:System.Text.StringBuilder#StringAndSB)</span><span class="sxs-lookup"><span data-stu-id="0119f-124">You can read more about the [reasons to choose string concatenation or the `StringBuilder` class](xref:System.Text.StringBuilder#StringAndSB)</span></span>

<span data-ttu-id="0119f-125">Eine weitere Option zum Verketten von Zeichenfolgen aus einer Sammlung ist die Verwendung von [LINQ](../programming-guide/concepts/linq/index.md) und der Methode <xref:System.Linq.Enumerable.Aggregate%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="0119f-125">Another option to join strings from a collection is to use [LINQ](../programming-guide/concepts/linq/index.md) and the <xref:System.Linq.Enumerable.Aggregate%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="0119f-126">Diese Methode kombiniert die Quellzeichenfolgen mithilfe eines Lambdaausdrucks.</span><span class="sxs-lookup"><span data-stu-id="0119f-126">This method combines the source strings using a lambda expression.</span></span> <span data-ttu-id="0119f-127">Der Lambdaausdruck fügt jede Zeichenfolge der vorhandenen Akkumulation zu.</span><span class="sxs-lookup"><span data-stu-id="0119f-127">The lambda expression does the work to add each string to the existing accumulation.</span></span> <span data-ttu-id="0119f-128">Im folgenden Beispiel wird ein Array von Worten kombiniert, indem zwischen jedem Wort im Array Leerzeichen hinzugefügt werden:</span><span class="sxs-lookup"><span data-stu-id="0119f-128">The following example combines an array of words by adding a space between each word in the array:</span></span>

[!code-csharp-interactive[string concatenation using LINQ expressions](../../../samples/snippets/csharp/how-to/strings/Concatenate.cs#5)]  


## <a name="see-also"></a><span data-ttu-id="0119f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0119f-129">See Also</span></span>  
 <xref:System.String>  
 <xref:System.Text.StringBuilder>  
 [<span data-ttu-id="0119f-130">C#-Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="0119f-130">C# Programming Guide</span></span>](../programming-guide/index.md)  
 [<span data-ttu-id="0119f-131">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="0119f-131">Strings</span></span>](../programming-guide/strings/index.md)