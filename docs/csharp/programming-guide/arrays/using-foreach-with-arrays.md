---
title: Verwenden von foreach mit Arrays (C#-Programmierhandbuch)
ms.date: 05/23/2018
helpviewer_keywords:
- arrays [C#], foreach
- foreach statement [C#], using with arrays
ms.assetid: 5f2da2a9-1f56-4de5-94cc-e07f4f7a0244
ms.openlocfilehash: b858f35167e24390a729769487ce98908a3d349f
ms.sourcegitcommit: 54231aa56fca059e9297888a96fbca1d4cf3746c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2018
ms.locfileid: "34549454"
---
# <a name="using-foreach-with-arrays-c-programming-guide"></a>Verwenden von foreach mit Arrays (C#-Programmierhandbuch)

Die Anweisung [foreach](../../language-reference/keywords/foreach-in.md) stellt eine einfache, klare Methode bereit, um die Elemente eines Arrays zu durchlaufen.

Bei eindimensionalen Arrays verarbeitet die Anweisung `foreach` Elemente in aufsteigender Indexreihenfolge, beginnend bei Index 0 und endend bei Index `Length - 1`:

[!code-csharp[csProgGuideArrays#28](./codesnippet/CSharp/using-foreach-with-arrays_1.cs)]

Bei mehrdimensionalen Arrays werden Elemente so durchlaufen, dass die Indizes der äußersten rechten Dimension zuerst erhöht werden, dann die der links daneben liegenden Dimension und so weiter, bis die linke Seite erreicht ist:

[!code-csharp[csProgGuideArrays#29](./codesnippet/CSharp/using-foreach-with-arrays_2.cs)]

Bei mehrdimensionalen Arrays haben Sie jedoch eine größere Kontrolle über die Reihenfolge bei der Verarbeitung von Arrayelementen, wenn Sie eine geschachtelte [for](../../language-reference/keywords/for.md)-Schleife verwenden.

## <a name="see-also"></a>Siehe auch  
 <xref:System.Array>  
 [C#-Programmierhandbuch](../index.md)  
 [Arrays](index.md)  
 [Eindimensionale Arrays](single-dimensional-arrays.md)  
 [Mehrdimensionale Arrays](multidimensional-arrays.md)  
 [Verzweigte Arrays](jagged-arrays.md)
