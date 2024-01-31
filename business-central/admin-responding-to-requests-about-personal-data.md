---
title: Umgang mit Anfragen wegen personenbezogener Daten von Benutzenden
description: 'Dieser Artikel erklärt, wie Sie auf Anfragen zu personenbezogenen Daten reagieren können.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 04/25/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Umgang mit Anfragen wegen personenbezogener Daten von Benutzenden

Datensubjekte können mehrere Arten von Aktionen für die Personendaten abfragen. Beispielsweise sie nach einigen Datenschutzgesetzen und -vorschriften das Recht, den Export, das Löschen oder die Änderung Ihrer Personendaten anzufordern. Diese Anträge heißen *Anträge betroffener Personen*. Wenn Sie die Vertraulichkeit Ihrer Daten klassifiziert haben und sicher sind, dass sie korrekt sind, kann ein Administrator mithilfe der Optionen auf der Registerkarte **Datenprivatsphäre** im **IT-Manager** Rollenzentrum antworten. 
<!--
For more information about classifying data and data sensitivity in [!INCLUDE[prod_long](includes/prod_long.md)], go to the following articles:

* [Classifying Data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) 
* [Classifying Data Sensitivity](admin-classifying-data-sensitivity.md)  -->

## Arten von Anträgen

Die folgende Tabelle enthält Beispiele über die Anträge, auf die Administrierende reagieren können.

> [!Note]
> Während wir Funktionen für die Antworten auf diese Art von Anträgen bereitstellen und so auf personenbezogene Daten zugreifen, ist es Ihre Verantwortung, sicherzustellen, dass personenbezogene und sensible Daten entsprechend zugeordnet und klassifiziert werden.

|Anforderungsart|Beschreibung und vorgeschlagene Antwort|
|-----|-----|
|Portabilitätsanforderungen|Eine betroffene Person kann einen Antrag auf Datenübertragbarkeit stellen. Sie müssen die personenbezogenen Daten der betroffenen Person aus Ihren Systemen exportieren und in einem strukturierten, gängigen Format bereitstellen. Um auf diese Anforderungen zu reagieren, verwenden Sie das **Datenschutz-Dienstprogramm**, um personenbezogene Daten in eine Excel-Datei oder eine RapidStart-Konfigurationsdatei zu exportieren. Mithilfe von Excel können Sie die Personendaten bearbeiten und in einem häufig verwendeten, maschinell lesbaren Format wie .csv oder .xml speichern. Für RapidStart-Konfigurationspakete können Sie auch Stammdatentabellen und die zugehörigen Tabellen, die Personendaten enthalten, konfigurieren. <br><br> **Hinweis:** Wenn Sie Daten exportieren möchten, geben Sie eine minimale Vertraulichkeitsstufe an. Das Ergebnis des Exports enthält die minimalen und alle Empfindlichkeitsebenen darüber. Wenn Sie beispielsweise Daten exportieren, die als „Personenbezogen“ klassifiziert sind, enthält der Export auch als „Vertraulich“ eingestufte Daten. <br><br>Wenn Sie Daten exportiert, die mit einem Datensubjekt verknüpft sind, schaut wird das **Datenschutz-Dienstprogramm** nach direkten Verbindungen zwischen dem Datensubjekt und den Daten, die mit dem Datensubjekt verknüpft werden. Indirekte Beziehungen zwischen den Daten, die mit dem Datensubjekt verknüpft werden und andere Daten werden nicht automatisch vom **Datenschutz-Dienstprogramm** exportiert. Beispielsweise hat die Tabelle Kontakt direkte Kontakt-Profil-Antwortdaten und die Tabelle "Kontakt Profilantwort" ist weiter mit den Profil-Fragendaten verknüpft. Wenn Sie auch Profil-Fragen exportieren möchten, müssen Sie diese Tabelle hinzufügen für eine Zeile mit dem gewünschten Filter in Konfigurationspaket, das **Datenschutz-Dienstprogramm** erstellt.|
|Anforderung für Löschen|Ein Datensubjekt kann anfordern, dass Sie die Personendaten löschen. Es gibt verschiedene Arten, Personendaten mithilfe der Anpassungsfunktionen zu löschen, aber die Entscheidung und die Implementierung ist Ihre Verantwortung. In einigen Fällen können Sie Ihre Daten direkt bearbeiten. Löschen Sie zum Beispiel einen Kontakt und führen Sie dann die Stapelverarbeitung für stornierte Aktivitäten aus, um Aktivitäten für den Kontakt zu löschen. <br><br> **Hinweis:** Wenn Sie ein Datum in dem Feld **Löschen des Belegs zulassen vor** der **Debitoren & Verkauf Einr.** oder der **Kreditoren & Einkauf Einr.** angegeben haben, müssen Sie vielleicht das Datum ändern, sodass Sie gebuchte Verkaufs- und Einkaufsbelege, für die ein Buchungsdatum für oder vor dem Datum vorliegt, löschen können.|
|Anforderung für Korrektur|Ein Datensubjekt kann verlagen, dass Sie die falschen Personendaten löschen. Es gibt mehrere Möglichkeiten dazu: In einigen Fällen können Sie Exporttarife nach Excel exportieren, mehrere Datensätze schnell auf einmal bearbeiten und importieren dann die aktualisierten Daten importieren. Weitere Informationen finden Sie unter [Geschäftsdaten nach Excel exportieren](about-export-data.md). Sie können auch manuell Eingabefelder, die Personendaten enthalten, wie Bearbeitungsinformationen über einen Debitor auf der Debitorenkarte bearbeiten. Datensätze wie allgemeine, Debitoren- und Steuerkontoeinträge sind jedoch wichtig. Wenn Sie Personendaten in den Geschäfttransaktionsdatensätzen speichern, erwägen Sie, die Anpassungsfunktionen zu verwenden, um solche Personendaten zu ändern.|

## Die Datenverarbeitung für eine betroffene Person einschränken

Ein Datensubjekt kann verlangen, dass Sie die vorübergehend keine Personendaten verarbeiten. Um solche Anforderungen zu ehren, können Sie ihren Datensatz als gesperrt markieren aufgrund des Datenschutzes und die Verarbeitung der Daten stoppen. Wenn ein Datensatz als gesperrt markiert wird, können Sie keine neuen Transaktionen erstellen, die den Datensatz verwenden. Beispielsweise können Sie eine neue Rechnung für keinen Debitor erstellen, wenn entweder der Debitor oder der Verkäufer gesperrt ist. Um ein Datensubjekt als gesperrt zu kennzeichnen, öffnen Sie die Karte für das Datensubjekt, beispielsweise die Debitoren-, Kreditoren- oder Kontaktkarte, und wählen Sie **Datenschutzsperre**. Sie müssen u **Mehr anzeigen**, um das Feld anzuzeigen.  

## Umgang mit den Anträgen betroffener Personen in einer Testversion

Bestimmte Arten personenbezogener Daten sind Teil eines Microsoft 365 Kontos und nur Administrierende können die Daten exportieren. Das Verfahren zur Verarbeitung von Datensubjektanforderungen ist abhängig vom [!INCLUDE[prod_short](includes/prod_short.md)]-Tenant-Typ.

Wenn Sie für ein Abonnement bezahlt haben [!INCLUDE[prod_short](includes/prod_short.md)], müssen Benutzende den Tenant-Administrierenden Ihrer Organisation kontaktieren, um den Antrag einer betroffenen Person vorzunehmen. Administrierende haben die Verwaltungsrechte und Tools, um Anträge betroffener Personen zu erfüllen.

Wenn Sie sich für [!INCLUDE[prod_short](includes/prod_short.md)] auf der Seite [Testversion](https://trials.dynamics.com/) registriert haben und immer noch die Testversion verwenden, können Benutzende ihre eigenen Daten auf der Seite [Arbeits- und Schuldatenschutz im Azure-Portal](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade) herunterladen und exportieren.

In der Arbeits- und Schuldatenschutzseite können Sie Ihr Konto schließen. Wir empfehlen jedoch, zunächst alle Daten zu exportieren und zu löschen. Wenn Sie Ihr Konto löschen, verlieren Sie den Zugriff auf [!INCLUDE[prod_short](includes/prod_short.md)].

Sie können Personal immer noch sperren aufgrund des Datenschutzes und Transaktionen wie in diesem Artikel erklärt bearbeiten oder löschen.  

## Daten aus Tabellen exportieren, die nicht nach betroffenen Personen klassifiziert sind

Wenn Sie Daten exportieren müssen, die nicht auf eine Weise klassifiziert werden, sodass sie automatisch exportiert werden, wie Daten aus der Tabelle „Profilantworten“, müssen Sie wie folgt vorgehen:

* Überlegen Sie, ob Sie wirklich zusätzliche Daten exportieren müssen, die sich nicht direkt auf den Kontakt beziehen.
* Fügen Sie die Tabelle und die Beziehung manuell zum Rapid-Start-Paket hinzu und exportieren Sie sie direkt aus dem Rapid-Start-Paket. Wir generieren für Sie ein Rapid-Start-Paket, damit Sie es in solchen Situationen optimieren können.

## Umgang mit Daten über Minderjährige

Wenn das Alter der Kontaktperson tiefer ist als das Alter der Volljährigkeit entsprechend dem Gesetz Ihres Landes, können Sie das mithilfe des Kontrollkästchens **Minderjährig** auf der Karte **Kontakt** aktivieren. Wenn Sie dies tun, wird das Kontrollkästchen **Datenschutzsperre** automatisch ausgewählt. Wenn Sie die Zustimmung des Feld von den Eltern oder dem Erziehungsberechtigten der minderjährigen Person erhalten, können Sie das Kontrollkästchen **Zustimmung eines Erziehungsberechtigten erhalten** aktivieren, um die Blockierung des Kontakts aufzuheben. Auch wenn Sie Personendaten für Minderjährige bearbeiten können, können Sie die Profilerstellungsfunktionalität in Dynamics 365 Sales nicht verwenden.

> [!Note]
> Das Änderungsprotokoll kann Details erfassen, wie wann und durch wen die **Zustimmung eines Erziehungsberechtigten erhalten** im Kontrollkästchen ausgewählt wurde. Ein Administrator kann dies mithilfe dem Leitfaden **Änderungsprotokoll einrichten** einrichten und kann auch das Kontrollkästchen **Protokoll-Änderung für Zustimmung eines Erziehungsberechtigten erhalten** auf der Karte **Kontakt** aktivieren. Weitere Informationen finden Sie unter [Änderungen protokollieren](across-log-changes.md).  

### Siehe auch

<!-- [Classifying Data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Classifying Data Sensitivity](admin-classifying-data-sensitivity.md)  -->
[Exportieren Ihrer Geschäftsdaten nach Excel](about-export-data.md)  
[Änderungen protokollieren](across-log-changes.md)  
[Anträge betroffener Personen](/microsoft-365/compliance/gdpr-data-subject-requests)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
