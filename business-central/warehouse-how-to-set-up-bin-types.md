---
title: So richten Sie Lagerplatzarten ein | Microsoft Docs
description: Sie können den Warenfluss durch die Lagerplätze steuern, die Sie für bestimmte Logistikaktivitäten definiert haben. Sie weisen jedem Lagerplatz eine Lagerplatzart zu und ordnen dadurch dem Lagerplatz seine grundlegenden Warenflussaktivitäten zu, und definieren hiermit auf welche ein Lagerplatz verwendet wird.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e54c82e2d00c26f191506b8057a730d31fddc867
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925396"
---
# <a name="set-up-bin-types"></a>Lagerplatzarten einrichten
Sie können den Warenfluss durch die Lagerplätze steuern, die Sie für bestimmte Logistikaktivitäten definiert haben. Sie weisen jedem Lagerplatz eine Lagerplatzart zu und ordnen dadurch dem Lagerplatz seine grundlegenden Warenflussaktivitäten zu, und definieren hiermit auf welche ein Lagerplatz verwendet wird.  

Es gibt sechs Arten. Sie können Ihr Lager mit allen möglichen sechs Lagerplatzarten betreiben oder Sie entscheiden sich, nur die Lagerplatzarten EING, EINLAGKOMM, AUSG und QK zu verwenden. Diese vier Lagerplatzarten ermöglichen der Anwendung, Vorschläge zu machen, um den Warenfluss zu unterstützen, und sie geben Ihnen die Möglichkeit, Abweichungen im Lagerbestand zu erfassen.  

## <a name="to-set-up-the-bin-types-you-want-to-use"></a>So richten die Lagerplatzarten ein, die Sie verwenden möchten:  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lagerplatzarten** ein, und wählen Sie dann den zugehörigen Link.  
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

## <a name="see-also"></a>Siehe auch
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Lagerverwaltung](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
