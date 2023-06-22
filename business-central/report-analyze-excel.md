---
title: Analysieren von Berichtsdaten mit Excel und XML
description: 'Lernen Sie, wie Sie mit Excel und XML ein Dataset für einen Bericht analysieren können.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, Word, dataset'
ms.date: 03/16/2022
ms.author: jswymer
---
# <a name="analyzing-report-data-with-excel-and-xml" />Analysieren von Berichtsdaten mit Excel und XML

[!INCLUDE[2021_releasewave2](includes/2021_releasewave2.md)]

Als Entwickler oder fortgeschrittener Benutzer ist es hilfreich, die Daten, die für ein bestimmtes Dataset eines Berichts erzeugt werden, zu prüfen, während Sie neue Berichte erstellen oder bestehende Berichte ändern. Um diese Funktion zu unterstützen, können Sie einen Berichtsdatensatz als Rohdaten in eine Excel-Arbeitsmappe oder eine XML-Datei exportieren direkt. In Excel können Sie beispielsweise dann eine Ad-hoc-Analyse der Daten durchführen und Probleme diagnostizieren.

## <a name="get-started" />Erste Schritte

Um einen Berichtsdatensatz in eine Excel-Arbeitsmappe oder eine XML-Datei zu exportieren, öffnen Sie den Bericht im Client und wählen Sie dann auf der Anforderungsseite **Senden an** > **Microsoft Excel-Dokument (nur Daten)** oder **XML-Dokument**. Die Datei wird auf Ihr Gerät heruntergeladen.

## <a name="more-about-excel-data-only" />Mehr über Excel (nur Daten)

**Microsoft Excel Beleg (nur Daten)** Die Option exportiert die Berichtsergebnisse und die Kriterien, die zu ihrer Erstellung verwendet wurden &mdash;aber sie enthält nicht das Berichtslayout. Die Excel-Datei enthält das komplette Dataset, als Rohdaten, angeordnet in Zeilen und Spalten. Alle Datenspalten des Datasets des Berichts sind enthalten, unabhängig davon, ob sie im Berichtslayout verwendet werden.

Sobald Sie die Excel-Datei haben, können Sie mit der Analyse der Daten beginnen. Sie könnten zum Beispiel die Daten filtern und Power Pivot verwenden, um sie anzuzeigen.

Jedes Mal, wenn Sie Ergebnisse exportieren, wird ein neues Arbeitsblatt erstellt. Mit der Option **Microsoft Excel Beleg (nur Daten)** können Sie denselben Bericht ausführen und Formatierungsänderungen wiederverwenden. Zum Beispiel können Sie für Power Pivot den Bericht für einen anderen Zeitraum erneut ausführen, die Ergebnisse in das Arbeitsblatt kopieren und dann das Arbeitsblatt aktualisieren. Eine App für Berichte finden Sie auch auf [AppSource](https://appsource.microsoft.com/).

> [!NOTE]
> Sie können keinen Bericht exportieren, der mehr als 1.048.576 Zeilen oder 16.384 Spalten hat. Bei Business Central lokal kann die maximale Anzahl der exportierten Zeilen sogar noch geringer sein. Business Central Server enthält eine Konfigurationseinstellung mit der Bezeichnung **Maximal zulässige Anzahl der an Excel zu sendenden Datenzeilen**, mit der Sie die Grenze vom Maximalwert herabsetzen können. Weitere Informationen finden Sie unter [Konfiguration von Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) oder wenden Sie sich an Ihren Administrator.

## <a name="for-administrators" />Für Administratoren

- **Microsoft Excel Beleg (nur Daten)** wurde als optionale Funktion in der 2021er Release-Welle 1, Update 18.3 eingeführt. Um Benutzern Zugriff auf diese Funktion zu geben, wenn Sie Veröffentlichungszyklus Welle 1 2021 ausführen, aktivieren Sie die Funktion **Berichts-Dataset in Microsoft Excel Beleg speichern** in **Funktionsverwaltung**. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management). In der Release-Welle 2 von 2021 wurde diese Funktion permanent, so dass Sie sie nicht mehr aktivieren müssen.

- Um die Funktion **Microsoft Excel Dokument (nur Daten)** zu verwenden, benötigen Benutzerkonten die Berechtigung **Aktion Exportieren von Berichtsdataset nach Excel zulassen**. Sie können Benutzern diese Berechtigung erteilen, indem Sie entweder die Berechtigung **Fehlerbehebungtools** oder **Export Bericht Excel** festlegen. Weitere Informationen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)  

## <a name="for-developers-and-advanced-users" />Für Entwickler und fortgeschrittene Benutzer

Die Option **Microsoft Excel Dokument (nur Daten)** exportiert alle Spalten, einschließlich Spalten, die Filter und Formatierungsanweisungen für andere Werte enthalten. Hier sind einige Punkte von Interesse:

- Binäre Daten in einem Feld, wie ein Bild, werden nicht exportiert.

  In Spalten, die binäre Daten enthalten, enthalten Felder den Text **Binäre Daten ({0} Bytes)**, wobei **{0}** die Anzahl der Bytes angibt.
- Ab Business Central 2021 Release Wave 2 enthält die Excel-Datei auch das Arbeitsblatt **Berichts-Metadaten**.

  Dieses Arbeitsblatt zeigt die auf den Bericht angewendeten Filter und allgemeine Berichtseigenschaften, wie Name, ID und Erweiterungsdetails. Die Filter werden in der Spalte **Filter (DataItem ::Table ::FilterGroupNo ::FieldName)** angezeigt. Die Filter in dieser Spalte enthalten Filter, die auf der Anforderungsseite des Berichts festgelegt wurden. Sie enthält auch Filter, die im AL-Code definiert sind, zum Beispiel durch die [DataItemLink-Eigenschaft](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) und [DataItemTableView-Eigenschaft](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Weitere Informationen zur Berichtsgestaltung finden Sie unter [Berichtsübersicht](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

## <a name="see-also" />Weitere Informationen

[Arbeiten mit Berichten](ui-work-report.md)  
[Verwaltung von Berichts- und Dokumentlayouts](ui-manage-report-layouts.md)  
[Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
