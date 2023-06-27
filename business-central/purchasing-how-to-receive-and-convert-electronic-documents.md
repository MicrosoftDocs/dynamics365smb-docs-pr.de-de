---
title: 'Vorgehensweise: Elektronische Belege empfangen und konvertieren'
description: 'Dieses Thema beschreibt, wie Sie elektronische Belege direkt von Handelspartnern oder von einem OCR-Dienst empfangen können.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '189, 190, 191'
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="receive-and-convert-electronic-documents" />Vorgehensweise: Elektronische Belege empfangen und konvertieren

Die generische Version von [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt das Empfangen von elektronischen Rechnungen und Gutschriften im PEPPOL-Format, das von den wichtigsten Anbietern von Belegaustauschdiensten unterstützt wird. Um beispielsweise eine Rechnung von einem Kreditor in Form eines elektronischen PEPPOL-Belegs zu erhalten, verarbeiten Sie den Beleg auf der Seite Eingehende Belege, um diesen in eine Einkaufsrechnung oder Fibu Buch.-Blattzeile in [!INCLUDE[prod_short](includes/prod_short.md)] zu konvertieren.

Zusätzlich zur Empfangen von elektronischen Dokumenten direkt von Handelspartnern können Sie elektronische Belege von einem OCR-Dienst erhalten, der Ihre PDF- oder Bilddateien in elektronische Belege umgewandelt hat.  

Bevor Sie elektronische Belege durch den Belegaustauschdienst empfangen können, müssen Sie verschiedene Stammdaten (wie Firmendaten, Kreditoren, Artikel und Einheiten) einrichten. Diese werden verwendet, um Geschäftspartner und Artikel zu identifizieren, wenn Daten in Elementen im eingehenden Beleg zu Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] konvertiert werden. Weitere Informationen finden Sie unter [Belegaustausch-Dienst](across-how-to-set-up-a-document-exchange-service.md).  

Bevor Sie elektronische Belege vom OCR-Dienst empfangen können, müssen Sie die vorkonfigurierte Serviceverbindung einrichten und aktivieren. Weitere Informationen finden Sie unter [Eingehende Belege einrichten](across-how-setup-income-documents.md).  

Der Verkehr von elektronischen Belegen in und aus [!INCLUDE[prod_short](includes/prod_short.md)] wird durch die Funktion Aufgabenwarteschlange verwaltet. Bevor Sie elektronische Belege empfangen können, muss die betreffende Projektwarteschlange gestartet werden.  

Sie können die Konvertierung von elektronischen Belegen entweder manuell beginnen, wie in diesem Verfahren beschrieben, oder Sie können einen Workflow aktivieren, der elektronische Belege automatisch konvertiert, wenn sie eintreffen. Die generische Version von [!INCLUDE[prod_short](includes/prod_short.md)] enthält die Workflowvorlage *Eingehenden elektronischen Beleg über OCR bis Einkaufsrechnung öffnen – Workflow*, die in einen Workflow kopiert und aktiviert werden kann. Weitere Informationen finden Sie unter [Workflow](across-workflow.md)  

> [!NOTE]  
> Wenn Sie die aus dem OCR-Service erhalten elektronischen Belege in die Belege oder Buch.-Blattzeilen in [!INCLUDE[prod_short](includes/prod_short.md)] umwandeln, dann werden mehrere Zeilen im Herkunftsbeleg in einer Zeile summiert. Die einzelne Zeile hat den Typ "Sachkonto" und die Felder **Beschreibung** und Sachkonto **Nr.** sind leer. Felder sind leer. Der Wert im Feld **Betrag** entspricht dem Gesamtbetrag ohne MwSt. aller Zeilen im Herkunftsbeleg.  
>
> Um sicherzustellen dass **Beschreibung** und **Nr.** Felder sind ausgefüllt, Sie können die Schaltfläche **Text zu Konto zuordnen** auf der Seite **Eingehende Belege** auswählen. Hiermit legen Sie fest, dass ein bestimmter Rechnungstext immer einem bestimmten Soll- oder Habenkonto in der Finanzbuchhaltung zugeordnet wird. Dadurch wird das Feld **Beschreibung** in Belegen oder Buch.-Blattzeilen, die aus einem elektronischen Beleg für diesen Kreditor oder Debitor erstellt werden, mit dem entsprechenden Text ausgefüllt, und das Feld Sachkonto **Nr.** Feld mit dem fraglichen Konto ergänzt.  
>
> Anstelle der Zuordnung zu einem Sachkonto können Sie auch ein Bankkonto zuordnen. Dies ist beispielsweise für elektronische Belege für Ausgaben nützlich, die bereits bezahlt wurden, für die Sie jedoch eine Fibu Buch.-Blattzeile erstellen möchten, die auf ein Bankkonto buchen kann.  

Die folgenden Schritte zeigen, wie Sie eine Kreditorenrechnungen empfangen und in eine Einkaufsrechnung in [!INCLUDE[prod_short](includes/prod_short.md)] konvertieren können. Der Vorgang ist derselbe wie beim Konvertieren einer Kreditorenrechnung in eine Fibu Buch.-Blattzeile.  

### <a name="to-receive-and-convert-an-electronic-invoice-to-a-purchase-invoice" />So empfangen Sie eine elektronische Rechnung und konvertieren sie in eine Einkaufsrechnung:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Eingehende Belege** ein und wählen Sie dann den zugehörigen Link.  

2. Markieren Sie die Zeile für den Eingangsdatensatz, der eine neue elektronische Eingangsrechnung darstellt, und wählen Sie dann die Aktion **Bearbeiten**.  

    Auf der Seite **Eingehende Belege** wird die entsprechende XML-Datei angehängt, und die meisten Felder werden mit den Informationen aus der elektronischen Rechnung ausgefüllt. Weitere Informationen finden Sie unter [So geht's: Eingehende Belege erstellen](across-how-create-income-document-records.md).  

3. Wählen Sie im Feld **Datenaustauschart** die Option **PEPPOL - Rechnung** oder **OCR - Rechnung** aus, je nachdem, woher der elektronische Beleg stammt.  

4. Um Text in der Kreditorenrechnung einem bestimmten Sollkonto zuzuordnen, wählen Sie auf der Registerkarte **Aktion** in der Gruppe **Allgemein** die Option **Text zu Konto zuordnen**, und füllen Sie dann die Seite **Kontozurodnungsarbeitsblatt** aus.  

5. Wählen Sie die Aktion **Dokument erstellen**.  

    Eine Einkaufsrechnung wird in [!INCLUDE[prod_short](includes/prod_short.md)] basierend auf den Daten im elektronischen Beleg erstellt.  

    Überprüfungsfehler, die üblicherweise mit falschen oder fehlenden Stammdaten in [!INCLUDE[prod_short](includes/prod_short.md)] zusammenhängen, werden im Inforegister **Fehlermeldungen** angezeigt.  

## <a name="see-related-microsoft-training" />Siehe verwandte [Microsoft Schulungen](/training/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also" />Siehe auch

[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Eingehende Belege](across-income-documents.md)  
[Einrichten von Senden und Empfangen von elektronischen Belegen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Daten elektronisch austauschen](across-data-exchange.md)   
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
