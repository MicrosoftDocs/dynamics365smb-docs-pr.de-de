---
title: 'Vorgehensweise: Verfolgen von Artikeln mit Artikelverfolgung | Microsoft Docs'
description: "Sie können sehen, wo ein Artikel mit Artikelverfolgung verwendet wurde. Dazu gehören die Informationen, wie und wann der Artikel entgegengenommen oder produziert, umgelagert, verkauft, verbraucht oder zurückgegeben wurde. Sie können außerdem alle aktuellen Instanzen einer bestimmten Serien- oder Chargennummern in der Datenbank suchen. Dazu können Sie die Funktionen \"Artikelablaufverfolgung\" und \"Navigieren\" verwenden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cc24989d2cf770cd88bbde23d483e3859ff4a68a
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="trace-item-tracked-items"></a>Verfolgen von Artikeln mit Artikelverfolgung
Sie können sehen, wo ein Artikel mit Artikelverfolgung verwendet wurde. Dazu gehören die Informationen, wie und wann der Artikel entgegengenommen oder produziert, umgelagert, verkauft, verbraucht oder zurückgegeben wurde. Sie können außerdem alle aktuellen Instanzen einer bestimmten Serien- oder Chargennummern in der Datenbank suchen. Dazu können Sie die Funktionen "Artikelablaufverfolgung" und "Navigieren" verwenden.  

 Diese Funktionen können insbesondere in der Qualitätssicherung hilfreich sein, wenn Sie herausfinden müssen, welcher Debitor Produkte mit einer bestimmten Chargennummer erhalten hat oder aus welcher Charge eine defekte Komponente stammte.  

 Im Fenster **Artikelnachverfolgung** können Sie in einer Abfolge von gebuchten Lagertransaktionen die Serien- oder Chargennummer vorwärts oder rückwärts verfolgen.  

 Im Fenster **Navigieren** können Sie die Abfolge von Transaktionen nicht sehen, aber Sie können alle Datensätze der Serien- oder Chargennummer sehen, und zwar gebuchte Posten und offene Datensätze.  

 Die beiden Funktionen können in Kombination verwendet werden, indem eine verfolgte Serien- oder Chargennummer an das Fenster **Navigieren** übertragen wird, um ein vollständiges Verfolgungsszenario fertig zu stellen. Weitere Informationen hierzu finden Sie unter [Vorgehensweise: Chargen- oder Seriennummern nachverfolgen](walkthrough-tracing-serial-lot-numbers.md).  

## <a name="to-trace-item-tracked-items"></a>Artikel mit Artikelverfolgung verfolgen  

1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Artikel-Nachverfolgung** ein und wählen den zugehörenden Link aus.  
2.  Geben Sie in die Filterfelder oben im Fenster die Artikelnummern oder einen Filter für die Artikelnummern ein, die Sie verfolgen möchten.  
3.  Wählen Sie im Feld **Komponenten anzeigen** aus, ob auch angezeigt werden soll, woher die Komponenten für die Artikel stammten. In diesem Feld haben Sie die folgenden Optionen.  

    |Feld|Description|  
    |----------------------------------|---------------------------------------|  
    |**Nein**|Wählen Sie diese Option aus, wenn keine Komponenten angezeigt werden sollen.|  
    |**Nur Artikelverfolgung**|Wählen Sie diese Option aus, wenn nur Komponenten angezeigt werden sollen, die eine Chargen- oder Seriennummer haben.|  
    |**Alle**|Wählen Sie diese Option aus, wenn alle Komponenten angezeigt werden sollen.|  

4.  Wählen Sie im Feld **Ablaufverfolgungsmethode** die Methode aus, die für die Ablaufverfolgung des Artikels verwendet werden soll. Es gibt folgende Optionen  

    |Feld|Description|  
    |----------------------------------|---------------------------------------|  
    |**Verbrauch -> Ursprung**|Bei dieser Methode wird der Artikel ab dem Punkt, an dem er verwendet wurde, bis zu dem Punkt, von dem er kam, zurückverfolgt. Wenn beispielsweise ein Produktionsartikel an einen Debitor verkauft wurde, wird für den Artikel im Fenster **Artikelablaufverfolgung** zuerst die Verkaufslieferzeile angezeigt, die Sie erweitern können, um zu sehen, zu welchem Fertigungsauftrag der Artikel gehörte.|  
    |**Ursprung -> Verbrauch**|Bei dieser Methode wird der Artikel ab dem Punkt, an dem er in den Lagerbestand übernommen wurde, bis zu dem Punkt verfolgt, an dem er verwendet wurde. Wenn beispielsweise ein Produktionsartikel an einen Debitor verkauft wurde, wird für den Artikel im Fenster **Artikelablaufverfolgung** zuerst der beendete Fertigungsauftrag angezeigt, den Sie erweitern können, um die Verkaufslieferungszeilen zu sehen, in denen der Artikel verwendet wurde.|  

5.  Klicken Sie auf Aktionen **Ablaufverfolgung**, damit die Ablaufverfolgung ausgeführt wird.  

> [!NOTE]  
>  Wenn Sie eine Charge über mehrere Transaktionen erhalten haben, Zeigt das Fenster **Artikelverfolgung** möglicherweise nicht alle Transaktionen an. Nur ausgeglichene Transaktionen werden angezeigt.  

> [!NOTE]  
>  Wenn ein zusätzlicher Buchungsverlauf unter einer Artikelablaufverfolgungszeile bereits durch eine weitere Zeile darüber aufgezeichnet wurde, ist das Kontrollkästchen **Bereits nachverfolgt** aktiviert. Um eine einfachere Ansicht zu bieten, werden solche zugrunde liegenden Zeilen nicht angezeigt.  
>   
>  Um die Artikelablaufverfolgungszeilen zu suchen, in denen der Buchungsverlauf bereits aufgezeichnet wurde, wählen Sie die Schaltfläche **Wechseln zu bereits nachvollzogen**. Die betreffende Artikelablaufverfolgungszeile wird ausgewählt, und alle zugrunde liegenden Zeilen werden erweitert.  

## <a name="to-find-item-tracked-items-with-navigate"></a>So suchen Sie Artikel mit Artikelverfolgung mithilfe von "Navigieren"  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Navigieren** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Geben Sie im Inforegister **Artikelverfolgung** in den Feldern **Seriennr.** und **Chargennr.** die Artikelverfolgungsnummern ein, die Sie verfolgen möchten.  
3.  Wählen Sie auf der Registerkarte Aktionen in der Gruppe Seite die Option **Suchen** aus, um alle Instanzen der Serien- oder Chargennummer und in der Datenbank zu finden.  

## <a name="see-also"></a>Siehe auch  
[Lagerbest](inventory-manage-inventory.md)  
[Unter Designdetails: Artikelverfolgung](design-details-item-tracking.md)
[Unter Designdetails - Artikelverfolgung und  Reservierungen](design-details-item-tracking-and-reservations.md)  
[Artikel reservieren](inventory-how-to-reserve-items.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Exemplarische Vorgehensweise: Verfolgung von Serien-/Chargennummern](walkthrough-tracing-serial-lot-numbers.md)

