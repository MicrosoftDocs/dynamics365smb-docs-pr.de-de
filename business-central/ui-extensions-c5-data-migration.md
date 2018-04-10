---
title: C5-Datenmigrations-Erweiterung verwenden | Microsoft Docs
description: Verwenden Sie diese Erweiterung, um Debitoren, Kreditoren, Artikel und Sachkonten von Microsoft Dynamics C5 2012 zu Financials zu migrieren.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 7fe6393ad43dbad032512b2d6d45cc8ee0392236
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a>Die C5 Datenmigrations-Erweiterung für Business Central
Verwenden Sie diese Erweiterung, um Debitoren, Kreditoren, Artikel und Sachkonten von Microsoft Dynamics C5 2012 zu [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren. Sie können historische Posten für Sachkonten auch migrieren.

> [!Note]
> Der Mandant darf in [!INCLUDE[d365fin](includes/d365fin_md.md)] keine Daten in enthalten. Nachdem Sie mit der Migration begonnen haben, erstellen Sie keine Debitoren, Kreditoren, Artikel oder Konten, bis die Migration beendet wurde.

##<a name="what-data-is-migrated"></a>Welche Daten migriert?
Die folgenden Daten werden für jede Einheit migriert:

**Debitoren**
* Ort
* Land
* Kunden-Dimensionen (Abteilung, Kostenträger, Kostenstelle)
* Lieferbedingungsmethode
* Vertriebsmitarbeiter
* Zahlungsbedingungen
* Zahlungsform
* Debitorenpreisgruppe
* Debitorenrechnungsrabatt

Wenn Sie Konten migrieren, werden auch die folgenden Daten migriert:

* Debitorenbuchungsgruppe
* Fibu Buch.-Blattname
* Migrieren Sie offene Debitorenposten (Kundenbucheinträge)

**Kreditoren**
* Ort
* Land
* Kunden-Dimensionen (Abteilung, Kostenträger, Kostenstelle)
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

Wenn Sie Konten migrieren, werden auch die folgenden Daten migriert:

* Lagerbuchungseinrichtung
* Buchungsmatrix Einrichtung
* Artikel Buch.-Blattname
* Öffnen Sie das Fenster Transaktionen (Artikel Kreditorenposten)

> [!Note]
> Wenn es offene Transaktionen gibt, die Fremdwährungen verwenden, werden die Wechselkurse für alle Währungen auch migriert. Andere Wechselkurse werden nicht migriert.

## <a name="to-migrate-data"></a>Um Daten zu migrieren
Es gibt nur einige wenige Schritte, um die Daten aus C5 zu exportieren und sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu importieren:  

1. In C5 verwenden Sie die Funktion **Datenbank exportieren**, um die Daten zu exportieren. Senden Sie dann den Exportordner an einen komprimierten (gezippten) Ordner.  
2. Wählen Sie dann in [!INCLUDE[d365fin](includes/d365fin_md.md)] das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben Sie **Datenmigration** ein und wählen dann **Datenmigration**.  
3. Schliessen Sie die Schritte im unterstützten Setup ab. Stellen Sie sicher, dass Sie**Importieren aus Microsoft Dynamcis C5 2012** als die Datenquelle auswählen.  

> [!Note]
> Mandanten fügen häufig Felder hinzu, um C5 für ihren jeweiligen Geschäftsbereich anzupassen. [!INCLUDE[d365fin](includes/d365fin_md.md)] migriert nicht Daten vom benutzerdefinierten Feldern. Die Migration schlägt fehl, wenn Sie mehr als 10 benutzerdefinierte Felder haben.

## <a name="viewing-the-status-of-the-migration"></a>Zeigt den Status der Datenmigration an
Verwenden Sie die Seite **Datenmigrations-Übersicht**, um den Erfolg der Migration zu überwachen. Die Seite zeigt Informationen wie die Anzahl von Einheiten, die migriert wurde, den Status der Migration und die Anzahl von Artikeln an, die migriert wurden und ob sie erfolgreich war. Sie zeigt auch die Anzahl von Fehlern, Sie können überprüfen, was schief ging und macht es wenn möglich einfach, zur Einheit zu gehen und das Problem zu lösen. Weitere Informationen finden Sie im nächsten Abschnitt dieses Themas.  

> [!Note]
> Während Sie auf die Ergebnisse der Migration warten, müssen Sie die Seite aktualisieren, um die Ergebnisse anzuzeigen.

## <a name="correcting-errors"></a>Nachbesserung
Falls etwas schief geht und ein Fehler auftritt, wird das **Status** Feld **Abgeschlossen mit Fehlern** angezeigt und das Feld **Fehlerzahl** zeigt an, wie viele es sind. Um eine Liste der Fehler anzuzeigen, können Sie die Seite öffnen indem Sie **Datenmigrations-Fehler** auswählen:  

* Die Nummer im Feld **Fehlerzahl** für die Einheit.  
* Die Einheit und dann die Aktion **Fehler anzeigen**.  

Um auf der Seite **Datenmigrations-Fehler** einen Fehler zu korrigieren, können Sie eine Fehlermeldung auswählen, und dann **Datensatz bearbeiten** auswählen, um die Seite zu öffnen, welche de Daten für die migrierte Einheit enthält. Nachdem Sie eines oder mehrere Fehler korrigiert haben, können Sie **Migrieren von** wählen, um nur die Einheiten zu migrieren, die Sie korrigierten, ohne die Migration vollständig erneut durchführen zu müssen.  

> [!Tip]
> Wenn Sie mehr als einen Fehler korrigiert haben, können Sie die Funktion **Weitere auswählen** verwenden, um mehrere Zeilen auszuwählen, um diese zu migrieren. Wenn es Fehler gibt, die nicht zur Korrektur wichtig sind, können Sie diese auswählen und dann **Auswahl überspringen** auswählen.

> [!Note]
> Wenn Sie Artikel haben, die in der Stückliste enthalten sind, müssen Sie diese mehrmals migrieren, wenn der ursprüngliche Artikel nicht vor den Varianten erstellt wird, auf die sie verweist. Wenn eine Artikelvariante zuerst erzeugt wird, kann die Referenz zum ursprünglichen Artikel eine Fehlermeldung verursachen.  

## <a name="verifying-data-after-migrating"></a>Prüfen von Daten nach dem Migrieren
Wenn Sie sicherstellen möchten, dass Ihre Daten ordnungsgemäß migriert werden, können Sie die nächste Seiten in C5 und in [!INCLUDE[d365fin](includes/d365fin_md.md)]anzeigen.

|Microsoft Dynamics C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|Debitoreneinträge| Fibu Buch.-Blätter|
|Kreditoreneinträge| Fibu Buch.-Blätter|
|Artikelposten| Artikel Buch.-Blätter|

In [!INCLUDE[d365fin](includes/d365fin_md.md)], wird der Stapel für die migrierten Daten **C5MIGRATE** genannt.

## <a name="stopping-data-migration"></a>Datenmigration anhalten
Sie können Datenmigration unterbrechen, indem Sie **Automatisches Beenden alle Migrationen** auswählen. Wenn Sie dies tun, werden alle offenen Migrationen beendet.

## <a name="see-also"></a>Siehe auch
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  
[Erste Schritte](product-get-started.md) 

