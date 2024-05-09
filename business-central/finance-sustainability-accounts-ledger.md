---
title: Diagramm der Nachhaltigkeitskonten und Nachhaltigkeitssachkonto
description: 'Erfahren Sie, wie Sie das Diagramm der Nachhaltigkeitskonten, -kategorien und -unterkategorien verwalten und Details zu Nachhaltigkeitsposten abrufen.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Diagramm der Nachhaltigkeitskonten und Nachhaltigkeitssachkonto 

## Diagramm der Nachhaltigkeitskonten  

Das **Diagramm der Nachhaltigkeitskonten** (CoSA) bildet die grundlegende strukturierte Liste, die zur Erfassung aller Emissionsdaten verwendet wird. Es fungiert als Rahmen, der Nachhaltigkeitskonten anhand ihrer Attribute, wie Scope oder anderen Gruppierungen, kategorisiert und organisiert. Jedem Konto wird normalerweise zur einfachen Bezugnahme und Nachverfolgung ein eindeutiger Code oder eine eindeutige Nummer zugewiesen, wobei die gleiche Struktur wie bei einem herkömmlichen **Kontenplan** verwendet, diese jedoch speziell an die Überwachung nachhaltigkeitsbezogener Daten und Kennzahlen innerhalb einer Organisation angepasst wird. 
 
Benutzende können **Kontokategorien** und **-unterkategorien** hinzufügen, um das Verhalten des Systems zu bestimmen, indem sie spezielle Emissionen zur Nachverfolgung, Emissionsfaktoren, Formeln und ähnliche Konfigurationen auswählen.  

>[!NOTE]
>Um Sie mit den Scopes vertraut zu machen: Basierend auf den THG-Standards (Treibhausgase) gibt es drei Emissions-Scopes:  
>- **Umfang-1-Emissionen**: umfassen Emissionen, die aus der stationären und mobilen Verbrennung stammen, sowie aus unbeabsichtigten flüchtigen Emissionen. 
>- **Bereich-2-Emissionen** enthalten indirekte Emissionen aus der Energieerzeugung, die von Versorgungsunternehmen bezogen wird. 
>- **Scope-3-Emissionen**: umfassen ein breites Spektrum an Emissionen, von gekauften Waren und Dienstleistungen und Investitionsgütern, kraftstoff- und energiebezogenen Aktivitäten, vor- und nachgelagerten Transporten, erzeugtem Abfall, Geschäftsreisen und Pendelverkehr der Mitarbeitenden usw. 

Vom **Diagramm der Nachhaltigkeitskonten** (CoSA) aus können Sie zum Beispiel Folgendes tun:  

-   Berichte ansehen, die die Nachhaltigkeitsposten und -salden zeigen. 
-   Die **Nachhaltigkeitskontokarte** öffnen, um Einstellungen hinzuzufügen oder zu ändern.  
-   Sich die Kategorie und Unterkategorie für dieses Konto anzeigen lassen.   
-   Separate Salden für jede der Emissionen für ein einzelnes Konto anzeigen. 
-   Jedem Konto eine oder mehrere **Dimensionen** hinzufügen und einen Dimensionsfilter festlegen. 
    
Sie können **Nachhaltigkeitskonten** hinzufügen, ändern oder löschen. Um Unstimmigkeiten zu vermeiden, können Sie jedoch ein **Nachhaltigkeitskonto** nicht löschen, wenn mit diesem Konto ein oder mehrere Posten verknüpft sind.  

### Hinzufügen oder Ändern von Konten  

1. Wählen Sie das ![Glühbirne, öffnet die „Wie möchten Sie weiter verfahren“-Funktion 3.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Diagramm der Nachhaltigkeitskonten** ein und wählen Sie dann den zugehörigen Link. 
2. Auf der Seite **Diagramm der Nachhaltigkeitskonten** (CoSA) können Sie jedes **Nachhaltigkeitskonto** öffnen und dann Einstellungen hinzufügen oder ändern. Fahren Sie über ein Feld, um eine Kurzbeschreibung zu lesen. 

Für Konten der Art **Summe** müssen Sie das Feld **Zusammenzählung** ausfüllen. Für Konten der Art **Bis-Summe** wird dieses Feld automatisch durch die Funktion "Einrückung des Kontenplans" ausgefüllt. Nachdem Sie alle Konten festgelegt haben, wählen Sie dafür die Aktion **Diagramm der Nachhaltigkeitskonten einrücken** aus.  

>[!IMPORTANT]
>Wenn Sie vor dem Ausführen der Funktion Einrücken Definitionen in den Feldern **Summe** für **Endsumme** Konten eingegeben haben, müssen Sie diese erneut eingeben, da die Funktion die Werte in allen **Endsumme** Feldern überschreibt.  

### Konten löschen  

Sie können ein **Nachhaltigkeitskonto** löschen. Bevor Sie es löschen, müssen Sie jedoch sicherstellen, dass ein oder mehrere Posten mit diesem Konto verknüpft sind, da Business Central Sie in diesem Fall daran hindert, ein **Nachhaltigkeitskonto** zu löschen.  

## Kontokategorien   

Benutzende müssen die **Kategorie des Nachhaltigkeitskontos** für jedes **Nachhaltigkeitskonto** hinzufügen, um das Verhalten des Systems festzulegen, Emissionsscopes, dedizierte Emissionen zur Nachverfolgung, Formeln und ähnliche Konfigurationen auszuwählen.  

Um die **Kategorien des Nachhaltigkeitskontos** zu überprüfen, gehen Sie wie folgt vor: 

1.  Wählen Sie das ![Glühbirne, öffnet die „Wie möchten Sie weiter verfahren“-Funktion 3.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Kategorien des Nachhaltigkeitskontos** ein und wählen Sie dann den zugehörigen Link. 
2.  Auf der Seite **Kategorien des Nachhaltigkeitskontos** können Sie die vorhandene Liste bearbeiten oder eine neue Kategorie erstellen. Um eine neue Kategorie zu erstellen, wählen Sie die Aktion **Neu**.  
3.  Füllen Sie die Felder **Code** und **Beschreibung** aus.   
4.  Richten Sie das Feld **Emissionsscope** ein, indem Sie eine der Scopeoptionen auswählen.  
5.  Wählen Sie die Gasemissionen aus, die Sie nachverfolgen möchten. Derzeit können Sie eine der folgenden Optionen verwenden: **CO2**, **CH4** oder **N2O**. Sie können jede beliebige Kombination auswählen, die Sie nachverfolgen möchten, müssen aber über mindestens eine Emission zur Nachverfolgung verfügen.  
6.  Im Feld **Berechnungsgrundlage** können Sie eine der Formeln auswählen, die Sie verwenden möchten, falls Sie die genaue Emissionsmenge nicht kennen. Hier geben Sie die Berechnungsgrundlage (Formel) für die Emissionsberechnung an. Sie können eine der folgenden Optionen auswählen: **Kraftstoff/Strom**, **Entfernung**, **Installation** oder **Benutzerdefiniert**. 
7.  Wenn Sie die **Benutzerdefinierte** Formel auswählen, können Sie im Feld **Benutzerdefinierter Wert** eine benutzerdefinierte Beschreibung konfigurieren.  

>[!NOTE]
>Wenn die im Feld **Berechnungsgrundlage** angebotenen Formeln nicht ausreichen, können Sie dieses Feld erweitern und dem System weitere Berechnungen hinzufügen, die in den **Nachhaltigkeits-Buch.-Blättern** verwendet werden können.  

Wenn Sie die **Berechnungsgrundlage** (Formeln) verwenden, gibt es eine Erklärung, wie das System die Berechnung basierend auf der von Ihnen gewählten Option vornimmt (**EF** ist der **Emissionsfaktor**, den Sie auf der Seite **Unterkategorien des Nachhaltigkeitskontos** konfigurieren können): 

|  Emissionsart  |  Berechnungsgrundlage  |  Formel         | Kommentar      |
|------------|--------------|------------------------------|---------------------------------|
| **SCOPE 1**  |
| Stationäre Verbrennung | Treibstoff/Strom | Emission = Kraftstoff * EF | _d. h. Kraftstoff = Menge des für Kessel, Heizungen, thermische Oxidationsanlagen usw. verbrauchten Brennstoffs._ |
| Mobile Verbrennung | Treibstoff/Strom | Emission = Kraftstoff * EF | _d. h. Kraftstoff = Menge an Kraftstoff, die für Straßenfahrzeuge, Geländefahrzeuge, Schienenfahrzeuge usw. verbraucht wird._ |
|  |  |  Emissionen = Entfernung * EF | _d. h. Entfernung = von Straßen- oder Geländefahrzeugen, Schienenverkehr usw. gefahrene Kilometer_ |
| Flüchtige Emissionen | Installation | Emission = Installationsmultiplikator * benutzerdefinierte Menge/100 * Zeitfaktor | _d. h. benutzerdefinierte Menge = Montageverluste, jährliche Leckrate usw._ |
| **SCOPE 2**  |
| Versorgungsunternehmen | Treibstoff/Strom | Emissionen = Strom * EF | _d. h. Kraftstoff/Strom = Strommenge, Dampfmenge, Heizeinheit usw._ |
|  | Benutzerdefiniert | Emission = Benutzerdefinierte Menge * EF | _d. h. benutzerdefinierte Menge = Kilomwatt, Kilowattstunde usw._ |
| **SCOPE 3**  |
| Gekaufte Waren und Dienstleistungen sowie Investitionsgüter | Benutzerdefiniert | Emission = Benutzerdefinierte Menge * EF | _d. h., benutzerdefinierte Menge = Kosten (Finanzbuchhaltung) usw._ |
| Upstream-Transport und -Vertrieb | Entfernung | Emissionen = Entfernung * EF |  |
|  | Entfernung | Emissionen = Entfernung * Multiplikator * EF | _Multiplikator = Tonnen Fracht_ |
| Downstream-Transport und -Vertrieb | Entfernung | Emissionen = Entfernung * EF |  |
|  | Entfernung | Emissionen = Entfernung * Multiplikator * EF | _Multiplikator = Tonnen Fracht_ |
| Abfälle aus dem Betrieb und der Entsorgung verkaufter Produkte | Benutzerdefiniert | Emission = Benutzerdefinierte Menge * EF | _d. h., benutzerdefinierte Menge = Abfall_ |
| Geschäftsreisen und Pendeln von Mitarbeitenden | Entfernung | Emissionen = Entfernung * EF | _d. h. Entfernung = vom genutzten Firmenwagen, Mietwagens, Zugs, Flugs usw. zurückgelegte Kilometer_ |
|  | Benutzerdefiniert | Emission = Benutzerdefinierte Menge * EF | _d. h. benutzerdefinierter Betrag = Hotelaufenthalte usw._ |
|  | Treibstoff/Strom | Emission = Kraftstoff * EF | _d. h. Kraftstoff = Menge an Kraftstoff, die im Firmenwagen, Mietwagen usw. verbraucht wird_ |

## Kontounterkategorien  

Benutzende müssen die **Unterkategorie des Nachhaltigkeitskontos** zu jedem der **Nachhaltigkeitskonten** hinzufügen, um Emissionsfaktoren festzulegen, die in den Formeln verwendet werden. Sie basiert jedoch auf der in der **Kategorie des Nachhaltigkeitskontos** zur Nachverfolgung ausgewählten Kategorie.  

Um die **Unterkategorien des Nachhaltigkeitskontos** zu überprüfen, gehen Sie wie folgt vor:  

1.  Wählen Sie das ![Glühbirne, öffnet die „Wie möchten Sie weiter verfahren“-Funktion 3.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Unterkategorien des Nachhaltigkeitskontos** ein und wählen Sie dann den zugehörigen Link. 
2.  Auf der Seite **Unterkategorien des Nachhaltigkeitskontos** können Sie die vorhandene Liste bearbeiten oder eine neue Kategorie erstellen. Um eine neue Kategorie zu erstellen, wählen Sie die Aktion **Neu**.  
3.  Füllen Sie die Felder **Code** und **Beschreibung** aus.   
4.  Basierend auf den Gasemissionen, die Sie in der **Kategorie des Nachhaltigkeitskontos** nachverfolgen möchten und mit denen Sie diese Unterkategorie verknüpfen, können Sie auch einen oder mehrere Emissionsfaktoren angeben: 

   - **Emissionsfaktor CO2**: Gibt einen Emissionsfaktor für die CO2-Emissionen an.  
   - **Emissionsfaktor CH4**: Gibt einen Emissionsfaktor für die CH4-Emissionen an. 
   - **Emissionsfaktor N2O**: Gibt einen Emissionsfaktor für die N2O-Emissionen an.  

5.  Wenn diese Unterkategorie mit erneuerbaren Energien zusammenhängt, wählen Sie das Feld **Erneuerbare Energie** aus.   

>[!NOTE]
>Die Felder **Daten importieren** und **Importieren von** sind für eine mögliche Integration mit externen Systemen vorgesehen, die zur Erfassung von Emissionsfaktoren verwendet werden. In **1. Veröffentlichungszyklus 2024** können sie jedoch standardmäßig nicht als Feature verwendet werden.  

## Nachhaltigkeitsposten  

Das **Nachhaltigkeitssachkonto** speichert den Verlauf aller gebuchten Nachhaltigkeitstransaktionen und organisiert alle Emissionsdaten gemäß dem **Diagramm der Nachhaltigkeitskonten**. Wenn Benutzende das **Nachhaltigkeits-Buch.-Blatt** buchen, werden dort alle wichtigen Daten erfasst. Alle aktiven Berichte werden auf Basis der **Nachhaltigkeitsposten** generiert.   

Benutzende können dieses Sachkonto für ein bestimmtes Konto mit der Aktion **Posten** auf der Seite **Diagramm des Nachhaltigkeitskontos** öffnen oder, um alle Posten zu öffnen, das ![Glühbirne, welche das Feature „Sie wünschen ...“ 3 öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol auswählen, **Nachhaltigkeitsposten** eingeben und den zugehörigen Link auswählen. Fahren Sie über ein Feld, um eine Kurzbeschreibung zu lesen.  

>[!IMPORTANT]
>Sobald Sie Ihre Daten in das Nachhaltigkeitssachkonto gebucht haben, können Sie sie nicht mehr löschen. Falls Ihnen ein Fehler unterläuft, können Sie die Rückbuchung mit den gleichen Angaben, aber mit dem Minuszeichen für den Betrag buchen.  

## Siehe auch  
[Finanzen](finance.md)    
[Nachhaltigkeitsverwaltung – Übersicht](finance-manage-sustainability.md)
[Nachhaltigkeitseinrichtung](finance-sustainability-setup.md)
[Vorgehensweise: Erfassen von Emissionen](finance-sustainability-journal.md)
[Mit [!INCLUDE[prod_short](includes/prod_short.md)] arbeiten](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
