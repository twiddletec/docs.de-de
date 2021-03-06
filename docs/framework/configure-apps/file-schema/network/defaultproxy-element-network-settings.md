---
title: '&lt;DefaultProxy&gt; -Element (Netzwerkeinstellungen)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#defaultProxy
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy
helpviewer_keywords:
- defaultProxy element
- <defaultProxy> element
ms.assetid: 9d663c4b-07b4-4f6f-9b12-efbd3630354f
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 1e9548c6d43824ea5017b73a132eb49444ed6c77
ms.sourcegitcommit: 736ec4d3e2c74895b47a0d36126657b95da383c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2018
ms.locfileid: "37140189"
---
# <a name="ltdefaultproxygt-element-network-settings"></a>&lt;DefaultProxy&gt; -Element (Netzwerkeinstellungen)
Konfiguriert den HTTP-Proxyserver (Hypertext Transfer Protocol).  
  
 \<configuration>  
\<system.net>  
\<DefaultProxy >  
  
## <a name="syntax"></a>Syntax  
  
```xml  
      <defaultProxy  
        enabled="true|false"  
        useDefaultCredentials="true|false">  
           <bypasslist> … </bypasslist>  
           <proxy> … </proxy>  
           <module> … </module>  
      </defaultProxy>
```  
  
## <a name="attributes-and-elements"></a>Attribute und Elemente  
 In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.  
  
### <a name="attributes"></a>Attribute  
  
|**Element**|**Beschreibung**|  
|-----------------|---------------------|  
|`enabled`|Gibt an, ob ein Webproxy verwendet wird. Der Standardwert ist `true`.|  
|`useDefaultCredentials`|Gibt an, ob die Standardanmeldeinformationen für diesen Host für den Zugriff auf den Webproxy verwendet werden. Der Standardwert ist `false`.|  
  
### <a name="child-elements"></a>Untergeordnete Elemente  
  
|**Element**|**Beschreibung**|  
|-----------------|---------------------|  
|[BypassList](../../../../../docs/framework/configure-apps/file-schema/network/bypasslist-element-network-settings.md)|Gibt einen Satz von regulären Ausdrücken zur Beschreibung der Adressen an, die keinen Proxy verwenden.|  
|[Modul](../../../../../docs/framework/configure-apps/file-schema/network/module-element-network-settings.md)|Fügt der Anwendung ein neues Proxymodul hinzu.|  
|[Proxy](../../../../../docs/framework/configure-apps/file-schema/network/proxy-element-network-settings.md)|Definiert einen Proxyserver.|  
  
### <a name="parent-elements"></a>Übergeordnete Elemente  
  
|**Element**|**Beschreibung**|  
|-----------------|---------------------|  
|[System.NET](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|Enthält Einstellungen, die festlegen, wie Verbindungen zwischen .NET Framework und dem Netzwerk hergestellt werden.|  
  
## <a name="remarks"></a>Hinweise  
 Wenn das defaultProxy-Element leer ist, werden die Proxyeinstellungen von Internet Explorer verwendet. Dieses Verhalten unterscheidet sich von .NET Framework 1.1.  
  
 Eine Ausnahme wird ausgelöst, wenn die [Modul](../../../../../docs/framework/configure-apps/file-schema/network/module-element-network-settings.md) Element gibt einen nicht öffentlichen Typ, der Typ nicht ableiten der <xref:System.Net.IWebProxy> -Klasse, eine Ausnahme vom Standardkonstruktor dieses Objekts aufgetreten ist, oder eine Ausnahme aufgetreten ist während das System angegebenen Standardproxys werden abgerufen. Die <xref:System.Exception.InnerException%2A>-Eigenschaft für die Ausnahme muss zusätzliche Informationen zur Fehlerursache enthalten.  
  
## <a name="configuration-files"></a>Konfigurationsdateien  
 Dieses Element kann in der Anwendungskonfigurationsdatei oder in der Computerkonfigurationsdatei ("Machine.config") verwendet werden.  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel verwendet die Standardeinstellungen des Internet Explorer-Proxys, gibt die Adresse des Proxyservers an und umgeht den Proxy für den lokalen Zugriff und "contoso.com".  
  
```xml  
<configuration>  
  <system.net>  
    <defaultProxy>  
      <proxy  
        usesystemdefault="true"  
        proxyaddress="http://192.168.1.10:3128"  
        bypassonlocal="true"  
      />  
      <bypasslist>  
        <add address="[a-z]+\.contoso\.com$" />  
      </bypasslist>  
    </defaultProxy>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a>Siehe auch  
 <xref:System.Net.WebProxy?displayProperty=nameWithType>  
 [Network Settings Schema (Schema für Netzwerkeinstellungen)](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
