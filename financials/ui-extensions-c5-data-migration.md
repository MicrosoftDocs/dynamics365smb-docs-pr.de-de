---
title: C5-Datenmigrations-Erweiterung verwenden | Microsoft Docs
description: Verwenden Sie diese Erweiterung, um Debitoren, Kreditoren, Artikel und Sachkonten von Microsoft Dynamics C5 2012 zu Financials zu migrieren.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 09/26/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 2d7d533662936116ffa40ded07b68e845fed810b
ms.contentlocale: de-de
ms.lasthandoff: 11/10/2017

---

# <a name="the-c5-data-migration-extension-for-dynamics-365-for-finance-and-operations-business-edition"></a>Die C5-Datenmigrations-Erweiterung für Dynamics 365 for Finance and Operations, Business Edition
Verwenden Sie diese Erweiterung, um Debitoren, Kreditoren, Artikel und Sachkonten von Microsoft Dynamics C5 2012 zu [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren.  
  
> [!Note] 
> Der Mandant darf in [!INCLUDE[d365fin](includes/d365fin_md.md)] keine Daten in enthalten. Nachdem Sie mit der Migration begonnen haben, erstellen Sie keine Debitoren, Kreditoren, Artikel oder Konten, bis die Migration beendet wurde.

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
[Willkommen bei [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  

