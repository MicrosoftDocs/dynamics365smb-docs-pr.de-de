---
title: So erstellen Sie Serviceaufträge
description: 'Lernen Sie die verschiedenen Aufgaben kennen, die mit dem Erstellen von Serviceaufträgen in Business Central verbunden sind, z.B. das Erstellen eines neuen Serviceauftrags oder von Aufträgen auf der Basis eines Servicevertrags.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---
# <a name="create-service-orders"></a>Erstellen von Serviceaufträgen
Sie können die Seite **Serviceauftrag** verwenden, um Belege zu erstellen, in die Sie Informationen über den Service (Reparatur und Wartung) von Serviceartikeln auf Debitorenanfrage eingeben.  

Wenn Sie einen Serviceauftrag erstellen, müssen Sie nur einige wenige Felder ausfüllen. Einige Felder sind optional und viele werden automatisch ausgefüllt, wenn Sie die damit verknüpften Felder ausfüllen.  

## <a name="to-create-a-service-order"></a>So erstellen Sie einen Serviceauftrag
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Serviceaufträge** ein und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie einen neuen Serviceauftrag.  
3. Geben Sie im Feld **Nr.** eine Nummer für den Serviceauftrag ein.  

     Wenn Sie alternativ auf der Seite **Serviceverwaltungseinrichtung** Nummernserien für Serviceaufträge definiert haben, wählen Sie <kbd>EINGABETASTE</kbd>, um die nächste verfügbare Serviceauftragsnummer auszuwählen.  

4. Klicken Sie im Feld **Debitorennr.** Feld wählen Sie den relevanten Debitoren aus der Liste. Die für den Debitor relevanten Felder werden mit den Informationen aus der Tabelle **Debitor** ausgefüllt.  

5. Abhängig von den Einstellungen im Inforegister **Pflichtfelder** auf der Seite **Serviceverwaltungseinrichtung** muss das Feld **Serviceauftragsart** im Feld **Verkäufercode** ausgefüllt werden.  
6. Optional können Sie die restlichen Felder ausfüllen.  
7. Erfassen Sie die Serviceartikelzeilen.  

## <a name="to-create-a-service-order-from-a-contract"></a>So erstellen Sie Serviceaufträge aus Verträgen
Serviceaufträge können für die Wartung von Serviceartikeln aus Verträgen angelegt werden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Aufträge für Verträge erst erstellen** ein, und wählen Sie dann den zugehörigen Link.  
2. Geben Sie auf dem Inforegister **Servicevertragskopf** die gewünschten Filter ein.  
3. Füllen Sie auf dem Inforegister **Optionen** die Felder **Startdatum** und **Enddatum** mit dem Startdatum und dem Enddatum der Periode aus, für die Sie Serviceaufträge erstellen möchten. Die Stapelverarbeitung erzeugt Serviceaufträge mit Serviceartikeln aus Serviceverträgen mit einem Datum des Typs "Nächster geplanter Service am" innerhalb dieser Periode.  

    > [!NOTE]  
    >  Die Anzahl der Tage, die Sie als Zeitraum für diese Stapelverarbeitung verwenden können, ist eingeschränkt. Sie legen diese Begrenzung im Feld **Serviceaufträge max. Tage** auf der Seite **Serviceverwaltungseinrichtung** fest.  

4. Wählen Sie im Feld **Aktion** den Eintrag **Serviceauftrag erstellen** aus.  
    > [!NOTE]  
    >  Sie können keinen Auftrag mit mehreren Serviceartikeln erstellen, wenn Sie das Feld **Ein Serviceartikel pro Auftrag** auf der Seite **Serviceverwaltungseinrichtung** festlegen. 

## <a name="to-convert-a-service-quote-to-a-service-order"></a>So konvertieren Sie ein Serviceangebot in einen Serviceauftrag
Wenn ein Debitor ein Angebot akzeptiert hat, wandeln Sie dieses in einen Serviceauftrag um. Das Angebot wird gelöscht, und es wird ein neuer Serviceauftrag mit derselben Beschreibung wie im Angebot eingerichtet. Die Felder "Reagieren bis (Datum)" und "Reagieren bis (Zeit)" werden erneut berechnet, und der Status des Serviceauftrags wird auf **Offen** festgelegt. Der Reparaturstatus der Serviceartikel in dem Auftrag wird auf **Anfang** geändert.  

[!INCLUDE[prod_short](includes/prod_short.md)] sucht nach Zuordnungen für alle Serviceartikel des Serviceangebots mit dem Status **Aktiv**. Falls solche Zuordnungsposten gefunden werden, wird der Zuordnungsstatus auf **Neuzuordnung notwendig** aktualisiert. Wenn Sie die Serviceartikel in dem Serviceauftrag neu zuordnen, wird der Status der Zuordnungsposten, die für das Angebot erfasst wurden, auf **Erledigt** aktualisiert.   

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Servicevertragsangebote** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das Serviceangebot aus, das Sie in einen Serviceauftrag umwandeln möchten.  
3. Wählen Sie die **Auftrag erstellen** Aktion aus.  

## <a name="to-check-item-availability-for-one-or-more-orders"></a>So überprüfen Sie die Artikelverfügbarkeit für mindestens einen Auftrag
Sie können überprüfen, ob ein Artikel, den Sie für einen Auftrag benötigen, auf Lager ist, und wenn nicht, wann der Artikel auf Lager sein wird. Außerdem können Sie, wenn ein Artikel reservierbar ist, ihn reservieren, um sicherzustellen, dass er für Ihre Verwendung verfügbar ist. Sie können die Verfügbarkeit für einen bestimmten Auftrag oder für alle Aufträge überprüfen.  

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einsatzplanung** ein und wählen Sie den zugehörigen Link.  
2. Führen Sie einen der folgenden Schritte aus:  

    * Für einen bestimmten Auftrag wählen Sie den Auftrag und dann die **Bedarfsübersicht** Aktion aus.  
    * Für alle Aufträge wählen Sie **Beleg anzeigen** aus. Die Seite **Serviceauftrag** wird geöffnet.  

3. Erweitern Sie auf der Seite **Bedarfsübersicht** die Artikelgruppierung, und zeigen Sie Informationen über die Verfügbarkeit des Artikels an. Beispielsweise wird angezeigt, wie viele Artikel sich im Lager befinden. Sie können auch feststellen, ob und wann ein Artikel verfügbar ist, ob er sich in Rückstand befindet (das heißt, ob die Herkunftsart = Einkauf ist) oder ob er reserviert wurde.

## <a name="to-reserve-an-item-for-a-service-order"></a>So reservieren Sie einen Artikel für einen Serviceauftrag:
Wenn Sie sicher sein müssen, dass ein Artikel für einen Serviceauftrag verfügbar ist, können Sie den Artikel reservieren.

1. Geben Sie im Feld **Suchen** **Serviceaufträge** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie das Menü Bestellung, und wählen Sie dann **Bearbeiten**.  
3. Wählen Sie **Aktionen** , **Auftrag**, und klicken Sie anschließend auf **Servicezeilen**.  
4. Auf der Seite **Servicezeilen** wählen Sie den zu reservierenden Artikel und die **Reservieren** Aktion aus.  
5. Auf der Seite **Reservierung** wählen Sie **Von aktueller Zeile reservieren** aus.

## <a name="to-insert-lines-based-on-standard-service-codes"></a>So fügen Sie Zeilen basierend auf Standardservicecodes ein
Wenn Sie Standardservicecodes eingerichtet und Serviceartikelgruppen zugewiesen haben, können Sie die mit den Standardservicecodes verknüpften Standardzeilen in Servicebelege einfügen. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Standardservicecodes](service-how-setup-service-coding.md)   

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Serviceaufträge** ein und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie einen neuen Serviceauftrag.  
3. Füllen Sie die Felder je nach Bedarf aus.  
4. Geben Sie in die Serviceartikelzeilen die erforderlichen Informationen ein.  
5. Wählen Sie die Zeile mit dem Serviceartikel, für den Sie Servicezeilen erstellen möchten, und wählen Sie dann **Std.-Servicecodes abrufen** aus. Die Seite **Std.-Serviceartikelgr.-Codes** mit den Standardcodes für die Serviceartikelgruppe, die der Zeile entspricht, wird geöffnet.  
6. Wählen Sie den entsprechenden Code aus, und klicken Sie auf **OK**, um Standardservicezeilen einzugeben.  

> [!NOTE]  
>  Wenn das Feld **Serviceartikelgruppencode** in der Serviceartikelzeile des Belegs leer ist, weist dies darauf hin, dass der Serviceartikel nicht zu einer Serviceartikelgruppe gehört. In diesem Fall enthält die Seite **Std.-Serviceartikelgr.-Codes** eine Liste aller Standardservicecodes. Sie sollten einen Code aus der Liste auswählen, um Standardservicezeilen in den Beleg einzufügen. Sie können auch aus einer Liste von Standardservicecodes wählen, die einer bestimmten Serviceartikelgruppe zugeordnet sind. Um die Liste anzuzeigen, wählen Sie den entsprechenden Code im Feld **Serviceartikelgruppencode** auf der Seite **Standard-Serviceartikelgruppen-Codes** aus.  

## <a name="to-register-internal-or-public-comments"></a>So erfassen Sie interne oder öffentliche Bemerkungen
Sie können Bemerkungen hinzufügen, die auf Serviceaufträgen und Serviceangeboten gedruckt werden, um zusätzliche Informationen bereitzustellen. Sie können bis zu 80 Zeichen, einschließlich Leerzeichen, hinzufügen. Wenn Sie mehr Text eingeben müssen, wählen Sie eine andere Zeile aus. Um eine Bemerkung zu registrieren, wählen Sie eine Zeile und die **Bemerkungen** Aktion aus.  

## <a name="to-delete-invoiced-service-orders"></a>So löschen Sie fakturierte Serviceaufträge
Aufträge werden automatisch gelöscht, nachdem diese vollständig fakturiert wurden. Beim Buchen einer Rechnung wird ein entsprechender Posten auf der Seite **Gebuchte Servicerechnungen** erstellt. Der gebuchte Beleg kann auf der Seite **Gebuchte Servicerechnung** angezeigt werden.  

Serviceaufträge werden aber nicht automatisch gelöscht, wenn die Gesamtmenge des Auftrags nicht aus dem eigentlichen Serviceauftrag, sondern von der Seite **Servicerechnung** gebucht wurde. In diesem Fall müssen Sie fakturierte Aufträge, die nicht gelöscht wurden, manuell löschen. Dazu führen Sie die Stapelverarbeitung **Fakturierte Serviceaufträge löschen** aus.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Fakturierte Serviceaufträge löschen** ein und wählen Sie dann den zugehörigen Link. Das Anforderungsfenster des Batchauftragsseite **Servicebelegprotok. löschen** wird geöffnet.  
2. Um die zu löschenden Aufträge auszuwählen, können Sie Filter in den Feldern **Nr.**, **Debitorennr.** und **Rech. an Deb.-Nr.** festlegen. Felder.  
3. Wählen Sie **OK** aus.  


## <a name="see-also"></a>Siehe auch
[Servicebuchung](service-service-posting.md)  
[Serviceauftrag buchen](service-how-to-post-service-orders.md)  
[Einrichten der Serviceverwaltung](service-setup-service.md)  
[Mit Serviceaufgaben arbeiten](service-how-to-work-on-service-tasks.md)  
[Ressourcen zuordnen](service-how-to-allocate-resources.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
