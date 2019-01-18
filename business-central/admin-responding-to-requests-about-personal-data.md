---
title: Antworten auf Anforderungen zu Personendaten
description: "Sie müssen auf Datenenbetreffanforderungen reagieren."
author: bholtorf
ms.service: dynamics365-business-central
ms.author: bholtorf
ms.custom: na
ms.date: 11/06/2018
ms.reviewer: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 313ebe68ae1963e22bc17d53a7c41ae8f090de60
ms.contentlocale: de-de
ms.lasthandoff: 11/22/2018

---

# <a name="responding-to-requests-about-personal-data"></a>Antworten auf Anforderungen zu Personendaten  
Datenenbetreffe können mehrere Arten von Aktionen für die Personendaten abfragen. Beispielsweise unter dem Gesetz zum Schutz der allgemeinen Daten (DSGVO), haben EU-Bewohner das Recht, Export, das Löschen oder die Änderung Ihrer Personendaten anzufordern. Dieses wird *Datenen-Betreff-Anforderung* genannt. Wenn Sie sensible Daten klassifiziert haben und sicher sind, dass sie korrekt sind, kann ein Administrator auf Anforderungen reagieren, indem er den **Daten-Klassifizierungsvorschlag** im Rollencenter **Verwalten Sie Benutzer, Benutzergruppen und Berechtigungen** nutzt, wenn Sie den Windows-Client im **IT-Manager Rollencenter** verwenden. Weitere Informationen zum Klassifizieren vol sensiblen Daten in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] und [Klassifizieren von Daten](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) und [Klassieren von Datensensibilität](admin-classifying-data-sensitivity.md).  

## <a name="types-of-requests"></a>Arten von Anforderungen

Die folgende Tabelle enthält Beispiele über die Anforderungen, auf die Sie reagieren können.

> [!Note]
> Während wir Funktionen für die Antworten auf diese Art von Anfragen bereitstellen und so auf Personendaten zugreifen, ist es Ihre Verantwortung, sicherzustellen, dass persönlich und sensible Daten entsprechend zugeordnet und klassifiziert werden.

|Anforderungsart|Beschreibung und vorgeschlagene Antwort|
|-----|-----|
|Portabilitätsanforderungen|Ein Datenbetreff kann einen Datenenportabilitätsantrag erstellen, d. h. zum Teil, dass Sie die entsprechenden Daten der Personendaten aus Ihrem Systemen exportieren und in einem strukturierten, häufig genutzten Format bereitstellen müssen. Um auf diese Anforderungen zu reagieren, verwenden Sie die Funktion **Schutz der Privatsphäre**, um personenbezogene Daten in eine Excel-Datei oder eine RapidStart-Konfigurationsdatei zu exportieren. Mithilfe von Excel können Sie die Personendaten bearbeiten und in einem häufig verwendeten, maschinell lesbaren Format wie .csv oder .xml speichern. Für RapidStart Konfigurationspakete können Sie auch Stammdatentabellen und die zugehörigen Tabellen, die Personendaten enthalten, konfigurieren. <br><br> **Hinweis:**, Wenn Sie Daten exportieren möchten, geben Sie eine Mahnstufe der minimalen Empfindlichkeit an. Das Ergebnis des Exports enthält die minimalen und alle Empfindlichkeitsebenen darüber. Wenn Sie beispielsweise wählen, Daten zu exportieren, die als Persönlich klassifiziert sind, enthält der Export auch Daten, die als "Vertraulich" bezeichnet sind. <br><br>Wenn Sie Daten exportiert, die  mit einem Datenbetreff verknüpft sind, schaut  wird das **Datenschutz-Dienstprogramm** nach direkten Verbindungen zwischen dem Datenbetreff und den Daten, die mit dem Datenbetreff verknüpft werden. Indirekte Beziehungen zwischen den Daten, die mit dem Datenenbetreff verknüpft werden und andere Daten werden nicht automatisch vom **Datenschutz-Dienstprogramm** exportiert. Beispielsweise hat die Tabelle Kontakt direkte Kontakt-Profil-Antwortdaten und die Tabelle "Kontakt Profilantwort" ist weiter mit den Profil-Fragendaten verknüpft. Wenn Sie auch Profil-Fragen exportieren möchten, müssen Sie diese Tabelle hinzufügen für eine Zeile mit dem gewünschten Filter in Konfigurationspaket, das **Daten-Hilfsprogramme** erstellt.|
|Anforderung für Löschen|Ein Datenenbetreff kann anfordern, dass Sie die Personendaten löschen. Es gibt verschiedene Arten, Personendaten mithilfe der Anpassungsfunktionen zu löschen, aber die Entscheidung und die Implementierung ist Ihre Verantwortung. In einigen Fällen können Sie die Daten direkt bearbeiten, zum Beispiel einen Kontakt löschen und dann die Stapelverarbeitung für stornierte Aktivitäten ausführen, um den Kontakt zu löschen. <br><br> **Hinweis:**, Wenn Sie ein Datum in dem Feld **Löschen des Belegs zulassen vor** der **Debitoren & Verkauf Einr.** oder der **Kreditoren & Einkauf Einr.** angegeben haben, können Sie das Datum ändern, sodass gebuchte Verkaufs- und Einkaufsbelege, die Sie gedruckt haben und für die ein Buchungsdatum für oder vor dem Datum vorliegt, gelöscht werden können.|
|Anforderung für Korrektur|Ein Datenenbetreff kann verlagen, dass Sie die falschen Personendaten löschen. Es gibt mehrere Möglichkeiten dazu: In einigen Fällen können Sie Exporttarife nach Excel exportieren, mehrere Datensätze schnell auf einmal bearbeiten und importieren dann die aktualisierten Daten importieren. Weitere Informationen finden Sie unter [Geschäftsdaten nach Excel exportieren](about-export-data.md). Sie können auch manuell Eingabefelder, die Personendaten enthalten, wie Bearbeitungsinformationen über einen Debitor auf der Debitorenkarte bearbeiten. Es sind jedoch Änderungssätze wie Allgemein, Debitor und Steuerposten für die Integrität des Unternehmensressourcenplanungssystems wichtig. Wenn Sie Personendaten in den Geschäfttransaktionsdatensätzen speichern, erwägen Sie, die Anpassungsfunktionen zu verwenden, um solche Personendaten zu ändern.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Beschränken der Datumsverarbeitung für Datenen-Betreff
Ein Datenbetreff kann verlangen, dass Sie die vorübergehend keine Personendaten verarbeiten. Um solche Anforderungen zu ehren, können Sie ihren Datensatz  als gesperrt markieren aufgrund des Datenschutzes und die Verarbeitung der Daten stoppen. Wenn ein Datensatz als gesperrt markiert wird, können Sie keine neuen Transaktionen erstellen, die den Datensatz verwenden. Beispielsweise können Sie eine neue Rechnung für keinen Debitor erstellen, wenn entweder der Debitor oder der Verkäufer gesperrt ist. Um einen Datenbetreff als gesperrt zu kennzeichnen, öffnen Sie die Karte für den Datenbetreff, beispielsweise die Debitoren-, Kreditoren- oder Kontaktkarte, und wählen Sie **Datenschutz gesperrt**. Sie müssen u **Mehr anzeigen**, um das Feld anzuzeigen.  

## <a name="handling-data-subject-requests-while-in-trial"></a>Behandlung von Daten-Betreff-Anforderungen in der Testphase
Bestimmte Arten von Personendaten ist Teil des Office 365 Kontos und erfordert Verwaltungszugriff auf Exportieren, wenn Sie eine Datenenbetreffanforderung von einem Anwender für diese Art von Personendaten unter der Schutz-Regelung (DSGVO) Daten erhalten. Das Verfahren zur Verarbeitung von Datenenbetreffanforderungen ist abhängig von der Art des Tenants [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Wenn Sie für ein Abonnement bezahlt haben [!INCLUDE[d365fin](includes/d365fin_md.md)], müssen Sie den Tenant Administrator Ihrer Organisation kontaktieren, um eine Datenenbetreffantrag vorzunehmen. Der Administrator hat die Verwaltungsrechte und Werkzeuge bei Bedarf zu erfüllen.  

Wenn Sie bei [!INCLUDE[d365fin](includes/d365fin_md.md)] angemeldet sind für [Test](https://trials.dynamics.com/) und Sie diese Testumgebung für ein Abonnement bei Ihrer Organisation verlassen haben, können Sie Ihre eigene Datenbetreffanforderung auf der [Datenschutzseite im Azure-Portal](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade)erfüllen. Hier können Sie Ihre Personendaten exportieren und herunterladen.

In der Arbeits- und Schuldatenschutzseite können Sie Ihr Konto schließen. Es empfiehlt sich, dass Sie sicherstellen, dass Sie zuerste alle Daten exportiert und gelöscht haben, wenn Sie Ihr Konto löschen und bedeutet, dass Sie auf [!INCLUDE[d365fin](includes/d365fin_md.md)] zugreifen.  

Sie können Personal immer noch sperren aufgrund des Datenschutzes und Transaktionen wie in diesem Artikel erklärt bearbeiten oder löschen.  

## <a name="exporting-data-from-tables-not-classified-by-data-subject"></a>Daten aus Tabellen exportieren, die nicht nach Datenensubjekten klassifiziert sind
Wenn Sie eine Situation haben, in der Sie Daten exportieren müssen, die nicht auf eine Weise klassifiziert werden, so dass sie automatisch exportiert werden, wie Daten aus den Profil-Antworten Tabelle, müssen Sie wie folgt vorgehen: 
-   Berücksichtigen Sie, dass wenn Sie tatsächlich diese ergänzenden Daten exportieren möchten oder müssen, die nicht mit dem Kontakt verknüpft ist, setzt dies voraus, dass er kein direktes Verhältnis dazu hat. 
-   Fügen Sie diese Tabelle und Verbindung manuell mit dem Rapid Start Paket hinzu und exportieren Sie es direkt aus dem Rapid Start Paket - daher erstellen wir ein Anfangspaket einfach für Sie, so dass Sie dieses in Situationen wie dieser ändern können.

## <a name="handling-data-about-minors"></a>Behandlung von Daten Minderjähriger
Wenn das Alter der Kontaktperson tiefer ist als das Alter der Volljährigkeit entsprechend dem Gesetz Ihres Landes, können Sie das mithilfe des Kontrollkästchens **Minderjährig** auf der Karte **Kontakt** aktivieren. Wenn Sie dies tun, wird das Kontrollkästchen **Datenschutz gesperrt** automatisch ausgewählt. Wenn Sie die Zustimmung des Feld von den Eltern oder dem Erziehungsberechtigten der minderjährigen Person erhalten, können Sie das Kontrollkästchen **Elterliche Einwilligung erhalten** aktivieren, um die Blockierung des Kontakts aufzuheben. Auch wenn Sie Personendaten für Minderjährige bearbeiten können, können Sie die Profilerstellungsfunktionalität in Microsoft Dynamics 365 for Sales nicht verwenden.

> [!Note]
> Das Änderungsprotokoll kann Details erfassen, wie wann und durch wen die **Elterliche Einwilligung erhalten** im Kontrollkästchen ausgewählt wurde. Ein Administrator kann dies mithilfe dem Leitfaden **Änderungsprotokoll einrichten** einrichten und kann auch das Kontrollkästchen **Protokoll-Änderung für die elterliche Einwilligung erhalten** auf der Karte **Kontakt** aktivieren. Weitere Informationen finden Sie unter [Änderungen nachverfolgen](across-log-changes.md).  

## <a name="see-also"></a>Siehe auch
[Klassifizieren von Daten](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Datensensitivität klassieren](admin-classifying-data-sensitivity.md)  
[Exportieren Ihrer Geschäftsdaten nach Excel](about-export-data.md)  
[Änderungen protokollieren](across-log-changes.md)  
[Datenen-Betreff-Anfragen um das DSGVO](/microsoft-365/compliance/gdpr-data-subject-requests)  

