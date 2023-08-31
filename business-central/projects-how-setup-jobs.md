---
title: 'Jobs, Preise und Buchungsgruppen festlegen'
description: 'Beschreibt, wie allgemeine Informationen zu Projekten eingerichtet werden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 04/25/2023
ms.custom: bap-template
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
---
# Jobs, Preise und Buchungsgruppen festlegen

Als Projekt-Manager können Sie Projekte einrichten, die jedes der Projekte definieren, das Sie in [!INCLUDE[prod_short](includes/prod_short.md)] verwalten. Verwenden Sie die Seite **Projekt Einrichtung**, um festzulegen, wie Sie Projektfeatures verwenden.

Geben Sie für jedes Projekt verschiedene Informationen an:

* Preise für Projektartikel
* Projektressourcen
* Projektsachkonten
* Projektbuchungsgruppen (falls erforderlich)

## Um allgemeine Informationen für Projekte einzurichten:

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Projekt Einrichtung** ein und wählen Sie den zugehörigen Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Der Umschalter **Verbrauchslink standardmäßig anwenden** auf der Seite **Projekt Einrichtung** zeigt an, ob Projektsachkontoeinträge standardmäßig mit Projektplanungszeilen verknüpft werden. Aktivieren Sie den Umschalter, um diese Einstellung auf alle neuen Projekte anzuwenden. Sie können die Nachverfolgung des Projektverbrauchs für ein bestimmtes Projekt aktivieren oder deaktivieren, indem Sie den Umschalter **Verbrauchslink anwenden** auf der Seite **Projektkarte** ein- oder ausschalten.

### Projektverbrauch-Nachverfolgung einrichten

Wenn Sie an einem Projekt arbeiten, möchten Sie vielleicht wissen, wie sich Ihr Verbrauch im Vergleich zu Ihrem Plan verhält. Um den Verbrauch herauszufinden, können Sie einen Link zwischen Ihren Projektplanungszeilen und dem tatsächlichen Verbrauch erstellen. Über den Link können Sie Ihre Kosten verfolgen und nachvollziehen, wie viel Arbeit noch übrig ist. Standardmäßig ist de Projektplanungszeilentyp **Plan**, aber die Verwendung der Zeilenart **Plan und fakturierbar** hat ähnliche Effekte.

Nachdem Sie die Verbrauchsverfolgung über den Umschalter **Verbrauchsverknüpfung standardmäßig anwenden** aktiviert haben, können Sie die Informationen der Projektplanungszeile überprüfen. Beispielsweise können Sie die Menge der Ressource, des Artikels oder des Sachkontos festlegen. Sie können auch die Menge festlegen, die Sie an das Projekt Buch.-Blatt übertragen möchten. Das Feld **Restmenge** auf der Projektplanungszeile zeigt Ihnen an, was noch übertragen und im Projekt Buch.-Blatt gebucht werden muss.

>[!NOTE]
> Wenn die **Verbrauchsverknüpfung anwenden** auf dem einzelnen Projekt gewählt wird und das Feld **Zeilentyp** auf der Projekt Buch.-Blatt oder Einkaufszeile **Fakturierbar** ist, dann werden neue Projektplanungszeilen des Zeilentyps **Sowohl Budget als auch fakturierbar** erstellt, wenn Sie das Projekt Buch.-Blatt oder den Einkaufsbeleg buchen.  
>
> Weitere Informationen finden Sie unter [Datensätze für Aufträge](projects-how-record-job-usage.md) und [Auftragsvorräte verwalten](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Wenn Sie im Feld **Zeilentyp** auf der Zeile für die Projekt Buchungsblattzeile oder den Kauf keinen Wert angeben, werden keine Projektplanungszeilen erstellt, wenn Sie das Projekt Buch.-Blatt oder den Einkaufsbeleg buchen.

## Erstellen projektspezifischer Preise für Ressourcen, Artikel und Sachkonten für Projekte

> [!NOTE]
> In der 2020er Release-Welle 2 haben wir neue Prozesse zum Einrichten und Verwalten von Preisen und Rabatten freigegeben. Wenn Sie ein neuer Kunde sind, nutzen Sie die neue Erfahrung. Wenn Sie bereits Kunde sind, hängt es davon ab, ob Sie die neue Erfahrung verwenden, ob Ihr Administrator die Funktionsaktualisierung **Neues Verkaufspreiserlebnis** in **Funktionsverwaltung** akualisiert hat. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management).

Sie können Preise für die Artikel, Ressourcen und Sachkonten für Projekte einrichten. 

#### [Aktuelle Erfahrung](#tab/current-experience)

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Ressource**, **Artikel** oder **Sachkonto** aus.
3. Füllen Sie auf den Seiten **Res.-VK-Preise Projekt**, **Projektartikelpreise**, oder **Projekt-Sachkontopreise** die Felder nach Bedarf aus.

Wenn Sie ein Ressourcen-, Artikel- oder Sachbuchkonto für ein Projekt auswählen, verwendet [!INCLUDE [prod_short](includes/prod_short.md)] Informationen in den optionalen Feldern in Projektplanungszeilen und Projekt Buch.-Blatt. Die folgende Tabelle erläutert, wie.

|Spalte1  |Spalte2  |
|---------|---------|
|**Projektressourcen**|Die Felder **Projektaufgabennr.**, **Arbeitstyp**, **Währungscode**, **Zeilenrabatt %** und **Einstandspreis**. Der Wert im Feld **Einzelpreis** für die Ressource wird in den Projektplanungszeilen und Projekt Buch.-Blätter verwendet, wenn Sie eine Ressource oder eine der Ressourcengruppe zugeordnete Ressource eingeben. Dieser Preis überschreibt immer die auf der Seite **Ressourcen-VK-Preis/Ressourcengruppen-VK-Preise** angegebenen Preise.|
|**Projektartikel**|Die Felder **Projektaufgabennr.**, **Währungscode** und **Zeilenrabatt %**. Dies ist der Wert im Feld **VK-Preis** der in den Projektplanungszeilen und Projektbuchungsblättern verwendet wird, wenn dieser Artikel eingegeben wird. Dieser Preis hat Vorrang vor dem regulären Debitorenpreis (Mechanismus für „bester Preis“) für Artikel. Um den regulären Debitorenpreis zu verwenden, geben Sie keine Projektartikelpreise für den Projekt an.|
|**Sachkonten**|Die Informationen in den Feldern **Projektaufgabennr.**, **Währungscode**, **Zeilenrabatt %**, **Einheitskostenfaktor** und **Einheitskosten** werden auf den Projektplanungszeilen und Verbrauchsbuchungsblättern verwendet, wenn diese Ressource eingegeben und dem Projekt hinzugefügt wird. Wenn Sie ein Sachkonto auswählen, verwenden Projektplanungszeilen und Projekt Buch.-Blätter den Wert im Feld **Einzelpreis** für das Aufwandssachkonto.|

#### [Neue Erfahrung](#tab/new-experience)

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Markieren Sie den entsprechenden Job und wählen Sie dann die Aktion **Verkaufspreislisten**.

---

## Projektbuchungsgruppen einrichten

Ein Aspekt der Projektenplanung besteht darin, zu entscheiden, welche Buchungskonten für die Projektkalkulation verwendet werden. Damit Projekte gebucht werden können, müssen Sie Konten für die Buchung für jede Projektbuchungsgruppe einrichten. Eine Buchungsgruppe stellt eine Verknüpfung zwischen dem Projekt und der Art dar, wie es in der Finanzbuchhaltung zu behandeln ist. Wenn Sie ein Projekt erstellen, geben Sie eine Buchungsgruppe an, und standardmäßig wird jede Aufgabe, die Sie erstellen, dieser Buchungsgruppe zugeordnet. Wenn Sie Aufgaben erstellen, können Sie jedoch die Voreinstellung überschreiben und eine Buchungsgruppe auswählen, die geeigneter ist.  

> [!NOTE]  
> Sie müssen die Konten in den Kontenplan eingegeben, bevor Sie Buchungsgruppen einrichten können. Weitere Informationen finden Sie unter [Einrichten oder ändern des Kontenplans](finance-setup-chart-accounts.md).  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Projektbuchungsgruppen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** und füllen Sie dann die Felder wie in der folgenden Tabelle beschrieben aus.  

| Das Feld "Konto" | Description |
| --- | --- |
| **Code** |Eine Kennung für die Buchungsgruppe. Sie können bis zu 10 Zeichen, einschließlich Leerzeichen, eingeben. |
| **Konto f. Kosten n. abgs. Arb.** |Das WIP-Konto für die berechneten Kosten der Projekt-WIP, bei dem es sich um ein Bilanz-Aktivkonto für Kapital handelt. |
| **Konto f. aufgel. Kosten n. abgs. Arb.** |Ein Konto für die Einstandswert- oder Vertriebskostenmethode der WIP-Berechnung. Dieses Konto ist für die aufgelaufene Kosten in Ihrer Bilanz. Wenn die WIP-Regulierung erfordert, dass Sie die Verbrauchsosten, die Sie in Ihrer Gewinn- und Verlustrechnung buchen, erhöhen, buchen Sie dies auf dieses Konto. |
| **Projektkostenausgleich-Konto** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Konto für ausgeglichene Artikelpreise** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Konto für ausgeglichene Ressourcenpreise** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Kostenausgleich-Konto** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Projektkostenregulierung-Konto** |Das Gegenkonto zum WIP-Konto für aufgelaufene Kosten, bei dem es sich um ein Aufwandskonto handelt. |
| **Aufwandssachkonto (Budget)** |Das Verkaufskonto, das für Aufwandssachposten in Projektaufgaben mit dieser Buchungsgruppe verwendet werden soll. Wenn dieses Feld leer gelassen wird, wird das für die Projektplanungszeile eingegebene Hauptbuchungskonto verwendet. |
| **Konto f. aufgel. Verkäufe n. abgs. Arb.** |Das WIP-Konto für den berechneten Verkaufswert der WIP, bei dem es sich um ein Konto für aufgelaufene Umsätze für Ihre Bilanz handelt. Wenn eine WIP-Regulierung erfordert, dass Sie die anerkannten Umsätze erhöhen, buchen Sie dies auf dieses Konto. |
| **Konto f. fakt. Verkäufe n. abgs. Arb.** |Das Konto für den fakturierten WIP-Verkaufswert, der nicht deklariert werden kann. Es handelt sich dabei um ein Bilanzblatt für nicht realisierte Einnahmen. |
| **Projektverkaufsausgleich-Konto** |Das Gegenkonto zum WIP-Konto für fakturierte Verkäufe, bei dem es sich um ein Ertragsgegenkonto handelt. |
| **Projektverkaufsregulierungs-** Konto |Das Gegenkonto zum WIP-Konto für den Umsatz, bei dem es sich um ein Ertragskonto handelt. |
| **Konto deklarierte Kosten** |Das Aufwandskonto, das die deklarierten Kosten für das Projekt enthält. Dabei handelt es sich normalerweise um ein Soll-Aufwandskonto. |
| **Konto deklarierte Verkäufe** |Das Ertragskonto, das den deklarierten Umsatz für das Projekt enthält. Dabei handelt es sich normalerweise um ein Haben-Ertragskonto. |

## Siehe verwandte [Microsoft Schulungen](/training/paths/set-up-jobs-resources/)

## Siehe auch

[Projektmanagement einrichten](projects-setup-projects.md)  
[Video: Wie man einen Auftrag in Dynamics 365 Business Central erstellt](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Projekte verwalten](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
