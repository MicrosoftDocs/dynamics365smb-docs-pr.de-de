---
title: Designdetails – Ändern der Lagerabgangsmethode für Artikel
description: Erfahren Sie, wie Sie einem Artikel eine andere Lagerabgangsmethode zuweisen, obwohl Sie den Artikel bereits in Transaktionen verwendet haben.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing methods, costing, item cost
ms.search.form: 8645
ms.date: 06/08/2021
ms.author: bholtorf
ms.openlocfilehash: 1f726a40e23fcfcc5d00616965111254ebcd14d8
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512334"
---
# <a name="design-details-change-the-costing-method-for-items"></a>Designdetails: Lagerabgangsmethode für Artikel ändern

In [!INCLUDE[prod_short](includes/prod_short.md)] können Sie eine Lagerabgangsmethode für einen Artikel nicht ändern, nachdem Sie den Artikel in eine Transaktion aufgenommen haben. Zum Beispiel, nachdem Sie den Artikel gekauft oder verkauft haben. Wenn dem Artikel oder den Artikeln eine falsche Lagerabgangsmethode zugewiesen wurde, können Sie das Problem möglicherweise erst feststellen, wenn Sie Ihre Finanzberichterstattung durchführen.

In diesem Thema wird beschrieben, wie Sie diese Situation beheben können. Der empfohlene Ansatz besteht darin, den Artikel mit der falschen Lagerabgangsmethode durch einen neuen Artikel zu ersetzen und mithilfe eines Montageauftrags den Lagerbestand vom alten auf den neuen Artikel zu übertragen.

> [!NOTE]
> Durch die Verwendung von Montageaufträgen können die Kosten weiterhin fließen, obwohl noch ausstehende Einkaufsrechnungen oder Versandkosten zu buchen sind. Darüber hinaus können Sie die Konvertierung rückgängig machen und bei Bedarf die Mengen der ursprünglichen Artikel zurückerhalten.

> [!TIP]
> Um sich mit dem Prozess vertraut zu machen, empfehlen wir, den Konvertierungsprozess mit einem einzelnen Artikel oder einer kleinen Gruppe von Artikeln zu starten.

## <a name="about-costing-methods"></a>Info zu Lagerabgangsmethoden

Kalkulationsmethoden steuern die Kostenberechnung, wenn Waren gekauft, in den Lagerbestand übernommen und verkauft werden. Lagerabgangsmethoden beeinflussen den Zeitpunkt der im COGS (Wareneinsatz) erfassten Beträge, die sich auf den Bruttogewinn auswirken. Dieser Fluss berechnet den COGS. Die Kosten der verkauften Waren (COGS) und die Umsätze werden wie folgt zur Ermittlung des Bruttogewinns verwendet:

*Bruttoertrag* = *Einnahmen - COGS*

Wenn Sie Lagerartikel einrichten, müssen Sie eine Kalkulationsmethode zuweisen. Die Methode kann von Unternehmen zu Unternehmen und von Artikel zu Artikel variieren. Daher ist es wichtig, die richtige auszuwählen. Die folgenden Lagerabgangsmethoden werden in [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt:

* Durchschnitt
* FIFO
* LIFO
* Standard
* Ausgewählt

Weitere Informationen finden Sie unter [Designdetails: Lagerabgangsmethoden](design-details-costing-methods.md).

## <a name="use-assembly-orders-to-change-costing-method-assignments"></a>Verwenden von Montageaufträgen zum Ändern der Zuordnung von Lagerabgangsmethoden

In diesem Abschnitt werden die folgenden Schritte zum Ändern der einem Artikel zugewiesenen Lagerabgangsmethode beschrieben:

1. Definieren Sie eine standardmäßige Lagerabgangsmethode.
2. Identifizieren Sie die Artikel, für die die Lagerabgangsmethode geändert werden soll, und nummerieren Sie sie neu.
3. Erstellen Sie neue Artikel mit dem alten Nummerierungsschema, und kopieren Sie die Stammdaten in einem Stapel.
4. Kopieren Sie zugehörige Masterdaten manuell aus dem vorhandenen Artikel in den neuen Artikel.
5. Bestimmen Sie die Bestandsmenge, die vom ursprünglichen Artikel in den neuen Artikel konvertiert werden soll.
6. Übertragen Sie den Lagerbestand in den neuen Artikel.
7. Behandeln Sie Bestandsmengen, die der Nachfrage zugeordnet sind.
8. Blockieren Sie die weitere Verwendung des ursprünglichen Artikels.  

### <a name="define-a-default-costing-method"></a>Standardmäßige Lagerabgangsmethode definieren

Um zukünftige Fehler zu vermeiden, können Sie eine standardmmäßige Lagerabgangsmethode für neue Artikel angeben. Wenn jemand einen neuen Artikel erstellt, schlägt [!INCLUDE[prod_short](includes/prod_short.md)] immer die standardmäßige Lagerabgangsmethode vor. Sie können die standardmäßige Lagerabgangsmethode im Feld **Standardmäßige Lagerabgangsmethode** auf der Seite **Lagereinrichtung** festlegen. 

### <a name="identify-the-items-to-change-the-costing-method-for-and-renumber-them"></a>Identifizieren Sie die Artikel, für die die Lagerabgangsmethode geändert werden soll, und nummerieren Sie sie neu.

Möglicherweise möchten Sie Ihren neuen Artikeln die gleichen Nummern geben wie denen, die sie ersetzen. Ändern Sie dazu die Nummern der vorhandenen Elemente. Wenn die vorhandene Artikelnummer beispielsweise „P1000“ lautet, können Sie sie in „X-P1000“ ändern. Dies ist eine manuelle Änderung, die Sie für jeden Artikel vornehmen müssen.

### <a name="create-new-items-with-the-old-numbering-scheme-and-copy-the-master-data-in-a-batch"></a>Erstellen Sie neue Artikel mit dem alten Nummerierungsschema, und kopieren Sie die Masterdaten in einem Stapel.

Erstellen Sie die neuen Artikel mit dem aktuellen Nummernschema. Mit Ausnahme des Felds **Lagerabgangsmethode** sollten die neuen Artikel sollten die gleichen Masterdaten enthalten wie die vorhandenen Elemente. Verwenden Sie die Aktion **Element kopieren** auf der Seite **Artikelkarte** Seite, um die Masterdaten für den Artikel und zugehörige Daten aus anderen Funktionen zu übertragen. Weitere Informationen finden Sie unter [Kopieren Sie vorhandene Elemente, um neue Elemente zu erstellen](inventory-how-copy-items.md).

Nachdem Sie die neuen Artikel erstellt und die Masterdaten übertragen haben, weisen Sie die richtige Lagerabgangsmethode zu.

### <a name="manually-copy-related-master-data-from-the-original-item-to-the-new-item"></a>Kopieren Sie zugehörige Masterdaten manuell aus dem ursprünglichen in den neuen Artikel.

Damit die neuen Artikel vollständig verwendet werden können, müssen Sie einige Stammdaten aus anderen Bereichen manuell kopieren, wie in der folgenden Tabelle beschrieben.

|Bereich  |Zu kopieren  |Vorgehensweise  |
|---------|---------|---------|
|Lagerbestand |Lagerhaltungsdaten |Überprüfen Sie, ob für den ursprünglichen Artikel Lagerhaltungsdaten angegeben sind. Wenn für jede Lagerhaltungsdatenkarte Planungsparameter eingegeben wurden, müssen Sie die Lagerhaltungsdaten für den neuen Artikel manuell erstellen. Wenn die Parameter nicht angegeben sind, können Sie den Stapelverarbeitungsauftrag **Lagerhaltungsdaten erstellen** auf der Seite **Artikelkarte** verwenden, um die Daten zu erstellen.|
| |Ersatzartikel |Überprüfen Sie, ob für den ursprügnlichen Artikel Ersatzartikel definiert sind. Falls ja, übertragen Sie diese Daten auf den neuen Artikel. Verwenden Sie die Aktion **Ersatzartikel** auf der Karte **Artikelkarte**, um Ersatzartikel anzuzeigen. |
| |Analyseberichte |Überprüfen Sie die Berichte „Artikelanalyse“, „Verkaufsanalyse“ und „Einkaufsanalyse“. Für diejenigen, die auf die ursprünglichen Artikel verweisen, können Sie entweder einen neuen Analysebericht mit einem Verweis auf den neuen Artikel erstellen (wobei der ursprüngliche Analysebericht als Verlauf verwendet wird) oder die Berichte so anpassen, dass sie auf den neuen Artikel verweisen. |
| |Standard Buch.-Blätter |Überprüfen Sie, ob Standard Buch.-Blätter auf den ursprünglichen Artikel verweisen, und übertragen Sie diese Daten bei Bedarf auf den neuen Artikel. Diese Informationen finden Sie in den Standard Buch.-Blättern, die im Artikel Buch.-Blatt verfügbar sind.  |
|Verkauf |Vorauszahlungsprozentsatz für Verkäufe | Überprüfen Sie, ob für den ursprünglichen Artikel Vorauszahlungsprozentsätze für Verkäufe definiert sind, und übertragen Sie diese Daten auf den neuen Artikel. Wählen Sie zum Anzeigen von Vorauszahlungsprozentsätzen für Verkäufe auf der Seite **Artikelkarte** die Option **Verkauf** und dann **Zahlungsprozentsätze** aus.|
|Einkauf |Vorauszahlungsprozentsatz für Einkäufe |Überprüfen Sie, ob für den ursprünglichen Artikel Vorauszahlungsprozentsätze für Einkäufe definiert sind, und übertragen Sie diese Daten auf den neuen Artikel. Wählen Sie zum Anzeigen von Vorauszahlungsprozentsätzen für Verkäufe auf der Seite **Artikelkarte** die Option **Einkäufe** und dann **Zahlungsprozentsätze** aus. |
|Logistik |Lagerplatzinhalt |Überprüfen Sie den für den ursprünglichen Artikel definierten Lagerplatzinhalt. Wenn Spalten wie „Min. Menge“, „Max. Menge“, „Standard“ und „Dediziert“ einzeln eingegeben wurden, müssen Sie anschließend den den Lagerplatzinhalt für den neuen Artikel manuell erstellen. Ist dies nicht der Fall, ist keine Aktion erforderlich. [!INCLUDE[prod_short](includes/prod_short.md)] verwaltet die Aufzeichnungen, wenn Sie Logistikbelege und Logistik Buch.-Blätter registrieren.|
|Projekt |Projektpreise |Überprüfen Sie, ob für den ursprünglichen Artikel Projektpreise definiert sind, und übertragen Sie diese Daten auf den neuen Artikel. Diese Informationen finden Sie auf der Seite **Projektkarte** im Abschnitt **Projektdetails – Anzahl Preise** des **Infoboxbereichs**. |
|Service |Qualifikationen der Serviceressourcen |Überprüfen Sie, ob für den ursprünglichen Artikel die Qualifikation der Serviceressourcen definiert ist, und übertragen Sie diese Daten auf den neuen Artikel. Verwenden Sie zum Anzeigen der Qualifikationen der Ressourcen die Aktion **Qualifikationen der Ressourcen** auf der Seite **Artikelkarte**.  |
| |Serviceartikelkomponenten |Überprüfen Sie, ob für den ursprünglichen Serviceartikel die Komponenten definiert sind, und übertragen Sie diese Daten auf den neuen Artikel. Zum Anzeigen der Komponenten von Serviceartikeln verwenden Sie auf der Seite **Artikelkarte** die Option **Serviceartikel**, um die Liste der zugehörigen Serviceartikel zu öffnen, und wählen Sie dann die Aktion **Komponenten** aus.  |
|Produktion |Fertigungsstücklisten |Überprüfen Sie, ob Fertigungsstücklisten den ursprünglichen Artikel enthalten, und ersetzen Sie ihn durch den neuen Artikel. Zum Ersetzen des ursprünglichen Artikels wählen Sie auf der Seite **Fertigungsstücklisten** die Aktion **Fertigungsstückliste ersetzen** aus. |
|Montage |Montagestücklisten |Überprüfen Sie, ob Montagestücklisten den ursprünglichen Artikel enthalten, und ersetzen Sie ihn manuell durch den neuen Artikel. |

> [!IMPORTANT]
> Wenn die neue Lagerabgangsmethode „Standard“ lautet, sollten Sie einen Wert in das Feld eingeben **Einstandspreis (fest)** auf der Seite **Artikelkarte** eingeben. Auf der Seite **Einst.-Preis (fest) Arbeitsblatt** können Sie die Kostenanteile entsprechend festlegen. Weitere Informationen zum Erstellen von Erfassungen finden Sie unter [Standard-Buch.-Blätter aktualisieren](finance-how-to-update-standard-costs.md).

### <a name="determine-the-inventory-quantity-to-convert-from-the-original-item-to-the-new-item"></a>Bestandsmenge bestimmen, die vom ursprünglichen Artikel in den neuen Artikel konvertiert werden soll

> [!NOTE]
> In diesem Schritt werden keine Mengen berücksichtigt, die in nicht versendeten Bestellungen enthalten sind. Weitere Informationen finden Sie unter [Bestandsmengen verarbeiten, die der Nachfrage zugeordnet sind](design-details-changing-costing-methods.md#handle-inventory-quantities-that-are-allocated-to-demand). 

Verwenden Sie ein Inventur-Buch.-Blatt , um eine Liste der Mengen im Mengen im Lagerbestand zu erstellen. Verwenden Sie je nach Einrichtung des Lagerorts eine der folgenden Optionen:

* Inventur Buch.-Blätter
* Logistik Inventur Buch.-Blätter

Beide Blätter können die Lagermenge des Artikels berechnen, einschließlich Standort, Variante, Lagerplatz und Lagerort. Weitere Informationen finden Sie unter [Erfassen, Regulieren und Umbuchen von Lagerbestand mithilfe von Buch.-Blättern](inventory-how-count-adjust-reclassify.md)

### <a name="transfer-the-inventory-to-the-new-item"></a>Lagerbestand auf den neuen Artikel übertragen

Erstellen und buchen Sie Montageaufträge, um die Kosten und die Bestandsmenge vom ursprünglichen Artikel auf den neuen Artikel zu übertragen. Montageaufträge können einen Artikel in einen anderen umwandeln, wobei die Kosten erhalten bleiben. Auf diese Weise wird sichergestellt, dass die Nettosummen für das Bestandskonto und die COGS nicht betroffen sind (außer wenn die neue Lagerabgangsmethod auf „Standard“ festgelegt ist. In diesem Fall können die Kosten auf Abweichungskonten verteilt werden). Weitere Informationen finden Sie unter [Montageverwaltung](assembly-assemble-items.md).

Verwenden Sie beim Erstellen von Montageaufträgen die Informationen aus dem Inventur Buch.-Blatt oder dem Logistik Inventur Buch.-Blatt. In den folgenden Tabellen werden die Informationen in den Berichten beschrieben, die in die Kopfzeile und die Zeilen des Montageauftrags eingegeben werden sollen.

#### <a name="header"></a>Header

|Feld  |Einzugebender Wert  |
|---------|---------|
|Artikelnr. |Die Nummer des neuen Artikels. |
|Menge |Die Menge im Inventur-Buch.-Blatt.<br> **HINWEIS:** Die von den Inventur Buch.-Blättern berechneten Mengen enthalten nicht die Mengen, die sich auf Bestellungen befinden, die noch nicht versendet wurden.  |
|Variantencode |Identisch mit dem Inventur-Buch.-Blatt.  |
|Lagerortcode |Identisch mit dem Inventur-Buch.-Blatt. |
|Einheitencode |Identisch mit dem Inventur-Buch.-Blatt. |
|Lagerplatzcode |Identisch mit dem Inventur-Buch.-Blatt. |

#### <a name="lines"></a>Zeilen

|Feld  |Einzugebender Wert  |
|---------|---------|
|Typ |Artikel |
|Anzahl |Die Nummer des ursprünglichen Artikels. |
|Komponentenmenge |1 |
|Variantencode |Identisch mit dem Inventur-Buch.-Blatt. |
|Lagerortcode |Identisch mit dem Inventur-Buch.-Blatt. |
|Einheitencode |Identisch mit dem Inventur-Buch.-Blatt. |

> [!NOTE]
> Ein Montageauftrag kann jeweils nur die Lagerhaltungsdaten eines Artikels verarbeiten. Sie müssen einen Montageauftrag für jede Kombination von Lagerhaltungsdaten erstellen, die eine Menge im Lagerbestand haben.

> [!NOTE]
> Für einen Lagerort müssen Sie möglicherweise Kommissionierungen erstellen, bevor Sie den Montageauftrag buchen können. Überprüfen Sie die Einrichtung für Kommissionierungen auf der Seite **Standortkarte**, um dies zu untersuchen. Weitere Informationen finden Sie unter [Artikel und Standorte für die gesteuerte Einlagerung und Kommissionierung einrichten](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md)

### <a name="handle-inventory-quantities-that-are-allocated-to-demand"></a>Bestandsmengen verarbeiten, die der Nachfrage zugeordnet sind

Im Idealfall sollte der Lagerbestand für den ursprünglichen Artikel nach der Übertragung der Bestandsmengen auf Null gehen. Es können jedoch ausstehende Bestellungen, Arbeitsblätter und Buchungsblätter (siehe Tabelle unten) vorhanden sein, für die noch eine Menge des ursprünglichen Artikels erforderlich ist. Die Menge kann auch durch eine Reservierung oder Artikelverfolgung blockiert werden.

**Beispiel**: Im Lager befinden sich 1000 Stück. und 20 Stück sind für einen Kundenauftrag reserviert, der noch nicht versendet wurde. In diesem Fall können Sie die 20 Stück im alten Artikel behalten, sodass Sie die ausstehende Bestellung erfüllen können.

> [!NOTE]
> Es gibt Funktionsbereiche, die sich auf die Menge auswirken können, wie in der folgenden Tabelle aufgeführt. Daher kann es schwierig sein, die richtige Menge zu finden. Sie können im obigen Beispiel 100 Stück behalten und stattdessen die restlichen 900 Stück übertragen. Eine andere Möglichkeit wäre, die Belege und Buch.-Blätter zu verarbeiten, dass nur noch eine überschaubare Anzahl übrig bleibt. Eine weitere Alternative besteht darin, die gesamte Menge auf den neuen Artikel zu übertragen und dann einen Teil davon mithilfe des Montageauftrags wieder auf den ursprünglichen Artikel zu übertragen.

In der folgenden Tabelle sind Funktionsbereiche aufgeführt, in denen möglicherweise noch Mengen ausstehen.

|Ursprungs- / Bestimmungsregion  |Nach ausstehenden Mengen suchen  |
|---------|---------|
|Verkauf |Verkaufsbelege, einschließlich Bestellungen, Rücksendungen, Rechnungen, Angebote, Rahmenaufträge und Gutschriften |
|Lagerbestand |Artikel-Buch.-Blätter, Reservierungen, Artikelverfolgung und Einst.-Preis (fest) Arbeitsblatt |
|Einkauf |Einkaufsbelege, einschließlich Bestellungen, Rücksendungen, Rechnungen, Angebote, Rahmenaufträge und Gutschriften |
|Planung |Bestellarbeitsblatt, Planungsarbeitsblatt und Auftragsplanung |
|Logistik |Umlagerungsaufträge, Warenausgänge, Logistik Buch.-Blätter und Lagerkommissionierungen, Lagereinlagerungen und Umlagerungen, interne Kommissionierungen und Einlagerungen sowie Lagerplatz Erst.-Arbeitsblätter |
|Montage |Montagedokumente, einschließlich Bestellungen, Rücksendungen und Rahmenbestellungen |
|Projekte |Projektplanungszeilen und Projekt-Buch.-Blattzeilen |
|Service |Servicebelege und Serviceverträge |
|Produktion |Fertigungsauftrag (geplant, fest geplant und freigegeben) |

### <a name="block-the-original-item-from-further-use"></a>Verwendung des ursprünglichen Artikels blockieren

Wenn der Bestand für den ursprünglichen Artikel Null ist, können Sie den Artikel blockieren, um zu verhindern, dass er für neue Transaktionen verwendet wird. Wenn Sie den Artikel blockieren möchten, klicken Sie auf die Seite **Artikelkarte**, und aktivieren Sie das Kontrollkästchen **Blockiert**. Weitere Informationen finden Sie unter [Artikel aus Verkauf oder Einkauf sperren](inventory-how-block-items.md).

## <a name="summary"></a>Zusammenfassung

In [!INCLUDE[prod_short](includes/prod_short.md)] ist das Ändern der Lagerabgangsmethode für Artikel, die in Transaktionen verwendet wurden, ein Prozess und keine Standardaktion. Sie können die in diesem Thema beschriebenen Schritte als Vorlage für den Prozess verwenden.

Der Prozess kann zeitaufwändig sein, da mehrere manuelle Schritte erforderlich sind. Wenn Sie sich jedoch die Zeit nehmen, um den Prozess abzuschließen, werden die Auswirkungen von Fehlern auf die Finanzbuchhaltung minimiert.

Wir empfehlen Folgendes:

1. Bewerten Sie die Durchführbarkeit des Prozesses, indem Sie einen oder mehrere repräsentative Artikel den gesamten Prozess durchlaufen lassen.
2. Wenden Sie sich an einen erfahrenen Partner, der Ihnen bei diesem Prozess helfen kann.

## <a name="see-also"></a>Siehe auch

[Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)  
[Matrix](design-details-inventory-costing.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]