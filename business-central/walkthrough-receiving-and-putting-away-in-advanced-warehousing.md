---
title: Wareneingang und Einlagerung in der erweiterten Lagerhaltung
description: 'Die eingehenden Prozesse für den Empfang und die Einlagerung können auf vier Arten mit unterschiedlichen Funktionalitäten durchgeführt werden, je nach Komplexitätsgrad des Lagers.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="walkthrough-receiving-and-putting-away-in-advanced-warehouse-configurations"></a><a name="walkthrough-receiving-and-putting-away-in-advanced-warehouse-configurations"></a>Exemplarische Vorgehensweise: Eingang und Einlagerung bei erweiterten Lagerkonfigurationen

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

In [!INCLUDE[prod_short](includes/prod_short.md)] tritt der Eingang und das Einlagern mit einer der vier in der folgenden Tabelle beschriebenen Methoden auf.

|Art|Eingangsprozess|Wareneingang erforderlich|Einlagerung erforderlich|Komplexitätsgrad (Weitere Informationen unter [Lagermanagementübersicht](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Posteinlieferungsschein und die Einlagerung der Auftragszeile|||Keine dedizierte Lageraktivität.|  
|B|Posteinlieferungsschein und Einlagerung aus dem Beleg "Lagereinlagerung"||Aktiviert|Basis: Auftragsbezogene Logistik|  
|U|Posteinlieferungsschein und Einlagerung aus einem Wareneingangsbeleg|Aktiviert||Basis: Konsolidierte Eingangs-/Versandbuchung für mehrere Bestellungen.|  
|T|Posteinlieferungsschein aus einem Wareneingangsbeleg und Posteinlagerung aus einem Einlagerungsbeleg|Aktiviert|Aktiviert|Erweitert|  

Weitere Informationen finden Sie unter [Eingehender Lagerfluss](design-details-inbound-warehouse-flow.md).

In der folgenden Vorgehensweise wird Methode D in der vorhergegangenen Tabelle beschrieben.  

## <a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise

In der erweiterten Lagerkonfiguration verwenden Sie dann, wenn Ihr Standort so eingerichtet ist, dass er Eingangs- und Einlagerungsverarbeitung durchführen muss, die Seite **Lagerort-Eingang** zur Aufzeichnung und Buchung des Eingangs von Artikeln zu mehreren eingehenden Aufträgen. Wenn der Lagereingang gebucht wird, werden ein oder mehrere Belege für die Einlagerung erstellt, um die Arbeitskräfte im Lager anzuweisen, die empfangenen Artikel zu nehmen und sie an den vorgesehenen Plätzen gemäß der Einrichtung der Lagerplätze oder in anderen Lagerplätzen zu platzieren. Die spezifische Platzierung der Artikel wird bei der Registrierung der Lager-Einlagerung im Datensatz festgehalten. Der eingehende Herkunftsbeleg kann eine Einkaufsbestellung, eine Verkaufsreklamation, ein eingehender Umlagerungsauftrag oder Montage oder ein Fertigungsauftrag sein, dessen Endprodukt zur Einlagerung bereitsteht. Wenn der Wareneingang aus einem eingehenden Auftrag erstellt wird, kann mehr als ein eingehender Herkunftsbeleg für den Wareneingang abgerufen werden. Wenn Sie diese Methode verwenden, können Sie viele Artikel erfassen, die von unterschiedlichen eingehenden Bestellungen mit einem Wareneingang ankommen.  

In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

-   WEISSEN Lagerort für Eingang und Einlagerung einrichten.  
-   Erstellen und Freigeben zweier Bestellungen für volle Lagerdurchlaufzeit.  
-   Erstellen und Buchen eines Wareneingangsbelegs für mehrere Einkaufszeilen von bestimmten Kreditoren.  
-   Erfassen einer Einlagerungszeile für die eingegangenen Artikel.  

## <a name="roles"></a><a name="roles"></a>Rollen

Die Aufgaben in dieser Demonstration werden von den folgenden Benutzerrollen ausgeführt:  

-   Lagerortleiter  
-   Einkäufer  
-   Eingangsmitarbeiter  
-   Lagermitarbeiter  

## <a name="prerequisites"></a><a name="prerequisites"></a>Voraussetzungen

Für diese exemplarische Vorgehensweise gelten folgende Voraussetzungen:  

-   CRONUS installiert.  
-   So machen Sie sich anhand der nachfolgenden Schritte selbst zu einem Lagermitarbeiter am Standort WHITE:  

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagermitarbeiter** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie das Feld **Benutzer-ID** aus, und wählen Sie Ihr eigenes Benutzerkonto auf der Seite **Benutzer** aus.  
3.  Geben Sie im Feld **Lagerortcode** WHITE ein.  
4.  Wählen Sie das Feld **Standard** aus.  

## <a name="story"></a><a name="story"></a>Hintergrund

Ellen, der Lager-Manager bei CRONUS, erstellt zwei Einkaufsbestellungen für Zubehörartikel von den Kreditoren 10000 und 20000, die an das WHITE-Lager geliefert werden sollen. Wenn die Lieferungen im Lagerankommen, verwendet, Sammy, der für das Empfangen von Artikeln der Kreditoren 10000 und 20000 zuständig ist, einen Filter, um Wareneingangszeilen für die Bestellungen zu erstellen, die von den beiden Kreditoren ankommen. Sammy bucht die Artikel als in den Lagerbestand im Wareneingang eingegangen und stellt die Artikel für Verkauf oder anderen Bedarf bereit. John, der Lagermitarbeiter, nimmt die Artikel vom Wareneingangslagerplatz und lagert sie ein. Er lagert alle Einheiten in ihren Standardlagerplätze ein, mit Ausnahme von 40 der 100 eingegangenen Scharniere, die er in der Montageabteilung einlagert, indem er die Einlagerungsanforderungszeile aufteilt. Wenn John die Einlagerung registriert, werden die Lagerplatzinhalte aktualisiert, und die Artikel werden für die Kommissionierung aus dem Lager bereitgestellt.  

## <a name="reviewing-the-white-location-setup"></a><a name="reviewing-the-white-location-setup"></a>Überprüfung des Setup des WEISSEN Lagerorts

Das Einrichten der Seite **Lagerortkarte** definiert die Warenflüsse des Unternehmens.  

### <a name="to-review-the-location-setup"></a><a name="to-review-the-location-setup"></a>So prüfen Sie die Lagerorteinrichtung

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.  
2.  Öffnen Sie die WHITE Lagerortkarte.  
3.  Beachten Sie im Inforegister **Lager**, dass das Kontrollkästchen **Gesteuerte Einlag. u. Kommiss.** ausgewählt ist.  

    Dies bedeutet, dass der Ort für die höchste Komplexitätsebene eingerichtet wird, widergespiegelt durch die Tatsache, dass alle Lagerdurchlaufzeitkontrollkästchen im Inforegister aktiviert sind.  

4.  Beachten Sie im Inforegister **Lagerplätze**, dass Lagerplätze in den Feldern **Wareneingangslagerplatzcode** und **Warenausgangslagerplatzcode** angegeben sind.  

Das bedeutet, dass beim Erstellen eines Wareneingangs dieser Lagerplatzcode standardmäßig zum Kopf des Wareneingangsbelegs und zu den Zeilen der resultierenden Einlagerung kopiert wird.  

## <a name="creating-the-purchase-orders"></a><a name="creating-the-purchase-orders"></a>Erstellen der Bestellungen

Bestellungen sind die häufigste Art des eingehenden Herkunftsbelegs.  

### <a name="to-create-the-purchase-orders"></a><a name="to-create-the-purchase-orders"></a>So erstellt man Bestellungen

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die Aktion **Neu** aus.  
3.  Erstellen Sie eine Bestellung für den Kreditor 10000 auf das Arbeitsdatum (23. Januar) mit den folgenden Einkaufszeilen.  

    |Artikel|Lagerortcode|Menge|  
    |----------|-------------------|--------------|  
    |70200|WEISS|100 STÜCK|  
    |70201|WEISS|50 STÜCK|  

    Fahren Sie fort, das Lager zu informieren, dass die Einkaufsbestellung in Lagerdurchlaufzeit bereit ist, wenn die Lieferung eingeht.  

4.  Wählen Sie die Aktion **Freigeben**. Der Status ändert sich von Offen auf Freigegeben.

    Fahren Sie fort mit dem Estellen der zweiten Einkaufsbestellung.  

5.  Wählen Sie die Aktion **Neu**.  
6.  Erstellen Sie eine Bestellung für den Kreditor 20000 auf das Arbeitsdatum (23. Januar) mit den folgenden Einkaufszeilen.  

    |Artikel|Lagerortcode|Menge|  
    |----------|-------------------|--------------|  
    |70100|WEISS|10 CAN|  
    |70101|WEISS|12 CAN|  

    Wählen Sie die Aktion **Freigeben**. Der Status ändert sich von Offen auf Freigegeben.

    Die Lieferungen von Artikeln der Kreditoren 10000 und 20000 sind im WHITE-Lager eingegangen, und Sammy beginnt mit der Verarbeitung der Einkaufslieferungen.  

## <a name="receiving-the-items"></a><a name="receiving-the-items"></a>Eingang der Artikel

Auf der Seite **Wareneingang** können Sie mehrere eingehende Aufträge für Herkunftsbelege, wie eine Bestellung, verwalten.  

### <a name="to-receive-the-items"></a><a name="to-receive-the-items"></a>So erhalten Sie die Artikel
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Wareneingänge** ein, und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie die Aktion **Neu**.  
3.  Geben Sie im Feld **Lagerortcode** WHITE ein.  
4.  Wählen Sie **Aktionen** und dann **Funktionen** und wählen Sie die **Filter verwenden, um Src. Docs.** Aktion.  
5.  Geben Sie im Feld **Code** **ZUBEHÖR** ein.  
6.  Geben Sie im Feld **Beschreibung** **Kreditoren 10000 und 20000** ein.  
7.  Wählen Sie die Aktion **Bearbeiten** aus.  
8.  Geben Sie im Inforegister **Einkauf** im Feld **Eink. von Kred.-Nr. Filter** den Wert **10000&#124;20000** ein.  
9. Wählen Sie die Aktion **Ausführen** aus. Der Wareneingang wird mit vier Zeilen gefüllt, die Einkaufszeilen für die angegebenen Kreditoren darstellen. Das Feld **Eingehende Menge** wird ausgefüllt, da Sie das Kontrollkästchen **Bewegungsmenge nicht ausfüllen** auf der Seite **Filter um Herkunftsdokument abzurufen** nicht markiert haben.  
10. Wenn Sie einen Filter verwenden möchten, wie zuvor in diesem Abschnitt beschrieben, können Sie optional auf der Registerkarte Aktionen in der Gruppe Funktionen **Herkunftsbeleg holen** auswählen, und dann Einkaufsbestellungen aus den entsprechenden Kreditoren auswählen.  
11. Wählen Sie **Buchen**, dann die Aktion **Empfang buchen** und anschließend die Schaltfläche **Ja**.  

    Die positiven Artikelposten spiegeln die gebuchten Zubehör-Einkaufslieferungen der Kreditoren 10000 und 20000 wieder, und die Artikel können im Lager aus dem Wareneingangslagerplatz eingelagert werden.  

## <a name="putting-the-items-away"></a><a name="putting-the-items-away"></a>Einlagerung von den Artikeln

Auf der Seite **Lagereinlagerung** können Sie Einlagerungen für einen spezifischen Wareneingangsbeleg, der sich auf mehrere Herkunftsbelege bezieht, verwalten. Wie alle Lageraktivitätsbelege wird jeder Artikel in der Einlagerung durch eine Entnahme- und eine Einlagerungszeile dargestellt. Im folgenden Verfahren ist der Lagerplatzcode in den Entnahmezeilen der Standardplatz für Wareneingänge am WEISSEN Lagerort, W-08-0001.  


### <a name="to-put-the-items-away"></a><a name="to-put-the-items-away"></a>So lagern Sie die Artikel ein
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einlagerungen** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie den einzigen Lager-Einlagerungsbeleg in der Liste aus und wählen Sie dann die Aktion **Bearbeiten**.  

    Der Einlagerungsbeleg wird geöffnet mit insgesamt acht Take- oder Place-Zeilen für die vier Einkaufsauftragszeilen.

    Der Arbeitskraft im Lager wird mitgeteilt, dass 40 Scharniere in der Montage benötigt werden, und sie teilt die einzelne Zeile „Platz“, um eine zweite Zeile „Platz“ für den Lagerplatz W-02-0001 in der Montage festzulegen, wo die Arbeitskraft im Lager diesen Teil der erhaltenen Scharniere platziert.  

3.  Wählen Sie die zweite Zeile auf der Seite **Lagereinlagerung** aus, die Einlagerungszeile für Artikel 70200.  
4.  Ändern Sie den Wert im Feld **Zu verarbeitende Menge** von 100 zu 60.  
5.  Wählen Sie auf dem Inforegister **Zeilen** die Option **Funktionen**, und klicken Sie dann auf **Zeile aufteilen**. Eine neue Zeile wird für Artikel 70200 mit 40 in Feld **Zu verarbeitende Menge** eingefügt.  
6.  Geben Sie im Feld **Lagerplatzcode** W-02-0001 ein. Das Feld **Gebietscode** wird automatisch ausgefüllt.  

    Standardmäßig ist das Feld **Zonencode** in den Verkaufszeilen ausgeblendet, sodass Sie es einblenden müssen. Dazu müssen Sie die Seite personalisieren. Weitere Informationen finden Sie unter [So starten Sie die Personalisierung einer Seite über das Personalisierungsbanner](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

    Fahren Sie fort mit dem Registrieren der Einlagerung.  

7.  Wählen Sie die Aktion **Beleg buchen** aus und wählen Sie dann die Schaltfläche **Ja** aus.  

    Das erhaltene Zubehör wird jetzt in den Standardlagerplätzen der Artikel eingelagert, und 40 Scharniere werden in die Montageabteilung gebracht. Die eingegangenen Artikel sind jetzt für die Kommissionierung zum internen Bedarf, wie etwa für Montageaufträge, oder zum externen Bedarf, wie etwa für Verkaufslieferungen, verfügbar.  

## <a name="see-also"></a><a name="see-also"></a>Siehe auch
 [Einlagern von Artikeln mit Lagereinlagerungen](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Umlagerung von Artikeln in erweiterten Lagerkonfigurationen](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Designdetails: Eingehender Lagerfluss](design-details-inbound-warehouse-flow.md)   
 <!-- [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)    -->
 [Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
