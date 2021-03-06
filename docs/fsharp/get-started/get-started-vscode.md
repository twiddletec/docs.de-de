---
title: Erste Schritte mit f# in Visual Studio Code
description: Erfahren Sie, wie Sie f# mit Visual Studio Code und Ionide-Plug-Ins Suite verwenden.
ms.date: 05/28/2018
ms.openlocfilehash: 1afe985a4fe73d18b1e47b071b119c15a4672022
ms.sourcegitcommit: 59b51cd7c95c75be85bd6ef715e9ef8c85720bac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2018
ms.locfileid: "37874350"
---
# <a name="get-started-with-f-in-visual-studio-code"></a>Erste Schritte mit f# in Visual Studio Code

Können Sie f# in schreiben [Visual Studio Code](https://code.visualstudio.com) mit der [Ionide-Plug-Ins](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp) um plattformübergreifende, einfache (Integrated Development Environment, IDE) Erfahrung mit IntelliSense und basic-Code zu erhalten. Refactorings. Besuchen Sie [Ionide.io](http://ionide.io) Weitere Informationen zu den-Plug-in.

Um zu beginnen, stellen Sie sicher, dass man [f# und Ionide-Plug-in ordnungsgemäß installiert](install-fsharp.md#install-f-with-visual-studio-code).

## <a name="creating-your-first-project-with-ionide"></a>Erstellen Ihres ersten Projekts mit Ionide

Um ein neues F#-Projekt zu erstellen, öffnen Sie Visual Studio Code in einem neuen Ordner (Sie können diese Namen beliebig).

Öffnen Sie als Nächstes den Befehl dem vorgangsergebnis (**Ansicht >-Befehl dem Vorgangsergebnis**) und geben Sie Folgendes:

```
> F# new project
```

Dieser Vorgang beruht die [FÄLSCHEN](https://github.com/fsharp-editing/Forge) Projekt.

> [!NOTE]
Wenn Sie Vorlagenoptionen für die nicht angezeigt wird, versuchen Sie es Aktualisieren von Vorlagen mithilfe des folgenden Befehls in der Befehlspalette: `>F#: Refresh Project Templates`.

Wählen Sie durch Drücken von "f#: New Project" **EINGABETASTE**. Dadurch gelangen Sie mit dem nächsten Schritt, die für das Auswählen einer Projektvorlage.

Wählen Sie die `classlib` Vorlage und Trefferanzahl **EINGABETASTE**.

Wählen Sie als Nächstes ein Verzeichnis zum Erstellen des Projekts in ein. Wenn Sie sie leer lassen, wird das aktuelle Verzeichnis verwendet.

Zum Schluss benennen Sie Ihr Projekt im letzten Schritt an. F#-verwendet [Pascal-Schreibweise](http://c2.com/cgi/wiki?PascalCase) für Projektnamen. In diesem Artikel wird `ClassLibraryDemo` als Namen. Wenn Sie den Namen eingegeben haben, für das Projekt erstellt werden sollen, drücken Sie **EINGABETASTE**.

Wenn Sie den vorherigen Schritt ausgeführt haben, erhalten Sie Visual Studio Code-Arbeitsbereich auf der linken Seite mit den folgenden angezeigt:

1. Der F#-Projekt selbst, darunter die `ClassLibraryDemo` Ordner.
2. Zum Hinzufügen von Paketen über die richtige Verzeichnisstruktur [ `Paket` ](https://fsprojects.github.io/Paket/).
3. Eine plattformübergreifende Buildskript mit [ `FAKE` ](https://fsharp.github.io/FAKE/).
4. Die `paket.exe` ausführbare Datei, Abrufen von Paketen und Abhängigkeiten für Sie beheben kann.
5. Ein `.gitignore` Datei, wenn Sie dieses Projekt zur quellcodeverwaltung im Git-basierte hinzufügen möchten.

## <a name="writing-some-code"></a>Schreiben von code

Öffnen der *ClassLibraryDemo* Ordner.  Daraufhin sollte die folgenden Dateien:

1. `ClassLibraryDemo.fs`, eine F#-Implementierungsdatei mit einer definierten Klasse.
2. `ClassLibraryDemo.fsproj`, eine F#-Projektdatei verwendet, um das Projekt zu erstellen.
3. `Script.fsx`, eine F#-Skriptdatei, die von der Quelldatei geladen.
4. `paket.references`, ein Paket-Abhängigkeits-Datei, die die Abhängigkeiten des Projekts angibt.

Open `Script.fsx`, und fügen Sie den folgenden Code am Ende des Zertifikats:

[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/to-pig-latin.fsx)]

Diese Funktion konvertiert ein Wort in eine Form der [Pig Latin](https://en.wikipedia.org/wiki/Pig_Latin). Der nächste Schritt ist mit f# Interactive (FSI) ausgewertet.

Markieren Sie die gesamte Funktion (es sollte 11 Zeilen lang sein). Sobald er hervorgehoben wird, enthalten die **Alt** Schlüssel, und klicken Sie auf **EINGABETASTE**. Sehen Sie ein Fenster angezeigt werden, unten, und es sollte etwa wie folgt angezeigt:

![Beispiel für f# Interactive-Ausgabe mit Ionide](media/getting-started-vscode/vscode-fsi.png)

In diesem Fall drei Dinge:

1. Es werden die FSI-Prozess wurde gestartet.
2. Sie haben den markierten Code über den Prozess FSI gesendet.
3. Der Prozess FSI ausgewertet den Code, dem Sie über gesendet.

Da war gesendeten über eine [Funktion](../language-reference/functions/index.md), Sie können nun Aufrufen dieser Funktion mit FSI! Geben Sie im interactive-Fenster Folgendes ein:

```fsharp
toPigLatin "banana";;
```

Daraufhin sollte das folgende Ergebnis:

```fsharp
val it : string = "ananabay"
```

Jetzt testen wir ein Vokal als den ersten Buchstaben. Geben Sie Folgendes ein:

```fsharp
toPigLatin "apple";;
```

Daraufhin sollte das folgende Ergebnis:

```fsharp
val it : string = "appleyay"
```

Die Funktion wird wie erwartet funktioniert. Herzlichen Glückwunsch, Sie einfach Ihre erste F#-Funktion in Visual Studio Code geschrieben, und es mit FSI ausgewertet.

>[!NOTE]
Wie Sie möglicherweise bemerkt haben, werden die Zeilen in FSI mit beendet `;;`. Dies ist da FSI mehrere Zeilen eingeben kann. Die `;;` können Sie am Ende FSI wissen, wann der Code beendet wurde.

## <a name="explaining-the-code"></a>Erläutern den code

Wenn Sie nicht sicher sind, zu der Code tatsächlich Wozu dient, wird eine detaillierte Anleitung.

Wie Sie sehen können, `toPigLatin` ist eine Funktion, die ein Wort als Eingabe und konvertiert es in ein Pig-Latin-Darstellung des Begriffs. Die Regeln für diese sind wie folgt aus:

Wenn das erste Zeichen in einem Wort mit einem Vokal beginnt, fügen Sie am Ende des Worts "juhu" hinzu. Wenn sie mit einem Vokal nicht startet, wird verschieben Sie dem ersten Zeichen am Ende des Worts zu, und fügen Sie "Weg" hinzu.

Sie haben möglicherweise im FSI Folgendes festgestellt:

```fsharp
val toPigLatin : word:string -> string
```

Dies gibt an, dass `toPigLatin` ist eine Funktion, die in akzeptiert eine `string` als Eingabe (namens `word`), und wird ein anderes `string`. Dies bezeichnet man als den [der Typsignatur der Funktion](https://fsharpforfunandprofit.com/posts/function-signatures/), ein wesentlicher Bestandteil von f#, die Schlüssel zum Verständnis der f#-Code ist. Sie werden dies auch feststellen, wenn Sie darauf zeigen, dass die Funktion in Visual Studio Code.

In den Text der Funktion sehen Sie zwei Teile:

1. Eine innere Funktion namens `isVowel`, die bestimmt, ob ein angegebenes Zeichen (`c`) überprüfen, ob diese einer der über die angegebenen Muster entspricht, besteht ein Vokal [Musterabgleich](../language-reference/pattern-matching.md):

   [!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/to-pig-latin.fsx#L2-L6)]

2. Ein [`if..then..else`](../language-reference/conditional-expressions-if-then-else.md) -Ausdruck, der prüft, ob das erste Zeichen ist ein Vokal Konstrukte, die einen Rückgabewert aus der Eingabezeichen abhängig, ob das erste Zeichen wurde ein Vokal oder nicht:

   [!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/to-pig-latin.fsx#L8-L11)]

Die ablaufsteuerung `toPigLatin` ist daher:

Überprüfen Sie, ob das erste Zeichen des eingegebenen Worts ein Vokal ist. Wenn es sich handelt, fügen Sie am Ende des Worts "juhu". Andernfalls verschieben Sie dem ersten Zeichen am Ende des Worts zu, und fügen Sie "Weg" hinzu.

Eine letzte Sache dazu bitte beachten Sie: Es gibt keine explizite Anweisung von der Funktion, im Gegensatz zu es viele weitere Sprachen zurückgegeben. Dies ist da f# ausdrucksbasiert ist, und der letzte Ausdruck in den Hauptteil einer Funktion der Rückgabewert ist. Da `if..then..else` ist selbst ein Ausdruck, der Text der der `then` Block oder im Text der der `else` Block wird je nach dem eingegebenen Wert zurückgegeben werden.

## <a name="moving-your-script-code-into-the-implementation-file"></a>Verschieben von Skriptcode in der Implementierungsdatei hinzu

Die vorherigen Abschnitten in diesem Artikel veranschaulicht die allgemeine ersten Schritt bei der Schreiben von F#-Code: das Schreiben einer anfänglichen-Funktion und interaktiv mit FSI ausgeführt wird. Dies bezeichnet man als REPL-driven Development, in denen [REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) steht für "Lesen-auswerten-ausgeben-Schleife". Es ist eine hervorragende Möglichkeit, mit der Funktionalität zu experimentieren, bis Sie funktioniert haben.

Der nächste Schritt in der REPL-gesteuerte Entwicklung ist funktionierenden Code in einer F#-Implementierungsdatei zu verschieben. Sie können dann vom F#-Compiler in eine Assembly kompiliert werden, die ausgeführt werden können.

Öffnen Sie zunächst `ClassLibraryDemo.fs`.  Sie werden feststellen, dass der Code bereits vorhanden vorhanden ist. Fahren Sie fort, und löschen Sie die Definition der Klasse, aber stellen Sie sicher, dass die [ `namespace` ](../language-reference/namespaces.md) Deklaration oben.

Als Nächstes erstellen Sie ein neues [ `module` ](../language-reference/modules.md) namens `PigLatin` , und kopieren Sie die `toPigLatin` als solche in diese Funktion:

[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]

Öffnen Sie als Nächstes die `Script.fsx` -Datei erneut, und löschen Sie das gesamte `toPigLatin` funktionieren, aber Achten Sie darauf, halten die folgenden zwei Zeilen in der Datei:

```fsharp
#load "ClassLibraryDemo.fs"
open ClassLibraryDemo
```

Die erste Zeile wird für FSI zum Laden von Skripts benötigt `ClassLibraryDemo.fs`. In der zweite Zeile wird aus Gründen der benutzerfreundlichkeit: weglassen, ist optional, aber Sie benötigen, geben Sie `open ClassLibraryDemo` in einem FSI-Fenster, wenn Sie, schalten Sie möchten die `ToPigLatin` Modul in den Bereich.

Rufen Sie als Nächstes im Fenster FSI-Funktion mit dem `PigLatin` -Modul, das Sie zuvor definiert:

```
> PigLatin.toPigLatin "banana";;
val it : string = "ananabay"
> PigLatin.toPigLatin "apple";;
val it : string = "appleyay"
```

Erfolgreich! Sie erhalten die gleichen Ergebnisse wie vor, aber jetzt aus einer F#-Implementierungsdatei geladen. Der Hauptunterschied ist, dass es sich bei F#-Quelldateien in Assemblys kompiliert werden, die nicht nur in FSI überall ausgeführt werden können.

## <a name="summary"></a>Zusammenfassung

In diesem Artikel haben Sie Folgendes gelernt:

1. Wie Sie Visual Studio Code mit Ionide einrichten.
2. Wie Sie Ihr erste F#-Projekt mit Ionide zu erstellen.
3. Informationen zum Verwenden von F#-Skripts schreiben Ihre erste F#-Funktion in Ionide, und führen Sie ihn anschließend in FSI.
4. Informationen zum Migrieren von Skriptcode an F#-Quelle, und rufen Sie dann diesen Code von FSI.

Sie sind jetzt viel mehr F#-Code mithilfe von Visual Studio Code und Ionide schreiben ausgestattet.

## <a name="troubleshooting"></a>Problembehandlung

Hier sind einige Möglichkeiten, wie, die Sie bestimmte Probleme beheben können, denen auftreten können:

1. Um den Code Bearbeitungsfunktionen Ionide zu erhalten, müssen Ihre F#-Dateien gespeichert werden, auf dem Datenträger und in einen Ordner, der in der Visual Studio Code-Arbeitsbereich geöffnet ist.
2. Wenn Sie Änderungen an Ihrem System oder Ionide erforderlichen Komponenten installiert, mit Visual Studio Code geöffnet haben, starten Sie Visual Studio Code neu.
3. Überprüfen Sie, dass Sie die f#-Compiler und f# interactive über die Befehlszeile ohne einen vollständig qualifizierten Pfad verwenden können. Sie können dazu eingeben `fsc` in einer Befehlszeile für den f#-Compiler und `fsi` oder `fsharpi` für die Visual F#-tools für Windows und Mono unter Mac/Linux, bzw.
4. Wenn Sie ungültige Zeichen in Ihrem Projektverzeichnisse verfügen, funktionieren möglicherweise nicht Ionide.  Benennen Sie Ihre Projektverzeichnisse, wenn dies der Fall ist.
5. Wenn keines der Ionide-Befehle verwenden, überprüfen Sie Ihre [standardtastenzuordnungen von Visual Studio Code](https://code.visualstudio.com/docs/customization/keybindings#_customizing-shortcuts) um festzustellen, ob Sie sie versehentlich überschreiben möchten.
6. Versuchen Sie es entfernen, wenn Ionide auf Ihrem Computer aufgeteilt wird und keines der genannten wurde das Problem behoben, die `ionide-fsharp` Verzeichnis auf Ihrem Computer und installieren Sie die Suite-Plug-In erneut.

Ionide ist ein open-Source-Projekt durch Mitglieder der F#-Community erstellt und verwaltet. Sie Probleme melden und gerne am beitragen die [Ionide-VSCode: FSharp-GitHub-Repository](https://github.com/ionide/ionide-vscode-fsharp).

Wenn Sie ein Problem gemeldet haben, führen Sie [die Anweisungen zum Abrufen von Protokollen zu verwenden, wenn ein Problem meldet](https://github.com/ionide/ionide-vscode-fsharp#how-to-get-logs-for-debugging--issue-reporting).

Sie können auch weitere Hilfe bitten, aus der Ionide-Entwickler und f#-Community in den [Ionide Gitter Kanal](https://gitter.im/ionide/ionide-project).

## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zu f# und die Funktionen der Sprache, sehen Sie sich [Einführung in f#](../tour.md).
