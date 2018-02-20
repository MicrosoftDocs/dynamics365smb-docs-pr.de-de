---
title: "So geht es: Aufträge mit XBRL erstellen | Microsoft Docs"
description: "XBRL (eXtensible Business Reporting Language) ist eine XML-basierte Sprache zum Kennzeichnen von Finanzdaten, dies es Unternehmen ermöglicht, Daten effizient und genau zu verarbeiten und freizugeben."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 659b3bebb20e3deb33e6e392c5318810848285a1
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="create-reports-with-xbrl"></a>Berichte mit XBRL erstellen
XBRL (eXtensible Business Reporting Language) ist eine XML-basierte Sprache zum Kennzeichnen von Finanzdaten, dies es Unternehmen ermöglicht, Daten effizient und genau zu verarbeiten und freizugeben. Die XBRL-Initiative ermöglicht die Erstellung globaler Finanzberichte durch verschiedene ERP-Softwareunternehmen und internationale Buchhaltungsorganisationen. Das Ziel der Initiative ist es, einen Standard für die einheitlichen Berichterstellung der Finanzdaten für Banken, Investoren und Regierungsbehörden bereitzustellen. Solche Geschäftsberichte können Folgendes umfassen:  

 • Finanzauswertungen  
 • Finanzinformationen  
 • Finanzfremde Informationen  
 • Behördliche Erklärungen, beispielsweise jährlich oder quartalsweise abzugebende Finanzauswertungen  

 [!INCLUDE[d365fin](includes/d365fin_md.md)]  Microsoft Dynamics NAV ermöglicht Unternehmen die Implementierung von Daten in XBRL. Die Unternehmen profitieren dadurch von der Flexibilität und Automatisierung, die Ihnen XBRL beim Sammeln und gemeinsamen Nutzen von Daten bietet.  

## <a name="extensible-business-reporting-language"></a>eXtensible Business Reporting Language
XBRL (e **X**tensible **B**usiness **R**eporting **L**anguage) ist eine XML-basierte Sprache für das Finanzberichtswesen. XBRL (eXtensible Business Reporting Language) ist eine XML-basierte Sprache für Finanzberichtswesen. XBRL ist ein Standard für alle Nutzer der Supply-Chain zur einheitlichen Finanzberichterstattung. Dazu können private Unternehmen, das Buchhaltungswesen, Verwaltungen, Analysten, Investmentfirmen, Kapitalmärkte und Kreditgeber als auch Dritte in Schlüsselpositionen wie Softwareentwickler und Datenverwalter gehören.  

Taxonomien sind unter www.xbrl.org erhältlich. Auf der XBRL-Website können Sie Taxonomien herunterladen oder weitere Informationen erhalten.  

Jemand, der Informationen über Ihre finanzielle Situation haben möchte, stellt Ihnen eine Taxonomie zur Verfügung (ein XML-Dokument), die ein oder mehrere Schema/ta enthält, in denen ein oder mehrere Zeilen ausgefüllt werden können. Die Zeilen entsprechen den individuellen Finanzfakten, die vom Sender verlangt werden. Sie importieren diese Taxonomie in Ihre Anwendung und füllen dann das/die Schema/ta aus, indem Sie eingeben, welche/s Konto/Konten der jeweiligen Zeile entspricht, welcher Zeitrahmen benutzt wird, z. B. Bewegung oder Saldo bis Datum. In einigen Fällen können Sie ersatzweise eine Konstante eingeben wie z. B. die Mitarbeiteranzahl. Nun können Sie das Instance Document (ein XML-Dokument) an denjenigen schicken, der die Informationen angefordert hat. Der Gedanke dahinter ist, dass sich dieser Vorgang mehrmals wiederholen kann, so dass Sie, trotz eventueller Änderungen an der Taxonomie, nur neue Instance Documents für andere Zeiträume exportieren müssen.  

## <a name="xbrl-is-comprised-of-the-following-components"></a>XBRL besteht aus den folgenden Komponenten  
Die XBRL **Spezifikation** erklärt, was XBRL ist, wie XBRL Instance Documents und XBRL-Taxonomien erstellt werden. Die XBRL-Spezifikation erklärt XBRL mit technischen Ausdrücken und ist für Techniker gedacht.  

Die XBRL **Schemata** sind die niederen Kernelemente von XBRL. Das Schema ist die physikalische XSD-Datei, die wiedergibt, wie Instance Documents und Taxonomien erstellt werden.  

Bei den XBRL- **Linkbases** handelt es sich um physische XML-Dateien, die Informationen über die Elemente enthalten, die im XBRL-Schema definiert sind, wie z. B. Labels in einer oder mehreren Sprachen, wie Elemente summiert werden etc.  

Eine XBRL- **Taxonomie** ist ein "Vokabular" oder ein "Wörterbuch", das von einer Gruppe in Einklang mit den XBRL-Spezifikationen erstellt wurde, um Geschäftsinformationen auszutauschen.  

Ein XBRL **Instance Document** ist ein Geschäftsbericht, wie ein Finanzbericht, für die XBRL-Spezifikation. Die Bedeutung der Werte in dem Dokument werden durch die Taxonomie erklärt. Ein Instance Document ist so gut wie nutzlos, wenn Sie nicht wissen, für welche Taxonomie es erstellt wurde.  

## <a name="layered-taxonomies"></a>Geschichtete Taxonomien  
Eine Taxonomie kann aus einer Grundtaxonomie, z .B. US-GAAP oder IAS, und einer oder mehreren Erweiterungen bestehen. Aus diesem Grund bezieht sich eine Taxonomie auf mehrere Schemata (oder ein einzelnes), die alle separate Taxonomien sind. Wenn die zusätzlichen Taxonomien in die Datenbank geladen werden, werden die neuen Elemente einfach an die bestehenden Elemente angehängt.  

## <a name="linkbases"></a>Linkbases  
 In XBRL Spez. 2 wird die Taxonomie in verschiedenen XML-Dateien beschrieben. Die erste XML-Datei ist die Taxonomieschemadatei selbst (.xsd-Datei), die lediglich eine ungeordnete Liste von Elementen oder Informationen für den Bericht enthält. Zusätzlich sind normalerweise einige Linkbasedateien (.xml) damit verknüpft. Die Linkbasedateien enthalten Daten, die die einfache Taxonomie (.xsd-Datei) vervollständigen. Es gibt sechs Arten von Linkbase-Dateien, von denen vier für XBRL Produktnamen von Bedeutung sind. Und zwar:  

-   Beschriftungslinkbase: Diese Linkbase enthält Beschriftungen oder Namen für die Elemente. Die Datei enthält möglicherweise Beschriftungen in verschiedenen Sprachen, die mit einer XML-Eigenschaft namens "lang" identifiziert werden. Die XML-Sprachen-ID enthalten normalerweise eine zweibuchstabige Abkürzung, und obwohl es einfach sein sollte, zu beurteilen, was die Abkürzung bedeutet, gibt es keine Verbindung zum Windows-Sprachcode oder zu den Sprachcodes, die in den Demodaten definiert werden. Wenn der Benutzer daher die Sprachen nach einer bestimmten Taxonomie durchsucht, sieht er alle Beschriftungen für das erste Element in der Taxonomie, was bedeutet, dass er ein Beispiel jeder Sprache anzeigen kann. Eine Taxonomie kann mehrere Beschriftungslinkbases haben, die damit verknüpft werden, solange diese Linkbases unterschiedliche Sprachen enthalten.  

-   Darstellungslinkbase: Diese Linkbase enthält Informationen zur Elementstruktur, genauer gesagt, Informationen darüber, wie der Ersteller der Taxonomie möchte, dass die Anwendung dem Anwender die Taxonomie darstellen soll. Die Linkbase enthält eine Reihe von Verknüpfungen, die jeweils zwei Elemente als über- und untergeordnet verknüpfen. Bei der Anwendung dieser Verknüpfungen können die Elemente hierarchisch dargestellt werden. Beachten Sie, dass die Darstellungslinkbase nur das behandelt: Die Darstellung der Elemente für den Anwender.  

-   Berechnungslinkbase: Diese Linkbase enthält Informationen darüber, welche Elemente übernommen werden. Die Struktur ähnelt der der Darstellungslinkbase, mit der Ausnahme, dass jeder Link oder "Bogen" über eine "Weight"(Gewicht)-Eigenschaft verfügt. Das Gewicht kann entweder 1 oder -1 betragen und damit anzeigen, ob das Element zu seinem übergeordneten Element addiert oder von ihm subtrahiert werden soll. Beachten Sie, dass die Roll-ups für die visuelle Darstellung nicht notwendig sind.  

-   Referenzlinkbase: Bei dieser Linkbase handelt es sich um eine XML-Datei, die zusätzliche Informationen über die Daten enthält, die vom Anwender der Taxonomie benötigt werden.

## <a name="to-set-up-xbrl-lines"></a>XBRL-Zeilen einrichten:  
Nach dem Importieren oder der Aktualisierung der Taxonomie müssen die Zeilen der Schemata mit allen nötigen Informationen gefüllt werden. Diese Informationen beinhalten die Unternehmensdaten, die Finanzinformationen, Bemerkungen zu den Finanzinformationen, zusätzliche Schemata und andere Informationen, die zum Erfüllen der bestimmten Anforderungen des Finanzberichtes notwendig sind.  

Sie richten die XBRL-Zeilen ein, indem Sie die Daten in der Taxonomie Ihren Daten in der Finanzbuchhaltung zuordnen.  

1.  Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seiten- oder Berichtsymbol suchen") und geben **XBRL-Taxonomien** ein und wählen dann den zugehörigen Link aus.  
2.  Im Fenster **XBRL-Taxonomies** wählen Sie eine Taxonomie in der Liste aus.  
3.  Wählen Sie die Aktion **Zeilen** aus.  
4.  Wählen Sie eine Zeile und füllen Sie die Felder aus.   
5.  Durch Klicken auf die Aktion **Information** können Sie die Detailinformationen lesen.  
6.  Um die Sachkonten aus dem Kontenplan den XBRL-Zeilen zuzuordnen, klicken Sie auf **Verknüpfte Finanzbuchhaltungszeile**.  
7.  Um dem Finanzbericht eine Notiz hinzuzufügen, wählen Sie die **Notizen** Aktion.  

> [!NOTE]  
>  Sie können nur Daten exportieren, die der Herkunftsart entsprechen, die Sie in dem Feld **Herkunftsart** ausgewählt haben, einschließlich Beschreibung und Notizen.  

> [!NOTE]  
>  Unwichtige Zeilen können als **NICHT ANWENDBAR** gekennzeichnet werden und werden dann nicht exportiert.

 ## <a name="to-import-an-xbrl-taxonomy"></a>Importieren von XBRL-Taxonomien  
Der erste Schritt, um mit der XBRL-Funktionalität arbeiten zu können, ist, die Taxonomie in Ihre Datenbank zu importieren. Eine Taxonomie besteht aus einem oder mehreren Schema/ta und einigen Linkbases. Wenn Sie den Import des/der Schemas/Schemata und Linkbases durchgeführt haben und die Linkbases dem Schema zugewiesen haben, können Sie die Zeilen einrichten und die Sachkonten des Kontenplans den entsprechenden Taxonomiezeilen zuordnen.  

1.  Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seiten- oder Berichtsymbol suchen") und geben **XBRL-Taxonomien** ein und wählen dann den zugehörigen Link aus.  
2.  Erstellen Sie im Fenster **XBRL Taxonomie** eine neue Zeile, und geben Sie Name und Beschreibung der Taxonomie ein.  
3.  Klicken Sie auf **Schemas** und fügen Sie die Beschreibung für das Schema ein.  
4.  Um das Schema zu importieren, wählen Sie im Fenster **XBRL-Schemata** auf der Registerkarte **Importieren** und wählen Sie dann einen Ordner und eine XSD-Datei aus. Wählen Sie die Schaltfläche **Öffnen** aus.  
5.  Um die Linkbase zu importieren, wählen Sie im Fenster **XBRL-Schemata** auf der Registerkarte **Importieren** und wählen Sie dann einen Ordner und eine XML-Datei aus. Wählen Sie die Schaltfläche **Öffnen** aus.  
6.  Jetzt können Sie die Linkbase auf das Schema anwenden. Wiederholen Sie den Vorgang, bis Sie alle Linkbases importiert haben.  
7. Wählen Sie die **Auf Taxonomie anwenden** Aktion aus, um die Linkbase auf das Schema anzuwenden.  

> [!IMPORTANT]  
>  Anstatt die Linkbases einzeln nach dem Import anzuwenden, können Sie warten, bis Sie alle Linkbases importiert haben, und sie dann alle gleichzeitig anwenden. Dazu wählen Sie die Schaltfläche **NEIN**, wenn sie aufgefordert werden, die neu importierte Linkbase auf das Schema anzuwenden. Wählen Sie dann die Zeilen mit den Linkbases aus, die Sie anwenden möchten.  

## <a name="to-update-an-xbrl-taxonomy"></a>Um eine XBRL-Taxonomie zu aktualisieren  
Wenn sich eine Taxonomie ändert, müssen Sie die aktuelle Taxonomie dementsprechend ändern. Der Grund für die Aktualisierung kann ein verändertes Schema, eine veränderte Linkbase oder eine neue Linkbase sein. Nach Aktualisierung der Taxonomie müssen Sie nur die Zeilen an die geänderten oder neuen Zeilen anpassen.  

1.  Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seiten- oder Berichtsymbol suchen") und geben **XBRL-Taxonomien** ein und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie im Fenster **XBRL-Taxonomien** die Aktion **Schemas** aus.  
3.  Wählen Sie zum Aktualisieren des Schemas das zu aktualisierende Schema aus, und klicken Sie auf **Importieren**.  
4.  Um eine neue Linkbase zu aktualisieren oder hinzuzufügen, wählen Sie **Linkbases** aus.  
5.  Wählen Sie die gewünschte Linkbase aus oder drücken Sie STRG+N, um eine neue Zeile zu erhalten, wählen Sie die Art der Linkbase aus, und fügen Sie dann eine Beschreibung ein.  
6.  Um die Linkbase zu importieren, wählen Sie die **Importieren** Aktion aus.  
7.  Wählen Sie die Schaltfläche **Ja** aus, um die Linkbase auf das Schema anzuwenden.  

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)    
[Business Intelligence](bi.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

