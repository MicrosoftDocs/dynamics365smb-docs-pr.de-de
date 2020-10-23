---
title: Währungswechselkurse
description: Am Ende des Geschäftsjahres, müssen Wechselkurse für Verbindlichkeiten und Forderungen reguliert werden, sodass sie ordnungsgemäß in der Jahresbilanz bewertet werden. Der Batchauftrag **Wechselkurse regulieren** unterstützt verschiedene Bewertungsmethoden, um so die rechtlichen Anforderungen in Deutschland zu erfüllen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 69c66cea8688195c39fdc0ce1d6d4a29ec2ad26e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920098"
---
# <a name="currency-exchange-rates"></a>Währungswechselkurse
Am Ende des Geschäftsjahres, müssen Wechselkurse für Verbindlichkeiten und Forderungen reguliert werden, sodass sie ordnungsgemäß in der Jahresbilanz bewertet werden. Der Batchauftrag **Wechselkurse regulieren** unterstützt verschiedene Bewertungsmethoden, um so die rechtlichen Anforderungen in Deutschland zu erfüllen.  

## <a name="valuation-methods"></a>Bewertungsmethoden  
Gemäß dem Bilanzmodernisierungsgesetz (BilMoG) werden Verbindlichkeiten und Forderungen unterschiedlich bewertet, je nach Abweichung zwischen Referenzdatum und Fälligkeitsdatum. Dies wird durch den Batchauftrag **Wechselkurse regulieren** verwaltet, in dem sie angeben können, welche Bewertungsmethode verwendet werden soll. Wenn das Fälligkeitsdatum weniger als ein Jahr nach dem Referenzdatum liegt, muss der Batchauftrag **Wechselkurse regulieren** mit der Bewertungsmethode für den niedrigsten Wert ausgeführt werden.  

In der folgenden Tabelle werden die Bewertungsmethoden näher erläutert.  

|Bewertungsmethode|Description|  
|----------------------|---------------------------------------|  
|BilMoG (Deutschland)|Beginnend mit dem Jahr 2010 wird jeder Sachkontoposten folgendermaßen reguliert:<br /><br /> -   Wenn das Fälligkeitsdatum weniger als ein Jahr nach Referenzdatum liegt, werden Verbindlichkeits-/Forderungsbuchungen nach dem tatsächlichen Wechselkurs bewertet.<br />-   Wenn das Fälligkeitsdatum mehr als ein Jahr nach dem Referenzatum liegt, werden Verbindlichkeits-/Forderungsbuchungen nach dem niedrigsten Wert bewertet, mit der Möglichkeit einer Aufwertung (Wertaufholung) bis um Ausgangswert. **Hinweis:**  Sachkontoposten müssen ein Fälligkeitsdatum enthalten. Ein Posten, der kein Fälligkeitsdatum hat, wird als langfristige Verbindlichkeit behandelt.|  
|Niedrigster Wert|Wechselkurse werden unter Verwendung des niedrigsten Wertes der beiden Wechselkurse reguliert. Währungsverluste werden immer berechnet und gebucht. Währungsgewinne werden nur bis zum ursprünglichen Landeswährungswert der Transaktion berechnet und gebucht.<br /><br /> Dadurch wird sichergestellt, dass Forderungen nicht höher als ihre ursprünglichen Buchungsbeträge bewertet werden und dass Verbindlichkeiten nicht niedriger als ihre ursprünglichen Buchungsbeträge bewertet werden.|  
|Standard|Wechselkurse werden entsprechend den Standardbewertungsprinzipien reguliert. Volle unrealisierte Gewinne und Verluste werden berechnet und gebucht. Wenn die Transaktion teilweise angewendet wird, wird nur der Restbetrag in die Regulierung einbezogen. Weitere Informationen finden Sie unter „Wechselkurse regulieren“.|  

Deutsche Unternehmen müssen die Option **BilMoG (Deutschland)** verwenden, wenn sie den Batchauftrag **Wechselkurse regulieren** ausführen. Dadurch ist sichergestellt, dass jede Transaktion mithilfe der entsprechenden Bewertungsmethode wie in Deutschland erforderlich reguliert wird. Dadurch werden außerdem zwei Felder auf der Anforderungsseite aktiviert, in denen Sie die zwei Datumswerte angeben können, die verwendet werden müssen, um die Regulierung zu berechnen. Die Felder werden in der folgenden Tabelle beschrieben.  

|Feld|Description|  
|---------------------------------|---------------------------------------|  
|**Bewertungsreferenzdatum**|Gibt das Basisdatum an, das verwendet wird, um zu berechnen, welche Posten kurzfristige Posten sind.|  
|**Kurzfristige Verbindlichkeiten bis**|Gibt das Datum an, das kurzfristige Posten von langfristigen Posten trennt. Kurzfristige Posten können ein Fälligkeitsdatum aufweisen, das vor oder an diesem Datum liegt. Der Standardwert ist der Wert des Feldes **Bewertungsreferenzdatum** plus ein Jahr.|  

## <a name="see-also"></a>Siehe auch  
[Währungswechselkurse aktualisieren](../../finance-how-update-currencies.md)  
[Einrichten einer zusätzlichen Berichtswährung](../../finance-how-setup-additional-currencies.md)
