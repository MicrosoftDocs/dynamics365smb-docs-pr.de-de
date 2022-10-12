---
title: Artikel montieren
description: Wenn das Feld Wiederbeschaffungssystem auf der Artikelkarte Montage enthält, besteht die Standardmethode zur Vorratsbeschaffung darin, den Artikel aus definierten Komponenten zusammenzubauen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: e9d53a6369e2955e0e097471e70cb83438540539
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607045"
---
# <a name="assemble-items"></a>Artikel montieren

Wenn das Feld **Beschaffungsmethode** auf der Artikelkarte **Montage** enthält, besteht die Standardmethode zur Bereitstellung des Artikels darin, es aus definierten Komponenten und eventuell mit einer definierten Ressource zu montieren.  

Die Komponenten und Ressourcen, die in diese Art eines Montageartikels gehören, müssen in einer Montagestückliste definiert werden. Weitere Informationen finden Sie unter [Arbeiten mit Montagestücklisten](assembly-how-work-assembly-boms.md).

Montageartikel können für zwei unterschiedliche Montagevorgänge eingerichtet werden:  

- Lagermontage  
- Auftragsmontage  

In der Regel nutzen Sie die **Lagerfertigung** für Artikel, die Sie vor dem Verkauf montieren möchten - wie zur Vorbereitung einer Kit-Kampagne - und auf Lager zu halten, bis sie bestellt werden. Diese Artikel sind normalerweise Standardartikel, wie gepackte Kits, die Sie nicht an Debitorenanfragen anpassen.  

In der Regel nutzen Sie die **Auftragsmontage** für Artikel, die Sie nicht auf Lager haben möchten, da Sie erwarten, dass diese für Debitorenanfragen angepasst werden müssen, oder weil Sie die Lagerkosten minimieren möchten, indem Sie diese Just-In-Time bereitstellen. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).  

Weitere Informationen darüber, wie Sie einen Montageartikel einrichten finden Sie unter [Auftragsmontage oder Lagermontage verstehen](assembly-assemble-to-order-or-assemble-to-stock.md).  

Diese Einrichtungsoptionen sind Standardeinstellungen, die verwalten, wie Verkaufs- und Montageauftragszeilen anfangs verarbeitet werden. Sie können diese Vorgaben anpassen und den Montageartikel bei der Verarbeitung eines Verkaufs auf die optimalste Art bereitstellen. Weitere Informationen finden Sie unter [Verkaufen von Lagerartikel in der Montage-zu-Auftrags-Fluss](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) und [Montage-zu-Beschaffungsartikel und Lagerartikel zusammen verkaufen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Montagekomponenten werden auf eine spezielle Art in den Basislagerkonfigurationen behandelt. Weitere Informationen finden Sie im Abschnitt „Verwenden von Auftragsmontageartikeln in Lagerkommissionierungen“ in [Artikel mit Lagerkommissionierungen auswählen](warehouse-how-to-pick-items-with-inventory-picks.md).   

In diesem Verfahren erstellen und verarbeiten Sie einen Montageauftrag für Artikel, die für das Lager montiert werden, d. h. ohne einen verknüpften Verkaufsauftrag. Die Schritte enthalten das Initiieren des Montageauftrags, die Behandlung potenzieller Komponentenverfügbarkeitsprobleme und die Teilbuchung des Montageartikelausstoßes.

## <a name="to-assemble-an-item"></a>Um einen Artikel zu montieren

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Montageaufträge** ein, und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie die Aktion **Neu** aus. Die Seite **Neuer Montageauftrag** wird geöffnet.  
3.  Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Wählen Sie im Feld **Artikelnr.** den Montageartikel aus, den Sie verarbeiten möchten. Das Feld wird gefiltert, um nur Artikel angezeigt, die für die Montage eingerichtet sind, d.h., denen Montagestücklisten zugeordnet sind.  
5.  Geben Sie im Feld **Menge** ein wie viele Einheiten des Artikels Sie montieren möchten.  

    > [!NOTE]  
    >  Wenn eine oder mehrere Komponenten nicht verfügbar sind, um die eingegebene Menge des Montageartikels zum definierten Fälligkeitsdatum herzustellen, dann wird automatisch die Seite **Montageverfügbarkeit** geöffnet, um detaillierte Informationen darüber anzuzeigen, wie viele Montageartikel basierend auf der Komponentenverfügbarkeit montiert werden können. Weitere Informationen finden Sie unter [Die Verfügbarkeit von Artikeln anzeigen](inventory-how-availability-overview.md) Wenn Sie die Seite schließen, wird der Montageauftrag mit Verfügbarkeitswarnungen in den betroffenen Komponentenzeilen erstellt.  

    Die Montageauftragszeilen werden automatisch mit dem Inhalt der Montagestückliste und mit Zeilenmengen entsprechend dem Montageauftragskopf gefüllt.  

    > [!NOTE]  
    >  Wenn die Seite **Montageverfügbarkeit** beim Ausfüllen des Montageauftragskopfs geöffnet wurde, dann enthalten alle betroffenen Montageauftragszeilen **Ja** im Feld **Verfügbarkeitswarnung** und eine Verknüpfung zu den detaillierten Verfügbarkeitsinformationen. Weitere Informationen finden Sie unter Verfügbarkeit prüfen. Sie können ein Komponentenverfügbarkeitsproblem lösen, indem Sie das Startdatum verschieben, die Komponente durch einen anderen Artikel ersetzen oder einen verfügbaren Ersatzartikel auswählen, sofern ein solcher definiert ist.  

6.  Geben Sie im Feld **Menge für Montage** ein, wie viele Einheiten des Montageartikels Sie als Ausstoß buchen möchten, wenn Sie den Montageauftrag das nächste Mal buchen. Diese Menge kann unter dem Wert im Feld **Menge** liegen, um eine Teilbuchung anzuzeigen.  

    > [!NOTE]  
    >  Um sicherzustellen, dass die Buchung des Komponentenverbrauchs der Istmeldungsbuchung des Montageartikels entspricht, werden die Mengenfelder in den Montageauftragszeilen automatisch an den Wert angepasst, den Sie im Feld **Menge für Montage** eingeben.  
7.  Geben Sie in Montageauftragszeilen vom Typ **Artikel** oder **Ressource** im Feld **Verbrauchsmenge** ein, wie viele Einheiten Sie als Verbrauch buchen möchten, wenn Sie den Montageauftrag das nächste Mal buchen.
8.  Wenn Sie bereit sind, die Teil- oder die vollständige Buchung durchzuführen, wählen Sie die Aktion **Buchen**.  

    > [!NOTE]  
    >  Falls in den einzelnen Montageauftragszeilen noch Warnungen vorhanden sind, wird die Buchungen gesperrt. Eine Meldung über die Komponenten, die nicht im Lager sind, wird angezeigt.  

Nach erfolgreicher Buchung wird der Montageartikel als Ausstoß für den Lagerortcode und den potenziellen Lagerplatzcode gebucht, die im Montageauftrag definiert sind. Für manuell erstellte Montageaufträge wird der Lagerplatz möglicherweise aus dem Einrichtungsfeld **Standardlagerort für Aufträge** kopiert. Für Auftragsmontageflüsse wird der Lagerortcode möglicherweise aus der Verkaufsauftragszeile kopiert.  

## <a name="see-related-microsoft-training"></a>Siehe zugehörige [Microsoft Schulungen](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit Stücklisten für die Montage](assembly-how-work-assembly-boms.md)  
[Bestand](inventory-manage-inventory.md)  
[Design Details: Lagerort Management](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
