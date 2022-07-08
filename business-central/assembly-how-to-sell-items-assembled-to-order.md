---
title: Verkaufen von Auftragsmontageartikeln
description: Wenn der Montageartikels für die Auftragsmontage eingerichtet ist, dann nimmt der Standard-Verkaufsauftragsprozess an, dass der Artikel nicht auf Lager ist und für den jeweiligen Verkaufsauftrag speziell montiert werden muss.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting, substitute items
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 07/29/2021
ms.author: edupont
ms.openlocfilehash: b66efde55918886132def51ad898fa9e89054c02
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077345"
---
# <a name="sell-items-assembled-to-order"></a>Verkaufen von Auftragsmontageartikeln

Wenn das Feld **Montagerichtlinie** auf der Artikelkarte eines Montageartikels **Auftragsmontage** anzeigt, wird nicht erwartet, dass der Artikel im Lagerbestand vorhanden ist, und er muss speziell für einen Verkaufsauftrag montiert werden. Wenn Sie den Artikel auf einer Verkaufsauftragszeile eingeben, wird ein Montageauftrag automatisch erstellt und mit dem Verkaufsauftrag verknüpft.  

> [!NOTE]  
>  Wenn einige Auftragsmontageartikel bereits im Lager vorhanden sind, dann können Sie die Menge von dem Montageauftrag abziehen und sie aus dem Lager reservieren. Weitere Informationen finden Sie unter [Verkaufen von Lagerartikeln in Programmfertigungs-Flow](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)  

Bei diesem Verfahren verarbeiten Sie den verkauf eines Artikels, der gemäß den Spezifikationen montiert wird, die vom Debitor gewünscht werden. Die Schritte enthalten das Initiieren der Verkaufsauftragszeile, das Anpassen der Montageartikels durch Bearbeitung seiner Komponenten und Ressourcen, die Prüfung der Verfügbarkeit, um ein Lieferdatum festzulegen und die Freigabe des Verkaufsauftrag für die Montage und den sofortigen Versand.  

> [!NOTE]  
>  Die folgende Vorgehensweise enthält nicht die Standard-Verkaufsauftragsschritte vor dem Schritt, in dem Sie den Auftragsmontageartikel in eine Verkaufsauftragszeile eingeben.  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>So verkaufen Sie einen Auftragsmontageartikel:

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2.  Erstellen Sie einen Auftrag. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)  
3.  Geben Sie im Feld **Nr.** Geben Sie im Feld Nr. einen Artikel ein, der als Auftragsmontageartikel eingerichtet ist.  
4.  Geben Sie im Feld **Lagerortcode** den Lagerort an, von dem aus der Artikel verkauft werden wird. Der Montageprozess wird an diesem Lagerort durchgeführt.  
5.  Geben Sie im Feld **Menge** ein, wie viele Einheiten zu verkaufen sind.  

    > [!NOTE]  
    >  Wenn eine oder mehrere Komponenten der angefragten Montageartikelmenge nicht verfügbar sind, dann wird ein detailliertes Verfügbarkeitswarnungsseite geöffnet. Weitere Informationen finden Sie unter Montageverfügbarkeit.  

    Ein Montageauftrag wird automatisch erstellt und mit der Verkaufsauftragszeile verknüpft. Das Fälligkeitsdatum dieses Montageauftrags wird mit dem Lieferdatum der Verkaufsauftragszeile synchronisiert.  

    Die zu verkaufende Menge wird in das Feld **Menge für Auftragsmontage** kopiert, das angibt, dass die Artikeleinrichtung erwartet, dass die gesamte Menge auf der Verkaufsauftragszeile gemäß dem Auftrag montiert wird. Sie können die Menge für die Auftragsmontage vermindern, etwa wenn Sie wissen, dass mehrere Artikel bereits verfügbar sind. Weitere Informationen finden Sie unter [Verkaufen von Lagerartikeln in Programmfertigungs-Flow](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)  

6.  Um zu berücksichtigen, dass der Debitor einen weiteren Artikel in einem Kit wünscht, wählen Sie auf dem Inforegister **Zeilen** die Aktion **Zeile**, wählen die Aktion **Auftragsmontage** und dann die Aktion **Auftragsmontagezeilen**, um die Standardmontagekomponenten anzuzeigen und zu ändern. Wählen Sie das Feld **Menge für Auftragsmontage** aus.  
7.  Erstellen Sie auf der Seite **Auftragsmontagezeilen** eine neue Zeile der Art **Artikel** für den angeforderten zusätzlichen Kit-Inhalt. Die Zeile stellt eine zusätzliche Montagekomponente dar.  

    Sie können den Auftrag auch anpassen, indem Sie die Menge eines Standardartikels im Kit erhöhen. Sie können dies tun, indem Sie den Wert im Feld **Komponentenmenge** auf der jeweiligen Montageauftragszeile erhöhen.  

    > [!NOTE]  
    >  Die Seite **Auftragsmontagezeilen** enthält nur die grundlegenden Felder, die ein Verkäufer für die Anpassung der Komponentenliste, die Hinzufügung von Artikelnachverfolgungsnummern oder zur Lösung von Artikelverfügbarkeitsproblemen benötigt. Wählen Sie zur Anzeige weiterer Auftragsmontageinformationen, wie etwa das Anfangsdatums der Auftragsmontage, die Aktion **Belege anzeigen**. Dadurch wird eine vollständige Ansicht des Montageauftrags angezeigt, der mit der Verkaufsauftragszeile verknüpft ist. Sie können die Inhalte der meisten Felder des Auftragsmontagekopfes nicht ändern, und Sie können daraus auch keine Montageausgaben buchen, da Sie dazu die Lieferungsbuchung der Verkaufsauftragszeile verwenden müssen.  
    >   
    >  Im Kopfbereich von verknüpften Montageaufträgen kann nur das Feld **Startdatum** geändert werden, um Montagearbeitern bei Beginn des Prozesses zu ermöglichen, ein Datum anzugeben, das vor dem Fälligkeitsdatum liegt. Alle Felder auf den Zeilen des verknüpften Montageauftrags können geändert werden, so dass die Lagermitarbeiter während des Prozesses Verbrauchsdaten eingeben können.  

8.  Prüfen Sie Komponentenverfügbarkeitsprobleme und reagieren Sie darauf. Wählen Sie zum Beispiel einen verfügbaren Ersatzartikel.  
9. Schließen Sie die Seite **Auftragsmontagezeilen**. Der verknüpfte Montageauftrag ist jetzt bereit damit zu beginnen, die angepassten Komponenten nach Fälligkeitsdatum zu montieren.  
10. Wählen Sie im Verkaufsauftrag die Aktion **Freigeben**, um die Montageabteilung zu benachrichtigen, dass der Montagevorgang begonnen werden kann.  
11. Führen Sie in der Montageabteilung die Schritte zur Montage der Artikel aus, die in diesem Prozess verkauft werden. Weitere Informationen finden Sie unter [Entnahme von Artikeln](assembly-how-to-assemble-items.md).  

> [!NOTE]  
> Beachten Sie, dass Artikelersetzungen nicht automatisch dazu führen, dass ein Artikel durch einen anderen Artikel ersetzt wird, beispielsweise beim Erstellen eines Verkaufsauftrags oder in einer Stückliste. Stattdessen werden Sie darüber benachrichtigt, dass Ihnen ein Ersatzartikel zur Verfügung steht.

## <a name="see-related-training-at-microsoft-learn"></a>Siehe zugehörige Schulung unter [Microsoft Learn](/learn/modules/assemble-to-order-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit Stücklisten](inventory-how-work-BOMs.md)  
[Bestand](inventory-manage-inventory.md)  
[Designdetails: Warehouse Management](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Neue Artikel registrieren](inventory-how-register-new-items.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
