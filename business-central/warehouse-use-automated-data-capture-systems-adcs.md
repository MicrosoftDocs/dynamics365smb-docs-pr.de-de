---
title: Automatisierte Datenerfassung (MDE) verwenden | Microsoft Docs
description: Sie verwenden die mobile Datenerfassung (MDE), um die Artikelbewegungen im Lager und die Aktivitäten im Buch.-Blatt zu erfassen, wie Mengenanpassungen im Logistik Artikel Buch.-Blatt und Inventuren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: barcode
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5fe40d26a9128b9f689c5ec4502af929d0af04c2
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925347"
---
# <a name="use-automated-data-capture-systems-adcs"></a>Automatisierte Datenerfassung (MDE) verwenden

> [!NOTE]
> Die ADCS-Lösung (Automated Data Capture System) ermöglicht [!INCLUDE[d365fin](includes/d365fin_md.md)] die Kommunikation mit mobilen Geräten über Webdienste. Sie müssen mit einem Microsoft-Partner zusammenarbeiten, der die Verbindung zwischen dem Webdienst und dem jeweiligen mobilenGerät herstellen kann. 

Sie verwenden die mobile Datenerfassung (MDE), um die Artikelbewegungen im Lager und die Aktivitäten im Buch.-Blatt zu erfassen, wie Mengenanpassungen im Logistik Artikel Buch.-Blatt und Inventuren. Bei ADCS wird normalerweise ein Strichcode gescannt.

Um MDE nutzen zu können, müssen Sie für jeden im Lager vorhandenen Artikel einen Artikelbezeichner angeben. Sie müssen außerdem Miniforms, Endgerätfunktionen, Datenaustausch einrichten und Einstellungen für Felder vornehmen, die MDE steuern. Sie legen fest, ob MDE auf der Lagerortkarte des Lagers verwendet wird.

Auf der Basis der Anforderungen Ihres Lagers legen Sie in der Miniform-Einrichtung die Informationen fest, die auf dem mobilen Gerät angezeigt werden. Die folgenden Beispiele zeigen Informationen, die Sie anzeigen können:  

- Daten aus Tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)], wie eine Liste der Kommissionierungsbelege, aus denen der Anwender auswählen kann.  
- Textinformation.  
- Nachrichten, die Bestätigungen oder Fehler für Aktivitäten anzeigen, die der Endgerätebenutzer ausgeführt und registriert hat.

## <a name="to-enable-web-services-for-adcs"></a>So aktivieren Sie Webdienste für ADCS
Um das automatisierte Datenerfassungssystem verwenden zu können, müssen Sie den ADCS-Webdienst aktivieren.  

## <a name="to-enable-and-publish-the-adcs-web-service"></a>So aktivieren und veröffentlichen Sie den ADCS-Webdienst  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Webdienste** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu**.  
3. Geben Sie auf der Seite **Webdienste** die folgenden Informationen in eine neue Zeile ein:  

    |Feld|Wert|  
    |---------------------------------|-----------|  
    |**Objekttyp**|Codeunit|  
    |**Objekt-ID**|7714|  
    |**Dienstname**|ADCS **Wichtig**: Sie müssen **ADCS** als Namen für den Dienst festlegen.|  

5. Aktivieren Sie das Kontrollkästchen **Veröffentlicht**.  
6. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="to-set-up-a-warehouse-to-use-adcs"></a>So richten Sie ein Lager für die Verwendung von MDE ein:  
Um MDE nutzen zu können, müssen Sie festlegen, welche Lagerorte die Technologie verwenden.  

> [!NOTE]  
>  Es ist empfehlenswert, dass Sie ein Lager nicht für die Verwendung von MDE einrichten, wenn das Lager auch eine Lagerplatzkapazitätsprüfung hat.

1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Lagerorte** ein und wählen Sie den entsprechenden Link.
2.  Wählen Sie ein Lager aus der Liste aus, für das Sie MDE aktivieren möchten, und wählen die **Bearbeiten** Aktion aus.
3. Auf der Seite **Lagerortkarte** wählen Sie das Kontrollkästchen **MDE verwenden** aus.  

## <a name="to-specify-an-item-to-use-adcs"></a>So geben Sie einen Artikel für die Verwendung von MDE an  
Jedem Logistik Artikel, den Sie mit MDE verwenden möchten, muss ein Barcode zugeordnet werden, um ihn mit der Artikelnummer zu verknüpfen. Beispielsweise können Sie den Barcode des Artikels als Identifzierungscode verwenden. Ein Artikel kann also mehrere Barcodes haben. Dies kann hilfreich sein, wenn ein Artikel in verschiedenen Maßeinheiten verfügbar ist, wie als Stück und als Palette. In diesem Fall weisen Sie jeder Einheit einen Barcode zu.    

1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie einen Artikel aus der Liste aus, der Teil der MDE-Lösung ist, und wählen die **Bearbeiten** Aktion aus.
3. Wählen Sie auf der Seite **Artikelkarte** die Aktion **Kennzeichner** aus.
4. Wählen Sie auf der Seite **Artikelbarcodes** die Aktion **Neu** aus.
5. Geben Sie im Feld **Code** die Kennzeichner für den Artikel an. Beispielsweise können Sie den Barcode des Artikels als Kennzeichner verwenden.  

    Sie können auch einen **Variantencode** und einen Code für die **Einheit** eingeben.  

6. Bei Bedarf können Sie mehrere Codes für jeden Artikel eingeben.
7. Wählen Sie die Schaltfläche **OK** aus.  
8.  Um die Informationen zu prüfen, wählen Sie das Feld **Artikelbarcode** aus, um die Seite **Artikelbarcodes** zu öffnen.

## <a name="to-add-an-adcs-user"></a>Um einen MDE-Benutzer hinzufügen  
Sie können einen beliebigen Benutzer als Benutzer eines automatisierten Datenerfassungssystems hinzufügen (ADCS). Wenn Sie dies tun, muss der Benutzer außerdem ein Kennwort eingeben. Optional können Sie auch eine Verbindung angeben, die den MDE-Benutzer als Lagermitarbeiter identifiziert. Das MDE-Benutzerkennwort kann sich vom Windows-Anmeldungskennwort des Benutzers unterscheiden. Weitere Informationen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).

1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **ADCS Benutzer** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**.  
3.  Geben Sie im Feld **Namen** einen Namen für den Benutzer ein. Der Name darf einschließlich Leerzeichen maximal 20 Zeichen lang sein.  
4.  Geben Sie im **Kennwort** Feld ein Kennwort ein. Das Kennwort wird maskiert.  

### <a name="to-specify-that-a-warehouse-employee-is-an-adcs-user"></a>So geben Sie an, dass ein Lagermitarbeiter ein MDE-Benutzer ist  
1.  Wählen Sie die ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Lagerort-Mitarbeiter** ein und wählen Sie dann den entsprechenden Link.  
2.  Fügen Sie bei Bedarf einen neuen Lagermitarbeiter hinzu. Weitere Informationen finden Sie unter [Lagermitarbeiter einrichten](warehouse-how-to-set-up-warehouse-employees.md)  
3.  Wählen Sie die Aktion **Liste bearbeiten** aus.  
4.  Wählen Sie einen Lagermitarbeiter in der Liste aus. Klicken Sie im Feld **MDE-Benutzer** auf den Dropdownpfeil, und wählen Sie den Namen eines MDE-Benutzers in der Liste aus.  

> [!NOTE]  
>  Das standardmäßige Lager für den Mitarbeiter muss MDE verwenden.

## <a name="to-create-and-customize-miniforms"></a>So erstellen und passen Sie Miniforms an
Mit Miniforms beschreiben Sie die Informationen, die Sie auf einem Endgerät präsentieren wollen. Beispielsweise können Sie Miniforms erstellen, um die Lageraktivität des Kommissionierens zu unterstützen. Nachdem Sie ein Miniform erstellt haben, können Sie Funktionen für häufige Aktionen hinzufügen, die ein Benutzer mit mobilen Geräten durchführt, wie eine Zeile nach oben oder unten verschieben.  

> [!NOTE] 
> Um die Änderung einer Miniform-Funktion zu implementieren, müssen Sie eine neue Codeunit für das Feld **Codeunit verwalten** erstellen oder eine bestehende ändern, um die erforderliche Aktion oder die Antwort auszuführen. Weitere Informationen zur ADCS-Funktionalität erhalten Sie, indem Sie Codeeinheiten wie 7705, 7706, 7712 und 7713 untersuchen.  

### <a name="to-create-a-miniform-for-adcs"></a>Um ein Miniform für MDE zu erstellen  
1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Miniformulare** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**.  
3.  In dem Feld **Code** geben Sie einen Code für die Miniform ein. Geben Sie optional in allen anderen Feldern Werte ein.  

    Aktivieren Sie das Kontrollkästchen **Miniformular starten**, um anzugeben, dass das Miniform das erste Formular ist, das der Benutzer bei der Anmeldung sieht.  

4.  Definieren Sie im Inforegister **Zeilen** die Felder, die im Miniform erscheinen. Die Reihenfolge, in der Sie Zeilen eingeben, ist die Reihenfolge, in der die Zeilen auf dem Endgerät angezeigt werden.  

Wenn Sie ein Miniform erstellt haben, sind die nächsten Schritte das Erstellen von Funktionen und das Zuordnen von Funktionalität zu verschiedenen Tastatureingaben.  

### <a name="to-customize-miniform-functions"></a>Um Miniform-Funktionen anzupassen  
1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Miniformulare** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie ein Miniform aus der Liste, und wählen sie die Aktion **Bearbeiten** aus.  
3.  Wählen Sie die Aktion **Funktionen** aus.  
4.  Wählen Sie in der Dropdownliste **Funktionencode** einen Code aus, der für die Funktion steht, die Sie dem Miniform zuordnen möchten. Beispielsweise können Sie ESC auswählen, was die Funktion des Drückens der Taste ESC zuordnet.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
