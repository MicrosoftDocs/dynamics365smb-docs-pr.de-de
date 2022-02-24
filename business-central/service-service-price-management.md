---
title: Servicepreismanagement | Microsoft Docs
description: In diesem Thema wird beschrieben, wie Sie den Serviceaufträgen die besten Preise zuzuordnen, individuelle Preisvereinbarungen mit Kunden einzurichten, die Effizienz der Servicemitarbeiter zu verbessern und den Rechnungsstellungsprozess zu beschleunigen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: cc5593c1ff9f0de1cfabe5deaa903f6b99dc0e64
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192411"
---
# <a name="service-price-management"></a>Servicepreismanagement
Die Funktionalität "Servicepreismanagement" erlaubt Ihnen, den Serviceaufträgen die besten Preise zuzuordnen, individuelle Preisvereinbarungen mit Kunden einzurichten, die Effizienz der Servicemitarbeiter zu verbessern und den Rechnungsstellungsprozess zu beschleunigen.  
  
Mit dem Servicepreismanagement können Sie verschiedene Servicepreisgruppen einrichten und dabei den Serviceartikel oder die Serviceartikelgruppe sowie den Problemcode der Serviceaufgabe berücksichtigen. Sie können diese Gruppen für begrenzte Zeiträume oder für bestimmte Kunden oder Währungen einrichten. Sie können Preiskalkulationsstrukturen als Vorlagen verwenden, um einer bestimmen Serviceaufgabe einen bestimten Preis zuzuordnen.  
  
Damit können beispielsweise bestimmte Serviceartikel sowie der Arbeitstyp bei Servicepreisen berücksichtigt werden. Zudem können auch unterschiedliche MwSt.- und Rabattbeträge in den Servicepreisgruppen verwendet werden. Um sicherzustellen, dass der richtige Preis angewendet wird, können – je nach Vereinbarung mit dem Kunden – feste, minimale und maximale Preise zugewiesen werden.  
  
Bevor die Servicepreiskorrektur für einen Serviceartikel in einem Serviceauftrag durchgeführt wird, wird eine Übersicht über das Ergebnis der Preiskorrektur angezeigt. Sie können diese Ergebnisse bestätigen oder weitere Änderungen vornehmen, wenn Sie ein anderes Ergebnis wünschen. Die gesamte Korrektur wird Zeile für Zeile vorgenommen, d. h. es werden keine zusätzlichen Zeilen hinzugefügt.  
  
Statistiken für die Servicepreisgruppen und Berichte erlauben Ihnen, die Profitabilität jeder Servicepreisgruppe zu verfolgen.  
  
## <a name="service-price-adjustment-groups"></a>Servicepreiskorrekturgruppen  
Sie verwenden Servicepreiskorrekturgruppen, um verschiedene Arten von Preiskorrekturen einzurichten. Sie können beispielsweise eine Servicepreiskorrekturgruppe für Ersatzteile einrichten, eine für Ressourcen, eine für Kosten usw. Sie können darüber hinaus festlegen, ob die Servicepreiskorrektur nur für einen bestimmten Artikel oder eine bestimmte Ressource oder für alle Artikel und Ressourcen gelten soll.  
  
Jede Servicepreiskorrekturgruppe enthält Informationen darüber, welche Korrekturen Sie in den Servicezeilen vornehmen möchten.  
  
Die Funktion "Preiskorrektur" wird bei Serviceartikeln, die zu Serviceverträgen gehören, nicht angewendet. Sie können nur Servicepreise von Artikeln korrigieren, die Teil eines Serviceauftrages sind. Sie können nicht den Preis eines Serviceartikels korrigieren, wenn dieser noch Garantie hat. Sie können den Preis eines Serviceartikels in einem Serviceauftrag nicht korrigieren, wenn die damit verknüpfte Servicezeile ganz oder teilweise als Rechnung gebucht wurde.  
  
Wenn Sie die Funktion "Servicepreise korrigieren" aufrufen, werden alle Rabatte im Auftrag durch die Werte der Servicepreiskorrektur ersetzt.  
  
## <a name="service-price-groups"></a>Servicepreisgruppen  
Sie können Servicepreisgruppen einrichten, um Gruppen von Serviceartikeln zu bilden, die derselben Servicepreisgestaltung unterliegen. Nachdem Sie Servicepreisgruppen eingerichtet haben, können Sie diese mit Serviceartikeln in Serviceartikelzeilen verbinden. Servicepreisgruppen können auch mit Serviceartikelgruppen verbunden werden.  
  
Bevor Sie eine Servicepreisgruppe einem Serviceartikel zuweisen, müssen Sie festlegen, auf welchen Problembereichscode, welche Währung oder welche Servicepreiskorrekturgruppe die Servicepreisgruppe Anwendung findet. Sie müssen festlegen, auf welchen Betrag der Servicepreis korrigiert werden soll und ob dieser Betrag inklusive MwSt. und Rabatt sein soll. Darüber hinaus müssen Sie festlegen, ob diese Korrektur einen festen Betrag betrifft oder nur unter bestimmten Bedingungen angewendet werden soll.  
  
Wenn Sie einem Serviceartikel eine Servicepreisgruppe zuweisen, dann gelten alle in dieser Gruppe eingerichteten Bedingungen für diesen Serviceartikel.  
  
## <a name="service-pricing"></a>Servicepreise  
Sie richten die eigentlichen Servicepreisarten (Preiskorrekturart und Preis) für eine Kombination aus Servicepreisgruppen und Debitorpreisgruppen ein. Sie wählen für jede Art von Servicepreisgestaltung eine Servicepreiskorrekturgruppe. Des Weiteren legen Sie die Servicepreiskorrekturart (Fix, Maximum oder Minimum) sowie den tatsächlichen Preis fest.  
  
Sie können z. B. Arten von Servicepreisen für eine Radioservicepreisgruppe einrichten. Für Debitoren, die keiner Preisgruppe zugewiesen wurden, können Sie festlegen, dass für Serviceleistungen ein maximaler Preis berechnet werden soll (= Preiskorrekturgruppe für Serviceleistungen). Für Debitoren, die einer bestimmten Preisgruppe zugewiesen wurden, können Sie festlegen, dass für Serviceleistungen ein fixer Preis berechnet werden soll, dieselbe Preisausorrekturgruppe für Serviceleistungen.  
  
## <a name="service-price-adjustment"></a>Servicepreiskorrekturen  
Die Servicepreiskorrektur ermöglicht Ihnen, die Preise für Artikel, Ressourcen, dem Sachkonto oder den Kosten in einem Serviceauftrag zu korrigieren.  
  
Nachdem Sie einen Artikel in die Serviceartikelzeile eingegeben haben, erfassen Sie alle Informationen über die Kosten für diesen Artikel in den Servicezeilen. Wenn Sie die Funktion "Servicepreis korrigieren" ausführen, können Sie die Preiskorrekturen in der Vorschau sehen. Sie können hier bei Bedarf Änderungen vornehmen. Wenn Sie die Änderungen bestätigen, werden die Korrekturen berechnet und in die Servicezeilen übertragen. Dann buchen Sie den Serviceauftrag.  
  
Abhängig von der Art der Servicepreiskorrektur wird der Gesamtbetrag der Korrekturen wie folgt berechnet:  
  
Die Berechnungen sind in der folgenden Tabelle beschrieben.  
  
|Option | Description |  
|----------------------------------|---------------------------------------|  
|**Fester Preis**|Das bedeutet, dass Sie einen festen Preis für Serviceartikel, Ressourcen, das Sachkonto oder die Kosten in Rechnung stellen, ungeachtet der tatsächlichen Kosten. Mit dieser Option wird die Servicepreiskorrektur genau auf den angegebenen Betrag in der Servicepreisgruppe durchgeführt.|  
|**Maximum**|Damit legen Sie, ungeachtet der tatsächlichen Kosten, einen Höchstbetrag für den Rechnungsbetrag für den Kunden fest. Bei dieser Option wird nur dann eine Servicepreiskorrektur durchgeführt, wenn der Gesamtbetrag den in der Servicepreisgruppe angegebenen Betrag übersteigt.|  
|**Minimum**|Das bedeutet, dass Sie, ungeachtet der tatsächlichen Kosten, eine Untergrenze definieren. Bei dieser Option werden Servicepreiskorrekturen nur durchgeführt, wenn der Gesamtbetrag geringer ist als der Betrag, der in der Servicepreisgruppe angegeben wurde.|  
  
## <a name="see-also"></a>Siehe auch  
[Einrichten von Preisen und zusätzlichen Kosten für Services](service-how-setup-service-costs-pricing.md)  
[Einrichten der Serviceverwaltung](service-setup-service.md)  
