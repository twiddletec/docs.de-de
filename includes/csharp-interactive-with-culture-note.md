
> [!NOTE]
> <span data-ttu-id="7bf95-101">Die C#-Beispiele in diesem Artikel werden in der Inlinecodeausführung und dem Playground von [Try.NET](https://try.dot.net) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7bf95-101">The C# examples in this article run in the [Try.NET](https://try.dot.net) inline code runner and playground.</span></span> <span data-ttu-id="7bf95-102">Klicken Sie auf die Schaltfläche **Ausführen**, um ein Beispiel in einem interaktiven Fenster auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7bf95-102">Select the **Run** button to run an example in an interactive window.</span></span> <span data-ttu-id="7bf95-103">Nachdem Sie den Code ausgeführt haben, können Sie ihn ändern und den geänderten Code durch erneutes Anklicken der Schaltfläche **Ausführen** ausführen.</span><span class="sxs-lookup"><span data-stu-id="7bf95-103">Once you execute the code, you can modify it and run the modified code by selecting **Run** again.</span></span> <span data-ttu-id="7bf95-104">Der geänderte Code wird entweder im interaktiven Fenster ausgeführt, oder das interaktive Fenster zeigt alle C#-Compilerfehlermeldungen an, wenn die Kompilierung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="7bf95-104">The modified code either runs in the interactive window or, if compilation fails, the interactive window displays all C# compiler error messages.</span></span> 
>  
> <span data-ttu-id="7bf95-105">Die [aktuelle Kultur](xref:System.Globalization.CultureInfo.CurrentCulture) von [Try.NET](https://try.dot.net)-Inlinecodeausführung und Playground ist die [invariante Kultur](xref:System.Globalization.CultureInfo.InvariantCulture).</span><span class="sxs-lookup"><span data-stu-id="7bf95-105">The [current culture](xref:System.Globalization.CultureInfo.CurrentCulture) of the [Try.NET](https://try.dot.net) inline code runner and playground is the [invariant culture](xref:System.Globalization.CultureInfo.InvariantCulture).</span></span> <span data-ttu-id="7bf95-106">Daher unterscheidet sich die Ausgabe der Inlinecodeausführung von der Ausgabe, die von Beispielen angezeigt wird, die eine Standardkultur als aktuelle Kultur verwenden.</span><span class="sxs-lookup"><span data-stu-id="7bf95-106">As a result, the output produced by the inline code runner differs from the output displayed by examples that use a default culture as the current culture.</span></span> 
>
> <span data-ttu-id="7bf95-107">Sie können diese Einschränkung umgehen, indem Sie wie im Folgenden eine Codezeile hinzufügen, um die invariante Kultur festzulegen: `System.Globalization.CultureInfo.CurrentCulture = new System.Globalization.CultureInfo("en-US");` ersetzen Sie `en-US` mit der invarianten Kultur, die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bf95-107">You can work around this limitation by adding a line of code like the following to set the culture: `System.Globalization.CultureInfo.CurrentCulture = new System.Globalization.CultureInfo("en-US");` Just replace `en-US` with the name of the culture that you'd like to be the current culture.</span></span>

