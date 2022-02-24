---
title: Inventurerfassung mit belegbasierten Funktionen | Microsoft Docs
description: Beschreibt, wie eine Inventurerfassung mithilfe der Seiten für die Inventurauftrags- und Inventurerfassung durchgeführt wird.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, status, negative, positive, increase, decrease
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 944ce9e3950ea64fafada118b6f99f5d891242a5
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182204"
---
# <a name="count-inventory-using-documents"></a>Erfassung des Lagerbestand mithilfe von Belegen
Sie können mithilfe der Inventurauftrags- und Inventurerfassungsbelege eine Inventur der Artikel durchführen. Die Seite **Inventurauftrag** wird verwendet, um das vollständige Inventurerfassungsprojekt zu organisieren, zum Beispiel eines pro Standort. Die Seite **Inventurerfassung** wird verwendet, um die tatsächliche Zählung von Artikeln mitzuteilen und zu erfassen. Sie können mehrere Aufzeichnungen für einen Auftrag erstellen, z. B. das Verteilen von Artikelgruppen an verschiedene Mitarbeiter.

Der Bericht **Inventurerfassung** kann aus jeder Erfassung gedruckt werden und enthält leere Mengenfelder zur Eingabe des gezählten Lagerbestands. Wenn ein Benutzer fertig mit der Erfassung ist und die Mengen auf der Seite **Inventurerfassung** eingegeben wurden, wählen Sie die Schaltfläche **Fertigstellen** aus. Dadurch werden die Mengen an die entsprechenden Zeilen der Seite **Inventurauftrag** übertragen. Durch diese Funktion ist sichergestellt, dass keine Artikelanzahl zweimal erfasst werden kann.      

> [!NOTE]
> Diese Vorgehensweise beschreibt, wie Sie eine Inventur mithilfe von Belegen durchführen, ein Verfahren, das eine größere Kontrolle bietet und die Verteilung der Erfassung auf mehrere Mitarbeiter unterstützt. Sie können die Aufgabe auch mithilfe von Buch.-Blättern durchführen, den Seiten **Inventur Buch.-Blätter** und **Logistik-Inventur-Buch.-Blatt** verwenden. Weitere Informationen finden Sie unter [Erfassen, Regulieren und Umbuchen von Lagerbestand mithilfe von Buch.-Blättern](inventory-how-count-adjust-reclassify.md)<br /><br />
> Hinweis: Wenn Sie die Funktionen für Lagerplätze oder Zonen verwenden, können Sie Inventuraufträge nicht verwenden. Verwenden Sie stattdessen die Seite **Logistik-Inventur-Buch.-Blatt**, um Ihre Lagerposten zu zählen, bevor Sie sie mit Artikelposten synchronisieren.

Das Erfassen des Lagerbestands mithilfe von Belegen besteht aus den folgenden Gesamtschritten:

1. Erstellen Sie einen Inventurauftrag mit den erwarteten vorab ausgefüllten Artikelmengen.
2. Generieren Sie eine oder mehrere Inventurerfassungen aus dem Auftrag.
3. Geben Sie die gezählten Artikelmengen zu den Erfassungen ein, wie beispielsweise auf den Ausdrucken erfasst, und legen Sie sie auf **Beendet** fest.
4. Schließen Sie den Inventurauftrag ab und buchen Sie ihn.

## <a name="to-create-a-physical-inventory-order"></a>So erstellen Sie einen Inventurauftrag
Auf Anwendungsebene ist ein Inventurauftrag ein vollständiger Beleg, der aus einem Inventurauftragskopf und einigen Inventurauftragszeilen besteht. Die Informationen im Inventurauftragskopf geben an, wie die Inventur durchgeführt werden soll. Die Inventurauftragszeilen enthalten Informationen über die Artikel und deren Lagerorte.

Um die Inventurauftragszeilen zu erstellen, verwenden Sie üblicherweise die Funktion **Zeilen berechnen**, um den aktuellen Lagerbestand als Zeilen auf dem Auftrag darzustellen. Alternativ können Sie die Funktion **Aus Beleg kopieren** verwenden, um die Zeilen mit dem Inhalt eines anderen offenen oder gebuchten Inventurauftrags zu füllen. Nachfolgend wird nur beschrieben, wie Sie die Funktion **Zeilen berechnen** verwenden.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Physische Inventuraufträge** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die erforderlichen Felder auf dem Inforegister **Allgemein** aus. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie die Aktion **Zeilen berechnen** aus.
5. Wählen Sie die Optionen nach Bedarf aus.
6. Richten Sie die Filter beispielsweise so ein, dass nur eine Teilmenge der Artikel bei der ersten Erfassung gezählt wird.

    > [!TIP]
    > Um mehrere Mitarbeiter für die Erfassung des Lagerbestands einzuplanen, ist es ratsam, jedes Mal verschiedene Filter festzulegen, wenn Sie die Aktion **Zeilen berechnen** verwenden, damit nur der Auftrag mit der Teilmenge von Lagerartikeln eingegeben wird, den der jeweilige Benutzer erfasst. Wenn Sie mehrere Inventurerfassungen für mehrere Mitarbeiter generieren, minimieren Sie das Risiko, dass Artikel zweimal gezählt werden. Weitere Informationen finden Sie im Abschnitt „So erstellen Sie eine Inventurerfassung”.

7.  Wählen Sie die Schaltfläche **OK** aus.

Eine Zeile für jeden Artikel, der im ausgewählten Lagerort und entsprechend der festgelegten Filter und Optionen vorhanden ist, wird im Auftrag eingefügt. Für Artikel, die in der Artikelverfolgung eingerichtet sind, wird das Kontrollkästchen **Artikelverfolgung verwenden** ausgewählt. Informationen über die erwartete Menge von Serien- und Chargennummern sind verfügbar, indem Sie die Aktion **Zeilen** und dann **Artikelverfolgungszeilen** auswählen. Weitere Informationen finden Sie im Abschnitt „Verarbeitung der Artikelverfolgung beim Erfassen des Lagerbestands”.

Sie können jetzt fortfahren, um mindestens eine Erfassung zu erstellen. Dabei handelt es sich um Anweisungen für die Mitarbeiter, die die eigentliche Inventur durchführen.  

## <a name="to-create-a-physical-inventory-recording"></a>So erstellen Sie eine Inventurerfassung
Sie können für jeden Inventurauftrag einen oder mehrere Inventurerfassungsbelege erstellen, auf dem bzw. denen Mitarbeiter die gezählten Mengen entweder manuell oder über ein integriertes Lesegerät eingeben können.

Standardmäßig wird die Erfassung aller Zeilen im zugehörigen Inventurauftrag erstellt. Um zu vermeiden, dass zwei Mitarbeiter dieselben Artikel bei der verteilten Zählung erfassen, ist es ratsam, den Inventurauftrag nach und nach auszufüllen, indem Sie die Filter im Batchauftrag **Zeilen berechnen** festlegen (siehe Abschnitt „So erstellen Sie einen Inventurauftrag”) und dann die Inventurerfassung erstellen, während Sie das Kontrollkästchen **Nur nicht erfasste Zeilen** auswählen. Durch diese Einstellungen wird sichergestellt, dass jede neue Erfassung, die Sie erstellen, nur andere als die in anderen Aufzeichnungen enthaltenen Artikel aufweist.

Im Falle der manuellen Zählung können Sie eine Liste ausdrucken, den Bericht **Inventurerfassung**, der eine leere Spalte enthält, in der die gezählten Mengen aufgeschrieben werden. Wenn die Zählung abgeschlossen ist, geben Sie die erfassten Mengen in die entsprechenden Zeilen auf der Seite **Inventurerfassung** ein. Zuletzt übertragen Sie die erfassten Mengen in den zugehörigen Inventurauftrag, indem Sie den Status auf **Beendet** setzen.

1. Wählen Sie auf der Seite **Inventurauftrag**, die Zeilen für die zu zählenden Artikel in einer Erfassung enthält, die Aktion **Neue Erfassung erstellen** aus.
2. Wählen Sie die Optionen und Filter nach Bedarf aus.
3. Wählen Sie die Schaltfläche **OK** aus.

    Ein Beleg für die Inventurerfassung wird erstellt.

4. Jede Gruppe von Artikeln, die gezählt wird, laden Sie in den zugehörigen Inventurauftrag. Dann wiederholen Sie die Schritte 1 bis 3 bei aktiviertem Kontrollkästchen **Nur nicht erfasste Zeilen**.

5. Wählen Sie die Aktion **Erfassungen** aus, um die Seite **Inventurerfassungsübersicht** zu öffnen.
6. Öffnen Sie die entsprechende Erfassung.
7. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus.
8. Bei Artikeln, die die Artikelverfolgung verwenden, erstellen Sie eine weitere Zeile für jeden Chargen- oder Seriennummerncode, indem Sie die Aktion **Funktionen** und dann die Aktion **Zeile kopieren** auswählen. Weitere Informationen finden Sie im Abschnitt „Verarbeitung der Artikelverfolgung beim Erfassen des Lagerbestands”.    
9. Wählen Sie die Aktion **Drucken** aus, um den Beleg vorzubereiten, den Mitarbeiter verwenden, um die gezählten Mengen aufzuschreiben.

## <a name="to-finish-a-physical-inventory-recording"></a>So schließen Sie eine Inventurerfassung ab
Wenn die Mitarbeiter die Lagerbestandsmengen gezählt haben, müssen Sie die Erfassung im System vorbereiten.

1. Wählen Sie auf der Seite **Inventurerfassungsübersicht** die Inventurerfassung aus, die Sie abschließen möchten, und wählen Sie dann die Aktion **Bearbeiten** aus.
2. Füllen Sie dann im Inforegister **Zeilen** die tatsächlich gezählte Menge im Feld **Menge** für jede Zeile aus.
3. Für Artikel mit Serien- oder Chargennummern (bei ausgewähltem Kontrollkästchen **Artikelverfolgung verwenden**) geben Sie die gezählten Mengen in den entsprechenden Zeilen für die betreffenden Serien- und Chargennummern der Artikel ein. Weitere Informationen finden Sie im Abschnitt „Verarbeitung der Artikelverfolgung beim Erfassen des Lagerbestands”.
4. Aktivieren Sie in jeder Zeile das Kontrollkästchen **Erfasst**.
5. Wenn Sie alle Daten für eine Inventurerfassung eingegeben haben, wählen Sie die Aktion **Fertig stellen** aus. Beachten Sie, dass bei allen Zeilen das Kontrollkästchen **Erfasst** ausgewählt sein muss.

> [!NOTE]
> Wenn Sie eine Inventurerfassung abschließen, wird jede Zeile in die Zeile des zugehörigen Inventurauftrags übertragen, mit der sie genau übereinstimmt. Damit sie übereinstimmen, müssen die Werte in den Feldern **Artikelnr.**, **Variantencode**, **Lagerortcode** und **Lagerplatzcode** mit der Erfassung und den Auftragszeilen übereinstimmen.<br /><br />
> Wenn keine übereinstimmende Inventurauftragszeile vorhanden ist und das Kontrollkästchen **Erfassung ohne Auftrag erlauben** aktiviert ist, wird automatisch eine neue Zeile eingefügt und das Kontrollkästchen **Ohne Auftrag erfasst** in der entsprechenden Inventurauftragszeile aktiviert. Andernfalls wird eine Fehlermeldung angezeigt, und der Prozess wird abgebrochen.<br /><br />
> Wenn mehr als eine Zeile einer Inventurerfassung mit einer Zeile eines Inventurauftrags übereinstimmt, wird eine Meldung angezeigt und der Vorgang abgebrochen. Wenn aus irgendwelchen Gründen zwei identische Inventurerfassungszeilen im Inventurauftrag landen, können Sie eine Funktion verwenden, um das Problem zu lösen. Weitere Informationen finden Sie im Abschnitt „So finden Sie doppelte Inventurauftragszeilen”.

## <a name="to-complete-a-physical-inventory-order"></a>So schließen Sie einen Inventurauftrag ab
Wenn Sie eine Inventurerfassung abgeschlossen haben, wird das Feld **Erfasste Menge (Basis)** im zugehörigen Inventurauftrag mit den gezählten (erfassten) Werten aktualisiert und das Kontrollkästchen **In Erfassung** aktiviert. Wenn ein gezählter Wert sich vom erwarteten Wert unterscheidet, dann wird diese Differenz entsprechend im Feld **Positive Menge (Basis)** oder **Negative Menge (Basis)** angezeigt.

Um sich die erwartete Mengen und alle erfassten Differenzen für Artikel mit Artikelverfolgung anzeigen zu lassen, wählen Sie die Aktion **Zeilen** und dann die Aktion **Artikelverfolgungszeilen** aus, um verschiedene Ansichten für Serien- und Chargennummern auszuwählen, die in der Inventarerfassung berücksichtigt wurden.

Sie können auch die **Phys. Inventory Order Diff.** Aktion auswählen, um Unterschiede zwischen der erwarteten und der gezählten Menge anzuzeigen.

### <a name="to-find-duplicate-physical-inventory-order-lines"></a>So finden Sie doppelte Inventurauftragszeilen

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Physische Inventuraufträge** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie den Inventurauftrag, für den Sie doppelte Zeilen anzeigen möchten.
3. Wählen Sie die **Doppelte Zeilen anzeigen** Aktion aus.

Es werden alle doppelten Inventurauftragszeilen angezeigt, sodass Sie sie löschen und nur eine Zeile mit eindeutigem Satz von Werten in den Feldern **Artikelnr.**, **Variantencode**, **Lagerortcode** und **Lagerplatzcode** behalten können.

### <a name="to-post-a-physical-inventory-order"></a>So buchen Sie einen Inventurauftrag
Nach Fertigstellen eines Inventurauftrags und Ändern des Status in **Beendet** kann er gebucht werden. Der Status eines Inventurauftrags kann unter folgenden Voraussetzungen nur auf **Beendet** festgelegt werden:

- Alle zugehörigen Inventurerfassungen weisen den Status **Beendet** auf.
- Jede Inventurauftragszeile wurde in mindestens einer Inventurerfassungszeile erfasst.
- Die Kontrollkästchen **In Erfassungszeilen enthalten** und **Berechnete erw. Menge** wurden für alle Inventurauftragszeilen aktiviert.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Physische Inventuraufträge** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Inventurauftrag aus, den Sie fertig stellen möchten, klicken Sie auf **Bearbeiten**.

    Auf der Seite **Inventurauftrag** kann die Menge angezeigt werden, die im Feld **Erfasste Menge (Basis)** erfasst wurde.
3. Wählen Sie die Schaltfläche **Fertigstellung** aus.

    Der Wert im Feld **Status** wird auf **Erledigt** geändert, und Sie können den Auftrag jetzt nur ändern, indem Sie zuerst die Aktion **Erneut öffnen**.
4. Um den Auftrag zu buchen, wählen Sie dann die Aktion **Buchen** und dann die Schaltfläche **OK** aus.

Die betreffenden Artikelposten werden zusammen mit allen verknüpften Artikelverfolgungsposten aktualisiert.

### <a name="to-view-posted-physical-inventory-orders"></a>So zeigen Sie gebuchte Inventuraufträge an
Nach der Buchung wird der Inventurauftrag gelöscht und Sie können den Beleg als gebuchten Inventarauftrag einschließlich der Inventurerfassungen und möglicher Bemerkungen einsehen und auswerten.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Gebuchte Physische Inventuraufträge** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Geb. Inventuraufträge** den gebuchten Inventurauftrag aus, den Sie anzeigen möchten, klicken Sie auf Aktionen und anschließend auf **Ansicht**.
3. Um einer Liste zugehörige Inventurerfassungen anzuzeigen, wählen Sie die Aktion **Erfassungen** aus.

## <a name="handling-item-tracking-when-counting-inventory"></a>Verarbeitung der Artikelverfolgung beim Erfassen des Lagerbestands
Die Artikelverfolgung gehört zu den Serien- oder Chargennummern, die Artikeln zugeordnet sind. Beim Erfassen eines Artikels, der im Bestand zum Beispiel unter zehn verschiedenen Chargennummern gespeichert wird, muss der Mitarbeiter erfassen, welche und wie viele Einheiten einer Chargennummer im Lager vorhanden sind. Weitere Informationen zur Artikelverfolgungsfunktion finden Sie unter [Arbeiten mit Serien- und Chargennummern](inventory-how-work-item-tracking.md).

Das Kontrollkästchen **Artikelverfolgung verwenden** in Inventurauftragszeilen wird automatisch ausgewählt, wenn ein Artikelverfolgungscode für den Artikel eingerichtet wird, Sie können diesen aber auch manuell aus- oder abwählen.

### <a name="example---prepare-a-physical-inventory-recording-for-an-item-tracked-item"></a>Beispiel – Vorbereiten einer Inventurerfassung für einen Artikel mit Artikelverfolgung
Berücksichtigen Sie eine Inventur für Artikel A, der im Lagerbestand unter zehn verschiedene Seriennummern gespeichert wird.
1. Wählen Sie in der Erfassungszeile für den Artikel das Kontrollkästchen **Artikelverfolgung verwenden** aus.
2.  Wählen Sie das Feld **Seriennr.** aus, die erste Seriennummer, die im Lagerbestand für den Artikel existiert, und wählen Sie dann die Schaltfläche **OK** aus.

    Fahren Sie fort und kopieren Sie die Zeile für den ersten Artikel mit Artikelverfolgung, um zusätzliche Zeilen entsprechend der Anzahl von Seriennummern einzufügen, die im Bestand gespeichert sind.

3. Wählen Sie die Aktion **Funktionen** und dann die Aktion **Zeile kopieren** aus.
4. Geben Sie auf der Seite **Inventurerfassungszeile kopieren** 9 in das Feld **Anzahl Kopien** ein und wählen Sie dann die Schaltfläche **OK** aus.
5. Wählen Sie in der ersten Kopiezeile das Feld **Seriennr.** und die nächste Seriennummer für den Artikel aus.
6. Wiederholen Sie den Schritt 5 für die verbleibenden acht Seriennummern. Achten Sie darauf, dieselbe Nummer nicht zweimal auszuwählen.
7. Wählen Sie die Aktion **Drucken** aus, um den Beleg vorzubereiten, den Mitarbeiter verwenden, um die gezählten Artikel und Serien-/Chargennummern aufzuschreiben.

Beachten Sie, dass der Bericht **Inventurerfassung** zehn Zeilen für Artikel A enthält, einen für jede Seriennummer.

### <a name="example---record-and-post-counted-lot-number-differences"></a>Beispiel – Erfassen und buchen von erfassten Chargennummer-Differenzen
Ein Artikel mit Chargennummern wird im Bestand mit der Lager mit der CHARGEN-Nummernserie gespeichert.

**Voraussichtlich verfügbar**:

|Chargennr.|Menge|
|-|-|
|LOT1001|80|
|LOT1003|30|
|LOT1006|10|
|Summe|120|

**Erfasste Mengen**:

|Chargennr.|Menge|
|-|-|
|LOT1001|80|
|LOT0002|12|
|LOT1003|20|
|LOT1006|10|
|Summe|112|

**Zu buchende Mengen**:

|Chargennr.|Erwartete Menge|Erfasste Menge|Zu buchende Menge|
|-|-|-|-|
|LOT1001|80|80|0|
|LOT1002|0|12|+12|
|LOT1003|30|20|-10|
|LOT1006|10|0|-10|
|Summe|120|112|-8|

Auf der Seite **Inventurauftrag** enthält das Feld **Negative Menge (Basis)** die Zahl *8*. Für die betreffende Auftragszeile enthält die Seite **Inventurverfolgungsübersicht** die positiven oder negativen Mengen für die einzelnen Chargennummern.

## <a name="see-also"></a>Siehe auch
[Erfassen, Regulieren und Umbuchen von Lagerbestand mithilfe von Buch.-Blättern](inventory-how-count-adjust-reclassify.md)  
[Arbeiten mit Chargennummern und Seriennummern](inventory-how-work-item-tracking.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Logistik](warehouse-manage-warehouse.md)    
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
