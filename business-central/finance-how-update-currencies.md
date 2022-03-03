---
title: Währungswechselsätze aktualisieren (enthält Video)
description: Verfolgen Sie Beträge in verschiedenen Währungen mithilfe der Währungscodes, und lassen Sie mithilfe von Business Central die Wechselkurse der gebuchte Posten mit einer Fremdleistung anpassen.
author: SorenGP
ms.topic: conceptual
ms.search.keywords: multiple currencies, adjust exchange rates, FX rates
ms.search.form: 5, 118
ms.date: 02/17/2022
ms.author: edupont
ms.openlocfilehash: 04f96b269b842045c1a804f976ffddfd5348befc
ms.sourcegitcommit: 75a388b1d8917e2bbd49398ef76cf86cf37e6767
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323266"
---
# <a name="update-currency-exchange-rates"></a>Währungswechselkurse aktualisieren

Da die Anzahl der Länder, in denen Unternehmen Geschäftsbeziehungen unterhalten, wächst, wird es unerlässlich, dass Finanzdaten in mehreren Währungen erfasst und angezeigt werden können. Die lokale Währung (LCY) ist auf der Seite **Hauptbucheinrichtung** definiert, wie im Artikel [Finanzen einrichten](finance-setup-finance.md) beschrieben. Sobald die Mandantenwährung (MW) definiert wurde, wird sie als leere Währung dargestellt. Wenn das Feld **Währung** also leer ist, bedeutet dies, dass es sich um MW handelt.  

Als Nächstes müssen Sie Währungscodes für jede Währung einrichten, die Sie verwenden, wenn Sie in anderen Währungen als Ihrer lokalen Währung (LCY) kaufen oder verkaufen. Auch Bankkonten können mit Währungen erstellt werden. Es ist möglich, Sachtransaktionen in verschiedenen Währungen zu erfassen, diese werden jedoch immer in der Mandantenwährung (MW) gebucht.

> [!Important]
> Erstellen Sie den Mandantenwährungscode nicht im **Hauptbucheinrichtung** und auf der Seite **Währungen**. Dies führt zu Verwechslungen zwischen der leeren Währung und dem MW-Code in der Währungstabelle. Außerdem können versehentlich Bankkonten, Debitoren oder Kreditoren erstellt werden, einige mit der leeren Währung und andere mit dem LCY-Code.

Ihre Finanzbuchhaltung wird in der Mandantenwährung (MW) eingerichtet. Sie können sie jedoch auch für die Verwendung einer anderen Währung einrichten, der Sie einen Währungswechselkurs zuweisen. Wird eine zweite Währung als [!INCLUDE[prod_short](includes/prod_short.md)] Berichtswährung festgelegt, werden Beträge automatisch für jeden Sachposten und weitere Posten, wie zum Beispiel MwSt.-Posten, in der Mandantenwährung und der Berichtswährung erfasst. Weitere Informationen finden Sie unter [Zusätzliche Berichtswährung einrichten](finance-how-setup-additional-currencies.md). Die Berichtswährung wird am häufigsten verwendet, um die Finanzberichterstellung für Eigentümer zu erleichtern, die in Ländern/Regionen ansässig sind, die andere Währungen als die Mandantenwährung (MW) verwenden.  

> [!IMPORTANT]
> Wenn Sie eine zusätzliche Berichtswährung für die Finanzberichterstattung verwenden wollen, vergewissern Sie sich, dass Sie die Einschränkungen verstehen. Weitere Informationen finden Sie unter [Zusätzliche Berichtswährung einrichten](finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Wenn Sie mit einem Währungscode auf Sachkonten buchen, z. B. um einen Aufwand in einem FibuBuch.-Blatt mit einem Währungscode buchen, wird die Transaktion mit dem Wechselkurs des Buchungsdatums in MW umgerechnet. Der Sachposten enthält keine Informationen darüber, welche Währung verwendet wurde, sondern nur deren Wert in MW. Wenn Sie die ursprüngliche Währung verfolgen möchten, z. B. für eine Rechnung, müssen Sie die Verkaufs- und Einkaufsbeleg sowie Bankkonten verwenden, die Währungscodeinformationen für die Einträge speichern.

## <a name="currencies"></a>Währungen

> [!NOTE]  
> Wenn Sie in [!INCLUDE[prod_short](includes/prod_short.md)] nach Echtzeitinformationen zu Wechselkursen (FX) oder älteren Kursen suchen, werden diese als Währung bezeichnet. Siehe neben diesem Artikel auch [Einrichten einer zusätzlichen Berichtswährung](finance-how-setup-additional-currencies.md).

Sie geben die Währungscodes unter **Währungen** an, darunter zusätzliche Informationen und Einstellungen, die für jeden Währungscode erforderlich sind.

> [!TIP]
> Erstellen Sie die Währungen mit dem internationalen ISO-Code als Code, um die Arbeit mit der Währung in Zukunft zu vereinfachen.

|Feld|Beschreibung|  
|---------------------------------|---------------------------------------|  
|**Code**|Die Kennung für die Währung.|
|**Beschreibung**|Eine Freitextbeschreibung der Währung.|
|**ISO-Code**|Der internationale aus drei Buchstaben bestehende Code für die in ISO 4217 definierte Währung.|
|**Numerischer ISO-Code**|Die internationale numerische Referenz für die in ISO 4217 definierte Währung.|
|**Datum des Wechselkurses**|Das letzte tatsächliche Wechselkursdatum.|
|**EWU-Währung**|Gibt an, ob die Währung eine EWU-Währung (Wirtschafts- und Währungsunion) ist, z. B. EUR.|
|**Kursgewinn realisiert Konto**|Das Konto, auf dem der tatsächliche Gewinn gebucht wird, wenn Sie Zahlungen für Forderungen erhalten oder den tatsächlichen Wechselkurs für Zahlungen an Verbindlichkeiten registrieren. Ein Beispiel für eine ausstehende Währungstransaktion finden Sie im Beispiel unter dieser Tabelle. |
|**Kursverlust realisiert Konto**|Das Konto, auf dem der tatsächliche Verlust gebucht wird, wenn Sie Zahlungen für Forderungen erhalten oder den tatsächlichen Wechselkurs für Zahlungen an Verbindlichkeiten registrieren. Ein Beispiel für eine ausstehende Währungstransaktion finden Sie im Beispiel unter dieser Tabelle. |
|**Kursgewinn unrealisiert Konto**|Das Konto, auf dem der theoretische Gewinn gebucht wird, wenn Sie eine Währungsanpassung durchführen.|
|**Kursverlust unrealisiert Konto**|Das Konto, auf dem der theoretische Verlust gebucht wird, wenn Sie eine Währungsanpassung durchführen.|
|**Betragsrundungspräzision**|Einige Währungen haben andere Formate für Rechnungsbeträge als auf der Seite **Finanzbuchhaltung Einrichtung** definiert. Wenn Sie die Betragsrundungspräzision für eine Währung ändern, werden alle Rechnungsbeträge in dieser Währung mit der aktualisierten Genauigkeit gerundet.|
|**Betragsdezimalstellen**|Einige Währungen haben andere Formate für Rechnungsbeträge als auf der Seite **Finanzbuchhaltung Einrichtung** definiert. Wenn Sie die Betragsdezimalstellen für eine Währung ändern, werden alle Rechnungsbeträge in der Währung mit den aktualisierten Dezimalstellen gerundet.|
|**Rechnungsrundungsart**|Gibt die zu verwendende Methode an, wenn die Beträge gerundet werden müssen. Die Optionen lauten **Kaufmännisch**, **Aufrunden** und **Abrunden**.|
|**Stückpreisrundungspräzision**|Einige Währungen haben andere Formate für Stückpreise als auf der Seite **Finanzbuchhaltung Einrichtung** definiert. Wenn Sie die Stückpreisrundungspräzision für eine Währung ändern, werden alle Stückpreise in der Währung mit der aktualisierten Genauigkeit gerundet.|
|**Stückpreisdezimalstellen**|Einige Währungen haben andere Formate für Stückpreise als auf der Seite **Finanzbuchhaltung Einrichtung** definiert. Wenn Sie die Stückpreisdezimalstellen für eine Währung ändern, werden alle Stückpreise in der Währung mit den aktualisierten Dezimalstellen gerundet.|
|**Ausgl. Rundungspräzision**|Gibt die Intervallgröße an, innerhalb deren Grenzen Rundungsdifferenzen erlaubt sind, wenn mit einem Posten in dieser Währung ein Posten in einer anderen Währung ausgeglichen werden soll.|
|**Konvertierungs-MW-Rundung. Sollkonto**|Gibt Konvertierungsinformationen an, die auch ein Sollkonto enthalten müssen, wenn Sie Korrekturzeilen für Rundungsdifferenzen in Fibu-Buch.-Blattzeilen mit der Aktion **Rundungszeilen f. MW-Konvertierung einfügen** einfügen möchten.|
|**Konvertierungs-MW-Rundung. Habenkonto**|Gibt Konvertierungsinformationen an, die auch ein Habenkonto enthalten müssen, wenn Sie Korrekturzeilen für Rundungsdifferenzen in Fibu-Buch.-Blattzeilen mit der Aktion **Rundungszeilen f. MW-Konvertierung einfügen** einfügen möchten.|
|**Reguliert am**|Das Datum der letzten Währungsanpassung.|
|**Korrigiert am**|Das Änderungsdatum der Einrichtung der Währung.|
|**Zahlungstoleranz %**|Die maximale Zahlungstoleranz in %, die für diese Währung festgelegt wurde. Weitere Informationen finden Sie unter [Zahlungstoleranz und Skontotoleranz](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Max. Zahlungstoleranzbetrag**|Der maximale Zahlungstoleranzbetrag, der für diese Währung festgelegt wurde. Weitere Informationen finden Sie unter [Zahlungstoleranz und Skontotoleranz](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Währungsfaktor**|Legt die Beziehung zwischen der Berichtswährung und der Mandantenwährung mit dem tatsächlichen Währungskurs fest.|
|**Sachkto. Kursgewinn real. Kto.**|Gibt das Sachkonto an, mit dem Wechselkursgewinne für Wechselkursregulierungen zwischen der Mandantenwährung (MW) und der Berichtswährung gebucht werden sollen. Die Wechselkursgewinne werden berechnet, wenn die Stapelverarbeitung „Wechselkurse regulieren“ ausgeführt wird, um Sachkonten zu regulieren. Dieses Feld ist möglicherweise standardmäßig nicht sichtbar. Sie kann durch Personalisierung der Seite abgerufen werden.|
|**Sachkto. Kursverlust real. Kto**|Gibt das Sachkonto an, mit dem Wechselkursverluste für Wechselkursregulierungen zwischen der Mandantenwährung (MW) und der Berichtswährung gebucht werden sollen. Die Wechselkursgewinne werden berechnet, wenn die Stapelverarbeitung „Wechselkurse regulieren“ ausgeführt wird, um Sachkonten zu regulieren. Dieses Feld ist möglicherweise standardmäßig nicht sichtbar. Sie kann durch Personalisierung der Seite abgerufen werden.|
|**Differenzkonto Gewinn**|Gibt das Sachkonto an, mit dem Rundungsgewinne (Rundungsdifferenzen) gebucht werden, wenn eine Berichtswährung im Finanzbuchhaltungsbereich verwendet wird. Dieses Feld ist möglicherweise standardmäßig nicht sichtbar. Sie kann durch Personalisierung der Seite abgerufen werden.|
|**Differenzkonto Verlust**|Gibt das Sachkonto an, mit dem Rundungsverluste (Rundungsdifferenzen) gebucht werden, wenn eine Berichtswährung im Finanzbuchhaltungsbereich verwendet wird. Dieses Feld ist möglicherweise standardmäßig nicht sichtbar. Sie kann durch Personalisierung der Seite abgerufen werden.|
|**Max. MwSt.-Differenz zulässig**|Der Höchstbetrag für MwSt.-Differenzen in dieser Währung. Weitere Informationen finden Sie unter [MwSt.-Beträge in Verkaufs- und Einkaufsbelegen manuell korrigieren](finance-work-with-vat.md#correcting-vat-amounts-manually-in-sales-and-purchase-documents). Dieses Feld ist möglicherweise standardmäßig nicht sichtbar. Sie kann durch Personalisierung der Seite abgerufen werden.|
|**MwSt.-Rundungsmethode**|Gibt die Rundungsmethode für die manuelle Korrektur von MwSt.-Beträgen in Verkaufs- und Einkaufsbelegen an. Dieses Feld ist möglicherweise standardmäßig nicht sichtbar. Sie kann durch Personalisierung der Seite abgerufen werden.|

### <a name="example-of-a-receivable-currency-transaction"></a>Beispiel für eine ausstehende Währungstransaktion

Wenn Sie eine Rechnung von einer Firma in einer Fremdwährung erhalten, ist es relativ einfach, den Wert der Rechnung in lokaler Währung (LCY) auf der Grundlage des heutigen Wechselkurses zu berechnen. Allerdings ist die Rechnung oft mit Zahlungsbedingungen versehen, sodass Sie die Zahlung auf ein späteres Datum verschieben können, was einen potenziell anderen Währungssatz impliziert. Dieses Problem in Kombination mit der Tatsache, dass die Bankwährungskurse immer von den offiziellen Währungskursen abweichen, macht es unmöglich, den genauen Betrag in lokaler Währung (LCY) vorherzusagen, der zur Deckung der Rechnung erforderlich ist. Wenn sich das Fälligkeitsdatum der Rechnung in den nächsten Monat erstreckt, müssen Sie möglicherweise auch den Betrag in Hauswährung (LCY) am Ende des Monats neu bewerten. Die Währungsanpassung ist notwendig, weil der neue LCY-Wert, der zur Deckung des Rechnungsbetrags erforderlich ist, anders sein könnte und sich die Schulden der Firma gegenüber dem Kreditor möglicherweise geändert haben. Der neue LCY-Betrag kann höher oder niedriger sein als der vorherige Betrag und stellt daher einen Gewinn oder einen Verlust dar. Da die Rechnung jedoch noch nicht bezahlt wurde, wird der Gewinn oder Verlust als *unrealisiert* betrachtet. Später wird die Rechnung bezahlt, und die Bank hat sich mit dem tatsächlichen Satz für die Zahlung zurückgemeldet. Erst jetzt wird der *realisierte* Gewinn oder Verlust berechnet. Dieser nicht realisierte Gewinn oder Verlust wird dann storniert und stattdessen wird der realisierte Gewinn oder Verlust gebucht.

Im folgenden Beispiel geht am 1. Januar eine Rechnung mit dem Währungsbetrag von 1000 ein. Zu diesem Zeitpunkt beträgt der Währungssatz 1,123.

|Datum|Aktion|Währungsbetrag|Belegkurs|MW-Betrag auf Beleg|Regulierungsrate|Unrealisierter Kursgewinn|Zahlungskurs|Realisierter Kursverlust|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Fakturieren**|1000|1,123|1123|||||
|1/31|**Regulierung**|1000||1125|1,125|2|||
|2/15|**Anpassungsrücksetzung bei Zahlung**|1000||||-2|||
|2/15|**Zahlung**|1000||1120|||1,120|-3|

Am Ende des Monats wird eine Währungsanpassung durchgeführt, bei der der Anpassungswährungskurs auf 1,125 festgelegt wurde, was einen nicht realisierten Gewinn von 2 auslöst.

Zum Zeitpunkt der Zahlung weist der tatsächlich bei der Banktransaktion registrierte Währungskurs einen Währungskurs von 1,120 auf.

Hier liegt eine nicht realisierte Transaktion vor und wird daher mit der Zahlung storniert.

Abschließend wird die Zahlung registriert und der tatsächliche Verlust auf das realisierte Verlustkonto gebucht.

## <a name="available-currency-functions"></a>Verfügbare Währungsfunktionen

In der folgenden Tabelle sind die wichtigsten Aktionen auf der Seite **Währungen** aufgeführt. Einige der Aktionen werden in den nächsten Abschnitten erklärt.  

|Menü|Aktion|Beschreibung|
|-------------|--------------|------------------------------|
|**Verarbeiten**|**Konten vorschlagen**|Verwenden Sie Konten aus den anderen Währungen. Die am häufigsten verwendeten Konten werden eingefügt.|
||Zahlungstoleranz ändern|Ändern Sie entweder die maximale Zahlungstoleranz oder die Zahlungstoleranz in Prozent, und filtern Sie nach Währung. Weitere Informationen finden Sie unter [Zahlungstoleranz und Skontotoleranz](finance-payment-tolerance-and-payment-discount-tolerance.md).|
||**Wechselkurse**|Zeigen Sie aktualisierte Wechselkurse für die verwendeten Währungen an.|
||**Wechselkurse regulieren**|Aktualisiert Sach-, Debitoren-, Kreditoren- und Bankkontenposten, wenn sich der Wechselkurs seit Buchung der Posten geändert hat.|
||**Kursregulierungsjournal**|Sehen Sie sich die Ergebnisse der Ausführung der Stapelverarbeitung **Wechselkurse reguieren** an. Für jede Währung oder für jede an der Regulierung beteiligte Kombination aus einer Buchungsgruppe und einer Währung wird eine Zeile erstellt.|
|**Wechselkursdienst**|**Wechselkursdienste**|Die Einrichtung der Dienste anzeigen oder bearbeiten, die eingerichtet werden, um aktualisierte Währungswechselkurse abzurufen, wenn Sie die Aktion **Wechselkurse aktualisieren** auswählen.|
||**Wechselkurse aktualisieren**|Rufen Sie die neuesten Währungswechselkurse bei einem Dienstanbieter ab.|
|**Berichte**|**Fremdwährungssaldo**|Zeigen Sie die Salden aller Debitoren und Kreditoren in der Fremdwährung und in der Landeswährung (Mandantenwährung, MW) an. Der Bericht zeigt zwei Salden in MW an. Dazu gehört auch der Fremdwährungssaldo, der mithilfe des Wechselkurses zum Zeitpunkt der Transaktion in MW konvertiert wird. Außerdem gehört dazu der Fremdwährungssaldo, der mithilfe des Wechselkurses des Arbeitsdatums in MW konvertiert wird.|

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

## <a name="adjusting-exchange-rates"></a>Regulieren von Wechselkursen

Da sich Wechselkurse ständig ändern, müssen weitere Währungsentsprechungen im System in regelmäßigen Abständen reguliert werden. Werden diese Regulierungen nicht durchgeführt, sind Beträge, die aus fremden (oder zusätzlichen) Währungen umgerechnet und in der Mandantenwährung in der Finanzbuchhaltung gebucht wurden, möglicherweise irreführend. Darüber hinaus müssen Tagesposten, die vor der Eingabe eines Tageswechelkurses in der Anwendung gebucht werden, aktualisiert werden, nachdem der Tageswechselkurs eingegeben wurde.

Der Batchauftrag **Wechselkurse anpassen** wird verwendet, um die Wechselkurse von gebuchten Debitor-, Kreditor- und Bankkonten-Buchungen manuell anzupassen. Berichtswährungsbeträge in Sachposten können hiermit ebenfalls aktualisiert werden.  

> [!TIP]
> Sie können einen Dienst verwenden, um Wechselkurse im System automatisch zu regulieren. Weitere Informationen finden Sie unter [So richten Sie einen Währungswechselkurs-Service ein](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Die Wechselkurse für bereits gebuchte Transaktionen werden hierdurch jedoch nicht reguliert. Um Wechselkurse für gebuchte Einträge zu regulieren, verwenden Sie die Stapelverarbeitung **Wechselkurse regulieren**.

### <a name="effect-on-customers-and-vendors"></a>Auswirkung auf Debitoren und Kreditoren

Für Debitoren- und Kreditorenkonten reguliert der Batchauftrag die Währung unter Verwendung des Wechselkurses, der zum Zeitpunkt des im Batchauftrag angegebenen Buchungsdatums gültig ist. Die Stapelverarbeitung berechnet die Differenzen für die einzelnen Währungssalden und bucht die Beträge auf das Sachkonto, das im Feld **Kursgewinn unrealisiert Kto.** oder im Feld **Kursverlust unrealisiert Kto.** auf der Seite **Währungen** angegeben ist. Gegenposten werden automatisch auf die Debitoren- und Kreditorensammelkonten in der Finanzbuchhaltung gebucht.

Die Stapelverarbeitung bearbeitet alle offenen Debitoren- und Kreditorenposten. Wenn es eine Wechselkursdifferenz für eine Buchung gibt, erstellt der Batchauftrag einen neuen detaillierten Debitoren- oder Kreditoren-Sachkonto-Eintrag, der den angepassten Betrag auf dem Debitoren- oder Kreditoren-Sachkonto-Eintrag wiedergibt.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensionen in Debitoren- und Kreditorenposten

Den Differenzposten werden die Dimensionen von den Debitoren-/Kreditorenposten zugewiesen. Die Differenzen werden pro Kombination von Dimensionswerten gebucht.

### <a name="effect-on-bank-accounts"></a>Auswirkungen auf Bankkonten

Für Bankkonten reguliert der Batchauftrag die Währung unter Verwendung des Wechselkurses, der zum Zeitpunkt des im Batchauftrag angegebenen Buchungsdatums gültig ist. Die Stapelverarbeitung berechnet die Differenzen für jedes Bankkonto mit einem Währungscode und bucht die Beträge auf das Sachkonto, das im Feld **Kursgewinn realisiert Kto.** oder im Feld **Kursverlust realisiert Kto.** der Tabelle **Währungen** angegeben ist. Gegenposten werden automatisch auf die Banksachkonten gebucht, die in den Bankkontenbuchungsgruppen angegeben sind. Die Stapelverarbeitung erzeugt einen Posten pro Währung pro Buchungsgruppe.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensionen in Bankposten

Den Differenzposten für das Sachkonto des Bankkontos und für das Gewinn- und Verlustkonto werden die Vorgabedimensionen des Bankkontos zugewiesen.

### <a name="effect-on-gl-accounts"></a>Auswirkungen auf Sachkonten
Wenn Sie in einer Berichtswährung buchen, kann die Stapelverarbeitung neue Sachposten für Wechselkursregulierungen zwischen Mandantenwährung und Berichtswährung erstellen. Die Stapelverarbeitung berechnet die Differenzen für jeden Sachposten und reguliert den Sachposten abhängig vom Inhalt des Felds **Kursregulierung** für jedes Sachkonto.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensionen in Sachposten
Den Differenzposten werden die Vorgabedimensionen der Konten zugewiesen, auf die sie gebucht werden.

> [!Important]
> Bevor Sie den Batchauftrag aufrufen können, müssen Sie die Wechselkurse eingeben, die zum Regulieren der Fremdwährungssalden verwendet werden. Dies erfolgt auf der Seite **Währungswechselkurse**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>So richten Sie einen Währungswechselkurs-Service ein
Sie können einen externen Service verwenden, um Ihre Währungswechselkurse wie FloatRates auf dem neuesten Stand zu halten. 

> [!NOTE]
> Die meisten Wechselkursdienste stellen Daten bereit, die mit dem Importprozess in [!INCLUDE[prod_short](includes/prod_short.md)] kompatibel sind. Manchmal sind die Daten jedoch anders formatiert, und Sie müssen Ihren Importvorgang anpassen. Sie können dazu das Datenaustauschframework verwenden, indem Sie Ihre eigene Codeunit hinzufügen. Dazu benötigen Sie wahrscheinlich die Hilfe eines Entwicklers. Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Währungswechselkurs-Dienste** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie auf der Seite **Währungswechselkurs-Service** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Aktivieren Sie das Kontrollkästchen **Aktiviert**, um den Dienst zu aktivieren.

> [!NOTE]
> Das folgende Video zeigt ein Beispiel für die Verbindung zu einem Wechselkursdienst am Beispiel der Europäischen Zentralbank. In dem Abschnitt, der das Einrichten von Feldzuordnungen beschreibt, gibt die Einstellung in der Spalte **Quelle** für die Option **Übergeordneter Knoten für Währungscode** nur die erste gefundene Währung zurück. Die Einstellung sollte auf `/gesmes:Envelope/Code/Code/Code` festgelegt sein.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Um Währungswechselkurse über einen Service zu aktualisieren
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Währungen** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die **Aktualisieren von Wechselkursen** Aktion aus.

Der Wert im Feld **Wechselkurs** wird auf der Seite **Währung** mit dem aktuellen Währungswechselkurs aktualisiert.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch
[Einrichten einer zusätzlichen Berichtswährung](finance-how-setup-additional-currencies.md)  
[Abschlussjahre und -perioden](year-close-years-periods.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
