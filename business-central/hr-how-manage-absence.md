---
title: Verwalten der Abwesenheit von Mitarbeitern| Microsoft Docs
description: Beschreibt, wie die Abwesenheit von Mitarbeitern erfasst wird und Abwesenheitsstatistiken analysiert werden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 89f164207b78a9b1845ed7add0b6dea7c4b6efbc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782138"
---
# <a name="manage-employee-absence"></a>Analysiert die Fehlzeiten der Mitarbeiter.
Damit die Abwesenheit eines Mitarbeiters verwaltet werden kann, muss diese auf der Seite **Abwesenheitsregistrierung** aufgezeichnet werden. Sie kann dann auf verschiedene Art und Weise zur Analyse und Berichterstellungszwecken angezeigt werden.

Mitarbeiterabwesenheiten können auf zwei unterschiedlichen Seiten angezeigt werden:

* Die Seite **Abwesenheitsregistrierung**, in dem Sie alle Abwesenheitszeiten von Mitarbetiern mit einer Zeile pro Fehlzeit erfassen.
* Die Seite **Mitarbeiter Abwesenheiten**, in dem lediglich die Abwesenheitszeiten für einen Mitarbeiter angezeigt werden. Hierbei handelt es sich um die Informationen, die auf der Seite **Abwesenheitsregistrierung** eingegeben wurden – gefiltert nach einem bestimmten Mitarbeiter.

Verwenden Sie immer die gleiche Einheit (Stunden oder Tage), wenn Sie Mitarbeiterabwesenheiten registrieren, um eine aussagekräftige Statistik zu erhalten.

## <a name="to-register-employee-absence"></a>So erfassen Sie die Abwesenheit eines Mitarbeiters
Sie können die Mitarbeiterabwesenheiten auf täglicher Basis oder einem anderen Intervall erfassen, das Ihre organisatorischen Anforderungen erfüllt.

1. Wählen Sie in der rechten oberen Ecke das Symbol **Nach Seite oder Bericht suchen** und geben **Abwesenheitsregistrierung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie für Mitarbeiterabwesenheit, die Sie erfassen möchten, eine Zeile aus.
4. Schließen Sie die Seite.

    > [!Tip]
    > Verwenden Sie immer die gleiche Einheit (Stunden oder Tage), wenn Sie Mitarbeiterabwesenheiten registrieren, um aussagekräftige Statistiken zu erhalten.

## <a name="to-view-an-individual-employees-absence"></a>So zeigen Sie die Abwesenheit für einen einzelnen Mitarbeiter an
1. Wählen Sie in der rechten oberen Ecke das Symbol **Nach Seite oder Bericht suchen** und geben **Mitarbeiter** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie den entsprechenden Mitarbeiter aus und wählen Sie dann die Aktion **Abwesenheiten** aus.

    Die Seite **Mitarbeiter Abwesenheiten** wird geöffnet und zeigt alle Abwesenheiten sowie deren Beginn und Ende an.

## <a name="to-view-an-employees-absence-by-categories"></a>So zeigen Sie die Abwesenheit eines Mitarbeiters nach Kategorien an
1. Wählen Sie in der rechten oberen Ecke das Symbol **Nach Seite oder Bericht suchen** und geben **Mitarbeiter** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie den entsprechenden Mitarbeiter aus und wählen Sie dann die Aktion **Abwesenheiten nach Kategorien** aus.
3. Auf der Seite **Mitarbeiter Abw. n. Kategorien** füllen Sie die Filterfelder bedarfsgerecht aus und wählen Sie dann die Aktion **Matrix anzeigen** aus.

    Die Seite **Mitarbeiter Abw. n. Kat. Matr.** wird geöffnet und zeigt alle Abwesenheiten an, aufgeschlüsselt nach Abwesenheitsgründen.

## <a name="to-view-all-employee-absences-by-category"></a>So zeigen Sie alle Mitarbeiterabwesenheiten nach Kategorie an
1. Wählen Sie in der rechten oberen Ecke das Symbol **Nach Seite oder Bericht suchen** und geben **Abwesenheitsregistrierung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie auf der Seite **Abwesenheitsregistrierung** die Aktion **Übersicht nach Kategorien** aus.
3. Legen Sie auf der Seite **Abwesenheit nach Kategorien** einen Filter im Feld **Mitarbeiternr. Filter** fest, um Mitarbeiterabwesenheiten für einzelne Mitarbeiter oder eine definierte Gruppe von Mitarbeitern anzuzeigen.
4. Wählen Sie die Aktion **Matrix anzeigen** aus.

    Die Seite **Abwesenheit nach Kategorien - Matrix** wird geöffnet und zeigt alle Abwesenheiten von Mitarbeitern an, aufgeschlüsselt nach den einzelnen Abwesenheitsursachen.

## <a name="to-view-all-employee-absences-by-period"></a>So zeigen Sie alle Mitarbeiterabwesenheiten nach Perioden an
1. Wählen Sie in der rechten oberen Ecke das Symbol **Nach Seite oder Bericht suchen** und geben **Abwesenheitsregistrierung** ein. Wählen Sie dann den zugehörigen Link aus.
   Wählen Sie auf der Seite **Abwesenheitsregistrierung** die Aktion **Übersicht nach Perioden** aus.
2. Legen Sie auf der Seite **Abwesenheiten nach Perioden** einen Filter im Feld **Abwesenheitsgrundfilter** fest, um die Abwesenheiten von Mitarbeitern nach bestimmten Abwesenheitsursachen anzuzeigen.
3. Wählen Sie die Aktion **Matrix anzeigen** aus.

    Die Seite **Abwesenheiten nach Perioden - Matrix** wird geöffnet und zeigt Abwesenheiten von Mitarbeitern an, aufgeschlüsselt nach Perioden.

## <a name="see-also"></a>Siehe auch
[Personalwesen verwalten](hr-manage-human-resources.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Funktionen, die angezeigt werden ändern](ui-experiences.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]