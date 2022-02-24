---
title: Datensensitivität klassieren
description: Sie müssen festlegen, welche Art von Daten Sie über Mitarbeiter speichern, sodass Sie sich auf Datensubjektanforderungen reagieren können.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 04/01/2020
ms.openlocfilehash: e1b199c16bb39feb4ecbef9b36ccd49a5c32e3c8
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187412"
---
# <a name="classifying-data-sensitivity"></a>Datensensitivität klassieren
Um die Felder zu klassifizieren, die vertrauliche oder Personendaten enthalten, kann ein Microsoft Partner die Eigenschaft ```DataClassification``` auf Felder setzen. Dazu müssen Zugriff auf die Datenbanktabellen haben, entweder über die Entwicklungsumgebung oder indem ein Windows PowerShell-Skript ausgeführt wird. Weitere Informationen finden Sie unter [Daten klassieren](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data).  

Als Debitor können Sie eine zweite Ebene der Klassierung hinzufügen, indem Sie die Empfindlichkeitsebenen für die Daten festlegen, die Sie in den Feldern Standard und Benutzerdefiniert speichern. Datenempfindlichkeit klassifizieren hilft sicherzustellen, dass Sie wissen, wo Sie Personendaten im System erfasst haben und macht es einfacher, auf Anforderungen von Datensubjekten zu reagieren. Wenn ein Kontakt oder Debitor Sie auffordert, die Personendaten zu exportieren. Weitere Informationen finden Sie unter [Antworten auf Anforderungen zu Personendaten](admin-responding-to-requests-about-personal-data.md).

> [!Important]
> Microsoft stellt dies Klassifizierungsfunktion als Mehrwert für Sie bereit. Es ist Ihre Aufgabe, die Daten entsprechend einzuteilen und sämtliche Gesetze und Bestimmungen, die gelten, einzuhalten. Microsoft lehnt jede Verwantwortung hinsichtlich Ansprüchen ab, die im Zusammenhang mit Ihrer Klassifikation von Daten stehen.  

Die folgende Tabelle beschreibt Datenempfindlichkeitsebenen, die Sie zuweisen können.

|Datensensitivität|Description|
|----|----|
|Sensitiv | Informationen über die rassistische oder ethnische Herkunft, politische Meinungen, religiöser Glauben, Mitglied bei Gewerkschaften, psychische oder mentale Gesundheit, Sexualität oder Details über Straftaten. |
|Persönlich | Informationen, die verwendet werden können, um ein Datensubjekt, entweder direkt oder in Kombinationen mit anderen Daten zu identifizieren.|
|Vertraulich | Kommerzielle Daten, die Sie für Buchhaltungs- oder andere Geschäftszwecke nutzen und nicht mit anderen Einheiten teilen möchten. Beispielsweise können dies Verkaufsposten sein.|
|Normal | Allgemeine Daten, die keine andere Klassifizierung haben.|

## <a name="how-do-i-classify-my-data"></a>Wie klassiere ich meine Daten?
Das Klassifizieren der Empfindlichkeit vieler Feler kann lange dauern. Um den Vorgang zu beschleunigen, stellen wir Werkzeuge bereit, die Sie verwenden können, um die sensiblen Felder aufeinmal zu klassieren. Sie können danach bestimmte Felder noch weiter abstimmen. bestimmte Felder. Sie können Werkzeuge im Feld Daten-Klassifizierungsvorschlag suchen, die für die Verwaltung von Benutzern, Benutzergruppen und Rollencenter-Berechtigungen verfügbar sind. Zur Ausführung dieser Aktivität benötigen Sie Administratorrechte oder müssen das Arbeitsblatt nutzen.

> [!Important]
> Wenn Sie den Daten-Klassifizierungsvorschlag zum ersten Mal öffnen, wird er leer sein. Sie müssen das Daten-Klassifizierungshandbuch ausführen, um die Liste der Felder zu generieren. Um den Leitfaden zu starten, wählen Sie die Aktion **Datenklassifizierungen einrichten**.

Beispielsweise können Sie mit dem Arbeitsblatt Datenklassifizierung folgendes tun:  

* Verwenden Sie das Daten-Klassifizierungshandbuch, um die Felder in eine Excel-Arbeitsmappe zu exportieren, wo Sie sie auf einmal klassifizieren können. Für die Nutzung des Excel-Arbeitsblattes ist es besonders nützlich, wenn Sie mit einem Microsoft Partner zusammenarbeiten. Nachdem Sie das Arbeitsblatt aktualisiert haben, können Sie den Leitfaden verwenden, um die Klassifizierungen zu importieren und zu übernehmen. Sie können den Leitfaden auch verwenden, um Felder manuell zu klassifizieren.  
* Wählen Sie ein Feld und filtern Sie die Liste, um ähnliche Felder zu finden, die wahrscheinlich zusammen gehören.  
* Untersuchen Sie ein Feld, indem Sie seinen Inhalt anzeigen.  

> [!Tip]
> Wir haben Beispielempfindlichkeitsklassifizierungen für die Tabellen und Felder im Cronus-Demomandanten definiert. Sie können diese Klassifizierungen als Inspiration verwenden, wenn Sie Ihre eigenen Tabellen und Felder klassifizieren.

## <a name="see-also"></a>Siehe auch

[Klassifizieren von Daten](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data)  
