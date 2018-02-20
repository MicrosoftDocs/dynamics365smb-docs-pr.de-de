---
title: Preise und Projektbuchungsgruppen einrichten| Microsoft Docs
description: "Beschreibt, wie allgemeine Projektinformationen und Preise für Projektartikel, Ressourcen und Sachkonten und Projektbuchungsgruppen eingerichtet werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2c57b2bd4b4c99373d4ce16905fbf626e549bc1f
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-jobs"></a>Einrichten von Projekten
Im Fenster **Projekteinrichtung** müssen Sie festlegen, wie Sie bestimmte Projektfunktionen verwenden möchten.

In den einzelnen Projektkarten müssen Sie Preise für Projektressourcen Projektartikel, Projekt und Sachkonten einrichten, und müssen Sie Projektbuchungsgruppen einrichten.

## <a name="to-set-general-information-for-jobs"></a>Um allgemeine Informationen für Projekte einzurichten:
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt einrichten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Das Kontrollkästchen **Verbrauchslink anwenden** ist sehr umfangreich und wird deshalb im folgenden Abschnitt erläutert.

## <a name="to-set-up-job-usage-tracking"></a>Projektverbrauch-Nachverfolgung einrichten
Wenn Sie ein Projekt erstellen, werden Sie wissen wollen, ob Ihr Verbrauch mit dem Plan übereinstimmt. Um diesen Vorgang zu vereinfachen, können Sie einen Link zwischen Ihren Projektplanungszeilen und dem tatsächlichen Verbrauch erstellen. So können Sie Ihre Kosten verfolgen und schnell sehen, wie viel Arbeit noch zu tun ist. Standardmäßig ist de Projektplanungszeilentyp **Plan**, aber die Verwendung der Zeilenart **Plan und fakturierbar** hat ähnliche Effekte.

Wenn Sie das Kontrollkästchen **Verbraucherlink anwenden** ausgewählt haben, können Sie die Projektplanungszeile überprüfen. Sie können die Menge der Ressource, des Artikels oder des Sachkontos einrichten und dann festlegen, welche Menge Sie in das Projektbuchungsblatt übertragen möchten. Das Feld **Restmenge** auf der Projektplanungszeile zeigt Ihnen an, was noch übertragen und im Buchungsblatt gebucht werden muss.

Wenn das Kontrollkästchen **Verbrauchslink anwenden** aktiviert ist und die Projektplanungszeile auf **Fakturierbar** eingestellt ist, wird eine Projektplanungszeile vom Typ **Plan** erstellt, nachdem Sie die Buchungsblattzeile gebucht haben.

> [!NOTE]  
>   Wenn das Kontrollkästchen **Verbrauchslink anwenden** auf der Projektkarte ausgewählt ist, und das Feld Projekttyp in der P**rojektjournalzeile** leer ist, dann werden die neuen Projektplanungszeilen der Zeilenart **Plan** erstellt, wenn Sie Projektjournalzeilen buchen. Wenn das Kontrollkästchen **Verbrauchslink anwenden** auf der **Projektkarte** nicht aktiviert ist und das Feld in der Projektjournalzeile leer ist, werden keine neuen Projektplanungszeilen erstellt, wenn Sie Projektjournalzeilen buchen. Weitere Informationen finden Sie unter [Nutzung von Projekten](projects-how-record-job-usage.md).

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt einrichten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Aktivieren oder deaktivieren sie das Kontrollkästen **Verbrauchslink anwenden**.

> [!NOTE]  
>   Sie können eine andere Einstellungen aus dem Kontrollkästchen **Verbrauchslink anwenden** in den einzelnen Projektkarten vornehmen. In diesem Argument setzt die Einstellung für dieses Projekt den allgemeinen, oben beschriebenen Standard außer Kraft.

## <a name="to-set-up-prices-for-job-resources"></a>So richten Sie Verkaufspreise für Projektressourcen ein
Sie können bestimmte Verkaufspreise für Ressourcen für ein Projekt einrichten. Dazu verwenden Sie das Fenster **Res.-VK-Preise Projekt**.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Ressource** aus.
3. Füllen Sie im Fenster **Projektressourcen-Preise** die notwendigen Felder aus.

Die optionalen Informationen in den Feldern **Projektaufgabennr.**, **Arbeitstyp**, **Währungscode**, **Zeilenrabatt %** und **Einstandspreisfaktor** werden auf den Projektplanungszeilen und Verbrauchsbuchungsblättern verwendet, wenn diese Ressource eingegeben und dem Projekt hinzugefügt wird.  

Der Wert im Feld **Einheitspreis** für die Ressource wird in den Projektplanungszeilen und Projektbuchungsblättern verwendet, wenn diese Ressource, eine der Ressourcengruppe zugeordnete Ressource bzw. eine beliebige Ressource eingegeben wird.  

> [!NOTE]  
>   Dieser Preis hat immer Vorrang vor allen Preisen, die in vorhandenen Tabellen des Typs **Ressourcen-VK-Preis/Ressourcengruppen-VK-Preis** eingerichtet sind.

## <a name="to-set-up-prices-for-job-items"></a>So richten Sie Preise für Projektartikel ein
Sie können bestimmte Preise für Artikel für ein Projekt einrichten. Dazu verwenden Sie das Fenster **Projektartikelpreise**.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Artikel** aus.
3. Füllen Sie im Fenster **Projektressourcen-Artikel** die notwendigen Felder aus.

Die optionalen Informationen in den Feldern **Projektaufgabennummer**, **Währungscode** und **Zeilenrabatt %** werden in den Projektplanungszeilen und Projektbuchungsblättern verwendet, wenn dieser Artikel eingegeben wird.  

Dies ist der Wert im Feld **Einheitspreis** der in den Projektplanungszeilen und Projektbuchungsblättern verwendet wird, wenn dieser Artikel eingegeben wird.  

> [!NOTE]  
>   Dieser Preis hat immer Vorrang vor dem regulären Kundenpreis (Mechanismus für "bester Preis") für Artikel. Wenn Sie den Mechanismus für den regulären Kundenpreis verwendet wollen, erstellen Sie keine Projektartikelpreise für das Projekt.

## <a name="to-set-up-prices-for-job-general-ledger-accounts"></a>Preise für Projektbuchungskonten einrichten
Sie können bestimmte Preise für die Aufwandssachposten eines Projekts einrichten. Dazu verwenden Sie das Fenster **Projekt-Sachkontopreise**.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Sachkonto** aus.  
3. Füllen Sie im Fenster **Sachkonto-Preise** die notwendigen Felder aus.

Die optionalen Informationen in den Feldern **Projektaufgabennr.**, **Währungscode**, **Zeilenrabatt %**, **Einheitskostenfaktor** und **Einheitskosten** werden auf den Projektplanungszeilen und Verbrauchsbuchungsblättern verwendet, wenn diese Ressource eingegeben und dem Projekt hinzugefügt wird.  

Füllen Sie das Feld **Einheits-Preis** für das Aufwandssachkonto aus. Dies ist der Verkaufspreis, der in den Projektplanungszeilen und Projektbuchungsblättern verwendet wird, wenn dieses Sachkonto eingegeben wird.

## <a name="to-set-up-job-posting-groups"></a>Projektbuchungsgruppen einrichten
Ein Aspekt der Projektenplanung besteht darin, zu entscheiden, welche Buchungskonten für die Projektkalkulation verwendet werden. Damit Projekte gebucht werden können, müssen Sie Konten für die Buchung für jede Projektbuchungsgruppe einrichten. Eine Buchungsgruppe stellt eine Verknüpfung zwischen dem Projekt und der Art dar, wie es in der Finanzbuchhaltung zu behandeln ist. Wenn Sie ein Projekt erstellen, geben Sie eine Buchungsgruppe an, und standardmäßig wird jede Aufgabe, die Sie erstellen, dieser Buchungsgruppe zugeordnet. Wenn Sie Aufgaben erstellen, können Sie jedoch die Voreinstellung überschreiben und eine Buchungsgruppe auswählen, die geeigneter ist.  

> [!NOTE]  
>   Die erforderlichen Konten der Kontenliste müssen eingegeben, bevor Sie Buchungsgruppen einrichten können. Weitere Informationen finden Sie unter [Einrichten oder ändern des Kontenplans](finance-setup-chart-accounts.md).  

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt-Buchungsgruppe** ein. Wählen Sie dann den zugehörigen Link aus.  
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
| **Projektverkaufsregulierungs-**Konto |Das Gegenkonto zum WIP-Konto für den Umsatz, bei dem es sich um ein Ertragskonto handelt. |
| **Konto deklarierte Kosten** |Das Aufwandskonto, das die deklarierten Kosten für das Projekt enthält. Dabei handelt es sich normalerweise um ein Soll-Aufwandskonto. |
| **Konto deklarierte Verkäufe** |Das Ertragskonto, das den deklarierten Umsatz für das Projekt enthält. Dabei handelt es sich normalerweise um ein Haben-Ertragskonto. |

## <a name="see-also"></a>Siehe auch
[Projektmanagement einrichten](projects-setup-projects.md)  
[Projekte verwalten](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

