---
title: 'Vorgehensweise: Verfolgen von Artikeln mit Artikelverfolgung | Microsoft Docs'
description: Sie können sehen, wo ein Artikel mit Artikelverfolgung verwendet wurde. Dazu gehören die Informationen, wie und wann der Artikel entgegengenommen oder produziert, umgelagert, verkauft, verbraucht oder zurückgegeben wurde. Sie können außerdem alle aktuellen Instanzen einer bestimmten Serien- oder Chargennummern in der Datenbank suchen. Dazu können Sie die Funktionen "Artikelablaufverfolgung" und "Navigieren" verwenden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 50de593aa3ff2416461aa4468f8c063c22f7b085
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377673"
---
# <a name="trace-item-tracked-items"></a>Verfolgen von Artikeln mit Artikelverfolgung
Sie können sehen, wo ein Artikel mit Artikelverfolgung verwendet wurde. Dazu gehören die Informationen, wie und wann der Artikel entgegengenommen oder produziert, umgelagert, verkauft, verbraucht oder zurückgegeben wurde. Sie können außerdem alle aktuellen Instanzen einer bestimmten Serien- oder Chargennummern in der Datenbank suchen. Dazu können Sie die Funktionen „Artikelablaufverfolgung“ und [Posten suchen](ui-find-entries.md) verwenden.  

Diese Funktionen können insbesondere in der Qualitätssicherung hilfreich sein, wenn Sie herausfinden müssen, welcher Debitor Produkte mit einer bestimmten Chargennummer erhalten hat oder aus welcher Charge eine defekte Komponente stammte.  

 Auf der Seite **Artikelnachverfolgung** können Sie in einer Abfolge von gebuchten Lagertransaktionen die Serien- oder Chargennummer vorwärts oder rückwärts verfolgen.  

 Auf der Seite **Posten suchen** können Sie die Abfolge von Transaktionen nicht sehen, aber Sie können alle Datensätze der Serien- oder Chargennummer sehen, und zwar gebuchte Posten und offene Datensätze.  

 Die beiden Funktionen können in Kombination verwendet werden, indem eine verfolgte Serien- oder Chargennummer auf die Seite **Posten suchen** übertragen wird, um ein vollständiges Verfolgungsszenario fertig zu stellen. Weitere Informationen hierzu finden Sie unter [Vorgehensweise: Chargen- oder Seriennummern nachverfolgen](walkthrough-tracing-serial-lot-numbers.md).  

## <a name="to-trace-item-tracked-items"></a>Artikel mit Artikelverfolgung verfolgen  

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Artikelablaufverfolgung** ein und wählen Sie dann den entsprechenden Link.  
2.  Geben Sie in die Filterfelder oben auf der Seite die Artikelnummern oder einen Filter für die Artikelnummern ein, die Sie verfolgen möchten.  
3.  Wählen Sie im Feld **Komponenten anzeigen** aus, ob auch angezeigt werden soll, woher die Komponenten für die Artikel stammten. In diesem Feld haben Sie die folgenden Optionen.  

    |Feld|Description|  
    |----------------------------------|---------------------------------------|  
    |**Nein**|Wählen Sie diese Option aus, wenn keine Komponenten angezeigt werden sollen.|  
    |**Nur Artikelverfolgung**|Wählen Sie diese Option aus, wenn nur Komponenten angezeigt werden sollen, die eine Chargen- oder Seriennummer haben.|  
    |**Alle**|Wählen Sie diese Option aus, wenn alle Komponenten angezeigt werden sollen.|  

4.  Wählen Sie im Feld **Ablaufverfolgungsmethode** die Methode aus, die für die Ablaufverfolgung des Artikels verwendet werden soll. Es gibt folgende Optionen  

    |Feld|Description|  
    |----------------------------------|---------------------------------------|  
    |**Verbrauch -> Ursprung**|Bei dieser Methode wird der Artikel ab dem Punkt, an dem er verwendet wurde, bis zu dem Punkt, von dem er kam, zurückverfolgt. Wenn beispielsweise ein Produktionsartikel an einen Debitor verkauft wurde, wird für den Artikel auf der Seite **Artikelablaufverfolgung** zuerst die Verkaufslieferzeile angezeigt, die Sie erweitern können, um zu sehen, zu welchem Fertigungsauftrag der Artikel gehörte.|  
    |**Ursprung -> Verbrauch**|Bei dieser Methode wird der Artikel ab dem Punkt, an dem er in den Lagerbestand übernommen wurde, bis zu dem Punkt verfolgt, an dem er verwendet wurde. Wenn beispielsweise ein Produktionsartikel an einen Debitor verkauft wurde, wird für den Artikel auf der Seite **Artikelablaufverfolgung** zuerst der beendete Fertigungsauftrag angezeigt, den Sie erweitern können, um die Verkaufslieferungszeilen zu sehen, in denen der Artikel verwendet wurde.|  

5.  Klicken Sie auf Aktionen **Ablaufverfolgung**, damit die Ablaufverfolgung ausgeführt wird.  

> [!NOTE]  
>  Wenn Sie eine Charge über mehrere Transaktionen erhalten haben, zeigt die Seite **Artikelverfolgung** möglicherweise nicht alle Transaktionen an. Nur ausgeglichene Transaktionen werden angezeigt.  

> [!NOTE]  
>  Wenn ein zusätzlicher Buchungsverlauf unter einer Artikelablaufverfolgungszeile bereits durch eine weitere Zeile darüber aufgezeichnet wurde, ist das Kontrollkästchen **Bereits nachverfolgt** aktiviert. Um eine einfachere Ansicht zu bieten, werden solche zugrunde liegenden Zeilen nicht angezeigt.  
>   
>  Um die Artikelablaufverfolgungszeilen zu suchen, in denen der Buchungsverlauf bereits aufgezeichnet wurde, wählen Sie die Schaltfläche **Wechseln zu bereits nachvollzogen**. Die betreffende Artikelablaufverfolgungszeile wird ausgewählt, und alle zugrunde liegenden Zeilen werden erweitert.  

## <a name="to-find-item-tracked-items-with-find-entries"></a>So suchen Sie Artikel mit Artikelverfolgung mithilfe von „Posten suchen“  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen...“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Posten suchen** ein und wählen Sie dann den entsprechenden Link aus.  
2. Wählen Sie **Aktionen** > **Suchen anhand von** > **Anhand von Artikelreferenz suchen**.
3. Geben Sie in den Feldern **Seriennr.** und **Chargennr.** die Artikelverfolgungsnummern ein, die Sie nachverfolgen möchten.  
4. Wählen Sie auf der Registerkarte Aktionen in der Gruppe Seite die Option **Suchen** aus, um alle Instanzen der Serien- oder Chargennummer und in der Datenbank zu finden.  

## <a name="see-also"></a>Siehe auch  
[Lagerbestand](inventory-manage-inventory.md)  
[Unter Designdetails: Artikelverfolgung](design-details-item-tracking.md)
[Unter Designdetails - Artikelverfolgung und Reservierungen](design-details-item-tracking-and-reservations.md)  
[Artikel reservieren](inventory-how-to-reserve-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
[Exemplarische Vorgehensweise: Verfolgung von Serien-/Chargennummern](walkthrough-tracing-serial-lot-numbers.md)  
[Posten finden](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]