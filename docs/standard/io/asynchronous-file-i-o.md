---
title: Asynchrone Datei E-A
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- streams, synchronous streams
- asynchronous I/O
- synchronous I/O
- streams, asynchronous streams
- I/O [.NET Framework], asynchronous I/O
- Stream class, synchronous I/O
- data streams, asynchronous streams
- Stream class, asynchronous I/O
- multiple I/O requests
- data streams, synchronous streams
ms.assetid: dbdd55e7-d6b9-4f9e-8abb-ab0edd4457f7
caps.latest.revision: "23"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: d8a461d79ecdcadc3f880f6a813918cf891abd45
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="asynchronous-file-io"></a><span data-ttu-id="bb0d6-102">Asynchrone Datei-E/A</span><span class="sxs-lookup"><span data-stu-id="bb0d6-102">Asynchronous File I/O</span></span>
<span data-ttu-id="bb0d6-103">Mithilfe von asynchronen Vorgängen können Sie ressourcenintensive E/A-Vorgänge auszuführen, ohne den Hauptthread zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="bb0d6-103">Asynchronous operations enable you to perform resource-intensive I/O operations without blocking the main thread.</span></span> <span data-ttu-id="bb0d6-104">Diese Überlegungen zur Leistung sind insbesondere in einer [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] -App oder [!INCLUDE[desktop_appname](../../../includes/desktop-appname-md.md)] -App wichtig, bei der ein zeitaufwendiger Streamvorgang den UI-Thread blockieren kann und es dann den Anschein hat, dass Ihre App nicht funktioniert.</span><span class="sxs-lookup"><span data-stu-id="bb0d6-104">This performance consideration is particularly important in a [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] app or [!INCLUDE[desktop_appname](../../../includes/desktop-appname-md.md)] app where a time-consuming stream operation can block the UI thread and make your app appear as if it is not working.</span></span>  
  
 <span data-ttu-id="bb0d6-105">Ab [!INCLUDE[net_v45](../../../includes/net-v45-md.md)]enthalten die E/A-Typen asynchrone Methoden, um asynchrone Vorgänge zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="bb0d6-105">Starting with the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)], the I/O types include async methods to simplify asynchronous operations.</span></span> <span data-ttu-id="bb0d6-106">Eine asynchrone Methode enthält `Async` in ihrem Namen, z. B. <xref:System.IO.Stream.ReadAsync%2A>, <xref:System.IO.Stream.WriteAsync%2A>, <xref:System.IO.Stream.CopyToAsync%2A>, <xref:System.IO.Stream.FlushAsync%2A>, <xref:System.IO.TextReader.ReadLineAsync%2A>und <xref:System.IO.TextReader.ReadToEndAsync%2A>.</span><span class="sxs-lookup"><span data-stu-id="bb0d6-106">An async method contains `Async` in its name, such as <xref:System.IO.Stream.ReadAsync%2A>, <xref:System.IO.Stream.WriteAsync%2A>, <xref:System.IO.Stream.CopyToAsync%2A>, <xref:System.IO.Stream.FlushAsync%2A>, <xref:System.IO.TextReader.ReadLineAsync%2A>, and <xref:System.IO.TextReader.ReadToEndAsync%2A>.</span></span> <span data-ttu-id="bb0d6-107">Diese asynchronen Methoden werden für Streamklassen wie <xref:System.IO.Stream>, <xref:System.IO.FileStream>und <xref:System.IO.MemoryStream>sowie für Klassen implementiert, die für das Lesen und das Schreiben in Streams verwendet werden, z. B. <xref:System.IO.TextReader> und <xref:System.IO.TextWriter>.</span><span class="sxs-lookup"><span data-stu-id="bb0d6-107">These async methods are implemented on stream classes, such as <xref:System.IO.Stream>, <xref:System.IO.FileStream>, and <xref:System.IO.MemoryStream>, and on classes that are used for reading from or writing to streams, such <xref:System.IO.TextReader> and <xref:System.IO.TextWriter>.</span></span>  
  
 <span data-ttu-id="bb0d6-108">In .NET Framework 4 und vorherigen Versionen müssen Sie Methoden wie <xref:System.IO.Stream.BeginRead%2A> und <xref:System.IO.Stream.EndRead%2A> verwenden, um asynchrone E/A-Vorgänge zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="bb0d6-108">In the .NET Framework 4 and earlier versions, you have to use methods such as <xref:System.IO.Stream.BeginRead%2A> and <xref:System.IO.Stream.EndRead%2A> to implement asynchronous I/O operations.</span></span> <span data-ttu-id="bb0d6-109">Diese Methoden sind weiterhin verfügbar in [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] , um Legacycode zu unterstützen; allerdings können Sie mithilfe der asynchronen Methoden leichter asynchrone E/A-Vorgänge implementieren.</span><span class="sxs-lookup"><span data-stu-id="bb0d6-109">These methods are still available in the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] to support legacy code; however, the async methods help you implement asynchronous I/O operations more easily.</span></span>  
  
 <span data-ttu-id="bb0d6-110">Ab [!INCLUDE[vs_dev11_long](../../../includes/vs-dev11-long-md.md)]stellt Visual Studio zwei Schlüsselwörter für asynchrone Programmierung bereit:</span><span class="sxs-lookup"><span data-stu-id="bb0d6-110">Starting with [!INCLUDE[vs_dev11_long](../../../includes/vs-dev11-long-md.md)], Visual Studio provides two keywords for asynchronous programming:</span></span>  
  
 <span data-ttu-id="bb0d6-111">Der`Async` -Modifizierer (Visual Basic) bzw. `async` -Modifizierer (C#), der verwendet wird, um eine Methode zu kennzeichnen, die einen asynchronen Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="bb0d6-111">`Async` (Visual Basic) or `async` (C#) modifier, which is used to mark a method that contains an asynchronous operation.</span></span>  
  
 <span data-ttu-id="bb0d6-112">Der`Await` -Operator (Visual Basic) bzw. `await` -Operator (C#), der auf das Ergebnis einer asynchronen Methode angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb0d6-112">`Await` (Visual Basic) or `await` (C#) operator, which is applied to the result of an async method.</span></span>  
  
 <span data-ttu-id="bb0d6-113">Um asynchrone E/A-Vorgänge zu implementieren, verwenden Sie diese Schlüsselwörter in Verbindung mit den asynchronen Methoden, wie in den folgenden Beispielen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="bb0d6-113">To implement asynchronous I/O operations, use these keywords in conjunction with the async methods, as shown in the following examples.</span></span> <span data-ttu-id="bb0d6-114">Weitere Informationen finden Sie unter [Asynchrone Programmierung mit Async und Await](http://msdn.microsoft.com/library/db854f91-ccef-4035-ae4d-0911fde808c7).</span><span class="sxs-lookup"><span data-stu-id="bb0d6-114">For more information, see [Asynchronous Programming with Async and Await](http://msdn.microsoft.com/library/db854f91-ccef-4035-ae4d-0911fde808c7).</span></span>  
  
 <span data-ttu-id="bb0d6-115">Das folgende Beispiel zeigt, wie mithilfe von zwei <xref:System.IO.FileStream> -Objekten Dateien asynchron aus einem Verzeichnis in ein anderes kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="bb0d6-115">The following example demonstrates how to use two <xref:System.IO.FileStream> objects to copy files asynchronously from one directory to another.</span></span> <span data-ttu-id="bb0d6-116">Beachten Sie, dass der <xref:System.Web.UI.WebControls.Button.Click> -Ereignishandler für das <xref:System.Windows.Controls.Button> -Steuerelement mit dem `async` -Modifizierer markiert wird, da er eine asynchrone Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="bb0d6-116">Notice that the <xref:System.Web.UI.WebControls.Button.Click> event handler for the <xref:System.Windows.Controls.Button> control is marked with the `async` modifier because it calls an asynchronous method.</span></span>  
  
 [!code-csharp[Asynchronous_File_IO_async#1](../../../samples/snippets/csharp/VS_Snippets_CLR/Asynchronous_File_IO_async/cs/example.cs#1)]
 [!code-vb[Asynchronous_File_IO_async#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/Asynchronous_File_IO_async/vb/example.vb#1)]  
  
 <span data-ttu-id="bb0d6-117">Das folgende Beispiel ähnelt dem vorherigen, allerdings werden <xref:System.IO.StreamReader> - und <xref:System.IO.StreamWriter> -Objekte verwendet, um den Inhalt einer Textdatei asynchron zu lesen und zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="bb0d6-117">The next example is similar to the previous one but uses <xref:System.IO.StreamReader> and <xref:System.IO.StreamWriter> objects to read and write the contents of a text file asynchronously.</span></span>  
  
 [!code-csharp[Asynchronous_File_IO_async#2](../../../samples/snippets/csharp/VS_Snippets_CLR/Asynchronous_File_IO_async/cs/example2.cs#2)]
 [!code-vb[Asynchronous_File_IO_async#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/Asynchronous_File_IO_async/vb/example2.vb#2)]  
  
 <span data-ttu-id="bb0d6-118">Im folgenden Beispiel werden die Code-Behind-Datei und die XAML-Datei gezeigt, mit denen eine Datei als ein <xref:System.IO.Stream> in einer App [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] geöffnet wird und der Inhalt mithilfe einer Instanz der <xref:System.IO.StreamReader> -Klasse gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="bb0d6-118">The next example shows the code-behind file and the XAML file that are used to open a file as a <xref:System.IO.Stream> in a [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] app, and read its contents by using an instance of the <xref:System.IO.StreamReader> class.</span></span> <span data-ttu-id="bb0d6-119">Im Beispiel werden asynchrone Methoden verwendet, um die Datei als Stream zu öffnen und ihren Inhalt zu lesen.</span><span class="sxs-lookup"><span data-stu-id="bb0d6-119">It uses asynchronous methods to open the file as a stream and to read its contents.</span></span>  
  
 [!code-csharp[System.IO.WindowsRuntimeStorageExtensions#2](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.windowsruntimestorageextensions/cs/blankpage.xaml.cs#2)]
 [!code-vb[System.IO.WindowsRuntimeStorageExtensions#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.windowsruntimestorageextensions/vb/blankpage.xaml.vb#2)]  
  
 [!code-xaml[System.IO.WindowsRuntimeStorageExtensions#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.windowsruntimestorageextensions/cs/blankpage.xaml#1)]  
  
## <a name="see-also"></a><span data-ttu-id="bb0d6-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb0d6-120">See Also</span></span>  
 <xref:System.IO.Stream>  
 [<span data-ttu-id="bb0d6-121">Datei- und Stream-E/A</span><span class="sxs-lookup"><span data-stu-id="bb0d6-121">File and Stream I/O</span></span>](../../../docs/standard/io/index.md)  
 [<span data-ttu-id="bb0d6-122">Asynchrone Programmierung mit Async und Await</span><span class="sxs-lookup"><span data-stu-id="bb0d6-122">Asynchronous Programming with Async and Await</span></span>](http://msdn.microsoft.com/library/db854f91-ccef-4035-ae4d-0911fde808c7)