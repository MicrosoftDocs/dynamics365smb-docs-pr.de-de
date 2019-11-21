---
title: Anhänge, Links und Notizen zu Datensätzen hinzufügen| Microsoft Docs
description: Fügen Sie einem Dokument oder einer Website einen Link zu einem bestimmten Datensatz hinzu, beispielsweise zu einer Debitorenkarte oder einem Dokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/21/2019
ms.author: sgroespe
ms.openlocfilehash: 88e6a04a8e4a992b6a5df3fee87104eba7b5510e
ms.sourcegitcommit: be1e2c49a8434d3f440d5a201508af9c3c8cc87f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2019
ms.locfileid: "2649788"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Verwalten von Anhängen, Links und Notizen zu Karten und Dokumenten

In der Infobox der meisten Karten und Dokumente können Sie Dateien anhängen, Links hinzufügen und Notizen schreiben. Bei Links und Notizen können Sie dies auch auf der Listenseite tun, indem Sie zuerst die entsprechende Zeile auswählen.

Um einen dieser angehängten Informationstypen anzuzeigen oder zu ändern, müssen Sie zuerst die Registerkarte **Anhänge** in der Infobox öffnen. Die Zahl hinter dem Titel der Registerkarte gibt an, wie viele angehängte Dateien, Links oder Notizen für die Karte oder das Dokument vorhanden sind.

Anhänge, Links und Notizen bleiben angehängt, wenn die Karte oder das Dokument in einen anderen Status verarbeitet wird, z. B. von einem laufenden Kundenauftrag zu einer gebuchten Kundenrechnung. Beachten Sie jedoch, dass keiner der Anhangstypen vom System ausgegeben wird, z. B. beim Drucken oder beim Speichern in einer Datei.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>So hängen Sie eine Datei an eine Eikaufsrechnung an
Sie können jede Art von Datei, die Text, Bilder oder Videos enthält, an eine Karte oder ein Dokument anhängen. Dies ist beispielsweise nützlich, wenn Sie eine Lieferantenrechnung als PDF-Datei auf der zugehörigen Einkaufsrechnung in [!INCLUDE[d365fin](includes/d365fin_md.md)] speichern möchten.

> [!NOTE]
> Dateien, die mit der Funktion Eingehende Belege angehängt sind, werden auf der Registerkarte **Anhänge** nicht eingeschlossen. Weitere Informationen finden Sie unter [Eingehende Belege](across-income-documents.md).

Das folgende Verfahren basiert auf einer Auftragsabwicklung. Die Schritte sind für alle anderen unterstützten Belege und Karten ähnlich.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Kaufrechnungen** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie den Verkaufsauftrag, den Sie einer Datei zuordnen möchten.
3. Öffnen Sie in der Infobox die Registerkarte **Anhänge**.
4. Wählen Sie den Wert hinter dem Feld **Belege** z. B. "0".
5. Auf der Seite **Beleg anfügen** im Feld **Dateianhang**, wählen Sie die Schaltfläche **Wählen Sie die Datei aus** aus.
5. Wählen Sie eine Datei aus jedem Lagerort, und wählen Sie dann die Schaltfläche **Öffnen** aus.

Die Datei wird nun der Einkaufsrechnung zugeordnet.

## <a name="to-add-a-link-from-an-item-card"></a>Um einen Link von einer Artikelkarte hinzuzufügen
Sie können jeder URL oder jedem Pfad einen Link von einer Karte oder einem Dokument hinzufügen. Dies ist beispielsweise hilfreich, wenn Sie eine Artikelkarte mit dem Artikelkatalog des Lieferanten verknüpfen möchten.

Das folgende Verfahren basiert auf einer Elementkarte. Die Schritte sind für alle anderen unterstützten Belege und Karten gleich.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie das Element aus, zu dem Sie einen Link hinzufügen möchten, und wählen Sie dann die Registerkarte **Anhänge** in der Infobox.
3. In dem **Link**, wählen Sie das **+** Symbol.
4. Geben Sie im Feld **Link Adresse** den Link ein.

    Der Link muss eine gültige Internet- oder Intranet-URL sein.

5. Geben Sie im Feld **Beschreibung** die Informationen zu dem Link ein.  
6. Wählen Sie die Schaltfläche **OK** aus.

Der Link ist jetzt an die Artikel-Karte angehängt.  

## <a name="to-write-a-note-on-a-sales-order"></a>So schreiben Sie eine Notiz zu einem Verkaufsauftrag
Sie können eine Notiz auf ein Dokument oder eine Karte schreiben, um beispielsweise anderen Benutzern des Dokuments oder der Karte spezielle Anweisungen zu übermitteln. Sie können Dateilinks und URLs in Notizen einfügen.

> [!NOTE]
> Hinweise auf der Registerkarte **Anhänge** haben nichts mit der internen Notizfunktion zu tun, die hauptsächlich für die Kommunikation zwischen Workflowbenutzern verwendet wird. Weitere Informationen finden Sie unter [Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md).

Das folgende Verfahren basiert auf einer Auftragsabwicklung. Die Schritte sind für alle anderen unterstützten Dokumente und Karten ähnlich.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Verkaufsauftrag aus, zu dem Sie einen Link hinzufügen möchten, und wählen Sie dann die Registerkarte **Anhänge** in der Infobox.
3. In dem Abschnitt **Notizen** wählen Sie das **+** Symbol.
4. In dem Feld **Hinweis** geben Sie in das Feld einen beliebigen Text ein, z. B. "Dies ist eine dringende Bestellung.".
5. Wählen Sie die Schaltfläche **OK** aus.

Der Hinweis ist jetzt dem Verkaufsauftrag beigefügt.

## <a name="see-also"></a>Siehe auch  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Eingehende Belege](across-income-documents.md)  
[Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)  
