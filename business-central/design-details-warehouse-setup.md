---
title: Designdetails - Lagerhaus Einrichten | Microsoft Docs
description: Lagerfunktionen in Business Central enthalten verschiedene Komplexitätsstufen, definiert durch Lizenzberechtigungen in den angebotenen Elementen. Die Komplexitätsstufe in einer Lagerlösung ist weitgehend durch den Lagerplatz definiert, der auf Lagerortkarten eingerichtet ist, die wiederum lizenz-gesteuert ist, sodass der Zugriff auf Lagerplatzsetupfelder durch die Lizenz definiert ist.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 4346b3a2570710f09d5deaded2788274155f1a5a
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214778"
---
# <a name="design-details-warehouse-setup"></a>Designdetails: Lagereinrichtung

Lagerfunktionen in [!INCLUDE[prod_short](includes/prod_short.md)] enthalten verschiedene Komplexitätsstufen, definiert durch Lizenzberechtigungen in den angebotenen Elementen. Die Komplexitätsstufe in einer Lagerlösung ist weitgehend durch den Lagerplatz definiert, der auf Lagerortkarten eingerichtet ist, die wiederum lizenz-gesteuert ist, sodass der Zugriff auf Lagerplatzsetupfelder durch die Lizenz definiert ist. Darüber hinaus steuern die Anwendungsobjekte in der Lizenz, welche UI-Dokumente für die unterstützten Lageraktivitäten zu verwenden sind.  
<!--
The following warehouse-related granules exist:  

- Basic Inventory (4010)  
- Bin (4170)  
- Put Away (4180)  
- Warehouse Receipt (4190)  
- Pick (4200)  
- Warehouse Shipment (4210)  
- Warehouse Management Systems (4620)  
- Internal Picks and Put-aways (4630)  
- Automated Data Capture System (4640)
- Bin Setup (4660)  

For more information about each granule, see [[!INCLUDE[prod_short](includes/prod_short.md)] Price Sheets](https://go.microsoft.com/fwlink/?LinkId=238341) (requires PartnerSource account). -->

Die nachstehende Tabelle zeigt, welche Elemente benötigt werden, um verschiedene Lagerkomplexitätsebenen zu definieren, welche UI-Dokumente die einzelnen Ebenen unterstützen und welche Lagerortcodes diese Ebenen in der [!INCLUDE[prod_short](includes/prod_short.md)] Demodatenbank widerspiegeln.  

[!INCLUDE [locations-cronus](includes/locations-cronus.md)]

|Komplexitätsebene|Beschreibung|UI-Dokument|Beispiel Ort|Minimale Elementanforderung|  
|----------------|-----------|-----------|---------------|---------------------------|  
|1|Keine dedizierte Lageraktivität.<br /><br /> Eingangs-/Lieferungsbuchung aus Aufträgen.|Bestellung|BLAU|Grundlegender Lagerbestand|  
|2|Keine dedizierte Lageraktivität.<br /><br /> Eingangs-/Lieferungsbuchung aus Aufträgen.<br /><br /> Lagerplatzcode ist erforderlich.|Auftrag, mit Lagerplatzcode|SILBER|Grundlegender Lagerbestand/Lagerplatz|  
|3 <br /><br /> **Hinweis**: Obwohl die Einstellungen **Kommissionierung erforderlich** und **Einlagerung erforderlich** genannt werden, können Sie weiterhin Wareneingänge und Lieferungen direkt aus den Quellgeschäftsunterlagen an Lagerorten, in denen Sie diese Kontrollkästchen aktivieren.|Grundlegende Lageraktivität, Auftrag für Auftrag.<br /><br /> Eingangs-/Lieferungsbuchung aus Lagereinlagerungs-/Kommissionierbelegen. <br /><br /> Lagerplatzcode ist erforderlich.|Einlagerung/Lagerbestandsumlagerung/Kommissionierung, mit Lagerplatzcode|(SILBER + Einlagerung erfordern oder Einlagerung erfordern)|Grundlegender Lagerbestand/Lagerplatz/Einlagerung/Kommissionierung|  
|4|Erweiterte Lageraktivität, für mehrere Aufträge.<br /><br /> Konsolidierte Eingangs-/Lieferungsbuchung, basierend auf Lager-Einlagerungs-/Kommissionierungsregistrierungen.|Wareneingang/Einlagerung/Kommissionierung/Warenausgang/Kommissionierarbeitsblatt|GRÜN|Grundlegender Lagerbestand/Wareneingang/Einlagerung/Kommissionierung/Lagerlieferung|  
|5|Erweiterte Lageraktivität, für mehrere Aufträge.<br /><br /> Konsolidierte Eingangs-/Lieferungsbuchung, basierend auf Lager-Einlagerungs-/Kommissionierungsregistrierungen.<br /><br /> Lagerplatzcode ist erforderlich.|Wareneingang/Einlagerung/Kommissionierung/Warenausgang/Kommissionierarbeitsblatt/Einlagerungsarbeitsblatt, mit Lagerplatzcode|(GRÜN + Lagerplatz notwendig)|Grundlegender Lagerbestand/Lagerplatz/Wareneingang/Einlagerung/Kommissionierung/Lagerlieferung|  
|6 <br /><br /> **Hinweis**: Diese Ebene wird als WMS bezeichnet, da sie die detailliertesten Warehouse Management Systeme benötigt.|Erweiterte Lageraktivität, für mehrere Aufträge<br /><br /> Konsolidierte Eingangs-/Lieferungsbuchung, basierend auf Lager-Einlagerungs-/Kommissionierungsregistrierungen.<br /><br /> Lagerplatzcode ist erforderlich.<br /><br /> Zone/Klassencode ist optional.<br /><br /> Lagermitarbeiter durch Workflow gesteuert<br /><br /> Lagerplatzauffüllungsplanung<br /><br /> Lagerplatzpriorität<br /><br /> Lagerplatz-Setup nach Kapazität<br /><br /> Einfügen  <!-- Hand-held device integration -->|Wareneingang/Einlagerung/Kommissionierung/Warenausgang/Kommissionierarbeitsblatt/Einlagerungsarbeitsblatt. Kommissionierung/interne Einlagerung, mit/Lagerplatz/Zonencode Klasse<br /><br /> Verschiedene Arbeitsblätter für Lagerplatzverwaltung<br /><br /> ADCS-Bildschirme|WEISS|Grundlegender Lagerbestand/Lagerplatz/Einlagerung/Wareneingang/Kommissionierung/Lagerlieferung/Logistiksysteme/interne Kommissionierungen und Einlagerungen/Lagerplatzeinrichtung<!-- Automated Data Capture System/ -->Lagerplatz-Setup|  

Beispiele dazu, wie die UI-Dokumente pro Lagerkomplexitätsebene verwendet werden, finden Sie unter [Designdetails: Eingehender Lagerhausfluss](design-details-inbound-warehouse-flow.md).  

## <a name="bin-and-bin-content"></a>Lagerplatz,Lagerplatzinhalt

Ein Lagerplatz ist ein Speicherbehälter, der dafür ausgelegt ist, diskrete Teile aufzunehmen. Es ist die kleinste Containereinheit in [!INCLUDE[prod_short](includes/prod_short.md)]. Artikelmengen in Lagerplätzen werden als Lagerplatzinhalte bezeichnet. Ein Lookup aus dem Feld **Artikel** oder aus Feld **Lagerplatzcode** auf jeder lagerbezogenen Belegzeile zeigt die berechnete Verfügbarkeit des Artikels am Lagerplatz an.  

Ein Lagerplatzinhalt kann die Eigenschaft "Fest", "Dediziert" oder "Standard" erhalten, um festzulegen, wie er verwendet werden kann. Lagerplätze mit keinen dieser Eigenschaften gelten als chaotische Lagerplätze.  

Ein fester Lagerplatz enthält Artikel an, die dem jeweiligen Lagerplatzcode zugeordnet sind. Die Eigenschaft „fester Lagerplatz “ stellt sicher, dass auch dann, wenn der Inhalt des Lagerplatzes vorübergehend leer ist, der Lagerplatzinhalt nicht verschwindet und der Lagerplatz daher erneut ausgewählt wird, sobald er wieder aufgefüllt wurde.  

Ein dedizierter Lagerplatz enthält Lagerplatzinhalt, der nur für die dedizierte Ressource, wie etwa einen Arbeitsplatz, kommissioniert werden kann, die den betreffenden Lagerplatz verwendet. Anderer NichtEntnahmeinhalt, wie z.B. Mengen, die in einer Lieferungsbuchung ausgehend sind, können durch einen dedizierten Lagerplatz noch verbraucht werden. Nur Lagerplatzinhalt, der durch den Algorithmus **Kommissionierung erstellen** berücksichtigt wird, wird in einem dedizierten Lagerplatz geschützt.  

Die Standardlagerplatzeigenschaft wird vom System verwendet, um Lagerplätze für Lageraktivitäten vorzuschlagen. An WMS-Lagerorten wird die Standardlagerplatzeigenschaft nicht verwendet. An Lagerorten, an denen Lagerplätze erforderlich sind, wird die Eigenschaft in eingehenden Flüssen verwendet, um anzugeben, wo Artikel zu platzieren sind. In ausgehenden Flüssen wird die Eigenschaft verwendet, um anzugeben, wo Artikel entnommen werden sollen.  

> [!NOTE]  
>  Wenn die ausgehenden Artikel in mehrere Lagerplätze eingelagert werden, werden Artikel zuerst den nicht standardmäßigen Lagerplätzen entnommen, um diesen Lagerplatzinhalt zu leeren, und dann werden die anderen Artikel dem Standardlagerplatz entnommen.  

Es kann nur einen Vorgabelagerplatz pro Artikel pro Lagerort geben.  

## <a name="bin-type"></a>Lagerplatzart

In WMS-Installationen können Sie die Lageraktivitäten einschränken, die für einen Lagerplatz möglich sind, indem Sie einen Lagerplatztyp zuweisen. Die folgenden Lagerplatzarten sind verfügbar:  

|Lagerplatzart|Beschreibung|  
|------------------|---------------------------------------|  
|EING|Die Artikel werden als erhalten registriert, aber noch nicht eingelagert.|  
|AUSG|Die Artikel wurden für Warenausgangszeilen kommissioniert, der Warenausgang wurde jedoch noch nicht gebucht.|  
|EINLAG|Normalerweise werden hier Artikel in großen Einheiten eingelagert, die jedoch nicht für die Kommissionierung verwendet werden soll. Da die Lagerplätze nicht zum kommissionieren verwendet werden, weder für Fertigungsaufträge noch für Warenausgänge, kann Ihre Nutzung von Lagerplätzen der Art "Einlagerung" begrenzt sein, diese Lagerplatzart kann jedoch sinnvoll sein, wenn Sie eine große Menge an Artikeln eingekauft haben. Lagerplätze dieser Art sollten immer eine niedrige Lagerplatzpriorität haben, so dass beim Einlagern von angenommenen Artikeln diese zuerst in die Lagerplätze der Art EINLAGKOMM mit höherer Priorität einlagert werden, die als Standard für diesen Artikel definiert wurden. Wenn Sie diese Art von Lagerplatz nutzen, müssen Sie regelmäßig eine Lagerplatzauffüllung durchführen, so dass die Artikel, die in diesen Lagerplätzen gelagert werden, auch in Lagerplätzen der Art EINLAGKOMM oder KOMMISS verfügbar sind.|  
|KOMMISS|Nur für Kommissionierung zu verwendende Artikel. Die Auffüllung dieser Lagerplätze kann nur durch Umlagerungen, nicht durch Einlagerungen, durchgeführt werden.|  
|EINLAGKOMM|Artikel an Lagerplätzen, die für Einlagerungs- und Kommissionierungsfunktionen vorgeschlagen werden. Lagerplätze dieser Art haben wahrscheinlich unterschiedliche Lagerplatzprioritäten. Sie können Ihre Palettenlagerplätze mit dieser Lagerplatzart und mit Prioritäten einrichten, die niedriger sind als die Ihrer normalen Kommissionierungslagerplätze oder der besonders bevorzugten Kommissionierungslagerplätze.|  
|QK|Dieser Lagerplatz wird für einen Ausgleich von Lagerbestand verwendet, wenn Sie diesen Lagerplatz auf der Lagerortkarte im Feld **Ausgleichlagerplatzcode** angeben. Sie können Lagerplätze dieser Art auch für beschädigte Artikel und Artikel, die für Qualitätskontrollen verwendet werden, einrichten. Sie können Artikel in diese Art von Lagerplätzen umlagern, wenn Sie möchten, dass diese für den normalen Warenfluss nicht zugänglich sein sollen. **HINWEIS:**  Anders als alle anderen Lagerplatzarten hat die Lagerplatzart **QK** keine standardmäßig aktivierten Kontrollkästchen für die Behandlung. Dies bedeutet, dass jeder Inhalt, den Sie an einem QC-Lagerplatz platzieren, aus den Artikelströmen ausgeschlossen ist.|  

Für alle Lagerplatzarten, außer PICK, PUTPICK und PUTAWAY, ist keine andere Aktivität für den Lagerplatz erlaubt als die, die durch ihre Lagerplatzart definiert ist. Beispielsweise kann ein Lagerplatz Art **Eingang** nur verwendet werden, um Artikel zu erhalten oder Artikel zu kommissionieren.  

> [!NOTE]  
> Nur Umlagerung kann an den Lagerplätzen des Typs EING und QC erfolgen. Ebenso können nur Umlagerungen aus Lagerplätzen des Typs SHIP und QC vorgenommen werden.  

## <a name="bin-ranking"></a>Lagerplatzpriorität

In der erweiterten Lagerhaltung können Sie automatisieren und optimieren, wie Artikel in Lagerplätzen gesammelt und Arbeitsblätter nach entnommen werden können, so dass Artikel gemäß Empfehlung und gemäß Rankingkriterien eingelagert oder entnommen werden, damit der Lagerplatz optimal genutzt wird.  

Die Einlagerungszeilen Prozesse werden optimiert nach Lagerplatzprioritäten, indem Sie mit höherer Priorität bevor Niedrigklassifizierungslagerplätze vorschlagen. Ebenso werden Entnahmeprozesse durch erste vorschlagende Artikel aus dem Lagerplatzinhalt mit hoher Lagerplatzpriorität optimiert. Darüber hinaus werden Lagerplatzauffüllungen aus den Lagerplätzen mit niedrigerem oder höherem Rang vorgeschlagen.  

Die Lagerplatzpriorität zusammen mit den Lagerplatzinhaltinformationen sind die grundlegenden Eigenschaften, anhand derer Benutzer Artikel im Lager einsortieren.  

## <a name="bin-setup"></a>Lagerplatz-Setup  
In erweiterten Lagerorten können Lagerplätze mit Kapazitätswerten, wie Menge, Gesamtvolumen und Gewicht eingerichtet werden, um zu steuern, welche Artikel wie an dem Lagerplatz aufbewahrt werden.  

In jeder Artikelkarte können Sie eine Einheit (UOM) für den Artikel, wie Stück, Paletten, Liter, Gramm oder Felder zuordnen. Sie können eine Grundlage Mengeneinheit für einen Artikel ebenfalls haben und größere Mengeneinheit für einen Artikel, die darauf basieren, angeben. Beispielsweise können Sie eine Palette auf 16 Stück festlegen (die Basismengeneinheit).  

Wenn Sie eine maximale Menge eines bestimmten Artikels für die Speicherung in einem einzelnen Lagerplatz einrichten möchten und für den Artikel mehr als eine Mengeneinheit besteht, müssen Sie die Höchstmenge für jede Mengeneinheit auf der Artikelkarte einrichten. Entsprechend gilt: Wenn ein Artikel so eingerichtet wurde, dass er nach Stück und Paletten bearbeitet wird, muss das **Maximale Menge**-Feld auf der Seite **Lagerplatz-Inhalt** für diesen Artikel ebenfalls nach Stück und Paletten organisiert sein. Andernfalls wird die zulässige Menge für diesen Lagerplatz nicht korrekt berechnet.  

Bevor Sie Kapazitätseinschränkungen für Lagerplatzinhalte an einem Lagerplatz einrichten, müssen Sie zuerst prüfen, ob die Mengeneinheit und die Dimensionen des Artikels auf der Artikelkarte eingerichtet wurden.  

> [!NOTE]  
> Es kann nur mit mehrfachen Maßeinheiten in WMS-Installationen verfahren werden. In allen anderen Konfigurationen können Lagerplatzinhalte nur in der Basismengeneinheit platziert werden. In allen Transaktionen mit einer Einheit größer als die Basiseinheit des Artikels wird die Menge in die Basiseinheit umgewandelt.  

## <a name="zone"></a>Servicegebiet

In der erweiterten Lagerhaltung können Lagerplätze in Zonen gruppiert werden, um den Workflow der Lageraktivitäten zu verwalten.  

Eine Zone kann eine empfangende Zone oder eine Lagerzone sein, und jede Zone kann aus einem oder mehreren Lagerplätzen bestehen.  

Die meisten Eigenschaften, die einer Zone zugeordnet sind, werden standardmäßig dem Lagerplatz zugeordnet, der aus dieser Zone erstellt wird.  

## <a name="class"></a>Klasse  
In der erweiterten Lagerhaltung können Sie Lagerklassencodes den Artikeln, Lagerplätzen und auch Zonen zuordnen, um festzulegen, wo verschiedene Artikelklassen gespeichert werden, wie z.B. Tiefkühlkost. Sie können eine Zone in mehrere Lagerklassen aufteilen. Beispielsweise können Artikel in der empfangenden Zone als eingefroren, gefährlich oder einer anderen klasse zugehörig gespeichert werden.  

Wenn Sie mit Lagerklassen und standardmäßigen Empfangs-/Versandlagerplätzen arbeiten, müssen Sie die entsprechenden Lagerplätze im Wareneingang und in den Lieferzeilen manuell ausfüllen.  

In eingehenden Flüssen wird der Klassencode nur auf eingehenden Zeilen hervorgehoben, auf denen der Artikelklassencode nicht dem standardmäßigen Wareneingangslagerplatz entspricht. Wenn die richtigen Standardlagerplätze nicht zugewiesen werden, kann die Menge nicht empfangen werden.  

## <a name="location"></a>Lagerort

Ein Lagerort ist eine physische Struktur oder ein Ort, an der/dem Lagerbestand erhalten, gespeichert und geliefert wird, möglicherweise organisiert in Lagerplätze. Ein Lagerort kann ein Lager, ein Service-Auto, ein Verkaufsraum, eine Anlage oder ein Bereich in einer Anlage sein.  

## <a name="first-expired-first-out"></a>Ausgang nach frühestem Ablaufdatum

Wenn Sie das Kontrollkästchen **Gemäß FEFO kommissionieren** im Inforegister **Lagerplatzprüfung** auf der Lagerortkarte wählen, werden Artikel mit Artikelverfolgung entsprechend ihrem Ablaufdatum kommissioniert. Die Artikel mit den frühesten Ablaufdaten werden zuerst kommissioniert.  

Lageraktivitäten in allen Kommissionierungs- und Umlagerungsdokumenten werden gemäß FEFO sortiert, es sei denn, den fraglichen Artikel ist bereits eine Serien-/Chargennummer zugeordnet. Wenn nur einem Teil der Menge auf der Zeile bereits Chargen- oder Seriennummern zugewiesen sind, wird die verbleibende zu kommissionierende Menge nach dem FEFO-Prinzip sortiert.  

Bei der Kommissionierung über FEFO wählt die Anwendung verfügbare Artikel auf der Grundlage des Ablaufdatums aus; das Ergebnis ist eine temporäre Artikelverfolgungsliste, die auf dem Ablaufdatum basiert. Weisen zwei Artikel dasselbe Ablaufdatum aus, wählt die Anwendung den Artikel mit der niedrigeren Chargen- oder Seriennummer zuerst aus. Sind die Chargen- oder Seriennummern identisch, wählt die Anwendung den Artikel aus, der zuerst ausgewählt wurde. Die Standardkriterien für die Auswahl der Artikel in Kommissionierungslagerplätzen, wie z. B. nach Lagerplatzpriorität und Gebindeanbruch, werden auf diese temporäre FEFO-Artikelverfolgungsliste angewendet.  

## <a name="put-away-template"></a>Einlagerungsvorlage

Die Einlagerungsvorlage kann einem Artikel und einem Lagerort zugewiesen werden. Die Einlagerungsvorlage gibt einen Satz priorisierter Regeln an, die bei der Erstellung von Einlagerungen berücksichtigt werden müssen. Beispielsweise kann eine Einlagerungsvorlage erfordern, dass der Artikel in einen Lagerplatz mit Lagerplatzinhalt gesetzt wird, der der Mengeneinheit entspricht, und wenn ein ähnlicher Lagerplatz mit genügender Kapazität nicht gefunden werden kann, muss der Artikel in einen leeren Lagerplatz gesetzt werden.  

## <a name="see-also"></a>Siehe auch

[Designdetails: Logistik](design-details-warehouse-management.md)   
[Designdetails: Verfügbarkeit im Lager](design-details-availability-in-the-warehouse.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]