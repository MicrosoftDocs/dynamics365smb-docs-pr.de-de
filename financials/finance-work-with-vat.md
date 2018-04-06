---
title: Mit MwSt im Verkauf und Einkauf arbeiten  | Microsoft Doc
description: "Dieses Thema beschreibt, wie Aufgaben wie Korrektur von gebuchter MwSt in EU-Ländern/Regionen, jedes Verkaufs- und Einkaufstransaktionen von der MwSt-Berechnungen abhängt. Dieses Thema beschreibt wie."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, sales, purchases,
ms.date: 09/08/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 31b28811529cb4e5296a04c18f1f41d9f452a9be
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-vat-on-sales-and-purchases"></a>Arbeiten mit MwSt im Verkauf und Einkauf
Wenn Ihr Land oder Ihre Region es erfordert, die Mehrwertsteuer (MwSt) in Einkaufs- und Verkaufstransaktionen zu berechnen, sodass Sie die Beträge einer Steuerbehörden melden können, können Sie festlegen, dass [!INCLUDE[d365fin](includes/d365fin_md.md)]MwSt in Einkaufs- und Verkaufsbelegen automatisch berechnet wird. Weitere Informationen finden Sie [Einrichten der Berechnungs- und Buchungsmethoden für Mehrwertsteuer] (finance-setup-vat.md).

Es gibt jedoch Mehrwertsteuer-verknüpfte Aufgaben, die Sie manuell tun können. Beispielsweise müssen Sie möglicherweise einen gebuchten Betrag korrigieren, wenn Sie feststellen, dass ein Kreditor eine andere Rundungsmethode verwendet.

## <a name="calculating-and-displaying-vat-amounts-in-sales-and-purchase-documents"></a>Berechnen und Anzeigen von MwSt.-Beträgen in Verkaufs- und Einkaufsbelegen  
Je nach Debitoren- oder Kreditorenart können MwSt.-Beträge in Verkaufs- und Einkaufsbelegen unterschiedlich berechnet und angezeigt werden. Darüber hinaus kann der von der Anwendung berechnete MwSt.-Betrag außer Kraft gesetzt werden und der von Ihrem Kreditor für ein bestimmtes Geschäft berechnete MwSt.-Betrag verwendet werden.  

### <a name="unit-price-and-line-amount-includingexcluding-vat-on-sales-documents"></a>Verkaufspreis und Zeilenbetrag inklusive/exklusive MwSt. auf Verkaufsdokumenten  
Wenn Sie eine  Artikelnummer im **Nr.** Feld in einem Verkaufsbeleg auswählen, wird [!INCLUDE[d365fin](includes/d365fin_md.md)] von der Anwendung auch das Feld **Einheitspreis** ausgefüllt. Der Verkaufspreis wird von der **Artikel**karte übernommen oder anhand der Artikelpreise berechnet, die für den Artikel und den Debitor zulässig sind. [!INCLUDE[d365fin](includes/d365fin_md.md)]berechnet den **Zeilenbetrag** nur dann, wenn Sie eine Menge für die Zeile eingeben.  

Wenn Sie an einen Einzelhandelskunden verkaufen, möchten Sie möglicherweise, dass die Preise in Verkaufsbelegen die Mehrwertsteuer enthalten. Um dies zu tun, aktivieren Sie das Kontrollkästchen **Preise inkl. MwSt.** im Beleg.  

### <a name="including-or-excluding-vat-on-prices"></a>Mit oder ohne Mehrwertsteuer auf Preise
Ist das Feld  **Preise inkl. MwSt.** aktiviert, werden die Felder  **VK-Preis** und  **Zeilenbetrag** mit der MwSt. berechnet und der Feldname zeigt dies ebenfalls. Standardmäßig ist die MwSt nicht in diesen Feldern enthalten.  

Ist das Feld nicht aktiviert, wird in die Felder **VK-Preis** und **Zeilenbetrag** ein Betrag ohne MwSt. eingegeben. Dies wird auch durch die Feldnamen wiedergegeben.  

Sie können die Standardeinstellung der **Preise inkl. MwSt.** für alle Verkaufsbelege eines Debitors im Feld **Preise inkl. MwSt.** auf der **Debitor**-Karte einrichten. Darüber hinaus können Sie auch Artikelpreise inklusive oder exklusive MwSt. einrichten. Normalerweise ist auf der Artikelkarte der Artikelpreis ohne MwSt. angegeben. Die Daten im Feld **VK-Preis inkl. MwSt.** auf der **Artikelkarte** dienen zur Ermittlung des Verkaufspreises für Verkaufsbelege.  

Die folgende Tabelle bietet einen Überblick darüber, wie in der Anwendung Verkaufspreise für einen Verkaufsbeleg berechnet werden, wenn im Fenster **VK-Preise** keine Preise eingerichtet sind:  

|**Feld "VK-Preis inkl. MwSt." auf Artikelkarte**|**Feld "Preise inkl. MwSt." im Verkaufskopf**|**Durchgeführte Aktion**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Kein Häkchen|Kein Häkchen|Der **VK-Preis** auf der Artikelkarte wird in das Feld **VK-Preis ohne MwSt.** in den Verkaufszeilen kopiert.|  
|Kein Häkchen|Häkchen|Der MwSt.-Betrag pro Einheit wird berechnet und zu dem **VK-Preis** auf der Artikelkarte hinzugefügt. Dieser Gesamtverkaufspreis wird dann in das Feld **VK-Preis inkl. MwSt.** in den Verkaufszeilen eingegeben.|  
|Häkchen|Kein Häkchen|Die Anwendung berechnet die MwSt.-Betrag, der in **VK-Preis** auf der Artikelkarte unter Verwendung des MwSt.-Prozentsatzes enthalten ist, der mit der Kombination aus MwSt.-Geschäftsbuchungsgruppe (Preis) und MwSt.-Produktbuchungsgruppe verknüpft ist. Der **VK-Preis** auf der Artikelkarte, verringert um den MwSt.-Betrag, wird dann im Feld **VK-Preis ohne MwSt.** in den Verkaufszeilen eingegeben.|  
|Häkchen|Häkchen|Der **VK-Preis** auf der Artikelkarte wird in das Feld **VK-Preis inkl. MwSt.** in den Verkaufszeilen kopiert.|

## <a name="correcting-vat-amounts-manually-in-sales-and-purchase-documents"></a>MwSt.-Beträgen in Verkaufs- und Einkaufsbelegen manuell korrigieren  
An  gebuchten MwSt.-Posten können Korrekturen durchgeführt werden. Auf diese Weise können Sie die MwST-Beträge sämtlicher Einkäufe oder Verkäufe ändern, ohne die MwSt-Bemessungsgrundlage zu verändern. Sie werden dies beispielsweise tun wollen, wenn Sie eine Rechnung von einem Kreditor bekommen, der die MwSt. nicht korrekt berechnet hat.  

Auch wenn Sie möglicherweise bereits eine oder mehrere Kombinationen für die Verarbeitung der Einfuhrumsatzsteuer eingerichtet haben, müssen Sie mindestens einen MwSt.-Produktbuchungsgruppencode einrichten. Beispielsweise können Sie den Namen **RICHTIG** für Korrekturen angeben, es sei denn, Sie können dasselbe Sachkonto im Feld **Vorsteuerkonto** in der MwSt.-Buchungsmatrixzeile verwenden. Weitere Informationen finden Sie [Einrichten der Berechnungs- und Buchungsmethoden für Mehrwertsteuer](finance-setup-vat.md).

Wenn Skonto auf der Basis einer Rechnung inklusive MwSt. berechnet wurde, haben Sie die Möglichkeit, den Skontoanteil des MwSt.-Betrages zu berichtigen, wenn Skonto gewährt wird. Beachten Sie, dass Sie das Feld **Skonto berichtigen** sowohl in der Finanzbuchhaltungs-Einrichtung: allgemein als auch in der MwSt.-Buchungsmatrix Einrichtung für bestimmte Kombinationen von MwSt.-Geschäftsbuchungsgruppe und MwSt.-Produktbuchungsgruppe aktivieren müssen.  

#### <a name="to-manually-enter-vat-in-sales-documents"></a>So geben Sie die MwSt. in Verkaufsbelegen manuell ein  
1. Geben Sie im Fenster  **Finanzbuchhaltungs-Einrichtung:** eine  **maximal zulässige MwSt.-Differenz** zwischen dem von der Anwendung berechneten Betrag und dem manuell eingegebenen Betrag an.  
2. Versehen Sie im Fenster **Debitoren & Verkauf Einr.** das Feld **MwSt.-Differenz zulassen** mit einem Häkchen.  

#### <a name="to-adjust-vat-for-a-sales-document"></a>Die MwSt. für einen Verkaufsbeleg anpassen:  
1. Öffnen Sie den entsprechenden Verkaufsauftrag.  
2. Wählen Sie die Aktion **Statistik** aus.  
3. Klicken Sie auf das Inforegister **Fakturierung**.  
  
    > [!NOTE]  
    >  Der gesamte MwSt.-Betrag für die Rechnung wird gruppiert nach MwSt.-Kennzeichen in den Zeilen angezeigt. Sie können den Betrag manuell im Feld **MwSt.-Betrag** in den Zeilen für jedes MwSt.-Kennzeichen anpassen. Wenn Sie das Feld **MwSt.-Betrag** ändern, prüft die Anwendung, ob die Mehrwertsteuer um einen höheren Betrag als die maximal zulässige Differenz geändert wurde. Liegt der Betrag außerhalb des unter **Max. MwSt.-Differenz zulässig** angegebenen Bereichs, werden Sie in einer Warnmeldung über die maximal zulässige Differenz informiert. Sie können erst dann fortfahren, wenn der Betrag an die zulässigen Parameter angeglichen wurde. Klicken Sie auf **OK** , und geben Sie einen anderen **MwSt.-Betrag** ein, der innerhalb des zulässigen Bereichs liegt. Wenn die MwSt.-Differenz der zulässigen Abweichung entspricht oder höher ist, wird die MwSt. proportional auf die Belegzeilen mit demselben MwSt.-Kennzeichen aufgeteilt.  

## <a name="calculating-vat-manually-using-journals"></a>MwSt.-Berechnung mithilfe von Buch.-Blättern manuell berechnen  
Sie können MwSt.-Beträge auch in den Buch.-Blättern Allgemein, Verkauf und Einkauf anpassen. Dies ist unter Umständen dann erforderlich, wenn Sie eine Kreditorenrechnung in das Buch.-Blatt eingeben und zwischen der von der [!INCLUDE[d365fin](includes/d365fin_md.md)] Anwendung berechneten MwSt. und dem MwSt.-Betrag auf der erhaltenen Kreditorenrechnung eine Differenz besteht.  

#### <a name="before-you-manually-enter-vat-on-a-general-journal"></a>Bevor Sie MwSt.-Beträge manuell in einem Fibu-Buch.-Blatt eingeben  
1. Geben Sie im Fenster  **Finanzbuchhaltungs-Einrichtung:** eine  **maximal zulässige MwSt.-Differenz** zwischen dem von der Anwendung berechneten Betrag und dem manuell eingegebenen Betrag an.  
2. Wählen Sie auf der Seite  **Allgemeine Buch.-Blatt Vorlage** das Kontrollkästchen **MwSt-Differenz zulassen** mit einem Häkchen.  

#### <a name="before-you-manually-enter-vat-on-sales-and-purchase-journals"></a>Bevor Sie MwSt.-Beträge manuell in Verkaufs- und Einkaufs-Buch.-Blättern eingeben  
1. Auf der Seite **Kreditoren & Einkauf Einr.** wählen Sie das Kontrollkästchen **MwSt.-Differenz zulassen**.  
2. Nachdem Sie die oben beschriebene Einrichtung durchgeführt haben, können Sie den Betrag im Feld **MwSt.-Betrag** in der Fibu-Buch.-Blattzeile oder das Feld **Gegenkonto MwSt.-Betrag** in der Verkaufs- oder Einkaufs-Buch.-Blattzeile an den MwSt.-Betrag der Rechnung anpassen. [!INCLUDE[d365fin](includes/d365fin_md.md)]Die Anwendung prüft, ob die Differenz die festgelegte maximale Differenz übersteigt.  
  
    > [!NOTE]  
    > Wenn die Differenz größer ist, wird in einer Warnmeldung über die maximal zulässige Differenz informiert. Um fortfahren, müssen Sie den Betrag korrigieren. Klicken Sie auf **OK** , und geben Sie einen anderen MwSt.-Betrag ein, der innerhalb des zulässigen Bereichs liegt. Wenn die MwSt.-Differenz der maximal zulässigen Differenz entspricht oder höher ist, wird [!INCLUDE[d365fin](includes/d365fin_md.md)] die Abweichung im Feld **MwSt.-Differenz** angezeigt.  

## <a name="to-post-import-vat-with-purchase-invoices"></a>Import-MwSt mit Einkaufsrechnungen buchen
Zur Buchung einer Rechnung mit Einfuhrumsatzsteuer kann anstelle eines Fibu-Buch.-Blatts auch eine Einkaufsrechnung verwendet werden.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices"></a>Einkauf für die Buchung von Rechnungen mit Einfuhrumsatzsteuer einrichten  
1. Richten Sie eine Kreditorenkarte für die Einfuhrbehörde ein, die Ihnen die Einfuhrumsatzsteuerrechnung sendet. Die **Geschäftsbuchungsgruppe** und **MwSt.-Geschäftsbuchungsgruppe** werden genauso eingerichtet, wir das Sachkonto für die Einfuhrumsatzsteuer.  
2. Erstellen Sie eine **Produktbuchungsgruppe** für die Einfuhrumsatzsteuer, und richten Sie eine **Vorg.-MwSt.-Produktbuchungsgruppe** für die Einfuhrumsatzsteuer für die zugehörige **Produktbuchungsgruppe** ein.  
3. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Kontenplan** ein und wählen dann den zugehörigen Link aus.  
4. Wählen Sie das Sachkonto Einfuhrumsatzsteuer aus. Wählen Sie dann auf der Registerkarte **Start** in der Gruppe **Verwalten** die Option **Bearbeiten** aus.  
5. Wählen Sie auf dem Inforegister **Buchung** im Feld **Produktbuchungsgruppe** die Option SONST aus. [!INCLUDE[d365fin](includes/d365fin_md.md)] wird automatisch das Feld **VAT Prod. Buchungsgruppe** ausfüllen.  
6. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Buchungsmatrix Einrichtung** ein und wählen dann den zugehörigen Link aus.  
7. Im Fenster erstellen Sie eine Kombination **Gen. Bus. Buchungsgruppe** für die MwSt.-Behörde und der **Gen. Prod. Buchungsgruppe** für die Einfuhrumsatzsteuer. Für diese neue Kombination im Feld **Einkaufskonten**, wählen Sie das Sachkonto für die Einfuhrumsatzsteuer aus.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup"></a>So erstellen Sie eine neue Rechnung für die als Kreditor fungierende Einfuhrbehörde, nachdem Sie die Einrichtung abgeschlossen haben  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Einkaufsrechnungen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Erstellen Sie eine neue Einkaufsrechnung.  
3. Wählen Sie im Feld **Eink. von Kred.-Nr.** die als Kreditor fungierende Einfuhrbehörde, und klicken Sie danach auf **OK**.  
4. Klicken Sie in der ersten Einkaufszeile im Feld **Art**und wählen Sie **Sachkonto** und dann das **Nr.** Feld, wählen das Sachkonto Einfuhrumsatzsteuer aus.  
5. Geben Sie im Feld **Menge** den Wert **1** ein.  
6. Geben Sie im Feld **EK-Preis ohne MwSt.** den MwSt.-Betrag an.  
7. Buchen Sie die Rechnung.  

## <a name="to-process-certificates-of-supply"></a>Verarbeiten von Gelangensbestätigungen
Wenn Sie Waren an einen Debitor in einem anderen EU-Land/einer anderen EU-Region verkaufen, müssen Sie dem Kunden eine Gelangensbestätigung zusenden, die dieser unterschreiben und an Sie zurücksenden muss. Die folgenden Verfahren sind für die Bearbeitung von Zertifikaten von Vorrat für Verkaufslieferungen gedacht, dieselben Schritte gelten jedoch auch für Servicelieferungen von Artikeln und Rücklieferungen an Kreditoren.  

### <a name="to-view-certificate-of-supply-details"></a>So zeigen Sie die Details der Gelangensbestätigung an  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Gebuchte Rücklieferungen** ein und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die relevante Verkaufslieferung an einen Debitor in einem anderen EU-Land/einer anderen EU-Region aus.  
3. Wählen Sie **Details der Gelangensbestätigung**.  
4. Standardmäßig ist bei der Einrichtung des MwSt.-Buchungsgruppen-Setup für den Debitor das Kontrollkästchen **Gelangensbestätigung erforderlich** ausgewählt, dann ist das Feld **Status** standardmäßig auf **Erforderlich** festgelegt. Sie können das Feld automatisch aktualisieren, um anzugeben, dass Sie das Zertifikat von dem Debitor erhalten haben.  

    > [!Note]  
    >  Wenn bei der MwSt.-Buchungsgruppen-Einrichtung nicht das Kontrollkästchen **Gelangensbestätigung erforderlich** ausgewählt ist, wird ein Datensatz erstellt und das Feld **Status** auf **Nicht anwendbar** festgelegt. Sie können das Feld automatisch aktualisieren, um die richtigen Statusinformationen widerzuspiegeln. Sie können den Status bei Bedarf manuell von **Nicht anwendbar** in **Erforderlich** und von **Erforderlich** in **Nicht anwendbar** ändern.  

   Wenn Sie das Feld **Status** von **Erforderlich** in **Empfangen** oder in **Nicht erhalten** aktualisieren, wird ein Zertifikat erstellt.  
  
    > [!TIP]  
    >  Sie können das **Gelangensbestätigung**-Fenster verwenden, um eine Ansicht des Status aller gebuchten Lieferungen zu erhalten, für die eine Gelangensbestätigung erstellt wurde.  

5. Wählen Sie **Gelangensbestätigung drucken**.  
  
    > [!Note]  
    >  Sie können das Dokument in der Vorschau anzeigen oder drucken. Wenn Sie **Gelangensbestätigung drucken** auswählen und den Beleg drucken, wird das Kontrollkästchen **Gedruckt** automatisch ausgewählt. Darüber hinaus wird der Status des Zertifikats, wenn dies nicht bereits angegeben ist, zu **Erforderlich** aktualisiert. Sofern erorderlich, legen Sie das gedruckte Zertifikat der Lieferung bei.  

### <a name="to-print-a-certificate-of-supply"></a>So drucken Sie eine Gelangensbestätigung  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Gebuchte Rücklieferungen** ein und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die relevante Verkaufslieferung an einen Debitor in einem anderen EU-Land/einer anderen EU-Region aus.  
3. Wählen Sie **Gelangensbestätigung drucken**.  

    > [!NOTE]  
    >  Alternativ können Sie ein Zertifikats im Fenster **Gelangensbestätigung** drucken.  

4. Wählen Sie das Kontrollkästchen **Positionsdetails drucken**, um Informationen aus den Zeilen im Warenausgangsbeleg auf der Gelangensbestätigung zu berücksichtigen.  
5. Wählen Sie das Kontrollkästchen **Gelangensbestätigungen erstellen, falls nicht bereits erstellt**, um von [!INCLUDE[d365fin](includes/d365fin_md.md)] Zertifikate auf gebuchte Lieferungen erstellen zu lassen, die zum Zeitpunkt der Ausführung keine haben. Wenn Sie das Kontrollkästchen aktivieren, werden neue Zertifikate für alle gebuchten Lieferungen erstellt, die über keine Zertifikate innerhalb des ausgewählten Bereichs verfügen.  
6. Standardmäßig betreffen die Filtereinstellungen den Warenausgangsbeleg, den Sie ausgewählt haben. Füllen Sie die Filterinformationen aus, um eine spezifische Gelangensbestätigung auszuwählen, die Sie drucken möchten.  
7. Wählen Sie im Fenster **Gelangenbestätigung** die Schaltfläche **Drucken** aus, um den Bericht zu drucken, oder die Schaltfläche **Vorschau**, um den Bericht auf dem Bildschirm anzuzeigen.  

    > [!Note]  
    > Das **Gelangenbestätigung**-Feld und das Feld **Gedruckt**werden für die Lieferung im **Gelangensbestätigungen**-Fenster aktualisiert.  

8. Sie müssen die gedruckte Gelangensbestätigung zur Unterschrift an den Debitor senden.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment"></a>Um den Status einer Gelangensbestätigung für eine Lieferung zu aktualisieren  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Gebuchte Rücklieferungen** ein und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die relevante Verkaufslieferung an einen Debitor in einem anderen EU-Land/einer anderen EU-Region aus.  
3. Wählen Sie im Feld **Status** die entsprechende Option aus.  

   Wenn der Kunde eine Gelangensbestätigung zurücksendet, wählen Sie **Erhalten** aus. Das Feld **Eingangsdatum** wird aktualisiert. Standardmäßig ist das Wareneingangsdatum auf das aktuelle Arbeitsdatum festgelegt.  

   Sie können das Datum ändern, sodass das Datum angezeigt wird, an dem Sie die unterschriebene Gelangensbestätigung des Debitors erhalten haben. Sie können mit der Standard-[!INCLUDE[d365fin](includes/d365fin_md.md)]-Verknüpfung einen Link zu dem unterschriebenen Zertifikat hinzufügen.  

   Wenn der Kunde keine Gelangensbestätigung zurücksendet, wählen Sie **Nicht erhalten** aus. Sie müssen dem Debitor dann eine neue Rechnung mit MwSt. senden, da die ursprüngliche Rechnung vom Finanzamt nicht akzeptiert wird.  

Um eine Gruppe von Zertifikaten anzuzeigen, beginnen Sie im **Gelangensbestätigungen**-Fenster und aktualisieren dann die Informationen über den Status der ausstehenden Zertifikate nach und nach, wenn Sie sie von den Debitoren erhalten. Dies kann nützlich sein, wenn Sie für alle Zertifikate suchen möchten, die einen bestimmten Status haben, beispielsweise **Erforderlich**, um deren Status auf **Nicht erhalten** zu aktualisieren.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply"></a>Um den Status einer Gelangensbestätigungsgruppe zu aktualisieren  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Kostenzuteilungen** ein und wählen dann den zugehörigen Link aus.  
2. Dient zum Filtern des Feldes **Status** über den gewünschten Wert, um die Liste der Zertifikate zu erstellen, die Sie verwalten möchten.  
3. Um die Statusinformationen zu aktualisieren, aktivieren Sie **Liste bearbeiten**.  
4. Wählen Sie im Feld **Status** die entsprechende Option aus.  

   Wenn der Kunde eine Gelangensbestätigung zurücksendet, wählen Sie **Erhalten** aus. Das Feld **Eingangsdatum** wird aktualisiert. Standardmäßig ist das Wareneingangsdatum auf das aktuelle Arbeitsdatum festgelegt.  

   Sie können das Datum ändern, sodass das Datum angezeigt wird, an dem Sie die unterschriebene Gelangensbestätigung erhalten haben. Sie können mit der Standard-[!INCLUDE[d365fin](includes/d365fin_md.md)]-Verknüpfung einen Link zu dem unterschriebenen Zertifikat hinzufügen.  

    > [!NOTE]  
    >  Sie können keine neue Gelangensbestätigung im Fenster **Gelangensbestätigung** erstellen, indem Sie sie mithilfe dieses Verfahrens öffnen. Um ein Zertifikat für eine Lieferung zu erstellen, die nicht so eingerichtet wurde, dass eines erforderlich ist, öffnen Sie die gebuchte Verkaufslieferung und eine der beiden oben beschriebenen Prozeduren:  
    >   
    > * So erstellen Sie eine Gelangensbestätigung manuell  
    > * So drucken Sie eine Gelangensbestätigung.

## <a name="see-also"></a>Siehe auch  
[Methoden für die Berechnung und Buchung von Mehrwertsteuer einrichten](finance-setup-vat.md)   
[So gehts: Melden von MwSt. an eine Steuerbehörde](finance-how-report-vat.md)   

