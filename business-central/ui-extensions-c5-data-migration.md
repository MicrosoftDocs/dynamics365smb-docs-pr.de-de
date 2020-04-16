---
title: C5-Datenmigrations-Erweiterung verwenden | Microsoft Docs
description: Verwenden Sie diese Erweiterung, um Debitoren, Kreditoren, Artikel und Sachkonten von Microsoft Dynamics C5 2012 zu Business Central zu migrieren.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: cdf14002e28b777441a803fc7804fdac8afe5b77
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194331"
---
# <a name="the-c5-data-migration-extension"></a>Die C5-Datenmigrations-Erweiterung
Verwenden Sie diese Erweiterung, um Debitoren, Kreditoren, Artikel und Sachkonten von Microsoft Dynamics C5 2012 zu [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren. Sie können historische Posten für Sachkonten auch migrieren.

> [!Note]
> Der Mandant darf in [!INCLUDE[d365fin](includes/d365fin_md.md)] keine Daten in enthalten. Nachdem Sie mit der Migration begonnen haben, erstellen Sie keine Debitoren, Kreditoren, Artikel oder Konten, bis die Migration beendet wurde.

## <a name="what-data-is-migrated"></a>Welche Daten migriert?
Die folgenden Daten werden für jede Einheit migriert:

**Debitoren**
* Kontakte  
* Ort
* Land
* Debitoren-Dimensionen (Abteilung, Kostenträger, Kostenstelle)
* Lieferbedingungsmethode
* Verkäufer
* Zahlungsbedingungen
* Zahlungsform
* Debitorenpreisgruppe
* Debitorenrechnungsrabatt

Wenn Sie Konten migrieren, werden auch die folgenden Daten migriert:

* Debitorenbuchungsgruppe
* Fibu Buch.-Blattname
* Migrieren Sie offene Debitorenposten (Debitorenbucheinträge)

**Kreditoren**
* Kontakte
* Ort
* Land
* Debitoren-Dimensionen (Abteilung, Kostenträger, Kostenstelle)
* Rechnungsrabatt
* Lieferbedingungsmethode
* Einkäufer
* Zahlungsbedingungen
* Zahlungsform
* Kreditorenrechnungsrabatte

Wenn Sie Konten migrieren, werden auch die folgenden Daten migriert:

* Kreditorenbuchungsgruppe
* Fibu Buch.-Blattname
* Öffnen Sie das Fenster Transaktionen (Kreditorenposten)

**Artikel**
* Ort
* Land
* Element-Dimensionen (Abteilung, Kostenträger, Kostenstelle)
* VK-Zeilenrabatte
* Debitorenrabattgruppen
* Artikelrabattgruppen
* Verkaufspreis
* Zollposition
* Einheiten
* Artikelverfolgungscode
* Debitorenpreisgruppe
* Montagestücklisten

Wenn Sie Konten migrieren, werden auch die folgenden Daten migriert:

* Lagerbuchungseinrichtung
* Buchungsmatrix Einrichtung
* Artikel Buch.-Blattname
* Öffnen Sie das Fenster Transaktionen (Artikel Kreditorenposten)

> [!Note]
> Wenn es offene Transaktionen gibt, die Fremdwährungen verwenden, werden die Wechselkurse für alle Währungen auch migriert. Andere Wechselkurse werden nicht migriert.

**Kontenplan**  
* Standard-Dimensionen (Abteilung, Kostenträger, Kostenstelle)  
* Historische Transaktionen  

> [!Note]
> Historische Transaktionen werden so gut unterschiedlich behandelt. Wenn Sie Daten migrieren, setzen Sie einen **Aktuelle Periode** Parameter. Dieser Parameter gibt an, wie Ihre Transaktionen verarbeitet werden. Transaktionen nach diesem Datum werden einzeln migriert. Transaktionen vor diesem Zeitpunkt werden pro Konto aggregiert und migriert als einzelner Betrag. Nehmen wir an, es gibt Transaktionen 2015, 2016, 2017 und 2018 und Sie definieren 1. Januar 2017 im aktuellen Periodenfeld. Für jedes Konto sind Beträge für Transaktionen an oder vor dem 31. Dezember 2106, in einer eigenen Fibu Buch.-Blattzeile für jedes Sachkonto aggregiert. Transaktionen nach diesem Datum werden einzeln migriert.

## <a name="file-size-requirements"></a>Dateigrößen-Anforderungen
Die maximale Dateigröße, die Sie zu [!INCLUDE[d365fin](includes/d365fin_md.md)] hochladen können, ist 150 MB. Wenn die Datei, die Sie aus C5 exportieren, größer ist, erwägen Sie, Daten in mehreren Dateien zu migrieren. Beispielsweise exportieren Sie ein oder zwei Arten von Entitäten aus C5, beispielsweise Debitoren und Kreditoren, in eine Datei, und exportieren Sie dann Elemente in eine andere Datei usw. Sie können Dateien einzelnen in [!INCLUDE[d365fin](includes/d365fin_md.md)] importieren.

## <a name="to-migrate-data"></a>Um Daten zu migrieren
Es gibt nur einige wenige Schritte, um die Daten aus C5 zu exportieren und sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu importieren:  

1. In C5 verwenden Sie die Funktion **Datenbank exportieren**, um die Daten zu exportieren. Senden Sie dann den Exportordner an einen komprimierten (gezippten) Ordner.  
2. Wählen Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] die Option ![Glühbirne, die das Tell Me-Feature öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Datenmigration** ein und wählen Sie dann **Datenmigration**.  
3. Schliessen Sie die Schritte im unterstützten Setup ab. Stellen Sie sicher, dass Sie**Importieren aus Microsoft Dynamcis C5 2012** als die Datenquelle auswählen.  

## <a name="viewing-the-status-of-the-migration"></a>Zeigt den Status der Datenmigration an
Verwenden Sie die Seite **Datenmigrations-Übersicht**, um den Erfolg der Migration zu überwachen. Die Seite zeigt Informationen wie die Anzahl von Einheiten, die migriert wurde, den Status der Migration und die Anzahl von Artikeln an, die migriert wurden und ob sie erfolgreich war. Sie zeigt auch die Anzahl von Fehlern, Sie können überprüfen, was schief ging und macht es wenn möglich einfach, zur Einheit zu gehen und das Problem zu lösen. Weitere Informationen finden Sie im nächsten Abschnitt dieses Themas.  

> [!Note]
> Während Sie auf die Ergebnisse der Migration warten, müssen Sie die Seite aktualisieren, um die Ergebnisse anzuzeigen.

## <a name="how-to-avoid-double-posting"></a>Wie Sie Doppel-Buchung vermeiden
Um Doppelbuchungen in der Finanzbuchhaltung zu vermeiden, werden folgende Gegenkonten für offene Transaktionen verwendet:  

* Für Kreditoren verwenden wir das A-/P-Konto in der Kreditorenbuchungsgruppe.  
* Für Debitore verwenden wir das A-/P-Konto in der Debitorenbuchungsgruppe.  
* Für Artikel erstellen wir eine Buchungsmatrix, bei der im Korrekturkonto das Konto jenes ist, das als Lagerkonto in der Lagerbuchungseinrichtung angegeben ist.  

## <a name="correcting-errors"></a>Nachbesserung
Falls etwas schief geht und ein Fehler auftritt, wird das **Status** Feld **Abgeschlossen mit Fehlern** angezeigt und das Feld **Fehlerzahl** zeigt an, wie viele es sind. Um eine Liste der Fehler anzuzeigen, können Sie die Seite öffnen indem Sie **Datenmigrations-Fehler** auswählen:  

* Die Nummer im Feld **Fehlerzahl** für die Einheit.  
* Die Einheit und dann die Aktion **Fehler anzeigen**.  

Um auf der Seite **Datenmigrations-Fehler** einen Fehler zu korrigieren, können Sie eine Fehlermeldung auswählen, und dann **Datensatz bearbeiten** auswählen, um die Daten für die migrierte Einheit anzuzeigen. Wenn Sie mehrere Fehler beheben müssen, können Sie **Stapelfehlerkorrektur** auswählen, um auf die Einheiten in einer Liste zu bearbeiten. Sie müssen immer noch einzelne Datensätze öffnen, wenn der Fehler durch einen entsprechenden Posten verursacht wurde. Beispielsweise wird ein Kreditor nicht migriert, wenn die E-Mail-Adresse einer Kontaktperson ein ungültiges Format hat.

Nachdem Sie eines oder mehrere Fehler korrigiert haben, können Sie **Migrieren von** wählen, um nur die Einheiten zu migrieren, die Sie korrigierten, ohne die Migration vollständig erneut durchführen zu müssen.  

> [!Tip]
> Wenn Sie mehr als einen Fehler korrigiert haben, können Sie die Funktion **Weitere auswählen** verwenden, um mehrere Zeilen auszuwählen, um diese zu migrieren. Wenn es Fehler gibt, die nicht zur Korrektur wichtig sind, können Sie diese auswählen und dann **Auswahl überspringen** auswählen.

> [!Note]
> Wenn Sie Artikel haben, die in der Stückliste enthalten sind, müssen Sie diese mehrmals migrieren, wenn der ursprüngliche Artikel nicht vor den Varianten erstellt wird, auf die sie verweist. Wenn eine Artikelvariante zuerst erzeugt wird, kann die Referenz zum ursprünglichen Artikel eine Fehlermeldung verursachen.  

## <a name="verifying-data-after-migrating"></a>Prüfen von Daten nach dem Migrieren
Wenn Sie sicherstellen möchten, dass Ihre Daten ordnungsgemäß migriert werden, können Sie die nächste Seiten in C5 und in [!INCLUDE[d365fin](includes/d365fin_md.md)]anzeigen.

|Microsoft Dynamics C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]| Zu verwendender Batchauftrag |
|-----|-----|-----|
|Debitoreneinträge| Fibu Buch.-Blätter| CUSTMIGR |
|Kreditoreneinträge| Fibu Buch.-Blätter| VENDMIGR|
|Artikelposten| Artikel Buch.-Blätter| ITEMMIGR |
|Sachposten| Fibu Buch.-Blätter| GLACMIGR |

## <a name="stopping-data-migration"></a>Datenmigration anhalten
Sie können Datenmigration unterbrechen, indem Sie **Automatisches Beenden alle Migrationen** auswählen. Wenn Sie dies tun, werden alle offenen Migrationen beendet.

## <a name="see-also"></a>Siehe auch
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] über Erweiterungen](ui-extensions.md)  
[Erste Schritte](product-get-started.md)
