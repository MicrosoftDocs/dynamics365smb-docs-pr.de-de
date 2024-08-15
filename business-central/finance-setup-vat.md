---
title: Mehrwertsteuer einrichten
description: 'Überprüfen Sie, ob Sie die MwSt für Verkäufe und Einkäufe korrekt berechnen, buchen und melden. Es wird empfohlen, dass Sie diesen Einrichtungsleitfaden verwenden, um die MwSt einzurichten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '10, 118, 391, 470, 471, 472, 575, 734, 747, 748, 1877,'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Berechnungen und Buchungsmethoden für Mehrwertsteuer einrichten

Verbraucher und Geschäfte bezahlen Mehrwertsteuer (MwSt), wenn Sie Waren oder Dienstleistungen einkaufen. Der zu bezahlende MwSt-Betrag kann abhängig von verschiedenen Faktoren variieren. In [!INCLUDE[prod_short](includes/prod_short.md)] legen Sie die Sätze fest, die für die Berechnung der Steuerbeträge auf der Grundlage der folgenden Parameter verwendet werden sollen:

* An wen Sie verkaufen  
* Von wem Sie kaufen  
* Was Sie verkaufen  
* Was Sie kaufen  

Sie können die Berechnungen der MwSt manuell einrichten, aber das kann heikel und zeitaufwendig sein. Es kommt leicht vor, dass versehentlich unterschiedliche Mehrwertsteuersätze verwendet werden, wodurch ungenaue Mehrwertsteuer verknüpfte Berichte entstehen würde. Um die Einrichtung der Mehrwertsteuer zu vereinfachen, empfehlen wir Ihnen, die geführte Anleitung **Mehrwertsteuer einrichten** im Produkt zu verwenden.

Wenn Sie MwSt-Berechnungen selbst einrichten möchten oder einfach mehr über jeden Schritt erfahren möchten, enthält dieser Artikel Beschreibungen jedes Schrittes.  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="set-up-vat-using-the-assisted-setup-guide-recommended"></a>Verwenden der Anleitung zur unterstützten Einrichtung der Mehrwertsteuer (empfohlen)

> [!NOTE]
> Sie können die Anleitung **MwSt.-Einrichtung** nur nutzen, wenn Sie *Meine Unternehmen* erstellt haben, und keine Transaktionen gebucht haben, die Mehrwertsteuer beinhalten. Weitere Informationen zu „Mein Unternehmen“ finden Sie unter [Neue Unternehmen in [!INCLUDE[prod_short](includes/prod_short.md)] erstellen](about-new-company.md).

Um die unterstützte Einrichtung zu starten, gehen Sie folgendermaßen vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol. Geben Sie **Unterstützte Einrichtung** ein. 
2. Wählen Sie **Mehrwertsteuer (MwSt.) einrichten** aus, und führen Sie die Schritte aus.
3. Nachdem Sie die unterstützte Einrichtung abgeschlossen haben, wechseln Sie zur Seite **MwSt.-Buchungseinrichtung** und überprüfen Sie, ob Sie entsprechend den lokalen Anforderungen in Ihrer Version von [!INCLUDE [prod_short](includes/prod_short.md)] weitere Felder ausfüllen müssen. Weitere Informationen unter [Lokale Funktion in Business Central](about-localization.md).  

### <a name="check-the-vat-posting-setup"></a>Überprüfen Sie die Einrichtung der MwSt.-Buchung

Um Sie beim schnellen Einstieg zu unterstützen, zeigt [!INCLUDE [prod_short](includes/prod_short.md)] Ihnen Benachrichtigungen an, wenn Ihnen Hauptbuchkonten (Sachkonten) in Buchungsgruppen oder Buchungseinstellungen fehlen, wie z. B. die **Einrichtung der MwSt.-Buchung**-Seite. Sie können diese Art der Benachrichtigung über **Sachkonto ist nicht in der Buchungsgruppe oder Einrichtung vorhanden**-Benachrichtigung in der **Meine Benachrichtigungen**-Seite ein- oder ausschalten. Wählen Sie einfach auf der Seite **Meine Einstellungen** den Link **Ändern, wenn ich Benachrichtigungen erhalte** aus.  

Wenn Sie die Benachrichtigung auswählen, erstellt [!INCLUDE [prod_short](includes/prod_short.md)] automatisch diese Buchungseinstellungen basierend auf den Buchungsgruppen in dem Dokument oder Journal, an dem Sie gerade arbeiten.  

An dieser Stelle können Sie einfach die fehlenden Sachkonten ausfüllen. Aber wenn Sie Ihre Einrichtung später weiter verfeinern, stellen Sie möglicherweise fest, dass Ihre ursprüngliche Einrichtung falsch ist. [!INCLUDE [prod_short](includes/prod_short.md)] ermöglicht Ihnen nicht, eine MwSt.-Buchungseinrichtung und eine allgemeine Buchungseinrichtung zu löschen, nachdem diese zum Erstellen von Posten verwendet wurden. Um zu verhindern, dass Benutzer versehentlich eine Einrichtung verwenden, die für neue Buchungen nicht mehr relevant ist, können Sie das Feld **Gesperrt** auf der Seite **Buchungsmatrix**.

## <a name="set-up-a-default-vat-date-for-documents-and-journals"></a>Richten Sie ein Standard-MwSt.-Datum für Dokumente und Journale ein

Umsatzsteuermeldung in [!INCLUDE [prod_short](includes/prod_short.md)] basiert auf dem **MwSt.-Datum**, um MwSt.-Einträge in MwSt.-Berichte in eine MwSt.-Periode aufzunehmen. Das MwSt.-Datum kann für alle Dokumente und Journale geändert werden, aber Sie müssen einen Standardwert für das MwSt.-Datum angeben.

> [!NOTE]
> Nach dem Buchen des Belegs oder Journals erscheint das **MwSt.-Datum** unter **MwSt.-Einträge** und **Sachkonteneinträge** sowie auf dem gebuchten Beleg, falls vorhanden.

Gehen Sie folgendermaßen vor, um einen Standardwert für ein MwSt.-Datum einzurichten:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Hauptbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie im Inforegister **Allgemein** im **Standard-MwSt.-Datum** entweder **Buchungsdatum** oder **Belegdatum**.
3. Die Seite schließen.  

> [!NOTE]
> Standardmäßig ist das **Standard-MwSt.-Datum** das **Buchungsdatum**.

### <a name="enable-or-disable-the-vat-date-feature"></a>Das Feature „MwSt.-Datum“ aktivieren oder deaktivieren

Manche Länder/Regionen verlangen, dass Unternehmen ein bestimmtes MwSt.-Datum verwenden, andere Länder/Regionen jedoch nicht. In einigen Ländern/Regionen müssen Unternehmen in bestimmten Situationen das MwSt.-Datum ändern, nachdem sie die Belege gebucht haben, in anderen Ländern/Regionen ist eine Änderung des MwSt.-Datums jedoch nicht zulässig. Um unterschiedliche Kontexte zu berücksichtigen, können Sie wählen, ob und in welchem Umfang Sie diese Funktionalität nutzen möchten.

Führen Sie die folgenden Schritte aus, um die Höhe der Verwendung von MwSt.-Daten einzurichten:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Hauptbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie auf dem Inforegister **Allgemein** im Feld **Verwendung des MwSt.-Datums** den Grad an, zu dem Sie das Feature für das MwSt.-Datum verwenden möchten. Sie haben eine der folgenden Optionen auswählen:

   | Typ | Beschreibung |
   |--------------------|-----------------------------------------|
   | **Die Funktion MwSt.-Datum vollumfänglich verwenden** | Alles rund um das **MwSt.-Datum** funktioniert standardmäßig und Sie haben die größtmögliche **MwSt.-Datum**-Funktionalität. Sie können das Datum einrichten, es in Belegen ändern, darauf basierende Berichte erstellen und das Datum nach der Buchung ändern, solange der Zeitraum nicht geschlossen oder durch zulässige Daten für die Buchung geschützt ist. |
   | **Verwenden ohne Änderungen zuzulassen** | Alles rund um das **MwSt.-Datum** funktioniert standardmäßig mit einer Ausnahme. Sie können das **MwSt.-Datum** in **MwSt.-Posten**. |
   | **Die Funktion MwSt.-Datum nicht verwenden** | [!INCLUDE [prod_short](includes/prod_short.md)] blendet die Felder **MwSt.-Datum** aus und macht sie für Belege, Journale und Posten nicht verfügbar. Das **Standard-MwSt.-Datum** wird als **Buchungsdatum** konfiguriert. |

3. Schließen Sie die Seite.

> [!IMPORTANT]
> Auch wenn Sie sich für die Option **ie Funktion MwSt.-Datum nicht verwenden** nicht verwenden, nutzt [!INCLUDE [prod_short](includes/prod_short.md)] **MwSt.-Datum** im Hintergrund. Weil das **Standard-MwSt.-Datum** als **Buchungsdatum** konfiguriert ist und Sie es in diesem Fall nicht ändern können, ist die Erfahrung dieselbe wie ohne diese Funktion. Die **MwSt.-Datum**-Felder werden von allen Seiten entfernt, aber dieses Feld ist weiterhin in Tabellen vorhanden und Berichte funktionieren basierend darauf.

### <a name="limiting-periods-for-posting-and-changing-the-vat-date"></a>Zeiträume für die Buchung und Änderung des MwSt.-Datums einschränken

Sie können verhindern, dass Personen MwSt.-Posten in bestimmten Datumsbereichen buchen oder ändern. Sie legen die Einschränkung mithilfe von zwei Einstellungen fest:

* Basierend auf dem geschlossenen **MwSt.-Rückgabezeitraum**
* Basierend auf den Feldern **Buchungen zulassen ab** und **Buchungen zulassen bis**.

#### <a name="to-limit-posting-based-on-vat-return-period"></a>Um die Buchung basierend auf dem MwSt.-Rückgabezeitraum zu begrenzen

1. Wählen Sie die ![Glühbirne, die da „Wie möchten Sie weiter verfahren“-Feature 1.](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Hauptbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie auf dem Inforegister **Allgemein** im Feld **MwSt.-Zeitraum kontrollieren** den Grad ein, bis zu dem der MwSt.-Rückgabezeitraum kontrolliert werden kann. Die Optionen werden in der folgenden Tabelle beschrieben.

| Typ | Beschreibung |
|--------------------|-----------------------------------------|
| **Buchung innerhalb geschlossenen Zeitraums sperren und für freigegebenen Zeitraum warnen** | Verhindern Sie, dass Belege oder Journale gebucht oder MwSt.-Posten ändert werden, die ein MwSt.-Datum innerhalb eines geschlossenen **MwSt.-Rückgabezeitraums** haben. [!INCLUDE [prod_short](includes/prod_short.md)] zeigt auch eine Warnung an, wenn Ihr **MwSt.-Rückgabezeitraum** geöffnet ist, aber der Status **MwSt.-Rückgabe** **Freigegeben** oder **Eingereicht** lautet. |
| **Buchung innerhalb geschlossenen Zeitraums sperren** | Verhindern Sie, dass Belege oder ein Journale gebucht oder MwSt.-Posten geändert werden, die ein MwSt.-Datum innerhalb des geschlossenen **MwSt.-Rückgabezeitraums** haben. |
| **Bei Buchung in geschlossenem Zeitraum warnen** | Zeigen Sie eine Warnung an, aber blockieren Sie die Buchung nicht, wenn Sie einen Beleg oder ein Journal buchen möchten, dessen MwSt.-Datum in einem geschlossenen **MwSt.-Rückgabezeitraum** liegt. |
| **Deaktiviert** | Ergreifen Sie keine Maßnahmen basierend auf einem geschlossenen **MwSt.-Rückgabezeitraum**. |

#### <a name="limit-posting-based-on-allow-fromto-period"></a>Buchen basierend auf dem „Erlauben ab/bis“-Zeitraum einschränken

> [!NOTE]
> Ab Business Central Version 23.1 wird dieses Steuerelement geändert. In früheren Versionen gab es auf der Seite **Finanzbuchhaltung Einrichtung** nur ein Steuerelement sowohl für das Buchungsdatum als auch für das MwSt-Datum. Jetzt sind diese Steuerelemente aufgeteilt, sodass das Steuerelement auf der Seite **Finanzbuchhaltung Einrichtung** nur für das **Buchungsdatum** gilt und das Steuerelement auf der Seite **MwSt.-Einrichtung** gilt nur für das **MwSt-Datum**. Es gibt auch neue Datumssteuerelemente auf der Seite **Benutzereinstellungen**.  

##### <a name="version-231-or-newer"></a>Version 23.1 oder neuer

> [!IMPORTANT]
> Beachten Sie beim Upgrade auf eine neue Version, dass die Werte im neuen **MwSt.-Datum zulassen von** auf der Seite **MwSt.-Einrichtung** basierend auf den Werten von **Buchungen zulassen ab/bis** im **Finanzbuchhaltung Einrichtung** aktualisiert werden. Wenn Sie andere Datumssteuerelemente verwenden möchten, öffnen Sie die Seite **MwSt.-Einrichtung** und nehmen Sie Änderungen vor.  

Sie können Einschränkungen für das Unternehmen oder bestimmte Benutzerebenen einrichten.

So beschränken Sie alle Buchungen für das gesamte Unternehmen:

1. Wählen Sie die ![Glühbirne, welche die 1. „Sie wünschen ...“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Geben Sie **MwSt.-Einrichtung** ein und wählen Sie dann den zugehörigen Link aus.  
2. Geben Sie auf dem Inforegister **MwSt.-Datum** im Feld **MwSt.-Datum zulassen von** das MwSt.-Datum an, ab dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MwSt.-Datum vor diesem Datum ist nicht zulässig.  
3. Geben Sie auf dem Inforegister **MwSt.-Datum** im Feld **MwSt.-Datum zulassen bis** das MwSt.-Datum an, bis zu dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MwSt.-Datum nach diesem Datum ist nicht zulässig. 

So begrenzen Sie Buchungen für einen bestimmten Benutzenden:  

1. Wählen Sie die ![Glühbirne, welche die 1. „Sie wünschen ...“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Benutzereinrichtung** ein und wählen Sie dann den zugehörigen Link aus.  
2. Geben Sie unter **Benutzer-ID** den Benutzenden an, der in einem bestimmten Zeitraum buchen darf.  
3. Geben Sie im Feld **MwSt.-Datum zulassen von** das MwSt.-Datum an, ab dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MwSt.-Datum vor diesem Datum ist nicht zulässig. 
4. Geben Sie im Feld **MwSt.-Datum zulassen bis** das MwSt.-Datum an, bis zu dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MwSt.-Datum nach diesem Datum ist nicht zulässig.  

##### <a name="versions-before-231"></a>Versionen vor 23.1

Sie können eine Einschränkung für das Unternehmen oder bestimmte Benutzerebenen einrichten.

So beschränken Sie alle Buchungen für das gesamte Unternehmen:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Hauptbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie auf dem Inforegister **Allgemein** im Feld **Buchungen zulassen ab** das MwSt.-Datum an, ab dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MwSt.-Datum vor diesem Datum ist nicht zulässig.  
3. Geben Sie auf dem Inforegister **Allgemein** im Feld **Buchungen zulassen bis** das MwSt.-Datum an, bis zu dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MwSt.-Datum nach diesem Datum ist nicht zulässig.

So begrenzen Sie Buchungen für einen bestimmten Benutzenden:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Benutzereinrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie unter **Benutzer-ID** den Benutzenden an, der in einem bestimmten Zeitraum buchen darf.  
3. Geben Sie im Feld **Buchungen zulassen ab** das MwSt.-Datum an, ab dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MwSt.-Datum vor diesem Datum ist nicht zulässig.
4. Geben Sie im Feld **Buchungen zulassen bis** das MwSt.-Datum an, bis zu dem Sie Buchungen zulassen. Das Buchen eines Belegs oder Journals mit einem MwSt.-Datum nach diesem Datum ist nicht zulässig.

## <a name="set-up-vat-registration-numbers-for-your-countryregion"></a>Umsatzsteuer-Identifikationsnummern für Ihr Land/Ihre Region festlegen

Um zu helfen sicherzustellen, dass Personal gültige MwSt-IdNr. eingeben, können Sie die MwSt-IdNr für die Länder/Regionen verwenden, in denen Sie Geschäfte tätigen. [!INCLUDE[prod_short](includes/prod_short.md)] zeigt eine Fehlermeldung an, wenn jemand einen Fehler macht oder ein Format verwendet, das für das Land/die Region falsch ist.

Um MwSt-Nr. einzurichten, gehen Sie folgendermaßen vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 2.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Länder/Regionen** ein.
2. Wählen Sie das Land bzw. die Region, und wählen die **MwSt Reg. Nr. Formaten** Aktion aus.
3. Im Feld **Formate** definieren Sie das Format, indem Sie einen oder mehrere der folgenden Zeichen eingeben:  

* **#** Erfordert eine einstellige Nummer.  
* **@** Erfordert einen Buchstaben. Bei diesem Format wird nicht zwischen Groß- und Kleinschreibung unterschieden.  
* **?** Erlaubt jegliches Zeichen.  

    > [!TIP]
    > Sie können andere Zeichen verwenden, sofern sie immer im Land- oder Bereichsformat vorkommen. Wenn Sie also eine Periode oder einen Bindestrich zwischen und Nummern einfügen möchten, können Sie ##.####.### oder @@-###-### definieren.  

## <a name="set-up-vat-business-posting-groups"></a>MwSt.-Geschäftsbuchungsgruppen festlegen

MwSt.-Geschäftsbuchungsgruppen sollten die Märkte darstellen, in denen Sie Geschäfte mit Debitoren und Kreditoren tätigen, und definieren, wie die Mehrwertsteuer in jedem Zielmarkt berechnet und gebucht werden. Beispiele von MwSt.-Produktbuchungsgruppen sind **Inland** und **Europäischen Union (EU)**.  

Verwenden Sie aussagekräftige Codes, an die Sie sich leicht erinnern können, z. B. **EU** **Nicht-EU** oder **Inland**. Jeder Code muss eindeutig sein. Sie können beliebig viele Codes einrichten, aber es ist nicht möglich, denselben Code zweimal in einer Tabelle zu verwenden.

Um eine MwSt.-Geschäftsbuchungsgruppe festzulegen, gehen Sie wie folgt vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 3.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **MWSt.-Geschäftsbuchungsgrp. ein** und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder nach Bedarf aus.

Sie richten Vorgabe MwSt.-Geschäftsbuchungsgruppen ein, indem Sie sie mit den Geschäftsbuchungsgruppen verbinden. [!INCLUDE[prod_short](includes/prod_short.md)] fügt automatisch die MwSt Geschäftsbuchungsgruppe hinzu, wenn Sie die Geschäftsbuchungsgruppe einem Debitor, Kreditor oder Sachkonto zuweisen.

## <a name="set-up-vat-product-posting-groups"></a>Legen Sie MwSt.-Produktbuchungsgruppen fest

Mithilfe der MwSt.-Produktbuchungsgruppencodes wird die Berechnung und Buchung der MwSt. gemäß der Art des gekauften Artikels oder der Art der Ressourcen bestimmt.

Es ist sinnvoll, Codes zu verwenden, an die man sich einfach erinnern kann, und die die Werte, wie **Keine MwSt.** oder **Null**, **MwSt.** oder **Reduziert** für 10 % MwSt. beschreiben, und **MwSt. 25** oder **Standard** für 25 % zu verwenden.

Um eine MwSt.-Geschäftsbuchungsgruppe festzulegen, gehen Sie wie folgt vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 4.](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **MWSt.-Produktbuchungsgruppen** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder nach Bedarf aus.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Kombinieren Sie MwSt.-Buchungsgruppen in MwSt.-Buchungseinrichtungen

[!INCLUDE[prod_short](includes/prod_short.md)] berechnet MwSt.-Beträge in Verkaufs- und Einkaufsberichten basierend auf MwSt.-Buchungsmatrix Einrichtung, die Kombinationen von Mehrwertsteuergeschäfts und -Produktbuchungsgruppen sind. Für jede Kombination können Sie den MwSt.-Prozentsatz, die MwSt.-Berechnungsart und die Sachkontonummern für die Buchung der MwSt. für Verkäufe, Käufe und Erwerbssteuer eingeben. Sie können auch angeben, ob die MwSt. neu berechnet wird, wenn Skonto angewandt oder erhalten wird.  

Sie können beliebig viele Codes einrichten. Um MwSt.-Buchungsmatrixeinrichtungen mit ähnlichen Attributen in Gruppen zusammenzufassen, können Sie für jede Gruppe ein **MwSt.-Kennzeichen** erstellen und das Kennzeichen dann den Gruppenmitgliedern zuweisen.  

> [!NOTE]
> Ein **MwSt.-Kennzeichen** ist ein Code, den Sie zum Gruppieren ähnlicher Attribute verwenden können. Wir empfehlen Ihnen, unterschiedliche MwSt.-Kennzeichen für unterschiedliche MwSt.-Prozentsätze zu verwenden.  

Um MwSt.-Buchungseinrichtungen zu kombinieren, gehen Sie folgendermaßen vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 5.](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **MWSt.-Buchungseinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Weisen Sie VAT-Buchungsgruppen standardmäßig mehreren Entitäten zu

Wenn Sie identische MwSt.-Buchungsgruppen für mehrere Einheiten übernehmen möchten, können Sie [!INCLUDE[prod_short](includes/prod_short.md)] festlegen, um dies standardmäßig durchzuführen.

* Sie können MwSt.-Geschäftsbuchungsgruppen allgemeinen Geschäftsbuchungsgruppen oder Debitoren- oder Kreditorenvorlagen zuweisen.
* Sie können MwSt.-Produktbuchungsgruppen allgemeinen Produktbuchungsgruppen zuweisen.  

Die MwSt- Geschäfts- oder - Produktbuchungsgruppe wird zugewiesen, wenn Sie eine Geschäfts- oder eine Produktbuchungsgruppe für einen Debitor, einen Kreditor, einen Artikel oder eine Ressource auswählen.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Weisen Sie Konten, Debitor, Kreditor, Artikel und Ressourcen Buchungsgruppen für die Mehrwertsteuer zu.

Die folgenden Abschnitten beschreiben, wie die MwSt.-Buchungsgruppen einzelnen Einheiten zugewiesen werden.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>So weisen Sie MwSt.-Buchungsgruppen einzelnen Sachkonten zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 6.](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnet Sie die **Sachkontokarte** für das Konto.  
3. Wählen Sie im Inforegister **Buchen** im Feld **Buchungsart** entweder **Verkauf** oder **Einkauf** aus.  
4. Wählen Sie die MwSt.-Buchungsgruppen aus, die Sie für das Verkaufs- bzw. das Wareneingangskonto verwenden möchten.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Um MwSt-Geschäftsbuchungsgruppen Debitoren und Kreditoren zuzuweisen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 7.](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Kunde** oder **Kreditor** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Karte **Debitor** oder **Debitor** erweitern Sie das Inforegister **Fakturierung**.  
3. Wählen Sie die MwSt-Geschäftsbuchungsgruppe aus.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Um MwSt-Produktbuchungsgruppen einzelnen Artikeln und Ressourcen zuzuweisen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 8.](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Element** oder **Ressource** ein und wählen Sie dann den zugehörigen Link.  
2. Führen Sie einen der folgenden Schritte aus:  

    * Auf der Karte **Artikel** erweitern Sie das Inforegister **Preis und Buchung**, und wählen Sie dann **Mehr anzeigen**, um das Feld **MwSt Produktbuchungsgruppe** anzuzeigen.  
    * Erweitern Sie auf der Karte **Ressource** das Inforegister **Fakturierung**.  
3. Wählen Sie die MwSt-Produktbuchungsgruppe aus.  

## <a name="set-up-clauses-to-explain-vat-exemption-or-nonstandard-vat-rates"></a>Klauseln zur Erklärung der MwSt.-Befreiung oder von nicht standardmäßigen MwSt.-Sätzen einrichten

Sie richten eine MwSt.-Klausel ein, um Informationen über die Art der MwSt. zu beschreiben, die angewendet wird. Diese Informationen werden möglicherweise aufgrund behördlicher Regulierungen verlangt. Nachdem Sie eine MwSt.-Klausel festgelegt und sie einer MwSt.-Buchungsmatrix zugeordnet haben, wird die MwSt.-Klausel auf allen gedruckten Verkaufsbelegen angezeigt, die diese MwSt.-Buchungsgruppeneinrichtung verwenden.

Bei Bedarf können Sie auch festlegen, wie Mehrwertsteuerklauseln in andere Sprachen übersetzt werden. Wenn Sie für einen Debitor einen Verkaufsbeleg erstellen und drucken, der ein MwSt.-Kennzeichen enthält, enthält der gedruckte Beleg die MwSt.-Klausel in übersetzter Form. Der auf der Kundenkarte angegebene Sprachcode bestimmt die Sprache.

Wenn Sie in verschiedenen Belegtypen, wie Rechnungen oder Gutschriften, nicht standardisierte Mehrwertsteuersätze verwenden, müssen Sie möglicherweise Text für die Mehrwertsteuerbefreiung (MwSt.-Klausel) einfügen. Aus dem Befreiungstext geht hervor, warum ein ermäßigter Mehrwertsteuersatz oder ein Nullsteuersatz berechnet wurde. Auf der Seite **MwSt.-Klauseln nach Belegtyp** können Sie für jeden Belegtyp unterschiedliche MwSt.-Klauseln definieren, die in Geschäftsdokumente aufgenommen werden sollen.

Sie können eine MwSt.-Klausel ändern oder löschen, und Ihre Änderungen werden in einem generierten Bericht angezeigt. [!INCLUDE[prod_short](includes/prod_short.md)] bewahrt jedoch keinen Verlauf der Änderung auf. In dem Bericht werden die MwSt.-Klauselbeschreibungen für alle Zeilen im Bericht neben dem MwSt.-Betrag und der MwSt.-Bemessungsgrundlage gedruckt und angezeigt. Wenn eine MwSt.-Klausel nicht für eine oder mehrere Zeilen des Verkaufsbelegs festgelegt wurde, wird der gesamte Abschnitt weggelassen, wenn der Bericht gedruckt wird.

### <a name="to-set-up-vat-clauses"></a>Einrichten von MwSt.-Klauseln

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 9.](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **MWSt.-Klauseln** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **MwSt.-Klauseln** erstellen Sie eine neue Zeile.  
3. Geben Sie im Feld **Code** eine Kennung für die Klausel ein. Nutzen Sie diesen Code, um die Klausel der MwSt-Buchungsgruppe zuzuweisen.  
4. Geben Sie im Feld **Beschreibung** den Text für die Mehrwertsteuerbefreiung ein, den Sie für Belege, die Mehrwertsteuer enthalten können, anzeigen möchten. Geben Sie im Feld **Beschreibung 2** bei Bedarf weiteren Text ein. Der Text wird auf neuen Belegzeilen angezeigt.
5. Wählen Sie die Aktion **Beschreibung nach Dokumenttyp**.
6. Über die **MwSt-Klausel von Doc. Typ** Seite, füllen Sie die Felder aus, um festzulegen, welcher MwSt.-Befreiungstext für welche Dokumentart angezeigt werden soll.  
7. Optional: Um die MwSt-Klausel sofort einem Setup für die Mehrwertsteuerbuchung zuzuordnen, wählen Sie **Einrichtung**, und wählen Sie dann die Klausel. Wenn Sie warten möchten, können Sie die Klausel später auf der Seite **MwSt.-Buchungsmatrix** zuordnen.  
8. Optional: Um zu bestimmen wie die Mehrwertsteuerklausel übersetzt wird, wählen Sie die Aktion **Übersetzungen**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>So weisen Sie eine MwSt.-Klausel einer Buchungsgruppe zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 10.](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **MwSt.-Buchungseinrichtung** ein und wählen Sie dann den entsprechenden Link.  
2. In der Spalte **MwSt.-Klausel** wählen Sie die Klausel, die für jede MwSt.-Buchungseinrichtung gilt.  

### <a name="to-specify-translations-for-vat-clauses"></a>Um Beschreibungen für Mehrwertsteuerklauseln festzulegen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 11.](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **MWSt.-Klauseln** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Übersetzung** aus.  
3. Wählen Sie im Feld **Sprachcode** Sie die Sprache aus, in die Sie übersetzen.  
4. Geben Sie in den Feldern **Beschreibung** und **Beschreibung 2** den Text ein, der eine Übersetzung der Beschreibungen ist. Dieser Text wird in den übersetzten MwSt.-Berichten angezeigt.  

### <a name="to-specify-extended-text-for-vat-clauses"></a>So legen Sie Textbausteine für Mehrwertsteuerklauseln fest

> [!NOTE]  
> Wenn Ihr Land oder Ihre Region einen längeren Text für die MwSt.-Klauseln erfordert, als die Standardversion unterstützt, können Sie den längeren Text für die MwSt.-Klauseln als *Textbaustein* angeben, damit dieser in den Verkaufs- und Einkaufsberichten gedruckt wird.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 11.](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. aus, geben Sie **MWSt.-Klauseln** ein, und wählen Sie dann den entsprechenden Link aus.  
2. Wählen Sie die Aktion **Erweiterte Texte** aus.  
3. Wählen Sie die Aktion **Neu**.  
4. Füllen Sie die Felder **Sprachencode** und **Beschreibung** aus.  
5. Wählen Sie optional das Feld **Alle Sprachcodes** aus, oder geben Sie die entsprechende Sprache im Feld **Sprachcode** an, wenn Sie Sprachcodes verwenden.  
6. Füllen Sie die Felder **Startdatum** und/oder **Enddatum** aus, wenn Sie die Verwendung des Textbausteins zeitlich einschränken möchten.  
7. Geben Sie den Textbaustein für Ihre MwSt.-Klauseln in den Zeilen für **Text** ein.  
8. Wählen Sie die entsprechenden Felder für die Belegtypen aus, deren Textbausteine gedruckt werden sollen.  
9. Schließen Sie die Seite.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Erstellen Sie eine MwSt.-Buchungseinrichtung zur Behandlung der Import-MwSt.

Verwenden Sie die Funktion *Import-MwSt.*, wenn Sie einen Beleg buchen müssen, bei dem der gesamte Betrag aus Mehrwertsteuer besteht. Sie verwenden diese Funktion, wenn Sie eine MwSt.-Rechnung für importierte Waren von der Steuerbehörde erhalten.  

Gehen Sie folgendermaßen vor, um Codes für die Einfuhrsteuerfelder festzulegen:  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 12.](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. aus, geben Sie **Mw.-Produktbuchungsgruppen** ein, und wählen Sie dann den entsprechenden Link aus.  
2. Auf der Seite MwSt Produktbuchungsgruppe richten Sie eine neue MwSt.-Produktbuchungsgruppen für Einfuhrsteuer ein.  
3. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 13.](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. aus, geben Sie **MwSt.-Buchungseinrichtung** ein, und wählen Sie dann den entsprechenden Link aus.  
4. Auf der Seite MwSt Buchungseinrichtung erstellen Sie eine neue Zeile oder nutzen einen bestehende MwSt-Buchungsgruppe in Kombination mit der neuen MwSt.-Produktbuchungsgruppe für die Einfuhrsteuer.  
5. Wählen Sie im Feld **MwSt.-Berechnungsart** **Volle MwSt.** aus.  
6. Geben Sie im Feld **Vorsteuerkonto** das Sachkonto an, auf das Sie Einfuhrumsatzsteuer buchen wollen. Alle anderen Konten sind optional.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countriesregions"></a>Erwerbssteuer für den Handel zwischen EU-Ländern/-Regionen verwenden

Gewisse Unternehmen müssen Erwerbssteuer abführen, wenn Sie Handel mit anderen Ländern innerhalb der EU betreiben. Die Regel gilt beispielsweise für Einkäufe aus EU-Ländern/-Regionen und Verkäufe an EU-Länder/-Regionen.  

> [!NOTE]  
> Diese Regel gilt für den Handel mit Unternehmen, die in einem anderen EU-Land/in einer anderen EU-Region als umsatzsteuerpflichtig registriert sind. Wenn Sie direkt mit Verbrauchern in anderen EU-Ländern/-Regionen Geschäfte tätigen, sollten Sie sich bei den Steuerbehörden über die geltenden Regeln für die MwSt. informieren.  

> [!TIP]  
> Sie können überprüfen, ob ein Unternehmen in einem anderen EU-Land bzw. einer anderen EU-Region als umsatzsteuerpflichtig registriert ist, wenn Sie den EU-MwSt.ID-Nr.-Überprüfungsdienst verwenden. Der Service ist in [!INCLUDE[prod_short](includes/prod_short.md)] kostenlos verfügbar. Weitere Informationen finden Sie unter [Überprüfen von MwSt.-Registrierungsnummern](finance-how-validate-vat-registration-number.md).

### <a name="sales-to-eu-countriesregions"></a>Verkäufe in EU-Ländern/-Regionen

Auf Verkäufe an umsatzsteuerpflichtige Unternehmen in anderen EU-Ländern/-Regionen wird keine MwSt. berechnet. Der Wert derartiger Verkäufe an EU-Länder/-Regionen muss separat auf der MwSt.-Abrechnung ausgewiesen werden.  

Um MwSt. bei Verkäufen in EU-Länder/-Regionen korrekt zu berechnen, gehen Sie folgendermaßen vor:  

* Richten Sie eine Zeile für Verkäufe mit den gleichen Informationen ein, wie zuvor für Einkäufe beschrieben. Wenn im Fenster **MwSt.-Buchungsmatrix Einrichtung** Zeilen für Einkäufe aus EU-Ländern/-Regionen eingerichten, können Sie diese Zeilen auch für Verkäufe verwenden.  
* Weisen Sie die MwSt.-Geschäftsbuchungsgruppen im Feld **MwSt.-Geschäftsbuchungsgruppe** auf dem Inforegister **Fakturierung** der Debitorenkarte jedes EU-Debitors zu. Sie sollten auch die USt-IdNr. des Debitors im Feld **USt-IdNr.** im Inforegister **Außenhandel** eingeben.  

Wenn Sie einen Verkauf an einen Debitor in einem anderen EU-Land/einer anderen EU-Region buchen, berechnet [!INCLUDE [prod_short](includes/prod_short.md)] den MwSt.-Betrag und erstellt einen MwSt.-Posten basierend auf Informationen zur Erwerbssteuer und zur MwSt.-Bemessungsgrundlage. Dieser Betrag wird zur Berechnung des MwSt.-Betrag verwendet. Auf die MwSt.-Konten in der Finanzbuchhaltung werden keine Posten gebucht.

Wenn Sie die Kombination aus MwSt.-Geschäftsbuchungsgruppe und MwSt.-Produktbuchungsgruppe in den regelmäßigen MwSt.-Erklärungen als Dienstleistung aufführen möchten, markieren Sie das Feld **EU-Service**.

> [!NOTE]  
> Das Feld **EU-Service** gilt nur für MwSt.-Berichte. Das Feld steht in keinem Zusammenhang mit den Funktionen **Service-Deklaration** oder **Intrastat für Dienstleistungen** .

## <a name="vat-rounding-for-documents"></a>Mehrwertsteuer-Rundung für Belege

Beträge in Belegen, die nicht gebucht sind, werden gerundet und auf eine Weise angezeigt, die der endgültigen Rundung gebuchter Beträge entspricht. [!INCLUDE [prod_short](includes/prod_short.md)] berechnet die MwSt. für einen vollständigen Beleg. Die MwSt.-Berechnung basiert auf der Summe aller Zeilen mit demselben MwSt.-Kennzeichen im Beleg.  

## <a name="set-up-vat-reporting"></a>MwSt.-Berichte festlegen

Sie müssen Informationen darüber festlegen, wie die Steuerbehörden in Ihrem Land oder Ihrer Region von Ihnen verlangen, MwSt.-Berichte zu senden. Die folgenden Schritte veranschaulichen die am häufigsten verwendeten Informationen. Für Ihr Land oder Ihre Region sind jedoch möglicherweise zusätzliche Schritte erforderlich. Weitere Informationen finden Sie in dem entsprechenden Artikel im Abschnitt *Lokale Funktionen* in der Leiste auf der linken Seite.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## <a name="see-also"></a>Siehe auch

[Vorlagen für Umsatzsteuerabrechnungen und Namen von Umsatzsteuerabrechnungen einrichten](finance-how-setup-vat-statement.md)  
[Nicht realisierte Mehrwertsteuer einrichten](finance-setup-unrealized-vat.md)  
[Meldung der Mehrwertsteuer an eine Steuerbehörde](finance-how-report-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Arbeiten mit dem Tool zur Änderung des MwSt.-Satzes](finance-how-use-vat-rate-change-tool.md)  
[Umsatzsteuer-Identifikationsnummern überprüfen](finance-how-validate-vat-registration-number.md)  
[Lokale Funktion in Business Central](about-localization.md)  
[MwSt.-Berichterstattung in der deutschen Version](LocalFunctionality/Germany/vat-reporting.md)  
[Belgische MwSt](LocalFunctionality/Belgium/belgian-vat.md)  
[Italienische MwSt](LocalFunctionality/Italy/italian-vat.md)  
[Elektronische Mehrwertsteuer- und ICP-Erklärungen in der niederländischen Version einrichten](LocalFunctionality/Netherlands/how-to-set-up-electronic-vat-and-icp-declarations.md)  
[MwSt.-Bericht in der spanischen Version](LocalFunctionality/Spain/vat-reports.md)  
[Waren- und Dienstleistungssteuer-Buchung in der australischen Version einrichten](LocalFunctionality/Australia/how-to-set-up-goods-and-service-tax-posting.md)  
[MwSt. in der tschechischen Version](LocalFunctionality/Czech/finance-vat.md)  
[MwSt.-Abrechnung in der norwegischen Version](LocalFunctionality/Norway/norwegian-vat-reporting.md)  
[Steuern auf Waren und Dienstleistungen und Harmonised Sales Tax in Kanada melden](LocalFunctionality/Canada/sales-tax-goods-services.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
