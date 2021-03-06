---
title: 'How to: Query for Sentences that Contain a Specified Set of Words (LINQ) (C#) (Gewusst wie: Abfragen von Sätzen, die bestimmte Wörter enthalten (LINQ) (C#))'
ms.date: 07/20/2015
ms.assetid: 0724b429-4b87-4d26-a7b1-409358f3fc20
ms.openlocfilehash: 736078ccf97ba3e61748932c3e48fb436b2c5564
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33319883"
---
# <a name="how-to-query-for-sentences-that-contain-a-specified-set-of-words-linq-c"></a>How to: Query for Sentences that Contain a Specified Set of Words (LINQ) (C#) (Gewusst wie: Abfragen von Sätzen, die bestimmte Wörter enthalten (LINQ) (C#))
Dieses Beispiel zeigt, wie Sie Sätze in einer Textdatei suchen, die Übereinstimmungen für jedes Wort einer bestimmten Gruppe von Wörtern enthält. Obwohl das Array von Suchbegriffen in diesem Beispiel hartcodiert ist, kann es auch zur Laufzeit dynamisch aufgefüllt werden. In diesem Beispiel gibt die Abfrage die Sätze zurück, die die Wörter „Historically“ (ursprünglich), „data“ (Daten) und „integrated“ (integriert) enthalten.  
  
## <a name="example"></a>Beispiel  
  
```csharp  
class FindSentences  
{  
    static void Main()  
    {  
        string text = @"Historically, the world of data and the world of objects " +  
        @"have not been well integrated. Programmers work in C# or Visual Basic " +  
        @"and also in SQL or XQuery. On the one side are concepts such as classes, " +  
        @"objects, fields, inheritance, and .NET Framework APIs. On the other side " +  
        @"are tables, columns, rows, nodes, and separate languages for dealing with " +  
        @"them. Data types often require translation between the two worlds; there are " +  
        @"different standard functions. Because the object world has no notion of query, a " +  
        @"query can only be represented as a string without compile-time type checking or " +  
        @"IntelliSense support in the IDE. Transferring data from SQL tables or XML trees to " +  
        @"objects in memory is often tedious and error-prone.";  
  
        // Split the text block into an array of sentences.  
        string[] sentences = text.Split(new char[] { '.', '?', '!' });  
  
        // Define the search terms. This list could also be dynamically populated at runtime.  
        string[] wordsToMatch = { "Historically", "data", "integrated" };  
  
        // Find sentences that contain all the terms in the wordsToMatch array.  
        // Note that the number of terms to match is not specified at compile time.  
        var sentenceQuery = from sentence in sentences  
                            let w = sentence.Split(new char[] { '.', '?', '!', ' ', ';', ':', ',' },  
                                                    StringSplitOptions.RemoveEmptyEntries)  
                            where w.Distinct().Intersect(wordsToMatch).Count() == wordsToMatch.Count()  
                            select sentence;  
  
        // Execute the query. Note that you can explicitly type  
        // the iteration variable here even though sentenceQuery  
        // was implicitly typed.   
        foreach (string str in sentenceQuery)  
        {  
            Console.WriteLine(str);  
        }  
  
        // Keep the console window open in debug mode.  
        Console.WriteLine("Press any key to exit");  
        Console.ReadKey();  
    }  
}  
/* Output:  
Historically, the world of data and the world of objects have not been well integrated  
*/  
```  
  
 Die Abfrage funktioniert, indem der Text zuerst in Sätze aufgeteilt wird. Diese Sätze werden wiederum in ein Array von Zeichenfolgen aufgeteilt, das jedes Wort enthält. Für jedes dieser Arrays entfernt die <xref:System.Linq.Enumerable.Distinct%2A>-Methode alle Wortduplikate, und anschließend führt die Abfrage einen <xref:System.Linq.Enumerable.Intersect%2A>-Vorgang für das Wortarray und das `wordsToMatch`-Array durch. Wenn die Anzahl der Schnittmenge identisch mit der Anzahl des `wordsToMatch`-Arrays ist, werden alle gefundenen Wörter in den Wörtern und der ursprüngliche Satz zurückgegeben.  
  
 Im Aufruf von <xref:System.String.Split%2A> werden die Satzzeichen als Trennlinien verwendet, damit sie aus der Zeichenfolge entfernt werden können. Wenn Sie dies nicht getan haben, haben Sie z.B. eine „ursprüngliche“ Zeichenfolge, die „usprünglich“ nicht mit dem `wordsToMatch`-Array übereinstimmen würde. Sie müssen möglicherweise zusätzliche Trennzeichen verwenden, abhängig von den Satzzeichen, die im Quelltext vorkommen.  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Erstellen Sie ein neues Projekt, das auf die .NET Framework-Version 3.5 oder höher ausgelegt ist, mit einer Referenz zu System.Core.dll und `using`-Direktiven für System.Linq- und System.IO-Namespaces.  
  
## <a name="see-also"></a>Siehe auch  
 [LINQ und Zeichenfolgen (C#)](../../../../csharp/programming-guide/concepts/linq/linq-and-strings.md)
