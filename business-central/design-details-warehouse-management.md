---
title: Lager-Aktivitäten verwalten
description: Zusätzlich zu Eingängen und Lieferungen unterstützt Business Central eine Reihe interner Lageraktivitäten.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/05/2022
ms.custom: bap-template
---

# <a name="warehouse-management-overview" />Lagerverwaltung – Übersicht

Es gibt zwei Dinge, die für alle Unternehmen wichtig sind, die Waren physisch in ihr Lager ein- und auslagern:

* Sie haben einen Überblick über die Lagerbestände und die Platzierung der Artikel im Lager.
* Sie können Artikel schnell und genau empfangen, kommissionieren und versenden.

Um Unternehmen dabei zu helfen, diese Dinge zu erreichen, fügen Lagerfunktionen in [!INCLUDE[prod_short](includes/prod_short.md)] der Bestandsverwaltung die folgenden Funktionen hinzu:

* Lagerplätze
* Warenausgänge
* Lagerkommissionierungen
* Lagerplatzumlagerungsarbeitsblatt

Implementieren Sie diese Funktionen in verschiedenen Kombinationen, um Ihre Lagerprozesse an Ihr Unternehmen anzupassen. Berücksichtigen Sie eine zunehmende Komplexität, wenn Ihr Unternehmen wächst und sich Ihre Prozesse ändern.

## <a name="overview-of-different-configuration-options" />Übersicht über verschiedene Konfigurationsmöglichkeiten

Sie können Lagerfunktionen auf verschiedene Weise konfigurieren. Es ist wichtig, Optionen zu wählen, die Ihre Prozesse verbessern, ohne Gemeinkosten zu verursachen. Die folgende Tabelle gibt einen Überblick über typische Konfigurationen für den Umgang mit physischen Gütern.

|Komplexitätsebene|Description|Einstellungen|Lagerplatzcode|Beispiel für eingehenden Fluss|Beispiel für den ausgehenden Fluss|Beispiel für internen Fluss|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Keine dedizierte Lageraktivität.|Buchung von Aufträgen und Journalen.||Optional. Gesteuert durch den Schalter **Lagerplatzcode obligatorisch**.|Einkaufsbestellung|Verkaufsauftrag| Produktionsauftrag -> FA-Verb. Buch.-Blatt|  
|Standard|Konsolidierte Eingangs-/Versandbuchung für mehrere Bestellungen.|**Wareneingang erforderlich**<br>**Warenausgang erforderlich**.|Optional. Gesteuert durch den Schalter Lagerplatzcode obligatorisch|Bestellung(en) -> Wareneingang|Verkaufsauftrag -> Warenausgangskopf|Wie oben.|
|Standard|Auftrag für Auftrag|Einlagerung erfordern oder Kommissionierung erfordern </br><br/> **HINWEIS**: Obwohl die Einstellungen **Kommissionierung erforderlich** und **Einlagerung erforderlich** genannt werden, können Sie weiterhin Wareneingänge und Lieferungen direkt aus den Quellunterlagen an Lagerorten, in denen Sie diese Kontrollkästchen aktivieren.|Optional. Gesteuert durch den Schalter **Lagerplatzcode obligatorisch**.|Einkaufsbestellung -> Lagereinlagerung|Verkaufsauftrag -> Lagerkommissionierung|Fertigungsauftrag -> Lagerbestandkommissionierung|
|Erweitert|Konsolidierte Eingangs-/Versandbuchung für mehrere Bestellungen.<br /><br />Konsolidierte Kommissionierungs-/Einlagerungsaktivitäten für mehrere Herkunftsbelege.|Wareneingang erforderlich + Einlagerung erforderlich</br> Warenausgang erforderlich + Kommissionierung erforderlich|Optional. Gesteuert durch den Schalter Lagerplatzcode obligatorisch|Bestellung(en) -> Wareneingang -> Einlagerung|Verkaufsaufträge -> Lagerlieferungen -> Kommissionierungsarbeitsblatt -> Kommissionierungen| Fertigungsauftrag -> Kommissionierungsarbeitsblatt -> Kommissionierungen -> FA-Verbrauchs Buch.-Blatt|
|Erweitert|Wie oben + Gezielte Kommissionierungs-/Einlagerungsaktivitäten|Gezielte Kommissionierung und Einlagerung (abhängige Schalter werden automatisch aktiviert)|Notwendig|Wie oben.|Wie oben.| Fertigungsauftrag -> Kommissionierungsarbeitsblatt -> Kommissionierungen FA-Verbrauchs Buch.-Blatt|

Die Komplexität steigt mit der Größe Ihrer Organisation und der Anzahl der beteiligten Abteilungen und Personen. Ein Prozess kann beispielsweise einfach sein, wenn dieselbe Person einen Verkaufsbeleg erstellt und bucht. Prozesse können auch komplexer sein und mehrere Schritte und Personen umfassen. Die folgenden Schritte sind ein Beispiel für einen komplexeren Prozess:

1. Der Verarbeiter eines Auftrags erstellt einen Verkaufsauftrag.
1. Ein Lagerleiter erstellt Kommissionierungsanweisungen.
1. Ein Lagermitarbeiter schließt den Ablauf ab, indem er die Lagerlieferung bucht.

Der Grad der Komplexität wird auch durch die Arten von Dokumenten beeinflusst, die Sie in Ihren Lageraktivitäten verwenden. Beispielsweise können Sie Wareneingangs- und Lagereinlagerungsbelege für Ihren Wareneingangsfluss, aber Bestandsentnahmebelege für Ihren Warenausgangsfluss verwenden.

Ein weiterer Faktor, der sich auf die Komplexität auswirkt, ist die Darstellung Ihres physischen Lagers in [!INCLUDE[prod_short](includes/prod_short.md)]. Weitere Informationen finden Sie unter [Modellierung des physischen Lagers](#modeling-the-physical-warehouse).

## <a name="modeling-the-physical-warehouse" />Modellierung des physischen Lagers

In [!INCLUDE[prod_short](includes/prod_short.md)] haben Sie mehrere Möglichkeiten, den realen Aufbau Ihres Lagers darzustellen. Ihre Auswahl bestimmt, wie Sie mit Warehouse-Funktionen arbeiten.

Bei der Platzierung von Artikeln kann es sich um Regale, Standorte oder Lagerplätze handeln, und es gibt Vor- und Nachteile für jede Option.

### <a name="locations-and-bins" />Lagerorte und Lagerplätze

Um physische Waren zu handhaben, müssen Sie mindestens einen Standort haben. Sie können mehrere Standorte oder Lagerplätze verwenden, um Ihre Lager- und Organisationsstruktur zu modellieren.

Standorte sind in der Regel die bevorzugte Methode für die Organisation von Vorgängen, die über geografische Gebiete verteilt sind. In einigen Fällen möchten Sie jedoch möglicherweise mehrere Standorte erstellen, die sich am selben Ort befinden. Die Verwendung von Standorten hat folgende Vorteile:

* Gewähren Sie Zugriff über die Seiten **Lagermitarbeiter** und **Verantwortungszentren**.
* Definieren Sie Kalender, Arbeitspläne sowie eingehende und ausgehende Bearbeitungszeiten für die Datumsberechnung und -planung. Weitere Informationen unter [Info zu Planungsfunktionen](production-about-planning-functionality.md).
* Geben Sie Standarddimensionen an und verwenden Sie unterschiedliche Lagerbuchungseinstellungen.
* Richten Sie Planungsparameter ein. Erfahren Sie mehr unter [Planungsparameter](production-about-planning-functionality.md#planning-parameters).  
* Verwenden Sie für jeden Standort unterschiedliche Lagerfunktionen.

### <a name="shelves-and-bins" />Regale und Lagerplätze

Wenn Sie einen Artikel immer am selben Ort lagern, können Sie das Feld **Regal-Nr.** auf den Seiten **Artikelkarte** oder **Lagerhaltungseinheitskarte** verwenden. Dieses Feld kann ein grundlegendes manuelles Speichersystem in Umgebungen ohne Lagerplätze sein. Der Feldwert wird von der Artikelkarte in die Belegzeilen und Berichte kopiert, dient jedoch nur zur Information. Der Wert wird nicht in Lageraktivitäten oder Verfügbarkeitsberechnungen verwendet.

Lagerplätze stellen die grundlegende Lagerstruktur dar und werden verwendet, um Vorschläge zur Einlagerung von Artikeln zu erstellen.

* Mindestens einen festen Lagerplatz für einen Artikel.
* Lagerplätze für bestimmte Vorgänge, z. B. ein Versandlagerplatz oder ein Produktionsausgabelagerplatz.
* Lagerplatzkapazitäts- und Gewichtsbeschränkungen (nur für gesteuerte Einlagerung und Kommissionierung).
* Lagerplatzbewertung (nur für gesteuerte Einlagerung und Kommissionierung).

## <a name="typical-warehouse-workflow" />Typischer Lagerablauf

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Artikeln, die sie beschreiben.

|**Bis**|**Siehe**|  
|------------|-------------|  
|Verwenden Sie in einem einfachen Ablauf auf Auftrag-für-Auftrag-Basis eine Lagereinlagerung, um den Eingang von Artikeln an Standorten zu erfassen, einschließlich etwaiger Übereingänge. Oder verwenden Sie einen Wareneingang, wenn Sie mehrere Aufträge im Beleg zusammenfassen.|[Eingehender Fluss](design-details-inbound-warehouse-flow.md)|
|Erfassen Sie den Versand von Artikeln von Lagerstandorten. Verwenden Sie auf Auftrag-zu-Auftrag-Basis eine Lagerkommissionierung. Oder verwenden Sie einen Warenausgang, wenn Sie mehrere Aufträge in der Versendung zusammenfassen.|[Ausgehender Warenfluss](design-details-outbound-warehouse-flow.md)|
|Bearbeiten Sie Artikel innerhalb des Lagerstandorts. Zum Beispiel, wenn Sie Komponenten in die Produktion verschieben oder eine Inventur durchführen.|[Interne Flüsse](design-details-internal-warehouse-flows.md)|

Richten Sie die Lagerprozesse ein, die für Ihr Unternehmen geeignet sind. Weitere Informationen finden Sie unter [Einrichten von Warehouse Management](warehouse-setup-warehouse.md).

## <a name="terminology-related-to-warehouse-management" />Terminologie im Zusammenhang mit der Lagerverwaltung

### <a name="complexity-levels" />Komplexitätsebenen

Wir verwenden die Begriffe „einfach“ und „fortgeschritten“, um zwischen Komplexitätsebenen zu unterscheiden. Diese einfache Unterscheidung umfasst mehrere Komplexitätsebenen in der Lagerorteinrichtung, wobei jede durch unterschiedliche Lagerdokumente unterstützt werden. Die erweiterte Ebene der Lagerhaltung wird als „gesteuertes Einlagern und Kommissionieren“ bezeichnet. Um die gesteuerte Einlagerung und Entnahme für einen Standort zu verwenden, aktivieren Sie die **gesteuerte Einlagerung und Kommissionierung** auf der **Standortkarte**-Seite.

### <a name="warehouse-flows" />Lagerabläufe

* Eingehender Fluss - Artikel in den Lagerort einbringen und verfügbar machen, z.B. Einkäufe und eingehende Umlagerungen.
* Ausgehender Fluss – Artikel kommissionieren und an Kunden oder andere Standorte versenden.
* Interner Fluss – Artikel innerhalb eines Standorts bearbeiten. Beispiel: Komponenten in die Produktion verschieben oder eine Inventur durchführen.

### <a name="basic-documents" />Grundlegende Dokumente

Die folgenden Dokumente werden in grundlegenden Lagerabläufen verwendet.

* Lagereinlagerung
* Lagerkommissionierung
* Lagerbestandsumlagerung
* Artikel Buch.-Blatt
* Artikel Umlag. Buch.-Blatt

### <a name="advanced-documents" />Erweiterte Dokumente

Die folgenden Dokumente werden in erweiterten Lagerabläufen verwendet.

* Wareneingang
* Einlagerungsarbeitsblatt
* Einlagerung
* Kommissionierarbeitsblatt
* Kommissionierung
* Lagerplatzumlagerungsarbeitsblatt
* Lagerplatzumlagerung
* Interne Lagerkommissionierung
* Interne Einlagerungsanforderung
* Lagerplatz Erst.-Arbeitsblatt
* Lagerplatzinh. Erst.-Arbeitsblatt
* Logistik Artikel Buch.-Blatt
* Lagerartikelumlagerungs Buch.-Blatt

### <a name="pages-and-settings" />Seiten und Einstellungen

In diesem Abschnitt werden die Konzepte hinter den wichtigsten Seiten und Einstellungen für die Lagerhaltung beschrieben.

#### <a name="bins-and-bin-content" />Lagerplatze und Lagerplatzinhalt

Ein Lagerplatz ist ein Speicherbehälter, der dafür ausgelegt ist, diskrete Teile aufzunehmen. Es ist die kleinste Containereinheit in [!INCLUDE[prod_short](includes/prod_short.md)]. Artikelmengen in Lagerplätzen werden als *Lagerplatzinhalte* bezeichnet. Ein Lookup aus dem Feld **Artikel** oder aus Feld **Lagerplatzcode** auf jeder lagerbezogenen Belegzeile zeigt die berechnete Verfügbarkeit des Artikels am Lagerplatz an.  

Lagerplatzinhalte können die Eigenschaft **Fest**, **Dediziert** oder **Standard** erhalten, um festzulegen, wie dir verwendet werden können. Lagerplätze mit keinen dieser Eigenschaften gelten als *chaotische* Lagerplätze.  

Ein fester Lagerplatz enthält Artikel an, die dem Lagerplatzcode zugeordnet sind. Die feste Lagerplatzeigenschaft stellt sicher, dass der Lagerplatzinhalt auch dann nicht verschwindet, wenn der Lagerplatz geleert wird. Sie können den Lagerplatz erneut auswählen, sobald sein Inhalt aufgefüllt ist.  

Ein dedizierter Lagerplatz enthält Lagerplatzinhalt, der nur für die dedizierte Ressource, kommissioniert werden kann, die den Lagerplatz verwendet. Zum Beispiel ein Maschinenzentrum. Anderer Nicht-Entnahmeinhalt, wie z.B. Mengen, die in einer Lieferungsbuchung ausgehend sind, können durch einen dedizierten Lagerplatz verbraucht werden. Nur Lagerplatzinhalt, der durch den Algorithmus **Kommissionierung erstellen** berücksichtigt wird, wird in einem dedizierten Lagerplatz geschützt.  

[!INCLUDE [prod_short](includes/prod_short.md)] verwendet die **Standard**-Lagerplatzeigenschaft, um Lagerplätze für Lageraktivitäten vorzuschlagen. An Lagerorten mit gesteuerter Einlagerung und Kommissionierung wird die Standardlagerplatzeigenschaft nicht verwendet. An Lagerorten, an denen Lagerplätze erforderlich sind, gibt die Eigenschaft an, wo Artikel bei eingehenden Flüssen zu platzieren sind. In ausgehenden Flüssen gibt die Eigenschaft an, wo Artikel entnommen werden sollen.  

> [!NOTE]  
> Wenn ausgehende Artikel in mehrere Lagerplätze eingelagert werden, werden Artikel zuerst den nicht standardmäßigen Lagerplätzen entnommen, um diesen Lagerplatzinhalt zu leeren, und dann werden die anderen Artikel dem Standardlagerplatz entnommen.  

Sie können einen Vorgabelagerplatz pro Artikel pro Lagerort geben.  

#### <a name="bin-type" />Lagerplatzart

Lagerplätze, die gesteuerte Einlagerung und Entnahme verwenden, können Lagerplatztypen verwenden. Lagerplatztypen steuern die Aktivitäten, die Sie für einen Lagerplatz zulassen. Die folgenden Lagerplatztypen sind verfügbar:  

|Lagerplatzart|Beschreibung|  
|------------------|---------------------------------------|  
|EING|Artikel, die empfangen, aber nicht eingelagert werden.|  
|AUSG|Artikel, die für Warenausgangszeilen kommissioniert, aber nicht als Warenausgang gebucht wurden.|  
|EINLAG|Normalerweise werden hier Artikel in großen Einheiten eingelagert, die jedoch nicht für die Kommissionierung verwendet werden soll. Diese Lagerplätze werden nicht für die Kommissionierung verwendet, weder für Produktionsaufträge noch für Lieferungen, sodass ihre Verwendung möglicherweise eingeschränkt ist. Diese Art von Lagerplatz ist nützlich, wenn Sie eine große Menge an Artikeln kaufen. Die Lagerplätze sollten immer einen niedrigen Lagerplatzrang haben, damit Artikel mit höherrangigen PUTPICK-Lagerplätzen zuerst eingelagert werden. Füllen Sie diese Art von Lagerplätzen regelmäßig auf, damit ihre Artikel in den Lagerplätzen des Typs PUTPICK oder PICK verfügbar sind.|  
|KOMMISS|Nur für Kommissionierung zu verwendende Artikel. Sie können Bewegungen nur zur Auffüllung dieser Lagerplätze verwenden, nicht für Einlagerungen.|  
|EINLAGKOMM|Artikel an Lagerplätzen, die für Einlagerung und Kommissionierung vorgeschlagen werden. Lagerplätze dieser Art haben wahrscheinlich unterschiedliche Lagerplatzprioritäten. Richten Sie Ihre Palettenlagerplätze mit geringerer Lagerplatzbewertung als normale Kommissionierungslagerplätze oder Lagerplätze in Ihren bevorzugten Kommissionierungsbereichen ein.|  
|QK|Dieser Lagerplatz wird für einen Ausgleich von Lagerbestand verwendet, wenn Sie diesen Lagerplatz auf der Lagerortkarte im Feld **Ausgleichlagerplatzcode** angeben. Sie können Lagerplätze dieser Art auch für beschädigte Artikel und Artikel, die für Qualitätskontrollen verwendet werden, einrichten. Sie können Artikel in diese Art von Lagerplätzen umlagern, wenn Sie möchten, dass diese für den normalen Warenfluss nicht zugänglich sein sollen. **HINWEIS:**  Anders als alle anderen Lagerplatzarten hat die Lagerplatzart **QK** keine standardmäßig aktivierten Kontrollkästchen für die Behandlung. Inhalt, den Sie an einem QC-Lagerplatz platzieren, ist aus den Artikelströmen ausgeschlossen.|  

Mit Ausnahme der Lagerplatztypen KOMMISSIONIERUNG, EINLAGKOMM und EINLAGERUNG definiert die Lagerplatzart die für einen Lagerplatz zulässige Aktivität. Beispiel: Sie können einen Lagerplatz des Typs EINGANG nur dazu verwenden, um Artikel zu empfangen oder zu kommissionieren.  

> [!NOTE]  
> Sie müssen Verschiebungen verwenden, um Artikel an EMPFANGS- und QC-Lagerplätze zu verschieben. Verwenden Sie Bewegungen, um Artikel aus VERSAND- und QC-Lagerplätzen zu verschieben.  

#### <a name="bin-ranking" />Lagerplatzpriorität

In der erweiterten Lagerhaltung können Sie automatisieren und optimieren, wie Artikel in Einlagerungs- und Kommissionierungsarbeitsblättern den gesammelt werden, indem Sie Lagerplätze bewerten. Artikel werden gemäß der Lagerplatzbewertungen für Kommissionierung und Einlagerung empfohlen.

Die Einlagerungsabläufe werden nach Lagerplatzprioritäten optimiert , indem Lagerplätze mit höherer Bewertung vor Lagerplätzen mit niedriger Bewertung vorgeschlagen werden. Kommissionierungsabläufe schlagen Artikel mit höherer Lagerplatzbewertung aus Lagerplatzinhalt zuerst vor. Lagerplatzauffüllung schlägt Lagerplätze mit niedrigerem Rang vor Lagerplätzen mit höherem Rang vor.  

Lagerplatzrang und Lagerplatzinhalt sind die grundlegenden Eigenschaften, die Lagermitarbeiter im Lager leiten.  

#### <a name="bin-setup" />Lagerplatz-Setup

Bei der erweiterten Lagerhaltung können Sie die folgenden Kapazitätswerte angeben, um zu steuern, wie und in welchen Lagerplätzen Sie Artikel lagern:

* Menge
* Gesamtkubatur
* Gewichtung  

Sie können Artikeln eine Basiseinheit (UOM) zuweisen. Eine Basiseinheit kann aus Stücken, Paletten, Litern, Gramm oder Kartons bestehen. Sie können auch größere Maßeinheit basierend auf Ihrer Basiseinheit erstellen. Wenn beispielsweise Stücke Ihre Basiseinheit sind, kann eine Palette 16 Stück entsprechen.  

Wenn ein Artikel mehr als eine Maßeinheit hat, legen Sie die maximale Menge für jede Maßeinheit auf der Artikelkarte fest. Wenn Sie einen Artikel nach Stück und Paletten bearbeiten, muss das **Maximale Menge**-Feld auf der Seite **Lagerplatz-Inhalt** für diesen Artikel ebenfalls nach Stück und Paletten organisiert sein. Andernfalls wird die zulässige Menge für diesen Lagerplatz nicht korrekt berechnet.  

Bevor Sie Kapazitätseinschränkungen für Lagerplatzinhalte an einem Lagerplatz einrichten, stellen Sie sicher, ob die Mengeneinheit und die Dimensionen des Artikels auf dem Artikel eingerichtet wurden.  

> [!NOTE]  
> Sie können mehrere Maßeinheiten nur an Standorten verwenden, die eine gesteuerte Einlagerung und Entnahme verwenden. In allen anderen Konfigurationen können Sie nur Lagerplatzinhalte in der Basiseinheit verwenden. In Transaktionen mit einer Maßeinheit, die größer als die Basiseinheit des Artikels ist, wird die Menge in die Basiseinheit umgewandelt.  

#### <a name="zone" />Servicegebiet

In der erweiterten Lagerhaltung können Lagerplätze in Zonen gruppiert werden, um den Workflow der Lageraktivitäten für Lagerorte zu verwalten.  

Eine Zone kann eine empfangende Zone oder eine Lagerzone sein, und jede Zone kann aus einem oder mehreren Lagerplätzen bestehen.  

Die meisten Eigenschaften, die einer Zone zugeordnet sind, werden Lagerplätzen zugeordnet, die aus dieser Zone erstellt werden.  

#### <a name="warehouse-class" />Lagerklasse

In der erweiterten Lagerhaltung können Sie den folgenden Entitäten Lagerklassencodes zuweisen: 

* Artikel
* Lagerplätze
* Zonen

Warehouse-Klassen steuern, wo Artikel gelagert werden. Sie können eine Zone in mehrere Lagerklassen aufteilen. Beispielsweise lagern Sie Artikel möglicherweise in der empfangenden Zone als eingefroren, gefährlich oder einer anderen Klasse zugehörig.

Wenn Sie mit Lagerklassen und standardmäßigen Empfangs-/Versandlagerplätzen arbeiten, müssen Sie die entsprechenden Lagerplätze im Wareneingang und in den Lieferzeilen manuell auswählen.  

In eingehenden Flüssen wird der Klassencode nur auf eingehenden Zeilen hervorgehoben, auf denen der Artikelklassencode nicht dem standardmäßigen Wareneingangslagerplatz entspricht. Wenn die richtigen Standardlagerplätze nicht zugewiesen werden, kann die Menge nicht empfangen werden.  

#### <a name="location" />Lagerort

Ein Lagerort ist eine physische Struktur oder ein Ort, an dem Bestand empfangen, gelagert und versandt wird. Ein Lagerort kann ein Lager, ein Servicefahrzeug, ein Ausstellungsraum, eine Fabrik oder ein Bereich in einer Fabrik sein. Bestand wird oft in Lagerplätzen und Zonen organisiert.

#### <a name="first-expired-first-out" />Ausgang nach frühestem Ablaufdatum

Wenn Sie das Kontrollkästchen **Gemäß FEFO kommissionieren** im Inforegister **Lagerplatzprüfung** auf der Seite **Lagerortkarte** wählen, werden Artikel mit Artikelverfolgung entsprechend ihrem Ablaufdatum an dem Lagerort kommissioniert. Artikel mit den frühesten Ablaufdaten werden zuerst kommissioniert.  

Lageraktivitäten in allen Kommissionierungs- und Umlagerungsdokumenten werden gemäß FEFO sortiert, es sei denn, der Artikel ist eine Serien- oder Chargennummer zugeordnet. Wenn ein Teil aber nicht die gesamte Menge auf der Zeile Chargen oder Seriennummern zugewiesen sind, wird die verbleibende Menge nach dem FEFO-Prinzip sortiert.  

Bei der Kommissionierung über FEFO wählt die Anwendung Artikel auf der Grundlage des Ablaufdatums aus; das Ergebnis ist eine temporäre Artikelverfolgungsliste, die auf dem Ablaufdatum basiert. Weisen zwei Artikel dasselbe Ablaufdatum aus, wählt die Anwendung den Artikel mit der niedrigeren Chargen- oder Seriennummer zuerst aus. Sind die Chargen- oder Seriennummern identisch, wählt die Anwendung den Artikel aus, der zuerst ausgewählt wurde. Die Standardkriterien für die Auswahl der Artikel in Kommissionierungslagerplätzen, wie z. B. nach Lagerplatzpriorität und Gebindeanbruch, werden auf diese temporäre FEFO-Artikelverfolgungsliste angewendet.  

#### <a name="put-away-template" />Einlagerungsvorlage

Einlagerungsvorlagen geben einen Satz priorisierter Regeln an, die gelten,wenn Sie Einlagerungen erstellen. Beispielsweise kann eine Einlagerungsvorlage erfordern, dass Sie Artikel in einen Lagerplatz mit Lagerplatzinhalt legen, der dieselbe Maßeinheit hat. Wenn kein ähnlicher Lagerplatz mit ausreichender Kapazität gefunden werden kann, muss der Artikel an einen leeren Lagerplatz gelegt werden. Sie weisen eine Einlagerungsvorlage einem Artikel und einem Lagerort zu.  

## <a name="see-related-microsoft-training" />Siehe verwandte [Microsoft Schulungen](/training/modules/get-started-warehouse-management/)

## <a name="see-also" />Siehe auch

[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
