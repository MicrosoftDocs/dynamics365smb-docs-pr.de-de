---
title: Automatisches Datenerfassungssystem (ADCS) verwenden
description: 'Erfahren Sie, wie Sie Ihr automatisches Datenerfassungssystem (ADCS) verwenden, um die Umlagerung von Artikeln im Lager zu registrieren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7700, 7703, 7704, 7706, 7707, 7710, 9813, 9814'
---
# Automatisches Datenerfassungssystem (ADCS) verwenden

> [!NOTE]
> Die ADCS-Lösung (Automated Data Capture System) ermöglicht [!INCLUDE[prod_short](includes/prod_short.md)] die Kommunikation mit mobilen Geräten über Webdienste. Sie müssen mit einem Microsoft-Partner zusammenarbeiten, der die Verbindung zwischen dem Webdienst und dem jeweiligen mobilenGerät herstellen kann. 

Sie verwenden die mobile Datenerfassung (MDE), um die Artikelbewegungen im Lager und die Aktivitäten im Buch.-Blatt zu erfassen, wie Mengenanpassungen im Logistik Artikel Buch.-Blatt und Inventuren. Bei ADCS wird normalerweise ein Strichcode gescannt.

Um MDE nutzen zu können, müssen Sie für jeden im Lager vorhandenen Artikel einen Artikelbezeichner angeben. Sie müssen außerdem Miniforms, Endgerätfunktionen, Datenaustausch einrichten und Einstellungen für Felder vornehmen, die MDE steuern. Sie legen fest, ob MDE auf der Lagerortkarte des Lagers verwendet wird.

Auf der Basis der Anforderungen Ihres Lagers legen Sie in der Miniform-Einrichtung die Informationen fest, die auf dem mobilen Gerät angezeigt werden. Die folgenden Beispiele zeigen Informationen, die Sie anzeigen können:  

- Daten aus Tabellen in [!INCLUDE[prod_short](includes/prod_short.md)], wie eine Liste der Kommissionierungsbelege, aus denen der Anwender auswählen kann.  
- Textinformation.  
- Nachrichten, die Bestätigungen oder Fehler für Aktivitäten anzeigen, die der Endgerätebenutzer ausgeführt und registriert hat.

## So aktivieren Sie Webdienste für ADCS

Um das automatisierte Datenerfassungssystem verwenden zu können, müssen Sie den ADCS-Webdienst aktivieren.  

## So aktivieren und veröffentlichen Sie den ADCS-Webdienst  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Webdienste** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu**.  
3. Geben Sie auf der Seite **Webdienste** die folgenden Informationen in eine neue Zeile ein:  

    |Feld|Wert|  
    |---------------------------------|-----------|  
    |**Objekttyp**|Codeunit|  
    |**Objekt-ID**|7714|  
    |**Dienstname**|ADCS **Wichtig**: Sie müssen **ADCS** als Namen für den Dienst festlegen.|  

4. Schalten Sie **Veröffentlicht** ein.  
5. Wählen Sie die Schaltfläche **OK**.  

## So richten Sie ein Lager für die Verwendung von MDE ein:  

Um MDE nutzen zu können, müssen Sie festlegen, welche Lagerorte die Technologie verwenden.  

> [!NOTE]  
> Es ist empfehlenswert, dass Sie ein Lager nicht für die Verwendung von MDE einrichten, wenn es auch eine Lagerplatzkapazitätsprüfung hat.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie den zugehörigen Link.
2. Wählen Sie das Lager aus, für das Sie MDE aktivieren möchten, und wählen die **Bearbeiten** Aktion aus.
3. Auf der Seite **Lagerortkarte** aktivieren Sie den Schalter **MDE verwenden**.  

## So geben Sie einen Artikel für die Verwendung von MDE an  

Jedem Logistik Artikel, den Sie mit MDE verwenden möchten, muss ein Barcode zugeordnet werden, um ihn mit der Artikelnummer zu verknüpfen. Beispielsweise können Sie den Barcode des Artikels als Identifzierungscode verwenden. Ein Artikel kann also mehrere Barcodes haben. Dies kann hilfreich sein, wenn ein Artikel in verschiedenen Einheiten verfügbar ist, wie als Stück und als Palette. In diesem Fall weisen Sie jeder Einheit einen Barcode zu.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Elemente** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie einen Artikel aus der Liste aus, der Teil der MDE-Lösung ist, und wählen die **Bearbeiten** Aktion aus.
3. Wählen Sie auf der Seite **Artikelkarte** die Aktion **Kennzeichner** aus.
4. Wählen Sie auf der Seite **Artikelbarcodes** die Aktion **Neu** aus.
5. Geben Sie im Feld **Code** die Kennzeichner für den Artikel an. Beispielsweise können Sie den Barcode des Artikels als Kennzeichner verwenden.  

    Sie können auch einen **Variantencode** und einen Code für die **Einheit** eingeben.  

6. Bei Bedarf können Sie mehrere Codes für jeden Artikel eingeben.
7. Wählen Sie die Schaltfläche **OK** aus.  
8. Um die Informationen zu prüfen, wählen Sie das Feld **Artikelbarcode** aus, um die Seite **Artikelbarcodes** zu öffnen.

## Um einen MDE-Benutzer hinzufügen  

Sie können beliebige Benutzer zu einem MDE hinzufügen. Wenn Sie das tun, muss der Benutzer ein Kennwort eingeben. Optional können Sie auch eine Verbindung angeben, die den MDE-Benutzer als Lagermitarbeiter identifiziert. Das MDE-Benutzerkennwort kann sich von ihrem Anmeldungskennwort unterscheiden. Weitere Informationen erhalten Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **ADCS-Benutzer** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**.  
3. Geben Sie im Feld **Namen** einen Namen für den Benutzer ein. Der Name darf einschließlich Leerzeichen maximal 20 Zeichen lang sein.  
4. Geben Sie im **Kennwort** Feld ein Kennwort ein.  

### So geben Sie an, dass ein Lagermitarbeiter ein MDE-Benutzer ist  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagermitarbeiter** ein, und wählen Sie dann den zugehörigen Link.  
2. Fügen Sie bei Bedarf einen neuen Lagermitarbeiter hinzu. Erfahren Sie mehr unter [Lagermitarbeiter einrichten](warehouse-how-to-set-up-warehouse-employees.md).  
3. Wählen Sie die Aktion **Liste bearbeiten** aus.  
4. Wählen Sie einen Lagermitarbeiter in der Liste aus. Wählen Sie im Feld **MDE-Benutzer** den Namen eines MDE-Benutzers aus der Liste aus.  

> [!NOTE]  
> Das standardmäßige Lager für den Mitarbeiter muss MDE verwenden.

## So erstellen und passen Sie Miniforms an

Mit Miniforms beschreiben Sie die Informationen, die Sie auf einem Endgerät präsentieren wollen. Beispielsweise können Sie Miniforms erstellen, um die Lageraktivität des Kommissionierens zu unterstützen. Nachdem Sie ein Miniform erstellt haben, können Sie Funktionen für häufige Aktionen hinzufügen, die ein Benutzer mit mobilen Geräten durchführt, wie eine Zeile nach oben oder unten verschieben.  

> [!NOTE]
> Um die Änderung einer Miniform-Funktion zu implementieren, müssen Sie eine neue Codeunit für das Feld **Codeunit verwalten** erstellen oder eine bestehende ändern, um die erforderliche Aktion oder die Antwort auszuführen. Weitere Informationen zur MDE-Funktionalität erhalten Sie, indem Sie folgende Codeeinheiten untersuchen.
>
> * 7705
> * 7706
> * 7712
> * 7713  

### Um ein Miniform für MDE zu erstellen  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Miniforms** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu**.  
3. In dem Feld **Code** geben Sie einen Code für die Miniform ein. Geben Sie optional in allen anderen Feldern Werte ein.  

    Aktivieren Sie den Schalter **Miniformular starten**, um anzugeben, dass das Miniform das erste Formular ist, das bei Anmeldung eines Benutzers verfügbar ist.  

4. Definieren Sie im Inforegister **Zeilen** die Felder, die im Miniform erscheinen. Die Reihenfolge, in der Sie Zeilen eingeben, ist die Reihenfolge, in der die Zeilen auf dem Endgerät angezeigt werden.  

Wenn Sie ein Miniform erstellt haben, sind die nächsten Schritte das Erstellen von Funktionen und das Zuordnen von Funktionalität zu verschiedenen Tastatureingaben.  

### Um Miniform-Funktionen anzupassen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Miniforms** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie ein Miniform aus der Liste, und wählen sie die Aktion **Bearbeiten** aus.  
3. Wählen Sie die Aktion **Funktionen** aus.  
4. Wählen Sie in der Dropdownliste **Funktionencode** einen Code aus, der für die Funktion steht, die Sie dem Miniform zuordnen möchten. Beispielsweise können Sie **ESC** auswählen, um die Funktion der Taste **ESC** zuzuweisen.  

## Weitere Informationen  

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]