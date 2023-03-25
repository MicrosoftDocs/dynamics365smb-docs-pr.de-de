---
title: So erstellen Sie Berichte mit XBRL
description: 'XBRL ist eine XML-basierte Sprache zur Kennzeichnung von Finanzdaten, die es Unternehmen ermöglicht, ihre Daten effizient und genau zu verarbeiten und weiterzugeben.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/14/2022
ms.author: edupont
---
# Berichte mit XBRL erstellen

> [!NOTE]
> Wir sind dabei, die Funktionen für XBRL-Berichte aus [!INCLUDE[prod_short](includes/prod_short.md)] zu entfernen. Erfahren Sie mehr unter [Änderungen in 2022 Veröffentlichungswelle 1](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1).

XBRL (e**X**tensible **B**business **R**eporting **L**anguage) ist eine auf der eXtensible Markup Language (XML) basierende Sprache zur Kennzeichnung von Finanzdaten, die es Unternehmen ermöglicht, ihre Daten effizient und genau zu verarbeiten und auszutauschen. Die XBRL-Initiative ermöglicht die globale Finanzberichterstattung zahlreicher Firmen für Enterprise Resource Planning (ERP)-Software und internationaler Buchhaltungsorganisationen. Ziel der Initiative ist es, einen Standard für die einheitliche Meldung von Finanzinformationen für Banken, Investoren und Regierungsbehörden zu schaffen. Solche Geschäftsberichte können Folgendes umfassen:  

* Finanzberichte  
* Finanzielle Informationen  
* Nicht-finanzielle Informationen  
* Regulatorische Einreichungen, wie z.B. Jahres- und Quartalsabschlüsse  

> [!NOTE]
> Sie können Hauptbuch-bezogene Schemata importieren und XBRL-Instanzdokumente erstellen, indem Sie die Daten des Hauptbuchs (Sachkonto) aus dem Kontenplan Elementen in Taxonomien zuordnen, die für Finanzberichte, wie Bilanzen, Gewinn- und Verlustrechnungen usw., entwickelt wurden.
>
> Die XBRL-Funktionalitäten in Business Central unterstützen Taxonomien für die Spezifikation 2.1. Die Taxonomien können jedoch nicht unterstützte Elemente wie Formel-Linkbases oder iXBRL (Inline XBRL) enthalten oder andere strukturelle Unterschiede aufweisen. Wir empfehlen Ihnen, die XBRL-Funktionalitäten zu validieren, bevor Sie sie für die Berichterstattung verwenden.
>
> Für die vollständige Unterstützung von Taxonomien sind möglicherweise XBRL-Tagging und -Tools von Dritten erforderlich. Die Organisation XBRL International verfügt über eine Liste von Tools und Dienstleistungen. Je nach den XBRL-Berichtsanforderungen für eine bestimmte Taxonomie sollten Sie diese Ressourcen prüfen. Erfahren Sie mehr unter [Einstieg für Unternehmen](https://go.microsoft.com/fwlink/?linkid=2153466) und [Tools und Dienstleistungen](https://go.microsoft.com/fwlink/?linkid=2153356).

## eXtensible Geschäfts-Berichterstellungs-Sprache

Die XBRL-Taxonomien werden von www.xbrl.org gepflegt. Auf der XBRL-Website können Sie die Taxonomien herunterladen und ausführlichere Informationen lesen.  

Nehmen wir an, jemand möchte Finanzinformationen von Ihnen. Man stellt Ihnen eine Taxonomie (ein XML-Dokument) zur Verfügung, die ein oder mehrere Schemata enthält, die jeweils eine oder mehrere Zeilen zum Ausfüllen haben. Die Zeilen entsprechen den einzelnen Finanzdaten, die der Absender benötigt. Sie importieren diese Taxonomie und füllen dann das/die Schema(s) aus, indem Sie das/die Konto/Konten eingeben, das/die jeder Zeile entspricht/entsprechen und welche Berechnung gewünscht ist, z.B. Nettoveränderung oder Saldo zum Datum. In manchen Fällen können Sie stattdessen auch eine Konstante eingeben, z.B. die Anzahl der Mitarbeiter. Nun können Sie das Instance Document (ein XML-Dokument) an denjenigen schicken, der die Information angefordert hat. Der Gedanke dahinter ist, dass sich dieser Vorgang mehrmals wiederholen kann, so dass Sie, trotz eventueller Änderungen an der Taxonomie, nur neue Instance Documents für andere Zeiträume exportieren müssen.

## XBRL umfasst die folgenden Komponenten

Die XBRL **Spezifikation** erklärt, was XBRL ist und wie man XBRL-Instanzdokumente und Taxonomien erstellt. Die XBRL-Spezifikation erklärt XBRL in technischen Begriffen und ist für eine technische Zielgruppe bestimmt.  

Die XBRL **Schemata** sind die niederen Kernelemente von XBRL. Das Schema ist die physische XSD-Datei (auch XML-Schemadefinition genannt), die ausdrückt, wie XBRL-Instanzdokumente und -Taxonomien zu erstellen sind.

Die XBRL **Linkbases** sind die physischen XML-Dateien, die Informationen über die im XBRL-Schema definierten Elemente enthalten, wie z.B. Labels in einer oder mehreren Sprachen, wie sie sich zueinander verhalten, wie man Elemente zusammenfasst und so weiter.  

Eine XBRL **Taxonomie** ist ein „Vokabular“ oder „Wörterbuch“, das von einer Gruppe erstellt wird, die mit der XBRL-Spezifikation konform ist und den Austausch von Geschäftsinformationen ermöglicht.  

Ein XBRL **Instance Document** ist ein Geschäftsbericht, wie ein Finanzbericht, für die XBRL-Spezifikation. Die Bedeutung der Werte in dem Dokument werden durch die Taxonomie erklärt. In der Tat ist ein Instanzdokument ziemlich nutzlos, wenn Sie die Taxonomie nicht kennen, für die es erstellt wurde.  

## Mehrschichtige Taxonomien

Eine Taxonomie kann aus einer Basistaxonomie bestehen, zum Beispiel US GAAP (United States generally accepted accounting principles) oder IAS (international accounting standards), und dann eine oder mehrere Erweiterungen haben. Um dies widerzuspiegeln, verweist eine Taxonomie auf ein oder mehrere Schemata, die jeweils selbst separate Taxonomien sind. Wenn die zusätzlichen Taxonomien in die Datenbank geladen werden, werden die neuen Elemente einfach an die bestehenden Elemente angehängt.  

## Linkbases

In XBRL Spec. 2 wird die Taxonomie in mehreren XML-Dateien beschrieben. Die erste XML-Datei ist die Taxonomieschemadatei selbst (.xsd-Datei), die lediglich eine ungeordnete Liste von Elementen oder Informationen für den Bericht enthält. Darüber hinaus gibt es in der Regel einige Linkbase-Dateien (.xml). Die Linkbase-Dateien enthalten Daten, die die Rohtaxonomie (.xsd-Datei) ergänzen. Es gibt sechs Arten von Linkbase-Dateien, von denen vier für [!INCLUDE[prod_short](includes/prod_short.md)] relevant sind. Und zwar:

* Beschriftungslinkbase: Diese Linkbase enthält Beschriftungen oder Namen für die Elemente. Die Datei enthält möglicherweise Beschriftungen in verschiedenen Sprachen, die mit einer XML-Eigenschaft namens "lang" identifiziert werden. Der XML-Sprachidentifikator enthält in der Regel eine zweibuchstabige Abkürzung, und obwohl es leicht zu erraten sein sollte, was die Abkürzung bedeutet, gibt es keine Verbindung zum Microsoft Windows-Sprachcode oder den in den Demo-Daten definierten Sprachcodes. Wenn Sie also die Sprachen für eine bestimmte Taxonomie nachschlagen, sehen Sie alle Labels für das erste Element in der Taxonomie, d.h. Sie können für jede Sprache ein Beispiel sehen. Eine Taxonomie kann mit mehreren Label-Linkbases verknüpft sein, solange diese Linkbases verschiedene Sprachen enthalten.  
* Präsentations-Linkdatenbank: Diese Linkbase enthält Informationen über die Struktur der Elemente oder, genauer gesagt, darüber, wie der Herausgeber der Taxonomie die Anwendung vorschlägt, die Ihnen die Taxonomie präsentiert. Die Linkbase enthält eine Reihe von Links, die jeweils zwei Elemente in einer übergeordneten Beziehung zueinander verbinden. Bei der Anwendung dieser Verknüpfungen können die Elemente hierarchisch dargestellt werden. Beachten Sie, dass sich die Präsentations-Linkbase genau damit befasst: mit der Präsentation der Elemente für Sie.
* Kalkulations-Linkbase: Diese Linkbase enthält Informationen darüber, wie die Elemente aufgerollt werden. Die Struktur ist der Präsentationsdatenbank sehr ähnlich, außer dass jeder Link, oder 'Bogen', wie er genannt wird, eine Gewichtseigenschaft hat. Die Gewichtung kann entweder 1 oder -1 sein und gibt an, ob das Element zu seinem übergeordneten Element hinzugefügt oder von diesem abgezogen werden soll. Beachten Sie, dass die Rollups nicht unbedingt mit der visuellen Darstellung übereinstimmen.  
* Referenz-Linkbase: Bei dieser Linkbase handelt es sich um eine xml-Datei, die zusätzliche Informationen über die vom Taxonomie-Emittenten benötigten Daten enthält.

## XBRL-Zeilen festlegen

Nachdem Sie die Taxonomie importiert oder aktualisiert haben, müssen die Zeilen des Schemas mit allen Informationen ausgefüllt werden, die zur Erfüllung der jeweiligen Finanzberichterstattungsanforderungen erforderlich sind. Zu diesen Informationen gehören grundlegende Informationen über die Firma, der eigentliche Jahresabschluss, Anmerkungen zum Jahresabschluss, zusätzliche Zeitpläne und so weiter.  

Sie legen XBRL-Zeilen fest, indem Sie die Daten in der Taxonomie den Daten in Ihrem Hauptbuch zuordnen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **XBRL-Taxonomies** ein und wählen Sie dann den entsprechenden Link.  
2. Auf der Seite **XBRL-Taxonomies** wählen Sie eine Taxonomie in der Liste aus.  
3. Wählen Sie die Aktion **Zeilen** aus.  
4. Wählen Sie eine Zeile und füllen Sie die Felder aus.  
5. Durch Klicken auf die Aktion **Information** können Sie die Detailinformationen lesen.  
6. Um die Zuordnung der Sachkonten im Kontenplan zu den XBRL-Zeilen festzulegen, wählen Sie die Aktion **G/L-Zeilen zuordnen**.  
7. Um dem Finanzbericht eine Notiz hinzuzufügen, wählen Sie die **Notizen** Aktion.  

   > [!TIP]
   > Um Zeilen aus den exportierten Daten auszuschließen, wählen Sie als Quellentyp **NICHT ANWENDBAR**.

   > [!NOTE]  
   > Sie können nur Daten exportieren, die der Auswahl im Feld **Quelle Typ** entsprechen. Dies beinhaltet Beschreibungen und Hinweise.  

   > [!NOTE]  
   > Taxonomien können Elemente enthalten, die von [!INCLUDE[prod_short](includes/prod_short.md)] nicht unterstützt werden. Wenn ein Element nicht unterstützt wird, wird das Feld **Quelle Typ** **Unzutreffend** anzeigen und das Feld **Beschreibung** zeigt eine Fehlermeldung an, wie **Unerwarteter Typ: bestimmter Typ nicht erkannt**. Wenn Sie das Element exportieren müssen, wählen Sie einen passenden Quelltyp. In der Regel ist dies eine Konstante oder eine Beschreibung. Auf diese Weise können Sie zwar Daten eingeben und exportieren, aber solche Elemente haben möglicherweise Validierungsregeln, die vor dem Export nicht überprüft werden können.

## Importieren einer XBRL-Taxonomie

Der erste Schritt bei der Arbeit mit der XBRL-Funktionalität besteht darin, eine Taxonomie in die Datenbank Ihrer Firma zu importieren. Eine Taxonomie besteht aus einem oder mehreren Schema/ta und einigen Linkbases. Wenn Sie den Import des/der Schemas/Schemata und Linkbases durchgeführt haben und die Linkbases dem Schema zugewiesen haben, können Sie die Zeilen einrichten und die Sachkonten des Kontenplans den entsprechenden Taxonomiezeilen zuordnen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **XBRL-Taxonomies** ein und wählen Sie dann den entsprechenden Link.  
2. Erstellen Sie auf der Seite **XBRL Taxonomie** eine neue Zeile, und geben Sie Name und Beschreibung der Taxonomie ein.  
3. Wählen Sie die Aktion **Schemas** und fügen Sie dann die Beschreibung des Schemas ein.  
4. Um das Schema zu importieren, wählen Sie auf der Seite **XBRL-Schemata** die Aktion **Importieren** und wählen dann einen Ordner und eine XSD-Datei aus. Wählen Sie **Öffnen**.  
5. Um die Linkbase zu importieren, wählen Sie auf der Seite **XBRL-Schemata** die Aktion **Linkbases** und wählen dann einen Ordner und eine XML-Datei aus. Wählen Sie **Öffnen**.  
6. Jetzt können Sie die Linkbase auf das Schema anwenden. Wiederholen Sie den Vorgang, bis Sie alle Linkbases importiert haben.  
7. Wählen Sie die **Auf Taxonomie anwenden** Aktion aus, um die Linkbase auf das Schema anzuwenden.  

> [!IMPORTANT]  
> Anstatt die Linkbases einzeln nach dem Import anzuwenden, können Sie warten, bis Sie alle Linkbases importiert haben, und sie dann alle gleichzeitig anwenden. Wählen Sie dazu **NEIN**, wenn Sie aufgefordert werden, die neu importierte Linkbase auf das Schema anzuwenden. Wählen Sie dann die Zeilen mit den Linkbases aus, die Sie anwenden möchten.  

## Aktualisieren einer XBRL-Taxonomie

Wenn sich eine Taxonomie ändert, müssen Sie die aktuelle Taxonomie dementsprechend ändern. Der Grund für die Aktualisierung kann ein verändertes Schema, eine veränderte Linkbase oder eine neue Linkbase sein. Nach Aktualisierung der Taxonomie müssen Sie nur die Zeilen an die geänderten oder neuen Zeilen anpassen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **XBRL-Taxonomies** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **XBRL-Taxonomien** die Aktion **Schemas** aus.  
3. Um ein Schema zu aktualisieren, wählen Sie das Schema aus, das Sie aktualisieren möchten, und wählen Sie dann die Aktion **Importieren**.  
4. Um eine neue Linkbase zu aktualisieren oder hinzuzufügen, wählen Sie **Linkbases** aus.  
5. Markieren Sie die entsprechende Linkbase oder wählen Sie <kbd>Strg</kbd>+<kbd>N</kbd> für eine neue Zeile, wählen Sie den Typ der Linkbase und fügen Sie eine Beschreibung ein.  
6. Um die Linkbase zu importieren, wählen Sie die **Importieren** Aktion aus.  
7. Wählen Sie **Ja**, um die Linkbase auf das Schema anzuwenden.  

## Siehe dazu die Schulung unter [Microsoft Learn](/learn/modules/xbrl-reports-dynamics-365-business-central/index).

## Siehe auch

[Financial Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
