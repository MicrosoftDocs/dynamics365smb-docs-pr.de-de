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
ms.openlocfilehash: deb1ac60e40306d9a8730b825b038e663bd51166
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605326"
---
# <a name="set-up-bank-accounts"></a>Bankkonten festlegen

Bankkonten in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden Sie, um den Überblick über Ihre Bank-Transaktionen zu behalten. Konten können auf Ihre Mandantenwährung oder eine Fremdwährung lauten. Nachdem Sie Bankkonten eingerichtet haben, können Sie auch Schecks drucken. Die Bankkonten enthalten zusätzliche Funktionen für [Zahlungsabgleich](receivables-apply-payments-auto-reconcile-bank-accounts.md), [Bankabgleich](bank-how-reconcile-bank-accounts-separately.md) und den Import und Export von Bankdateien. Die Bankkonten können auch in Transaktionen in den Allgemeinen Erfassungen einbezogen werden. Jedes Bankkonto ist über die zugewiesene Buchungsgruppe für Bankkonten mit einem Konto im Kontenplan verknüpft. Die Verwendung eines Bankkontos in einer Zahlungstransaktion erstellt automatisch einen Eintrag sowohl auf dem Bankkonto als auch auf dem damit verbundenen Hauptbuch (Sachkonto).  

Bankkonten funktionieren unterschiedlich, je nachdem, ob ein Währungscode angegeben ist:

- Wenn der Währungscode leer ist

  Alle Transaktionen auf dem Bankkonto erfolgen in der Mandantenwährung (MW) der aktuellen Firma. Wenn eine Transaktion auf dem Konto in einer anderen Währung durchgeführt wird, werden die Beträge auf der Grundlage des entsprechenden Wechselkurses in LCY auf das Konto gebucht. Alle Schecks, die von diesem Konto ausgestellt werden, müssen in MW ausgestellt werden. Wenn das Bankkonto in einem Journal verwendet wird, erbt die Buchungsblattzeile automatisch den leeren Währungscode.  
  
- Währungscode wird angegeben

  Alle Transaktionen auf diesem Konto und alle Schecks, die von diesem Konto ausgestellt werden, müssen in der gleichen Währung erfolgen, die auf dem Konto angegeben ist.

Sie können bei der Dateneingabe Zeit sparen, indem Sie ein Bankkonto als Standardkonto für die für das Konto angegebene Währung festlegen. Wenn Sie dies tun, wird das Konto den Verkaufs- und Dienstleistungsdokumenten zugeordnet, die diese Währung verwenden. Um das Konto als Standardkonto für Verkaufs- und Servicebelege festzulegen, aktivieren Sie auf der Seite **Bankkontokarte** den Umschalter **Als Standard für Währung verwenden**. Bei Bedarf können Sie ein anderes Konto auswählen, wenn Sie an einem Beleg arbeiten.

Ein Bankkonto ist ein integraler Bestandteil von [!INCLUDE[prod_short](includes/prod_short.md)] und spielt bei vielen anderen Funktionalitäten eine Rolle. Die folgende Illustration zeigt die wichtigsten Beziehungen:

![Illustration der Bankkontobeziehungen.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Sie sehen, dass das Erstellen eines Bankkontos dazu führt, dass es an allen oben genannten Stellen verfügbar ist und auch im entsprechenden Sachkonto und auf der Seite **Unternehmensdaten** gespiegelt wird.

Ein Bankkonto wird in der Regel täglich überwacht, um sicherzustellen, dass alle neuen Zahlungen von Kunden so schnell wie möglich registriert werden. Dies trägt dazu bei, dass der aktuelle Status eines Kunden in [!INCLUDE[prod_short](includes/prod_short.md)] wiedergegeben wird. Auf diese Weise haben Vertriebsmitarbeiter, Buchhalter und andere Mitarbeiter Zugriff auf die wichtigsten und aktuellsten Informationen, so dass sie unnötige Anrufe beim Kunden wegen überfälliger Rechnungen oder Verzögerungen bei der Lieferung vermeiden können.  

![Abbildung der Bankzahlung.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

Eine weitere Aufgabe besteht darin, die Zahlungen der Lieferantenwährungen mit den realisierten Sätzen zu importieren, um sicherzustellen, dass der aktuelle Status der Lieferanten auf dem neuesten Stand ist. Mit der Funktionalität [Zahlungsabgleich](receivables-apply-payments-auto-reconcile-bank-accounts.md) ist das am einfachsten zu bewerkstelligen. Im **Zahlungsabstimmungs Buch.-Blatt** können Sie Banktransaktionen direkt aus einer Online-Bankanwendung importieren und mehr oder weniger automatisch verbuchen lassen. Das Journal identifiziert und bucht automatisch Folgendes:  

- Lastschriftzahlungen von Kunden  
- Debitoren-Zahlungen von einzelnen Rechnungen  
- Pauschalzahlungen von Kunden  
- Debitoren-Zahlungen in Fremdwährungen  
- Zahlungen von Kreditoren  
- Kreditorenzahlungen in Fremdwährung  
- Wiederkehrende Zahlungen von Kreditoren und Abonnements  
- Bankgebühren und Zinsen  

Der Zahlungsabgleich sorgt für eine erhebliche Zeitersparnis bei der Buchung von ein- und ausgehenden Zahlungen. Allerdings gelten die Transaktionen auf dem Bankkonto in [!INCLUDE[prod_short](includes/prod_short.md)] erst dann als 100 % korrekt, wenn Sie einen Bankabgleich ausführen.  

Mit der Bankabstimmung stellen Sie sicher, dass das Bankkonto in [!INCLUDE[prod_short](includes/prod_short.md)] mit dem externen Konto bei der Bank übereinstimmt.  

 ![Illustration der Bankkontoabstimmung.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

In der obigen Abbildung steht die linke Seite für das Bankkonto in [!INCLUDE[prod_short](includes/prod_short.md)] und die rechte Seite für Transaktionen, die von der Bank über die Online-Bankanwendung importiert wurden. Das Diagramm in der Mitte zeigt die Transaktionen von beiden Seiten, das ist die Bankabstimmung.

Vom Bankkonto in [!INCLUDE[prod_short](includes/prod_short.md)] sollten die meisten Transaktionen bei der physischen Bank bekannt sein. Zu den wenigen Ausnahmen gehören die folgenden Fälle:  

- In [!INCLUDE[prod_short](includes/prod_short.md)] gebuchte Korrekturen  
- Ausgestellte Schecks, die noch nicht eingelöst worden sind 
- Kreditorenzahlungen, die noch nicht von der Bank genehmigt wurden  

Vom physischen Konto bei der Bank treffen immer wieder Transaktionen ein, die nicht im Zahlungsabstimmungs Buch.-Blatt ausgewiesen sind, wie z.B:  

- Neue Abonnements von Kreditoren  
- Debitoren-Zahlungen ohne Beschreibung
- Bankzinsen
- Bankgebühren
- Kreditkartenbelastungen, die noch nicht gemeldet wurden

Je besser Sie die Informationen im Zahlungsabstimmungs-Buch.-Blatt zuordnen können, desto mehr Transaktionen werden automatisch gebucht und desto einfacher wird der periodische Bankabgleich.

Sehen Sie im Video unten die grundlegenden Schritte zum Festlegen eines Bankkontos in [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

> [!WARNING]
> Einige Felder können sensible Daten enthalten, wie z.B. die Felder **BLZ**, **Bankkontonr.**, **SWIFT Code**, und **IBAN Code**. Erfahren Sie mehr unter [Überwachung sensibler Felder](across-log-changes.md#monitoring-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Bankkonten einrichten:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?"). Symbol. Geben Sie **Bankkonten** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Bankkonten** die Aktion **Neu** aus.
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Ein Beispiel wäre das **Bankkonto. Buchungsgruppe**, das das Bankkonto mit dem zugrunde liegenden Sachkonto in der Bilanz verknüpft. Erfahren Sie mehr unter [Buchungsgruppen festlegen](finance-posting-groups.md).

> [!TIP]
> Einige Felder sind ausgeblendet, bis Sie die Aktion **Mehr anzeigen** wählen, da sie in der Regel selten verwendet werden. Andere müssen durch Personalisierung hinzugefügt werden. Erfahren Sie mehr unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

Sie können so viele Bankkonten erstellen, wie Sie für Ihr Unternehmen benötigen. Für jedes Bankkonto müssen Sie Informationen angeben, die das Bankkonto eindeutig identifizierbar machen. Zu diesen Informationen gehören die geografische Adresse der Bank, Nummernserien für verschiedene Arten von Transaktionen, wie z.B. Lastschriften und Überweisungen, die Währung, in der die Beträge angegeben werden, und Informationen, die für den Import von Bankauszügen verwendet werden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the account.|
|Bank Branch No.|Typically used to identify the bank branch in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Typically used to identify the bank account number in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the bank account balance in the account currency.|
|Balance (LCY)|Shows the bank account balance in the local currency (LCY).|
|Our Contact Code|Specifies a code to identify the employee responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the single euro payments area (SEPA) format of the bank file to be exported when you choose **Create Direct Debit File** on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages created with the export file you create from the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series to be used on the direct debit file you export for a direct debit collection entry on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA direct debit. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing required according to the format standard you selected in the **Bank Clearing Standard** field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as the sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether or not to disable automatic payment matching after importing bank transactions for this bank account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies the tolerance the automatic payment application function will use to apply the *Amount Incl. Tolerance Matched* rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the *Amount Incl. Tolerance Matched* rule by percentage or amount. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name you can use to search for the record in question when you can't remember the value in the **Name** field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition managing the export of positive-pay files. Learn more at [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The country/region code of the bank branch.|
|Phone No.|The phone number of the bank branch.|
|Mobile Phone No.|The mobile phone number of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the **Contacts** module.|
|Fax No.|The fax number of the bank branch.|
|Email|The email address of the bank branch.|
|Home Page|The home page address of the bank branch website.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account limits all transactions to only using the applied currency code. Leaving the currency code blank allows transactions in all currencies, however, the amount will eventually be converted to the LCY using the applied currency rate. Checks issued from this account follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending balance of the last bank statement. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account's posting group. The **Bank Acc. Posting Group** connects the bank account to the G/L account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier (SWIFT) code of the bank in which you have account. The SWIFT code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number (IBAN). The IBAN code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file imported into this bank account. This format is used in both the payment reconciliation journals and bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that is exported when you choose **Export Payments to File** on the **Payment Journal** page.|
-->

## <a name="to-enter-an-opening-balance"></a>So geben Sie einen Eröffnungssaldo ein

Um das Feld **Saldo** mit einem Eröffnungssaldo zu füllen, müssen Sie eine Sachkonto-Buchung mit dem betreffenden Betrag vornehmen. Sie können dies tun, indem Sie eine Bankkontoabstimmung durchführen. Erfahren Sie mehr unter [Bankkonten abstimmen](bank-how-reconcile-bank-accounts-separately.md).  
>
> Alternativ können Sie den Eröffnungssaldo als Teil der allgemeinen Datenerstellung in neuen Firmen implementieren, indem Sie die Anleitung **Geschäftsdaten migrieren** für die unterstützte Einrichtung verwenden. Weitere Informationen unter [Bereitschaft für die Geschäftsabwicklung](ui-get-ready-business.md).  

> [!IMPORTANT]
> Buchen Sie den Eröffnungssaldo nicht direkt in das Hauptbuch. Direkt auf das Sachkonto gebuchte Einträge führen in der Regel dazu, dass Sie das Bankkonto nicht mehr abstimmen können. Bei Bankkonten in Fremdwährung führt eine solche Praxis dazu, dass sich die Differenzen häufen, wenn Sie mehr Bankabstimmungen buchen. Normalerweise buchen Sie den Eröffnungssaldo direkt auf das Bankkonto, und der Betrag landet auf dem Sachkonto. Alternativ können Sie ihn später aus dem Sachkonto stornieren, das Sie zum Ausgleich des Eröffnungssaldos des Hauptbuchs verwenden. In jedem Fall müssen Sie jede Direktbuchung auf das Sachkonto ausgleichen, bevor Sie mit der ersten Bankabstimmung beginnen &mdash;insbesondere wenn das Bankkonto auf eine Fremdwährung lautet.

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Um Ihre Bankkonten zum Importieren und Exportieren von Bankdateien einzurichten

Die Felder, die sich auf den Import und den Export von Bankfeeds und Dateien beziehen, befinden sich im Inforegister **Transfer** im Fenster **Bankkontenkarte**. Erfahren Sie mehr unter [Verwendung der Erweiterung AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) und [Einrichten des Dienstes Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 2.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Bankkonten** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte für das Bankkonto, für das Sie Bankdateien exportieren oder importieren möchten.
3. Füllen Sie im Inforegister **Übertrag** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Verschiedene Dateiexportdienstleistungen und deren Formaten benötigen verschiedene Einrichtungswerte auf der Seite **Bankkontokarte** Wenn Sie die Datei exportieren, werden Sie auf falsche oder fehlende Einrichtungswerte hingewiesen. Lesen die Kurzbeschreibungen der Felder sorgfältig durch oder gehen Sie zu den entsprechenden Verfahrensthemen. Wenn Sie beispielsweise eine Zahlungsdatei für eine nordamerikanische elektronische Überweisung (EFT) exportieren, müssen sowohl die Felder **Letzte Überweisungsmitteilung Nr.** als auch **Zustellungsnummer** ausgefüllt werden. Erfahren Sie mehr unter [Zahlungen in eine Bankdatei exportieren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Die Felder im Inforegister **Transit** auf dem Bankkonto dienen unterschiedlichen Zwecken, je nachdem, ob es sich um eine eingehende oder ausgehende Zahlung handelt.

Die folgende Abbildung zeigt den Weg der eingehenden Zahlungen (die Nummern in der Beschreibung entsprechen denen in der Abbildung):

:::row:::
    :::column:::

1. Die Transaktionen werden vom Bankkonto entweder in einem menschenlesbaren .csv-Format oder im bankeigenen Format exportiert.
2. Die *Data Exchange Definition* ordnet die Informationen in der Datei den Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] zu. Erfahren Sie mehr unter [Set Up Data Exchange](across-set-up-data-exchange.md)
3. Die *Einrichtung für Datenexport/-import* definiert den Export oder Import und verweist auf die Datenaustauschdefinition.
4. Das *Importformat für Bankauszüge* verknüpft die Einrichtung für den Import mit dem Bankkonto.
5. Die Zahlungen werden über das **Zahlungsausgangs Buch.-Blatt** oder die **Bankkontoabstimmung** Seite importiert.

  :::column-end:::
  :::column:::

        ![Illustration von Zahlungseingängen von der Bank auf Bankkonten.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)

  :::column-end:::
:::row-end:::

Eingehende Zahlungen werden immer über das **Zahlungsabstimmungs Buch.-Blatt** oder direkt in die **Bankkontoabstimmung** Seite importiert. Im Gegensatz dazu können ausgehende Zahlungen aus jedem Zahlungsausgangs Buch.-Blatt stammen. Die einzige Voraussetzung ist, dass das Feld **Zahlungsexport zulassen** im entsprechenden Batch des Zahlungsausgangs Buch.-Blatt markiert ist.

Die folgende Abbildung zeigt den Weg der ausgehenden Zahlungen (die Nummern in der Beschreibung entsprechen denen in der Abbildung):

:::row:::
    :::column:::

6. Die Transaktionen werden in ein Zahlungsausgangs Buch.-Blatt eingefügt, das für den Export von Zahlungen in eine Datei vorbereitet wurde.
7. Das *Importformat für Bankauszüge* verknüpft die Importeinrichtung mit dem Bankkonto.
8. Die *Einrichtung für Datenexport/-import* definiert den Export oder Import und verweist auf die Datenaustauschdefinition.
9. Die *Datenaustauschdefinition* ordnet die Informationen in der Datei den Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] zu. Mehr dazu erfahren Sie unter [Data Exchange festlegen](across-set-up-data-exchange.md)
10. Die Zahlungen werden aus der Erfassung des Zahlungsausgangs Buch.-Blatt exportiert und in das Bankkonto importiert.

  :::column-end:::
  :::column:::

        ![Illustration von Zahlungen von Bankkonten, die an die Bank gesendet werden.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)

  :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Um Ihre Bankkonten zum Importieren und Exportieren von Bankdateien einzurichten

Die Felder auf dem Inforegister **Überweisung** auf der Seite **Kreditoren Bankkontonummer** beziehen sich auf den Export von Bankfeeds und Dateien. Erfahren Sie mehr unter [Verwenden Sie die Erweiterung AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) und [Zahlungen in eine Bankdatei exportieren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

[!INCLUDE[purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

## <a name="changing-your-bank-account"></a>Ändern Ihres Bankkontos

Um ein anderes Bankkonto für Ihr Unternehmen zu verwenden, müssen Sie das neue Bankkonto in [!INCLUDE[prod_short](includes/prod_short.md)] erstellen. Wir empfehlen, dass Sie nicht einfach die Informationen über das derzeit verwendete Konto ersetzen, da dies zu falschen Daten führen kann. Zum Beispiel könnte Ihr Eröffnungssaldo falsch sein oder Ihr Bankfeed nicht mehr richtig funktionieren. Es ist wichtig, dass Sie das aktuelle und das neue Konto getrennt halten.

Nachdem Sie das neue Bankkonto erstellt haben, sollten Sie auch eine neue Bankbuchungsgruppe erstellen und diese einem neuen Hauptbuch-Konto zuordnen. Sie können eine bestehende Bankbuchungsgruppe wiederverwenden und die Transaktionen werden auf dieselben Hauptbuch-Konten gebucht wie auf andere Bankkonten, die sich diese Buchungsgruppe teilen. Wir empfehlen jedoch, eine neue Bankbuchungsgruppe und ein neues Hauptbuchkonto zu erstellen, damit die Abstimmungen einfacher zu erledigen sind.

> [!NOTE]
> Denken Sie daran, dass die Bankkontoinformationen auf offenen Verkaufsrechnungen immer noch das ursprüngliche Bankkonto anzeigen. Dementsprechend werden Zahlungen wahrscheinlich immer noch auf dieses Konto gebucht. Wir empfehlen Ihnen, beide Konten nach der Änderung noch eine Zeit lang aktiv zu halten.

Um eine komprimiertere Ansicht Ihrer Geldkonten in der Finanzberichterstattung zu erhalten, verwenden Sie die **Beginn-Summe** und **Ende-Summe** Konten in Ihrem Kontenplan, die **Summen** Zeilen in Finanzberichten oder Sachkonto-Kategorien. Erfahren Sie mehr im Abschnitt [Business Intelligence und Financial Reporting](bi.md).

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Einrichten von Banken](bank-setup-banking.md)  
[Einrichten von Buchungsgruppen](finance-posting-groups.md)  
[Abstimmen von Bankkonten](bank-manage-bank-accounts.md)  
[Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md)  
[SEPA-Lastschrift in Business Central](finance-collect-payments-with-sepa-direct-debit.md)  
[Um Ihr Bankkonto für SEPA-Lastschrift festzulegen](finance-collect-payments-with-sepa-direct-debit.md#to-set-up-your-bank-account-for-sepa-direct-debit)  
[Um ein Bankkonto für SEPA-Überweisung festzulegen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-set-up-a-bank-account-for-sepa-credit-transfer)  
[Zahlungen mit der Erweiterung AMC Banking 365 Fundamentals oder SEPA-Überweisung vornehmen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Zahlungsabstimmung](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Verständnis der Fibu und des COA](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
