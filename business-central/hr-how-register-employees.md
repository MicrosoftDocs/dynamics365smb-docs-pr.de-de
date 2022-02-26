---
title: Festlegen von Mitarbeitern und Ändern von Informationen
description: Beschreibt, wie Sie die Human Resources-Funktionalität verwenden, um neue Mitarbeiter zu registrieren oder Mitarbeiterinformationen für bestehende Mitarbeiter zu bearbeiten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personnel, people, employee, staff, HR
ms.search.form: 5200, 5201
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: c3e8215f80d2d035643166832b866c569e1d2d1a
ms.sourcegitcommit: f4b32ba1f926a2a712400c36305616f320757723
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/08/2022
ms.locfileid: "8101107"
---
# <a name="register-employees"></a>Erfassen eines Mitarbeiters
Um die Funktion Human Resources zu nutzen, müssen Sie zunächst jeden Mitarbeiter hinzufügen, indem Sie die Felder auf der Seite **Mitarbeiterkarte** ausfüllen.

## <a name="adding-new-customers"></a>Hinzufügen neuer Kunden
Sie können neue Mitarbeiter manuell hinzufügen, indem Sie die Felder auf der Seite **Mitarbeiterkarte** ausfüllen, oder Sie können Vorlagen verwenden, die vordefinierte Informationen enthalten. Sie können zum Beispiel Vorlagen für verschiedene Arten von Mitarbeiterprofilen erstellen. Die Verwendung von Vorlagen spart Zeit beim Hinzufügen neuer Mitarbeiter und hilft sicherzustellen, dass die Informationen jedes Mal korrekt sind. Wenn Sie Vorlagen für mehr als einen Mitarbeitertyp erstellen, können Sie die Vorlage auswählen, die Sie beim Hinzufügen eines Mitarbeiters verwenden möchten. Wenn Sie nur eine Vorlage erstellen, wird diese für alle neuen Mitarbeiter verwendet. Nachdem Sie eine Vorlage erstellt haben, können Sie die Aktion **Vorlage anwenden** verwenden, um sie auf einen oder mehrere ausgewählte Mitarbeiter anzuwenden. Um eine Vorlage zu erstellen, geben Sie auf der Seite Mitarbeiterkarte die Informationen ein, die Sie wiederverwenden möchten, und speichern sie dann als Vorlage.

> [!TIP]
> Es kann hilfreich sein, die Seite **Mitarbeitervorlage** zu personalisieren, wenn Sie eine Vorlage erstellen. So können Sie beispielsweise ein Feld hinzufügen, das auf der Seite noch nicht angezeigt wird. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Die Mitarbeiterinformationen können jederzeit geändert werden. Wenn Sie die Datensätze Ihrer Mitarbeiter auf dem neuesten Stand halten, können Sie personalbezogene Aufgaben vereinfachen. Wenn sich zum Beispiel die Adresse eines Mitarbeiters ändert, registrieren Sie dies auf der Seite Mitarbeiterkarte.

> [!NOTE]  
> Sie können einem Mitarbeiter seine Ausgaben während Geschäftsaktivitäten erstatten. Dazu müssen Sie die Felder auf dem Inforegister **Zahlungen** auf der Seite **Mitarbeiterkarte** ausfüllen. Weitere Informationen finden Sie unter [Erstatten Sie die Ausgaben der Mitarbeiter zurück](finance-how-record-reimburse-employee-expenses.md).

## <a name="to-set-up-an-employee"></a>Einen Mitarbeiter einrichten:
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Mitarbeiter** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu**.
3. Füllen Sie auf der Seite **Mitarbeiterkarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-insert-a-picture-of-an-employee"></a>Das Bild eines Mitarbeiters einfügen:
Wenn Sie ein Foto eines Mitarbeiters haben, können Sie es auf der Mitarbeiterkarte einfügen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Mitarbeiter** ein, und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte für den betreffenden Mitarbeiter.
3. In der Infobox **Mitarbeiter Bild** wählen die Dropdownschaltfläche, und wählen Sie dann **Importieren**.
4. Auf der Seite **Ein Bild zum Hochladen auswählen** wählen Sie die Schaltfläche **Auswählen** aus.
5. Wählen Sie die Datei aus und wählen Sie dann **Öffnen** aus.

Das Bild wurde jetzt in die Inforbox **Mitarbeiter Bild** importiert.

## <a name="to-register-various-information-about-an-employee"></a>Erfassen von verschiedenen Informationen über einen Mitarbeiter
Auf der Mitarbeiterkarte können Sie Informationen ablegen wie beispielsweise Gewerkschaftsangehörigkeit, Verwandte oder Verträge für den Mitarbeiter. Nachfolgend ist beschrieben, wie eine alternative Adresse eingerichtet wird. Für alle anderen Informationen, die Sie auf einer Mitarbeiterkarte ablegen können, sind die Schritte vergleichbar.

Sie können alternative Adressen verwenden, um die Aufenthaltsorte Ihrer Mitarbeiter nachzuverfolgen. Dies kann z. B. beim Einsatz im Ausland, langen Geschäftsreisen oder Aufenthalten in Sommerwohnsitzen nützlich sein.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Mitarbeiter** ein, und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte für den betreffenden Mitarbeiter.
3. Wählen Sie die **Alternativen-Adressen** Aktion aus.
4. Füllen Sie auf der Seite **Alternative Adressliste** die notwendigen Felder aus.
5. Wiederholen Sie Schritt 4 für jede alternative Adresse.

## <a name="see-also"></a>Siehe auch
[Geschäftsverwandte Ausgaben der Beschäftigten aufzeichnen und zurückzahlen](finance-how-record-reimburse-employee-expenses.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]