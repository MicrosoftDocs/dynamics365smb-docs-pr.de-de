---
title: Ungeplanmte Umlagerung von Artikeln in Basis-Lagerkonfigurationen
description: Dieser Artikel erläutert ungeplante interne Umlagerungen zwischen Lagerplätzen ohne Bedarf aus einem Herkunftsbeleg.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '393, 7382'
---
# <a name="move-items-internally-in-basic-warehouse-configurations"></a><a name="move-items-internally-in-basic-warehouse-configurations"></a><a name="move-items-internally-in-basic-warehouse-configurations"></a>Interne Umlagerung von Artikeln in Basis-Lagerkonfigurationen

Sie möchten vielleicht Artikel ohne einen Bedarf aus einem Herkunftsbeleg zwischen Lagerplätzen umlagern. Zum Beispiel im Rahmen der folgenden Aktivitäten:

* Reorganisieren Ihres Lagers.
* Artikel in einen Inspektionsbereich bringen.
* Zusätzliche Artikel zu und von einem Produktionsbereich umlagern. 

Wie Sie Artikel für die Produktion umlagern, hängt davon ab, wie Ihr Lagerort eingerichtet wurde. Weitere Informationen finden Sie unter [Einrichten von Warehouse Management](warehouse-setup-warehouse.md).

In Lagerkonfigurationen, in denen der Einrichtungsschalter **Lagerplatz obligatorisch** aktiviert **Gezielte Kommissionierung und Einlagerung** aber nicht, können Sie ungeplante Umlagerungen auf den folgenden Seiten registrieren:  

* Auf der Seite **Interne Umlagerung**.
* Auf der Seite **Umlagerungs Buch.-Blatt**.  

## <a name="internal-movements"></a><a name="internal-movements"></a><a name="internal-movements"></a>Interne Umlagerungen

Auf der Seite **Interne Umlagerungen** können Sie Entnahme- und Einlagerungszeilen angeben, wenn keine Nachfrage von einem Herkungsbeleg besteht. Die Seite „Interne Umlagerung“ ist wie ein Arbeitsblatt zum Organisieren von Dingen. Sie können die eigentliche Umlagerung daraus nicht direkt verarbeiten. Wenn eine Zeile ausgefüllt ist, verwenden Sie die Aktion **Lagerbestandsumlagerung erstellen**, um die Zeile an die Seite **Lagerbestandumlagerung** zu senden, wo Sie die Umlagerung verarbeiten und erfassen.

### <a name="to-move-items-as-an-internal-movement"></a><a name="to-move-items-as-an-internal-movement"></a><a name="to-move-items-as-an-internal-movement"></a>Um Artikel als interne Umlagerung zu verschieben

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Geben Sie **Interne Umlagerungen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu** aus. Stellen Sie sicher, dass das Feld **Nr.** auf dem Inforegister **Allgemein** ausgefüllt ist.
3. Geben Sie im Feld **Lagerortcode** den Lagerort ein, an dem die Bewegung stattfindet.  

    Wenn der Lagerort bereits Ihr Standardlagerort als Lagermitarbeiter ist, wird der Lagerortcode automatisch hinzugefügt.  
4. Geben Sie im Feld **Nach Lagerplatzcode** einen Code für den Lagerort ein, an den Sie Artikel umlagern möchten.

    Beispiel: In der Produktion könnte der Lagerplatz der Off. Fert.-Ber.-Lagerplatz sein, wie auf der Lagerortkarte oder in der Arbeitsplatzgruppe definiert ist.  
5. Geben Sie im Feld **Fälligkeitsdatum** das Datum ein, an dem die Umlagerung abgeschlossen sein muss.  
6. Füllen Sie auf jeder Zeile die Felder wie erforderlich aus. Belege für interne Umlagerungen haben eine Zeile pro Umlagerung. Die Zeile enthält sowohl die Entnahme- als auch die Einlagerungsaktionen.
7. Wählen Sie das Feld **Artikelnr.**, um die Seite **Lagerplatzinhaltsliste** zu öffnen. Wählen Sie den zu verschiebenden Artikel basierend auf seiner Verfügbarkeit in Lagerplätzen aus. Sie können auch die Aktion **Lagerplatzinhalt abrufen** auswählen, um die internen Umlagerungszeilen basierend auf Ihren Filtern zu füllen.  

    Nachdem Sie den Artikel ausgewählt haben, wird das Feld **Von Lagerplatzcode** automatisch entsprechend dem ausgewählten Lagerplatzinhalt ausgefüllt. Sie können einen beliebigen Lagerplatz auswählen, in dem der Artikel verfügbar ist. Die Felder **Artikelnr.** und **Von Lagerplatzcode** sind verwandt. Wenn Sie den Wert in einem Feld ändern, ändert sich möglicherweise der Wert im anderen.  

    Das Feld **Zu Lagerplatzcode** wird mit dem Wert ausgefüllt, den Sie in der Kopfzeile eingegeben haben. Sie können ihn auf der Zeile in jeden anderen Lagerplatzcode ändern, der nicht gesperrt oder für spezielle Zwecke bestimmt ist. Weitere Informationen finden Sie unter [Das dedizierte Feld](warehouse-how-to-create-individual-bins.md#the-dedicated-field).  

8. Nachdem Sie definiert haben, aus welchen Lagerplätze die Artikel verschoben werden sollen, geben Sie im Feld **Menge** die umzulagernde Menge ein.  

    > [!NOTE]  
    > Die Menge muss in dem Lagerplatz verfügbar sein, der im Feld **Von Lagerplatzcode** angegeben ist.  

9. Wenn Sie bereit sind, die Umlagerung zu verarbeiten, wählen Sie die Aktion **Lagerbestandsumlagerung erstellen** aus.  

    > [!NOTE]  
    >  Nachdem Sie die Lagerbestandsumlagerung erstellt haben, werden die Zeilen für die interne Umlagerung gelöscht.  

Führen Sie den Rest der ungeplanten Umlagerung auf der Seite **Lagerbestandsumlagerung** auf dieselbe Weise durch, wie Sie eine Lagerplatzumlagerung basierend auf Herkunftsbelegen ausführen würden.

### <a name="to-record-the-inventory-movement"></a><a name="to-record-the-inventory-movement"></a><a name="to-record-the-inventory-movement"></a>So erfassen Sie die Lagerbestandsumlagerung

1. Öffnen Sie auf der Seite **Lagerbestandsumlagerung** das Dokument, für das die Umlagerung erfasst werden soll.  
2. Im Feld **Lagerplatzcode** auf den Umlagerungszeilen der Lagerplatz, bei dem der Artikel aus dem er kommissioniert werden muss, an dem der Artikel verfügbar ist. Sie können den Lagerplatz bei Bedarf ändern.
3. Führen Sie die Umlagerung durch und geben Sie die Informationen über die tatsächlich umgelagerte Menge in das Feld **Bewegungsmenge** ein. Die Werte in den Zeilen "Entnahme" und "Einlagerung" müssen gleich sein. Andernfalls kann die Lagerplatzumlagerung nicht gebucht werden.

    Wenn Sie die Artikel für eine Zeile aus mehr als einem Lagerplatz entnehmen müssen, beispielsweise, da sich die gesamte Menge nicht in dem Lagerplatz befindet, verwenden Sie die Aktion **Zeile aufteilen** im Inforegister **Zeilen**. Die Aktion erstellt eine Zeile für die zu bearbeitende Restmenge.  
4. Wählen Sie die Aktion **Lagerbestandsumlagerung registrieren** aus.  

Folgendes passiert während des Buchungsprozesses:

* Lagerplatzeinträge geben an, dass die Menge von den Entnahmelagerplätzen zu den Eingangslagerplätzen übertragen wird.

## <a name="to-move-items-with-the-item-reclassification-journal"></a><a name="to-move-items-with-the-item-reclassification-journal"></a><a name="to-move-items-with-the-item-reclassification-journal"></a>Um Artikel mit dem Artikel-Umlagerungs-Buch.-Blatt umzulagern

Statt Umlagerungsbelege zu verwenden, können Sie Umlagerungen von Artikeln erfassen, indem Sie Lagerplatzcodes auf Artikeln neu klassifizieren. Weitere Informationen finden Sie unter [Erfassen, Regulieren und Umbuchen von Lagerbestand mithilfe von Buch.-Blättern](inventory-how-count-adjust-reclassify.md).

> [!NOTE]  
> Durch Umlagerungen, die mit Umbuch.-Blättern gebucht werden, werden Umlagerungsbelege nicht zur Umlagerung bereit.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Element umklassifizieren. Erfassungen** ein und wählen Sie dann den zugehörigen Link.  
2. Degfinieren Sie in jeder Buch.-Blattzeile die Lagerplätze, von denen Sie Artikel umlagern möchten, indem Sie die Felder **Lagerplatzcode** und **Neuer Lagerplatzcode** ausfüllen.  

    1. Um den gesamten Inhalt eines Lagerplatzes in einen anderen Lagerplatz umzulagern, wählen Sie die Aktion **Lagerplatzinhalt holen** aus.  
    2. Verwenden Sie die Filter, um den Lagerplatz zu suchen, der die Artikel enthält, die Sie umlagern möchten, und wählen Sie **OK**. Die Buch.-Blattzeilen werden mit dem Inhalt des Lagerplatzes ausgefüllt.  
3. Füllen Sie die übrigen Felder jeder Buch.-Blattzeile aus.
4. Buchen Sie das Umbuch.-Blatt.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/manage-internal-warehouse-processes/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
