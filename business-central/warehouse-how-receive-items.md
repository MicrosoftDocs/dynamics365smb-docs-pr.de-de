---
title: Empfangen von Artikeln
description: Dieser Artikel gibt einen Überblick über die verschiedenen Möglichkeiten, Artikel in einem Lager zu empfangen, zum Beispiel Artikel mit einer Einkaufsbestellung oder Artikel mit einem Lager-Eingang.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008
ms.date: 09/02/2022
ms.author: edupont
ms.openlocfilehash: 8bd79a13bb7ecc806fea0dcdea33ec604bd98c41
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460886"
---
# <a name="receive-items"></a>Empfangen von Artikeln

Wenn Artikel bei einem Lager ankommen, das nicht für die Bearbeitung des Wareneingangs eingerichtet wurde, können Sie den Wareneingang einfach im zugehörigen Geschäftsdokument, wie einer Einkaufsbestellung, einer Verkaufsreklamation oder ein eingehender Umlagerungsauftrag, erfassen.

Wenn Artikel bei einem Lager ankommen, das für die Bearbeitung des Wareneingangs eingerichtet wurde, müssen Sie die Zeilen des freigegebenen Herkunftsbelegs abrufen, der ihren Wareneingang ausgelöst hat. Wenn Sie Lagerplätze nutzen, können Sie entweder den eingetragenen Standardlagerplatz akzeptieren oder, wenn der Artikel nie zuvor in diesem Lager verwendet wurde, tragen Sie den Lagerplatz ein, in den der Artikel eingelagert werden soll. Sie müssen dann die Mengen der Artikel eingeben, die Sie erhalten haben, und den Wareneingang buchen.  

## <a name="receive-items-with-a-purchase-order"></a>Empfangen Sie Artikel mit einer Einkaufsbestellung

Nachfolgend wird erläutert, wie Artikel mit einer Bestellung empfangen werden. Die Schritte für Verkaufsreklamationen und Umlagerungsaufträgen sind ähnlich.  

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie eine bestehende Bestellung, oder erstellen Sie eine neue. Erfahren Sie mehr unter [Einkäufe aufzeichnen](purchasing-how-record-purchases.md).
3. Geben Sie in dem Feld **Menge akt. Lieferung** die empfangene Menge an.

   > [!NOTE]
   > Wenn die eingegangene Menge höher ist als die in der Bestellung bestellte Menge im Feld **Menge** und der Kreditor so eingestellt ist, dass er einen Eingangsüberschuss zulässt, dann verwenden Sie das Feld **Eingangsüberschussmenge**, um die überschüssige Menge zu behandeln. Weitere Informationen finden Sie unter [Mehr Artikel als bestellt](warehouse-how-receive-items.md#receive-more-items-than-ordered).
4. Wählen Sie die Aktion **Buchen**.

  Der Wert im Feld **Bereits gelief. Menge** wird aktualisiert. Wenn dieses eine Teillieferung ist, ist der Wert niedriger als der Wert im Feld **Menge**.

> [!NOTE]
> Wenn Sie einen Lagerbeleg zum Buchen der Quittung verwenden, können Sie nicht die Aktion **Buchen** auf die Bestellung anwenden. Stattdessen hat ein Lagerarbeiter die Bestellmenge bereits als eingegangen gebucht. Erfahren Sie mehr unter [So empfangen Sie Artikel mit einem Wareneingang](warehouse-how-receive-items.md#receive-items-with-a-warehouse-receipt).

## <a name="receive-items-with-a-warehouse-receipt"></a>Empfangen Sie Artikel mit einem Wareneingang

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Wareneingänge** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**.  

    Füllen Sie die Felder auf dem Inforegister **Allgemein** aus. Beim Abrufen der Herkunftsbelegzeilen werden einige der Informationen in jede Zeile kopiert.  

    Für Lagerkonfigurationen mit gesteuerte Einlagerung und Kommissionierung: Wenn der Lagerort eine Vorgabezone und einen Vorgabelagerplatz für Wareneingänge hat, werden die Felder **Zonencode** und **Lagerplatzcode** automatisch ausgefüllt, Sie können diese jedoch bei Bedarf ändern.  

    > [!NOTE]  
    > Wenn Sie Artikel mit Lagerklassen annehmen möchten, die von den Lagerklassen der Lagerplätze im Feld **Lagerplatzcode** des Belegkopfes abweichen, müssen Sie den Inhalt des Feldes **Lagerplatzcode** des Kopfes löschen, bevor Sie die Herkunftsbelegzeilen der Artikel holen können.  
3. Wählen Sie die **Herkunftsbelege holen** Aktion aus. Die Seite **Herkunftsbelege** wird geöffnet.

    Aus einem neuen oder offenen Wareneingang können Sie die Seite **Filter z. Holen v. Herk.-Bel.** nutzen, um die Zeilen des freigegebenen Herkunftsbelegs zu erhalten, die festlegen, welche Artikel erhalten oder geliefert werden sollen.

    1. Wählen Sie die **Filter zum Holen von Herk.-Belegen verwenden** Aktion aus.  
    2. Um einen neuen Filter einzurichten, geben Sie einen beschreibenden Code in das Feld **Code** ein, und klicken Sie auf Aktionen **Bearbeiten**.  
    3. Legen Sie die Art von Herkunftsbelegzeilen fest, die Sie abrufen möchten, indem Sie die jeweiligen Filterfelder ausfüllen.  
    4. Wählen Sie **Ausführen** aus.  

    Alle Zeilen des freigegebenen Herkunftsbelegs, die die Filterkriterien erfüllen, werden nun auf der Seite **Wareneingang** eingefügt, in dem Sie die Filterfunktion aktiviert haben. 

    Die Filterkombinationen, die Sie definieren, werden auf der Seite **Filter z. Holen v. Herk.-Bel.** gespeichert, bis das nächste Mal benötigt werden. Sie können eine unbegrenzte Anzahl von Filterkombinationen erstellen. Sie können die Kriterien jederzeit ändern, indem Sie die Aktion **Bearbeiten** auswählen.

4. Wählen Sie die Herkunftsbelege, für die Sie Artikel annehmen möchten, und bestätigen Sie dann mit **OK**.  

    Die Zeilen des Herkunftsbelegs werden auf der Seite **Wareneingang** angezeigt. Das Feld **Menge akt. Lieferung** ist für jede Zeile gefüllt, Sie können die Menge jedoch bei Bedarf ändern. Wenn Sie den Inhalt des Feldes **Lagerplatzcode** m Inforegister **Allgemein** löschen, bevor Sie die Zeilen abrufen, muss in jeder Wareneingangszeile ein geeigneter Lagerplatzcode eingetragen werden.  

    > [!NOTE]  
    >  Um das Feld **Menge akt. Lieferung** in allen Zeilen mit Null auszufüllen, wählen Sie die Aktion **Menge akt. Lieferung löschen** aus. Um sie wieder mit den Restmengen auszufüllen, aktivieren Sie die Aktion **Menge akt. Lieferung autom. ausfüllen**.  
    >
    >  Sie können nicht mehr Artikel annehmen als die Anzahl im Feld **Restmenge** der Herkunftsbelegzeile. Um weitere Artikel anzunehmen, holen Sie einen weiteren Herkunftsbeleg, der eine Zeile für den Artikel enthält, indem Sie die Filterfunktion verwenden.  

5. Buchen Sie den Wareneingang. Die Mengenfelder in den Herkunftsbelegen werden aktualisiert und die Artikel als Teil des Lagerbestands des Unternehmens gespeichert.  

Wenn Sie Einlagerungen verwenden, werden die Wareneingangszeilen zur Funktion "Wareneingang" gesendet. Die Artikel können, obwohl sie eingegangen sind, nicht kommissioniert werden, bis sie eingelagert wurden. Die eingegangenen Artikel werden nur dann als verfügbar betrachtet, wenn die Einlagerung gebucht wurde.  

Wenn Sie keine Einlagerungen verwenden, jedoch Lagerplätze, wird die Einlagerung der Artikel in dem Lagerplatz gespeichert, der in der Herkunftsbelegzeile angegeben wurde.  

> [!NOTE]  
> Wenn Sie die Funktion **Buchen und drucken** verwenden, buchen Sie den Wareneingang und drucken eine Einlagerungsanweisung, die Ihnen zeigt, wo die Artikel eingelagert werden sollen.  
>
> Wenn Ihr Lagerort die gesteuerte Einlagerung und Kommissionierung verwendet, wird die Einlagerungsvorlage genutzt, um den besten Platz für die Einlagerung der Artikel zu berechnen. Dieser wird dann auf der Einlagerungsanweisung ausgedruckt.

## <a name="receive-more-items-than-ordered"></a>Mehr Artikel als bestellt erhalten

Wenn Sie mehr Waren erhalten, als Sie bestellt haben, möchten Sie diese möglicherweise erhalten, anstatt den Beleg zu stornieren. Beispielsweise kann es billiger sein, den Überschuss Ihres Inventars zu behalten, als ihn zurückzugeben, oder Ihr Verkäufer bietet Ihnen möglicherweise einen Skonto für die Aufbewahrung an.

### <a name="set-up-over-receipts"></a>Richten Sie Übereingänge ein

Sie müssen einen Prozentsatz festlegen, um den Sie beim Empfang eine Überschreitung der bestellten Menge zulassen. Sie definieren dies mit einem Übereingang-Code, der den Prozentsatz im Feld **Übereingangtoleranz %** enthält. Anschließend weisen Sie den Code den Karten der relevanten Artikel und/oder Lieferanten zu.  

Im Folgenden wird beschrieben, wie Sie einen Übereingangscode einrichten und einem Artikel zuordnen. Die Schritte sind mit denen der Debitoreinrichtung ähnlich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol einrichten möchten, geben Sie **Artikel** ein und wählen dann den entsprechenden Link.
2. Öffnen Sie die Karte für einen Artikel, von dem Sie vermuten, dass er manchmal mit einer höheren als der bestellten Menge geliefert wird.
3. Wählen Sie die **Suche** im Feld **Eingangsüberschusscode**.
4. Wählen Sie die Aktion **Neu**.
5. Erstellen Sie auf der Seite **Überempfangscodes** eine oder mehrere neue Zeilen, die verschiedene Überempfangsrichtlinien definieren. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
6. Wählen Sie eine Zeile aus, und wählen Sie dann aus **OK**.

Der Übereingangscode wird dem Artikel zugewiesen. Jede Bestellung oder jeder Lagerzugang für den Artikel erlaubt nun den Empfang von mehr als der bestellten Menge gemäß dem angegebenen Prozentsatz der Überzugstoleranz.

> [!NOTE]
> Sie können einen Genehmigungs-Workflow einrichten, um zu verlangen, dass überzählige Belege genehmigt werden müssen, bevor sie bearbeitet werden können. In diesem Fall müssen Sie das Kontrollkästchen **Genehmigung erforderlich** auf der Seite **Eingangsüberschuss-Code** aktivieren. Erfahren Sie mehr unter [Workflows erstellen](across-how-to-create-workflows.md).

### <a name="perform-an-over-receipt"></a>Führen Sie einen Übereingang durch

In Einkaufs- und Lagerzugangszeilen wird das Feld **Über-Empfangsmenge** dazu verwendet, überzählige Mengen zu erfassen, d.h. Mengen, die den Wert im Feld **Menge**, die bestellte Menge, überschreiten.

Wenn Sie einen Übereingang bearbeiten, können Sie entweder den Wert im Feld **Zu erhaltende Menge** auf die tatsächlich erhaltene Menge erhöhen. Das Feld **Übereingangsmenge** wird dann aktualisiert, um die Überschussmenge anzuzeigen. Alternativ können Sie die überschüssige Menge in das Feld **Übereingangsmenge** eingeben. Das Feld **Zu erhaltende Menge** wird dann aktualisiert, um die bestellte Menge plus die überschüssige Menge anzuzeigen. Das folgende Verfahren beschreibt, wie das Feld **Zu empfangende Menge** auszufüllen ist.  

1. Geben Sie bei einer Bestellung oder einem Lagerzugangsbeleg, bei dem die eingegangene Menge höher als die bestellte Menge ist, die tatsächlich eingegangene Menge in das Feld **Zu erhaltende Menge** ein.

    Wenn die Erhöhung innerhalb der durch einen zugeordneten Eingangsüberschusscode festgelegten Toleranz liegt, wird das Feld **Eingangsüberschussmenge** aktualisiert, um die Menge anzuzeigen, um die der Wert im Feld **Menge** überschritten wird.

    Wenn die Erhöhung über der angegebenen Toleranz liegt, ist der Eingangsüberschuss nicht zulässig. In diesem Fall können Sie untersuchen, ob ein anderer Überquittungscode existiert, der dies erlaubt. Andernfalls kann nur die bestellte Menge empfangen werden, und die überschüssige Menge muss anderweitig behandelt werden, z.B. durch Rücksendung an den Lieferanten.

2. Buchen Sie den Beleg wie jeden anderen Beleg.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] beinhaltet nicht die Funktionalität, automatisch die finanzielle Verwaltung von Eingangsüberschuss einzuleiten. Dies müssen Sie in Absprache mit dem Kreditor manuell regeln, z.B. indem der Lieferant eine neue oder aktualisierte Rechnung weiterleitet.

## <a name="see-related-training-at-microsoft-learn"></a>Siehe verwandte Schulungen unter [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-also"></a>Siehe auch

[Logistik](warehouse-manage-warehouse.md)  
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Designdetails: Warehouse Management](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
