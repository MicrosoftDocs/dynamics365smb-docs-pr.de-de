---
title: Antworten auf Anforderungen zu Personendaten
description: "Sie müssen auf Datenenbetreffanforderungen reagieren."
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.date: 03/13/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 89f53f24f74401ce384b54d04fbeb473aedad96d
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---

# <a name="responding-to-requests-about-personal-data"></a>Antworten auf Anforderungen zu Personendaten  
Datenenbetreffe können mehrere Arten von Aktionen für die Personendaten abfragen. Wenn Sie sensible Daten klassifiziert haben und sicher sind, dass sie korrekt sind, kann ein Administrator auf Anforderungen reagieren, indem er den Datenen-Klassifizierungsvorschlag im Rollencenter **Verwalten Sie Benutzer, Benutzergruppen und Berechtigungen** nutzt, wenn Sie den Windows-Client im **IT-Manager** Rollencenter verwenden. Weitere Informationen zum Klassifizieren von Daten und von Abteilungen und Datenenempfindlichkeit, und [Klassifizieren von Daten](/dynamics-nav/classifying-data) Sie sehen. [Abteilungen und Datenen-Empfindlichkeit](admin-classifying-data-sensitivity.md)

Die folgende Tabelle enthält Beispiele über die Anforderungen, auf die Sie reagieren können.

> [!Note]
> Während wir Funktionen für die Antworten auf diese Art von Anfragen bereitstellen und so auf Personendaten zugreifen, ist es Ihre Verantwortung, sicherzustellen, dass persönlich und sensible Daten entsprechend zugeordnet und klassifiziert werden.

|Anforderungsart|Beschreibung und vorgeschlagene Antwort|
|-----|-----|
|Portabilitätsanforderungen|Ein Datenbetreff kann einen Datenenportabilitätsantrag erstellen, d. h. zum Teil, dass Sie die entsprechenden Daten der Personendaten aus Ihrem Systemen exportieren und in einem strukturierten, häufig genutzten Format bereitstellen müssen. Um auf diese Anforderungen zu reagieren, verwenden Sie die Funktion Schutz der Privatsphäre, um personenbezogene Daten in eine Excel-Datei zu exportieren. Mithilfe von Excel können Sie die Personendaten bearbeiten und in einem häufig verwendeten, maschinell lesbaren Format wie .csv oder .xml speichern. Administratoren können Daten mithilfe von Anfangskonfigurationspaketen auch exportieren und dann Stammdatentabellen und die zugehörigen Tabellen, die Personendaten enthalten, konfigurieren. |
|Anforderung für Löschen|Ein Datenenbetreff kann anfordern, dass Sie die Personendaten löschen. Es gibt verschiedene Arten, Personendaten mithilfe der Anpassungsfunktionen zu löschen, aber die Entscheidung und die Implementierung ist Ihre Verantwortung. In einigen Fällen können Sie die Daten direkt bearbeiten, zum Beispiel einen Kontakt löschen und dann die Stapelverarbeitung für stornierte Aktivitäten ausführen, um den Kontakt zu löschen. <br><br> **Hinweis:**, Wenn Sie ein Datum in dem Feld **Löschen des Belegs zulassen vor** der **Debitoren & Verkauf Einr.** oder der **Kreditoren & Einkauf Einr.** angegeben haben, können Sie das Datum ändern, sodass gebuchte Verkaufs- und Einkaufsbelege, die Sie gedruckt haben und für die ein Buchungsdatum für oder vor dem Datum vorliegt, gelöscht werden können.|
|Anforderung für Korrektur|Ein Datenenbetreff kann verlagen, dass Sie die falschen Personendaten löschen. Es gibt mehrere Möglichkeiten dazu: In einigen Fällen können Sie Exporttarife nach Excel exportieren, mehrere Datensätze schnell auf einmal bearbeiten und importieren dann die aktualisierten Daten importieren. Weitere Informationen finden Sie unter [Geschäftsdaten nach Excel exportieren](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data). Sie können auch manuell Eingabefelder, die Personendaten enthalten, wie Bearbeitungsinformationen über einen Debitor auf der Debitorenkarte bearbeiten. Es sind jedoch Änderungssätze wie Allgemein, Debitor und Steuerposten für die Integrität des Unternehmensressourcenplanungssystems wichtig. Wenn Sie Personendaten in den Geschäfttransaktionsdatensätzen speichern, erwägen Sie, die Anpassungsfunktionen zu verwenden, um solche Personendaten zu ändern.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Beschränken der Datumsverarbeitung für Datenen-Betreff
Ein Datenbetreff kann verlangen, dass Sie die vorübergehend keine Personendaten verarbeiten. Um solche Anforderungen zu ehren, können Sie ihren Datensatz  als gesperrt markieren aufgrund des Datenschutzes und die Verarbeitung der Daten stoppen. Wenn ein Datensatz als gesperrt markiert wird, können Sie keine neuen Transaktionen erstellen, die den Datensatz verwenden. Beispielsweise können Sie eine neue Rechnung für keinen Debitor erstellen, wenn entweder der Debitor oder der Verkäufer gesperrt ist. Um einen Datenbetreff als gesperrt zu kennzeichnen, öffnen Sie die Karte für den Datenbetreff, beispielsweise die Debitoren-, Kreditoren- oder Kontaktkarte, und wählen Sie **Datenschutz gesperrt**. Sie müssen u **Mehr anzeigen**, um das Feld anzuzeigen.

## <a name="handling-data-about-minors"></a>Behandlung von Daten Minderjähriger
Wenn das Alter der Kontaktperson tiefer ist als das Alter der Volljährigkeit entsprechend dem Gesetz Ihres Landes, können Sie das mithilfe des Kontrollkästchens **Minderjährig** auf der Karte **Kontakt** aktivieren. Wenn Sie dies tun, wird das Kontrollkästchen **Datenschutz gesperrt** automatisch ausgewählt. Wenn Sie die Zustimmung des Feld von den Eltern oder dem Erziehungsberechtigten der minderjährigen Person erhalten, können Sie das Kontrollkästchen **Elterliche Einwilligung erhalten** aktivieren, um die Blockierung des Kontakts aufzuheben. Auch wenn Sie Personendaten für Minderjährige bearbeiten können, können Sie die Profilerstellungsfunktionalität in Microsoft Dynamics 365 for Sales nicht verwenden.

> [!Note]
> Das Änderungsprotokoll kann Details erfassen, wie wann und durch wen die **Elterliche Einwilligung erhalten** im Kontrollkästchen ausgewählt wurde. Ein Administrator kann dies mithilfe dem Leitfaden **Änderungsprotokoll einrichten** einrichten und kann auch das Kontrollkästchen **Protokoll-Änderung für die elterliche Einwilligung erhalten** auf der Karte **Kontakt** aktivieren. Weitere Informationen finden Sie unter [Änderungen nachverfolgen](/dynamics-nav-app/across-log-changes).  

## <a name="see-also"></a>Siehe auch
[Klassifizieren von Daten](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data)  
[Datensensitivität klassieren](admin-classifying-data-sensitivity.md)  
[Exportieren Ihrer Geschäftsdaten nach Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data)  

