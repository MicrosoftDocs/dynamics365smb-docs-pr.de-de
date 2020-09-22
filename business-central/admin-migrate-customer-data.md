---
title: Migrate Customer Data | Microsoft Docs
description: Sie können vorhandene Debitorendaten aus einem vorhandenen ERP-System zu Business Central migrieren, indem Sie die Datenmigrationswerkzeuge aus RapidStart Services verwenden. Sie können Excel-.xlsx-Dateien als Datenträger verwenden. Sie können die Daten auch manuell umlagern, indem Sie sie direkt in den Mandanten eingeben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 33d5caec7086d12b9a2450fc36224987c5a97642
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783526"
---
# <a name="migrate-customer-data"></a>Migrieren von Debitorendaten
Sie können vorhandene Debitorendaten aus einem vorhandenen ERP-System nach [!INCLUDE[d365fin](includes/d365fin_md.md)] migrieren, indem Sie die Datenmigrationswerkzeuge aus RapidStart Services verwenden. Sie können Excel-.xlsx-Dateien als Datenträger verwenden. Sie können die Daten auch manuell umlagern, indem Sie sie direkt in den Mandanten eingeben.

> [!NOTE]
> Felder vom Typ Blob können nicht mithilfe von Excel exportiert/importiert werden.

Die Seite **Migrationsübersicht** und das **Konfigurationsarbeitsblatt** bieten Zugriff auf Funktionen und Ansichten, um alle Aufgaben im Zusammenhang mit der Datenmigrierung auszuführen. Es ist empfehlenswert, dass Sie eine Tabelle jeweils einzeln migrieren, um alle Abhängigkeiten in Ihren Daten zu berücksichtigen. Von der Migration sind auch die Stammdatentabellen betroffen, die Informationen zu Debitoren, Kreditoren, Artikeln, Kontakten und der Finanzbuchhaltung enthalten.  

## <a name="to-import-configuration-packages"></a>So importieren Sie ein Konfigurationspaket
Wenn Sie ein neues Unternehmen erstellen, können Sie Unternehmenseinstellungen für den neuen Mandanten importieren. Sie importieren die Einstellungen von einer .rapidstart-Datei, die die Paketinhalte in einem komprimierten Format bereitstellt. Ein entsprechender Satz von Standard-Datenmigrationstabellen wird importiert. Der Datensatz enthält Stammdatentabellen und die Einrichtungsdatentabellen. Ihre erste Aufgabe bei der Datenmigration besteht in der Einschätzung, ob die Einrichtung der Standardmigration die Anforderungen des neuen Mandanten erfüllt.

> [!NOTE]  
>  Sie können eine Datei, die nicht bereits ein RapidStart Services-Konfigurationspaket ist, nicht als eine .rapidstart-Konfigurationspaketdatei umbenennen und versuchen, sie zu importieren. Wenn Sie versuchen so zu tun, erhalten Sie eine Fehlermeldung.  

Bevor Sie beginnen, müssen Sie sicherstellen, dass Sie über die Berechtigung zum Ausführen von RapidStart Services-Objekten verfügen. Sie können beispielsweise über die Berechtigungssätze SUPER oder D365 RAPIDSTART verfügen. Wir empfehlen außerdem, dass Sie sich in einem Rollencenter mit Links zu RapidStart Services, wie dem Verwaltungsrollencenter befinden. Weitere Informationen finden Sie unter [So ändern Sie die Rolle](ui-change-basic-settings.md#to-change-the-role).  

> [!IMPORTANT]  
> Wenn Sie Konfigurationspakete zwischen zwei Mandantendatenbanken exportieren und importieren, sollten die Datenbanken dasselbe Schema haben, damit sichergestellt ist, dass alle Daten erfolgreich übertragen werden. Das bedeutet, dass die Datenbanken dieselbe Tabelle und Feldstruktur aufweisen sollten, wobei die Tabellen dieselben Primärschlüssel und die Felder dieselben IDs und Datentypen haben.  
>
>  Sie können ein Konfigurationspaket importieren, das aus einer Datenbank exportiert wurde, die ein anderes Schema als die Zieldatenbank hat. Allerdings werden Tabellen oder Felder im Konfigurationspaket, die in der Zieldatenbank fehlen, nicht importiert.
>
> Tabellen mit unterschiedlichen Primärschlüsseln und Felder mit unterschiedlichen Datentypen werden ebenfalls nicht erfolgreich importiert. Wenn das Konfigurationspaket beispielsweise die Tabelle **Debitor 50000** mit dem Primärschlüssel **Code20** enthält und die Datenbank, in die Sie das Paket importieren die Tabelle **Debitor Bankkonto 50000** mit dem Primärschlüssel **Code20 + Code 20** enthält, werden diese Daten nicht importiert.  

1. Öffnen Sie das neue Unternehmen.  
2. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Konfigurationspakete** ein, und wählen Sie dann den zugehörigen Link.  
3. Wählen Sie die **Paket importieren**-Aktion aus. Navigieren Sie zur .rapidstart-Paketdatei, die Sie importieren möchten, und wählen Sie die **Öffnen** Aktion aus. Während des Imports werden die Paketinhalte dekomprimiert und der Paketdatensatz wird erstellt.  

    Nach Abschluss des Imports können Sie die Anzahl der Konfigurationstabellen, die importiert wurden, im Feld **Anzahl Tabellen** sehen.  
4. Um die Konfigurationstabellen zu überprüfen, wählen Sie die **Ansicht** Aktion.  
5. Um das gesamte Paket anzuwenden, wählen Sie **Paket anwenden**.  

    > [!NOTE]  
    >  Die Datenmigrationsinformationen basieren auf Konfigurationsvorlagen, wenn Sie eine angeben. Sie müssen die Vorlage zuerst aktualisieren, um die Liste der Felder zu ändern.  

6.  Um die Feldauswahl zu überprüfen, wählen Sie eine Tabelle aus, und wählen Sie dann auf der Registerkarte **Zeilen**, wählen Sie die **Felder** Aktion aus. Vergleichen und prüfen Sie die Anzahl der Felder, die von der Anzahl der Felder verfügbar sind, deren Daten angewendet wurden.  

Wenn die Auswahl der Tabellen für die Datenmigration Ihre Anforderungen nicht erfüllt, können Sie eine oder mehrere neue Datenmigrationsdateien erstellen. Wenn die Dateien für die Datenmigration genügen, können Sie mit der Datenmigration unter Verwendung von XLS- oder XML-Dateien fortfahren.

## <a name="to-create-a-data-migration-file"></a>So erstellen Sie eine Datenmigrationsdatei

Sie können neue Datenmigrationsdateien erstellen und diese anpassen, sodass sie Ihr Geschäft zu unterstützen.  

> [!TIP]
> Eine Datei kann nur verwendet werden, um ein Feld zu migrieren, das den **FieldClass**-Eigenschaftensatz **Normal** hat.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Konfigurationspaket** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie und öffnen Sie ein Paket, das Sie verwenden möchten, um Daten zu migrieren, und wählen Sie die **Tabellen abrufen** Aktion aus. Die Seite **Pakettabelle abrufen** wird geöffnet.  
3. Geben Sie im Feld **Tabellen-ID** eine Tabellennummer ein oder wählen Sie eine Tabelle aus der Liste, zum Beispiel Tabelle 18, **Debitor**. Das Feld **Tabellennamen** wird automatisch ausgefüllt.  
4. Wählen Sie die neue Migrationstabelle aus, und dann, auf der Registerkarte **Tabellen** aus, wählen Sie die **Felder** Aktion aus. Die Seite **Migrationsfeld** wird geöffnet.  
5. Deaktivieren Sie das Kontrollkästchen **Feld einschließen** für jedes Feld, das Sie nicht importieren möchten, und wählen Sie dann **Eingeschlossene festlegen** oder die **Eingeschlossene löschen** Aktion aus.  

> [!IMPORTANT]  
>  Wenn das Kontrollkästchen **Feld einschließen** standardmäßig aktiviert wird, ist dieses Feld ein Teil des Primärschlüssels. Die Auswahl sollte nicht gelöscht werden, ansonsten werden Fehler eingegeben und der Datensatz kann nicht importiert werden.  
>
>  Wenn Sie ein Feld einbinden, das eine Verbindung mit einer anderen Tabelle hat, wird das Kontrollkästchen **Feld überprüfen** automatisch ausgewählt. Die Prüfung kann zur Aktualisierung anderer Felder in dieser und anderen Tabellen führen und wird in der Reihenfolge der Feldnummern ausgeführt.  

Eine neue Migrationstabelle wird erstellt.  

## <a name="to-export-data-migration-files"></a>So exportieren Sie Datenmigrationsdateien
Nachdem Sie die Tabellen festgelegt haben, für die Sie Debitorendaten übertragen möchten, exportieren Sie die Dateien.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Konfigurationspakete** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das Paket aus, das Sie für den Export verwenden möchten, und öffnen Sie es.
3. Wählen Sie die Tabelle oder die Tabellen, die Sie exportieren möchten, und wählen die **In Excel exportieren** Aktion aus.
4. Speichern Sie die exportierte Excel-Datei.  
5. Wiederholen Sie diesen Vorgang für alle relevanten Datenmigrationstabellen. Wenn Sie mehrere Tabellen gleichzeitig ausgewählt haben, werden ihre Daten in eine Gemeinschaftstabelle exportiert.  

Wenn die Excel-Tabelle leer ist, enthält die resultierende Datenmigrationsdatei leere Zellen für die Felder, die Sie ausgewählt haben, als Sie Migrationstabellen für den neuen Mandanten ausgewählt oder erstellt haben. Wenn die ausgewählte Datenmigrationstabelle Daten enthält, wird sie exportiert.  

## <a name="to-map-values-to-be-used-during-import"></a>Werte zuordnen, die während des Imports verwendet werden sollen
Wenn Sie Daten anwenden, die Sie aus Excel oder von einem RapidStart-Paket importiert haben, behandelt [!INCLUDE[d365fin](includes/d365fin_md.md)] die Verteilung basierend auf der Tabellenrelationen:  

- Wenn Sie ein Zuordnung direkt für ein Feld in einer Tabelle definieren, dann verwendet [!INCLUDE[d365fin](includes/d365fin_md.md)] sie.  

- Wenn das Feld eine Relation zu einer anderen Tabelle hat, sucht [!INCLUDE[d365fin](includes/d365fin_md.md)] nach der Karte für das Feld "Primärschlüssel" in der zugehörigen Tabelle. Die verknüpfte Tabelle muss jedoch Teil des Konfigurationspakets sein.  

- Wenn das Zuordnen von Informationen an beiden Stellen definiert ist, für das Feld direkt und für den Primärschlüssel in der zugehörigen Tabelle, dann sucht [!INCLUDE[d365fin](includes/d365fin_md.md)] an beiden Stellen nach der Zuordnung.  

- Wenn die gleichen Zuordnungen direkt für ein Feld und in der zugehörigen Tabelle definiert sind, jedoch verschiedene Neuwerte haben, hat die Zuordnung, die direkt für das Feld definiert ist, eine höhere Priorität als die Zuordnung, die für die Tabelle definiert ist, auf die das Feld verweist.  

In den Verfahren, die folgen, sollten Sie im Voraus überprüfen, welche Werte Sie während des Migrationsvorgangs beibehalten möchten. Um die folgenden Verfahren auszuführen, benötigen Sie die Datenmigrationsdateien (.xls), die Sie aus [!INCLUDE[d365fin](includes/d365fin_md.md)] exportiert haben. Weitere Informationen finden Sie unter [So werden Datenmigrationsdateien exportiert](admin-migrate-customer-data.md#to-export-data-migration-files)

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Konfigurationspakete** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie das betreffende Konfigurationspaket.  
3. Wählen Sie die Tabelle, für die Sie Werte zuordnen möchten, und wählen Sie dann im Inforegister Tabellen die Option **Tabelle** und dann **Felder** aus.  
4. Für jedes Feld, das Sie zuordnen möchten, wählen Sie die **Zuordnung** Aktion aus.  
5. Geben Sie im Feld **Alter Wert** den Wert ein, den Sie ändern wollen. Geben Sie im Feld **Neuer Wert** den Wert ein, auf den Sie den alten Wert ändern wollen. Wählen Sie die Schaltfläche **OK** aus.  
6. Importieren Sie die Debitorendaten. Weitere Informationen finden Sie unter [So werden Kundendaten importiert](admin-migrate-customer-data.md#to-import-customer-data).
7. Prüfen Sie im Feld **Anzahl der Paketfehler**, ob Fehler gemeldet wurden. Ist dies der Fall, führen Sie Drilldown einen durch, um die Fehler anzuzeigen. Die Seite **Paketdatensätze konfig.** wird geöffnet.
8. Wählen Sie die Aktion **Fehler anzeigen** aus. Sie erhalten den folgenden Fehler: **XX ist keine gültige Option. Gültige Optionen sind: XX**. Wählen Sie die Schaltfläche **OK** aus.  
9. Um die Karte zu übernehmen die Sie eingerichtet haben, aktivieren Sie die **Daten übernehmen** Aktion.  

### <a name="mapping-example"></a>Zuordnungs-Beispiel  
Im folgenden Beispiel wird veranschaulicht, wie [!INCLUDE[d365fin](includes/d365fin_md.md)] Zuordnungsdefinitionen implementiert.  

1. Eine Konfigurationstabelle erstellen, die eine **Verkäufer/Käufer**-Tabelle hat. Definieren Sie eine Karte für das Feld **Code**.  
2. Fügen Sie zusätzliche Tabellen dem Paket hinzu, zum Beispiel **Debitor** und **Kreditor**. Diese beiden Tabellen referenzieren zur Tabelle **Verkäufer/Käufer** über die Felder **Einkäufercode** und **Verkäufercode**.  
3. Wenn Sie Daten ausgleichen, wird die Zuordnung, die Sie für das Feld **Code** in der Tabelle **Verkäufer/Käufer** bereitgestellt haben, auch während der Verarbeitung der Felder **Verkäufercode** und **Einkäufercode** berücksichtigt.

## <a name="to-add-additional-values-to-d365fin"></a>Um [!INCLUDE[d365fin](includes/d365fin_md.md)] weitere Werte hinzufügen  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Konfigurationspakete** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Tabelle, für die Sie zusätzliche Werte zuordnen möchten, und wählen Sie dann im Inforegister Tabellen die Option **Tabelle** und dann **Felder** aus.  
3. Für die Felder, für die Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] während der Migration zusätzliche Werte ermöglichen möchten, wählen Sie das **Fehlende Codes erstellen**-Kontrollkästchen.  
4. Importieren Sie die Debitorendaten. Weitere Informationen finden Sie unter [So werden Kundendaten importiert](admin-migrate-customer-data.md#to-import-customer-data).

## <a name="to-clean-up-and-process-data-before-applying-data"></a>So werden Daten bereinigt und verarbeitet, bevor Daten angewendet werden
In einigen Fällen möchten Sie möglicherweise Debitorendaten bereinigen und sie verarbeiten, bevor Sie sie auf die Datenbank anwenden. Um das zu tun, können Sie die **Config. Paket - Prozess** Stapelverarbeitung verwenden, um Probleme zu reparieren, beispielsweise:  

- Konvertieren von Datumswerten und Dezimalzahlen in das Format, das fü die regionalen Einstellungen auf dem Computer eines Benutzers erforderlich ist.  
- Entfernen Sie die Leerzeichen am Anfang oder Ende oder Sonderzeichen.  

Nachdem Sie die Stapelverarbeitung geändert haben, verwenden Sie das folgende Vorgehen, um die Daten zu verarbeiten.  

1. Öffnen Sie das Konfigurationspaket für den Mandanten.  
2. Wählen Sie die **Daten verarbeiten** Aktion aus.  
3. Um die Karte zu übernehmen die Sie eingerichtet haben, aktivieren Sie die **Daten übernehmen** Aktion.

## <a name="to-migrate-customer-data"></a>Migrieren von Debitorendaten
Nachdem Sie eine Migrationstabelle exportiert haben, besteht Ihr nächster Schritt darin, die Stammdaten des Debitors einzugeben. Um Ihre Aufgaben zu vereinfachen, können Sie die in Excel integrierten XML-Änderungswerkzeuge nutzen. Sie können die in Excel integrierten Funktionen auch für die Datenformatierung und zum Verschieben von Daten in die richtige Zelle verwenden.

Für Hilfe mit XML aktivieren Sie die Registerkarte **Entwickler**, und wählen Sie die **Herkunft** Aktion aus, um das XML-Schema der Migrationstabelle anzuzeigen, wie in Excel dargestellt.

Das folgende Verfahren basiert auf einem Excel-Arbeitsblatt, das Sie für die Migration erstellt haben. Weitere Informationen finden Sie unter [So werden Datenmigrationsdateien exportiert](admin-migrate-customer-data.md#to-export-data-migration-files)

> [!IMPORTANT]  
> Ändern Sie nicht die Spalten in den Excel-Arbeitsblättern. Wenn sie verschoben, geändert oder gelöscht werden, kann das Arbeitsblatt nicht in [!INCLUDE[d365fin](includes/d365fin_md.md)] importiert werden.

1. Öffnen Sie in Excel die exportierte Datendatei. Es gibt ein Arbeitsblatt mit dem Namen der Tabelle.
2. Benennen Sie Tabelle1 um, um anzugeben, dass das Arbeitsblatt zur Datenumwandlung verwendet wird. Kopieren Sie die Überschriftenzeile ohne Formatierung aus der exportierten Tabelle in das neue Arbeitsblatt.
3. Kopieren Sie alle Ihre Debitorendaten in ein drittes Arbeitsblatt. Benennen Sie das Arbeitsblatt in z. B. "Stammdaten" um.
4. Verwenden Sie eine Excel-Formel, um Daten im Arbeitsblatt für die Datenumwandlung zwischen den Feldern im exportierten Datenblatt und in den Debitorenstammdaten zuzuordnen.
5. Sobald Sie alle Daten zugeordnet haben, kopieren Sie den Bereich der Daten in das Arbeitsblatt mit der Migrationstabelle.
6. Speichern Sie die Datei und vergewissern Sie sich, dass Sie den Dateityp nicht ändern.

Jetzt können Sie die Datenmigrationsdateien, die Debitorenstammdaten enthalten, in [!INCLUDE[d365fin](includes/d365fin_md.md)] importieren.

## <a name="to-import-customer-data"></a>So importieren Sie Debitorendaten
Nachdem die Debitorendaten in die Excel-Dateien für die Datenmigration eingegeben wurden, importieren Sie die Dateien in [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Öffnen Sie die Seite **Konfigurationspaketkarte**.
2. Wählen Sie die Tabelle, für die Sie Werte importieren möchten, und wählen Sie dann im Inforegister Tabellen die Option **Tabelle** und dann **Von Excel importieren** aus.
3. Suchen und öffnen Sie die Datei, aus der Sie Daten importieren möchten.
4. Auf der Seite **Vorschau des Konfigurationspaketimports** überprüfen Sie den Inhalt, der importiert wird.

    Die Seite **Vorschau des Konfigurationspaketimports** bietet einen Überblick über den Excel-Dateiinhalt, der importiert werden soll. Außerdem wird angegeben, wenn ein neues Paket erstellt oder das vorhandene aktualisiert wird und wenn neue Konfigurationspaketpositionen (Tabellen) erstellt oder vorhandene aktualisiert werden.    
5. Wählen Sie die Aktion **Importieren** aus

Daten aus der Datei werden in die Konfigurationspakettabellen importiert. Sie können die Anzahl der Datenbanksätzen anzeigen, die im Feld **Anzahl Datenbanksätze** importiert wurden. Darüber hinaus können Sie die Anzahl der Migrationsfehler sehen.

## <a name="to-validate-customer-data"></a>So überprüfen Sie Debitorendaten
Debitorendaten müssen überprüft werden, bevor Sie die Datensätze auf die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank anwenden.  

> [!NOTE]  
>  In den meisten Fällen werden ungültige Daten nicht in der Datenbank erstellt. Jedoch kann die Anwendung gelegentlich gesperrt werden, wenn eine importierte Migrationstabelle Fehler enthält.  

1. Auf der Seite **Migrationsübersicht** überprüfen Sie das Feld **Anzahl Migrations-Fehlern**, um festzustellen, ob Fehler während des Imports aufgetreten sind.  
2. Wenn Fehler vorhanden sind, wählen Sie die Migrationstabelle und im Inforegister Tabellen **Tabelle** und anschließend **Fehler.** Das Kontrollkästchen **Ungültig** ist für jeden Datensatz aktiviert, der einen Fehler aufweist.  
3. Um Fehler zu prüfen, wählen Sie eine Zeile aus, und klicken Sie dann auf der Registerkarte Start auf **Fehler anzeigen**.  

    Das Feld **Fehlertext** enthält die Ursache für den Fehler. Das Feld **Feldbezeichung** enthält die Bezeichnung des Feldes, das den Fehler enthält.  
4.  Um einen Fehler zu korrigieren oder eine Aktualisierung vorzunehmen wählen Sie auf der Seite, **Migrationsübersicht** den **Migrationsdatensatz** und wählen Sie dann auf der Seite **Migrationsdatensatz** und korigieren den Datensatz mit dem Fehler.  

Nachdem Sie eine Korrektur durchgeführt haben, wird der Datensatz aus der Datensatzliste auf der Seite **Datenfehler migrieren** entfernt.  

Jetzt können Sie die Daten des Debitors auf die Datenbank anwenden.  

## <a name="to-apply-customer-data"></a>So wenden Sie Debitordaten an
Wenn Sie alle Datenmigrationsdatensätze, die gültig und fehlerlos sind, importiert haben, können Sie die Datensätze bei der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank anwenden.  

1. Öffnen Sie die Seite **Konfigurationspakete**.  
2. Wählen Sie eine Tabelle für die Datenmigrations aus, die Sie anwenden möchten und wählen Sie **Daten übernehmen** aus.

Sie können die Anzahl der Datenbanksätzen anzeigen, die im Feld **Anzahl Datenbanksätze** erstellt wurden. Sie können die Anzahl der Datenbanksätzen anzeigen, die im Feld **Anzahl Datenbanksätze** erstellt wurden.  

Die Unternehmensdatenbank des Debitors ist jetzt eingerichtet, und grundlegende Daten wurden importiert. Ihre nächsten Schritte im Implementierungsprozess bestehen darin, Benutzer zu schulen, Prozesse zu definieren, zusätzliche Daten zu erstellen, Berichte anzupassen usw.

## <a name="see-also"></a>Siehe auch  
[Einrichten eines Unternehmens mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)
