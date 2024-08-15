---
title: So arbeiten Sie mit Verantwortungszentren
description: 'Zuständigkeitseinheiten als Verwaltungszentren helfen Unternehmen, benutzerspezifische Ansichten von Einkaufs- und Kaufbelegen festzulegen, die sich ausschließlich auf das jeweilige Zentrum beziehen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.forms: '5714, 5715'
ms.date: 05/16/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="work-with-responsibility-centers"></a>Arbeiten mit Verantwortungseinheiten

Zuständigkeitseinheiten ermöglichen die Verwaltung von Verwaltungscentern. Eine Zuständigkeitseinheit kann ein Cost Center, ein Profit Center, ein Investment Center oder ein anderes unternehmensdefiniertes Verwaltungscenter sein. Beispiele von Zuständigkeitseinheiten können ein Verkaufsbüro, eine Einkaufsabteilung für mehrere Lagerorte und ein Fabrikplanungsbüro sein. Mithilfe dieser Funktionalität können Unternehmen beispielsweise benutzerspezifische Ansichten von Verkaufs- und Einkaufsdokumenten einrichten, die ausschließlich mit einem bestimmten Verwaltungscenter zusammenhängen.  

Die Verwendung mehrerer Lagerorte und Zuständigkeitseinheiten bietet Unternehmen mit mehreren Lagerorten die Möglichkeit, ihre Unternehmensabläufe äußerst flexibel und zugleich so optimal wie möglich zu verwalten.

Mehrere Standorte ermöglichen es Unternehmen, ihren Bestand an mehreren Standorten mithilfe einer Datenbank zu verwalten. Zwei Konzepte, Lagerorte und Lagerhaltungsdaten, bilden die Eckpfeiler dieses Elements. Ein Lagerort ist definiert als ein Ort, der die physische Platzierung von Artikeln sowie Artikelmengen verwaltet. Der Begriff ist weit genug gefasst, um auch Standorte wie Fabriken oder Produktionsanlagen sowie Vertriebszentren, Lager, Ausstellungsräume und Servicefahrzeuge einzuschließen. Lagerhaltungsdaten sind definiert als ein Artikel an einem bestimmten Lagerort und/oder als Variante. Mithilfe von Lagerhaltungsdaten können Unternehmen mit mehreren Standorten Beschaffungsdaten, Adressen sowie einige Finanzbuchungsdaten auf Standortebene hinzuzufügen. Dadurch können sie Varianten desselben Artikels für jeden Standort auffüllen und Artikel auf Grundlage standortspezifischer Nachschubinformationen bestellen.  

## <a name="to-set-up-a-responsibility-center"></a>Zuständigkeitseinheiten einrichten

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Zuständigkeitseinheiten** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**.  
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Wenn Sie den Mandanten mithilfe von Zuständigkeitseinheiten verwalten, empfiehlt es sich möglicherweise, eine standardmäßige Zuständigkeitseinheit für den Mandanten einzurichten.
4. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Unternehmensdaten** ein, und wählen Sie dann den zugehörigen Link.
5. Geben Sie auf der Registerkarte  **Versand**  im Feld  **Verantwortungszentrum**  einen Verantwortungszentrumcode ein.

Dieser Code wird auf Einkaufs- und Verkaufsbelegen oder Servicedokumenten verwendet werden, wenn der Anwender, Debitor oder Kreditor keine Vorgabe Zuständigkeitseinheit hat. Auf allen möglichen Verkaufs- oder Einkaufs-Dokumenten können Sie eine andere als der Vorgabe Zuständigkeitseinheit eingeben.

> [!NOTE]  
> Wenn Sie einen Zuständigkeitseinheitencode in einem Beleg angeben, beeinflusst er die Adresse, Dimensionen und Preise im Beleg.  

## <a name="to-assign-responsibility-centers-to-users"></a>Zuständigkeitseinheiten für Benutzer zuweisen:

Sie können die Benutzer so einrichten, dass [!INCLUDE [prod_short](includes/prod_short.md)] nur die entsprechenden Belege für ihre speziellen Arbeitsbereiche anzeigt. Benutzer sind einem Verantwortungszentrum zugeordnet und arbeiten nur mit Dokumenten, die sich auf bestimmte Anwendungsbereiche dieses Zentrums beziehen.  

Um dies einzurichten, weisen Sie Benutzern Zuständigkeitseinheiten in drei Basisfunktionsbereichen zu: Kreditoren, Einkauf und Servicemanagement.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Benutzereinrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie im Fenster **Benutzer einrichten** den Benutzer, dem Sie eine Zuständigkeitseinheit zuweisen wollen. Wenn sich der Benutzer nicht in der Übersicht befindet, müssen Sie eine Benutzer-ID im Feld **Benutzer-ID** eingeben.  
3. Im Feld **Verk.-Zuständigk.-Einh. Filter** geben Sie die Zuständigkeitseinheit ein, in der der Benutzer Aufgaben haben wird, die mit dem Verkauf verbunden sind.  
4. Im Feld **Eink.-Zuständigk.-Einh. Filter** geben Sie die Zuständigkeitseinheit ein, in der der Benutzer Aufgaben haben wird, die mit dem Einkauf verknüpft sind.  
5. Im Feld **Serv.-Zuständigk.-Einh. Filter** geben Sie die Zuständigkeitseinheit ein, in der der Benutzer Aufgaben haben wird, die mit Serviceverwaltung verknüpft sind.  

> [!NOTE]  
> Benutzer können nur die gebuchten Belege anzeigen, die sich auf ihr eigenes Verantwortungszentrum beziehen. Sie können jedoch alle Ledger-Einträge anzeigen und aus den Ledger-Einträgen zu anderen gebuchten Belegen navigieren.

## <a name="see-also"></a>Siehe auch

[Einrichten des Inventars](inventory-setup-inventory.md)    
[Warehouse Management einrichten](warehouse-setup-warehouse.md)    
[Lagerbest](inventory-manage-inventory.md)    
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    
[Definieren Sie eine Rechnungsbuchungsrichtlinie für Benutzer](admin-setup-invoice-posting-policy.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
