---
title: Bankkonten festlegen (enthält Video)
description: Erfahren Sie, wie Bankkonten in Business Central verwendet werden und wie Sie Beträge mit Ihrer Bank abstimmen können.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.search.form: 370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280
ms.date: 01/24/2022
ms.author: edupont
ms.openlocfilehash: fc0c01281b4a4fb1bccee4196917b4357413e4cf
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514121"
---
# <a name="set-up-bank-accounts"></a>Bankkonten festlegen

Bankkonten in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden Sie, um den Überblick über Ihre Bank-Transaktionen zu behalten. Konten können in Mandantenwährung oder in Fremdwährung geführt werden. Nachdem Sie Bankkonten eingerichtet haben, können Sie auch Schecks drucken. Die Bankkonten enthalten zusätzliche Funktionen für [Zahlungsabgleich](receivables-apply-payments-auto-reconcile-bank-accounts.md), [Bankabgleich](bank-how-reconcile-bank-accounts-separately.md) und den Import und Export von Bankdateien. Die Bankkonten können auch in Transaktionen in den Allgemeinen Erfassungen einbezogen werden. Jedes Bankkonto ist über die zugewiesene Buchungsgruppe für Bankkonten mit einem Konto im Kontenplan verknüpft. Die Verwendung eines Bankkontos in einer Zahlungstransaktion erstellt automatisch einen Eintrag sowohl auf dem Bankkonto als auch auf dem verbundenen Sachkonto.  

Bankkonten funktionieren unterschiedlich, je nachdem, ob ein Währungscode angegeben ist:

- Währungscode ist leer

  Alle Transaktionen auf dem Bankkonto werden in der lokalen Währung (LCY) der aktuellen Firma durchgeführt. Wenn eine Transaktion auf dem Konto in einer anderen Währung durchgeführt wird, werden die Beträge auf der Grundlage des entsprechenden Wechselkurses in LCY auf das Konto gebucht. Alle Schecks, die von diesem Konto ausgestellt werden, müssen in LCY ausgestellt sein. Wenn das Bankkonto in einem Journal verwendet wird, erbt die Buchungsblattzeile automatisch den leeren Währungscode.  
- Währungscode wird angegeben

  Alle Transaktionen, die auf diesem Konto vorgenommen werden, müssen in der gleichen Währung erfolgen, die auf dem Konto angegeben ist. Alle Schecks, die von diesem Konto ausgestellt werden, müssen ebenfalls diese Währung haben.  

Sie können bei der Dateneingabe Zeit sparen, indem Sie ein Bankkonto als Standardkonto für die für das Konto angegebene Währung festlegen. Bei dieser Vorgehensweise wird das Konto Verkaufs- und Servicebelegen zugeordnet, die die Währung verwenden. Um das Konto als Standardkonto für Verkaufs- und Servicebelege festzulegen, aktivieren Sie auf der Seite **Bankkontokarte** den Umschalter **Als Standard für Währung verwenden**. Bei Bedarf können Sie ein anderes Konto auswählen, wenn Sie an einem Beleg arbeiten.

Ein Bankkonto ist ein integrierter Teil von [!INCLUDE[prod_short](includes/prod_short.md)] und spielt bei vielen anderen Funktionalitäten eine Rolle. Die folgende Illustration zeigt die wichtigsten Beziehungen:

![Illustration der Bankkontobeziehungen.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Das heißt, wenn Sie ein Bankkonto erstellen, steht es an allen oben gezeigten Stellen zur Verfügung und wird auch im entsprechenden Sachkonto und auf der Seite **Unternehmensdaten** gespiegelt.

Ein Bankkonto wird normalerweise täglich überwacht, um sicherzustellen, dass alle neuen Zahlungen von Debitoren so schnell wie möglich registriert werden. Dadurch wird sichergestellt, dass der aktuelle Status der Debitoren in [!INCLUDE[prod_short](includes/prod_short.md)] wiedergegeben wird, sodass Vertriebsmitarbeiter, Buchhalter und andere Mitarbeiter Zugriff auf relevante und aktuelle Informationen haben. Auf diese Weise vermeiden sie unnötige Anrufe beim Debitor wegen überfälliger Rechnungen oder verspäteter Sendungen.  

![Abbildung der Bankzahlung.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

Eine weitere Aufgabe ist es, die Zahlungen der Kreditor-Währungen mit den realisierten Sätzen zu importieren, um sicherzustellen, dass der tatsächliche Status der Kreditor aktuell ist. Der einfachste Weg, um sicherzustellen, dass das Bankkonto aktualisiert wird, ist die Funktionalität [Zahlungsabstimmung](receivables-apply-payments-auto-reconcile-bank-accounts.md). Im **Zahlungsabstimmungs Buch.-Blatt** können Sie Banktransaktionen direkt aus einer Online-Bankanwendung importieren und mehr oder weniger automatisch verbuchen lassen. Das Journal identifiziert und bucht automatisch Folgendes:  

- Lastschriftzahlungen von Kunden  
- Debitoren-Zahlungen von einzelnen Rechnungen  
- Pauschalzahlungen von Kunden  
- Debitoren-Zahlungen in Fremdwährungen  
- Zahlungen von Kreditoren  
- Kreditorenzahlungen in Fremdwährung  
- Wiederkehrende Zahlungen von Kreditoren und Abonnements  
- Bankgebühren und Zinsen  

Der Zahlungsabgleich sorgt für eine massive Zeitersparnis bei der Buchung von Zahlungseingängen und -ausgängen. Die Transaktionen auf dem Bankkonto in [!INCLUDE[prod_short](includes/prod_short.md)] werden jedoch erst dann als 100 % korrekt angesehen, wenn Sie einen Bankabgleich ausführen.  

Mit der Bankabstimmung stellen Sie sicher, dass das Bankkonto in [!INCLUDE[prod_short](includes/prod_short.md)] mit dem externen Konto bei der Bank übereinstimmt.  

 ![Illustration der Bankkontoabstimmung.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

In der obigen Abbildung stellt die linke Seite das Bankkonto in [!INCLUDE[prod_short](includes/prod_short.md)] dar und die rechte Seite die Transaktionen, die von der Bank über die Online-Bankanwendung importiert wurden. Das Diagramm in der Mitte zeigt die Transaktionen von beiden Seiten, das ist die Bankabstimmung.

Vom Bankkonto in [!INCLUDE[prod_short](includes/prod_short.md)] sollten die meisten Transaktionen bei der physischen Bank bekannt sein. Die einzigen Ausnahmen sind die folgenden Fälle:  

- In [!INCLUDE[prod_short](includes/prod_short.md)] gebuchte Korrekturen  
- Ausgestellte Schecks, die noch nicht eingelöst worden sind  
- Zahlungen von Kreditoren, die noch nicht von der Bank genehmigt wurden  

Vom physischen Konto in der Bank treffen immer wieder unbekannte Transaktionen ein, die nicht im Zahlungsabstimmungs Buch.-Blatt identifiziert wurden, wie z.B. die folgenden  

- Neue Abonnements von Kreditoren  
- Debitoren-Zahlungen ohne Beschreibung
- Bankzinsen
- Bankbelastungen
- Kreditkartenbelastungen, die noch nicht gemeldet wurden

Je besser Sie die Zuordnung von Informationen im Zahlungsabstimmungs Buch.-Blatt vornehmen, desto mehr Transaktionen werden automatisch gebucht und desto einfacher wird der periodische Bankabgleich.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

<br><br>

> [!WARNING]
> Einige Felder können sensible Daten enthalten, wie z.B. die Felder **BLZ**, **Bankkontonr.**, **SWIFT Code**, und **IBAN Code**. Weitere Informationen finden Sie unter [Überwachen sensibler Felder](across-log-changes.md#monitoring-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Bankkonten einrichten:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Bankkonten** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Bankkonten** die Aktion **Neu** aus.
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Das Feld **Bankkto.-Buchungsgruppe** verbindet das Bankkonto mit dem zugrunde liegenden Sachkonto in der Bilanz. Weitere Informationen finden Sie unter [Buchungsgruppen einrichten](finance-posting-groups.md).

> [!TIP]
> Einige Felder sind ausgeblendet, bis Sie die Aktion **Mehr anzeigen** wählen, typischerweise weil sie selten verwendet werden. Andere müssen durch Personalisierung hinzugefügt werden. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

Sie können so viele Bankkonten erstellen, wie Sie für Ihr Unternehmen benötigen. Für jedes Bankkonto müssen Sie Informationen angeben, die das Bankkonto eindeutig identifizierbar machen. Zu diesen Informationen gehören die geografische Adresse der Bank, Nummernserien für verschiedene Arten von Transaktionen, wie z.B. Lastschriften und Überweisungen, die Währung, in der Beträge angegeben werden, und Informationen, die für den Import von Bankauszügen verwendet werden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the bank account.|
|Bank Branch No.|The Bank Branch No. is usually used to identify the bank branch in domestic payments. The Bank Branch No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Bank Account No. is usually used to identify the bank account no. in domestic payments. The Bank Account No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the Balance of the bank account in the account currency.|
|Balance (LCY)|Shows the Balance of the bank account in the local currency (LCY).|
|Our Contact Code|Specifies a code to specify the employee who is responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies that the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the SEPA format of the bank file that will be exported when you choose the **Create Direct Debit File** button in the **Direct Debit Collect. Entries** window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages that are created with the export file that you create from the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series that will be used on the direct debit file that you export for a direct-debit collection entry in the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA Direct Debit. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing that is required according to the format standard that you selected in the Bank Clearing Standard field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether to disable automatic payment matching after importing bank transactions for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies by which tolerance the automatic payment application function will apply the Amount Incl. Tolerance Matched rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the Amount Incl. Tolerance Matched rule by Percentage or Amount. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name that you can use to search for the record in question when you cannot remember the value in the Name field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition that manages the export of positive-pay files. Read more in [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The Country/Region Code of the bank branch.|
|Phone No.|The Phone No. of the bank branch.|
|Mobile Phone No.|The Mobile Phone No. of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the Contacts module.|
|Fax No.|The Fax No. of the bank branch.|
|Email|The Email of the bank branch.|
|Home Page|The Home Page of the bank branch.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account will limit all transactions to only use the applied currency code. Leaving the currency code blank will allow transactions in all currencies, however, the amount will be converted to the local currency (LCY) using the applied currency rate. Checks issued from this account will also follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending-balance of the last bank statement. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account posting group for the bank account. The Bank Acc. Posting Group connects the bank account to the G/L Account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier code (SWIFT) of the bank where you have the account. The SWIFT Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number. The IBAN Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file that can be imported into this bank account. The format is being used in both the payment reconciliation journals and the bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that will be exported when you choose the Export Payments to File button in the Payment Journal window.|
-->

## <a name="entering-an-opening-balance"></a>Eingeben einer Eröffnungsbilanz
Um das Feld **Saldo** mit einem Eröffnungsbilanz auszufüllen, müssen Sie den Bankposten mit dem entsprechenden Betrag buchen. Sie können dies tun, indem Sie eine Bankkontoabstimmung durchführen. Weitere Informationen finden Sie unter [Abstimmen von Bankkonten](bank-how-reconcile-bank-accounts-separately.md).  
>
> Alternativ können Sie die Eröffnungsbilanz als Teil der allgemeinen Datenerstellung in neuen Unternehmen implementieren, indem Sie den Leitfaden für das unterstützte Setup **Geschäftsdaten migrieren** verwenden. Weitere Informationen finden Sie unter [Vorbereitungen für das Ausführen von Geschäften](ui-get-ready-business.md).  

> [!IMPORTANT]
> Es ist wichtig, dass Sie den Anfangssaldo nicht direkt in der Finanzbuchhaltung buchen. Buchungen im Sachkonto, die direkt in der Finanzbuchhaltung gebucht werden, führen in der Regel dazu, dass Sie das Bankkonto nicht abgleichen können, oder bei Bankkonten in Fremdwährung, dazu, dass sich Differenzen ansammeln, wenn Sie mehr Bankabstimmungen buchen. Häufig wird der Anfangsbestand der Bank direkt auf das Bankkonto gebucht, und der Betrag landet dann auf dem Sachkonto. Alternativ können Sie eine Stornierung für ein Sachkonto durchführen, das Sie zum Ausgleich des Anfangssaldos des Sachpostens verwenden. In beiden Fällen müssen Sie alle Direktbuchungen auf das Sachkonto ausgleichen, bevor Sie mit der ersten Bankabstimmung beginnen, vor allem, wenn das Bankkonto auf eine Fremdwährung lautet.

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Um Ihre Bankkonten zum Importieren und Exportieren von Bankdateien einzurichten
Die Felder, die sich auf den Import und den Export von Bankfeeds und Dateien beziehen, befinden sich im Inforegister **Transfer** im Fenster **Bankkontenkarte**. Weitere Informationen finden Sie unter [Verwenden der AMC Banking 365 Fundamentals-Erweiterung](ui-extensions-amc-banking.md) und [Einrichten des Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Bankkonten** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Karte für ein Bankkonto, mit dem Sie Bankdateien exportieren oder importieren, indem Sie den Bankdatenkonvertierungs-Service verwenden.
3. Füllen Sie im Inforegister **Übertrag** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Verschiedene Dateiexportdienstleistungen und deren Formaten benötigen verschiedene Einrichtungswerte auf der Seite **Bankkontokarte** Sie werden über die falschen oder fehlende Einrichtungswerte informiert, wenn Sie versuchen, die Datei zu exportieren. Lesen die Kurzbeschreibungen der Felder sorgfältig durch oder gehen Sie zu den entsprechenden Verfahrensthemen. Für den Export einer Zahlungsdatei für den nordamerikanischen EFT (Electronic Funds Transfer) beispielsweise müssen die Felder **Letzte Rimesseavis-Nr.** und **Transitnr.** ausgefüllt werden. Weitere Informationen finden Sie unter [Zahlungen in eine Bankdatei exportieren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Die Felder im Inforegister **Transit** auf dem Bankkonto dienen unterschiedlichen Zwecken, je nachdem, ob es sich um eine eingehende oder ausgehende Zahlung handelt.

Die Abbildung zeigt den Arbeitsplan von eingehenden Zahlungen:

:::row:::
    :::column:::
        1. Die Transaktionen werden vom Bankkonto entweder in einem menschenlesbaren .csv-Format oder im bankeigenen Format exportiert.
        <br><br>
2. Die *Data Exchange Definition* ordnet die Informationen in der Datei den Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] zu. Weitere Informationen finden Sie unter [Set Up Data Exchange](across-set-up-data-exchange.md)
<br><br>
3. Die *Einrichtung für den Datenexport/-import* definiert den Export oder Import und verweist auf die Datenaustausch-Definition.
<br><br>
4. Das *Importformat für Bankauszüge* verknüpft die Einrichtung für den Import mit dem Bankkonto.
<br><br>
5. Die Zahlungen werden über das **Zahlungsausgangs Buch.-Blatt** oder die **Bankkontoabstimmung** Seite importiert.
    :::column-end:::
    :::column:::
        ![Illustration von Zahlungseingängen von der Bank auf Bankkonten.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)
    :::column-end:::
:::row-end:::

Zahlungseingänge werden immer über das **Zahlungsabstimmungs Buch.-Blatt** oder direkt über die Seite **Bankkontoabstimmung** importiert. Im Gegensatz dazu können ausgehende Zahlungen aus jedem Zahlungsausgangs Buch.-Blatt stammen. Die einzige Voraussetzung ist, dass das Feld **Zahlungsexport zulassen** im entsprechenden Batch des Zahlungsausgangs Buch.-Blatt markiert ist.

Die Abbildung zeigt den Arbeitsplan der ausgehenden Zahlungen:

:::row:::
    :::column:::
        6. Die Transaktionen, die in einem Zahlungsausgangs Buch.-Blatt aufgefüllt werden, das für den Export von Zahlungen in eine Datei vorbereitet wurde.
        <br><br>
        7. Das *Importformat für Bankauszüge* verknüpft die Importeinrichtung mit dem Bankkonto
        <br><br>
        8. Die Einrichtung *Datenexport/Import* definiert den Export oder Import und verlinkt mit der Datenaustausch-Definition.
        <br><br>
        9. Die *Data Exchange Definition* ordnet die Informationen in der Datei den Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] zu. Weitere Informationen finden Sie unter [Set Up Data Exchange](across-set-up-data-exchange.md)
        <br><br>
        10. Die Zahlungen werden aus dem Zahlungsausgangs Buch.-Blatt exportiert und in das Bankkonto importiert
    :::column-end:::
    :::column:::
        ![Illustration von Zahlungen von Bankkonten, die an die Bank gesendet werden.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)
    :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Um Ihre Bankkonten zum Importieren und Exportieren von Bankdateien einzurichten

Felder auf dem Inforegister **Transfer** auf der Seite **Bankkontenkarte** beziehen sich auf den Import und den Export von Bankfeeds und Dateien. Weitere Informationen finden Sie unter [AMC Banking 365 Fundamentals-Erweiterung verwenden](ui-extensions-amc-banking.md) und [Zahlungen in eine Bankdatei exportieren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kreditoren** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Karte für einen Kreditor, dem Sie Zahlungsbankdateien auf das Bankkonto exportieren möchten.
3. Wählen Sie die **Bankkonten** Aktion aus.
4. Wählen Sie aus der **Liste der Kreditorenbankkonten** das entsprechende Bankkonto aus, oder fügen Sie ein neues Bankkonto hinzu.  
5. Füllen Sie auf der Seite **Kreditoren-Bankkontokarte** im Inforegister **Übertragung** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!WARNING]
> Einige Felder auf dem Bankkonto des Kreditors enthalten sensible Daten, z.B. die Felder **BLZ**, **Bankkontonr.**, **SWIFT Code** und **IBAN Code**. Weitere Informationen finden Sie unter [Monitoring sensibler Felder](across-log-changes.md#monitoring-sensitive-fields).

## <a name="changing-your-bank-account"></a>Ändern Ihres Bankkontos

Wenn Sie ein anderes Bankkonto für Ihr Unternehmen verwenden möchten, müssen Sie das neue Bankkonto in [!INCLUDE[prod_short](includes/prod_short.md)] erstellen. Wir empfehlen, dass Sie nicht einfach die Informationen über das derzeit verwendete Konto ersetzen, da dies zu falschen Daten führen kann. Zum Beispiel könnte Ihr Eröffnungssaldo falsch sein oder Ihr Bankfeed nicht mehr richtig funktionieren. Es ist wichtig, dass Sie das aktuelle und das neue Konto getrennt halten.

Nachdem Sie das neue Bankkonto erstellt haben, sollten Sie auch eine neue Bankbuchungsgruppe erstellen und diese einem neuen Hauptbuch-Konto zuordnen. Sie können eine bestehende Bankbuchungsgruppe wiederverwenden, und die Transaktionen werden auf dieselben Hauptbuch-Konten gebucht wie die anderen Bankkonten, die sich die Bankbuchungsgruppe teilen. Wir empfehlen jedoch, eine neue Bankbuchungsgruppe und ein neues Hauptbuchkonto zu erstellen, damit die Abstimmungen einfacher zu erledigen sind.

> [!NOTE]
> Denken Sie daran, dass die Bankkontoinformationen auf offenen Verkaufsrechnungen immer noch das ursprüngliche Bankkonto anzeigen. Dementsprechend werden Zahlungen wahrscheinlich immer noch auf dieses Konto gebucht. Wir empfehlen Ihnen, beide Konten nach der Änderung noch eine Zeit lang aktiv zu halten.

Um eine komprimiertere Ansicht Ihrer Geldkonten in der Finanzberichterstattung zu erhalten, verwenden Sie die **Beginn-Summe** und **Ende-Summe** in Ihrem Kontenplan, die **Summen**-Zeilen in Kontenplänen oder Sachkonto-Kategorien. Weitere Informationen finden Sie im Abschnitt [Business Intelligence und Finanzberichte](bi.md).

## <a name="see-also"></a>Weitere Informationen

[Einrichten von Banken](bank-setup-banking.md)  
[Einrichten von Buchungsgruppen](finance-posting-groups.md)  
[Abstimmen von Bankkonten](bank-manage-bank-accounts.md)  
[Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md)  
[SEPA-Lastschrift in Business Central](finance-collect-payments-with-sepa-direct-debit.md)  
[Um Ihr Bankkonto für SEPA-Lastschrift festzulegen](finance-collect-payments-with-sepa-direct-debit.md#to-set-up-your-bank-account-for-sepa-direct-debit)  
[Um ein Bankkonto für SEPA-Überweisung festzulegen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-set-up-a-bank-account-for-sepa-credit-transfer)  
[Zahlungen mit der Erweiterung AMC Banking 365 Fundamentals oder SEPA Credit Transfer vornehmen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Zahlungsabstimmung](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Verständnis der Fibu und des COA](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
