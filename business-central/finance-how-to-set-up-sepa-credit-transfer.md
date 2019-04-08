---
title: SEPA Kredittransfer einrichten | Microsoft Docs
description: Erfahren Sie, wie Sie SEPA-Gutschriftenübertragungen in Business Central einrichten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sepa, credit, transfer, payment,
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer
ms.openlocfilehash: 6c35fdb6e5e37eb521b6d51050a552e52b66ec5d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798255"
---
# <a name="set-up-sepa-credit-transfer"></a>Einrichten von SEPA-Kreditübertragung
Auf der Seites dem Fenster **Zahlungsjournal** können Sie Zahlungen in eine Datei zum Upload zu Ihrer elektronischen Bank für die Verarbeitung der zugehörigen Geldüberweisungen exportieren. [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt das Abbuchungsformat SEPA, aber in Ihrem Land/die Region, sind möglicherweise andere Formate für den elektronischen Zahlungsverkehr verfügbar.  

Um das Exportieren von Bankdateiformaten zu aktivieren, die nicht durch die allgemeine oder lokale Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt werden, können Sie eine Datenaustauschdefinition einrichten, indem Sie das Datenaustauschframework verwenden. Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).  

Bevor Sie Zahlungen elektronisch durch den Export von Zahlungszeilen im SEPA-Banküberweisungsformat verarbeiten können, müssen Sie die folgenden Einrichtungsschritte ausführen:  

* Richten Sie das Bankkonto ein, um mit dem SEPA-Banküberweisungsformat umzugehen  
* Einrichten von Lieferantenkarten, um Zahlungen zu verarbeiten, indem Dateien im SEPA-Banküberweisungsformat exportiert werden.  
* Richten Sie das zugehörige Fibu Buch.-Blatt ein, um den Zahlungsexport auf der **Zahlungsjournal**-Seite zu aktivieren.  
* Verbindung der Datenaustauschdefinition für eine oder mehrere Zahlungsarten mit den relevanten Zahlungsverfahren  

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Ein Bankkonto für SEPA-Banküberweisung einrichten  
1. Geben Sie im Feld **Suchen** **Bankkonten** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie die Karte des Bankkontos, von dem Sie Zahlungsdateien im SEPA-Banküberweisungsformat exportieren.  
3. Wählen Sie im Inforegister **Umlagerung** im Feld **Format Zahlungsexport**, wählen Sie **SEPADD** aus.  
4. Wählen Sie im **SEPA-Lastschrift Nachr.-ID**-Feld eine Nummernserie aus, von der Nummern den SEPA-Banküberweisungsposten zugeordnet werden.  
5. Vergewissern Sie sich, dass das Feld **IBAN** ausgefüllt ist.  

    > [!NOTE]  
    >  Das Feld **Währungscode** muss auf **EUR** festgelegt werden, da SEPA-Banküberweisungen nur in der EURO-Währung gebucht werden können.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Eine Kreditorenkarte für SEPA-Banküberweisung einrichten  
1. Geben Sie im Feld **Suchen** **Kreditoren** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie die Karte des Debitors, den Sie elektronisch bezahlen, indem Sie Zahlungsdateien im SEPA-Banküberweisungsformat exportieren.  
3. Wählen Sie im Inforegister **Zahlung** im Feld **Zahlungsformencode** die Funktion **BANK** aus.  
4. Wählen Sie im **Bevorzugtes Bankkonto**-Feld die Bank aus, an die das Geld übertragen wird, wenn es durch Ihre elektronische Bank verarbeitet wird.  

     Der Wert im Feld **Bevorzugtes Bankkonto** wird aus dem Feld **Bankkonto Empfänger** auf der Seite **Zahlungsausgangs Buch.-Blatt** kopiert.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Das Zahlungsausgangs Buch.-Blatt für den Export von Zahlungsdateien festlegen  
1. Geben Sie im Feld **Suchen** einen Wert für **Zahlungsausgangs Buch.-Blatt** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie das Zahlungsausgangs Buch.-Blatt, das Sie verwenden möchten, um Zahlungen zu verarbeiten, indem Sie Dateien im SEPA-Banküberweisungsformat zu exportieren.  
3. Wählen Sie im Feld **Stapelname** die\-Dropdownschaltfläche aus.  
4. Wählen Sie auf der Seite **Fibu Buch.-Blattnamen** auf der Registerkarte **Start** in der Gruppe **Verwalten** die Option **Liste bearbeiten** aus.  
5. In der Zeile für das Zahlungsausgangs Buch.-Blatt, das Sie verwenden möchten, um Zahlungen zu exportieren, wählen Sie das Kontrollkästchen **Zahlungsexport zulassen** aus.  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>Verbindung der Datenaustauschdefinition für eine oder mehrere Zahlungsarten mit den relevanten Zahlungsverfahren  
1. Geben Sie im Feld **Suchen** einen Wert für **Zahlungsformen** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Auf der **Zahlungsformen**-Seite wählen Sie die Zahlungsform, die verwendet wird, um Zahlungen zu exportieren, und wählen Sie dann das Feld **Definition der Zahlungsexportzeile** aus.  
3. Auf der Seite **Pmt. Export-Zeilen-Definitionen** wählen Sie den Code, den Sie im Feld **Code** im Inforegister **Zeilendefinitionen** in Schritt 4 im Bereich "Formatierung aus Zeilen und Spalten von in der Datei beschreiben" im Vorgang [Atenaustauschdefinition einrichten](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="see-also"></a>Siehe auch  
[Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Richten Sie Datenaustauschdefinitionen ein.](across-how-to-set-up-data-exchange-definitions.md)  
[Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md)  
[Daten elektronisch austauschen](across-data-exchange.md)  
