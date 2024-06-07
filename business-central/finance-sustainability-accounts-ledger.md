---
title: Diagramm der Nachhaltigkeitskonten und des Sachkontos
description: 'Erfahren Sie, wie Sie den Nachhaltigkeitskontenplan (CoSA), Nachhaltigkeitskategorien und -unterkategorien verwalten und Details zu Nachhaltigkeitsposten abrufen.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Nachhaltigkeitskontenplan und Nachhaltigkeitssachkonto

## Nachhaltigkeitskontenplan

Der Nachhaltigkeitskontenplan (CoSA) bildet die grundlegende strukturierte Liste, mit der alle Emissionsdaten erfasst werden. Er dient als Rahmen, der Nachhaltigkeitskonten anhand ihrer Attribute, wie Scope oder anderen Gruppierungen, kategorisiert und organisiert. Jedem Konto wird normalerweise ein eindeutiger Code oder eine eindeutige Nummer zugewiesen, um einfach darauf verweisen oder es nachverfolgen zu können. Er hat die gleiche Struktur wie ein herkömmlicher Kontenplan, ist jedoch speziell auf die Überwachung von Daten und Kennzahlen rund um das Thema Nachhaltigkeit in einer Organisation zugeschnitten.

Benutzende können Nachhaltigkeitskontokategorien und -unterkategorien hinzufügen, um das Verhalten des Systems zu bestimmen. So können sie bestimmte nachzuverfolgende Emissionen sowie Emissionsfaktoren, Formeln und ähnliche Konfigurationen auswählen.

> [!NOTE]
> Ausgehend von den Treibhausgasstandards (THG-Standards) gibt es drei Emissionsscopes:
>
> - **Scope-1-Emissionen**: umfassen Emissionen, die aus der stationären und mobilen Verbrennung stammen, sowie aus unbeabsichtigten flüchtigen Emissionen.
> - **Scope-2-Emissionen** enthalten indirekte Emissionen aus der Energieerzeugung, die von Versorgungsunternehmen bezogen wird.
> - **Scope-3-Emissionen** umfassen ein breites Spektrum an Emissionen, von gekauften Waren und Dienstleistungen und Investitionsgütern, über kraftstoff- und energiebezogenen Aktivitäten, vor- und nachgelagerte Transporte, bis zu erzeugtem Abfall, Geschäftsreisen und Pendelverkehr der Mitarbeitenden usw.

Vom CoSA aus können Sie beispielsweise Folgendes tun:

- Berichte ansehen, die die Nachhaltigkeitsposten und -salden zeigen.
- Die Nachhaltigkeitskontokarte öffnen, um Einstellungen hinzuzufügen oder zu ändern.
- Sich die Kategorie und Unterkategorie für das Konto anzeigen lassen. 
- Separate Salden für jede Emission für ein einzelnes Konto anzeigen.
- Jedem Konto eine oder mehrere Dimensionen hinzufügen und Dimensionsfilter festlegen.

Sie können Nachhaltigkeitskonten hinzufügen, ändern oder löschen. Um Unstimmigkeiten zu vermeiden, können Sie ein Nachhaltigkeitskonto jedoch nicht löschen, wenn ein oder mehrere Posten damit verknüpft sind.

### Hinzufügen oder Ändern von Konten

1. Wählen Sie das ![Glühbirne, welche die 3. „Sie wünschen ...“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Nachhaltigkeitskontoplan** ein und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Nachhaltigkeitskontenplan** können Sie jedes Nachhaltigkeitskonto öffnen und dann Einstellungen hinzufügen oder ändern. Fahren Sie über ein Feld, um eine Kurzbeschreibung zu lesen.

Für Konten der Art **Summe** müssen Sie das Feld **Zusammenzählung** festlegen.

Bei Konten der Art **Bis-Summe** wird das Feld **Zusammenzählung** automatisch durch die Einrücken-Funktion festgelegt. Nachdem Sie alle Konten eingerichtet haben, wählen Sie die Aktion **Nachhaltigkeitskontenplan einrücken** aus, um die Einrücken-Funktion auszuführen und das Feld **Zusammenzählung** festzulegen.

> [!IMPORTANT]
> Die Einrücken-Funktion überschreibt den Wert aller Felder für Konten vom Typ **Bis-Summe**. Wenn Sie Definitionen im Feld **Zusammenzählung** für Konten vom Typ **Bis-Summe** eingegeben haben, bevor Sie die Einrücken-Funktion ausführen, müssen Sie sie daher noch dem Ausführen noch einmal eingeben.

### Konten löschen

Sie können ein Nachhaltigkeitskonto löschen. Allerdings müssen Sie zunächst sicherstellen, dass keine Posten damit verknüpft sind. Business Central lässt Sie ein Nachhaltigkeitskonto jedoch nicht löschen, wenn ein oder mehrere Posten damit verknüpft sind.

## Kontokategorien

Benutzende müssen jedem Nachhaltigkeitskonto eine Nachhaltigkeitskontokategorie hinzufügen, um das Verhalten des Systems zu bestimmen. Sie können Emissionsscopes, bestimmte nachzuverfolgende Emissionen, Formeln und ähnliche Konfigurationen auswählen.

Um die Nachhaltigkeitskontokategorien zu überprüfen, gehen Sie wie folgt vor:

1. Wählen Sie das ![Glühbirne, öffnet die „Wie möchten Sie weiter verfahren“-Funktion 3.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Kategorien des Nachhaltigkeitskontos** ein und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Kategorien des Nachhaltigkeitskontos** können Sie die vorhandene Liste bearbeiten oder eine neue Kategorie erstellen. Um eine neue Kategorie zu erstellen, wählen Sie die Aktion **Neu** aus.
3. Legen Sie die Felder **Code** und **Beschreibung** fest.
4. Wählen Sie im Feld **Emissionsscope** eine der Scopeoptionen aus.
5. Wählen Sie die Gasemissionen aus, die Sie nachverfolgen möchten. Die folgenden Optionen stehen zur Verfügung: **CO2**, **CH4** und **N2O**. Sie können jede beliebige Kombination auswählen, die Sie nachverfolgen möchten, müssen aber mindestens eine Emission auswählen.
6. Im Feld **Berechnungsgrundlage** können Sie die Berechnungsgrundlage (Formel) für die Emissionsberechnung auswählen, wenn Sie die genaue Emissionsmenge nicht kennen. Sie können eine der folgenden Optionen auswählen: **Kraftstoff/Strom**, **Entfernung**, **Installation** oder **Benutzerdefiniert**.

    > [!NOTE]
    > Wenn die im Feld **Berechnungsgrundlage** angebotenen Formeln nicht ausreichen, können Sie das Feld erweitern und dem System weitere Berechnungen hinzufügen, die in den Nachhaltigkeits-Buch.-Blättern verwendet werden können.

7. Wenn Sie im Feld **Berechnungsgrundlage** die Option **Benutzerdefiniert** festlegen, können Sie eine benutzerdefinierte Beschreibung im Feld **Benutzerdefinierter Wert** eingeben.

Wenn Sie das Feld **Berechnungsgrundlage** festlegen, können Sie der folgenden Tabelle entnehmen, wie das System die Emissionen basierend auf der von Ihnen ausgewählten Option berechnet. (In dieser Tabelle steht *EF* für den Wert **Emissionsfaktor**, den Sie auf der Seite **Unterkategorie des Nachhaltigkeitskontos** konfiguriert haben.)

| Emissionsart | Berechnungsgrundlage | Formel | Kommentar |
|---------------|------------------------|---------|---------|
| **Bereich 1** | | | |
| Stationäre Verbrennung | Treibstoff/Strom | *Emission* = *Kraftstoff* &times; *EF* | *Kraftstoff* = Menge des für Kessel, Heizungen, thermische Oxidationsanlagen usw. verbrauchten Brennstoffs |
| Mobile Verbrennung | Treibstoff/Strom | *Emission* = *Kraftstoff* &times; *EF* | *Kraftstoff* = Menge an Kraftstoff, die für Straßenfahrzeuge, Geländefahrzeuge, Schienenfahrzeuge usw. verbraucht wird |
| | | *Emissionen* = *Entfernung* &times; *EF* | *Entfernung* = von Straßen- oder Geländefahrzeugen, Schienenverkehr usw. gefahrene Kilometer |
| Flüchtige Emissionen | Installation | *Emission* = *Installationsmultiplikator* &times; *benutzerdefinierte Menge* &divide; 100 &times; *Zeitfaktor* | *Benutzerdefinierte Menge* = Montageverluste, jährliche Leckrate usw. |
| **Bereich 2** | | | |
| Versorgungsunternehmen | Treibstoff/Strom | *Emissionen* = *Strom* &times; *EF* | *Kraftstoff/Strom* = Strommenge, Dampfmenge, Heizeinheit usw. |
| | Benutzerdefiniert | *Emissionen* = *Benutzerdefinierte Menge* &times; *EF* | *Benutzerdefinierte Menge* = Kilowatt, Kilowattstunde usw. |
| **Bereich 3** | | | |
| Gekaufte Waren und Dienstleistungen sowie Investitionsgüter | Benutzerdefiniert | *Emissionen* = *Benutzerdefinierte Menge* &times; *EF* | *Benutzerdefinierte Menge* = Kosten (Finanzbuchhaltung) usw. |
| Upstream-Transport und -Vertrieb | Entfernung | *Emissionen* = *Entfernung* &times; *EF* | |
| | Entfernung | *Emissionen* = *Entfernung* &times; *Multiplikator* &times; *EF* | *Multiplikator* = Tonnen Fracht |
| Downstream-Transport und -Vertrieb | Entfernung | *Emissionen* = *Entfernung* &times; *EF* | |
| | Entfernung | *Emissionen* = *Entfernung* &times; *Multiplikator* &times; *EF* | *Multiplikator* = Tonnen Fracht |
| Abfälle aus dem Betrieb und der Entsorgung verkaufter Produkte | Benutzerdefiniert | *Emissionen* = *Benutzerdefinierte Menge* &times; *EF* | *Benutzerdefinierte Menge* = Abfall |
| Geschäftsreisen und Pendeln von Mitarbeitenden | Entfernung | *Emissionen* = *Entfernung* &times; *EF* | *Entfernung* = vom genutzten Firmenwagen, Mietwagen, Zug, Flug usw. zurückgelegte Kilometer |
| | Benutzerdefiniert | *Emissionen* = *Benutzerdefinierte Menge* &times; *EF* | *Benutzerdefinierter Betrag* = Hotelaufenthalte |
| | Treibstoff/Strom | *Emission* = *Kraftstoff* &times; *EF* | *Kraftstoff* = Menge an Kraftstoff, die im Firmenwagen, Mietwagen usw. verbraucht wird |

## Kontounterkategorien

Benutzende müssen jedem Nachhaltigkeitskonto eine Nachhaltigkeitskontounterkategorie hinzufügen. Diese Unterkategorie legt die Emissionsfaktoren fest, die in den Formeln verwendet werden und auf der zur Emissionsnachverfolgung als Nachhaltigkeitskontokategorie ausgewählten Option beruhen.

Um die Unterkategorien des Nachhaltigkeitskontos zu überprüfen, gehen Sie wie folgt vor:

1. Wählen Sie das ![Glühbirne, öffnet die „Wie möchten Sie weiter verfahren“-Funktion 3.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Unterkategorien des Nachhaltigkeitskontos** ein und wählen Sie dann den zugehörigen Link. 
2. Auf der Seite **Unterkategorien des Nachhaltigkeitskontos** können Sie die vorhandene Liste bearbeiten oder eine neue Kategorie erstellen. Um eine neue Kategorie zu erstellen, wählen Sie die Aktion **Neu** aus.
3. Legen Sie die Felder **Code** und **Beschreibung** fest.
4. Basierend auf den Gasemissionen, die Sie in der Kategorie des Nachhaltigkeitskontos nachverfolgen möchten und mit denen Sie diese Unterkategorie verknüpfen, können Sie auch einen oder mehrere Emissionsfaktoren festlegen: 

    - **Emissionsfaktor CO2**: Der Emissionsfaktor für Kohlendioxidemissionen (CO<sub>2</sub>).
    - **Emissionsfaktor CH4**: Der Emissionsfaktor für Methanemissionen (CH<sub>4</sub>)
    - **Emissionsfaktor N2O**: Der Emissionsfaktor für Lachgasemissionen (N<sub>2</sub>O).

5. Wenn die Unterkategorie mit erneuerbaren Energien zusammenhängt, wählen Sie das Feld **Erneuerbare Energie** aus.

> [!NOTE]
> Die Felder **Daten importieren** und **Importieren von** sind für eine mögliche Integration mit externen Systemen vorgesehen, die zur Erfassung von Emissionsfaktoren verwendet werden. Im **1. Veröffentlichungszyklus 2024** können diese Felder jedoch nicht standardmäßig als Feature verwendet werden.

## Nachhaltigkeitsposten

Das Nachhaltigkeitssachkonto speichert den Verlauf aller gebuchten Nachhaltigkeitstransaktionen und organisiert alle Emissionsdaten gemäß dem CoSA. Wenn Benutzende das Nachhaltigkeits-Buch.-Blatt buchen, werden dort alle wichtigen Daten erfasst. Alle aktiven Berichte werden auf Basis der Nachhaltigkeitsposten generiert.

Um dieses Sachkonto für ein bestimmtes Konto zu öffnen, verwenden Sie die Aktion **Posten** auf der Seite **Nachhaltigkeitskontenplan**. Um alle Posten zu öffnen, wählen Sie das ![Glühbirne, welche die 3. „Sie wünschen ...“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol aus, geben Sie **Nachhaltigkeitsposten** ein und wählen Sie den dazugehörigen Link aus. Fahren Sie über ein Feld, um eine Kurzbeschreibung zu lesen.

> [!IMPORTANT]
> Nachdem Sie Ihre Daten in das Nachhaltigkeitssachkonto gebucht haben, können Sie sie nicht mehr löschen. Falls Ihnen ein Fehler unterläuft, können Sie die Rückbuchung mit den gleichen Angaben, aber mit dem Minuszeichen vor dem Betrag buchen.

## Siehe auch

[Finanzen](finance.md)  
[Nachhaltigkeitsmanagement – Überblick](finance-manage-sustainability.md)  
[Nachhaltigkeitseinrichtung](finance-sustainability-setup.md)  
[Vorgehensweise: Erfassen von Emissionen](finance-sustainability-journal.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
