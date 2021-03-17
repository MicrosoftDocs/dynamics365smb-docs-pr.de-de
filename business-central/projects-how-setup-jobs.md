---
title: Preise und Projektbuchungsgruppen einrichten| Microsoft Docs
description: Beschreibt, wie allgemeine Projektinformationen und Preise für Projektartikel, Ressourcen und Sachkonten und Projektbuchungsgruppen eingerichtet werden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 04f5538b7c904b64c921cc50f64924bcaef93401
ms.sourcegitcommit: a9b771cc2b4b75aed835efca63ef7a6a44219d59
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/18/2021
ms.locfileid: "5476770"
---
# <a name="set-up-jobs"></a>Einrichten von Projekten

Als Projekt-Manager können Sie Projekte einrichten, die jedes der Projekte definieren, das Sie in [!INCLUDE[prod_short](includes/prod_short.md)] verwalten. Auf der Seite **Projekteinrichtung** müssen Sie festlegen, wie Sie bestimmte Projektfunktionen verwenden möchten.

Für jedes Projekt geben Sie dann die einzelnen Projektkarten mit Informationen zu Preisen für Projektressourcen Projektartikel, Projekt und Sachkonten an, und Sie müssen Projektbuchungsgruppen einrichten.

## <a name="to-set-general-information-for-jobs"></a>Um allgemeine Informationen für Projekte einzurichten:
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Projekteinrichtung** ein, und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Dies Auswirkungen des Felds **Verbrauchslink standardmäßig anwenden** sind sehr umfangreich und werden deshalb im folgenden Abschnitt erläutert.

### <a name="to-set-up-job-usage-tracking"></a>Projektverbrauch-Nachverfolgung einrichten

Wenn Sie ein Projekt erstellen, werden Sie wissen wollen, ob Ihr Verbrauch mit dem Plan übereinstimmt. Um diesen Vorgang zu vereinfachen, können Sie einen Link zwischen Ihren Projektplanungszeilen und dem tatsächlichen Verbrauch erstellen. So können Sie Ihre Kosten verfolgen und schnell sehen, wie viel Arbeit noch zu tun ist. Standardmäßig ist de Projektplanungszeilentyp **Plan**, aber die Verwendung der Zeilenart **Plan und fakturierbar** hat ähnliche Effekte.

Wenn Sie das Feld **Verbraucherlink standardmäßig anwenden** ausgewählt haben, können Sie die Projektplanungszeile überprüfen. Sie können die Menge der Ressource, des Artikels oder des Sachkontos einrichten und dann festlegen, welche Menge Sie in das Projektbuchungsblatt übertragen möchten. Das Feld **Restmenge** auf der Projektplanungszeile zeigt Ihnen an, was noch übertragen und im Buchungsblatt gebucht werden muss.

> [!TIP]  
> Sie können Projektverbrauch-Nachverfolgung für ein bestimmtes Projekt aktivieren oder deaktivieren. Der Wert des Felds **Verbrauchslink anwenden** auf der neuen Projektkarte setzt die Einstellung auf der Seite **Projekteinrichtung** außer Kraft.  

Wenn das Kontrollkästchen **Verbrauchslink standardmäßig anwenden** aktiviert ist und die Projektplanungszeile auf **Fakturierbar** eingestellt ist, wird eine Projektplanungszeile vom Typ **Plan** erstellt, nachdem Sie eine Projektbuchungsblattzeile gebucht haben.

> [!IMPORTANT]
> Wenn Projektverbrauch-Nachverfolgung aktiviert ist, entweder auf der Seite **Projekteinrichtung** oder im einzelnen Projekt, und das Feld **Projekttyp** in der Projektjournalzeile leer ist, dann werden die neuen Projektplanungszeilen der Zeilenart **Plan** erstellt, wenn Sie Projektjournalzeilen buchen.  
>  
> Wenn Projektverbrauch-Nachverfolgung *nicht* aktiviert ist, entweder auf der Seite **Projekteinrichtung** oder im einzelnen Projekt, und das Feld **Projekttyp** in der Projektjournalzeile leer ist, dann werden keine Projektplanungszeilen erstellt, wenn Sie Projektjournalzeilen buchen. Weitere Informationen finden Sie unter [Nutzung von Projekten](projects-how-record-job-usage.md).

1. Wählen Sie das Symbol ![Seite suchen oder Bericht](media/ui-search/search_small.png "Suchen Sie nach dem Symbol Seite oder Bericht"), geben Sie **Jobs einrichten** ein und wählen Sie dann den entsprechenden Link.
2. Aktivieren sie das Kontrollkästen **Verbrauchslink standardmäßig anwenden**.

## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-jobs"></a>Erstellen projektspezifischer Preise für Ressourcen, Artikel und Sachkonten für Projekte
> [!NOTE]
> In Veröffentlichungszyklus 2 von 2020 haben wir neue Prozesse zum Einrichten und Verwalten von Preisen und Rabatten veröffentlicht. Wenn Sie ein neuer Kunde sind, nutzen Sie die neue Erfahrung. Wenn Sie bereits Kunde sind, hängt es davon ab, ob Sie die neue Erfahrung verwenden, ob Ihr Administrator die Funktionsaktualisierung **Neues Verkaufspreiserlebnis** in **Funktionsverwaltung** akualisiert hat. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management).

Sie können Preise für die Artikel, Ressourcen und Sachkonten für Projekte einrichten. 

#### <a name="current-experience"></a>[Aktuelle Erfahrung](#tab/current-experience)
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Projekte** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Ressource**, **Artikel** oder **Sachkonto** aus.
3. Füllen Sie auf den Seiten **Res.-VK-Preise Projekt**, **Projektartikelpreise**, oder **Projekt-Sachkontopreise** die Felder nach Bedarf aus.

Die folgende Tabelle zeigt, wie die Informationen in den optionalen Feldern in Jobplanungszeilen und Journalen verwendet werden, wenn die Ressource, das Element oder das Hauptbuchkonto für den Job ausgewählt werden.

|Spalte1  |Spalte2  |
|---------|---------|
|**Projektressourcen**|Die Felder **Projektaufgabennr.**, **Arbeitstyp**, **Währungscode**, **Zeilenrabatt %** und **Einstandspreis**. Der Wert im Feld **VK-Preis** für die Ressource wird in den Projektplanungszeilen und Projektbuchungsblättern verwendet, wenn diese Ressource, eine der Ressourcengruppe zugeordnete Ressource bzw. eine beliebige Ressource eingegeben wird. Beachten Sie, dass dieser Preis immer Vorrang vor allen Preisen hat, die auf der vorhandenen Seite des Typs **Ressourcen-VK-Preis/Ressourcengruppen-VK-Preise** eingerichtet sind.|
|**Projektartikel**|Die Felder **Projektaufgabennr.**, **Währungscode** und **Zeilenrabatt %**. Dies ist der Wert im Feld **VK-Preis** der in den Projektplanungszeilen und Projektbuchungsblättern verwendet wird, wenn dieser Artikel eingegeben wird. Beachten Sie, dass dieser Preis immer Vorrang vor dem regulären Kundenpreis (Mechanismus für „bester Preis“) für Artikel hat. Wenn Sie den Mechanismus für den regulären Debitorenpreis verwendet wollen, erstellen Sie keine Projektartikelpreise für das Projekt.|
|**Sachkonten**|Die Informationen in den Feldern **Projektaufgabennr.**, **Währungscode**, **Zeilenrabatt %**, **Einheitskostenfaktor** und **Einheitskosten** werden auf den Projektplanungszeilen und Verbrauchsbuchungsblättern verwendet, wenn diese Ressource eingegeben und dem Projekt hinzugefügt wird. Füllen Sie das Feld **VK-Preis** für das Aufwandssachkonto aus. Dies ist der Verkaufspreis, der in den Projektplanungszeilen und Projektbuchungsblättern verwendet wird, wenn dieses Sachkonto eingegeben wird.|

---
#### <a name="new-experience"></a>[Neue Erfahrung](#tab/new-experience)
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Projekte** ein und wählen Sie dann den entsprechenden Link.  
2. Markieren Sie den entsprechenden Job und wählen Sie dann die Aktion **Verkaufspreislisten**.

---

## <a name="to-set-up-job-posting-groups"></a>Projektbuchungsgruppen einrichten
Ein Aspekt der Projektenplanung besteht darin, zu entscheiden, welche Buchungskonten für die Projektkalkulation verwendet werden. Damit Projekte gebucht werden können, müssen Sie Konten für die Buchung für jede Projektbuchungsgruppe einrichten. Eine Buchungsgruppe stellt eine Verknüpfung zwischen dem Projekt und der Art dar, wie es in der Finanzbuchhaltung zu behandeln ist. Wenn Sie ein Projekt erstellen, geben Sie eine Buchungsgruppe an, und standardmäßig wird jede Aufgabe, die Sie erstellen, dieser Buchungsgruppe zugeordnet. Wenn Sie Aufgaben erstellen, können Sie jedoch die Voreinstellung überschreiben und eine Buchungsgruppe auswählen, die geeigneter ist.  

> [!NOTE]  
>   Die erforderlichen Konten der Kontenliste müssen eingegeben, bevor Sie Buchungsgruppen einrichten können. Weitere Informationen finden Sie unter [Einrichten oder ändern des Kontenplans](finance-setup-chart-accounts.md).  

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Projekt-Buchungsgruppen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu** und füllen Sie dann die Kontenfelder wie in der folgenden Tabelle beschrieben aus.  

| Das Feld "Konto" | Beschreibung |
| --- | --- |
| **Code** |Ein Code für die Buchungsgruppe. Sie können bis zu 10 Zeichen, einschließlich Leerzeichen, eingeben. |
| **Konto f. Kosten n. abgs. Arb.** |Das WIP-Konto für die berechneten Kosten der Projekt-WIP, bei dem es sich um ein Bilanz-Aktivkonto für Kapital handelt. |
| **Konto f. aufgel. Kosten n. abgs. Arb.** |Ein Konto für die Methode "Einstandswert" oder "Vertriebskosten" der WIP-Berechnung, bei dem es sich um ein Bilanz-Passivkonto für aufgelaufene Ausgaben handelt. Auf dieses Konto wird gebucht, wenn die WIP-Regulierung eine Erhöhung der auf dem Konto für Gewinn und Verlust gebuchten Verbrauchskosten erfordert. |
| **Projektkostenausgleich-Konto** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Konto für ausgeglichene Artikelpreise** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Konto für ausgeglichene Ressourcenpreise** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Kostenausgleich-Konto** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Projektkostenregulierung-Konto** |Das Gegenkonto zum WIP-Konto für aufgelaufene Kosten, bei dem es sich um ein Aufwandskonto handelt. |
| **Aufwandssachkonto (Budget)** |Das Verkaufskonto, das für Aufwandssachposten in Projektaufgaben mit dieser Buchungsgruppe verwendet werden soll. Wenn dieses Feld leer gelassen wird, wird das für die Projektplanungszeile eingegebene Hauptbuchungskonto verwendet. |
| **Konto f. aufgel. Verkäufe n. abgs. Arb.** |Das WIP-Konto für den berechneten Verkaufswert der WIP, bei dem es sich um ein Bilanzblatt für aufgelaufene Einnahmen handelt. Auf dieses Konto wird gebucht, wenn die WIP-Regulierung eine Erhöhung der deklarierten Einnahmen erfordert. |
| **Konto f. fakt. Verkäufe n. abgs. Arb.** |Das Konto für den fakturierten WIP-Verkaufswert, der nicht deklariert werden kann. Es handelt sich dabei um ein Bilanzblatt für nicht realisierte Einnahmen. |
| **Projektverkaufsausgleich-Konto** |Das Gegenkonto zum WIP-Konto für fakturierte Verkäufe, bei dem es sich um ein Ertragsgegenkonto handelt. |
| **Projektverkaufsregulierungs-** Konto |Das Gegenkonto zum WIP-Konto für den Umsatz, bei dem es sich um ein Ertragskonto handelt. |
| **Konto deklarierte Kosten** |Das Aufwandskonto, das die deklarierten Kosten für das Projekt enthält. Dabei handelt es sich normalerweise um ein Soll-Aufwandskonto. |
| **Konto deklarierte Verkäufe** |Das Ertragskonto, das den deklarierten Umsatz für das Projekt enthält. Dabei handelt es sich normalerweise um ein Haben-Ertragskonto. |

## <a name="see-also"></a>Siehe auch

[Projektmanagement einrichten](projects-setup-projects.md)  
[Video: So erstellen Sie ein Projekt in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Projekte verwalten](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]