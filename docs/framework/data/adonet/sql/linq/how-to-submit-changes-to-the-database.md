---
title: 'Gewusst wie: Übergeben von Änderungen an die Datenbank'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: c7cba174-9d40-491d-b32c-f2d73b7e9eab
ms.openlocfilehash: fef41cd1bcb9d1c4b98f96975c56bfa19c675608
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33362885"
---
# <a name="how-to-submit-changes-to-the-database"></a>Gewusst wie: Übergeben von Änderungen an die Datenbank
Unabhängig von der Anzahl der Änderungen an Ihren Objekten erfolgen diese Änderungen nur an den Replikaten im Arbeitsspeicher. Sie haben die eigentlichen Daten in der Datenbank nicht verändert. Ihre Änderungen werden erst dann zum Server gesendet, wenn Sie explizit <xref:System.Data.Linq.DataContext.SubmitChanges%2A> im <xref:System.Data.Linq.DataContext> aufrufen.  
  
 Bei diesem Aufruf versucht der <xref:System.Data.Linq.DataContext>, die Änderungen in entsprechende SQL-Befehle zu übersetzen. Können Sie Ihre eigene Logik verwenden um diese Aktionen zu überschreiben, aber die Reihenfolge der Übergabe wird durch einen Dienst des orchestriert die <xref:System.Data.Linq.DataContext> bekannt als die *ändern Prozessor*. Die Ereignisse finden in der folgenden Reihenfolge statt:  
  
1.  Wenn Sie <xref:System.Data.Linq.DataContext.SubmitChanges%2A> aufrufen, prüft [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] den Satz unbekannter Objekte, um zu ermitteln, ob diesen neue Instanzen hinzugefügt wurden. Ist dies der Fall, werden diese Instanzen dem Satz verfolgter Objekte hinzugefügt.  
  
2.  Alle Objekte mit ausstehenden Änderungen werden in eine Objektsequenz gegliedert, die auf den Abhängigkeiten zwischen den Objekten basiert. Objekte, deren Änderungen von anderen Objekten abhängen, werden nach ihren Abhängigkeiten eingeordnet.  
  
3.  Direkt vor der Übergabe der eigentlichen Änderungen startet [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] eine Transaktion, um die Reihe einzelner Befehle zu kapseln.  
  
4.  Die Änderungen an den Objekten werden nacheinander in SQL-Befehle übersetzt und an den Server gesendet.  
  
 Zu diesem Zeitpunkt führen Fehler, die von der Datenbank erkannt werden, zum Stoppen der Übergabe, und eine Ausnahme wird ausgelöst. Alle Änderungen an der Datenbank werden rückgängig gemacht, als ob keine Übergabe stattgefunden hätte. Der <xref:System.Data.Linq.DataContext> verfügt weiterhin über eine vollständige Aufzeichnung aller Änderungen. Daher können Sie versuchen, das Problem zu beheben und <xref:System.Data.Linq.DataContext.SubmitChanges%2A> wie im folgenden Codebeispiel erneut aufrufen.  
  
## <a name="example"></a>Beispiel  
 Wird die Transaktion rund um die Übergabe erfolgreich abgeschlossen, akzeptiert der <xref:System.Data.Linq.DataContext> die Änderungen an den Objekten, indem er die Informationen zur Änderungsverfolgung ignoriert.  
  
 [!code-csharp[DLinqSubmittingChanges#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSubmittingChanges/cs/Program.cs#1)]
 [!code-vb[DLinqSubmittingChanges#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSubmittingChanges/vb/Module1.vb#1)]  
  
## <a name="see-also"></a>Siehe auch  
 [Vorgehensweise: Erkennen und Auflösen von Übergabekonflikten](../../../../../../docs/framework/data/adonet/sql/linq/how-to-detect-and-resolve-conflicting-submissions.md)  
 [Vorgehensweise: Verwalten von Änderungskonflikten](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)  
 [Downloading Sample Databases (Herunterladen von Beispieldatenbanken)](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)  
 [Vornehmen und Übergeben von Datenänderungen](../../../../../../docs/framework/data/adonet/sql/linq/making-and-submitting-data-changes.md)
