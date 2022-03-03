---
title: Erweiterung Zahlungen und Abstimmungen (DK)
description: Diese Erweiterung macht es einfach, dass Exportdateien, die vorformatiert sind, den Bankbedingungen für elektronische Posten erfüllen.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 06/24/2021
ms.author: bholtorf
ms.openlocfilehash: 6ba51935ba71c3caa6a74f2fc7a69b06d8731422
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8129916"
---
# <a name="the-payments-and-reconciliations-dk-extension"></a>Die Zahlungs- und Abstimmungs-Erweiterung

Machen Sie schnelle, fehlerfreie Zahlungen, indem Sie Dateien exportieren, die speziell für den Austausch mit Ihrem Kreditor oder Ihrer Bank formatiert werden. Diese Dateien beschleunigen die Zahlung und die Aussöhnungsprozesse und eliminieren Fehler, die auftreten können, wenn Sie versuchen, die Informationen über eine Bankwebsite einzugeben.  

Diese Erweiterung unterstützt Dateiformate für mehrere dänische Banken. Wenn Sie Zahlungsinformationen in eine Datei exportieren, packt die Erweiterungg die Daten in das Format, das Ihre Bank benötigt. Beispielsweise enthalten die Formate Bankdaten-V3, BEC, SDC und FIK, die viele unterschiedliche Banken nutzen und einige, die mehr für bestimmte Banken spezialisiert sind, zum Beispiel, Danske Bank und Nordea. Die Erweiterung enthält auch mehrere Formate für das Importieren und saldieren von Bankauszügen.  

> [!Note]
> Um die Erweiterung zu verwenden, müssen Sie das Format kennen, das die Bank oder der Kreditor benötigt. Einige Banken oder Kreditoren können diese Information auf ihren Websites bereitstellen; Sie müssen möglicherweise die Serviceabteilung kontaktieren, um die Informationen zu erhalten.  

## <a name="supported-bank-formats"></a>Unterstützte Bank-Formate
Diese Erweiterung kann folgende Dateiformate-Zahlungsdateien anwenden:  

* BANKDATA-V3  
* BEC-INDLAND  
* BEC-CSV  
* DANSKEBANK-CMKV  
* DANSKEBANK-CMKXKSX  
* DANSKEBANK  
* FIK71  
* NORDEA-ERHVERV-CSV  
* NORDEA  
* NORDEA-UNITEL-V3  
* SDC  
* SDC-CSV  

## <a name="to-set-up-the-extension"></a>Erweiterungen einrichten

Es gibt mehrere Schritte, um beginnen zu können.  

* Zahlungsexport erlauben Um Ihre Daten zu schützen, stehen diese nicht zeitnah zur Verfügung.  
* Einrichten von Einkauf und Verbindlichkeiten, sodass Sie nicht externen Belegnummern auf Rechnungen benötigen. Bei Bedarf können Sie die Referenznummer verwenden, um eine bestimmte Rechnung zu verwenden.  
* Gibt die Zahlungsform für jeden Kreditor an. Zahlungsformen definieren, wie Sie Rechnungen an Kreditoren bezahlen. Beispielsweise Bank, Kasse, Scheck oder Konto.  
* Geben Sie die Art des Formats an, das Sie für jede Ihrer Bankkonten verwenden. Zum Beispiel NORDEA, DANSKEBAN, SDC etc.  

Darüber hinaus müssen Sie Kreditoren einer inländischen **Gen. Bus. Buchungsgruppe** und **Kreditorenbuchungsgruppe** zuweisen. Die Land/Regions-Einstellung für den Kreditor muss Dänemark (DK) sein. Weitere Informationen finden Sie unter [Einrichten von Buchungsgruppen](finance-posting-groups.md).  

### <a name="to-allow-prod_short-to-export-payment-data"></a>[!INCLUDE[prod_short](includes/prod_short.md)] erlauben, Zahlungsdaten zu exportieren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zahlungsausgangs Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Projekt Buch.-Blatt bearbeiten** das Feld **Bank** Stapel aus.  
3. Wählen Sie das Kontrollkästchen **Zahlungsexport erlauben**.  

### <a name="to-specify-a-payment-method-for-a-vendor"></a>Gibt die Zahlungsform für jeden Kreditor an.

Die folgende Tabelle zeigt die FIK- und Kombinationen von GIRO-Zahlungsformen an, die [!INCLUDE[prod_short](includes/prod_short.md)] unterstützen.

|Kombination|01 eingeben | 04 eingeben | 71 eingeben | 73 eingeben |
|----|--------|---------|---------|---------|
|Girokonto-Nr. oder FIK-Gläubigerrn.? | Girokontorn. | Girokontorn. | FIK-Kreditornummer | FIK-Kreditornummer|
|Nachricht an Empfänger zulassen? | Ja |Nein |Nein | Ja |
|Enthält Zahlungs-Referenznummer? | Nein | Ja, 16 Ziffern. | Ja, 15 Ziffern. | Nein|

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kreditoren** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die Karte, erweitern Sie die Registerkarte **Zahlungen**, im Feld **Zahlungsform** und wählen Sie die Zahlungsform.  
3. Abhängig von Ihrer Wahl müssen Sie weitere Felder ausfüllen. Siehe die Tabelle oben für eine Beschreibung der Kombinationen.  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a>Das Adressformat definieren, um ein Bankkonto zu verwenden

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Bankkonten** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die Karte für das Bankkonto.  
3. Im Feld **Format Zahlungsexport** wählen Sie das Format für Ihre Exportdatei aus.  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a>Auswählen des FIK oder der Autogirozahlungsinformationen für Kreditorenrechnungen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie das Feld Debitor. Beachten Sie, dass dies ein dänischer Kreditor mit eine Adresse in Dänemark sein muss.
3. Eine Rechnung erstellen. Die Felder **Zahlungsform** und **Kreditorennummer** werden entsprechend den Einstellungen auf der Kreditorenkarte ausgefüllt. Sie können diese bei Bedarf ändern.
4. Geben Sie im Feld **Zahlungsreferenz** die Nummer mit 15 Ziffern von den Rechnungsbeträgen des Kreditors ein.  

    > [!Tip]
    > Sie müssen nur die letzten 11 Ziffern der Nummer hinzufügen. [!INCLUDE[prod_short](includes/prod_short.md)] fügt vier Null für den Anfang der Nummer hinzu.  

5. Buchen Sie die Rechnung.

## <a name="to-use-the-extension-to-export-payment-data"></a>Nutzung der Erweiterung, um Zahlungsdaten zu exportieren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zahlungsausgangs Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die **Zahlungsvorschlag-Buch.-Blätter** Aktion aus.  

    > [!Tip]
    > Wenn Sie nur bestimmte Zahlungen exportieren möchten, können Sie die Optionen zum Filtern der Daten nutzen.  

3. Bei Bedarf können Sie Filter hinzufügen, um nur bestimmte Zahlungen zu exportieren.  
4. Wählen Sie im Feld **Bankkontozahlungsart** die Option **Elektronische Zahlung** aus.  
5. Wählen Sie die Aktion **Exportieren** aus.  

## <a name="see-also"></a>Siehe auch

[Anpassen von Business Central für [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe der Erweiterungen](ui-extensions.md)  
[Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Arbeiten mit allgemeinen Buch.-Blättern](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]