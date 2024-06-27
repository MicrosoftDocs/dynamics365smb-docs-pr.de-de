---
title: Währungen einrichten
description: 'Sie müssen jede Währung einrichten, wenn Sie in anderen Währungen als Ihrer Hauswährung (LCY) kaufen oder verkaufen oder wenn Sie Sachbuchungen in verschiedenen Währungen erfassen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: multiple currencies
ms.search.form: '5, 118'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-currencies"></a>Währungen einrichten

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Verwenden Sie einen externen Dienst, um aktuelle Währungswechselkurse in der Liste **Währungen** abzurufen. Weitere Informationen finden Sie unter [So richten Sie einen Währungswechselkurs-Service ein](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service).  

[!INCLUDE [finance-currencies-lcy](includes/finance-currencies-lcy-note.md)]

## <a name="currencies"></a><a name="curr"></a>Währungen

In der folgenden Tabelle werden die Felder in der **Währungen**-Liste beschrieben.

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
|**Max. MwSt.-Differenz zulässig**|Der Höchstbetrag für MwSt.-Differenzen in dieser Währung. Weitere Informationen finden Sie unter [MwSt.-Beträge in Verkaufs- und Einkaufsbelegen manuell korrigieren](finance-work-with-vat.md#correcting-vat-amounts-manually-on-sales-and-purchase-documents). Dieses Feld ist möglicherweise standardmäßig nicht sichtbar. Sie kann durch Personalisierung der Seite abgerufen werden.|
|**MwSt.-Rundungsmethode**|Gibt die Rundungsmethode für die manuelle Korrektur von MwSt.-Beträgen in Verkaufs- und Einkaufsbelegen an. Dieses Feld ist möglicherweise standardmäßig nicht sichtbar. Sie kann durch Personalisierung der Seite abgerufen werden.|

### <a name="available-currency-functions"></a>Verfügbare Währungsfunktionen

In der folgenden Tabelle sind die wichtigsten Aktionen auf der Seite **Währungen** aufgeführt.  

|Menü|Aktion|Beschreibung|
|-------------|--------------|------------------------------|
|**Verarbeiten**|**Konten vorschlagen**|Verwenden Sie Konten aus den anderen Währungen. Die am häufigsten verwendeten Konten werden eingefügt.|
||**Zahlungstoleranz ändern**|Ändern Sie entweder die maximale Zahlungstoleranz oder die Zahlungstoleranz in Prozent, und filtern Sie nach Währung. Weitere Informationen finden Sie unter [Zahlungstoleranz und Skontotoleranz](finance-payment-tolerance-and-payment-discount-tolerance.md).|
||**Wechselkurse**|Zeigen Sie aktualisierte Wechselkurse für die verwendeten Währungen an.|
||**Wechselkurse regulieren**|Aktualisieren Sie Salden für Hauptbuch-, Debitoren-, Kreditoren- und Bankkontoeinträge. Die Aktualisierung ist dann sinnvoll, wenn sich der Wechselkurs nach der Buchung geändert hat.|
||**Wechselkursregulierungserfassung**|Sehen Sie sich die Ergebnisse der Ausführung der Stapelverarbeitung **Wechselkurse reguieren** an. Für jede Währung oder für jede an der Regulierung beteiligte Kombination aus einer Buchungsgruppe und einer Währung wird eine Zeile erstellt.|
|**Wechselkursdienst**|**Wechselkursdienste**|Die Einrichtung der Dienste anzeigen oder bearbeiten, die eingerichtet werden, um aktualisierte Währungswechselkurse abzurufen, wenn Sie die Aktion **Wechselkurse aktualisieren** auswählen.|
||**Wechselkurse aktualisieren**|Rufen Sie die neuesten Währungswechselkurse bei einem Dienstanbieter ab.|
|**Berichte**|**Fremdwährungssaldo**|Zeigen Sie die Salden aller Debitoren und Kreditoren in der Fremdwährung und in der Landeswährung (Mandantenwährung, MW) an. Der Bericht zeigt zwei Salden in MW an. Dazu gehört auch der Fremdwährungssaldo, der mithilfe des Wechselkurses zum Zeitpunkt der Transaktion in MW konvertiert wird. Außerdem gehört dazu der Fremdwährungssaldo, der mithilfe des Wechselkurses des Arbeitsdatums in MW konvertiert wird.|

## <a name="lcy-and-other-currencies"></a>LCY und andere Währungen

[!INCLUDE [finance-currencies-lcy-def](includes/finance-currencies-lcy-def.md)]

## <a name="rounding-currencies"></a>Runden von Währungen

Zum Verwalten von Währungen ohne Dezimalwerte sowie zum Vermeiden unnötiger Dezimalwerte in Fremdwährung stehen zwei unterschiedliche Rundungsfunktionen zur Verfügung:

- Stückpreisrundung  

- Betragsrundung  

Diese Funktionen können einzeln oder in Kombination verwendet werden. Darüber hinaus lassen sich die Funktionen auch mit der Rechungsrundung kombinieren.

Im Gegensatz zur Rechnungsrundung wirken sich die Betrags- und die Stückpreisrundung lediglich auf Beträge in Fremdwährung (und nicht auf die entsprechenden Beträge in der Mandantenwährung) aus. Mit diesen beiden Funktionen erfolgen keine Buchungen auf Sachkonten. Daher muss auch kein Sachkonto angegeben werden (weder in Buchungsgruppen noch an anderer Stelle).

### <a name="unit-amount-rounding"></a>Stückpreisrundung

Mit der Stückpreisrundung wird gesteuert, wie in Fremdwährung vorliegende Verkaufspreise für Artikel und Ressourcen in Verkaufs- und Einkaufszeilen gerundet werden. Die Regeln müssen in der Liste **Währungen** im Feld **Stückpreisrundungspräzision** für jede Währung einzeln angegeben werden.

Die Stückpreisrundung wird automatisch verwendet, wenn Sie eine Artikel- oder Ressourcennummer in eine Verkaufszeile eingeben. Handelt es sich um eine Rechnung für einen Debitor mit einem Währungscode, wird der Artikel- oder Ressourcenpreis in die Währung des Debitors konvertiert. Die Rundung des Preises erfolgt gemäß der Stückpreisrundungspräzision für die Währung.

### <a name="amount-rounding"></a>Betragsrundung

Mit der Betragsrundung wird gesteuert, wie in Fremdwährung vorliegende Beträge in Fibu Buch.-Blattzeilen, in Verkaufszeilen und in Einkaufszeilen gerundet werden. Die Regeln müssen in der Liste **Währungen** im Feld **Betragsrundungspräzision** für jede Währung einzeln angegeben werden.

Die Rundung von Fremdwährungsbeträgen erfolgt beim Ausfüllen und Buchen von Fibu Buch-Blattzeilen, Verkaufszeilen und Einkaufszeilen.

## <a name="exchange-rates"></a>Wechselkurse

Sie können für jede Fremdwährung Wechselkurse registrieren und angeben, ab welchem Datum der jeweilige Wechselkurs gelten soll. So lassen sich für jede Fremdwährung beispielsweise Tageswechselkurse, Monatswechselkurse oder Quartalswechselkurse angeben.

Zu Referenzzwecken können Sie auf der Seite **Währungswechselkurse** ältere Wechselkurse nachschlagen. Muss ein Wechselkurs aktualisiert werden, können Sie über die Schaltfläche **Aktualisieren von Wechselkursen** die aktuellen Wechselkurse von einem externen Dienstanbieter abrufen.

## <a name="general-ledger-accounts"></a>Sachkonten

Währungscodes können nicht mit Sachkonten verknüpft werden, da Sachkontobeträge in Mandantenwährung vorliegen. Wenn Sie über einen Bankkredit in USD verfügen und Einzahlungen auf ein Bankkonto in SEK tätigen, können Sie diese Konten überwachen, indem Sie Bankkonten in USD und SEK einrichten. Mithilfe von Buchungsgruppen können Sie die Konten mit den entsprechenden Sachkonten verknüpfen. In der Finanzbuchhaltung wird der Wert der Beträge in der Mandantenwährung angezeigt.

Sie können einen Währungscode in eine Fibu Buch.-Blattzeile eingeben und die Zeile auf ein Sachkonto buchen. Vor der Buchung auf das Sachkonto wird der Betrag anhand des entsprechenden Wechselkurses in die Mandantenwährung konvertiert.  

## <a name="example-of-a-receivable-currency-transaction"></a>Beispiel für eine ausstehende Währungstransaktion

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="see-also"></a>Siehe auch

[Währungswechselkurse aktualisieren](finance-how-update-currencies.md)  
[Einrichten einer zusätzlichen Berichtswährung](finance-how-setup-additional-currencies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
