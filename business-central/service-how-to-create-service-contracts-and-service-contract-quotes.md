---
title: So arbeiten Sie mit Serviceverträgen und Servicevertragsangeboten | Microsoft Docs
description: Sie können einen Servicevertrag manuell erstellen oder aus einem Servicevertragsangebot. Si können einen Vertrag auf einem Servicevertragsangebot erstellen.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 0a9e90f19584e3586bac0cc80dac3b2cc0d9ce74
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134884"
---
# <a name="work-with-service-contracts-and-service-contract-quotes"></a>Arbeiten mit Serviceverträgen und Servicevertragsangeboten
Sie können einen Servicevertrag manuell erstellen oder aus einem Servicevertragsangebot. Sie können ein Servicevertragsangebot als Vorläufer eines Servicevertrags verwenden, in dem Ihr Unternehmen dem Debitoren ein Angebot unterbreitet und die Genehmigung des Debitoren erhält, bevor das Angebot in einen Servicevertrag umgewandelt wird. Die Vorgehensweisen zur Erstellung eines Servicevertrags oder eines Servicevertragsangebots sind ähnlich.  

## <a name="to-create-a-service-contract-or-service-contract-quote"></a>So erstellen Sie einen Servicevertrag oder ein Servicevertragsangebot  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Serviceverträge** oder **Servicevertragsangebote** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie einen neuen Servicevertrag oder ein neues Servicevertragsangebot.  
3. Füllen Sie die **Felder Nr.** Feld Es wird ein Dialogfeld geöffnet, in dem Sie gefragt werden, ob Sie die allgemeinen Daten aus einer Vertragsvorlage verwenden möchten. Wenn Sie einen solchen Servicevertrag oder ein solches Servicevertragsangebot erstellen möchten, klicken Sie auf **Ja**. Die Seite **Servicevertragsvorl.-Übersicht** wird angezeigt.  
4. Wählen Sie die entsprechende Vorlage aus, und wählen Sie dann **OK** aus, um den Servicevertrag oder das Servicevertragsangebot mithilfe der Vorlage zu erstellen.  
5. Klicken Sie im Feld **Debitorennr.** auf den Debitor.  
6. Wenn die Differenz der jährlichen Beträge nicht automatisch verteilt werden soll, wählen Sie das Kontrollkästchen **Nicht ausgegl. Betr. zulassen** aus. Die Werte in den Feldern **Zu fakturieren (Jahr)** und **Berech. zu fakturieren (Jahr)** werden nicht automatisch ausgeglichen. Wenn Sie aber möchten, dass Die Anwendung die Differenzen der jährlichen Beträge, die sich aus einer Änderung im Servicevertrag ergeben, automatisch ausgleicht, aktivieren Sie **Nicht ausgegl. Betr. zulassen** nicht.  
7. Vertragszeilen einem Servicevertrag oder Servicevertragsangebot hinzufügen.  
8. Füllen Sie die restlichen Felder aus, soweit dies erforderlich ist.  

## <a name="to-convert-a-service-contract-quote-to-service-contract"></a>So wandeln Sie Servicevertragsangebote in Serviceverträge um  
Wenn ein Debitor ein Servicevertragsangebot akzeptiert hat, wandeln Sie dieses in einen Servicevertrag um. Gleichzeitig können Sie eine Servicerechnung für die Startperiode des Vertrags erstellen, falls das Startdatum des Vertrags vor dem Beginn des nächsten Fakturierungsintervalls liegt.

Nachdem Sie die folgenden Schritte ausführen, wird ein Servicevertrag mit dem Status **Unterzeichnet** erstellt. Falls eine Servicerechnung für die Anfangsperiode des Vertrags erstellt wird, wird der fakturierte Betrag folgendermaßen, abhängig davon, ob es sich um einen detaillierten Vertrag handelt oder nicht, berechnet.  

Für detaillierte Verträge wird der fakturierte Betrag folgendermaßen berechnet:  

* Fakturierter Betrag = Summe der fakturierten Beträge der einzelnen Vertragszeilen.  
* Fakturierter Betrag für die einzelne Vertragszeile = ((Angebotswert ÷ 12) × Anzahl der Monate in der Anfangsperiode) + ((Angebotswert ÷ Anzahl Tage im Jahr) × Anzahl der verbleibenden Tage in der Anfangsperiode).  
* Falls die Vertragszeile vor dem Ende der Anfangsperiode abläuft, wird das Ablaufdatum zum Enddatum der Anfangsperiode der Zeile.  

Für Verträge, die nicht detailliert sind, wird der fakturierte Betrag folgendermaßen berechnet:  

* Fakturierter Betrag = (jährlicher Betrag ÷ Anzahl der Tage im Jahr) × Anzahl der Tage in der Anfangsperiode.  
* Falls der Vertrag abläuft, bevor die Anfangsperiode endet, wird das Ablaufdatum zum Enddatum der Anfangsperiode.    

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Servicevertragsangebote** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie das Servicevertragsangebot, das Sie in einen Servicevertrag umwandeln möchten.  
3. Wählen Sie die **Vertrag erst.** Aktion aus.  
4. Falls das Startdatum des Vertrags vor dem Beginn des nächsten Fakturierungsintervalls liegt, werden Sie gefragt, ob Sie eine Servicerechnung für die Startperiode des Vertrags erstellen möchten. Wählen Sie **Ja** aus.  

 Die Servicerechnung wird auf das Servicekonto des Vertrags gebucht, auch wenn der Vertrag vorausbezahlt ist.

## <a name="to-create-contract-service-credit-memos"></a>So erstellen Sie Servicevertragsgutschriften
Sie können Servicevertragsgutschriften verwenden, wenn ein Debitor einen vorausbezahlten Servicevertrag kündigt oder einen Serviceartikel aus einem vorausbezahlten Vertrag entfernt. Sie verwenden sie ebenfalls, um fehlerhafte Servicerechnungen zu korrigieren.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Servicegutschriften** ein und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine neue Servicegutschrift.  
3. Füllen Sie die **Felder Nr.** Feld  
4. Klicken Sie im Feld **Debitorennr.** geben Sie die Nummer des Debitors im Servicevertrag ein.  

     Sie können auf dem Inforegister **Fakturierung** weitere Informationen anzeigen, die aus der Karte **Debitor** kopiert wurden. Wenn Sie die Gutschrift auf einen anderen Debitor buchen möchten, als den auf dem Inforegister **Allgemein** angegebenen Debitor, müssen Sie die Nummer dieses Debitors in **Rech. an Deb.-Nr.** eingeben. Feld  

    > [!NOTE]  
    >  Sie können die Gutschrift mit dem ursprünglich gebuchten Beleg auf der Seite **Gebuchte Servicerechnungen** vergleichen. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Gebuchte Servicerechnungen** ein und wählen Sie dann den zugehörigen Link.  

5. Füllen Sie die Felder **Buchungsdatum** und **Belegdatum** aus.  
6. Geben Sie in die Gutschriftszeilen Informationen über die Artikel ein, die zurückgeschickt oder entfernt wurden, oder den Nachlass, den Sie gewähren möchten. Sie können auch das Anforderungsformular für die Stapelverarbeitung **Vorausbezahlte Vertragseinträge** verwenden.  

 Aktivieren Sie auf der Seite **Servicevertrag** auf dem Inforegister **Fakturierungsdetails** die Option **Autom. Gutschriften**, um automatisch eine Gutschrift zu erstellen, wenn Sie Vertragszeilen aus einem Servicevertrag löschen.  

 Um eine Gutschrift manuell zu erstellen, wenn Vertragszeilen aus einem Servicevertrag entfernt werden, wählen Sie auf der Seite **Servicevertrag** die Aktion **Gutschrift**.  

## <a name="updating-and-evaluating-contracts"></a>Aktualisieren und Auswerten von Verträgen
Gelegentlich müssen Sie die Bedingungen eines Vertrags nach dessen Erstellung ändern. In den meisten Fällen wird der betreffende Vertrag auf der Seite **Serviceverträge** geöffnet und nach Bedarf geändert.  

Sie können den Status des Vertrags, der ursprünglich auf **Gesperrt** festgelegt war, ändern, Vertragszeilen hinzufügen und entfernen und einen Vertrag kündigen. Einen Überblick über die Gewinn- und Verlustentwicklung im Unternehmen erhalten Sie durch eine schnelle Unternehmensanalyse, die mithilfe der Funktion "Servicevertrag-Trendscape" erstellt werden kann.

## <a name="to-add-a-contract-line-to-a-service-contract-or-contract-quote"></a>So fügen Sie einem Serviceauftrag oder einem Vertragsangebot Vertragszeilen hinzu  
Wenn ein Debitor einen neuen Artikel kauft und diesen in einem bestehenden Servicevertrag aufnehmen möchte, können Sie den Artikel als Serviceartikel erstellen lassen und ihn dann als neue Vertragszeile zu dem Vertrag oder dem Vertragsangebot hinzufügen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Serviceverträge** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den relevanten Servicevertrag oder das relevante Servicevertragsangebot, für den/das Sie eine neue Vertragszeile hinzufügen möchten.  
3. Wählen Sie die Aktionen **Vertrag öffnen** aus, um den Servicevertrag oder das Servicevertragsangebot zwecks Bearbeitung zu öffnen.  
4. Aktivieren Sie im Inforegister **Rechnungsdetails** das Feld **Nicht ausgegl. Betr. zulassen**, wenn Sie den jährlichen Betrag ändern und die Differenz des Feldes "Zu fakturieren (Jahr)" in den Vertragszeilen manuell weitergeben möchten. Andernfalls deaktivieren Sie das Feld **Nicht ausgegl. Betr. zulassen**. Dies verteilt die Differenz des Feldes "Zu fakturieren (Jahr)" automatisch auf die Vertragszeilen, wenn Sie den jährlichen Betrag geändert haben.  
5. Fügen Sie dem Inforegister **Zeilen** in jede Vertragszeile einen Serviceartikel, einen Artikel oder eine Textbeschreibung hinzu. Alternativ können Sie Vertragsangebotszeilen hinzufügen. Beachten Sie, dass Sie pro Serviceartikel mehrere Verträge erzeugen können, um ihn gleichzeitig bei verschiedenen Serviceverträgen oder Vertragsangeboten einzuschließen.  
6. Prüfen und – falls notwendig – korrigieren Sie die Zahlen in den Feldern **Zeilenrabatt %**, **Zeilenrabattbetrag**, **Reaktionszeit**, **Serviceintervall** und anderen Feldern.

## <a name="to-remove-contract-lines"></a>So entfernen Sie Vertragszeilen  
Möglicherweise müssen Sie Vertragszeilen aus dem Servicevertrag entfernen, wenn Sie entsprechende Serviceartikel aus dem Servicevertrag entfernen. In der Regel entfernen Sie Vertragszeilen, die abgelaufen sind oder zu einem eingestellten Serviceartikel gehören.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Serviceverträge** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den Servicevertrag, aus dem Sie Vertragszeilen entfernen möchten.  
3. Wählen Sie die Aktionen **Vertrag öffnen** aus, um den Servicevertrag zwecks Bearbeitung zu öffnen.  
4. Wählen Sie die Vertragszeile aus, die Sie entfernen möchten. Geben Sie in das Feld **Vertragsablaufdatum** das Datum ein, ab dem die Vertragszeile entfernt werden soll. Beispielsweise könnten Sie das Datum eingeben, an dem der Serviceartikel eingestellt wurde.  
5. Wählen Sie die **Vertragszeilen löschen** Aktion aus. Die Seite **Vertragszeilen löschen** wird geöffnet.  
6. Füllen Sie die Standardfilter aus: **Vertragsnr.**, **Serviceartikelnr.** und **Vertragsart**. Bei Bedarf können Sie weitere Filter anwenden oder die bestehenden ändern.  
7. Füllen Sie die Felder auf der **Optionen** Inforegister aus, und wählen Sie dann die Aktion **Linien löschen**.  

> [!NOTE]  
>  Wenn es sich nicht um einen detaillierten Vertrag handelt, müssen Sie den Wert im Feld **Zu fakturieren (Jahr)** auf dem Inforegister **Fakturierungsdetails** auf der Seite **Servicevertrag** aktualisieren, damit das Entfernen des Serviceartikels aus dem Vertrag berücksichtigt wird.  
>   
>  Wenn es sich um einen detaillierten und vorausbezahlten Vertrag handelt und Sie Rechnungen für den Vertrag gebucht haben, können Sie eine Gutschrift für den Vertrag erstellen. Wählen Sie die Aktion **Gutschrift erstellen**. Dies ist unnötig, wenn das Kontrollkästchen im Feld **Autom. Gutschriften** im Inforegister **Rechnungsdetails** aktiviert ist. In diesem Fall wird automatisch eine Gutschrift erstellt wird, wenn Sie eine Vertragszeile entfernen.

## <a name="service-line-cost-and-value"></a>Servicezeile "Kosten und Wert"
In Servicevertragszeilen werden die Beträge in den Feldern **Zeileneinstandspreis** und **Zeilenwert** berechnet, wie in den folgenden Tabellen beschrieben.

| Zeileneinstandsbetrag-Optionen | Description|
|----------------------------------|---------------------------------------|  
|**Serviceartikel** | Der Einstandspreis wird automatisch aus dem Feld **Vorgabe Einst.-Betrag (Vert.)** der Tabelle **Serviceartikel** in das Feld **Zeileneinstandspreis** kopiert. Mit der folgenden Formel wird der Zeileneinstandspreis berechnet:<br /><br /> Einstandspreis × Vertragswert % ÷ 100|  
|**Artikel** | Der Einstandspreis wird automatisch aus dem Feld **Einstandspreis** der Tabelle **Artikel** und dem Wert aus dem Feld **Vertragswert %** der Tabelle **Service Einrichtung** ermittelt. Mit der folgenden Formel wird der Zeileneinstandspreis berechnet:<br /><br /> Einstandspreis × Vertragswert % ÷ 100|  
|**Textbeschreibung** | Der Wert des Felds **Zeileneinstandspreis** wird auf Null gesetzt.|  

| Zeilenwert-Optionen | Description|
|----------------------------------|---------------------------------------|  
|**Serviceartikel** | Der Preis wird automatisch aus dem Feld **Vorgabevertragswert** der Tabelle **Serviceartikel** in das Feld **Zeilenwert** kopiert.|  
|**Artikel** | Abhängig vom Wert im Feld **Vertragswertberechnungsmethode** in der Tabelle **Service Einrichtung** wird der Betrag entweder aus dem Feld **VK-Preis** oder **Einstandspreis** der Tabelle **Artikel"** übernommen. Danach wird der Wert mit dem Inhalt des Felds **Vertragswert %** in der Tabelle **Service Einrichtung** multipliziert und durch 100 dividiert. Dieser Betrag wird in das Feld Zeilenwert kopiert. Dieser Betrag wird in das Feld **Zeilenwert** kopiert.<br /><br /> **HINWEIS:** Wenn das Feld **Vertragswertberechnungsmethode** auf **Keine** gesetzt ist, dann wird der Inhalt des Felds **Zeilenwert** nicht berechnet.|  
|**Textbeschreibung** | Der Inhalt des Felds **Zeilenwert** wird auf Null gesetzt.|  

## <a name="to-add-a-contract-discount-to-service-contract-quotes"></a>So fügen Sie einen Vertragsrabatt für Servicevertragsangebote hinzu  
Sie können Vertragsrabatte für Services auf Vertragsangeboten und Serviceverträgen hinzufügen. Die Rabatte können auf Ersatzteile in bestimmten Serviceartikelgruppen, auf Arbeitsstunden von Ressourcen in bestimmten Ressourcengruppen und auf bestimmte Servicekosten gewährt werden.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Servicevertragsangebote** ein und wählen Sie den zugehörigen Link.  
2. Wählen Sie das Angebot aus, dem Rabatte hinzuzufügt werden sollen.  
3. Wählen Sie die **Servicerabatte** Aktion aus. Die Seite **Vertrags-/Servicerabatte** wird geöffnet.  
4. Wählen Sie die **Neu** Aktion aus, um einen neuen Rabattvertrag zu erstellen.  
5. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  

> [!Tip]  
>  Um Vertragsrabatte direkt zu einem Servicevertrag hinzuzufügen, führen Sie ähnliche Schritte auf der Seite **Servicevertrag** aus.  

## <a name="to-change-the-owner-of-a-service-contract"></a>So ändern Sie den Inhaber eines Servicevertrags  
Sie müssen möglicherweise den Inhaber eines Servicevertrags ändern. Wenn ein Serviceartikel in einem Servicevertrag in mehreren Verträgen, die nicht gekündigt sind und deren Inhaber derselbe Debitor ist, erfasst ist, wird der Inhaber aller Serviceverträge, die diesen Serviceartikel beinhalten, und alle Serviceartikel, die in diesen Verträgen enthalten sind, automatisch aktualisiert.  

> [!NOTE]  
>  In diesem Fall werden nur ungekündigte Verträge berücksichtigt. Der Status der Vertragsangebote wird nicht berücksichtigt.  

> [!IMPORTANT]  
>  Viele Serviceartikel und Verträge können miteinander verknüpft werden. Das Ändern des Besitzers eines Servicevertrags kann diese Beziehungen beeinflussen.  
>   
>  Zum Beispiel erscheint Serviceartikel Nr. 8 in den Verträgen SV00003 und SV00015. Vertrag SV00015 enthält darüber hinaus Serviceartikel Nr. 15, der ebenso in Vertrag SV00080 erscheint. In diesem Fall werden die Inhaber aller drei Verträge und Serviceartikel geändert.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Serviceverträge** ein und wählen Sie dann den zugehörigen Link. Öffnen Sie den Servicevertrag, dessen Besitzer Sie ändern möchten.  
2. Wählen Sie die Aktionen **Vertrag öffnen** aus, um den Vertrag zwecks Bearbeitung zu öffnen.  
3. Wählen Sie die **Debitor wechseln** Aktion aus. Die Seite **Debitor in Vertrag ändern** wird geöffnet.  
4. Im **Vertragsnummer** und **Serviceartikelnr**, sehen Sie die Nummern des Vertrags und des Serviceartikels des ausgewählten Debitors. Wenn der Debitor Inhaber mehrerer Verträge mit mehreren Serviceartikeln ist, ist der Wert dieser Felder **Mehrere**. Um die Liste der damit verbundenen Verträge oder Serviceartikel anzuzeigen, wählen Sie diese Feldwerte aus.  
5. Klicken Sie im Feld **Neue Debitorennr.** auf den neuen Debitor.  
6. Wählen Sie im Feld **Neuer Lief. an Code** die Adresse aus.  
7. Wählen Sie die Schaltfläche **OK**, um den Kunden- und Liefercode der Serviceverträge zu ändern.  
8. Wählen Sie auf Aktion **Vertrag sperren** aus, um den Vertrag zu sperren und sicherzustellen, dass die Änderungen in die Verträge übernommen werden.  

## <a name="to-update-a-service-contract-price"></a>So aktualisieren Sie Servicevertragspreise  
Sie können die Preise in Serviceverträgen durch die Eingabe eines Prozentsatzes aktualisieren.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Servicevertragspreise aktualisieren** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Servicevertrag aus.  
3. Geben Sie in dem Feld **Aktualisierung bis Datum** ein Datum ein. Mit dem Batchauftrag werden die Preise für Verträge mit einem nächsten Preisaktualisierungsdatum bis einschließlich zu diesem Datum aktualisiert.  
4. Geben Sie im Feld **Preisaktualisierung %** den Prozentsatz ein, mit dem Sie die Vertragspreise aktualisieren möchten.  
5. Wählen Sie im Feld **Aktion** die Option **Vertragspreise aktualisieren**.  

## <a name="to-post-prepaid-contract-entries"></a>So buchen Sie vorausbezahlte Vertragsposten  
Wenn Sie mit vorausbezahlten Verträgen arbeiten, müssen Sie regelmäßig vorausbezahlte Vertragsposten buchen und dabei die Vorauszahlungen von den Vorauszahlungskonten auf die regulären Konten übertragen.  

Bevor Sie die vorausbezahlten Vertragsposten buchen können, müssen Sie auf der Seite **Service Einrichtung** im Feld **Vorausbez. Buch.-Belegnummern** eine Nummernserie angeben.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Vorbezahlte Vertragsposten buchen** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie im Feld **Buchungsdatum** ein Buchungsdatum ein. Die Stapelverarbeitung bucht vorausbezahlte Serviceposten mit einem Buchungsdatum bis zu diesem Datum.  
4. Geben Sie im Feld **Buchungsdatum** das Datum ein, das Sie als Buchungsdatum in der Fibu Buch.-Blattzeile verwenden möchten.  
5. Klicken Sie im Feld **Aktion** auf **Vorausbezahlte Transaktionen buchen**.  
6. Klicken Sie auf **OK**, um die Posten zu buchen.

## <a name="changing-the-service-contract-status"></a>Ändern des Servicevertrag-Status
Nachdem der Servicevertrag unterschrieben wurde, wird der Wert des Felds **Status ändern** automatisch auf **Gesperrt** festgelegt. Wenn Sie Daten im Servicevertrag oder im Serviceangebot ändern möchten, müssen Sie zuerst den Status für Änderungen von **Gesperrt** in **Offen** ändern. Beachten Sie, dass es nicht möglich ist, Servicerechnungen für Serviceverträge zu erstellen, wenn der Status für Änderungen auf **Offen** steht. Nachdem der Vertrag oder das Vertragsangebot geändert wurde, müssen Sie den Status für Änderungen zurück auf **Gesperrt** setzen, damit es möglich ist, Servicerechnungen und Posten für den Servicevertrag zu erzeugen.  

> [!NOTE]  
>  Das Feld **Status ändern** ist nicht mit dem Feld **Release-Status** des Serviceauftragskopfs verbunden, der den Lagerdurchlauf von Serviceartikeln steuert.  

## <a name="to-cancel-a-service-contract"></a>So kündigen Sie einen Servicevertrag  
Sie müssen u. U. einen Servicevertrag kündigen, wenn dieser Vertrag ausläuft oder von Ihrer oder Debitorenseite gekündigt wird.  

> [!NOTE]  
>  Sie können einen Vertrag nicht erneut öffnen, wenn er gekündigt ist.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Serviceverträge** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den relevanten zu kündigenden Servicevertrag.  
3. Wählen Sie die Aktionen **Vertrag öffnen** aus, um den Servicevertrag zwecks Bearbeitung zu öffnen.  
4. Wählen Sie im Feld **Ursachencode bei Kündigung** den relevanten Ursachencode aus. Um weitere Ursachencodes hinzuzufügen, wählen Sie die **Erweitert** Aktion aus.  

     Wenn das Kontrollkästchen im Feld **Urs.-Code b. Vertr.-Kündigung** auf der Seite **Service Einrichtung** aktiviert ist, müssen Sie beim Kündigen von Verträgen einen Ursachencode angeben.  

5. Wählen Sie im Feld **Status** **Gekündigt** aus.  
6. Wenn ungebuchte Rechnungen, Gutschriften oder geöffnete vorausbezahlte Posten für den Vertrag vorliegen, wird eine Bestätigungsmeldung angezeigt. Klicken Sie im Meldungsfenster auf **Nein**, um zum Vertrag zurückzukehren und die Belege zu buchen, oder auf **Ja**, um mit dem Vertragskündigungsprozess fortzufahren.  

## <a name="filing-a-service-contract-or-contract-quote"></a>Archivieren eines Servicevertrags oder Vertragsangebots  
Sie können Serviceverträge und Vertragsangebote jederzeit archivieren, um eine Kopie des Vertrags oder des Angebots zu erfassen. [!INCLUDE[prod_short](includes/prod_short.md)] Servicevertrag wird automatisch archiviert, wenn Sie ein Vertragsangebot in einen Servicevertrag umwandeln oder einen Servicevertrag kündigen. Sie können selbst einen Vertrag oder Angebot archivieren, indem Sie die **Vertrag archivieren** Aktion auf den Seiten **Serviceverträge** oder **Servicevertragsangebote** auswählen. Wenn Sie Ihre archivierten Verträge der Angebote sehen möchten, indem Sie nach **Archivierte Verträge** suchen.

## <a name="see-also"></a>Siehe auch  
[Serviceverträge einzurichten:](service-how-setup-service-contracts.md)  
[Service](service-service.md)  
[Konvertieren von Serviceverträgen, die MwSt.-Beträge enthalten](service-how-to-convert-service-contracts.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]