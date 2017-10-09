---
title: 'Vorgehensweise: Verwalten der Abwesenheit von Mitarbeitern| Microsoft Docs'
description: Beschreibt, wie die Abwesenheit von Mitarbeitern erfasst wird und Abwesenheitsstatistiken analysiert werden.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/08/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4c5ce7e72c7084995b16b574f3ad670c815ef9ee
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-manage-employee-absence"></a>Vorgehensweise: Verwalten Sie die Abwesenheit von Mitarbeitern
Damit die Abwesenheit eines Mitarbeiters verwaltet werden kann, muss diese im Fenster **Abwesenheitsregistrierung** aufgezeichnet werden. Sie kann dann auf verschiedene Art und Weise zur Analyse und Berichterstellungszwecken angezeigt werden.

Mitarbeiterabwesenheit kann in zwei unterschiedlichen Fenstern angezeigt werden:

* Das Fenster **Abwesenheitsregistrierung**, in dem Sie alle Abwesenheitszeiten von Mitarbetiern mit einer Zeile pro Fehlzeit erfassen.
* Das Fenster **Mitarbeiter Abwesenheiten**, in dem lediglich die Abwesenheitszeiten für einen Mitarbeiter angezeigt werden. Hierbei handelt es sich um die Informationen, die im Fenster **Abwesenheitsregistrierung** eingegeben wurden – gefiltert nach einem bestimmten Mitarbeiter.

Verwenden Sie immer die gleiche Einheit (Stunden oder Tage), wenn Sie Mitarbeiterabwesenheiten registrieren, um eine aussagekräftige Statistik zu erhalten.

## <a name="to-register-employee-absence"></a>So erfassen Sie die Abwesenheit eines Mitarbeiters
Sie können die Mitarbeiterabwesenheiten auf täglicher Basis oder einem anderen Intervall erfassen, das Ihre organisatorischen Anforderungen erfüllt.

1. Wählen Sie in der rechten oberen Ecke das Symbol **Nach Seite oder Bericht suchen** und geben **Abwesenheitsregistrierung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie für Mitarbeiterabwesenheit, die Sie erfassen möchten, eine Zeile aus.
4. Schließen Sie das Fenster.

    > [!Tip]
    > Verwenden Sie immer die gleiche Einheit (Stunden oder Tage), wenn Sie Mitarbeiterabwesenheiten registrieren, um aussagekräftige Statistiken zu erhalten.

## <a name="to-view-an-individual-employees-absence"></a>So zeigen Sie die Abwesenheit für einen einzelnen Mitarbeiter an
1. Wählen Sie in der rechten oberen Ecke das Symbol **Nach Seite oder Bericht suchen** und geben **Mitarbeiter** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie den entsprechenden Mitarbeiter aus und wählen Sie dann die Aktion **Abwesenheiten** aus.

    Das Fenster **Mitarbeiter Abwesenheiten** wird geöffnet und zeigt alle Abwesenheiten sowie deren Beginn und Ende an.

## <a name="to-view-an-employees-absence-by-categories"></a>So zeigen Sie die Abwesenheit eines Mitarbeiters nach Kategorien an
1. Wählen Sie in der rechten oberen Ecke das Symbol **Nach Seite oder Bericht suchen** und geben **Mitarbeiter** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie den entsprechenden Mitarbeiter aus und wählen Sie dann die Aktion **Abwesenheiten nach Kategorien** aus.
3. Im Fenster **Mitarbeiter Abw. n. Kategorien** füllen Sie die Filterfelder bedarfsgerecht aus und wählen Sie dann die Aktion **Matrix anzeigen** aus.

    Das Fenster **Mitarbeiter Abw. n. Kat. Matr.** wird geöffnet und zeigt alle Abwesenheiten an, aufgeschlüsselt nach Abwesenheitsgründen.

## <a name="to-view-all-employee-absences-by-category"></a>So zeigen Sie alle Mitarbeiterabwesenheiten nach Kategorie an
1. Wählen Sie in der rechten oberen Ecke das Symbol **Nach Seite oder Bericht suchen** und geben **Abwesenheitsregistrierung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Abwesenheitsregistrierung** die Aktion **Übersicht nach Kategorien** aus.
3. Legen Sie im Fenster **Abwesenheit nach Kategorien** einen Filter im Feld **Mitarbeiternr. Filter** fest, um Mitarbeiterabwesenheiten für einzelne Mitarbeiter oder eine definierte Gruppe von Mitarbeitern anzuzeigen.
4. Wählen Sie die Aktion **Matrix anzeigen** aus.

    Das Fenster **Abwesenheit nach Kategorien - Matrix** wird geöffnet und zeigt alle Abwesenheiten von Mitarbeitern an, aufgeschlüsselt nach den einzelnen Abwesenheitsursachen.

## <a name="to-view-all-employee-absences-by-period"></a>So zeigen Sie alle Mitarbeiterabwesenheiten nach Perioden an
1. Wählen Sie in der rechten oberen Ecke das Symbol **Nach Seite oder Bericht suchen** und geben **Abwesenheitsregistrierung** ein. Wählen Sie dann den zugehörigen Link aus.
   Wählen Sie im Fenster **Abwesenheitsregistrierung** die Aktion **Übersicht nach Perioden** aus.
2. Legen Sie im Fenster **Abwesenheiten nach Perioden** einen Filter im Feld **Abwesenheitsgrundfilter** fest, um die Abwesenheiten von Mitarbeitern nach bestimmten Abwesenheitsursachen anzuzeigen.
3. Wählen Sie die Aktion **Matrix anzeigen** aus.

    Das Fenster **Abwesenheiten nach Perioden - Matrix** wird geöffnet und zeigt Abwesenheiten von Mitarbeitern an, aufgeschlüsselt nach Perioden.

## <a name="see-also"></a>Siehe auch
[Personalwesen verwalten](hr-manage-human-resources.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Anpassen der[!INCLUDE[d365fin](includes/d365fin_md.md)]Erfahrung](ui-experiences.md)

