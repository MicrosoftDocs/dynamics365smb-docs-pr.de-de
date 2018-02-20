---
title: 'Vorgehensweise: Einlagern von Artikeln mit Lagereinlagerungen | Microsoft Docs'
description: Wenn Ihr Lagerort so eingerichtet wurde, dass die Bearbeitung der Einlagerung und des Wareneingangs erforderlich ist, verwenden Sie die Funktion Einlagerungsbelege, um die Einlagerung der Artikel zu steuern.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6ccc452db91f7c227e052f60d50f8cc0fdf46fd0
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="put-items-away-with-warehouse-put-aways"></a>Einlagern von Artikeln mit Lagereinlagerungen
Wenn Ihr Lagerort so eingerichtet wurde, dass die Bearbeitung der Einlagerung und des Wareneingangs erforderlich ist, verwenden Sie die Funktion Einlagerungsbelege, um die Einlagerung der Artikel zu steuern.  

Wenn Sie eine Einlagerung buchen, werden die Herkunftsbelege, wie Einkaufsbestellung, eingehende Umlagerung oder Verkaufsreklamation aktualisiert, die eingegangene Menge als Artikelposten gebucht und die Zeilen über die eingegangenen Artikel an die Einlagerungsfunktion in der Logistik gesendet. Wenn Sie die interne Einlagerung und Kommissionierung nutzen, kann die interne Einlagerung auch Zeilen zur Einlagerung erzeugen.  

Abhängig von der Logistik-Einrichtung werden die Zeilen entweder im Einlagerungsvorschlag verfügbar gemacht, oder es werden sofort Einlagerungsanweisungen erstellt. Weitere Informationen finden Sie unter [Kommissionierungen im Vorschlag bearbeiten](warehouse-how-to-plan-put-aways-in-worksheets.md).  

Zusätzlich zu den Standardoptionen für das Erstellen von Lagereinlagerungen, die in diesem Thema beschrieben werden, können Sie die Einlagerung im zugehörigen gebuchten Wareneingang erstellen. Dies ist nützlich, wenn Sie die Einlagerungszeilen gelöscht haben, oder wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden und sich entschieden haben, den Einlagerungsvorschlag nicht zu verwenden, da Sie Einlagerungsanweisungen aus gebuchte Wareneingangszeilen folgendermaßen erstellen oder wiedererstellen können.  

## <a name="to-put-items-away-without-directed-put-away-and-pick"></a>So lagern Sie Artikel ein, ohne die gesteuerte Einlagerung und Kommissionierung zu verwenden:  
1.  Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Wareneingang** ein und wählen den entsprechenden Link aus.  
2.  Öffnen Sie die Einlagerung, die für die Bearbeitung bereit ist.  

    Sie können den Einlagerungszeilen nach verschiedenen Kriterien sortieren, beispielsweise nach Artikel, Regalnummer, Lagerplatz oder Fälligkeitsdatum, wodurch Sie den Einlagerungsprozess optimieren können.  
3.  Geben Sie in jeder Zeile im Feld **Bewegungsmenge** die Menge ein, die Sie einlagern möchten.  
4.  Nachdem Sie das Einlagern der Artikel abgeschlossen haben, wählen Sie die Aktion **Einlagerung registrieren**aus, um den Abschluss der Aktivität zu speichern und die Artikel zur Kommissionierung verfügbar zu machen.  

## <a name="to-put-items-away-with-directed-put-away-and-pick"></a>So lagern Sie Artikel mit der gesteuerten Einlagerung und Kommissionierung ein:  
1.  Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Wareneingang** ein und wählen den entsprechenden Link aus.
    Wenn Einlagerungsanweisungen erstellt wurden, wird eine Einlagerung angezeigt.  
2.  Öffnen Sie die Lagereinlagerung, mit der Sie arbeiten möchten.  
3.  Wenn dies in Ihrem Lager erforderlich ist, geben Sie Ihre Benutzer-ID im Inforegister **Allgemein** ein, wenn Sie anfangen, an einer bestimmten Einlagerung zu arbeiten.  
4.  Führen Sie die Entnahme- und Einlagerungsaktionen aus, die im Feld **Aktionsart** auf den Zeilen angegeben sind.  

    Beachten Sie, dass jede Wareneingangszeile zu mindestens zwei Zeilen in der Einlagerung geworden ist.  

    -   Die erste Zeile mit dem Feld **Entnahme** im Feld **Aktionsart** zeigt an, wo sich die Artikel im Wareneingangsbereich befinden. Sie können die Felder "Zone" und "Lagerplatz" in dieser Zeile nicht ändern.  
    -   Die nächste Zeile, mit **Einlagerung** in der **Aktionsart** zeigt an, wo Sie die Artikel im Lager einlagern müssen. Wenn das Lager eine große Menge an Artikeln in einer Wareneingangszeile erhält, kann es sein, dass die Anwendung diese in mehrere Lagerplätze einlagern muss und es eine Zeile der Art Einlagerung für jeden Lagerplatz gibt.  

        Wenn die Zeilen der Art "Entnahme" und "Einlagerung" einer Wareneingangszeile nicht direkt aufeinander folgen, Sie dies aber wünschen, können Sie die Zeilen sortieren lassen, indem Sie **Artikel** im Feld **Sortiermethode** auf dem Inforegister **Allgemein** auswählen.  

        Wenn die physische Struktur des Lagers den Lagerplatzprioritäten entspricht, können Sie die Sortiermethode **Lagerplatzpriorität** verwenden, um eine Einlagerungsrunde vorzubereiten, die die Wege im Lager minimiert.  

5.  Wenn Sie alle Artikel so in die Lagerplätze eingelagert haben, wie es die Anweisungen vorsehen, wählen Sie die Aktion **Einlagerung registrieren** aus.  

An Lagerorten, die für die Verwendung der gesteuerten Einlagerung und Kommissionierung eingerichtet sind, sind die folgenden Einstellungen Voraussetzungen für das obige Verfahren:  

- So richten Sie eine Einlagerungsmethode ein: Weitere Informationen finden Sie unter [Einrichten von Aktivitätvorlagen](warehouse-how-to-set-up-put-away-templates.md).  
- Das Gewicht, Volumen und spezielle Lagerungsanforderungen des Artikels oder der Lagerhaltungsdaten werden festgelegt. Weitere Informationen finden Sie unter Bruttogewicht  
- Die Kapazität, die Lagerplatzart und die Lagerplatzpriorität. Weitere Informationen finden Sie unter Lagerplatzpriorität.  

Die Lagerplatzpriorität wird berücksichtigt, wenn mehr als ein Lagerplatz den Kriterien der Einlagerungsvorlage entspricht. Wenn für mehr als einen Lagerplatz die Kriterien der Einlagerungsvorlage und die Lagerplatzpriorität gleich sind, wird der Lagerplatz mit der höchsten Nummer ausgewählt.

## <a name="to-create-a-put-away-from-a-posted-receipt"></a>Um eine Einlagerung aus dem gebuchten Wareneingang zu erstellen  
 Wenn für Ihren Lagerort die Bearbeitung der Einlagerung und des Wareneingangs erforderlich ist und Sie die Einlagerungszeilen gelöscht haben, oder wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden und sich entschieden haben, den Einlagerungsvorschlag nicht zu verwenden, können Sie Einlagerungsanweisungen für gebuchte Wareneingangszeilen folgendermaßen erstellen oder wiedererstellen.

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen"), geben **Geb. Wareneingang** ein und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie einen gebuchten Wareneingang aus, der eingelagert werden muss.  
3.  Wählen Sie die Aktion **Karte** aus.  

    Wenn das Feld **Belegstatus** leer ist, wurde der Wareneingang noch nicht eingelagert. Sonst zeigt das Feld an, dass der Wareneingang teilweise oder komplett eingelagert wurde.  

4.  Wenn der Wareneingang teilweise oder überhaupt nicht eingelagert wurde, wählen Sie die Aktion **Einlagerung erstellen** aus.  
5.  Füllen Sie das Anforderungsfenster der Stapelverarbeitung zum Erstellen der Einlagerung so aus, wie Sie es für geeignet halten, und wählen Sie **OK**.   

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

