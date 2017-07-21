---
title: "Verwalten Sie die MwSt, die an die Steuerbehörden gemeldet wird| Microsoft Docs"
description: "Erfahren Sie, wie Sie einen Bericht erstellen, der die MwSt aus Verkäufen in einer Zeilenliste in einer Periode darstellt, und übermitteln Sie den Bericht auf einer Steuerbehörde."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9b0db56fc08881a94b1f80bafed32d7bcbc24fd8
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---

# <a name="how-to-report-vat-to-tax-authorities"></a>So gehts: Melden von MwSt. an die Steuerbehörden
Der Verkaufslistenbericht der MwSt-Beträge der Europäischen Union (EU), die Sie für Debitoren innerhalb der EU eingetrieben haben, damit Sie die MwSt.-Beträge dem Webdienst einer Behörde übermitteln können.

> [!NOTE]  
>   In Großbritannien müssen alle Unternehmen, die mehr verkaufen, als einen bestimmten Wert jedes Jahr an Debitoren in EU-Mitgliedsstaaten eine elektronische Version aus seiner Europäischen Europäischen Union (EC)-, buchen,dasverkäufe Bericht im XML-Format-Format mit deren Website der Majestät Einnahmen- und Gewohnheits()HMRC auflisten.

Der EU-Verkaufsübersichts-Bericht passt nur für Länder in der EU. Beispielsweise enthält er keine MwSt für Verkäufe in Länder wie China oder den USA.

Um MwSt an eine Steuerbehörden zu übermitteln, müssen Sie den [!INCLUDE[d365fin](includes/d365fin_md.md)] mit der Steuerbehörde verbinden. Dazu ist es erforderlich, dass Sie ein Konto mit Ihrer Steuerbehörden einrichten. Wenn Sie ein Konto haben, können Sie eine Dienst-Verbindung ausführen, die wir in [!INCLUDE[d365fin](includes/d365fin_md.md)] voraussetzen. Zum Beispiel bei Großbritannien können Sie die **GovTalk** Dienst-Verbindung verwenden.

Der Bericht enthält eine Zeile für jede Art Transaktion mit dem Debitor und zeigt den Gesamtbetrag für jede Art von Transaktionen an. Es gibt drei Arten von Transaktionen, die der Bericht enthalten kann:  
  
* B2B-Waren  
* B2B-Dienste  
* Triangulierte Waren B2Bs  
  
B2B-Waren und Dienste geben an, ob Sie eine Ware oder einen Dienst verkauften, und werden durch die **EU-Service** in der MwSt.-Einrichtung gesteuert. Triangulierte Waren B2Bs geben an, ob Sie sich im Einzelhandel mit einem Kreditor engagierten und durch die Einstellung **EU-Dreiecksgeschäft** in Verkaufsbelegen, wie Aufträge, Rechnungen, Gutschriften, usw. gesteuert werden.  
  
Nachdem Sie den Bericht gesendet haben, überwacht [!INCLUDE[d365fin](includes/d365fin_md.md)] den Service und bewahrt einen Datensatz Ihrer Kommunikation auf. Das Feld **Status** gibt an, wo der Bericht in Bearbeitung ist. Beispielsweise wenn die Behörden Ihren Bericht verarbeiten, ändert sich der Status des Berichts auf **Erfolgreich**. Wenn die Steuerbehörde Fehler im Bericht finden, erhält der Bericht den Status **Fehler**. Sie können die Fehler unter **Fehler und Warnungen** anzeigen, korrigieren und den Bericht erneut senden. Um eine Liste Ihrer EU-Verkaufsübersichts-Berichte anzuzeigen, wechseln Sie zur Seite **EU-Verkaufsübersichts-Berichte**.  
  
> [!NOTE]  
>   Wenn Sie eine andere Methode verwenden, um den Bericht zu buchen, indem Sie beispielsweise die XML exportieren und sie in eine Steuerbehördenwebsite, können Sie sie danach **als übermittet markieren**, um den Berichtszeitraum zu schließen. Wenn Sie den Bericht als freigegeben kennzeichnen, ist er nicht mehr editierbar. Wenn Sie die Erklärung ändern müssen, nachdem Sie sie als freigegeben gekennzeichnet haben, müssen Sie sie zuerst erneut öffnen. 
  
Nachdem die Steuerbehörden den Bericht erneut erstellen, senden Sie eine E-Mail an die Kontaktperson des Unternehmens. In [!INCLUDE[d365fin](includes/d365fin_md.md)], wird die Kontaktperson auf der Seite **Firmendaten** angegeben. Bevor Sie den Bericht senden, prüfen Sie, ob eine Kontaktperson ausgewählt ist.

<!--> [!NOTE]  
>   Der EU-Verkaufsübersichts-Bericht kann bis 1000 Zeilen enthalten. Wenn Sie mehr Zeilen haben, müssen Sie einen anderen Bericht senden. -->

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Um sich mit der Webdienst Ihrer Steuerbehörde zu verbinden
[!INCLUDE[d365fin](includes/d365fin_md.md)] stellt die Dienst-Verbindungen bereit, die an die Steuerbehördenwebsites anschließen. Zum Beispiel wenn sie in Großbritannien sind, müssen Sie die **GovTalk** Dienst-Verbindung verwenden.  

1. In dem Feld **Nach Seiten oder Berichte suchen** geben Sie **Dienstverbindungen** ein und wählen Sie dann entsprechenden Link aus. <!-- remember to get the updated text for this-->  
2. Füllen Sie die entsprechenden Felder aus.  

## <a name="to-set-up-the-ec-sales-list-report"></a>Den EU-Verkaufsübersichts-Bericht einrichten
1. In dem Feld **Nach Seiten oder Berichte suchen** geben Sie **MwSt Bericht einrichten** ein und wählen Sie dann entsprechenden Link aus.  
2. Wenn Sie Benutzer diesen Bericht ändern und erneut senden wollen, wählen Sie das Kontrollkästchen **Übermittelte Berichte ändern**.  
3. Geben Sie die Nummernserie an, die für EU-Verkaufsübersichts-Berichte zu verwenden ist.  

## <a name="to-prepare-and-submit-the-ec-sales-list-report"></a>Um den EU-Verkaufsübersichts-Bericht vorzubereiten und zu buchen
1. In dem Feld **Nach Seiten oder Berichte suchen** geben Sie **EU-Verkaufsliste** ein und wählen Sie dann den entsprechenden Link aus.  
2. Wählen Sie Aktion **Neu** aus, und füllen Sie die relevanten Felder aus.  
3. Um den Inhalt des Berichts zu erstellen, wählen Sie die **Vorschlagszeilen** Aktion.  

    > [!NOTE]  
>   Sie können die Transaktionen überprüfen, die in der Zeile erfasst werden, bevor Sie den Bericht senden. Wählen Sie die Zeile mit der Verteilung, und wählen Sie dann die Aktion **MwSt-Einträge anzeigen** aus.  
4. Um einen Bericht für die Übermittlung vorzubereiten, wählen Sie die **Freigeben** Aktion.  
5. Um den Bericht zu buchen, wählen Sie die **Übermitteln** Aktion.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] prüft, ob der Bericht korrekt eingerichtet ist. Wenn die Prüfung fehlschlägt, werden die Fehler im Fenster **Fehler und Warnungen**  angezeigt, sodass Sie entsprechende Änderungen vornehmen können.

## <a name="viewing-communications-with-your-tax-authority"></a>Zeigt den Verlauf der Kommunikation mit der Steuerbehörde an
In einigen Ländern tauschen Sie Meldungen mit Steuerbehörden aus, wenn Sie Berichte senden. Sie können die erste und letzte Meldung anzeigen, die Sie gebucht oder erhalten haben, indem Sie die Aktionen **Übermittlungsnachricht herunterladen** und **Antwornachricht herunterladen** gewählt haben.  

## <a name="configuring-your-own-vat-reports"></a>MwSt-Bericht konfigurieren
Sie können den EU-Verkaufsübersichts-Berichtsstandard verwenden, aber Sie können auch eigene Berichte erstellen. Dazu ist es erforderlich, dass Sie mehrere Codeunits erstellen. Wenn Sie Hilfe benötigen, kontaktieren Sie einen Microsoft Partner.  
    
Die folgende Tabelle beschreibt Codeunits, die Sie für den Bericht erstellen müssen.

| Codeunit | Was sie tun müssen |
|----|-----|
|Vorschlagszeilen| Abrufen von Informationen aus der Tabelle MwSt.-Posten und sie in den Zeilen des MwSt-Berichts anzeigen|
|Inhalt | Kontollieren Sie das Format des Berichts. Beispielsweise ob es XML oder JSON ist. Das Format, das zu verwenden ist, hängt von den Anforderungen des Webdiensts Ihrer Steuerbehörden ab. |
|Übermittlung | Steuern Sie, wie und wann Sie den Bericht basierend auf den Anforderungen Ihrer Steuerbehörden senden. |
|Antwort-Handler | Bearbeit die Antwort der Steuerbehörden. Beispielsweise sendet sie eine E-Mail an die Kontaktperson Ihres Mandanten. |
|Abbrechen | Senden Sie eine Stornierung eines MwSt-Berichts, der zuvor zu Ihrer Steuerbehörden gesendet wurde. |

> [!NOTE]  
>   Wenn Sie Codeunits für den Bericht erstellen, passen Sie auf den Wert im Feld **MwSt Berichts-Version** auf. Dieses Feld muss der Version des Berichts entsprechen, der von der Steuerbehörde verlangt wurde oder verlangt wird. Beispielsweise können Sie**2017** in dieses Feld eingeben, um anzugeben, dass der Bericht der Anforderungen entspricht, die im letzten Jahr verlangt wurden. Um die aktuellen Version zu finden, setzen Sie sich mit den Steuerbehörden in Verbindung.  

## <a name="see-also"></a>Siehe auch
[MwSt. einrichten](finance-setup-vat.md)  
[Verkauf einrichten](sales-setup-sales.md)  
[Vorgehensweise: Fakturieren](sales-setup-sales.md)  

