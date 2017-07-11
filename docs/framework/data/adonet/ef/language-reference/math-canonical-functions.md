---
title: "Kanonische mathematische Funktionen | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-ado"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
ms.assetid: 6f6cddc6-b561-4ebe-84b6-841ef5b4113b
caps.latest.revision: 2
author: "JennieHubbard"
ms.author: "jhubbard"
manager: "jhubbard"
caps.handback.revision: 2
---
# Kanonische mathematische Funktionen
[!INCLUDE[esql](../../../../../../includes/esql-md.md)] enthält kanonische mathematische Funktionen.  
  
 In der folgenden Tabelle sind die kanonischen mathematischen [!INCLUDE[esql](../../../../../../includes/esql-md.md)]\-Funktionen aufgeführt.  
  
|Funktion|Beschreibung|  
|--------------|------------------|  
|`Abs(` `value` `)`|Gibt den Absolutwert von `value` zurück.<br /><br /> **Argumente**<br /><br /> `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double` und `Decimal`.<br /><br /> **Rückgabewert**<br /><br /> Der `value`\-Typ.<br /><br /> **Beispiel**<br /><br /> `Abs(-2)`|  
|`Ceiling(` `value` `)`|Gibt die kleinste ganze Zahl zurück, die nicht kleiner als `value` ist.<br /><br /> **Argumente**<br /><br /> `Single`, `Double` und `Decimal`.<br /><br /> **Rückgabewert**<br /><br /> Der `value`\-Typ.<br /><br /> **Beispiel**<br /><br /> [!code-csharp[DP EntityServices Concepts#EDM_CEILING](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_ceiling)]
 [!code-sql[DP EntityServices Concepts#EDM_CEILING](../../../../../../samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_ceiling)]|  
|`Floor(` `value` `)`|Gibt die größte ganze Zahl zurück, die nicht größer als `value` ist.<br /><br /> **Argumente**<br /><br /> `Single`, `Double` und `Decimal`.<br /><br /> **Rückgabewert**<br /><br /> Der `value`\-Typ.<br /><br /> **Beispiel**<br /><br /> [!code-csharp[DP EntityServices Concepts#EDM_FLOOR](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_floor)]
 [!code-sql[DP EntityServices Concepts#EDM_FLOOR](../../../../../../samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_floor)]|  
|`Power(` `value`, `exponent``)`|Gibt das Ergebnis der angegebenen `value` an die angegebene `exponent` zurück.<br /><br /> **Argumente**<br /><br /> `value`:  `Int32, Int64, Double` oder `Decimal`.<br /><br /> `exponent`:  `Int64``, Double` oder `Decimal`.<br /><br /> **Rückgabewert**<br /><br /> Der `value`\-Typ.<br /><br /> **Beispiel**<br /><br /> `Power(748.58,2)`|  
|`Round(` `value` `)`|Gibt `value` gerundet zur nächsten Ganzzahl zurück.<br /><br /> **Argumente**<br /><br /> `Single`, `Double` und `Decimal`.<br /><br /> **Rückgabewert**<br /><br /> Der `value`\-Typ.<br /><br /> **Beispiel**<br /><br /> `Round(748.58)`|  
|`Round(` `value`, `digits``)`|Gibt den `value` auf die nächstliegenden angegebenen `digits` gerundet zurück.<br /><br /> **Argumente**<br /><br /> `value`: `Double` oder `Decimal`.<br /><br /> `digits`: `Int16` oder `Int32`.<br /><br /> **Rückgabewert**<br /><br /> Der `value`\-Typ.<br /><br /> **Beispiel**<br /><br /> `Round(748.58,1)`|  
|`Truncate(` `value`, `digits``)`|Gibt den `value` auf die nächstliegenden angegebenen `digits` gekürzt zurück.<br /><br /> **Argumente**<br /><br /> `value`: `Double` oder `Decimal`.<br /><br /> `digits`: `Int16` oder `Int32`.<br /><br /> **Rückgabewert**<br /><br /> Der `value`\-Typ.<br /><br /> **Beispiel**<br /><br /> `Truncate(748.58,1)`|  
  
 Diese Funktionen geben `null` zurück, wenn die Eingabe `null` ist.  
  
 Entsprechende Funktionen sind für den verwalteten Anbieter des Microsoft SQL\-Clients verfügbar.  Weitere Informationen finden Sie unter [SqlClient für Entity Framework\-Funktionen](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md).  
  
## Siehe auch  
 [Kanonische Funktionen](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)