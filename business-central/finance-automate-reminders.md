---
title: Mahnungen im Inkasso automatisieren
description: 'Sparen Sie beim Inkasso Zeit, indem Sie die Prozesse zum Erstellen, Ausstellen und Senden von Mahnungen an Debitoren automatisieren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'collection, remindes'
ms.search.form: null
ms.date: 03/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Mahnungen im Inkasso automatisieren

Machen Sie Ihr Inkasso effektiver,, indem Sie den Prozess zum Erstellen, Ausstellen und Senden von Mahnungen an Ihre Debitoren automatisieren. Durch die Automatisierung können Sie den Zeitaufwand für das Inkasso erheblich reduzieren, einen besseren Überblick über den Prozess gewinnen und die volle Kontrolle über jeden Schritt erlangen.

Legen Sie auf der Seite **Mahnungsautomatisierung** die einzelnen Aktionen (Schritte) fest. Sie können die Schritte zum Erstellen, Ausstellen und Senden von Mahnungen kombinieren oder für jeden Schritt eine separate Automatisierung erstellen, wenn dies für Ihre Inkassoprozesse besser ist. Automatisierungen basieren auf den Mahnmethoden und -stufen. Weitere Informationen finden Sie unter [Mahnmethoden und Mahnstufen einrichten](finance-setup-reminders.md). Sie können Filter für Mahnmethoden für eine Automatisierung als Ganzes und Filter für jede Aktion in der Automatisierung festlegen. Sie können offene Rechnungen auch als PDF-Datei an E-Mails anhängen.

Die Automatisierung erfolgt über einen Eintrag in einer Aufgabenwarteschlange. Wenn Sie eine Automatisierung einrichten, verwenden Sie das Feld **Rhythmus**, um anzugeben, wie und wann sie ausgeführt wird. Wenn Sie **Manuell** wählen, wird die Automatisierung einmal ausgeführt, wenn Sie die Aktion **Starten** verwenden. Sie können auch **Wöchentlich**, **Monatlich** oder **Benutzerdefiniert** auswählen, um einen detaillierteren Rhythmus einzurichten. Wenn Sie **Benutzerdefiniert** wählen, müssen Sie eine Datumsformel eingeben. Weitere Informationen zum Eingeben einer Datumsformel finden Sie unter [Datumsformeln verwenden](ui-enter-date-ranges.md#use-date-formulas). Wenn Sie eine andere Option als **Manuell** wählen, wird die Automatisierung ausgeführt, bis Sie sie anhalten. Wenn Sie den Ausführungszeitpunkt noch genauer festlegen möchten, öffnen Sie mit der Aktion **Aufgabenwarteschlangeneinträge** die Seite **Aufgabenwarteschlangeneinträge** und ändern Sie die Wiederholung, zum Beispiel auf täglich oder einen bestimmten Wochentag.

## Den Mahnungsablauf automatisieren

Die folgenden Abschnitte beschreiben, wie Sie Mahnungen so einrichten, dass sie automatisch erstellt, ausgestellt und gesendet werden.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") geben Sie **Mahnungsautomatisierung** ein und wählen Sie dann den entsprechenden Link.
1. Wählen Sie **Neu** aus, und füllen Sie dann die Felder im Inforegister **Allgemein** aus.
1. Wählen Sie im Feld **Mahnungsmethodenfilter** die Mahnungsmethoden aus, für die diese Automatisierung verwendet werden sollen.
1. Wählen Sie im Feld **Rhythmus** aus, wie oft die Automatisierung ausgeführt wird.
1. Wählen Sie im Inforegister **Aktionen** die Option **Neu** und dann aus, ob die Automatisierung Mahnungen erstellt, ausstellt oder sendet. Wählen Sie **OK** aus.
1. Füllen Sie je nach Art der Aktion, die die Automatisierung ausführt, die Felder auf der Einrichtungsseite aus. Weitere Informationen zu den Einstellungen finden Sie unter [Einstellungen für Mahnungsaktionen](#settings-for-reminder-actions).
1. Nachdem Sie die Aktionen für die Automatisierung eingerichtet haben, können Sie die Reihenfolge, in der sie ausgeführt werden, über **Nach oben** und **Nach unten** anpassen.

## Einstellungen für Mahnungsaktionen

Die Einrichtungseinstellungen sind für die Aktionen „Erstellen“, „Ausstellen“ und „Senden“ einer Mahnung unterschiedlich. Die folgenden Abschnitte beschreiben, wie Sie sie nutzen.

### Erstellen

* Legen Sie die höchste Stufe auf allen Mahnungszeilen fest.  
* Erstellen Sie Mahnungen für Einträge mit dem Status „Gesperrt“. Diese Einstellung ist beispielsweise nützlich, wenn Sie eine laufende Auseinandersetzung mit einem Debitor haben und möchten, dass er den Gesamtzusammenhang sieht.
* Erstellen Sie Mahnungen für alle unbezahlten Rechnungen, nicht nur für überfällige. Der Bericht zeigt in separaten Abschnitten überfällige Rechnungen und solche, die noch nicht bezahlt, aber nicht überfällig sind.
* Legen Sie Filter fest, um die Mahnung spezifischer zu gestalten.

### Ausstellen

Wenn Sie eine Mahnung ausstellen, erstellen Sie einen Debitorenposten, der das Buchungsdatum und das Steuerdatum enthalten. Verwenden Sie die Einstellungen auf der Seite **Mahnungen ausstellen – Einrichtung**, um anzugeben, ob die Informationen auf der ausgestellten Mahnung durch die Informationen auf der erstellten Mahnung ersetzt werden sollen. Wenn Sie die Mahnung beispielsweise gestern erstellt haben und sie heute ausstellen, verschiebt sich das Fälligkeitsdatum um einen Tag.

### Senden

> [!NOTE]
> Für die Sendeautomatisierung müssen Sie in [!INCLUDE [prod_short](includes/prod_short.md)] E-Mails eingerichtet haben. Weitere Informationen zum Einrichten von E-Mail finden Sie unter [E-Mail einrichten](admin-how-setup-email.md).

Der Inhalt der E-Mails, wie Anhangstexte, E-Mail-Texte und Sprache, ergibt sich aus der Einrichtung der Mahnungsmethode. Weitere Informationen zu E-Mail-Einstellungen finden Sie unter [Mahnmethoden und Mahnstufen einrichten](finance-setup-reminders.md).

Verwenden Sie die Einstellungen auf der Seite **Mahnungen senden – Einrichtung**, um Folgendes zu steuern:

* Allgemeine Einstellungen, z. B. die Beschreibung und wie oft Sie dieselbe Mahnung senden.
* Einstellungen für den Inhalt der Mahnung.
* Einstellungen zum Nachverfolgen der von Ihnen versendeten Mahnungen durch das Erstellen von Interaktionen, ob Sie die Mahnung ausdrucken oder per E-Mail versenden und ob Sie nur überfällige Rechnungen, alle Rechnungen oder keine Rechnungen anhängen möchten. 

## Auf den Verlauf einer Mahnung zugreifen

[!INCLUDE [prod_short](includes/prod_short.md)] behält im Auge, wann eine Automatisierung jeweils ausgeführt wird. Sie können auf den Verlauf zugreifen, indem Sie die Aktion **Protokollposten** auswählen. Sie können auch die Aktion **Ausgestellte Mahnungen** verwenden, um auf eine Liste Ihrer Mahnungen zuzugreifen.

## Umgang mit Fehlern

Auf dem Inforegister **Aktionen** können Sie für jede Aktion angeben, ob die Automatisierung gestoppt werden soll, wenn die Aktion einen Fehler aufweist. Wenn Sie dies tun, verarbeitet die Automatisierung die darauffolgenden Aktionen nicht. Um dieses Feature ein- oder auszuschalten, verwenden Sie die Aktion **Stopp bei Fehler festlegen** oder **Stopp bei Fehler löschen**.

## Aktionseinstellungen für eine Automatisierung ändern

Sie können die Einstellungen für eine Automatisierung jederzeit ändern. Wählen Sie auf dem Inforegister **Aktionen** **Einrichtung** und nehmen Sie dann Ihre Änderungen vor.

## Siehe auch

[Mahnmethoden und Mahnstufen einrichten](finance-setup-reminders.md)  
[Mahnungen für Restbeträge versenden](receivables-send-reminders.md)  
