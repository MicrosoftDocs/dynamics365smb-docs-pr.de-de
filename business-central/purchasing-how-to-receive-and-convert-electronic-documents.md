---
title: 'Vorgehensweise: Elektronische Belege empfangen und konvertieren | Microsoft Docs'
description: -Sie können elektronische Belege direkt aus den Handelspartnern oder einem OCR-Dienst erhalten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e9543d9fc361f2948907bc0e84d37dd870139cd8
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2019
ms.locfileid: "2553866"
---
# <a name="receive-and-convert-electronic-documents"></a>Vorgehensweise: Elektronische Belege empfangen und konvertieren
Die generische Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt das Empfangen von elektronischen Rechnungen und Gutschriften im PEPPOL-Format, das von den wichtigsten Anbietern von Belegaustauschdiensten unterstützt wird. Um beispielsweise eine Rechnung von einem Kreditor in Form eines elektronischen PEPPOL-Belegs zu erhalten, verarbeiten Sie den Beleg auf der Seite Eingehende Belege, um diesen in eine Einkaufsrechnung oder Fibu Buch.-Blattzeile in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu konvertieren.

 Zusätzlich zur Empfangen von elektronischen Dokumenten direkt von Handelspartnern können Sie elektronische Belege von einem OCR-Dienst erhalten, der Ihre PDF- oder Bilddateien in elektronische Belege umgewandelt hat.  

 Bevor Sie elektronische Belege durch den Belegaustauschdienst empfangen können, müssen Sie verschiedene Stammdaten (wie Firmendaten, Kreditoren, Artikel und Einheiten) einrichten. Diese werden verwendet, um Geschäftspartner und Artikel zu identifizieren, wenn Daten in Elementen im eingehenden Beleg zu Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] konvertiert werden. Weitere Informationen finden Sie unter [Belegaustausch-Dienst](across-how-to-set-up-a-document-exchange-service.md).  

 Bevor Sie elektronische Belege vom OCR-Dienst empfangen können, müssen Sie die vorkonfigurierte Serviceverbindung einrichten und aktivieren. Weitere Informationen finden Sie unter [Eingehende Belege einrichten](across-how-setup-income-documents.md).  

 Der Verkehr von elektronischen Belegen in und aus [!INCLUDE[d365fin](includes/d365fin_md.md)] wird durch die Funktion Aufgabenwarteschlange verwaltet. Bevor Sie elektronische Belege empfangen können, muss die betreffende Projektwarteschlange gestartet werden.  

 Sie können die Konvertierung von elektronischen Belegen entweder manuell beginnen, wie in diesem Verfahren beschrieben, oder Sie können einen Workflow aktivieren, der elektronische Belege automatisch konvertiert, wenn sie eintreffen. Die generische Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] enthält die Workflowvorlage *Eingehenden elektronischen Beleg über OCR bis Einkaufsrechnung öffnen – Workflow*, die in einen Workflow kopiert und aktiviert werden kann. Weitere Informationen finden Sie unter [Workflow](across-workflow.md)  

> [!NOTE]  
>  Wenn Sie die aus dem OCR-Service erhalten elektronischen Belege in die Belege oder Buch.-Blattzeilen in [!INCLUDE[d365fin](includes/d365fin_md.md)] umwandeln, dann werden mehrere Zeilen im Herkunftsbeleg in einer Zeile summiert. Die einzelne Zeile hat den Typ "Sachkonto" und die Felder **Beschreibung** und Sachkonto **Nr.** sind leer. Felder sind leer. Der Wert im Feld **Betrag** entspricht dem Gesamtbetrag ohne MwSt. aller Zeilen im Herkunftsbeleg.  
>   
>  Um sicherzustellen dass **Beschreibung** und **Nr.** Felder ausgefüllt sind, können Sie die Schaltfläche **Text zu Konto zuordnen** auf der Seite **Eingehende Belege** auswählen. Hiermit legen Sie fest, dass ein bestimmter Rechnungstext immer einem bestimmten Soll- oder Habenkonto in der Finanzbuchhaltung zugeordnet wird. Dadurch wird das Feld **Beschreibung** in Belegen oder Buch.-Blattzeilen, die aus einem elektronischen Beleg für diesen Kreditor oder Debitor erstellt werden, mit dem entsprechenden Text ausgefüllt, und das Feld Sachkonto **Nr.** Feld mit dem fraglichen Konto ergänzt.  
>   
>  Anstelle der Zuordnung zu einem Sachkonto können Sie auch ein Bankkonto zuordnen. Dies ist beispielsweise für elektronische Belege für Ausgaben nützlich, die bereits bezahlt wurden, für die Sie jedoch eine Fibu Buch.-Blattzeile erstellen möchten, die auf ein Bankkonto buchen kann.  

 Die folgenden Schritte zeigen, wie Sie eine Kreditorenrechnungen empfangen und in eine Einkaufsrechnung in [!INCLUDE[d365fin](includes/d365fin_md.md)] konvertieren können. Der Vorgang ist derselbe wie beim Konvertieren einer Kreditorenrechnung in eine Fibu Buch.-Blattzeile.  

### <a name="to-receive-and-convert-an-electronic-invoice-to-a-purchase-invoice"></a>So empfangen Sie eine elektronische Rechnung und konvertieren sie in eine Einkaufsrechnung:  

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Eingehende Belege** ein, und wählen dann den zugehörigen Link aus.  

2.  Markieren Sie die Zeile für den Eingangsdatensatz, der eine neue elektronische Eingangsrechnung darstellt, und wählen Sie dann die Aktion **Bearbeiten**.  

     Auf der Seite **Eingehende Belege** wird die entsprechende XML-Datei angehängt, und die meisten Felder werden mit den Informationen aus der elektronischen Rechnung ausgefüllt. Weitere Informationen finden Sie unter [So geht's: Eingehende Belege erstellen](across-how-create-income-document-records.md).  

3.  Wählen Sie im Feld **Datenaustauschart** die Option **PEPPOL - Rechnung** oder **OCR - Rechnung** aus, je nachdem, woher der elektronische Beleg stammt.  

4.  Um Text in der Kreditorenrechnung einem bestimmten Sollkonto zuzuordnen, wählen Sie auf der Registerkarte **Aktion** in der Gruppe **Allgemein** die Option **Text zu Konto zuordnen**, und füllen Sie dann die Seite **Kontozurodnungs** aus.  

5.  Wählen Sie die Aktion **Dokument erstellen**.  

     Eine Einkaufsrechnung wird in [!INCLUDE[d365fin](includes/d365fin_md.md)] basierend auf den Daten im elektronischen Beleg erstellt.  

     Überprüfungsfehler, die üblicherweise mit falschen oder fehlenden Stammdaten in [!INCLUDE[d365fin](includes/d365fin_md.md)] zusammenhängen, werden im Inforegister **Fehlermeldungen** angezeigt.  

## <a name="see-also"></a>Siehe auch  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Eingehende Belege](across-income-documents.md)  
[Einrichten des Senden und Empfangen von elektronischen Belegen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Daten elektronisch austauschen](across-data-exchange.md)   
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
