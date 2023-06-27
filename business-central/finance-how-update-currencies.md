---
title: Währungswechselsätze aktualisieren (enthält Video)
description: 'Wenn Sie Beträge in verschiedenen Währungen erfassen, können Sie sich von Business Central dabei helfen lassen, die Wechselkurse der gebuchten Buchungen mit einem externen Dienst anzupassen.'
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: edupont
---
# <a name="update-currency-exchange-rates" />Währungswechselkurse aktualisieren

Sie können verschiedene Währungen in [!INCLUDE [prod_short](includes/prod_short.md)] definieren, wenn Sie beispielsweise in anderen Währungen als Ihrer Landeswährung handeln. Damit Sie die Änderungen der Wechselkurse verfolgen können, können Sie die Währungen manuell verwalten oder einen Wechselkursdienst einrichten.

## <a name="currencies" />Währungen

> [!TIP]  
> Wenn Sie in [!INCLUDE[prod_short](includes/prod_short.md)] nach Echtzeitinformationen zu Wechselkursen (FX) oder älteren Kursen suchen, werden diese als Währung bezeichnet. Siehe neben diesem Artikel auch [Einrichten einer zusätzlichen Berichtswährung](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Sie geben die Währungscodes in der Liste **Währungen** an, darunter zusätzliche Informationen und Einstellungen, die für jeden Währungscode erforderlich sind. Weitere Informationen finden Sie unter [Währungen](finance-set-up-currencies.md#curr)

### <a name="example-of-a-receivable-currency-transaction" />Beispiel für eine ausstehende Währungstransaktion

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="exchange-rates" />Wechselkurse

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

## <a name="adjusting-exchange-rates" />Regulieren von Wechselkursen

Da sich Wechselkurse ständig ändern, müssen weitere Währungsentsprechungen im System in regelmäßigen Abständen reguliert werden. Werden diese Regulierungen nicht durchgeführt, sind Beträge, die aus fremden (oder zusätzlichen) Währungen umgerechnet und in der Mandantenwährung in der Finanzbuchhaltung gebucht wurden, möglicherweise irreführend. Darüber hinaus müssen Tagesposten, die vor der Eingabe eines Tageswechelkurses in der Anwendung gebucht werden, aktualisiert werden, nachdem der Tageswechselkurs eingegeben wurde.

Der Batchauftrag **Wechselkurse anpassen** wird verwendet, um die Wechselkurse von gebuchten Debitor-, Kreditor- und Bankkonten-Buchungen manuell anzupassen. Berichtswährungsbeträge in Sachposten können hiermit ebenfalls aktualisiert werden.  

> [!TIP]
> Sie können einen Dienst verwenden, um Wechselkurse im System automatisch zu regulieren. Weitere Informationen finden Sie unter [So richten Sie einen Währungswechselkurs-Service ein](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Die Wechselkurse für bereits gebuchte Transaktionen werden hierdurch jedoch nicht reguliert. Um Wechselkurse für gebuchte Einträge zu regulieren, verwenden Sie die Stapelverarbeitung **Wechselkurse regulieren**.

Sie können eine Vorschau der Auswirkungen einer Anpassung auf die Buchung erstellen, bevor Sie tatsächlich buchen, indem Sie **Vorschau** auf der Seite **Wechselkurse** wählen. Außerdem können Sie auswählen, ob die Buchung im Hauptbuch detailliert (pro Buchung) oder zusammengefasst (pro Währung) erfolgen soll, indem Sie **Buchungen zusammenfassen** wählen. Sie können auch festlegen, wie die Dimensionen für Buchungen von nicht realisierten Gewinnen und Verlusten behandelt werden sollen, indem Sie eine der folgenden Optionen im Feld **Dimensionswerte übertragen** wählen:  

- **Quellenbuchung**: Bei Sachbuchungen für nicht realisierte Gewinne und Verluste werden Dimensionswerte aus der angepassten Buchung übernommen.
- **Nach Sachkonto**: Bei Sachkontoeinträgen für nicht realisierte Gewinne und Verluste werden die Dimensionswerte aus dem Quelleneintrag für die Dimensionseinstellungen des Sachkontos für nicht realisierte Gewinne und Verluste übernommen.
- **Keine Übertragung**: Sachbucheinträge für nicht realisierte Gewinne und Verluste haben keine Dimensionswerte.

### <a name="effect-on-customers-and-vendors" />Auswirkung auf Debitoren und Kreditoren

Für Debitoren- und Kreditorenkonten reguliert der Batchauftrag die Währung unter Verwendung des Wechselkurses, der zum Zeitpunkt des im Batchauftrag angegebenen Buchungsdatums gültig ist. Die Stapelverarbeitung berechnet die Differenzen für die einzelnen Währungssalden und bucht die Beträge auf das Sachkonto, das im Feld **Kursgewinn unrealisiert Kto.** oder im Feld **Kursverlust unrealisiert Kto.** auf der Seite **Währungen** angegeben ist. Gegenposten werden automatisch auf die Debitoren- und Kreditorensammelkonten in der Finanzbuchhaltung gebucht.

Die Stapelverarbeitung bearbeitet alle offenen Debitoren- und Kreditorenposten. Wenn es eine Wechselkursdifferenz für eine Buchung gibt, erstellt der Batchauftrag einen neuen detaillierten Debitoren- oder Kreditoren-Sachkonto-Eintrag, der den angepassten Betrag auf dem Debitoren- oder Kreditoren-Sachkonto-Eintrag wiedergibt.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries" />Dimensionen in Debitoren- und Kreditorenposten

Den Differenzposten werden die Dimensionen von den Debitoren-/Kreditorenposten zugewiesen. Die Differenzen werden pro Kombination von Dimensionswerten gebucht.

### <a name="effect-on-bank-accounts" />Auswirkungen auf Bankkonten

Für Bankkonten reguliert der Batchauftrag die Währung unter Verwendung des Wechselkurses, der zum Zeitpunkt des im Batchauftrag angegebenen Buchungsdatums gültig ist. Die Stapelverarbeitung berechnet die Differenzen für jedes Bankkonto mit einem Währungscode und bucht die Beträge auf das Sachkonto, das im Feld **Kursgewinn realisiert Kto.** oder im Feld **Kursverlust realisiert Kto.** der Tabelle **Währungen** angegeben ist. Gegenposten werden automatisch auf die Banksachkonten gebucht, die in den Bankkontenbuchungsgruppen angegeben sind. Die Stapelverarbeitung erzeugt einen Posten pro Währung pro Buchungsgruppe.

#### <a name="dimensions-on-bank-account-entries" />Dimensionen in Bankposten

Den Differenzposten für das Sachkonto des Bankkontos und für das Gewinn- und Verlustkonto werden die Vorgabedimensionen des Bankkontos zugewiesen.

### <a name="effect-on-gl-accounts" />Auswirkungen auf Sachkonten
Wenn Sie in einer Berichtswährung buchen, kann die Stapelverarbeitung neue Sachposten für Wechselkursregulierungen zwischen Mandantenwährung und Berichtswährung erstellen. Die Stapelverarbeitung berechnet die Differenzen für jeden Sachposten und reguliert den Sachposten abhängig vom Inhalt des Felds **Kursregulierung** für jedes Sachkonto.

##### <a name="dimensions-on-gl-account-entries" />Dimensionen in Sachposten
Den Differenzposten werden die Vorgabedimensionen der Konten zugewiesen, auf die sie gebucht werden.

> [!Important]
> Bevor Sie den Batchauftrag aufrufen können, müssen Sie die Wechselkurse eingeben, die zum Regulieren der Fremdwährungssalden verwendet werden. Dies erfolgt auf der Seite **Währungswechselkurse**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service" />So richten Sie einen Währungswechselkurs-Service ein
Sie können einen externen Service verwenden, um Ihre Währungswechselkurse wie FloatRates auf dem neuesten Stand zu halten. 

> [!NOTE]
> Die meisten Wechselkursdienste stellen Daten bereit, die mit dem Importprozess in [!INCLUDE[prod_short](includes/prod_short.md)] kompatibel sind. Manchmal sind die Daten jedoch anders formatiert, und Sie müssen Ihren Importvorgang anpassen. Sie können dazu das Datenaustauschframework verwenden, indem Sie Ihre eigene Codeunit hinzufügen. Dazu benötigen Sie wahrscheinlich die Hilfe eines Entwicklers. Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Währungswechselkurs-Dienste** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie auf der Seite **Währungswechselkurs-Service** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Aktivieren Sie das Kontrollkästchen **Aktiviert**, um den Dienst zu aktivieren.

> [!NOTE]
> Das folgende Video zeigt ein Beispiel für die Verbindung zu einem Wechselkursdienst am Beispiel der Europäischen Zentralbank. In dem Abschnitt, der das Einrichten von Feldzuordnungen beschreibt, gibt die Einstellung in der Spalte **Quelle** für die Option **Übergeordneter Knoten für Währungscode** nur die erste gefundene Währung zurück. Die Einstellung sollte auf `/gesmes:Envelope/Code/Code/Code` festgelegt sein.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service" />Um Währungswechselkurse über einen Service zu aktualisieren
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Währungen** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die **Aktualisieren von Wechselkursen** Aktion aus.

Der Wert im Feld **Wechselkurs** wird auf der Seite **Währung** mit dem aktuellen Währungswechselkurs aktualisiert.

## <a name="see-related-microsoft-training" />Siehe verwandte [Microsoft Schulungen](/training/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Währungen in Business Central](finance-currencies.md)  
[Einrichten von Währungen](finance-set-up-currencies.md)  
[Einrichten einer zusätzlichen Berichtswährung](finance-how-setup-additional-currencies.md)  
[Jahre und Perioden abschließen](year-close-years-periods.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
