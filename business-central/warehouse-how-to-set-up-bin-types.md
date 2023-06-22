---
title: Lagerplatzarten einrichten
description: 'Weisen Sie den Lagerplätzen Typen und grundlegende Flow-Aktivitäten zu und definieren Sie damit die Art und Weise, wie die Lagerplätze für bestimmte Lageraktivitäten verwendet werden.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7367
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="set-up-bin-types" />Lagerplatzarten einrichten

Sie können den Warenfluss durch die Lagerplätze steuern, die Sie für bestimmte Logistikaktivitäten definiert haben. Sie weisen jedem Lagerplatz eine Lagerplatzart zu und ordnen dadurch dem Lagerplatz seine grundlegenden Warenflussaktivitäten zu, und definieren hiermit auf welche ein Lagerplatz verwendet wird.  

Es gibt sechs Arten. Sie können Ihr Lager mit allen möglichen sechs Lagerplatzarten betreiben oder Sie entscheiden sich, nur die Lagerplatzarten EING, EINLAGKOMM, AUSG und QK zu verwenden. Diese vier Lagerplatzarten ermöglichen der Anwendung, Vorschläge zu machen, um den Warenfluss zu unterstützen, und sie geben Ihnen die Möglichkeit, Abweichungen im Lagerbestand zu erfassen.  

## <a name="to-set-up-the-bin-types-you-want-to-use" />So richten die Lagerplatzarten ein, die Sie verwenden möchten:

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagerplatzarten** ein und wählen Sie dann den zugehörigen Link.  
2.  Erzeugen Sie auf der Seite **Lagerplatzarten** einen Code mit 10 Zeichen für eine Lagerplatzart.  
3.  Wählen Sie die Aktivitäten aus, die mit den einzelnen Lagerplatzarten durchgeführt werden können.  

> [!NOTE]  
>  Lagerplatzarten können nur angewandt werden, wenn Sie die gesteuerte Einlagerung und Kommissionierung für Ihren Lagerort verwenden.  

Die Lagerplatzart legt fest, wie ein bestimmter Lagerplatz im Warenfluss verwendet wird. Sie können die Vorschläge für alle Logistikbelege immer überschreiben und Sie können Artikel mithilfe von Umlagerungen aus Lagerplätzen aus- und in Lagerplätze einlagern.  

Die Lagerplatzarten, die Sie erzeugen können, werden weiter unten aufgelistet.  

|Lagerplatzart|Description|  
|------------------|---------------------------------------|  
|EING|Die Artikel werden als gebuchte Wareneingänge registriert, die noch nicht eingelagert wurden.|  
|AUSG|Die Artikel wurden für Warenausgangszeilen kommissioniert, der Warenausgang wurde jedoch noch nicht gebucht.|  
|EINLAG|Normalerweise werden hier Artikel in großen Einheiten eingelagert, die jedoch nicht für die Kommissionierung verwendet werden soll. Da die Lagerplätze nicht zum kommissionieren verwendet werden, weder für Fertigungsaufträge noch für Warenausgänge, kann Ihre Nutzung von Lagerplätzen der Art "Einlagerung" begrenzt sein, diese Lagerplatzart kann jedoch sinnvoll sein, wenn Sie eine große Menge an Artikeln eingekauft haben. Lagerplätze dieser Art sollten immer eine niedrige Lagerplatzpriorität haben, so dass beim Einlagern von angenommenen Artikeln diese zuerst in die Lagerplätze der Art EINLAGKOMM mit höherer Priorität einlagert werden, die als Standard für diesen Artikel definiert wurden. Wenn Sie diese Art von Lagerplatz nutzen, müssen Sie regelmäßig eine Lagerplatzauffüllung durchführen, so dass die Artikel, die in diesen Lagerplätzen gelagert werden, auch in Lagerplätzen der Art EINLAGKOMM oder KOMMISS verfügbar sind.|  
|KOMMISS|Artikel, die nur zur Kommissionierung verwendet werden, z. B. Artikel, die demnächst Ihr Ablaufdatum erreichen, die Sie in diese Art von Lagerplatz eingelagert haben. Dieser Art von Lagerplätzen sollten Sie eine hohe Priorität zuordnen, so dass sie zuerst für eine Kommissionierung vorgeschlagen werden.|  
|EINLAGKOMM|Artikel an Lagerplätzen, die für Einlagerungs- und Kommissionierungsfunktionen vorgeschlagen werden. Lagerplätze dieser Art haben wahrscheinlich unterschiedliche Lagerplatzprioritäten. Sie können Ihre Palettenlagerplätze mit dieser Lagerplatzart und mit Prioritäten einrichten, die niedriger sind als die Ihrer normalen Kommissionierungslagerplätze oder der besonders bevorzugten Kommissionierungslagerplätze.|  
|QK|Dieser Lagerplatz wird für einen Ausgleich von Lagerbestand verwendet, wenn Sie diesen Lagerplatz auf der Lagerortkarte im Feld **Ausgleichlagerplatzcode** angeben. Sie können Lagerplätze dieser Art auch für beschädigte Artikel und Artikel, die für Qualitätskontrollen verwendet werden, einrichten. Sie können Artikel in diese Art von Lagerplätzen umlagern, wenn Sie möchten, dass diese für den normalen Warenfluss nicht zugänglich sein sollen.<br /><br /> **HINWEIS:** Anders als alle anderen Lagerplatzarten hat die Lagerplatzart **QK** keine standardmäßig aktivierten der Kontrollkästchen für die Behandlung. Dies bedeutet, dass jeder Inhalt, den Sie an einem QC-Lagerplatz platzieren, aus den Artikelströmen ausgeschlossen ist.|  

## <a name="see-related-microsoft-trainingtrainingmodulesset-up-zones-bins" />Siehe verwandte [Microsoft Schulungen](/training/modules/set-up-zones-bins/)

## <a name="see-also" />Siehe auch

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
