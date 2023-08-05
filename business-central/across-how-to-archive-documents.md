---
title: Archivieren von Einkaufs- und Kaufbelegen
description: 'Sie können Verkaufs- und Einkaufsaufträge, Angebote, Rücklieferungen und Rahmenaufträge archivieren und bei Bedarf die Originale wiederherstellen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 06/02/2023
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
---
# Beleg archivieren

Sie können Verkaufs- und Einkaufsaufträge, Angebote, Rücklieferungen und Rahmenaufträge archivieren. Durch das Archivieren von Belegen können Sie das Original bei Bedarf wiederherstellen. Sie können ein Verkaufs- oder Einkaufsbeleg mehrmals archivieren, wobei Sie jedes Mal eine andere archivierte Version speichern.

Für archivierte Verkaufsbelege, deren Original noch vorhanden und das nicht gebucht ist, können Sie die Aktion **Wiederherstellen** verwenden, um den aktuellen Beleg durch eine archivierte Version überschreiben.

Bei archivierten Belegen, deren Original gelöscht ist, können Sie den Inhalt nur durch Kopieren der Daten wiederverwenden, z. B. mit der Aktion **Aus Beleg kopieren**.  

## So richten Sie die automatische Archivierung von Belegen ein

Sie können die automatische Archivierung von Verkaufsaufträgen und Einkaufsbestellungen, Angeboten, Rahmenbestellungen und Verkaufsreklamationen einrichten. Wenn die automatische Archivierung aktiviert ist, wird eine neue Version des archivierten Dokuments erstellt, wenn ein Benutzer die folgenden Aktionen ausführt:

* Ändern oder Löschen eines Belegs
* Drucken, Herunterladen oder Senden eines Belegs per E-Mail
* Umwandeln eines Angebots in eine Bestellung oder eine Rechnung
* Buchen einer Bestellung

Nachfolgend wird beschrieben, wie die automatische Archivierung von Verkaufsbelegen eingerichtet wird. Die Schritte sind für eine Einkaufsdokumente ähnlich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Einrichtung Debitoren & Verkauf** ein und wählen Sie dann den entsprechenden Link.
2. Legen Sie im Inforegister **Archivierung** fest, ob die automatische Archivierung für die verschiedenen Typen von Verkaufsbeleg aktiviert werden soll. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

In der folgenden Tabelle werden die Optionen für das Feld **Angebote archivieren** beschrieben.

|Option|Description|
|------|-----------|
|**Nie**| Archivieren Sie keine Verkaufsangebote, wenn sie gelöscht werden.|
|**Frage**|Fordern Sie den Benutzer dazu auf, festzulegen, ob Verkaufsangebote archiviert werden sollen, wenn sie gelöscht werden.|
|**Immer**|Archivieren Sie Verkaufsangebote automatisch, wenn sie gelöscht werden.|

## So archivieren Sie einen Verkaufsauftrag manuell

Nachfolgend wird beschrieben, wie Sie einen Verkaufsauftrag manuell archivieren. Die Schritte sind für alle Aufträge, Rahmenaufträge, Rücklieferungen und Angebote ähnlich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie einen Verkaufsauftrag für Artikel, die Sie archivierne möchten.  
3. Wählen Sie die **Beleg archivieren**-Aktion aus.

Der Auftrag ist archiviert. Sie können sie auf der Seite **Archivierte Verkaufsaufträge** anzeigen.

## So stellen Sie einen nicht gebuchten Verkaufsauftrag aus dem Archiv wieder her

Die folgende Vorgehensweise beschreibt, wie Sie aus einem archivierten Verkaufsauftrag den ursprünglichen Verkaufsauftrag wiederherstellen. Das Wiederherstellen eines Belegs ist nur möglich, wenn der Originalbeleg nicht gebucht wurde. Die Schritte sind für alle Aufträge, Rahmenaufträge, Rücklieferungen und Angebote ähnlich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsauftragsarchive** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den archivierten Verkaufsauftrag oder eine Version davon aus, die Sie wiederherstellen möchten, und wählen Sie dann die Aktion **Wiederherstellen** aus.  

Die Inhalte des ursprünglichen Verkaufsauftrags werden durch die archivierte Version ersetzt.

## Archivierte Auftragsversionen löschen

Verwenden Sie eine Aufbewahrungsrichtlinie, um archivierte Dokumente zu bereinigen, die Sie nicht mehr benötigen. Mithilfe von Aufbewahrungsrichtlinien können Administratoren festlegen, wie lange sie Daten speichern möchten. Sie können beispielsweise eine Richtlinie einrichten, durch die Daten nach einem Ablaufdatum gelöscht werden. Weitere Informationen finden Sie unter [Aufbewahrungsrichtlinien definieren](admin-data-retention-policies.md).

Beim Erstellen von Aufbewahrungsrichtlinien für archivierte Dokumente sind einige Dinge zu beachten:

* * Wenn das Originaldokument nicht gelöscht wurde, löscht Business Central die archivierten Versionen nicht. Archivierte Versionen verfallen nicht, solange das Original vorhanden ist.
* Wenn Sie die Aufbewahrungsrichtlinie einrichten, können Sie angeben, dass die Richtlinie alle archivierten Versionen eines Dokuments außer der aktuellsten löschen soll. Beispielsweise verfügen Sie möglicherweise über 10 Versionen eines Dokuments und möchten eine Kopie der neuesten Version behalten. 
* Business Central berechnet das Ablaufdatum für Dokumente basierend auf dem Datum der letzten archivierten Version.

## Siehe auch

[Belegzeilen nachverfolgen](across-how-to-track-document-lines.md)  
[Verkauf](sales-manage-sales.md)  
[Allgemeine Unternehmensfunktionen](ui-across-business-areas.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
