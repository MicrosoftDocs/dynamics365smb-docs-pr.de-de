---
title: EU-Drittanbieter-Einkaufstransaktionen
description: 'In diesem Artikel wird erläutert, wie Sie Einkaufstransaktionen mit Drittanbietern innerhalb der Europäischen Union (EU) einrichten und verwenden.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.form: '50, 51, 52, 187, 317'
ms.search.keywords: 'EU3P, EU 3-P, EU 3-Party'
ms.date: 07/05/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="eu-third-party-purchase-transactions"></a>EU-Drittanbieter-Einkaufstransaktionen

Ein Dreiecksgeschäft in der Europäischen Union (EU) liegt vor, wenn Sie eine Kaufrechnung von einem Kunden in einem EU-Land/einer EU-Region erhalten und die Produkte in ein anderes EU-Land/eine andere EU-Region versandt werden, ohne dass das Wohnsitzland betreten wird. Der Transaktionsbetrag kann separat identifiziert und gemeldet werden, um den Anforderungen einiger EU-Länder/-Regionen an die Mehrwertsteuermeldung (MwSt.) und an das MwSt.-Informationsaustauschsystem (VIES) zu entsprechen. Microsoft Dynamics 365 Business Central ermöglicht die Einrichtung von Kauftransaktionen als EU-Dreiecksgeschäft. Gebuchte Transaktionen mit EU-Drittländern können in den Umsatzsteuerabrechnungen gefiltert und vom Betrag in der Spalte **Verkäufe an Kunden** des Berichts **Zusammenfassende Meldung** ausgeschlossen werden.

Auch wenn die Funktion als Erweiterung vorinstalliert ist, ist sie standardmäßig nicht aktiviert. Befolgen Sie diese Schritte, um die Funktion zu aktivieren.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, wechseln Sie zum Arbeitsbereich **Funktionsverwaltung**, und wählen Sie dann den entsprechenden Link aus.
2. In der Liste, suchen und wählen Sie **Funktionsaktualisierung: Ersatz der bestehenden EU-Dreiecksgeschäftsfunktion durch die neue EU-Dreiecksgeschäftserweiterung** aus.
3. Wählen Sie in der Spalte **Aktiviert für** die Option **Alle Benutzer** aus.

> [!NOTE]
> Wenn Sie die deutsche oder italienische Lokalisierung verwenden, können Sie diese App nicht aktivieren, da sie mit bestimmten Mehrwertsteuerfunktionen in diesen Lokalisierungen nicht kompatibel ist.  

## <a name="enable-eu-third-party-trade-functionality-for-a-purchase"></a>Aktivieren Sie die EU-Drittanbieter-Handelsfunktion für einen Kauf

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Geben Sie **MwSt.-Einrichtung** ein und wählen Sie dann den zugehörigen Link aus.
2. Markieren Sie auf der Seite **MwSt.-Einrichtung** das Feld **EU-Dreiecksgeschäft aktivieren**.

## <a name="use-eu-third-party-trade-functionality"></a>Nutzen Sie die EU-Dreiecksgeschäftsfunktion

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Einkaufsrechnung** (oder einen anderen Einkaufsbeleg) ein, und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie eine vorhandene Einkaufsrechnung aus, oder wählen Sie **Neu**, um eine neue zu erstellen.
3. Aktivieren Sie im Inforegister **Rechnungsdetails** das Kontrollkästchen **EU-Dreiecksgeschäft**.
4. Wählen Sie **OK** aus.

## <a name="include-or-exclude-eu-third-party-trade-records-on-the-vat-statement"></a>Fügen Sie Datensätze für EU-Dreiecksgeschäfte in die Mehrwertsteuerabrechnung ein oder schließen Sie sie aus

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **MwSt.-Abrechnung** ein, und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie auf der Seite **Mehrwertsteuererklärung** eine der folgenden Optionen aus, um mithilfe des Felds **EU-Dreiecksgeschäftsfilter** Datensätze für EU-Dreiecksgeschäfte anzuzeigen.

    | Option | Description |
    |--------|-------------|
    | Alle | Alle Datensätze anzeigen, unabhängig davon, ob das Feld **EU-Dreiecksgeschäft** in Belegen markiert wurde. |
    | EU3 | Nur Datensätze anzeigen, wo das Feld **EU-Dreiecksgeschäft** in Belegen markiert wurde. |
    | Nicht-EU3 | Nur Datensätze anzeigen, wo das Feld **EU-Dreiecksgeschäft** in Belegen nicht markiert wurde. |


## <a name="see-also"></a>Siehe auch
[Finanzmanagement](finance.md)  
[Arbeiten mit Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
