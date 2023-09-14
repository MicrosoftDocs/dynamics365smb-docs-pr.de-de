---
title: So aktivieren Sie die Kommissionierung nach FEFO | Microsoft Docs
description: 'FEFO (First-Expired-First-Out) ist eine Sortiermethode, durch die sichergestellt ist, dass die ältesten Artikel mit den frühesten Ablaufdatumsangaben zuerst kommissioniert werden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# Aktiveren der Kommissionierung von Artikeln nach FEFO
FEFO (First-Expired-First-Out) ist eine Sortiermethode, durch die sichergestellt ist, dass die ältesten Artikel mit den frühesten Ablaufdatumsangaben zuerst kommissioniert werden.  

 Diese Funktionen arbeiten nur, wenn die folgenden Kriterien erfüllt sein:  

-   Der Artikel muss eine Serien-/Chargennummer haben.  
-   Bei der Einrichtung des Artikelverfolgungscodes des Artikels muss das Feld **Seriennr.-Verf. Lager** oder das Feld **Chargennr.-Verf. Lager** ausgewählt werden.  
-   Der Artikel muss mit einem Ablaufdatum im Lager gebucht werden.  
-   Für den Standort müssen die Schalter **Kommissionierung erforderlich**, **Gemäß FEFO kommissionieren** und **Lagerplatz notwendig** eingeschaltet sein.  

 Wenn alle Kriterien erfüllt sein, werden zu kommissionierenden Artikel mit Serien-/Chargennummern bei allen in Kommissionierungen und Lagerplatzumlagerungen mit dem ältesten zuerst sortiert. Ausgenommen sind Artikel mit SN-spezifischer oder chargenspezifischer Verfolgung.  

> [!NOTE]  
> Wenn einige serien- oder chargennummerierte Artikel eine spezifische Verfolgung verwenden, werden diese zuerst berücksichtigt und danach werden die verbleibenden unspezifischen Serien-/Chargennummern gemäß FEFO aufgelistet.
<br /><br />
Weisen zwei Artikel mit Serien- oder Chargennummer dasselbe Ablaufdatum aufweisen, wählt die Anwendung den Artikel mit der niedrigeren Serien- oder Chargennummer aus.
<br /><br />
Werden Artikel mit Serien- oder Chargennummer an Lagerorten kommissioniert, die für die gesteuerte Einlagerung und Kommissionierung eingerichtet sind, werden bei der FEFO-Methode lediglich Mengen aus Lagerplätzen vom Typ *Kommissionierung* kommissioniert.  
<br /><br />
Die Aktivierung der Umlagerungen nach FEFO erfolgt entweder auf dem Feld **Von Lagerplatz** auf der Seite **Lagerbestandsumlagerung** oder der Seite **Lagerplatzumlagerungsarbeitsblatt**.  
<br /><br />
Wenn das Feld **Fixes Ablaufdatum** auf der **Artikelnachverfolgungscodekarte**ausgewählt, werden nur Artikel, die nicht abgelaufen sind, in die Auswahl aufgenommen, und die Zeilen werden nach dem FEFO-Prinzip sortiert.

## Weitere Informationen  
[Um Artikel für den Warenausgang zu kommissionieren](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Artikel mit der Lagerkommissionierung kommissionieren](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]