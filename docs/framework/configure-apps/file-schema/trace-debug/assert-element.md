---
title: '&lt;Assert-&gt; Element'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/assert
- http://schemas.microsoft.com/.NetConfiguration/v2.0#assert
helpviewer_keywords:
- <assert> element
- assert element
ms.assetid: ef4c3229-b151-4d85-8091-e6456af9b935
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: ab1644d23e4d6d78b62e701902e5ec39e134b38b
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
ms.locfileid: "32745119"
---
# <a name="ltassertgt-element"></a>&lt;Assert-&gt; Element
Gibt an, ob ein Meldungsfeld angezeigt wird, wenn Sie die <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType>-Methode aufrufen. Außerdem wird der Name der Datei angegeben, in die die Meldung geschrieben werden soll.  
  
 \<configuration>  
\<System.Diagnostics >  
\<Assert->  
  
## <a name="syntax"></a>Syntax  
  
```xml  
<assert assertuienabled="true|false" logfilename="file name"/>  
```  
  
## <a name="attributes-and-elements"></a>Attribute und Elemente  
 In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.  
  
### <a name="attributes"></a>Attribute  
  
|Attribut|Beschreibung|  
|---------------|-----------------|  
|`assertuienabled`|Optionales Attribut.<br /><br /> Gibt an, ob die anzuzeigenden ein Meldungsfeld, wenn die **Debug.Assert** Methode ergibt **"false"**.|  
|`logfilename`|Optionales Attribut.<br /><br /> Gibt den Namen der Datei zum Schreiben der Nachricht auf, wenn **Debug.Assert** ergibt **"false"**.|  
  
## <a name="assertuienabled-attribute"></a>assertuienabled-Attribut  
  
|Wert|Beschreibung|  
|-----------|-----------------|  
|`true`|Zeigt das Meldungsfeld an. Dies ist die Standardeinstellung.|  
|`false`|Das Meldungsfeld wird nicht angezeigt werden.|  
  
### <a name="child-elements"></a>Untergeordnete Elemente  
 Keine  
  
### <a name="parent-elements"></a>Übergeordnete Elemente  
  
|Element|Beschreibung|  
|-------------|-----------------|  
|`configuration`|Das Stammelement in jeder von den Common Language Runtime- und .NET Framework-Anwendungen verwendeten Konfigurationsdatei.|  
|`system.diagnostics`|Gibt Ablaufverfolgungslistener an, die Meldungen sammeln, speichern und weiterleiten sowie die Ebene, für die ein Ablaufverfolgungsschalter festgelegt ist.|  
  
## <a name="remarks"></a>Hinweise  
 Beide Attribute in der  **\<assert >** Element sind optional. Sie können Meldungsfelder deaktivieren, ohne Angabe einer Datei, um die Nachrichten schreiben oder können Sie eine Datei zum Schreiben, dass Nachrichten an die while-verlassen Felder aktiviert Nachricht angeben.  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt die Vorgehensweise beim Anzeigen von Meldungsfeldern deaktivieren, beim Aufrufen von **Debug.Assert** und Schreiben von Nachrichten auf `c:\log.txt`.  
  
```xml  
<configuration>  
   <system.diagnostics>  
      <assert assertuienabled="false" logfilename="c:\log.txt"/>  
   </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a>Siehe auch  
 <xref:System.Diagnostics.Debug>  
 [Trace and Debug Settings Schema (Schema für Ablaufverfolgungs- und Debugeinstellungen)](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
