---
title: So legen Sie Lagerorte für die Verwendung von Lagerplätzen fest
description: 'Lagerplätze stellen die grundlegende Lagerstruktur dar und werden verwendet, um Vorschläge zur Einlagerung von Artikeln zu erstellen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
---

# <a name="set-up-locations-to-use-bins" />Lagerorte für die Verwendung von Lagerplätzen einrichten

Lagerplätze stellen die grundlegende Lagerstruktur dar und Sie können diese verwenden, um vorzuschlagen, wo Artikel abgelegt werden sollen. Wenn Sie Ihre Lagerplätze erstellt haben, können Sie deren Inhalt definieren oder sie können als schwebende Lagerplätze ohne festgelegten Inhalt fungieren.

Um die Lagerplatz-Funktionalität an einem Standort zu nutzen, aktivieren Sie die Funktionalität auf der Seite Standortkarte, indem Sie das Feld **Lagerplätze obligatorisch** auf der Karte **Lager** auswählen. Nachdem Sie den Schalter einschalten, werden die **Lager-Code** und **Zonencode** Felder in den folgenden Dokumenten verfügbar:

* Warenempfangskopf
* Warenempfangszeilen
* Einlagerungszeilen
* Warenversandkopf
* Warenversandzeilen
* Einlagerungszeilen

Im nächsten Schritt entwerfen Sie den Warenfluss am Lagerort, indem Sie Lagerplatzcodes in den Einrichtungsfeldern angeben, die für die verschiedenen Flows stehen.  

> [!NOTE]  
> Bevor Sie Lagerplätze auf einem Platz angeben können, müssen Sie diese für den Lagerort definieren. Weitere Informationen finden Sie unter [Lagerplätze erstellen](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins" />Um einen Lagerort für die Verwendung von Lagerplätzen einzurichten

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie den Lagerort aus, an dem Sie Lagerplätze verwenden möchten.  
3. Wählen Sie die Aktion **Bearbeiten** aus.  
4. Aktivieren Sie im Inforegister **Lager** das Kontrollkästchen **Lagerplatz notwendig**.  
5. Wenn Sie für den Lagerort die gesteuerte Einlagerung und Kommissionierung nicht nutzen, tragen Sie im Feld **Standard-Lagerplatzauswahl** die Methode ein, die [!INCLUDE [prod_short](includes/prod_short.md)] verwenden soll, wenn sie einem Artikel einen Standardlagerplatz zuweist.  
6. Öffnen Sie  die Karte für den Lagerort, an dem Sie Lagerplätze einrichten möchten.
7. Wählen Sie im Inforegister **Lagerplätze** die Lagerplätze, die Sie als Standard für Lagerplätze für Wareneingänge, Warenausgänge sowie zur Fertigungsbereitstellung, als Fertigungsausgangslager und für die offene Fertigungsbereitstellung nutzen möchten.  

    Die Lagerplatzcodes, die Sie hier eintragen, erscheinen automatisch im Kopf und danach in den Zeilen von verschiedenen Logistikbelegen. Die Vorgabe Lagerplätze legen alle Start- und Endeinlagerungen von Artikeln im Lager fest.  
8. Wenn Sie die gesteuerte Einlagerung und Kommissionierung nutzen, wählen Sie einen Lagerplatz für den Ausgleich. Der Lagerplatzcode im Feld **Ausgleichslagerplatzcode** legt den virtuellen Lagerplatz fest, in dem die Anwendung Abweichungen im Lagerbestand erfasst, wenn Sie Folgendes registrieren:

    * Wenn Sie Differenzen feststellen, die im Artikeljournal des Lagers registriert sind
    * Differenzen, die die Anwendung berechnet hat, als Sie eine Logistik Inventur registriert haben  
9. Optional: Füllen Sie die Felder im Inforegister **Lagerrichtlinien** aus. Die wichtigsten Felder sind **Lagerkapazitätsprüfung**, **Gebindeanbruch zulassen** und **Einlagerungsvorlagencode**.  
10. Tragen Sie im Inforegister **Logistik** die Felder **Ausgeh. Lagerdurchlaufzeit**, **Eingeh. Lagerdurchlaufzeit** und **Basiskalendercode** ein. Um mehr zu erfahren, gehen Sie zu [Basiskalender einrichten](across-how-to-assign-base-calendars.md).

## <a name="fill-in-the-consumption-bin" />Auffüllen des Verbrauchslagerplatzes

Das folgende Flow-Diagramm zeigt, wie das Feld **Lagerplatzcode** auf den Zeilen der Produktionsauftragskomponenten entsprechend der Einrichtung Ihres Standorts gefüllt wird.

:::image type="content" source="media/binflow.png" alt-text="Lagercodefeld im Produktionsauftrag Komponentenzeilen.":::

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-bins-location" />Siehe verwandte [Microsoft Schulungen](/training/modules/configure-bins-location/)

## <a name="see-also" />Siehe auch

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
