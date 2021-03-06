---
title: 'Gewusst wie: Abrufen von Memberkonfliktinformationen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7dd6829e-79a5-4480-9023-9e588cb0bf2e
ms.openlocfilehash: 5d0788daac6c1be8dd7670c330d1efc36b074c2f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33354380"
---
# <a name="how-to-retrieve-member-conflict-information"></a>Gewusst wie: Abrufen von Memberkonfliktinformationen
Sie können die <xref:System.Data.Linq.MemberChangeConflict>-Klasse verwenden, um Informationen über einzelne kollidierende Member abzurufen. In diesem gleichen Kontext können Sie für jeden Member für eine benutzerdefinierte Behandlung des Konflikts sorgen. Weitere Informationen finden Sie unter [vollständige Parallelität: Übersicht über](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).  
  
## <a name="example"></a>Beispiel  
 Der folgende Code wechselt durch die <xref:System.Data.Linq.ObjectChangeConflict>-Objekte. Für jedes Objekt durchläuft er dann die <xref:System.Data.Linq.MemberChangeConflict>-Objekte.  
  
> [!NOTE]
>  Schließen Sie <xref:System.Reflection> ein, um <xref:System.Data.Linq.MemberChangeConflict.Member%2A>-Informationen bereitzustellen.  
  
 [!code-csharp[System.Data.Linq.MemberChangeConflict#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.memberchangeconflict/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.MemberChangeConflict#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.memberchangeconflict/vb/module1.vb#1)]  
  
## <a name="see-also"></a>Siehe auch  
 [Vorgehensweise: Verwalten von Änderungskonflikten](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
