---
title: Währungswechselsätze aktualisieren (enthält Video)
description: 'Wenn Sie Beträge in verschiedenen Währungen erfassen, können Sie sich von Business Central dabei helfen lassen, die Wechselkurse anzupassen.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 09/07/2023
ms.author: bholtorf
---
# <a name="update-currency-exchange-rates"></a>Währungswechselkurse aktualisieren

Sie können verschiedene Währungen in [!INCLUDE [prod_short](includes/prod_short.md)] definieren, wenn Sie beispielsweise in anderen Währungen als Ihrer Landeswährung handeln. Um Änderungen der Wechselkurse zu verfolgen, können Sie die Kurse manuell verwalten oder einen Wechselkursdienst einrichten.

## <a name="currencies"></a>Währungen

> [!TIP]  
> Wenn Sie in [!INCLUDE[prod_short](includes/prod_short.md)] nach Echtzeitinformationen zu Wechselkursen (FX) oder älteren Kursen suchen, werden diese als Währung bezeichnet. Siehe neben diesem Artikel auch [Einrichten einer zusätzlichen Berichtswährung](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Sie geben die Währungscodes in der Liste **Währungen** an, darunter zusätzliche Informationen und Einstellungen, die für jeden Währungscode erforderlich sind. Weitere Informationen finden Sie unter [Währungen](finance-set-up-currencies.md#curr)

### <a name="example-of-a-receivable-currency-transaction"></a>Beispiel für eine ausstehende Währungstransaktion

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="exchange-rates"></a>Wechselkurse

Die Wechselkurse sind das Werkzeug, um die Mandantenwährung (MW) jeder Währungstransaktion zu berechnen. Die Seite **Wechselkurse** enthält die folgenden Felder:

|Feld|Beschreibung|  
|---------------------------------|---------------------------------------|  
|**Startdatum**|Das Datum, an dem der Wechselkurs angewendet wurde|  
|**Währungscode**|Der Währungscode, der sich auf diesen Wechselkurs bezieht|  
|**Bezug auf Währungscode**|Wenn diese Währung Teil der Berechnung einer Dreieckswährung ist, kann der zugehörige Währungscode hier eingerichtet werden.|  
|**Wechselkursbetrag**|Der Wechselkursbetrag ist der Wechselkurs, der für den in der Zeile ausgewählten Währungscode verwendet wird. Normalerweise 1 oder 100|  
|**Bezug auf Wechselkursbetrag**|Der Bezug auf den Wechselkursbetrag bezieht sich auf den Wechselkurs, der für den Bezug auf den Währungscode verwendet wird.|  
|**Regulierung Wechselkursbetrag**|Der Betrag der Wechselkursregulierung ist der Kurs, der für den in der Zeile ausgewählten Währungscode für die Verwendung der Stapelverarbeitung **Wechselkurse regulieren** verwendet werden soll.|  
|**Bez. a. Reg. Wechselkursbetrag**|Der Bezug auf die Regulierung des Wechselkursbetrags ist der Kurs, der für den in der Zeile ausgewählten Währungscode für die Verwendung der Stapelverarbeitung **Wechselkurse regulieren** verwendet werden soll.|  
|**Fester Wechselkursbetrag**|Legt fest, ob Währungswechselkurse auf Rechnungs- und Buch.-Blattzeilen geändert werden können.|  

Im Allgemeinen werden die Werte der Felder **Wechselkursbetrag** und **Relationaler Wechselkursbetrag** als Standardwährungskurs für alle neu erstellten Forderungs- und Verbindlichkeitsbelege verwendet. Dem Beleg wird der Währungskurs gemäß dem aktuellen Arbeitstag zugeordnet.  

> [!Note]
> Der tatsächliche Wechselkurs wird mit dieser Formel berechnet:
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

Der Betrag des Anpassungs-Wechselkurses oder der Betrag des relationalen Anpassungs-Wechselkurses wird verwendet, um alle offenen Bank-, Debitoren- oder Kreditoren-Transaktionen zu aktualisieren.  

> [!Note]
> Der tatsächliche Wechselkurs wird mit dieser Formel berechnet:
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## <a name="adjusting-exchange-rates"></a>Wechselkurse regulieren

Da die Wechselkurse ständig schwanken, müssen Sie andere Währungsäquivalente periodisch anpassen. Wenn Sie dies nicht tun, können Beträge, die Sie aus Fremdwährungen (oder anderen Währungen) umgerechnet und in der lokalen Währung in das Hauptbuch gebucht haben, falsch sein. Außerdem müssen Sie die gebuchten Tageseinträge aktualisieren, bevor Sie einen täglichen Wechselkurs eingeben.

Der Batchauftrag **Wechselkurse anpassen** wird verwendet, um die Wechselkurse von gebuchten Debitor-, Kreditor- und Bankkonten-Buchungen manuell anzupassen. Der Batch-Job kann auch andere Berichtswährungsbeträge auf Sachbuchungen aktualisieren.  

> [!TIP]
> Sie können einen Dienst verwenden, um Wechselkurse im System automatisch zu regulieren. Weitere Informationen finden Sie unter [So richten Sie einen Währungswechselkurs-Service ein](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Die Wechselkurse für bereits gebuchte Transaktionen werden hierdurch jedoch nicht reguliert. Um Wechselkurse für gebuchte Einträge zu regulieren, verwenden Sie die Stapelverarbeitung **Wechselkurse regulieren**.

Sie können auch festlegen, wie die Dimensionen für Buchungen von nicht realisierten Gewinnen und Verlusten behandelt werden sollen, indem Sie eine der folgenden Optionen im Feld **Dimensionsbuchung** wählen:  

* **Quellpostendimensionen**: Übernehmen Sie Dimensionswerte für Sachbuchungen für nicht realisierte Gewinne und Verluste aus der Buchung, die Sie anpassen.  
* **Keine Dimensionen**: Übertragen Sie keine Dimensionswerte für nicht realisierte Gewinne und Verluste in Sachbuchungen. [!INCLUDE [prod_short](includes/prod_short.md)] verwendet weiterhin Standard-Dimensionseinstellungen, zum Beispiel **Code obligatorisch**, **Gleicher Code** oder **Kein Code**. Wenn die Quelltransaktionseinträge Dimensionswerte aufweisen, werden durch die Anpassung Einträge ohne Dimensionswerte erstellt.  
* **Sachkontodimensionen**: Übertragen Sie Dimensionswerte aus dem Quelleintrag der Dimensionseinstellungen des Sachkontos für nicht realisierte Gewinne und Verluste in Sachbucheinträge.

> [!NOTE]
> Um die Vorschaufunktion nutzen zu können, müssen Sie das **Funktionsupdate aktivieren: Aktivieren Sie die Verwendung der neuen erweiterbaren Wechselkursanpassung, einschließlich der Funktion zur Veröffentlichungsüberprüfung** auf der Seite **[Funktionsverwaltung](https://businesscentral.dynamics.com/?page=2610)**.

> [!IMPORTANT]
> Aufgrund lokaler Anforderungen in der Schweiz empfehlen wir Ihnen nicht, **Funktionsaktualisierung: Nutzung der neuen erweiterbaren Wechselkursanpassung, einschließlich Buchungsüberprüfung** in der Landesversion der Schweiz (CH) zu aktivieren.

## <a name="preview-the-effect-of-an-adjustment"></a>Sehen Sie sich die Auswirkungen einer Anpassung in der Vorschauversion an

Sie können die Auswirkungen einer Wechselkursanpassung auf die Buchung vor der eigentlichen Buchung in einer Vorschauversion anzeigen, indem Sie die Aktion **Buchungsvorschau** auf der Anforderungsseite **Wechselkursanpassung** auf der Anforderungsseite des Berichts (Bericht 596) wählen. Auf der Anfrageseite können Sie angeben, was in die Vorschau aufgenommen werden soll:

* Detaillierte Buchung im Hauptbuch nach Eintrag
* Erhalten Sie eine zusammengefasste Buchung nach Währung. Wählen Sie einfach das Feld **Pro Posten regulieren** im **Wechselkursanpassung**-Bericht.

### <a name="effect-on-customers-and-vendors"></a>Auswirkung auf Debitoren und Kreditoren

Für Debitoren- und Kreditorenkonten verwendet der Batch-Job den Wechselkurs, der am für den Batch-Job angegebenen Buchungsdatum gültig war, um die Währung anzupassen. Die Stapelverarbeitung berechnet die Differenzen für die einzelnen Währungssalden und bucht die Beträge auf das Sachkonto, das im Feld **Kursgewinn unrealisiert Kto.** oder im Feld **Kursverlust unrealisiert Kto.** auf der Seite **Währungen** angegeben ist. Gegenposten werden automatisch auf die Debitoren- und Kreditorensammelkonten in der Finanzbuchhaltung gebucht.

Die Stapelverarbeitung bearbeitet alle offenen Debitoren- und Kreditorenposten. Wenn es eine Wechselkursdifferenz für eine Buchung gibt, erstellt der Batchauftrag einen neuen detaillierten Debitoren- oder Kreditoren-Sachkonto-Eintrag. Der neue Eintrag spiegelt den angepassten Betrag im Debitoren- oder Kreditorenbucheintrag wider.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensionen in Debitoren- und Kreditorenposten

[!INCLUDE [prod_short](includes/prod_short.md)] ordnet die Dimensionen aus den Debitoren- oder Kreditorenbucheinträgen den Korrekturbuchungen zu und bucht Korrekturen für jede Kombination von Dimensionswerten.

### <a name="effect-on-bank-accounts"></a>Auswirkungen auf Bankkonten

Für Bankkonten reguliert der Batchauftrag die Währung unter Verwendung des Wechselkurses, der zum Zeitpunkt des im Batchauftrag angegebenen Buchungsdatums gültig ist. Die Stapelverarbeitung berechnet die Differenzen für jedes Bankkonto mit einem Währungscode und bucht die Beträge auf das Sachkonto, das im Feld **Kursgewinn realisiert Kto.** oder im Feld **Kursverlust realisiert Kto.** der Tabelle **Währungen** angegeben ist. Gegenposten werden automatisch auf die Banksachkonten gebucht, die in den Bankkontenbuchungsgruppen angegeben sind. Die Stapelverarbeitung erzeugt einen Posten pro Währung pro Buchungsgruppe.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensionen in Bankposten

Den Differenzposten für das Sachkonto des Bankkontos und für das Gewinn- und Verlustkonto werden die Vorgabedimensionen des Bankkontos zugewiesen.

### <a name="effect-on-gl-accounts"></a>Auswirkungen auf Sachkonten

Wenn Sie in einer anderen Berichtswährung buchen, kann die Stapelverarbeitung neue Sachposten für Wechselkursregulierungen zwischen lokaler Währung und anderer Berichtswährung erstellen. Die Stapelverarbeitung berechnet die Differenzen für jeden Sachposten und reguliert den Sachposten abhängig vom Inhalt des Felds **Kursregulierung** für jedes Sachkonto.

#### <a name="dimensions-on-gl-account-entries"></a>Dimensionen in Sachposten

Den Differenzposten werden die Vorgabedimensionen der Konten zugewiesen, auf die sie gebucht werden.

> [!Important]
> Bevor Sie den Batchauftrag aufrufen können, müssen Sie die Wechselkurse eingeben, die zum Regulieren der Fremdwährungssalden verwendet werden. Dies erfolgt auf der Seite **Währungswechselkurse**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>So richten Sie einen Währungswechselkurs-Service ein

Sie können einen externen Service verwenden, um Ihre Währungswechselkurse wie FloatRates auf dem neuesten Stand zu halten. 

> [!NOTE]
> Die meisten Wechselkursdienste stellen Daten bereit, die mit dem Importprozess in [!INCLUDE[prod_short](includes/prod_short.md)] kompatibel sind. Manchmal sind die Daten jedoch anders formatiert, und Sie müssen Ihren Importvorgang anpassen. Sie können dazu das Datenaustauschframework verwenden, indem Sie Ihre eigene Codeunit hinzufügen. Dazu benötigen Sie wahrscheinlich die Hilfe eines Entwicklers. Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Währungswechselkurs-Dienste** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie auf der Seite **Währungswechselkurs-Service** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Aktivieren Sie das Kontrollkästchen **Aktiviert**, um den Dienst zu aktivieren.

> [!NOTE]
> Das folgende Video zeigt ein Beispiel für die Verbindung zu einem Wechselkursdienst am Beispiel der Europäischen Zentralbank. In dem Abschnitt, der das Einrichten von Feldzuordnungen beschreibt, gibt die Einstellung in der Spalte **Quelle** für die Option **Übergeordneter Knoten für Währungscode** nur die erste gefundene Währung zurück. Die Einstellung sollte auf `/gesmes:Envelope/Code/Code/Code` festgelegt sein.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Um Währungswechselkurse über einen Service zu aktualisieren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Währungen** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die **Aktualisieren von Wechselkursen** Aktion aus.

Der Wert im Feld **Wechselkurs** wird auf der Seite **Währung** mit dem aktuellen Währungswechselkurs aktualisiert.

## <a name="see-also"></a>Siehe auch

[Währungen in Business Central](finance-currencies.md)  
[Einrichten von Währungen](finance-set-up-currencies.md)  
[Berichtswährung einrichten](finance-how-setup-additional-currencies.md)  
[Jahre und Perioden abschließen](year-close-years-periods.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
