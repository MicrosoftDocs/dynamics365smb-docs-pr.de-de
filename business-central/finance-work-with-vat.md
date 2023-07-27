---
title: Arbeiten mit der Mehrwertsteuer bei Verkäufen und Einkäufen
description: 'Dieses Thema beschreibt die verschiedenen Möglichkeiten, mit der Mehrwertsteuer sowohl manuell als auch mit der automatischen Einrichtung zu arbeiten, damit Sie die länder-/regionsspezifischen Vorschriften einhalten können.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, sales, purchases'
ms.search.form: '7, 118, 130, 142, 459, 460, 525'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="work-with-vat-on-sales-and-purchases"></a>Mit MwSt.im Verkauf und Einkauf arbeiten

Wenn Ihr Land oder Ihre Region verlangt, dass Sie die Mehrwertsteuer (MwSt.) auf Verkaufs- und Einkaufstransaktionen berechnen und melden, können Sie in [!INCLUDE[prod_short](includes/prod_short.md)] einrichten, dass Mehrwertsteuer berechnet wird. Weitere Informationen finden Sie [Einrichten der Berechnungs- und Buchungsmethoden für Mehrwertsteuer](finance-setup-vat.md).

Es gibt jedoch Mehrwertsteuer-verknüpfte Aufgaben, die Sie manuell tun können. Beispielsweise müssen Sie möglicherweise einen gebuchten Betrag korrigieren, wenn Sie feststellen, dass ein Kreditor eine andere Rundungsmethode verwendet.  

> [!TIP]
> Sie können [!INCLUDE[prod_short](includes/prod_short.md)] die Umsatzsteuer-Identifikationsnummern und andere Unternehmensinformationen, wenn Sie Dokumente erstellen oder aktualisieren lassen. Weitere Informationen finden Sie unter [Umsatzsteuer-Identifikationsnummern validieren](finance-how-validate-vat-registration-number.md).

## <a name="calculating-and-displaying-vat-amounts-on-sales-and-purchase-documents"></a>Berechnen und Anzeigen von MwSt.-Beträgen in Verkaufs- und Einkaufsbelegen

Wenn Sie eine Artikelnummer im **Nr.** Feld auf einem Verkaufs- oder Einkaufsbeleg, [!INCLUDE[prod_short](includes/prod_short.md)] füllt die Felder **Einzelpreis** und **Zeilenbetrag**. Der Verkaufspreis wird von der **Artikel**-Karte übernommen oder anhand der Artikelpreise berechnet, die für den Artikel und den Debitor zulässig sind. [!INCLUDE[prod_short](includes/prod_short.md)] berechnet den Zeilenbetrag nur dann, wenn Sie eine Menge für die Zeile eingeben.  

Wenn Sie möchten, dass die Einzelpreise und Zeilenbeträge Mehrwertsteuer enthalten, wenn Sie beispielsweise an Endverbraucher verkaufen, wählen Sie das **Preise inkl. MwSt**-Kontrollkästchen auf dem Dokument aus. Weitere Informationen finden Sie unter [Einschließlich oder ohne Mehrwertsteuer in Preisen und Zeilenbeträgen](#including-or-excluding-vat-in-prices-and-line-amounts). 

Je nach Debitoren- oder Kreditorenart können MwSt.-Beträge in Verkaufs- und Einkaufsbelegen unterschiedlich berechnet und angezeigt werden. Sie können den berechneten MwSt.-Betrag auch manuell ändern, z. B. um ihn an den von Ihrem Lieferanten für eine bestimmte Transaktion berechneten MwSt.-Betrag anzupassen.

### <a name="including-or-excluding-vat-in-prices-and-line-amounts"></a>Einschließlich oder ohne Mehrwertsteuer in Preisen und Zeilenbeträgen

Ist das Feld **Preise inkl. MwSt.** aktiviert, werden die Felder **VK-Preis** und **Zeilenbetrag** mit der MwSt. berechnet. Die Werte in diesen Feldern enthalten standardmäßig keine Mehrwertsteuer. Die Namen der Felder geben an, ob die Preise Mehrwertsteuer enthalten.  

Sie können die Standardeinstellung der **Preise inkl. MwSt.** für alle Verkaufsbelege eines Debitors im Feld **Preise inkl. MwSt.** auf der **Debitor**-Karte einrichten. Darüber hinaus können Sie auch Artikelpreise inklusive oder exklusive MwSt. einrichten. In der Regel enthalten die Preise auf der Artikelkarte keine Mehrwertsteuer. 

Die folgende Tabelle bietet einen Überblick darüber, wie in der Anwendung Verkaufspreise für einen Verkaufsbeleg berechnet werden, wenn auf der Seite **VK-Preise** keine Preise eingerichtet wurden:  

|**Feld "VK-Preis inkl. MwSt." auf Artikelkarte**|**Feld „Preise inkl. MwSt.“**|**Durchgeführte Aktion**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Nicht aktiviert|Nicht aktiviert|Der **VK-Preis** auf der Artikelkarte wird in das Feld **VK-Preis ohne MwSt.** in den Verkaufszeilen kopiert.|  
|Nicht aktiviert|Aktiviert|Die Anwendung berechnet den MwSt.-Betrag pro Einheit und fügt ihn dem **VK-Preis** auf der Artikelkarte hinzugefügt. Dieser Gesamtverkaufspreis wird dann in das Feld **VK-Preis inkl. MwSt.** in den Verkaufszeilen eingegeben.|  
|Aktiviert|Nicht aktiviert|Die Anwendung berechnet den MwSt.-Betrag, der im **VK-Preis** auf der **Artikelkarte** unter Verwendung des MwSt.-Prozentsatzes enthalten ist, der mit der Kombination aus MwSt.-Geschäftsbuchungsgruppe (Preis) und MwSt.-Produktbuchungsgruppe verknüpft ist. Der **VK-Preis** auf der Artikelkarte, verringert um den MwSt.-Betrag, wird dann im Feld **VK-Preis ohne MwSt.** in den Verkaufszeilen eingegeben. Weitere Informationen finden Sie unter [Verwenden von MwSt.-Geschäftsbuchungsgruppen und Kundenpreisgruppen](finance-work-with-vat.md#using-vat-business-posting-groups-and-customer-price-groups).|  
|Aktiviert|Aktiviert|Der **VK-Preis** auf der Artikelkarte wird in das Feld **VK-Preis inkl. MwSt.** in den Verkaufszeilen kopiert.|

#### <a name="using-vat-business-posting-groups-and-customer-price-groups"></a>Verwenden von MwSt.-Geschäftsbuchungsgruppen und Kundenpreisgruppen

Wenn Sie möchten, dass die Preise Mehrwertsteuer enthalten, können Sie Mehrwertsteuer-Geschäftsbuchungsgruppen verwenden, um den Betrag basierend auf der Mehrwertsteuerbuchungseinrichtung für die Gruppe zu berechnen. Weitere Informationen finden Sie unter [MwSt.-Geschäftsbuchungsgruppen festlegen](finance-setup-vat.md#set-up-vat-business-posting-groups).

Je nachdem, was Sie tun möchten, können Sie Debitoren oder Verkaufsbelegen eine MwSt.-Geschäftsbuchungsgruppe auf folgende Weise zuweisen:

* Um für alle Kunden denselben Mehrwertsteuersatz zu verwenden, können Sie eine Gruppe im **MwSt.-Geschäftsbuchungsgruppe (Preis)**-Feld auf der **Einrichtung von Verkäufen und Forderungen**-Seite auswählen.
* Um einen Mehrwertsteuersatz für einen bestimmten Kunden zu verwenden, können Sie auf der Seite **Debitorenkarte** im Feld **MwSt.-Geschäftsbuchungsgruppe (Preis)** eine Gruppe auswählen. 
* Um einen Mehrwertsteuersatz für bestimmte Debitoren zu verwenden, können Sie auf der Seite **Debitorenkarte** im Feld **Debitorenpreisgruppe** eine Gruppe auswählen. Dies ist beispielsweise nützlich, wenn Sie möchten, dass ein Preis für alle Debitoren in einer bestimmten geografischen Region oder einer bestimmten Branche gilt.
* Auf allen Verkaufsunterlagen im Feld **MwSt.-Geschäftsbuchungsgrp.**. Der für die Gruppe angegebene Mehrwertsteuerbetrag wird nur für das Dokument verwendet, an dem Sie gerade arbeiten.

> [!NOTE]
> Wenn Sie keine Gruppe im **MwSt.-Geschäftsbuchungsgruppe (Preis)** angeben, wird Mehrwertsteuer nicht in den Preisen enthalten sein.

#### <a name="examples"></a>Beispiele

Faktoren wie das Land oder die Region, in dem Sie verkaufen, oder die Art der Branchen, in die Sie verkaufen, können sich auf die Höhe der Mehrwertsteuer auswirken, die Sie abführen müssen. Beispielsweise kann ein Restaurant 6 % Mehrwertsteuer für Mahlzeiten berechnen, die im Haus eingenommen werden, und 17 % für Speisen zum Mitnehmen. Um dies zu erreichen, erstellen Sie eine Umsatzsteuer-Geschäftsbuchungsgruppe (Preis) für „Inhouse“ und eine für „Mitnahme“.

## <a name="working-with-vat-date"></a>Arbeiten mit MwSt.-Datum

### <a name="vat-date-in-documents"></a>Umsatzsteuerdatum in Dokumenten

Wenn Sie neue Verkaufs- oder Einkaufsbelege erstellen, basiert das **MwSt.-Datum** auf der Einstellung im Feld **Standard-MwSt.-Datum** auf der Seite **Hauptbuch einrichten**. Dieser Standardwert kann derselbe sein wie **Buchungsdatum** oder **Belegdatum**. Wenn Sie ein anderes MwSt.-Datum benötigen, können Sie den Wert im Feld **MwSt.-Datum** manuell ändern. Wenn Sie den Beleg buchen, wird das **MwSt.-Datum** auf dem Buchungsbeleg und in den Mehrwertsteuer- und Hauptbucheinträgen ausgewiesen.

> [!NOTE]
> Wenn das Feld **MwSt.-Datum** in Ihren Belegen oder Buchblättern nicht verfügbar ist, bedeutet dies, dass **Die Funktion „MwSt.-Datum“ nicht verwenden** im Feld **„MwSt.-Datum“-Nutzung** auf der Seite **Hauptbuchhaltungs-Einrichtung** nicht ausgewählt.  

> [!IMPORTANT]
> Wenn Sie **MwSt.-Zeitraum kontrollieren** in der **Hauptbuchhaltungs-Einrichtung** als **Buchung innerhalb geschlossenen Zeitraums sperren** oder **Buchung innerhalb geschlossenen Zeitraums sperren und für freigegebenen Zeitraum warnen** konfigurieren, können Sie Belege oder Buchblätter nur buchen, wenn sich das Datum im **MwSt.-Datum**-Feld nicht in einem geschlossenen Zeitraum in **Mehrwertsteuer-Rückgabeperioden** befindet. Auch wenn der Zeitraum in **Mehrwertsteuer-Rückgabeperioden** offen ist, erhalten Sie möglicherweise eine Warnung basierend auf dem **MwSt.-Rückgabestatus** und der Konfiguration im **MwSt.-Zeitraum kontrollieren**.

> [!IMPORTANT]
> Sie können das Buchen des **MwSt.-Datums** für bestimmte Datumsbereiche verhindern oder zulassen, indem Sie die Felder **Buchungen zugel. ab** und **Buchungen zugel. bis:** in der **Hauptbuchhaltungs-Einrichtung** und der **Benutzereinrichtung** verwenden.  

> [!NOTE]
> Wenn Sie **MwSt-Datum** leer lassen, verwendet [!INCLUDE [prod_short](includes/prod_short.md)] die Standardeinrichtung aus **Standard-Mwst-Datum** in der **Hauptbuchhaltungs-Einrichtung** als ein **MwSt-Datum** in der gebuchten Transaktion.  

### <a name="modifying-the-vat-date-in-posted-entries"></a>Ändern des MwSt.-Datums in gebuchten Einträgen

Bei Bedarf können Sie die gebuchten Belege zum MwSt.-Datum ändern. Zum Ändern des Datums im Feld **MwSt.-Datum** für gebuchte Belege müssen Sie die folgenden Schritte ausführen:

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun") Symbol. Geben Sie **MwSt.-Posten** ein und wählen Sie dann den entsprechenden Link. 
2. Finden Sie den Eintrag mit falschem Umsatzsteuerdatum.  
3. Wählen Sie die Aktion **Liste bearbeiten** und geben Sie dann das richtige Datum in das Feld **MwSt.-Datum** ein.  
4. Wenn Sie die Seite schließen, wird das MwSt-Datum in entspechenden **Sachkonteneinträgen** und im gebuchten Beleg geändert.  

> [!NOTE]
> Sie können das Feld **MwSt.-Datum** in **MwSt.-Einträge** nur ändern, wenn Ihr aktuelles Datum nicht in einer abgeschlossenen MwSt.-Rückgabezeitraum enthalten ist. Auch wenn der Zeitraum im Feld **Mehrwertsteuer-Rückgabeperioden** offen ist, erhalten Sie möglicherweise eine Warnung basierend auf dem **MwSt.-Rückgabestatus**.  

> [!NOTE]
> Wenn Ihr Beleg mehr als einen **MwSt.-Eintrag** enthält, müssen Sie nur den Wert im Feld **MwSt.-Datum** in einem Eintrag ändern, der sich auf den Beleg bezieht. Um die Einträge konsistent zu halten, ändert [!INCLUDE[prod_short](includes/prod_short.md)] das MwSt.-Datum in MwSt.-Einträgen, die sich auf diese Transaktion beziehen, automatisch. [!INCLUDE [prod_short](includes/prod_short.md)] aktualisiert das **MwSt.-Datum** in anderen Tabellen (FIBU-Einträge und Dokumente), jedoch nur in Bezug auf diese Transaktion.  

## <a name="correcting-vat-amounts-manually-on-sales-and-purchase-documents"></a>MwSt.-Beträgen in Verkaufs- und Einkaufsbelegen manuell korrigieren

Sie können Korrekturen an gebuchten MwSt.-Posten vornehmen und die Umsatzsteuer- und Vorsteuerbeträge verändern, ohne die MwSt.-Bemessungsgrundlage zu verändern. Zum Beispiel, wenn Sie eine Rechnung von einem Lieferanten mit einem falschen Mehrwertsteuerbetrag erhalten.  

Auch wenn Sie möglicherweise bereits eine oder mehrere Kombinationen für die Verarbeitung der Einfuhrumsatzsteuer eingerichtet haben, müssen Sie mindestens einen MwSt.-Produktbuchungsgruppencode einrichten. Beispielsweise können Sie den Namen **RICHTIG** für Korrekturen angeben, es sei denn, Sie können dasselbe Sachkonto im Feld **Vorsteuerkonto** in der MwSt.-Buchungsmatrixzeile verwenden. Weitere Informationen finden Sie [Einrichten der Berechnungs- und Buchungsmethoden für Mehrwertsteuer](finance-setup-vat.md).

Wenn Skonto auf der Basis einer Rechnung inklusive MwSt. berechnet wurde, haben Sie die Möglichkeit, den Skontoanteil des MwSt.-Betrages zu berichtigen, wenn Skonto gewährt wird. Beachten Sie, dass Sie das Feld **Skonto berichtigen** sowohl in der Finanzbuchhaltungs-Einrichtung: allgemein als auch in der MwSt.-Buchungsmatrix Einrichtung für bestimmte Kombinationen von MwSt.-Geschäftsbuchungsgruppe und MwSt.-Produktbuchungsgruppe aktivieren müssen.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-sales-documents"></a>Einrichtung des Systems für die manuelle MwSt.-Posten in Verkaufsbelegen
Im Folgenden wird beschrieben, wie manuelle MwSt.-Änderungen auf Verkaufsbelegen aktiviert werden. Die Schritte sind auf der Seite **Einrichten von Einkäufen und Verbindlichkeiten** gleich.

1. Geben Sie im Fenster **Finanzbuchhaltungs-Einrichtung:** eine **maximal zulässige MwSt.-Differenz** zwischen dem von der Anwendung berechneten Betrag und dem manuell eingegebenen Betrag an.  
2. Versehen Sie im Fenster **Debitoren & Verkauf Einr.** das Feld **MwSt.-Differenz zulassen** mit einem Häkchen.  

### <a name="to-adjust-vat-for-a-sales-document"></a>Die MwSt. für einen Verkaufsbeleg anpassen:

1. Öffnen Sie den entsprechenden Verkaufsauftrag.  
2. Wählen Sie die Aktion **Statistik** aus.  
3. Auf dem Inforegister **Fakturierung** wählen Sie im Feld den Wert **Anzahl der Steuerpositionen** aus.
4. Füllen Sie das Feld **MwSt.-Betrag** aus.   

> [!NOTE]  
> Der gesamte MwSt.-Betrag für die Rechnung wird gruppiert nach MwSt.-Kennzeichen in den Zeilen angezeigt. Sie können den Betrag manuell im Feld **MwSt.-Betrag** in den Zeilen für jedes MwSt.-Kennzeichen anpassen. Wenn Sie das Feld **MwSt.-Betrag** ändern, prüft die Anwendung, ob die Mehrwertsteuer um einen höheren Betrag als die maximal zulässige Differenz geändert worden ist. Liegt der Betrag außerhalb des unter **Max. MwSt.-Differenz zulässig** angegebenen Bereichs, werden Sie in einer Warnmeldung über die maximal zulässige Differenz informiert. Sie können erst dann fortfahren, wenn der Betrag an die zulässigen Parameter angeglichen wurde. Klicken Sie auf **OK** , und geben Sie einen anderen **MwSt.-Betrag** ein, der innerhalb des zulässigen Bereichs liegt. Wenn die MwSt.-Differenz der zulässigen Abweichung entspricht oder höher ist, wird die MwSt. proportional auf die Belegzeilen mit demselben MwSt.-Kennzeichen aufgeteilt.  

## <a name="calculating-vat-manually-using-journals"></a>MwSt.-Berechnung mithilfe von Buch.-Blättern manuell berechnen
Sie können MwSt.-Beträge auch in den Buch.-Blättern Allgemein, Verkauf und Einkauf anpassen. Dies ist unter Umständen dann erforderlich, wenn Sie eine Kreditorenrechnung in das Buch.-Blatt eingeben und zwischen der von der [!INCLUDE[prod_short](includes/prod_short.md)] Anwendung berechneten MwSt. und dem MwSt.-Betrag auf der erhaltenen Kreditorenrechnung eine Differenz besteht.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-general-journals"></a>Einrichtung des Systems für die manuelle MwSt.-Posten im Fibu Buch.-Blatt
Sie müssen die folgenden Schritte ausführen, bevor Sie die Mehrwertsteuer manuell in ein FibuBuch.-Blatt eingeben.  

1. Geben Sie im Fenster **Finanzbuchhaltungs-Einrichtung:** eine **maximal zulässige MwSt.-Differenz** zwischen dem von der Anwendung berechneten Betrag und dem manuell eingegebenen Betrag an.  
2. Wählen Sie auf der Seite **Allgemeine Buch.-Blatt Vorlage** das Kontrollkästchen **MwSt-Differenz zulassen** mit einem Häkchen.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-sales-and-purchase-journals"></a>Einrichtung des Systems für die manuellen MwSt.-Posten in einem Verkaufs- und Einkaufs-Buch.-Blatt

Sie müssen die folgenden Schritte ausführen, bevor Sie die Mehrwertsteuer manuell in ein Verkaufs- oder Einkaufs-FibuBuch.-Blatt eingeben.

1. Auf der Seite **Kreditoren & Einkauf Einr.** wählen Sie das Kontrollkästchen **MwSt.-Differenz zulassen**.  
2. Wiederholen Sie Schritt 1 für die Seite **Einkäufe und Verkäufe einrichten**.
3. Nachdem Sie die oben beschriebene Einrichtung durchgeführt haben, können Sie den Betrag im Feld **MwSt.-Betrag** in der Fibu-Buch.-Blattzeile oder das Feld **Gegenkonto MwSt.-Betrag** in der Verkaufs- oder Einkaufs-Buch.-Blattzeile an den MwSt.-Betrag der Rechnung anpassen. [!INCLUDE[prod_short](includes/prod_short.md)] Die Anwendung prüft, ob die Differenz die festgelegte maximale Differenz übersteigt.  

> [!NOTE]  
> Wenn die Differenz größer ist, wird in einer Warnmeldung über die maximal zulässige Differenz informiert. Um fortfahren, müssen Sie den Betrag korrigieren. Klicken Sie auf **OK** , und geben Sie einen anderen MwSt.-Betrag ein, der innerhalb des zulässigen Bereichs liegt. Wenn die MwSt.-Differenz der maximal zulässigen Differenz entspricht oder höher ist, wird [!INCLUDE[prod_short](includes/prod_short.md)] die Abweichung im Feld **MwSt.-Differenz** angezeigt.  

## <a name="posting-import-vat-with-purchase-invoices"></a>Einfuhrsteuer mit Einkaufsrechnungen buchen
Für die Buchung einer Rechnung mit Einfuhrumsatzsteuer kann anstelle eines Fibu-Buch.-Blatts auch eine Einkaufsrechnung verwendet werden.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices"></a>Einkauf für die Buchung von Rechnungen mit Einfuhrumsatzsteuer einrichten

1. Richten Sie eine Kreditorenkarte für die Einfuhrbehörde ein, die Ihnen die Einfuhrumsatzsteuerrechnung sendet. Die **Geschäftsbuchungsgruppe** und **MwSt.-Geschäftsbuchungsgruppe** werden genauso eingerichtet, wir das Sachkonto für die Einfuhrumsatzsteuer.  
2. Erstellen Sie eine **Produktbuchungsgruppe** für die Einfuhrumsatzsteuer, und richten Sie eine **Vorg.-MwSt.-Produktbuchungsgruppe** für die Einfuhrumsatzsteuer für die zugehörige **Produktbuchungsgruppe** ein.  
3. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.  
4. Markieren Sie das Hauptbuchkonto Einfuhrumsatzsteuer und wählen Sie dann die Aktion **Bearbeiten**.  
5. Wählen Sie auf dem Inforegister **Buchung** im Feld **Produktbuchungsgruppe** die Option SONST aus. [!INCLUDE[prod_short](includes/prod_short.md)] wird automatisch das Feld **VAT Prod. Buchungsgruppe** ausfüllen.  
6. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Allgemeine Buchungsmatrixeinrichtung** ein, und wählen Sie dann den zugehörigen Link.  
7. Im Fenster erstellen Sie eine Kombination **Gen. Bus. Buchungsgruppe** für die MwSt.-Behörde und der **Gen. Prod. Buchungsgruppe** für die Einfuhrumsatzsteuer. Für diese neue Kombination im Feld **Einkaufskonten**, wählen Sie das Sachkonto für die Einfuhrumsatzsteuer aus.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup"></a>So erstellen Sie eine neue Rechnung für die als Kreditor fungierende Einfuhrbehörde, nachdem Sie die Einrichtung abgeschlossen haben

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine neue Einkaufsrechnung.  
3. Wählen Sie im Feld **Eink. von Kred.-Nr.** die als Kreditor fungierende Einfuhrbehörde, und klicken Sie danach auf **OK**.  
4. Klicken Sie in der ersten Einkaufszeile im Feld **Art** und wählen Sie **Sachkonto** und dann das **Nr.** Feld, wählen das Sachkonto Einfuhrumsatzsteuer aus.  
5. Geben Sie im Feld **Menge** den Wert **1** ein.  
6. Geben Sie im Feld **EK-Preis ohne MwSt.** den MwSt.-Betrag an.  
7. Buchen Sie die Rechnung.  

## <a name="processing-certificates-of-supply"></a>Versorgungszertifikate verarbeiten

Wenn Sie Waren an einen Debitor in einem anderen EU-Land/einer anderen EU-Region verkaufen, müssen Sie dem Debitoren eine Gelangensbestätigung zusenden, die dieser unterschreiben und an Sie zurücksenden muss. Die folgenden Verfahren sind für die Bearbeitung von Zertifikaten von Vorrat für Verkaufslieferungen gedacht, dieselben Schritte gelten jedoch auch für Servicelieferungen von Artikeln und Rücklieferungen an Kreditoren.  

### <a name="to-view-certificate-of-supply-details"></a>So zeigen Sie die Details der Gelangensbestätigung an
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Gebuchte Verkaufslieferungen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die relevante Verkaufslieferung an einen Debitor in einem anderen EU-Land/einer anderen EU-Region aus.  
3. Wählen Sie **Details der Gelangensbestätigung**.  
4. Standardmäßig ist bei der Einrichtung des MwSt.-Buchungsgruppen-Setup für den Debitor das Kontrollkästchen **Gelangensbestätigung erforderlich** ausgewählt, dann ist das Feld **Status** standardmäßig auf **Erforderlich** festgelegt. Sie können das Feld automatisch aktualisieren, um anzugeben, dass Sie das Zertifikat von dem Debitor erhalten haben.  

> [!Note]  
>  Wenn bei der MwSt.-Buchungsgruppen-Einrichtung nicht das Kontrollkästchen **Gelangensbestätigung erforderlich** ausgewählt ist, wird ein Datensatz erstellt und das Feld **Status** auf **Nicht anwendbar** festgelegt. Sie können das Feld automatisch aktualisieren, um die richtigen Statusinformationen widerzuspiegeln. Sie können den Status bei Bedarf manuell von **Nicht anwendbar** in **Erforderlich** und von **Erforderlich** in **Nicht anwendbar** ändern.  

   Wenn Sie das Feld **Status** von **Erforderlich** in **Empfangen** oder in **Nicht erhalten** aktualisieren, wird ein Zertifikat erstellt.  

> [!TIP]  
>  Sie können auf der Seite **Gelangensbestätigung** verwenden, um eine Ansicht des Status aller gebuchten Lieferungen zu erhalten, für die eine Gelangensbestätigung erstellt wurde.  

5. Wählen Sie **Gelangensbestätigung drucken**.  

> [!Note]  
>  Sie können das Dokument in der Vorschau anzeigen oder drucken. Wenn Sie **Gelangensbestätigung drucken** auswählen und den Beleg drucken, wird das Kontrollkästchen **Gedruckt** automatisch ausgewählt. Darüber hinaus wird der Status des Zertifikats, wenn dies nicht bereits angegeben ist, zu **Erforderlich** aktualisiert. Sofern erorderlich, legen Sie das gedruckte Zertifikat der Lieferung bei.  

### <a name="to-print-a-certificate-of-supply"></a>So drucken Sie eine Gelangensbestätigung

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Gebuchte Verkaufslieferungen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die relevante Verkaufslieferung an einen Debitor in einem anderen EU-Land/einer anderen EU-Region aus.  
3. Wählen Sie **Gelangensbestätigung drucken**.  

> [!NOTE]  
>  Alternativ können Sie ein Zertifikats im Fenster **Gelangensbestätigung** drucken.  

4. Wählen Sie das Kontrollkästchen **Positionsdetails drucken**, um Informationen aus den Zeilen im Warenausgangsbeleg auf der Gelangensbestätigung zu berücksichtigen.  
5. Wählen Sie das Kontrollkästchen **Gelangensbestätigungen erstellen, falls nicht bereits erstellt**, um von [!INCLUDE[prod_short](includes/prod_short.md)] Zertifikate auf gebuchte Lieferungen erstellen zu lassen, die zum Zeitpunkt der Ausführung keine haben. Wenn Sie das Kontrollkästchen aktivieren, werden neue Zertifikate für alle gebuchten Lieferungen erstellt, die über keine Zertifikate innerhalb des ausgewählten Bereichs verfügen.  
6. Standardmäßig betreffen die Filtereinstellungen den Warenausgangsbeleg, den Sie ausgewählt haben. Füllen Sie die Filterinformationen aus, um eine spezifische Gelangensbestätigung auszuwählen, die Sie drucken möchten.  
7. Wählen Sie im Fenster **Gelangenbestätigung** die Schaltfläche **Drucken** aus, um den Bericht zu drucken, oder die Schaltfläche **Vorschau**, um den Bericht auf dem Bildschirm anzuzeigen.  

> [!Note]  
> Das **Gelangenbestätigung**-Feld und das Feld **Gedruckt** werden für die Lieferung auf der Seite **Gelangensbestätigungen** aktualisiert.  

8. Sie müssen die gedruckte Gelangensbestätigung zur Unterschrift an den Debitor senden.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment"></a>Um den Status einer Gelangensbestätigung für eine Lieferung zu aktualisieren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Gebuchte Verkaufslieferungen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die relevante Verkaufslieferung an einen Debitor in einem anderen EU-Land/einer anderen EU-Region aus.  
3. Wählen Sie im Feld **Status** die entsprechende Option aus.  

   Wenn der Debitor eine Gelangensbestätigung zurücksendet, wählen Sie **Erhalten** aus. Das Feld **Eingangsdatum** wird aktualisiert. Standardmäßig ist das Wareneingangsdatum auf das aktuelle Arbeitsdatum festgelegt.  

   Sie können das Datum ändern, sodass das Datum angezeigt wird, an dem Sie die unterschriebene Gelangensbestätigung des Debitors erhalten haben. Sie können mit der Standard-[!INCLUDE[prod_short](includes/prod_short.md)]-Verknüpfung einen Link zu dem unterschriebenen Zertifikat hinzufügen.  

   Wenn der Debitor keine Gelangensbestätigung zurücksendet, wählen Sie **Nicht erhalten** aus. Sie müssen dem Debitor dann eine neue Rechnung mit MwSt. senden, da die ursprüngliche Rechnung vom Finanzamt nicht akzeptiert wird.  

Um eine Gruppe von Zertifikaten anzuzeigen, beginnen Sie auf der Seite **Gelangensbestätigungen** und aktualisieren dann die Informationen über den Status der ausstehenden Zertifikate nach und nach, wenn Sie sie von den Debitoren erhalten. Dies kann nützlich sein, wenn Sie für alle Zertifikate suchen möchten, die einen bestimmten Status haben, beispielsweise **Erforderlich**, um deren Status auf **Nicht erhalten** zu aktualisieren.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply"></a>Um den Status einer Gelangensbestätigungsgruppe zu aktualisieren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Gelangensbestätigungen** ein, und wählen Sie den entsprechenden Link.  
2. Dient zum Filtern des Feldes **Status** über den gewünschten Wert, um die Liste der Zertifikate zu erstellen, die Sie verwalten möchten.  
3. Um die Statusinformationen zu aktualisieren, aktivieren Sie **Liste bearbeiten**.  
4. Wählen Sie im Feld **Status** die entsprechende Option aus.  

   Wenn der Debitor eine Gelangensbestätigung zurücksendet, wählen Sie **Erhalten** aus. Das Feld **Eingangsdatum** wird aktualisiert. Standardmäßig ist das Wareneingangsdatum auf das aktuelle Arbeitsdatum festgelegt.  

   Sie können das Datum ändern, sodass das Datum angezeigt wird, an dem Sie die unterschriebene Gelangensbestätigung erhalten haben. Sie können mit der Standard-[!INCLUDE[prod_short](includes/prod_short.md)]-Verknüpfung einen Link zu dem unterschriebenen Zertifikat hinzufügen.  

> [!NOTE]
> Sie können keine neue Gelangensbestätigung auf der Seite **Gelangensbestätigung** erstellen, indem Sie sie mithilfe dieses Verfahrens öffnen. Um ein Zertifikat für eine Lieferung zu erstellen, die nicht so eingerichtet wurde, dass eines erforderlich ist, öffnen Sie die gebuchte Verkaufslieferung und eine der beiden oben beschriebenen Prozeduren:  
>
> * So erstellen Sie eine Gelangensbestätigung manuell  
> * So drucken Sie eine Gelangensbestätigung.

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Berechnungen einrichten und Buchungsmethoden für Mehrwertsteuer](finance-setup-vat.md)  
[Meldung der Mehrwertsteuer an eine Steuerbehörde](finance-how-report-vat.md)  
[Eine Umsatzsteuer-Identifikationsnummer überprüfen](finance-how-validate-vat-registration-number.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
