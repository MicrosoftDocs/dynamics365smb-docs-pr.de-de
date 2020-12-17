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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 447012a66e75e1acf03f2aff1ba6b6922164312f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918563"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Verwalten von Anhängen, Links und Notizen zu Karten und Dokumenten

In der Infobox der meisten Karten und Dokumente können Sie Dateien anhängen, Links hinzufügen und Notizen schreiben. Bei Links und Notizen können Sie dies auch auf der Listenseite tun, indem Sie zuerst die entsprechende Zeile auswählen.

Um einen dieser angehängten Informationstypen anzuzeigen oder zu ändern, müssen Sie zuerst die Registerkarte **Anhänge** in der Infobox öffnen. Die Zahl hinter dem Titel der Registerkarte gibt an, wie viele angehängte Dateien, Links oder Notizen für die Karte oder das Dokument vorhanden sind.

Anhänge, Links und Notizen bleiben angehängt, wenn die Karte oder das Dokument in einen anderen Status verarbeitet wird, z. B. von einem laufenden Kundenauftrag zu einer gebuchten Kundenrechnung. Allerdings wird keiner der Anhangstypen vom System ausgegeben, z. B. beim Drucken oder beim Speichern in einer Datei.

> [!NOTE]
> Wenn Sie einen Verkaufsauftrag oder eine Einkaufsbestellung teilweise versenden und in Rechnung stellen, wird der Anhang nur der endgültigen Rechnung dieser Bestellung beigefügt. Wenn Sie mit der Funktion „Abgrenzungen“ abrechnen, wird der Anhang entsprechend nur an die Sachkontenbucheinträge für den Beleg angehängt, nicht jedoch an die Abgrenzungseinträge.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>So hängen Sie eine Datei an eine Eikaufsrechnung an
Sie können jede Art von Datei, die Text, Bilder oder Videos enthält, an eine Karte oder ein Dokument anhängen. Dies ist beispielsweise nützlich, wenn Sie eine Lieferantenrechnung als PDF-Datei auf der zugehörigen Einkaufsrechnung in [!INCLUDE[d365fin](includes/d365fin_md.md)] speichern möchten.

> [!NOTE]
> Dateien, die mit der Funktion Eingehende Belege angehängt sind, werden auf der Registerkarte **Anhänge** nicht eingeschlossen. Weitere Informationen finden Sie unter [Eingehende Belege](across-income-documents.md).

Das folgende Verfahren basiert auf einer Einkaufsrechnung. Die Schritte sind für alle anderen unterstützten Dokumente und Karten ähnlich.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Kaufrechnungen** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie den Verkaufsauftrag, den Sie einer Datei zuordnen möchten.
3. Öffnen Sie in der Infobox die Registerkarte **Anhänge**.
4. Wählen Sie den Wert hinter dem Feld **Belege** z. B. "0".
5. Wählen Sie auf der Seite **Angefügte Dokumente** im Feld **Anhang** die Aktion **Datei auswählen** aus.
5. Wählen Sie eine Datei aus jedem Lagerort, und wählen Sie dann die Schaltfläche **Öffnen** aus.

Die Datei wird nun der Einkaufsrechnung zugeordnet.

## <a name="to-view-an-attached-file"></a>So zeigen Sie eine angehängte Datei an
1. Öffnen Sie in der Infobox die Registerkarte **Anhänge**.
2. Wählen Sie den Wert hinter dem Feld **Belege** z. B. "1".
3. Wählen Sie auf der Seite **Angefügte Dokumente** die Aktion **Vorschau** aus.
4. Öffnen Sie die heruntergeladene Datei.

## <a name="to-save-a-document-as-a-pdf-attachment"></a>So speichern Sie ein Dokument als PDF-Anhang
Wann immer Sie ein Dokument als Datei speichern müssen, können Sie die Aktion **Anhängen als PDF** verwenden, um den aktuellen Dokumentinhalt als PDF-Datei zu erfassen, die an die FactBox des Dokuments angehängt wird. Dies ist z.B. nützlich, wenn Dokumente mehreren Schritten in einem Prozess folgen, wie z.B. einem Verkaufsprozess oder einem Genehmigungs-Workflow, und Sie sich auf einen Ausdruck des vorherigen Schritts beziehen möchten.

Das folgende Verfahren basiert auf einer Auftragsabwicklung. Die Schritte sind für alle unterstützten Dokumente ähnlich.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.
2. Markieren Sie einen Debitorenauftrag, und wählen Sie dann die Aktion **Anhängen als PDF**.

Eine PDF-Datei mit dem aktuellen Inhalt des Kundenauftrags wird der Registerkarte **Anlagen** im Infoboxbereich hinzugefügt.

## <a name="to-add-a-link-from-an-item-card"></a>Um einen Link von einer Artikelkarte hinzuzufügen
Sie können jeder URL oder jedem Pfad einen Link von einer Karte oder einem Dokument hinzufügen. Dies ist beispielsweise hilfreich, wenn Sie eine Artikelkarte mit dem Artikelkatalog des Lieferanten verknüpfen möchten.

Das folgende Verfahren basiert auf einer Elementkarte. Die Schritte sind für alle anderen unterstützten Belege und Karten gleich.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.
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

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Verkaufsauftrag aus, zu dem Sie einen Link hinzufügen möchten, und wählen Sie dann die Registerkarte **Anhänge** in der Infobox.
3. In dem Abschnitt **Notizen** wählen Sie das **+** Symbol.
4. In dem Feld **Hinweis** geben Sie in das Feld einen beliebigen Text ein, z. B. "Dies ist eine dringende Bestellung.".
5. Wählen Sie die Schaltfläche **OK** aus.

Der Hinweis ist jetzt dem Verkaufsauftrag beigefügt.

## <a name="see-also"></a>Siehe auch  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Eingehende Belege](across-income-documents.md)  
[Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)  
