---
title: Preisregulierungen von Artikeln verfolgen
description: 'Informieren Sie sich, wie Sie durch die Nachverfolgung von Artikelkostenanpassungen dafür sorgen können, dass Ihre Artikelkostendaten genau bleiben.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.search.form: null
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Preisregulierungen von Artikeln verfolgen

Es ist wichtig, die Artikelkosten genau zu halten und die Zeit zwischen der Buchung eines Eintrags und der Berücksichtigung der Kosten im Hauptbuch zu verkürzen. Sie können die Leistung der Kostenanpassungen für einzelne Anpassungsausführungen und Artikel verfolgen. Sollten Fehler auftreten, können Sie die problematischen Artikel identifizieren und Korrekturen vornehmen. Beispielsweise können Sie die Artikel von Berechnungen ausschließen, um sicherzustellen, dass Anpassungen für andere Artikel nicht unterbrochen werden. Sie können die Kosten für einzelne Artikel anpassen oder Stapel von Artikeln erstellen und diese alle gleichzeitig anpassen.

## Mit der Verfolgung von Kostenanpassungen beginnen

Der Einstieg ist ganz einfach. Auf der Seite **Lagereinrichtung** bietet das Feld **Protokollierung der Einstandspreisregulierung** einige Optionen:

* **Deaktiviert** bedeutet, dass Sie keine Kostenanpassungsausführungen protokollieren.
* **Nur Fehler** bedeutet, dass nur die Ausführungen protokolliert werden, die fehlgeschlagen sind.
* **Alle** bedeutet, alle Ausführungen zu protokollieren.

> [!NOTE]
> Um die Größe des Protokolls zu minimieren, protokolliert [!INCLUDE [prod_short](includes/prod_short.md)] nicht die Anpassungen, die automatisch erfolgen, wenn jemand einen Artikel postet.

Sie müssen außerdem den Aufgabenwarteschlangeneintrag **Lagerkosten buchen (1002)** einrichten. Dieser Aufgabenwarteschlangeneintrag passt die Kosten automatisch gemäß einem Zeitplan an. Mehr Informationen über Aufgabenwarteschlangeneinträge erhalten Sie unter [Aufgabenwarteschlangen für die Aufgabenplanung verwenden](admin-job-queues-schedule-tasks.md).

## Kostenanpassungen verwalten

Verwenden Sie die Seite **Lagerkostenregulierung**, um den Kostenregulierungsprozess zu verwalten und zu überwachen. Auf dieser Seite werden Artikel zusammen mit ihren Kostenparametern und dem Kostenregulierungsstatus angezeigt. Sie können die Liste filtern, um sich auf Elemente zu konzentrieren, die angepasst werden müssen oder die vom Kostenanpassungsprozess ausgeschlossen sind.

### Info zu Artikelstapeln

Sie können die Kostenanpassung für mehrere Artikel durchführen, indem Sie diese in Stapeln gruppieren. Mithilfe von Stapeln ist es beispielsweise einfacher, einige Artikel separat anzupassen, da die Anpassung länger dauert. Mithilfe von Stapeln können Sie außerdem problematische Artikel identifizieren.

Um einen Stapel zu erstellen, führen Sie auf der Seite **Lagerkostenregulierung** einen der folgenden Schritte aus:

* Wählen Sie die Artikel in der Liste, anschließend **Einstandspreisregulierung ausführen** und dann **Stapel hinzufügen** aus.
* Um einen Stapel anzulegen und die Kostenanpassung sofort auszuführen, markieren Sie die Artikel in der Liste, wählen Sie **Einstandspreisregulierung ausführen** und dann **Stapel hinzufügen und ausführen** aus.
* Wählen Sie **Einstandspreisregulierung ausführen** und dann **Artikelchargen** aus und geben Sie dann einen Filter in das Feld **Artikelfilter** ein.
  
> [!TIP]
> Um schnell einen weiteren Stapel für alle Artikel zu erstellen, die noch nicht in einem Stapel enthalten sind, wählen Sie auf der Seite **Einstandspreisregulierung – Artikelchargen** die Option **Fehlende Elemente hinzufügen** aus.

Wenn eine Ausführung für einen Stapel abgeschlossen ist, hat der Stapel einen der folgenden Status auf der Seite **Artikelchargen**:

* **Erfolg**: Die Kostenanpassung ist erfolgreich.
* **Fehlgeschlagen**: Wenn die Kostenanpassung fehlschlägt, identifiziert [!INCLUDE [prod_short](includes/prod_short.md)] den Artikel, der den Fehler verursacht hat, und teilt dann den aktuellen Stapel in zwei Teile auf. Eine Charge mit dem problematischen Artikel und eine weitere mit den restlichen Artikeln. Die Kostenanpassung wird für den Stapel mit den verbleibenden Artikeln erneut ausgeführt. Wenn dies erneut fehlschlägt, wird der Vorgang wiederholt. Sie legen die maximale Anzahl der Teilungen im Feld **Max. Wiederholungsversuche** fest. Der Standardwert für Wiederholungsversuche beträgt 10, Sie können jedoch ein neues Limit eingeben.
* **Zeitlimit überschritten**: Wenn die Kostenanpassung für einen Stapel nicht innerhalb des im Feld **Timeout (Minuten)** (im Bereich von 1 bis 720 Minuten) angegebenen Zeitraums abgeschlossen wird, wird die Sitzung beendet und die Änderungen werden rückgängig gemacht. [!INCLUDE [prod_short](includes/prod_short.md)] teilt anschließend den aktuellen Stapel in zwei Hälften und führt den Kostenanpassungsprozess für jede Hälfte erneut aus. Dieser Vorgang wird fortgesetzt, bis die Kostenanpassung erfolgreich ist oder die maximale Anzahl an Wiederholungsversuchen erreicht ist.

> [TIPP!] Jeder Stapel wird in einer separaten Sitzung ausgeführt. Um den Fortschritt zu überwachen, verwenden Sie die Aktion **Aktualisieren**.

### Einstandspreisregulierung ausführen

Verwenden Sie die Seite **Lagerkostenregulierung**, um Anpassungen vorzunehmen.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol, geben Sie **Lagerkostenregulierung** ein, und wählen Sie dann den zugehörigen Link aus.
1. Je nachdem, was Sie tun möchten, verwenden Sie eine der folgenden Optionen:

  * Wählen Sie für ein oder mehrere Artikel sofort die Artikel in der Liste aus und wählen Sie dann **Einstandspreisregulierung ausführen** aus.
  * Verwenden Sie für Stapel eine der folgenden Optionen:

    * Um einen Stapel anzulegen und die Kosten sofort anzupassen, wählen Sie die Artikel in der Liste, dann **Einstandspreisregulierung ausführen** und anschließend **Stapel hinzufügen und ausführen** aus.
    * Um es für alle Stapel auszuführen, wählen Sie **Einstandspreisregulierung ausführen**, **Artikelchargen** und dann **Ausführen** aus.
    
    Weitere Informationen zu Stapeln finden Sie unter [Info zu Artikelstapeln](#about-item-batches).

### Artikeldetails entdecken

Verwenden Sie das Menü **Artikel**, um auf Informationen zu Kostenanpassungen für einen ausgewählten Artikel zuzugreifen.

* **Artikelposten**: Listet Artikelposten für den Artikel auf. Mit der Aktion **Zur Regulierung markieren** können Sie die erneute Ausführung der Kostenanpassung für Artikel erzwingen, die direkt oder indirekt mit den von Ihnen ausgewählten eingehenden Einträgen verknüpft sind. Das Erzwingen einer Wiederholung kann hilfreich sein, wenn frühere Ausführungen zu falschen Kosten geführt haben.
* **Werteinträge**: Werteinträge für den Artikel auflisten.
* **Einstiegspunkte der Einstandspreisregulierung**: Öffnen Sie die Seite **Durchschnittlicher Kostenanpassungs-Einstiegspunkt**, die Sie hauptsächlich zur Berechnung der Durchschnittskosten verwenden. Auf der Seite werden Kombinationen aus Artikeln, Standorten, Varianten und Bewertungsdaten angezeigt, für die Kostenanpassungen durchgeführt werden oder durchgeführt werden müssen.
* **Einstandspreisregulierungsbestellungen**: Öffnen Sie die **Lagerregulierungspostenaufträge**, auf der Sie Produktions- und Montageaufträge anpassen. Es zeigt, dass die Aufträge angepasst wurden oder angepasst werden müssen.

### Ergebnis anzeigen

Verwenden Sie das Menü **Protokoll pro**, um das Ergebnis der Kostenanpassungen anzuzeigen:

* **Ausführen**: Kostenanpassungsprotokolle für jede Ausführung anzeigen. Das Protokoll enthält Daten über den Artikelfilter, den Status (Erfolg/Fehlgeschlagen/Zeitlimit überschritten), Start- und Enddatum/-zeit, Dauer und die durch die Ausführung verursachten Kostenunterschiede.
* **Artikel**: Detaillierte Informationen zum Anpassungsprozess für den ausgewählten Artikel anzeigen.

### Artikel in Anpassungen einschließen oder daraus ausschließen

Wenn ein oder mehrere Artikel fehlschlagen, können Sie die Artikel von der Anpassungsausführung ausschließen und sie dann in spätere Ausführungen einbeziehen. Wählen Sie eine der folgenden Optionen im Menü **Funktionen** aus:

* **Artikel von der Regulierung ausschließen** und **Artikel in Regulierung einbeziehen**: Kostenanpassung für einen ausgewählten Artikel vorübergehend deaktivieren und dann wieder aktivieren. Durch die Kostenanpassung bleiben die Kosten für andere Artikel weiterhin korrekt, während Sie ein Problem mit einem bestimmten Artikel untersuchen.

## Angepasste Kosten im Hauptbuch buchen

Normalerweise werden neue Werteinräge entsprechend dem Zeitplan für den Aufgabenwarteschlangeneintrag **Lagerkosten buchen (1002)** ins Hauptbuch gebucht. Sie können jedoch von der Seite **Lagerkostenregulierung** aus sofort Anpassungen im Hauptbuch vornehmen. Wählen Sie im Menü **Funktionen** die Option **Lagerkosten buchen** aus.

## Fehler bei Kostenanpassungen beheben

Verwenden Sie die folgenden Optionen im Menü **Diagnose** aus, um Probleme mit Kostenanpassungsausführungen zu beheben.

* **Artikeldaten exportieren**: Artikelbezogene Daten in eine Textdatei exportieren. Sie können die Datei für weitere Analysen in einer Sandbox-Umgebung verwenden oder sie an eine Supportanfrage anhängen, wenn Sie Probleme mit der Kostenberechnung untersuchen.
* **Artikeldaten importieren**: Importiert die zuvor exportierte Textdatei zurück in die Datenbank. Diese Aktion ist nur in Sandbox-Umgebungen oder Evaluierungsunternehmen aktiviert.
* **Einstandspreis zurücksetzen – wird reguliert**: Setzen Sie den Schalter **Einstandspreis ist reguliert** für Artikel, Produktionsaufträge oder Montageaufträge zurück. Mit dieser Einstellung können Sie für sie eine erneute Ausführung der Kostenanpassung erzwingen.
* **Bericht zur Erkennung von Kostenproblemen**: Diagnostizieren Sie typische Datenprobleme, die zu Berechnungsfehlern bei der Kostenrechnung führen. Es prüft, ob die Artikelposten, Wertposten, Artikelanwendungseinträge und Kapazitätsposten korrekt sind.
* **Artikeldaten löschen**: Alle artikelbezogenen Tabellen in der Datenbank löschen. Diese Aktion ist nur in Sandbox-Umgebungen oder Evaluierungsunternehmen verfügbar.

## Siehe auch

[Artikelpreise anpassen](inventory-how-adjust-item-costs.md)  
[Designdetails: Lagerregulierung](design-details-cost-adjustment.md)  
