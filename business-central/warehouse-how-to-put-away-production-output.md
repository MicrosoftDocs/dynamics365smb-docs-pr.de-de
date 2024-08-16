---
title: Lagern Sie die Produktionsausgabe ein
description: 'Dieser Artikel beschreibt, wie Sie Ihre Produktionsausgabe einlagern.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 08/12/2024
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# Lagern Sie Produktions- oder Montageausgaben ein

Wie Sie Ihren Output aus der Produktion einlagern, hängt davon ab, wie Ihr Lagerort festgelegt ist. Weitere Informationen finden Sie unter [Einrichten von Warehouse Management](warehouse-setup-warehouse.md).  

Aktivieren Sie in einer grundlegenden Lagerkonfiguration für den Eingangsfluss (Einlagerung) auf der Seite  **Standort Karte**  für den Standort die folgenden Einstellungen:

* Für die Produktion im Feld  **Produktionsausgabe-Lagerabwicklung**  Auswählen **Lagereinlagerung**.
* Montageprozesse unterstützen keine Lagereinlagerungen. Sie buchen einen Montageauftrag, um die Ausgabe zu registrieren. Wenn Sie Lagerplätze verwenden, können Sie Elemente später zwischen Lagerplätzen verschieben. Weitere Informationen finden Sie unter [Ad-hoc-Umlagerung von Artikeln in Basis-Lagerkonfigurationen](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  
* Bei Projekten ist die Einlagerung nicht anwendbar.

Erstellen Sie in erweiterten Lagerkonfigurationen, bei denen für einen Standort eine Einlagerung erforderlich ist, einen internen Einlagerungsbeleg oder einen Bewegungsbeleg, um die Ausgabe einzulagern.  

## So lagern Sie fertiggestellte Artikel aus der Produktion mit einer Lagereinlagerung ein:

Der erste Schritt zur Einlagerung von Ausgabe ist das Erstellen der Lagereinlagerungsanforderung. Diese Anforderung informiert das Lager, dass die Fertigprodukte aus der Produktion oder der Montage des Fertigungsauftrags zur Einlagerung bereit sind.

### So erstellen Sie die Lagereinlagerungsanforderung:  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Freigegebener Fertigungsauftrag** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie im Fertigungsauftrag, der für die Einlagerungen bereitsteht, und dann die Aktion **Eingehende Lageranf. erstellen** aus.  

> [!NOTE]  
> Sie können die Einlagerungsanforderung auch erstellen, indem Sie das Feld **Lagereinlag.-Anford. erstellen** aktivieren, wenn Sie den Fertigungsauftrag aktualisieren. Weitere Infromationen finden Sie unter [Aktualisieren oder Neugestalten von Fertigungsaufträgen](production-how-to-replan-refresh-production-orders.md).  

### So lagern Sie Ausstoß mit einer Lagereinlagerung ein  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagereinlagerungen** ein und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine neue Lagereinlagerung. Weitere Informationen finden Sie unter [Artikel mit Lagereinlagerungen einlagern](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3. Um zu den Fertigungsaufträgen zu gelangen, wählen Sie die Aktion **Herkunftsbeleg holen** aus, und wählen Sie den freigegebenen Fertigungsauftrag aus.  
4. Füllen Sie die Einlagerungszeilen nach Bedarf aus.
5. Wenn die Zeilen zum Buchen bereit sind, wählen Sie die Aktion **Buchen** aus. Durch das Buchen werden die Lagereinträge erstellt und der Abgang der Artikel gebucht.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

Sie können eine **Lagereinlagerung** auch direkt aus dem freigegebenen Fertigungsauftrag erstellen. Weitere Informationen finden Sie unter [Artikel mit Lagereinlagerungen einlagern](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Wenn Sie eine Lagereinlagerung buchen, [!INCLUDE [prod_short](includes/prod_short.md)] wird davon ausgegangen, dass alle Vorgänge entsprechend dem Standardarbeitsplan gebucht werden. Das heißt, die Ausbringungsmenge wird entsprechend dem letzten Vorgang gebucht. Sie können das FA-Istmeldungs Buch verwenden, um Abweichungen der fertiggestellten Menge zu buchen und Einstellungen der Bearbeitungszeiten vorzunehmen. Wenn Sie nach der Erstellung der Lagereinlagerung teilweise buchen müssen, können Sie dies für alle Vorgänge außer dem letzten für Rüstzeiten und Mengen tun. Die Lagereinlagerung steuert den letzten Vorgang.  

Wenn Sie nur die Rüst- oder Laufzeit des letzten Vorgangs buchen müssen, setzen Sie die Ausbringungsmenge des letzten Vorgangs auf 0. Sie können die letzte Zeile auch löschen, um sie überhaupt nicht zu veröffentlichen.

## So lagern Sie Montage- und Produktionsausgaben in erweiterten Lagerkonfigurationen ein

Wenn Sie die Ausgabe eines Produktions- oder Montageauftrags in einem Lager buchen, das die gesteuerte Einlagerung und Kommissionierung verwendet, wird die Ausgabe an den Lagerplatz gesendet, der im Produktions- oder Montageauftrag definiert ist. Weitere Informationen zu den verschiedenen Möglichkeiten zum Verschieben von Artikeln im Lager mit erweiterten Konfigurationen finden Sie unter  [Artikel in erweiterten Lagerkonfigurationen verschieben](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet).

> [!NOTE]  
> Sie können die Herkunftsbelegnummer, wie die Fertigungsauftragsnummer nicht in den Belegen für die interne Einlagerungsanforderung, Einlagerung oder Umlagerung für Montage- oder Fertigungsausgabeprozesse eingeben.  

## Weitere Informationen  

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
