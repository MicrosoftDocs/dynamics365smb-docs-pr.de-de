---
title: Die Data Archive-Erweiterung
description: Die Archivierung von Daten erstellt ein kostengünstiges Backup Ihrer Datensätze.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 630
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: e2df40494f72260a1ce7e66f57ea1c96fb35b301
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8130826"
---
# <a name="the-data-archive-extension"></a>Die Data Archive-Erweiterung
Im Laufe der Zeit wird sich in Ihrem Unternehmen eine beträchtliche Menge an Daten ansammeln, und als Administrator ist es wahrscheinlich eine gute Idee, eine Strategie für die Archivierung von Daten zu haben. Viele Daten können die Arbeit verlangsamen, z.B. kann es etwas länger dauern, Berichte zu erstellen oder sogar Datensätze zu sperren. Außerdem können große Datenmengen zu erhöhten Speicherkosten führen.

Die Data Archive-Erweiterung bietet ein grundlegendes Framework für die Archivierung und Sicherung von Daten im Rahmen der Datumsverdichtung. Wenn Sie die Datenkomprimierung verwenden, werden zusammenhängende Einträge in einem einzigen Eintrag konsolidiert und die Originale werden gelöscht. Weitere Informationen finden Sie unter [Komprimieren von Daten mit der Datumskomprimierung](admin-manage-documents.md#compress-data-with-date-compression). Es kann jedoch sinnvoll sein, diese Daten zu behalten. Anstatt sie zu löschen, können Sie sie zur späteren Verwendung archivieren.

## <a name="start-archiving-data"></a>Archivierung von Daten starten
Die Erweiterung ist vorinstalliert und auf der **Erweiterungsverwaltung** verfügbar, sodass Sie nichts weiter tun müssen, um loszulegen. Die Erweiterung ist in Microsoft AppSource verfügbar. 

Ihre Datenarchive werden auf der Seite **Datenarchivliste** aufgelistet. Jedes Archiv kann Daten aus mehreren Tabellen enthalten und kann bis zu 10.000 Datensätze aufnehmen. Gibt es mehr als 10.000 Datensätze in einer Tabelle, wird ein zweites Archiv für die nächsten 10.000 Datensätze erstellt usw. Wenn Sie z.B. 10.100 Sachbucheinträge archivieren, erstellt Business Central ein „Sachbucheintrag“-Archiv für die ersten 10.000 Einträge und dann ein zweites Archiv für die restlichen 100 Einträge. 

Nachdem Sie die Daten archiviert haben, können Sie sie mit Microsoft Excel oder als CSV-Datei durchsuchen.

* Wenn Sie die Excel-Option verwenden, enthält die Arbeitsmappe ein Arbeitsblatt für jede Datenarchivtabelle.
* Wenn Sie die CSV-Option verwenden, erhalten Sie eine ZIP-Datei mit einer CSV-Datei für jede Datenarchivtabelle.

> [!TIP]
> Die Excel- und CSV-Optionen erleichtern die Verwendung einer anderen App oder eines anderen Dienstes, um die Daten an einen anderen Lagerort zu verschieben, z. B. in den Azure Blob storage oder in ein Analyse-Tool, z. B. Microsoft Power BI.

Die Data Archive-Erweiterungen werden von den folgenden Batchaufträgen zur Datenkomprimierung verwendet.

|Batchaufträge  |
|---------|
|Datum Komp. Element Budget-Einträge |
|Datum komprimieren Bankabst. Posten |
|Datum Debitoren-Posten komprimieren |
|Datum Komprimieren FA-Posten |
|Datum Komprimieren Allgemeiner Posten |
|Datum Komprimieren Versicherung Posten |
|Datum Komprimieren Wartung. Posten |
|Datum Komprimieren Wartung. Posten |
|Datum Komprimieren Ressourcen Posten |
|Datum Komprimieren MwSt.-Posten |
|Datum Kreditor-Posten komprimieren |
|Datum Komprimieren Whse. Posten |
|Datum Kompr. Finanzbudgetposten |

Um die Archivierung von Daten zu starten, wenn Sie einen der Batchaufträge ausführen, schalten Sie die Option **Löschte Einträge archivieren** ein.

## <a name="storage-considerations"></a>Überlegungen zur Speicherung
Die archivierten Daten werden in der Tabelle **Tenant-Medien** gespeichert. Diese Tabelle wird bei der Berechnung der Datenbankgröße gemäß Ihren Lizenzbedingungen nicht berücksichtigt. Stattdessen zählt sie als Dateispeicher. Wir empfehlen Ihnen jedoch, alte Archive z.B. in eine CSV-Datei zu exportieren und dann die alten Datensätze zu löschen.

## <a name="see-also"></a>Weitere Informationen
[Speicher durch Löschen von Belegen oder Komprimieren von Daten verwalten](admin-manage-documents.md)
