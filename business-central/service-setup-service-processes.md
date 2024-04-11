---
title: Servicemanagementprozesse einrichten
description: 'Erfahren Sie, wie Sie Vorgänge einrichten, die zur vollständigen Zufriedenheit Ihrer Debitoren mit Ihren Services beitragen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: 'service, number sequences, setup, warnings, fee, contracts, warranties'
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="configure-service-management-processes"></a>Servicemanagementprozesse konfigurieren

Es folgen einige Beispiele für Einstellungen, die Sie bei Servicemanagementprozessen anwenden können:  
  
* Einige allgemeine Einstellungen für mehrere Vorgänge, wie Warnungen, Berechnung des nächsten Service für Serviceartikel, die zu ermittelnde Grundgebühr, die zu verwendende Ebene des Problemberichtswesens und so weiter.  
* Die Art der Informationen, die Technikfachkräfte in Servicebelegen eingeben müssen. Beispielsweise können Sie fordern, dass die Art des Auftrags, das Anfangs- und/oder Enddatum der Arbeit und die Art der erledigten Arbeit angegeben werden müssen  
* Einige Standardeinstellungen für Reaktionszeiten und Garantien. Diese schließen eine Standardreaktionszeit für das Startdatum des Serviceauftrags, Garantierabattprozentsätze für Teile und Arbeit ein und wie lange Garantien gültig sind.  
* Einstellungen für Verträge, wie die maximale Anzahl der Tage, die Sie für Vertragsserviceaufträge verwenden können, ob Ursachencodes verwendet werden, wenn ein Vertrag gekündigt wird, Standardtexte für Beschreibungen und Vertragswerte.  
* Die Anzahl der zu verwendenden Reihenfolgen bei dienstbezogenen Belegen und Artikeln.  

## <a name="to-enter-general-and-mandatory-settings"></a>So geben Sie allgemeine und obligatorische Einstellungen ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Service Einrichtung** ein, und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="set-up-service-invoice-posting-policies-for-users"></a>Richtlinien für die Buchung von Servicerechnungen für Benutzende einrichten

Unternehmen haben oft einzigartige Prozesse für Rechnungen und Lieferungen. Beispielsweise können die Prozesse von einer Person, die alles auf einer Servicebestellung bucht, bis zu mehreren Mitarbeitenden variieren, wobei jeder auf seinen eigenen Seiten arbeitet.

Mithilfe von Buchungsrichtlinien können Sie Benutzende daran hindern, Servicerechnungen zu buchen, oder sie dazu verpflichten, Rechnungen zusammen mit der zugehörigen Servicelieferung zu buchen. Um eine Buchungsrichtlinie auf der Seite **Benutzereinrichtung** im Feld **Buchungsrichtlinie für Servicerechnung** einzurichten, wählen Sie eine der folgenden Optionen aus:

* **Zugelassen** (Standard): Behalten Sie das aktuelle Verhalten bei, bei dem ein Benutzender die zu verwendende Buchungsoption auswählen kann, z. B. **Liefern**, **Fakturieren** und **Liefern und fakturieren**.
* **Verboten**: Verhindert, dass Personen Servicerechnungen buchen. [!INCLUDE [prod_short](includes/prod_short.md)] zeigt einen Bestätigungsdialog an, der nur die Option **Liefern** bereitstellt.
* **Obligatorisch**: Ermöglichen Sie es Benutzenden, Rechnungen zusammen mit Servicelieferungen zu buchen. [!INCLUDE [prod_short](includes/prod_short.md)] zeigt einen Bestätigungsdialog an, der nur die Option **Liefern und fakturieren** bereitstellt.

Diese Einstellung wirkt sich auf auf die folgenden Belege aus:

* Serviceaufträge
* Warenausgänge
* Servicerechnungen
* Servicegutschriften

In der folgenden Tabelle werden die Auswirkungen auf die unterschiedlichen Belege beschrieben.

|Beleg  |Zulassen<br>Zeigt eine Reihe von Optionen an   |Untersagt<br>Bestätigungsdialog  |Obligatorisch<br>Bestätigungsdialog  |
|---------|---------|---------|---------|
|Serviceauftrag     | * Liefern<br>* Fakturieren<br>* Liefern und fakturieren<br>* Liefern und verbrauchen         |* Liefern<br>* Liefern und verbrauchen  |Möchten Sie die Lieferung und Rechnung buchen?         |
|Warenausgang     |* Liefern<br>* Liefern und fakturieren         |Möchten Sie die Lieferung buchen?         | Möchten Sie die Lieferung und Rechnung buchen?        |
|Servicerechnung     | Möchten Sie die Rechnung buchen?         | Fehler: Sie können keine Buchung vornehmen.       |Möchten Sie die Rechnung buchen?         |
|Servicegutschrift     | Möchten Sie die Gutschrift buchen?         | Fehler: Sie können keine Buchung vornehmen.        |Möchten Sie die Gutschrift buchen?         |

> [!NOTE]
> Wenn Sie Servicerechnungen und Gutschriften buchen, stehen Ihnen keine Buchungsoptionen zur Verfügung. In den Belegen werden die physischen und finanziellen Transaktionen immer gemeinsam gebucht. Sie können Servicerechnungen und Gutschriften nicht teilweise buchen.

## <a name="see-also"></a>Siehe auch

[Problemberichtswesen einrichten](service-how-setup-fault-reporting.md)  
[Ressourcenzuordnung einrichten](service-how-setup-resource-allocation.md)  
[Einrichten von Codes für Standardservices](service-how-setup-service-coding.md)  
[Einrichten zusätzlicher Kosten für Services](service-how-setup-service-costs-pricing.md)  
[Lösungsanleitung Einrichtung](service-how-setup-troubleshooting.md)  
[Service](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
