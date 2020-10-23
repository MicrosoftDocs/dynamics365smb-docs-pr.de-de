---
title: 'Gewusst wie: Exportieren und Drucken von Intrastat-Berichten'
description: Intrastat-Berichterstattung ist in der gesamten Europäischen Union (EU) erforderlich und muss landesbezogenen Anforderungen entsprechen (beispielsweise bestimmten Formaten und Dateien). Alle Unternehmen innerhalb der EU sind verpflichtet, Auskunft über ihre Handelsaktivitäten mit anderen EU-Ländern zu geben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 998dc9282f526366059e665e057552fed1fbc30c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920078"
---
# <a name="export-and-print-intrastat-reports"></a>Exportieren und Drucken von Intrastat-Berichten
Intrastat-Berichterstattung ist in der gesamten Europäischen Union (EU) erforderlich und muss landesbezogenen Anforderungen entsprechen (beispielsweise bestimmten Formaten und Dateien). Alle Unternehmen innerhalb der EU sind verpflichtet, Auskunft über ihre Handelsaktivitäten mit anderen EU-Ländern zu geben. Warenbewegungen müssen jeden Monat dem Statistischen Amt Ihres Landes/Ihrer Region mitgeteilt und die Berichte müssen an die Steuerbehörden übermittelt werden.  

 Für Intrastat-Berichte müssen Sie Papierberichte und Dateien zur Verfügung stellen, die für Deutschland im ASCII-Format sein müssen. [!INCLUDE[d365fin](../../includes/d365fin_md.md)] schließt Berichte und Batchaufträgen ein, die alle Informationen generieren, die an die deutschen Steuerbehörden gesendet werden müssen. Diese Informationen umfasst automatisch alle gelieferten als auch alle erhaltenen Waren. Die Intrastat-Datei enthält die Daten, die in den Zeilen des **Intrastat**-Buchungsblatts eingetragen wurden.  

## <a name="to-print-the-german-intrastat-checklist"></a>So drucken Sie die Intrastat-Checkliste für Deutschland  

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Intrastat Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie im Feld **Buch.-Blattname** den erforderlichen Buch.-Blattnamen aus.
3.  Wählen Sie die **Bericht-Checkliste** Aktion aus.  
4.  Aktivieren Sie auf der Seite **Intrastat - Checklist DE** im Inforegister **Optionen** das Kontrollkästchen **Intrastat-Buch.-Blattzeilen anzeigen**.  

    > [!IMPORTANT]  
    >  Wenn Sie das Kontrollkästchen **Intrastat-Buch.-Blattzeilen anzeigen** deaktivieren, werden im Bericht nur die Informationen angezeigt, die an die Steuerbehörden gemeldet werden müssen, nicht jedoch die Zeilen im Buch.-Blatt.  

5.  Optional wählen Sie im Inforegister **Intrastat Buch.-Blattname** die entsprechenden Filter aus.  
6.  Optional wählen Sie im Inforegister **Intrastat Buch.-Blattname** die entsprechenden Filter aus.  
7.  Wählen Sie die Schaltfläche **Drucken** aus, um die Intrastat-Checkliste zu drucken, oder die Schaltfläche **Vorschau**, um den Bericht auf dem Bildschirm anzuzeigen.  

## <a name="to-print-the-german-intrastat-form"></a>So drucken Sie das Intrastat-Formular für Deutschland  

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Intrastat Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie im Feld **Buch.-Blattname** den erforderlichen Buch.-Blattnamen aus.  
3.  Wählen Sie die Aktion **Formular** aus.  
4.  Optional wählen Sie im Inforegister **Intrastat Buch.-Blattname** die entsprechenden Filter aus.  
5.  Optional wählen Sie im Inforegister **Intrastat Buch.-Blattname** die entsprechenden Filter aus.  
6.  Wählen Sie die Schaltfläche **Drucken** aus, um die Intrastat-Checkliste zu drucken, oder die Schaltfläche **Vorschau**, um den Bericht auf dem Bildschirm anzuzeigen.  

## <a name="to-export-intrastat-information-to-a-disk"></a>So exportieren Sie Intrastat-Informationen auf einen Datenträger  

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Intrastat Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie im Feld **Buch.-Blattname** den erforderlichen Buch.-Blattnamen aus.  
3.  Wählen Sie die **Diskette erstellen** Aktion aus.  
4.  Geben Sie im Inforegister **Optionen** im Feld **Pfad** den vollständigen Pfad und Namen der Datei ein, in die Sie die Informationen schreiben möchten.  

    Optional wählen Sie im Inforegister **Intrastat Buch.-Blattname** die entsprechenden Filter aus.  

5.  Um die Datei zu exportieren, wählen Sie die Schaltfläche **OK**, um den Export zu starten.  

Die Intrastat-Informationen werden exportiert, und Sie können entweder die Daten in einer Datei speichern oder die Datei in einem geeigneten Programm öffnen.  

 Beim Exportieren der Datei wird das Kontrollkästchen **Ausgewertet** auf der Seite **Intrastat Jnl. Buch.-Blattnamen** ausgewählt und **Interne Referenznr.** Feld für jeden Posten im Buch.-Blatt ausgefüllt. Sie können manuellen Änderungen in diesem Feld vornehmen. Sie können den Inhalt dieses Feldes auch ändern, wenn beispielsweise eine wiederholte Berichterstattung erforderlich ist. Weitere Informationen finden Sie unter Intrastat Stapelverarbeitung.  

## <a name="see-also"></a>Siehe auch  
 [MwSt.-Abrechnung](vat-reporting.md)  
 [Melden von MwSt. an die Steuerbehörden](../../finance-how-report-vat.md)
