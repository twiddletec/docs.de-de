---
title: "&lt;wsFederationHttpBinding&gt; | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "wsFederationBinding-Element"
ms.assetid: 9c3312b4-2137-4e71-bf3f-de1cf8e9be79
caps.latest.revision: 28
author: "Erikre"
ms.author: "erikre"
manager: "erikre"
caps.handback.revision: 28
---
# &lt;wsFederationHttpBinding&gt;
Definiert eine Bindung, die WS\-Federation unterstützt.  
  
## Syntax  
  
```  
  
<wsFederationHttpBinding>  
    <binding   
        bypassProxyOnLocal="Boolean"  
        closeTimeout="TimeSpan"   
        hostNameComparisonMode="StrongWildcard/Exact/WeakWildcard"  
        maxBufferPoolSize="integer"  
        maxReceivedMessageSize="integer"  
        messageEncoding="Text/Mtom"   
                name="string"  
        openTimeout="TimeSpan"   
        privacyNoticeAt="Uri"  
        privacyNoticeVersion="Integer"  
        proxyAddress="Uri"   
        receiveTimeout="TimeSpan"  
        sendTimeout="TimeSpan"  
        textEncoding="UnicodeFffeTextEncoding/Utf16TextEncoding/ Utf8TextEncoding"  
        transactionFlow="Boolean"  
        useDefaultWebProxy="Boolean">  
        <security mode="None/Message/TransportWithMessageCredential">  
         <message   
            algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
            issuedTokenType="string"   
            issuedKeyType="SymmetricKey/PublicKey"  
            negotiateServiceCredential="Boolean" >  
            <claimTypeRequirements>  
               <add claimType="URI"  
                    isOptional="Boolean" />  
            </claimTypeRequirements>  
                        <issuer address="Uri" >  
               <headers>  
                  <add name="String"  
                       namespace="String" />  
                          </headers>  
                              <identity>  
                                 <certificate encodedValue="String"/>  
                                <certificateReference findValue="String"   
                                 isChainIncluded="Boolean"  
                            storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"  
                                  storeLocation="LocalMachine/CurrentUser"  
                                   X509FindType=System.Security.Cryptography.X509certificates.X509findtype/>  
                                   <dns value="String"/>  
                                <rsa value="String"/>  
                                <servicePrincipalName value="String"/>  
                                <usePrincipalName value="String"/>  
                              </identity>  
                        </issuer>  
                        <issuerMetadata address=String" >  
               <headers>  
                  <add name="String"  
                       namespace="String" />  
               </headers>  
               <identity>  
                  <certificate encodedValue="String"/>  
                  <certificateReference findValue="String"   
                     isChainIncluded="Boolean"  
                     storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"  
                     storeLocation="LocalMachine/CurrentUser"  
                     x509FindType=System.Security.Cryptography.X509certificates.X509findtype/>  
                  <dns value="String"/>  
                  <rsa value="String"/>  
                  <servicePrincipalName value="String"/>  
                  <usePrincipalName value="String"/>  
               </identity>  
                        </issuerMetadata>  
            <tokenRequestParameters>  
               <xmlElement>  
               </xmlElement>  
            </tokenRequestParameters>  
           </message>  
        </security>  
        <reliableSession ordered="Boolean"  
           inactivityTimeout="TimeSpan"  
           enabled="Boolean" />  
       <readerQuotas   
            maxArrayLength="Integer"  
            maxBytesPerRead="Integer"  
            maxDepth="Integer"   
            maxNameTableCharCount="Integer"           
            maxStringContentLength="Integer" />  
    </binding>  
</wsFederationBinding>  
```  
  
## Attribute und Elemente  
 In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.  
  
### Attribute  
  
|Attribut|Beschreibung|  
|--------------|------------------|  
|bypassProxyOnLocal|Ein boolescher Wert, der angibt, ob der Proxyserver bei lokalen Adressen umgangen werden soll.  Die Standardeinstellung ist `false`.|  
|closeTimeout|Ein <xref:System.TimeSpan>\-Wert, der das Zeitintervall für den Abschluss eines Schließvorgangs angibt.  Dieser Wert muss größer oder gleich <xref:System.TimeSpan.Zero> sein.  Der Standardwert ist 00:01:00.|  
|hostnameComparisonMode|Gibt den HTTP\-Hostnamen\-Vergleichsmodus an, der verwendet wird, um URIs zu analysieren.  Dieses Attribut ist vom Typ <xref:System.ServiceModel.HostnameComparisonMode> und gibt an, ob beim Abgleich des URI der Hostname zum Erreichen des Dienstes verwendet wird.  Der Standardwert lautet <xref:System.ServiceModel.HostnameComparisonMode.StrongWildcard>, wodurch der Hostname beim Abgleich ignoriert wird.|  
|maxBufferPoolSize|Eine ganze Zahl, die die maximale Pufferpoolgröße für diese Bindung angibt.  Der Standardwert ist 524.288 Byte \(512 \* 1024\).  Viele Teile von Windows Communication Foundation \(WCF\) verwenden Puffer.  Das Erstellen und Zerstören von Puffern bei jeder Verwendung ist kostspielig. Dasselbe gilt für die Garbage Collection für Puffer.  Bei Pufferpools können Sie einen zu verwendenden Puffer aus dem Pool nehmen und ihn nach der Verwendung wieder dem Pool zuführen.  So wird der Aufwand beim Erstellen und Zerstören von Puffern vermieden.|  
|maxReceivedMessageSize|Eine positive ganze Zahl, die die maximale Nachrichtengröße in Bytes einschließlich Header angibt, die in einem für diese Bindung konfigurierten Kanal beim Nachrichtenempfang zulässig ist.  Der Absender einer Nachricht, die diese Grenze überschreitet, erhält einen SOAP\-Fehler.  Der Empfänger verwirft die Nachricht und erstellt einen Eintrag des Ereignisses im Ablaufverfolgungsprotokoll.  Der Standard ist 65536.|  
|messageEncoding|Definiert den Encoder, der verwendet wird, um die SOAP\-Nachricht zu codieren.  Folgende Werte sind gültig:<br /><br /> -   Text: Verwenden Sie einen Textnachrichtenencoder.<br />-   Mtom: Verwendung eines MTOM\-Encoders \(Message Transmission Organisation Mechanism 1.0\).<br /><br /> Der Standardwert ist Text.<br /><br /> Dieses Attribut ist vom Typ <xref:System.ServiceModel.WSMessageEncoding>.|  
|Name|Eine Zeichenfolge, die den Konfigurationsnamen der Bindung enthält.  Dieser Wert sollte eindeutig sein, da er von der Bindung zur Identifizierung verwendet wird.  Ab [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)] müssen Bindungen und Verhalten keinen Namen aufweisen.  Weitere Informationen zu Standardkonfiguration und zu namenlosen Bindungen und Verhalten finden Sie unter [Vereinfachte Konfiguration](../../../../../docs/framework/wcf/simplified-configuration.md) und [Vereinfachte Konfiguration für WCF\-Dienste](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).|  
|openTimeout|Ein <xref:System.TimeSpan>\-Wert, der das Zeitintervall für den Abschluss eines Öffnungsvorgangs angibt.  Dieser Wert muss größer oder gleich <xref:System.TimeSpan.Zero> sein.  Der Standardwert ist 00:01:00.|  
|privactyNoticeAt|Eine Zeichenfolge mit dem URI, an dem sich der Datenschutzhinweis befindet.|  
|privactyNoticeVersion|Eine ganze Zahl, die die Version des aktuellen Datenschutzhinweises angibt.|  
|proxyAddress|Ein URI, der die Adresse des HTTP\-Proxys angibt.  Wenn `useDefaultWebProxy` `true` ist, muss diese Einstellung `null` lauten.  Die Standardeinstellung ist `null`.|  
|receiveTimeout|Ein <xref:System.TimeSpan>\-Wert, der das Zeitintervall für den Abschluss eines Empfangsvorgangs angibt.  Dieser Wert muss größer oder gleich <xref:System.TimeSpan.Zero> sein.  Der Standardwert ist 00:10:00.|  
|sendTimeout|Ein <xref:System.TimeSpan>\-Wert, der das Zeitintervall für den Abschluss eines Sendevorgangs angibt.  Dieser Wert muss größer oder gleich <xref:System.TimeSpan.Zero> sein.  Der Standardwert ist 00:01:00.|  
|textEncoding|Legt die Zeichensatzkodierung fest, die zum Ausgeben von Nachrichten über die Bindung verwendet werden soll.  Folgende Werte sind gültig:<br /><br /> -   BigEndianUnicode: Unicode BigEndian\-Kodierung.<br />-   Unicode: 16\-Bit\-Codierung.<br />-   UTF8: 8\-Bit\-Codierung<br /><br /> Der Standard ist UTF8.  Dieses Attribut ist vom Typ <xref:System.Text.Encoding>.|  
|transactionFlow|Ein boolescher Wert, der angibt, ob die Bindung geleitete WS\-Transaktionen unterstützt.  Die Standardeinstellung ist `false`.|  
|useDefaultWebProxy|Ein boolescher Wert, der angibt, ob der automatisch konfigurierte HTTP\-Proxy des Systems verwendet wird.  Die Proxyadresse muss `null` sein \(das heißt, sie ist nicht festgelegt\), wenn dieses Attribut den Wert `true` hat.  Die Standardeinstellung ist `true`.|  
  
### Untergeordnete Elemente  
  
|Element|Beschreibung|  
|-------------|------------------|  
|[\<Sicherheit\>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-wsfederationhttpbinding.md)|Definiert die Sicherheitseinstellungen für die Nachricht.  Dieses Element ist vom Typ <xref:System.ServiceModel.Configuration.WSFederationHttpSecurityElement>.|  
|[\<readerQuotas\>](../Topic/%3CreaderQuotas%3E.md)|Definiert die Beschränkungen der Komplexität von SOAP\-Nachrichten, die von Endpunkten verarbeitet werden können, die mit dieser Bindung konfiguriert wurden.  Dieses Element ist vom Typ <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.|  
|[reliableSession](http://msdn.microsoft.com/de-de/9c93818a-7dfa-43d5-b3a1-1aafccf3a00b)|Gibt an, ob zuverlässige Sitzungen zwischen Kanalendpunkten aufgebaut werden.|  
  
### Übergeordnete Elemente  
  
|Element|Beschreibung|  
|-------------|------------------|  
|[\<Bindungen\>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|Dieses Element enthält eine Auflistung von standardmäßigen und benutzerdefinierten Bindungen.|  
  
## Hinweise  
 Ein Verbund zeichnet sich durch die Möglichkeit aus, Identitäten auf mehreren Systemen für Authentifizierung und Autorisierung freizugeben.  Diese Identitäten können auf Benutzer oder Computer verweisen.  Verbundenes HTTP unterstützt sowohl SOAP\-Sicherheit als auch Sicherheit im gemischten Modus, jedoch keine exklusive Verwendung von Transportsicherheit.  Diese Bindung bietet [!INCLUDE[indigo1](../../../../../includes/indigo1-md.md)]\-Unterstützung für das WS\-Verbundprotokoll.  Mit dieser Bindung konfigurierte Dienste müssen den HTTP\-Transport verwenden.  
  
 Bindungen bestehen aus einem Stapel von Bindungselementen.  Der Stapel von Bindungselementen in  
  
 `wsFederationHttpBinding` ist mit dem in `wsHttpBinding`  
  
 identisch, wenn [\<Sicherheit\>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-wsfederationhttpbinding.md) auf den Standardwert von <xref:System.ServiceModel.WSFederationHttpSecurityMode> festgelegt ist.  
  
 Die `wsFederationHttpBinding` steuert die Details der Nachrichtensicherheitseinstellungen in [\<message\>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-element-of-wsfederationhttpbinding.md).  Beachten Sie, dass das [\<Sicherheit\>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-wsfederationhttpbinding.md)\-Element nur Zugriff zum Abrufen bietet, da die von der Bindung verwendete Sicherheit nicht geändert werden kann, nachdem die Bindung erstellt wurde.  
  
 Die `wsFederationHttpBinding` bietet zudem ein privacyNoticeAt\-Attribut zum Festlegen und Abrufen des URIs, an dem sich der Datenschutzhinweis befindet.  
  
 Das Sichern von Richtlinien ist vor allem in Verbundszenarien wichtig.  Es wird empfohlen, Sicherheitsfunktionen wie HTTPS einzusetzen, um die Richtlinie vor bösartigen Benutzern zu schützen.  
  
 In Verbundszenarien, die diese Bindung nutzen, enthält die Dienstrichtlinie häufig wichtige Informationen, wie z.&\#160;B. den Schlüssel für die Verschlüsselung des ausgestellten \(SAML\-\) Tokens, den Anspruchstyp für das Token usw.  Wenn diese Richtlinie missbräuchlich genutzt wird, könnte ein Angreifer den Schlüssel des ausgestellten Tokens herausfinden und Informationen offen legen und andere böswillige Handlungen vornehmen.  Um dies zu vermeiden, muss die Richtlinie sicher vom Dienst abgerufen werden \(z.&\#160;B. über HTTPS\).  
  
 Weitere Informationen zu dieser Bindung finden Sie unter [Vorgehensweise: Erstellen einer WSFederationHttpBinding](../../../../../docs/framework/wcf/feature-details/how-to-create-a-wsfederationhttpbinding.md).  
  
## Beispiel  
  
```  
<configuration>  
<system.ServiceModel>  
<bindings>  
<wsFederationHttpBinding>  
    <binding   
        bypassProxyOnLocal="false"  
        transactionFlow="false"  
        hostNameComparisonMode="WeakWildcard"  
        maxReceivedMessageSize="1000"  
        messageEncoding="Mtom"   
        proxyAddress="http://foo/bar"   
        textEncoding="Utf16TextEncoding"  
        useDefaultWebProxy="false">  
        <reliableSession ordered="false"  
            inactivityTimeout="00:02:00" enabled="true" />  
        <security mode="None">  
           <message negotiateServiceCredential="false"  
                algorithmSuite="Aes128"  
                issuedTokenType="saml"   
                issuedKeyType="PublicKey">  
               <issuer address="http://localhost/Sts" />  
           </message>  
        </security>  
    </binding>  
</wsFederationBinding>  
</bindings>  
</system.ServiceModel>  
</configuration>  
```  
  
## Siehe auch  
 <xref:System.ServiceModel.WSFederationHttpBinding>   
 <xref:System.ServiceModel.Configuration.WSFederationHttpBindingElement>   
 [Vorgehensweise: Erstellen einer WSFederationHttpBinding](../../../../../docs/framework/wcf/feature-details/how-to-create-a-wsfederationhttpbinding.md)   
 [Bindungen](../../../../../docs/framework/wcf/bindings.md)   
 [Konfigurieren der vom System bereitgestellten Bindungen](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)   
 [Using Bindings to Configure Windows Communication Foundation Services and Clients](http://msdn.microsoft.com/de-de/bd8b277b-932f-472f-a42a-b02bb5257dfb)   
 [\<Bindung\>](../../../../../docs/framework/misc/binding.md)