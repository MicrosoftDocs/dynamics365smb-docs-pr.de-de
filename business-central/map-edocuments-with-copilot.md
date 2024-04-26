---
title: E-Belege mit Copilot Bestellzeilen zuordnen
description: 'Erfahren Sie, wie Sie mit Copilot E-Belege den Bestellpositionen zuordnen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: altotovi
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 04/10/2024
ms.custom: bap-template
---

# E-Belege mit Copilot Bestellpositionen zuordnen (Vorschauversion)

Da Beschaffungsprozesse zunehmend digitalisiert werden, spielt die E-Belegsfunktion in Business Central eine Schlüsselrolle bei der Automatisierung des Empfangs und der Verarbeitung von Kreditorenrechnungen. Copilot kann diesen Prozess unterstützen, indem er die Zuordnung und den Abgleich von Kreditorenrechnungen mit Bestellungen verbessert. Dadurch werden zeitaufwändige Aufgaben reduziert, die normalerweise umfangreiche Such-, Nachschlage- und Dateneingabevorgänge umfassen würden. Der Vorteil wird durch die Tatsache verstärkt, dass sich Kreditorenrechnungen häufig nicht genau auf Bestellungen beziehen. In diesem Fall ist Copilot besser in der Lage, die entsprechenden Bestellungen zu identifizieren. Von den erweiterten Abgleichsfunktionen profitieren insbesondere kleine und mittlere Unternehmen, die eine effiziente Belegverfolgung für Bestellpositionen benötigen. Copilot ist der KI-gestützte Arbeitsassistent, der die Kreativität fördert und die Produktivität von Business Central-Benutzenden verbessert.

> [!IMPORTANT]
> - Dies ist eine produktionsbereite Vorschaufunktion für Produktions- und Sandbox-Umgebungen in allen Länderlokalisierungen, mit Ausnahme von Kanada.
> - Für produktionsbereite Vorschaufunktionen gelten die ergänzenden Nutzungsbedingungen. Weitere Informationen: [Ergänzende Nutzungsbedingungen für die Dynamics 365-Vorschauversion](https://go.microsoft.com/fwlink/?linkid=2105274)
> - KI-generierte Inhalte können fehlerhaft sein.

In der ersten Version der App **E-Beleg** haben wir grundlegende Szenarien für E-Belege für den gesamten Verkaufsprozess vorgestellt. Allerdings besteht Bedarf an Verbesserungen und Automatisierung im Umgang mit den empfangenen Belegen, insbesondere im Rahmen von Einkaufsprozessen. Copilot verfeinert die Verwaltung von E-Belegen im Kaufprozess, insbesondere im Hinblick auf Bestellungen. Mit dem E-Belegs-Framework können Sie die Art des Einkaufsbelegs angeben, das für jeden Kreditoren erstellt werden soll, wenn Sie E-Rechnungen von ihm erhalten. Bisher bestand die einzige Möglichkeit darin, eine Einkaufsrechnung entweder als Beleg oder als Fibu.-Buch.-Blatt zu erstellen.

Sie können jetzt eine vorhandene Bestellung in Business Central mit den in der E-Rechnung erhaltenen Informationen aktualisieren.

<!--
> [!NOTE]
> - This feature is available as a production-ready preview for production and sandbox environments in any country localization, with the exception of Canada. Production-ready previews are subject to supplemental terms of use. For more information, see [Supplemental terms of use for Dynamics 365 preview](https://go.microsoft.com/fwlink/?linkid=2105274).
> - AI-generated content may be incorrect.-->

## So aktivieren Sie Copilot  

Falls Sie den Copilot der **Unterstützung beim Abgleich von E-Belegen** nicht aktiviert haben, müssen Sie dies manuell tun. Um den Copiloten zur **Unterstützung beim Abgleich von E-Belegen** zu aktivieren, gehen Sie wie folgt vor: 

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Copilot- und KI-Funktionen** ein und wählen Sie dann den zugehörigen Link. 
2. Wählen Sie in der Liste der Funktionen **Unterstützung beim Abgleich von E-Belegen** und ändern Sie den Status auf **Aktiv**.  

Sie können Copilot sofort nach der Aktivierung verwenden. 

## Bestellungen ermitteln

Zunächst können Sie die Bestellungen ermitteln, die Sie automatisch zuordnen können. Wenn bei Ihrem **Kreditor** das Feld **E-Beleg empfangen an** für die Arbeit mit **Bestellungen** konfiguriert ist, tut [!INCLUDE[prod_short](includes/prod_short.md)] nach der Erstellung des elektronischen Belegs (manuell oder von einem externen Endpunkt aus) in [!INCLUDE[prod_short](includes/prod_short.md)] Folgendes:

1. Wenn die **Bestellung** für diesen bestimmten Kreditor *existiert und eine Bestellnummer* in der empfangenen **E-Beleg**-Datei vorliegt, verknüpft [!INCLUDE[prod_short](includes/prod_short.md)] diesen **E-Beleg** automatisch mit der angegebenen **Bestellung**. Der **Belegstatus** dieses **E-Belegs** ist dann **In Bearbeitung** und der **Status des E-Belegs** auf der Unterseite **Dienststatus** lautet **Bestellung verknüpft**.  
Diese Verknüpfung wird im Feld **Beleg** dieses speziellen **E-Belegs** angezeigt. Wenn Sie die automatisch verknüpfte **Bestellung** ändern müssen, können Sie dies mit der Aktion **Bestellungslink aktualisieren** tun und dann manuell eine der vorhandenen Bestellungen für diesen Kreditor auswählen. Dies ist nur möglich, bevor Sie die Zeilen zwischen **E-Beleg** und **Bestellung** abgleichen.  
2. Wenn die **Bestellung** für diesen bestimmten Kreditor *vorliegt, aber keine Bestellnummer* in der empfangenen **E-Beleg**-Datei angegeben ist, falls Sie diesen Beleg manuell hochgeladen haben, bietet Ihnen [!INCLUDE[prod_short](includes/prod_short.md)] mehrere Möglichkeiten an, eine der vorhandenen Bestellungen auszuwählen. Dadurch wird die Liste **Bestellungen** geöffnet. Diese Bestellungen stammen aus Aufträgen, die Sie von Kreditoren erhalten haben, und erhalten nur den **E-Beleg**. Hier müssen Sie die gewünschte **Bestellung** und dann **OK** auswählen. Wenn Sie nicht die richtige **Bestellung** ausgewählt haben oder den **E-Beleg** automatisch von einem externen Endpunkt aus über die **Auftragswarteschlange** erhalten haben, wird der neue **E-Beleg** nicht mit einem Einkaufsbeleg verknüpft. Der **Belegstatus** lautet dann **Fehler** und der **Status des E-Belegs** auf der Unterseite **Dienststatus** lautet **Fehler bei der Verarbeitung des importierten Belegs**. Um die Verknüpfung der **Bestellung** abzuschließen, wählen Sie die Aktion **Bestellungslink aktualisieren** und wählen Sie dann eine der vorhandenen Bestellungen für diesen Kreditor aus.  

## Positionen zuordnen

Copilot hilft Ihnen, E-Rechnungszeilen automatisch mit Bestellpositionen abzugleichen und bietet zusätzliche Zuordnungsintelligenz, um die Übereinstimmungen zu verbessern.

Nachdem sie abgeglichen und zugeordnet wurden, aktualisiert [!INCLUDE [prod_short](includes/prod_short.md)] die abgeglichene Bestellung mit den relevanten Empfangsinformationen, um sicherzustellen, dass die richtigen Mengen in den Bestellpositionen eingehen.

Sie können Ihre empfangenen elektronischen Belege von zwei verschiedenen Orten aus mit den Zeilen der Bestellungen abgleichen: von der Seite **E-Belege** aus oder über die Seite **Bestellung**. Der einfachste Weg, die bereits verknüpften **Bestellungen** zu finden, ist die Kachel **Verknüpfte Bestellungen**, die zu den **E-Beleg-Aktivitäten** gehört. Alle nicht verlinkten Belege finden Sie über die Kachel **Wartende E-Einkaufsrechnungen**. Hier finden Sie eine Liste von **E-Belegen**, die Sie durchgehen müssen.  

> [!NOTE]
> Die **E-Beleg-Aktivitäten** mit diesen beiden Kacheln finden Sie in den folgenden Rollencentern: **Bewertung durch Geschäftsführung**, **Geschäftsführung**, **Buchhaltung**, **Lagerverwaltung** sowie **Versand und Wareneingang**.

Wenn Sie den Abgleich aus der Bestellung heraus durchführen möchten, wählen Sie die Aktion **E-Belegzeilen zuordnen**, die sowohl auf der Bestellung als auch auf den Bestellungslistenseiten vorhanden ist. Wenn Sie den Abgleich jedoch von der Seite **E-Belege** aus durchführen möchten, wählen Sie auf dieser Seite die Aktion **Bestellung abgleichen** aus. Gehen Sie wie folgt vor, um mit dem Abgleich fortzufahren:

1. Wählen Sie für bereits verknüpfte Belege die Aktion **E-Belegzeilen zuordnen** oder **Bestellung abgleichen**.  
2. Wie Sie sehen, funktioniert der Prompt **E-Belegsauftragszeilen mit Copilot abgleichen** und Sie haben die Seite **Bestellabgleich** im Hintergrund. Das heißt, derselbe Prozess findet statt, allerdings mit der automatischen Unterstützung von **Copilot**, der den Abgleichsprozess für Sie erledigt 
3. Nach einigen Sekunden schlägt **E-Belegsauftragszeilen mit Copilot abgleichen** Zeilen zum Abgleichen mit einigen weiteren Details vor: 

    1. In der Promptkopfzeile finden Sie die folgenden Informationen: 

    |Name des Felds |Beschreibung |
    |--------|-----------------|
    |Automatisch abgeglichen | Gibt die Anzahl der automatisch vorgeschlagenen Übereinstimmungen an. Diese basiert auf einem Zeichenfolgenvergleich. Wenn sich die Beschreibungen zu 80 % oder mehr überschneiden, gleicht das System diese Beschreibungen automatisch ab, ohne GPT-Funktionen zu verwenden. |
    |Copilot-Übereinstimmung | Gibt die Anzahl der von Copilot anhand von Zeichenfolgen- und semantischen Vergleichen vorgeschlagenen Übereinstimmungen an. |
    |E-Beleg-Nr. | Gibt die verknüpfte E-Belegnummer an. |
    |Gesamtrechnungsbetrag ohne MwSt. | Gibt den Gesamtrechnungsbetrag ohne MwSt. an. |
    |Abgeglichener Verkaufsbetrag inkl. MwSt. | Gibt den abgeglichenen Betrag ohne MwSt. an. |
    
    2. Wenn alle Zeilen übereinstimmen, wird in der oberen rechten Ecke dieser grüne Text angezeigt: **Alle Zeilen (100 %) wurden abgeglichen. Überprüfen Sie die Übereinstimmungsvorschläge**.  
    3. In den Zeilen **Zugeordneter Vorschlag** finden Sie die folgenden Informationen:  

    |Name des Felds |Beschreibung |
    |--------|-----------------|
    |E-Beleg-Zeilennr. | Gibt die Zeilennummer des E-Belegs an (aus der ursprünglichen E-Belegdatei). |
    |Beschreibung der E-Belegzeile | Gibt die Zeilenbeschreibung des E-Belegs an (aus der ursprünglichen E-Belegdatei). |
    |Abgeglichene Menge | Gibt die Menge an, die auf die Bestellzeile angewendet wird. |
    |Angebot | Gibt die von der KI vorgeschlagene Aktion an. Diese vorgeschlagenen Aktionen beziehen sich auf den Abgleich der Bestellzeilen. |

    4. Alle vollständig vorgeschlagenen und zugeordneten Zeilen sind grün markiert. Wenn ein Problem vorliegt, zum Beispiel der Preis anders ist, der aber im zulässigen Preisbereich liegt, wird diese Zeile gelb markiert. Wenn zwischen den Beschreibungsfeldern eine Ähnlichkeit besteht, der Preisunterschied jedoch größer als zulässig ist, wird die Zeile rot markiert. 
    5. Wenn Sie mit einigen Vorschlägen nicht zufrieden sind, können Sie diese mithilfe der Aktion **Zeile löschen** entfernen.  
    6. Wenn Sie die vorgeschlagenen Zuordnungen sehen möchten, können Sie den Link in der Spalte **Vorschlag** verwenden, um die Seite **Details zum E-Dokument-Abgleich** zu öffnen. 
    7. Auf der Seite **Details zum E-Beleg-Abgleich** können Sie die Details aus den **E-Belegen** und der **Bestellung** vergleichen, um die vorgeschlagene Übereinstimmung vor der Bestätigung zu überprüfen. 
    8. Schließen Sie die Seite nach der Überprüfung.   

4. Wenn Sie mit den meisten Vorschlägen nicht zufrieden sind oder das Feature **E-Belegsauftragszeilen mit Copilot abgleichen** nicht verwenden möchten, wählen Sie **Verwerfen** aus. Sie können dann wie zuvor erläutert mit dem [manuellen Abgleich](finance-how-use-edocuments-purchase.md) fortfahren.  
5. Wenn Sie Vorschläge behalten möchten, wählen Sie die Schaltfläche **Behalten**. Das System speichert dann alle von **Copilot** gemachten Vorschläge ab.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] schließt den Copilot-Prompt und die Zeilen auf der Seite **Bestellabgleich** werden grün markiert, da sie bereits abgeglichen wurden.  
7. Ab dann können Sie weitermachen, als würden Sie einen manuellen Abgleich durchführen. Das bedeutet, Sie können Zuordnungen entfernen, einen manuellen Abgleich durchführen, Zuordnungen zurücksetzen oder, wenn Sie keine Änderungen vornehmen möchten, einfach die Aktion **Auf Bestellung anwenden** auswählen und mit der **Bestellung** weiterarbeiten. 

> [!NOTE]
> Sie können auch die Aktion **Abgleich mit Copilot** auf der Seite **Bestellabgleich** erneut auswählen. In diesem Fall werden Sie jedoch gefragt, ob Sie die vorhandenen Zuordnungen überschreiben möchten, da alle Zeilen bereits abgeglichen wurden.  

> [!NOTE]
> Die Preis-/Kostenanalyse und die Prüfung der verfügbaren Menge gehören zur Vorverarbeitungsaktivität dazu. 

## Siehe auch

[Überblick über E-Belege](finance-edocuments-overview.md)    
[E-Belege im Verkauf verwenden](finance-how-use-edocuments.md)    
[E-Belege im Einkauf verwenden](finance-how-use-edocuments-purchase.md)   
[Probleme mit Copilot- und KI-Funktionen behandeln](ai-copilot-troubleshooting.md)    
[Häufig gestellte Fragen zur verantwortungsbewussten KI bei Unterstützung bei Bankkontoabstimmung](faqs-bank-reconciliation.md)    
