---
title: "So geht&quot;s: Verarbeiten einer Einkaufsrücklieferung oder von Stornierungen | Microsoft Docs"
description: "Vorgehensweise: Verarbeiten einer Verkaufsrücklieferung oder von Stornierungen"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: cf471e0c3a13a954ab7604a8b1d0f715f664722d
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-process-sales-returns-or-cancellations"></a>Vorgehensweise: Verarbeiten einer Verkaufsrücklieferung oder von Stornierungen
Wenn Ihr Debitor Artikel zurückschicken oder Dienstleistungen löschen will, die Sie verkauft haben, können Sie eine Einkaufsgutschrift erstellen und buchen, die die angeforderte Änderung im Hinblick auf die ursprünglichen Einkaufsrechnung angibt. Um korrekte Verkaufsrechnungsinformationen zu berücksichtigen, können Sie die Verkaufsgutschrift aus der gebuchten Verkaufsrechnung erstellen oder eine Kopierfunktion verwenden.  

**Hinweis:** Wenn eine gebuchte Verkaufsrechnung noch nicht bezahlt wurde, können Sie die Funktionen **Korrigieren** oder **Abbrechen** auf der gebuchten Verkaufsrechnung verwenden, um die entsprechenden Transaktionen automatisch zu stornieren. Diese Funktionen gehen nur für nicht geleistete Rechnungen, und sie unterstützen nicht Teil-Reklamationen oder Stornierungen. Weitere Informationen finden Sie unter [Vorgehensweise: Ändern oder löschen von unbezahlten Verkaufsrechnungen]](sales-how-correct-cancel-sales-invoice.md).

Zusätzlich zur ursprünglich gebuchten Verkaufsrechnung können Sie die Verkaufsgutschrift für andere Verkaufsbelege übernehmen, beispielsweise einer anderen gebuchten Verkaufsrechnung, da der Debitor auch die Artikel zurücksendet, die mit dieser Rechnung geliefert werden.

Eine Rücklieferungs- oder eine Vergütung kann sich nur auf einige der Artikel oder der Services in der ursprünglichen Verkaufsrechnung beziehen. In diesem Fall müssen Sie Informationen in den Zeilen der Verkaufsgutschrift bearbeiten. Wenn Sie die Verkaufsgutschrift buchen, werden die Verkaufsbelege, die von Änderungen betroffen sind rückgängig gemacht und eine Rückerstattung für den Debitor wird erstellt.  

Sie können die gebuchte Verkaufsgutschrift an den Debitor senden, um die Rücksendung oder Stornierung zu bestätigen und mitzuteilen, dass der zugehörige Wert erstattet werden wird, wenn zum Beispiel Artikel zurückgegeben werden oder eine Service-Stornierung vereinbart wurde.  

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Erstellt eine neue Verkaufsgutschrift, um eine gebuchte Verkaufsrechnung zurückzusetzen.
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus! ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Gebuchte Verkaufsrechnungen** eingeben und den entsprechenden Link auswählen.  
2. Wählen Sie das Feld **Gebuchte Verkaufsrechnung**, um das Fenster **Korrekturgutschrift erstellen** zu öffnen, und wählen Sie die gebuchte Verkaufsrechnung aus, die Sie stornieren möchten.

    Der Verkaufsgutschriftskopf enthält einige Informationen aus der gebuchten Verkaufsrechnung. Sie können alle Felder bearbeiten, zum Beispiel mit neuen Daten, die die Rückholvereinbarung wiedergeben.  
3. Bearbeiten Sie Informationen über die Zeilen entsprechend der Vereinbarung, wie die Anzahl der zurückzuerstattenden Artikel oder der gutzuschreibende Betrag.
4. Wählen Sie die Aktion **Posten ausgleichen...** aus.
5. Im Fenster **Debitorenposten zuweisen** wählen Sie die Zeile mit dem gebuchten Verkaufsbeleg, die Sie der Verkaufsgutschrift zuordnen möchten, und wählen Sie dann **Zuweisungs-ID festlegen** aus.

    Die Kennzeichnung der Verkaufsgutschrift wird im Feld **Zuweisungs-ID** angezeigt.
6. Geben Sie in jeder Zeile im Feld **Anzuwendender Betrag** den Betrag ein, den Sie ausgleichen möchten, wenn dieser kleiner ist als der ursprüngliche Betrag.  

    Im unteren Bereich des Fensters **Debitorenposten zuweisen** können Sie den Gesamtbetrag sehen, um alle beteiligten Posten zu stornieren, nämlich wenn der Wert im Feld **Saldo** Null ist.
7. Wählen Sie die Schaltfläche **OK** aus. Wenn Sie die Verkaufsgutschrift buchen, wird sie für die angegebenen gebuchten Verkaufsrechnungen angewandt.

    Nachdem Sie die erforderlichen Verkaufsgutschriftszeilen erstellt ober bearbeitet haben, und der Ausgleich einzelner oder mehrerer Posten angegeben wird, können Sie fortfahren, die Verkaufsgutschrift zu buchen.   
8. Wählen Sie die Aktion **Buchen und Senden** aus.  

Das Dialogfeld **Buchungs- und Sendebestätigung** wird geöffnet und zeigt die bevorzugte Sendemethode für den Debitor an. Sie können die Sendemethode ändern, indem Sie die Schaltfläche vom Feld **Beleg senden an** auswählen. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).  

Die gebuchten Verkaufsdokumente für die entsprechende Gutschrift werden nun storniert und eine Erstattung der Zahlung kann für den Debitor erstellt werden. Die Verkaufsgutschrift wird entfernt und durch einen neuen Beleg in der Liste der gebuchten Verkaufsgutschriften ersetzt.

## <a name="to-create-a-sales-credit-memo-from-scratch"></a>So erstellen Sie eine Verkaufsgutschrift von Grund auf
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus! ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Gebuchte Verkaufsrechnungen** eingeben und den entsprechenden Link auswählen.„”
2. Wählen Sie **Neu**, um eine neue leere Verkaufsgutschrift zu öffnen.
3. Geben Sie im Feld **Debitor** den Namen eines vorhandenen Debitors ein.
4. Wählen Sie die **Beleg kopieren**-Aktion aus.
5. Wählen Sie im Fenster **Verkaufsdokument kopieren** im Feld **Dokumenttyp** **Rechnung buchen** aus.
6. Wählen Sie das Feld **Belegnummer**, Wählen Sie das Feld **Gebuchte Verkaufsrechnung.** und wählen Sie dann die gebuchte Verkaufsrechnung aus, die die Zeile enthält, die Sie stornieren möchten.
7. Wählen Sie das Kontrollkästchen **Zeilen neu berechnen**, wenn die kopierten gebuchten Verkaufsrechnungszeilen, mit einzelnen Änderungen im Artikelpreis und im Einstandspreis, aktualisiert werden sollen, da die Rechnung gebucht wurde.
8. Wählen Sie die Schaltfläche **OK** aus. Die kopierten Rechnungszeilen werden in die Verkaufsgutschrift eingefügt.
9. Schließen Sie die Verkaufsgutschrift ab, so wie dies unter "Verkaufsgutschrift von Grund auf erstellen" in diesem Thema erklärt ist.

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Gewusst wie: Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]

