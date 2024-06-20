---
title: Gezieltes Einlagern und Kommissionieren festlegen
description: 'Gesteuertes Einlagern und Kommissionieren bietet Ihnen die Funktionalität, Ihr Lager effektiv zu führen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 11/07/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-items-and-locations-for-directed-put-away-and-pick"></a>Einrichten von Artikeln und Standorten für die gesteuerte Einlagerung und Kommissionierung

Wenn Sie einen Lagerort für die gesteuerte Einlagerung und Kommissionierung einrichten, steht Ihnen eine neue Funktionalität zur Verfügung, die Ihnen hilft, das Lager so effizient wie möglich zu betreiben. Um diese Funktionalität voll auszuschöpfen, liefern Sie der Anwendung zusätzliche Informationen zu den Artikeln, wodurch die Anwendung ihrerseits dabei unterstützt wird, die erforderlichen Berechnungen anzustellen, um die effizientesten und effektivsten Möglichkeiten zur Durchführung der Lageraktivitäten vorzuschlagen. 

## <a name="to-set-up-an-item-for-directed-put-away-and-pick"></a>So richten Sie einen Artikel für die gesteuerte Einlagerung und Kommissionierung ein:

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Artikel** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die Karte für den Artikel, den Sie für gesteuerte Einlagerung und Kommissionierung einrichten möchten.
3. Füllen Sie im Inforegister **Logistik** der Artikelkarte die Felder aus, um festzulegen, wie der Artikel im Lager verarbeitet werden soll.  
4. Wählen Sie die **Einheiten** Aktion aus.
5. Füllen Sie auf der Seite **Artikeleinheiten** die Einheiten aus, in denen der Artikel möglicherweise verarbeitet werden wird, indem Sie die Höhe, Breite, Länge, das Volumen und das Gewicht des Artikels angeben.
6. Wählen Sie die **Lagerplatzinhalte** Aktion aus.
7. Auf der Seite **Lagerplatzinhalte** können Sie den Lagerort und den Lagerplatz festlegen, mit denen der Artikel verknüpft sein soll. Das Feld **Vorgabewert** wird nicht verwendet, wenn der Lagerort für die gesteuerte Einlagerung und Kommissionierung eingerichtet wurde.  

## <a name="to-start-using-directed-put-away-and-pick"></a>So beginnen Sie mit der Verwendung von gezieltem Einlagern und Kommissionieren

Die gesteuerte Einlagerung und Kommissionierung verschafft Ihnen Zugang zu erweiterten Lagerkonfigurationsfunktionalitäten, die Ihre Effizienz und Datenzuverlässigkeit stark erhöhen können. Um diese Funktionalität nutzen zu können, müssen Sie zuerst eine Reihe von Parametern in Ihrem Lagerort einrichten.  

Um die gesteuerte Einlagerung und Kommissionierung zu nutzen, müssen Sie die Funktionalität auf der Lagerortkarte aktivieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie den Lagerort, bei dem Sie die gesteuerte Einlagerung und Kommissionierung nutzen möchten, wählen Sie dann die Aktion **Bearbeiten** aus.  
3. Wählen Sie im Inforegister **Lager** das Kontrollkästchen **Gesteuerte Einlag. u. Kommiss.**.  

Sie brauchen zu diesem Zeitpunkt der Einrichtung keine weiteren Felder auf der Lagerortkarte auszufüllen.  

> [!NOTE]  
> Sie können ein Lager nicht so einrichten, dass er Lagerplätze verwendet, wenn dieser Lagerort offene Artikelposten hat.  

Der nächste Schritt ist die Definition der Arten von Lagerplätzen, die Sie betreiben möchten. Weitere Informationen finden Sie unter [Einrichten von Lagerplatzarten](warehouse-how-to-set-up-bin-types.md). Die Lagerplatzart legt fest, wie ein bestimmter Lagerplatz im Warenfluss verwendet wird. Sie können sowohl einer Zone als auch einem Lagerplatz eine Lagerplatzart zuordnen.  

Sie können auch Lagerklassen definieren, wenn im Lager Artikel geführt werden, die bestimmte Lagerbedingungen benötigen. Lagerklassen werden verwendet, wenn der Einlagerung von Artikeln an Lagerplätzen vorgeschlagen wird. Sie weisen den Produktgruppen die Lagerklassen zu, die dann Artikeln und Lagerhaltungsdaten zugeordnet werden, oder auch Zonen und Lagerplätzen, die Lagerbedingungen bieten können, die von der Lagerklasse gefordert werden.  

Wenn Sie möchten, können Sie jetzt Zonen einrichten. Die Verwendung von Zonen reduziert die Anzahl der Felder, die Sie ausfüllen müssen, wenn Sie Ihre Lagerplätze einrichten, da Lagerplätze, die innerhalb einer Zone angelegt werden, einige Eigenschaften der Zone übernehmen. Zonen können es darüber hinaus neuen Mitarbeitern oder nur vorübergehend tätigen Mitarbeitern erleichtern, sich in Ihrem Lager zu orientieren. Beachten Sie, dass der Fluss nach Lagerplätzen gesteuert wird. Daher ist es möglich, mit Lagerplätzen und nur einer Zone zu arbeiten.  

## <a name="to-set-up-a-zone-in-your-warehouse"></a>So richten Sie eine Zone in Ihrem Lager ein:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie den Lagerort aus, in dem Sie die Zone einrichten möchten, öffnen Sie die Lagerortkarte, und wählen Sie dann die Aktion **Zonen** aus.  
3. Füllen Sie auf der Seite **Zonen** die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Wenn Sie einen Zonenparameter ändern, werden alle Lagerplätze, die von diesem Zeitpunkt an angelegt werden, die neuen Eigenschaften aufweisen.  

> [!NOTE]  
> Wenn Sie ohne Zonen arbeiten möchten, müssen Sie dennoch eine Zone erstellen, die außer für den Code undefiniert ist.  

Der nächste Schritt ist die Definition von Lagerplätzen. Weitere Informationen finden Sie unter [Vorgehensweise: Lagerorte für die Verwendung von Lagerplätzen einrichten](warehouse-how-to-set-up-locations-to-use-bins.md).  

Darüber hinaus müssen Sie Einlagerungsvorlagen und Inventurhäufigkeiten erstellen. Weitere Informationen finden Sie unter [Einrichten von Aktivitätvorlagen](warehouse-how-to-set-up-put-away-templates.md).  

## <a name="see-also"></a>Weitere Informationen

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
