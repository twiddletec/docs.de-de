---
title: 'Gewusst wie: Zeichnen eines Bereichs mit einem radialen Farbverlauf'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- brushes [WPF], painting with radial gradients
- radial gradients [WPF], painting with
- painting [WPF], with radial gradients
ms.assetid: b5d0fc8a-8986-4796-b003-a75b41a48928
ms.openlocfilehash: d794f85ce4968e1cf1759df5358834f3b4cdfb50
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33560640"
---
# <a name="how-to-paint-an-area-with-a-radial-gradient"></a>Gewusst wie: Zeichnen eines Bereichs mit einem radialen Farbverlauf
Dieses Beispiel zeigt, wie die <xref:System.Windows.Media.RadialGradientBrush> Klasse, um einen Bereich mit einem radialen Farbverlauf zu zeichnen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird eine <xref:System.Windows.Media.RadialGradientBrush> ein Rechteck mit einem radialen Farbverlauf gezeichnet, die von Gelb zu rot Gelbgrün Blau übergeht.  
  
 [!code-csharp[BrushesIntroduction_snip#SimpleRadialGradientExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BrushesIntroduction_snip/CSharp/RadialGradientBrushSnippet.cs#simpleradialgradientexamplewholepage)]
 [!code-vb[BrushesIntroduction_snip#SimpleRadialGradientExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/BrushesIntroduction_snip/visualbasic/radialgradientbrushsnippet.vb#simpleradialgradientexamplewholepage)]
 [!code-xaml[BrushesIntroduction_snip#SimpleRadialGradientExampleWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/BrushesIntroduction_snip/XAML/RadialGradientBrushSnippet.xaml#simpleradialgradientexamplewholepage)]  
  
 Die folgende Abbildung zeigt den Farbverlauf aus dem vorherigen Beispiel. Der Farbverlauf beendet wurden hervorgehoben.  
  
 ![Farbverlaufstopps in einem radialen Farbverlauf](../../../../docs/framework/wpf/graphics-multimedia/media/wcpsdk-graphicsmm-4gradientstops-rg.png "Wcpsdk_graphicsmm_4gradientstops_rg")  
  
> [!NOTE]
>  In den Beispielen in diesem Thema verwenden Sie das Standard-Koordinatensystem für Steuerpunkte festlegen. Der Standard-Koordinatensystem ist relativ zu einem umgebenden Feld: 0 gibt 0 Prozent des umgebenden Felds und 1 gibt 100 Prozent des umgebenden Felds an. Sie können dieses Koordinatensystems ändern, durch Festlegen der <xref:System.Windows.Media.GradientBrush.MappingMode%2A> -Eigenschaft auf den Wert <xref:System.Windows.Media.BrushMappingMode.Absolute>. Ein absolutes Koordinatensystem ist nicht relativ zu einem umgebenden Feld. Werte werden direkt im lokalen Raum interpretiert.  
  
 Für zusätzliche <xref:System.Windows.Media.RadialGradientBrush> finden Sie unter der [Pinsel Beispiel](http://go.microsoft.com/fwlink/?LinkID=159973). Weitere Informationen zu Farbverläufen und anderen Typen von Pinseln finden Sie unter [Zeichnen mit Volltonfarben und Farbverläufen (Übersicht)](../../../../docs/framework/wpf/graphics-multimedia/painting-with-solid-colors-and-gradients-overview.md).
