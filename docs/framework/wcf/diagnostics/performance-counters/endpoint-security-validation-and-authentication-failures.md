---
title: 'Endpunkt: Sicherheitsvalidierung und Authentifizierungsfehler'
ms.date: 03/30/2017
ms.assetid: 5bad60aa-6084-4c7b-aefd-9b581f04382e
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 8c46354fac11f5f0b46ef1b5629157f6da455fcb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33471806"
---
# <a name="endpoint-security-validation-and-authentication-failures"></a>Endpunkt: Sicherheitsvalidierung und Authentifizierungsfehler
Indikatorname: Sicherheitsvalidierung und Authentifizierungsfehler  
  
## <a name="description"></a>Beschreibung  
 Dieser Zähler wird jedes Mal inkrementiert, wenn eine Nachricht wegen eines Sicherheitsproblems abgelehnt wird, das nicht von dem Zähler "Nicht autorisierte Sicherheitsanrufe" abgedeckt wird. Zu derartigen Problemen gehören:  
  
-   Clienttoken kann nicht aus der Nachricht gelesen werden.  
  
-   Clienttoken hat die Authentifizierung nicht bestanden (ungültiges Kennwort).  
  
-   Signaturprüfung ist fehlgeschlagen (die Nachricht wurde manipuliert).  
  
-   Die Nachricht ist ein Duplikat einer vorherigen; dies kann während eines Replay-Angriffs geschehen.  
  
-   Ein Entschlüsselungsfehler ist aufgetreten.  
  
-   Einige erforderliche Elemente (fehlender Timestamp oder verschlüsselter Datenblock) fehlen in der Nachricht.  
  
-   Während des TLSNEGO-/SPNEGO-Handshakes sind Fehler aufgetreten.
