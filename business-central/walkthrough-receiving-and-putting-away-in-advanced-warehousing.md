---
title: Eingang und Einlagerung in erweiterten Lagerfunktionen | Microsoft Docs
description: In Business Central können die eingehenden Prozesse für das Empfangen und Einlagern auf vier Arten, mit den verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausgeführt werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2020
ms.author: sgroespe
ms.openlocfilehash: f71bafe0db7c22c65d7d88bd0e4434ab79bc89b4
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528235"
---
# <a name="walkthrough-receiving-and-putting-away-in-advanced-warehouse-configurations"></a>Exemplarische Vorgehensweise: Eingang und Einlagerung bei erweiterten Lagerkonfigurationen

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

In [!INCLUDE[d365fin](includes/d365fin_md.md)] können die eingehenden Prozesse für das Empfangen und Einlagern auf vier Arten, mit den verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausgeführt werden.  

|Art|Eingangsprozess|Lagerplätze|Geb. Umlag.-Eingänge|Einlagerungen|Komplexitätsebene anzeigen (siehe [Designdetails: Lagerhaus-Einrichtung](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Posteinlieferungsschein und die Einlagerung der Auftragszeile|X|||2|  
|F|Posteinlieferungsschein und Einlagerung aus dem Beleg "Lagereinlagerung"|||X|3|  
|L|Posteinlieferungsschein und Einlagerung aus einem Wareneingangsbeleg||X||4/5/6|  
|T|Posteinlieferungsschein aus einem Wareneingangsbeleg und Posteinlagerung aus einem Einlagerungsbeleg||X|X|4/5/6|  

Weitere Informationen finden Sie unter [Designdetails: Eingehender Lagerfluss](design-details-inbound-warehouse-flow.md).  

In der folgenden Vorgehensweise wird Methode D in der vorhergegangenen Tabelle beschrieben.  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise  
In der erweiterten Lagerkonfiguration verwenden Sie dann, wenn Ihr Standort so eingerichtet ist, dass er Eingangs- und Einlagerungsverarbeitung durchführen muss, die Seite **Lagerort-Eingang** zur Aufzeichnung und Buchung des Eingangs von Artikeln zu mehreren eingehenden Aufträgen. Wenn der Wareneingang gebucht wird, wird mindestens ein Einlagerungsbeleg erstellt, um Lagermitarbeiter anzuweisen, den erhaltenden Artikel zu entnehmen und an festgelegte Orte gemäß der Lagerplatzeinrichtung oder an andere Lagerplätze zu bringen. Die spezifische Position der Artikel wird erfasst, wenn die Einlagerung registriert wird. Der eingehende Herkunftsbeleg kann eine Einkaufsbestellung, eine Verkaufsreklamation, ein eingehender Umlagerungsauftrag oder Montage oder ein Fertigungsauftrag sein, dessen Endprodukt zur Einlagerung bereitsteht. Wenn der Wareneingang aus einem eingehenden Auftrag erstellt wird, kann mehr als ein eingehender Herkunftsbeleg für den Wareneingang abgerufen werden. Wenn Sie diese Methode verwenden, können Sie viele Artikel erfassen, die von unterschiedlichen eingehenden Bestellungen mit einem Wareneingang ankommen.  

In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert.  

-   WEISSEN Lagerort für Eingang und Einlagerung einrichten.  
-   Erstellen und Freigeben zweier Bestellungen für volle Lagerdurchlaufzeit.  
-   Erstellen und Buchen eines Wareneingangsbelegs für mehrere Einkaufszeilen von bestimmten Kreditoren.  
-   Erfassen einer Einlagerungszeile für die eingegangenen Artikel.  

## <a name="roles"></a>Rollen  
Die Aufgaben in dieser Demonstration werden von den folgenden Benutzerrollen ausgeführt:  

-   Lagerortleiter  
-   Einkäufer  
-   Eingangsmitarbeiter  
-   Lagermitarbeiter  

## <a name="prerequisites"></a>Voraussetzungen  
Für diese exemplarische Vorgehensweise gelten folgende Voraussetzungen:  

-   CRONUS AG installieren.  
-   So machen Sie sich anhand der nachfolgenden Schritte selbst zu einem Lagermitarbeiter am Standort WHITE:  

1.  Wählen Sie die ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") Symbol, geben Sie **Lagerort-Mitarbeiter** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie das Feld **Benutzer-ID** aus, und wählen Sie Ihr eigenes Benutzerkonto auf der Seite **Benutzer** aus.  
3.  Geben Sie im Feld **Lagerortcode** WHITE ein.  
4.  Wählen Sie das Feld **Standard** aus.  

## <a name="story"></a>Hintergrund  
Ellen, die Einkäuferin bei der CRONUS AG ist, erstellt zwei Bestellungen für Zubehörartikel von den Kreditoren 10000 und 20000, die zum WHITE-Lagerhaus geliefert werden sollen. Wenn die Lieferungen im Lagerankommen, verwendet, Sammy, der für das Empfangen von Artikeln der Kreditoren 10000 und 20000 zuständig ist, einen Filter, um Wareneingangszeilen für die Bestellungen zu erstellen, die von den beiden Kreditoren ankommen. Sammy bucht die Artikel als in den Lagerbestand im Wareneingang eingegangen und stellt die Artikel für Verkauf oder anderen Bedarf bereit. John, der Lagermitarbeiter, nimmt die Artikel vom Wareneingangslagerplatz und lagert sie ein. Er lagert alle Einheiten in ihren Standardlagerplätze ein, mit Ausnahme von 40 der 100 eingegangenen Scharniere, die er in der Montageabteilung einlagert, indem er die Einlagerungsanforderungszeile aufteilt. Wenn John die Einlagerung registriert, werden die Lagerplatzinhalte aktualisiert, und die Artikel werden für die Kommissionierung aus dem Lager bereitgestellt.  

## <a name="reviewing-the-white-location-setup"></a>Überprüfung des Setup des WEISSEN Lagerorts  
Das Einrichten der Seite **Standortkarte** definiert die Warenflüsse des Unternehmens.  

### <a name="to-review-the-location-setup"></a>So prüfen Sie die Lagerorteinrichtung  

1.  Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Standorte** ein, und wählen Sie dann den entsprechenden Link.  
2.  Öffnen Sie die WHITE Lagerortkarte.  
3.  Beachten Sie im Inforegister **Lager**, dass das Kontrollkästchen **Gesteuerte Einlag. u. Kommiss.** ausgewählt ist.  

    Dies bedeutet, dass der Ort für die höchste Komplexitätsebene eingerichtet wird, widergespiegelt durch die Tatsache, dass alle Lagerdurchlaufzeitkontrollkästchen im Inforegister aktiviert sind.  

4.  Beachten Sie im Inforegister **Lagerplätze**, dass Lagerplätze in den Feldern **Wareneingangslagerplatzcode** und **Warenausgangslagerplatzcode** angegeben sind.  

Das bedeutet, dass beim Erstellen eines Wareneingangs dieser Lagerplatzcode standardmäßig zum Kopf des Wareneingangsbelegs und zu den Zeilen der resultierenden Einlagerung kopiert wird.  

## <a name="creating-the-purchase-orders"></a>Erstellen der Bestellungen  
Bestellungen sind die häufigste Art des eingehenden Herkunftsbelegs.  

### <a name="to-create-the-purchase-orders"></a>So erstellt man Bestellungen  

1.  Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Einkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie die Aktion **Neu** aus.  
3.  Erstellen Sie eine Bestellung für den Kreditor 10000 auf das Arbeitsdatum (23. Januar) mit den folgenden Einkaufszeilen.  

    |Artikel|Lagerortcode|Menge|  
    |----------|-------------------|--------------|  
    |70200|WEISS|100 STÜCK|  
    |70201|WEISS|50 STÜCK|  

    Fahren Sie fort, das Lager zu informieren, dass die Einkaufsbestellung in Lagerdurchlaufzeit bereit ist, wenn die Lieferung eingeht.  

4.  Wählen Sie die Aktion **Freigabe** aus.  

    Fahren Sie fort mit dem Estellen der zweiten Einkaufsbestellung.  

5.  Wählen Sie die Aktion **Neu** aus.  
6.  Erstellen Sie eine Bestellung für den Kreditor 20000 auf das Arbeitsdatum mit den folgenden Einkaufszeilen.  

    |Artikel|Lagerortcode|Menge|  
    |----------|-------------------|--------------|  
    |70100|WEISS|10 CAN|  
    |70101|WEISS|12 CAN|  

    Wählen Sie die Aktion **Freigabe** aus.  

    Die Lieferungen von Artikeln der Kreditoren 10000 und 20000 sind im WHITE-Lager eingegangen, und Sammy beginnt mit der Verarbeitung der Einkaufslieferungen.  

## <a name="receiving-the-items"></a>Eingang der Artikel  
Auf der Seite **Wareneingang** können Sie mehrere eingehende Aufträge für Herkunftsbelege, wie eine Bestellung, verwalten.  

### <a name="to-receive-the-items"></a>So erhalten Sie die Artikel  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Wareneingänge** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die Aktion **Neu** aus.  
3.  Geben Sie im Feld **Lagerortcode** WHITE ein.  
4.  Wählen Sie die **Filter zum Holen von Herk.-Belegen verwenden** Aktion aus.  
5.  Geben Sie im Feld **Code** **ZUBEHÖR** ein.  
6.  Geben Sie im Feld **Beschreibung** **Kreditoren 10000 und 20000** ein.  
7.  Wählen Sie die Aktion **Bearbeiten** aus.  
8.  Geben Sie im Inforegister **Einkauf** im Feld **Eink. von Kred.-Nr. Filter** den Wert **10000&#124;20000** ein.  
9. Wählen Sie die Aktion **Ausführen** aus. Der Wareneingang wird mit vier Zeilen gefüllt, die Einkaufszeilen für die angegebenen Kreditoren darstellen. Das Feld **Eingehende Menge** wird ausgefüllt, da Sie das Kontrollkästchen **Bewegungsmenge nicht ausfüllen** auf der Seite **Filter um Herkunftsdokument abzurufen** nicht markiert haben.  
10. Wenn Sie einen Filter verwenden möchten, wie zuvor in diesem Abschnitt beschrieben, können Sie optional auf der Registerkarte Aktionen in der Gruppe Funktionen **Herkunftsbeleg holen** auswählen, und dann Einkaufsbestellungen aus den entsprechenden Kreditoren auswählen.  
11. Wählen Sie die Aktion **Beleg buchen** ausn und wählen Sie dann die Schaltfläche **Ja** aus.  

    Die positiven Artikelposten spiegeln die gebuchten Zubehör-Einkaufslieferungen der Kreditoren 10000 und 20000 wieder, und die Artikel können im Lager aus dem Wareneingangslagerplatz eingelagert werden.  

## <a name="putting-the-items-away"></a>Einlagerung von den Artikeln  
Auf der Seite **Lagereinlagerung** können Sie Einlagerungen für einen spezifischen Wareneingangsbeleg, der sich auf mehrere Herkunftsbelege bezieht, verwalten. Wie alle Lageraktivitätsbelege wird jeder Artikel in der Einlagerung durch eine Entnahme- und eine Einlagerungszeile dargestellt. Im folgenden Verfahren ist der Lagerplatzcode in den Entnahmezeilen der Standardplatz für Wareneingänge am WEISSEN Lagerort, W-08-0001.  

### <a name="to-put-the-items-away"></a>So lagern Sie die Artikel ein  
1.  Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Einlagerungen** ein, und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie den einzigen Lager-Einlagerungsbeleg in der Liste aus und wählen Sie dann die Aktion **Bearbeiten**.  

    Der Einlagerungsbeleg wird geöffnet mit insgesamt acht Take- oder Place-Zeilen für die vier Einkaufsauftragszeilen.

    Der Lagermitarbeiter erhält die Information, dass in der Montageabteilung 40 Scharniere benötigt werden; er teilt die einzelne Place-Zeile so, dass eine zweite Place-Zeile für Lagerplatz W-02-0001 in der Montageabteilung entsteht und platziert diesen Teil der eingegangenen Scharniere dort.  

3.  Wählen Sie die zweite Zeile auf der Seite **Lagereinlagerung** aus, die Einlagerungszeile für Artikel 70200.  
4.  Ändern Sie den Wert im Feld **Zu verarbeitende Menge** von 100 zu 60.  
5.  Wählen Sie auf dem Inforegister **Zeilen** die Option **Funktionen**, und klicken Sie dann auf **Zeile aufteilen**. Eine neue Zeile wird für Artikel 70200 mit 40 in Feld **Zu verarbeitende Menge** eingefügt.  
6.  Geben Sie im Feld **Lagerplatzcode** W-02-0001 ein. Das Feld **Gebietscode** wird automatisch ausgefüllt.  

    Fahren Sie fort mit dem Registrieren der Einlagerung.  

7.  Wählen Sie die Aktion **Beleg buchen** aus und wählen Sie dann die Schaltfläche **Ja** aus.  

    Das erhaltene Zubehör wird jetzt in den Standardlagerplätzen der Artikel eingelagert, und 40 Scharniere werden in die Montageabteilung gebracht. Die eingegangenen Artikel sind jetzt für die Kommissionierung zum internen Bedarf, wie etwa für Montageaufträge, oder zum externen Bedarf, wie etwa für Verkaufslieferungen, verfügbar.  

## <a name="see-also"></a>Siehe auch  
 [Einlagern von Artikeln mit Lagereinlagerungen](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Umlagerung von Artikeln in erweiterten Lagerkonfigurationen](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Designdetails: Eingehender Lagerfluss](design-details-inbound-warehouse-flow.md)   
 [Exemplarische Vorgehensweise: Eingang und Einlagerung in Basis-Lagerkonfigurationen](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)   
 [Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)
