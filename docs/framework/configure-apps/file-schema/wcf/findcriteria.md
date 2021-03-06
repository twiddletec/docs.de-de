---
title: '&lt;findCriteria&gt;'
ms.date: 03/30/2017
ms.assetid: 5454cd19-6bf5-4ba8-94d1-f58d10dc1917
ms.openlocfilehash: fc9cd3b87d0f47ae0f16b5c5bfcaa4a1167bae9f
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
ms.locfileid: "32748645"
---
# <a name="ltfindcriteriagt"></a>&lt;findCriteria&gt;
Ein Konfigurationselement, das einen Kriteriensatz bereitstellt, der von einer Clientanwendung zum Suchen nach einem Ermittlungsdienst verwendet wird. Kriterien können in Suchkriterien (was Sie suchen Dienste) gruppiert werden und Beendigungskriterien (wie lange soll die Suche dauern).  
  
 \<system.ServiceModel>  
\<StandardEndpoints >  
  
## <a name="syntax"></a>Syntax  
  
```xml  
<system.serviceModel>  
  <standardEndpoints>
    <dynamicEndpoint>
      <standardEndpoint>
        <discoveryClientSettings discoveryEndpoint="String">
          <findCriteria duration="TimeSpan" maxResults="Integer" scopeMatchBy="Uri">
            <contractTypeNames>
              <add name="String" namespace="String" />
            <contractTypeNames>
            <extensions />
            <scopes>
              <add scope="URI" />
            </scopes>
          </findCriteria>
        </discoveryClientSettings>
      </standardEndpoint>
    </dynamicEndpoint>
  </standardEndpoints>  
</system.serviceModel>  
```  
  
## <a name="attributes-and-elements"></a>Attribute und Elemente  
 In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.  
  
### <a name="attributes"></a>Attribute  
  
|Attribut|Beschreibung|  
|---------------|-----------------|  
|duration|Ein Timespan-Wert, der die maximale Zeit angibt, die auf Antworten von Diensten im Netzwerk gewartet wird. Der Standardzeitraum beträgt 20 Sekunden.|  
|maxResults|Eine ganze Zahl, die die maximale Anzahl an Antworten angibt, auf die von Diensten in einem Netzwerk oder im Internet gewartet wird. Wenn die maximale Anzahl erreicht wird, bevor der mit dem `duration`-Attribut festgelegte Zeitraum verstrichen ist, wird der Suchvorgang beendet.|  
|scopeMatchBy|Ein URI, der angibt, welcher Übereinstimmungsalgorithmus verwendet werden soll, während die Übereinstimmung der Bereiche der Probe-Nachricht mit denen des Endpunkts ermittelt wird.<br /><br /> Es gibt fünf unterstützte Bereichsübereinstimmungsregeln. Wenn keine Bereichsübereinstimmungsregel angegeben wird, wird `ScopeMatchByPrefix` verwendet. Weitere Informationen hierzu finden Sie unter <xref:System.ServiceModel.Discovery.FindCriteria>.|  
  
### <a name="child-elements"></a>Untergeordnete Elemente  
  
|Element|Beschreibung|  
|-------------|-----------------|  
|[\<ContractTypeNames >](../../../../../docs/framework/configure-apps/file-schema/wcf/contracttypenames.md)|Eine Auflistung von Konfigurationselementen, die die Namen von Workflowdienst-Vertragstypen enthalten.|  
|\<Extensions > von \<FindCriteria >|Eine Auflistung von XML-Elementobjekten, die Erweiterungen bereitstellen.|  
|[\<Bereiche >](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)|Eine Auflistung von Objekten, die absolute URIs enthalten, die während eines Suchvorgangs verwendet werden, um einen bestimmten Dienst oder bestimmte Dienste zu suchen.<br /><br /> Wenn der bestimmte Dienst gefunden wird, wurde eine erfolgreiche Übereinstimmung zwischen dem Dienst- und Bereichs-URI hergestellt. Dies geschieht mitunter mittels Bereichsregeln, die Probleme beim Abgleichen behandeln.|  
  
### <a name="parent-elements"></a>Übergeordnete Elemente  
  
|Element|Beschreibung|  
|-------------|-----------------|  
|[\<StandardEndpoints >](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|Enthält die Einstellungen, die von einer Anwendung benötigt werden, um am Dienstermittlungsprozess als Client teilzunehmen.|  
  
## <a name="see-also"></a>Siehe auch  
 <xref:System.ServiceModel.Discovery.FindCriteria>  
 <xref:System.ServiceModel.Discovery.Configuration.FindCriteriaElement>
