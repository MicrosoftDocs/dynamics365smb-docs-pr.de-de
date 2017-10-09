---
title: Arbeiten mit Dimensionen | Microsoft Docs
description: "Sie können Dimensionen nutzen, um Einträge zu kategorisieren, beispielsweise nach Abteilungen oder Projekt, sodass Sie können Daten einfacher verfolgen und analysieren."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/14/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 844668124df1897493737b28383a68a2a0a66d10
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="working-with-dimensions"></a>Arbeiten mit Dimensionen
Um Analyse in Belegen wie Verkaufsaufträgen einfacher durchzuführen, können Sie Dimensionen verwenden. Dimensionen sind Attribute und Werte, die Posten kategorisieren, sodass Sie sie verfolgen und analysieren können. So können Sie beispielsweise Dimensionen einrichten, mit denen angegeben wird, aus welchem Projekt oder aus welcher Abteilung ein Posten stammt.  

Dies ermöglicht die Verwendung von Dimensionen anstelle der Einrichtung separater Sachkonten für einzelne Abteilungen und Projekte. Kennzeichnet eine umfangreiche Verkaufschance zur Analyse, ohne dazu einen komplizierten Kontenplan zu erstellen. Weitere Informationen finden Sie unter [Business Intelligence](bi.md).

Oder Sie richten beispielsweise eine Dimension mit dem Namen *Abteilung* ein und verwenden diese Dimension und einen Dimensionswert, wenn Sie Verkaufsbelege buchen. Dadurch können Sie auch intelligente Geschäfts-Tools verwenden, um zu sehen, welche Abteilung die Artikel verkauft hat.
Je mehr Dimensionen Sie einrichten und verwenden, auf desto detaillierteren Berichten können Sie Ihre Geschäftsentscheidungen basieren. Zum Beispiel kann ein einzelner Verkaufsposten mehrere Dimensionsinformationen enthalten, wie:  

* Das Konto, auf das der Artikelverkauf gebucht wurde  
* Wo der Artikel verkauft wurde
* Wer ihn verkauft hat
* Die Art des Debitors, die ihn kaufte  

> [!NOTE]  
>   Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.

## <a name="analyzing-by-dimensions"></a>Nach Dimensionen analysieren
Die Funktionalität Dimensionen wird eine wichtige Rolle in der Business Intelligence spielen, wie auch beim Definieren von Analyseansichten. Weitere Informationen finden Sie unter [Vorgehensweise: Daten nach Dimensionen analysieren](bi-how-analyze-data-dimension.md).

> [!TIP]
> Als schnelle Möglichkeit, Transaktionsdaten nach Dimensionen zu analysieren, können Sie Summen im Kostenplan und Posten in allen **Posten**-Fenstern nach Dimensionen filtern. Suchen Sie nach der Aktion **Dimensionsfilter festlegen**.

## <a name="dimension-sets"></a>Dimensionssätze
Ein Dimensionssatz ist eine eindeutige Kombination von Dimensionswerten. Er wird als Dimensionssatzposten in die Datenbank gespeichert. Jeder Dimensionssatzposten stellt einen einzelnen Dimensionswert dar. Der Dimensionssatz wird durch eine allgemeine Dimensionssatz-ID identifiziert, die jedem Dimensionssatzposten zugewiesen wird, der zum Dimensionssatz gehört.  

Wenn Sie eine neue Buch.-Blattzeile, einen Belegkopf oder eine Belegzeile erstellen, können Sie eine Kombination von Dimensionswerten angeben. Anstatt jeden Dimensionswert explizit in der Datenbank zu speichern, wird eine Dimensionssatz-ID der Buch.-Blattzeile, dem Belegkopf oder der Belegzeile zugewiesen, um den Dimensionssatz anzugeben.  

## <a name="setting-up-dimensions"></a>Einrichtung von Dimensionen
Sie können die Dimensionen und die Dimensionswerte, die Sie verwenden möchten, definieren, um Buch.-Blätter und Belege zu kategorisieren, wie Verkaufsaufträge und Bestellungen einrichten. Sie errichten Dimensionen im Fenster **Dimensionen**, wo Sie eine Zeile für jede Dimension erstellen, wie *Projekt*, *Abteilung*, *Bereich* und *Verkaufsperson*.

Sie erstellen auch Einrichtungswerte für Dimensionen. Beispielsweise könnten Werte Abteilungen Ihres Unternehmens darstellen. Dimensionswerte können in einer hierarchischen Struktur eingerichtet werden, die der Struktur des Kontenplans gleicht, sodass die Daten in unterschiedlichen Granularitätsstufen aufgeschlüsselt und Untergruppen von Dimensionswerten summiert werden können. Sie können beliebig viele Dimensionen und Dimensionswerte in Ihrem Mandanten definieren und Sie können eine unbegrenzte Anzahl von Dimensionswerten für jede Dimension festlegen.

Sie können mehrere globale und Shortcutdimensionen einrichten:  

* **Globale Dimensionen** werden als Filter (beispielsweise in Berichten und Stapelverarbeitungen verwendet). Sie können nur zwei globale Dimensionen verwenden, also wählen Sie Dimensionen, die Sie häufig verwenden.
* **Shortcutdimensionen** sind verfügbar als Felder in Buch.-Blattzeilen und Belegzeilen. Sie können bis zu sechs davon erstellen.  

### <a name="setting-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Standarddimensionen für Debitoren, Kreditoren und andere Konten einrichten
Sie können eine Standarddimension für ein bestimmtes Konto einrichten. Die Dimension wird in das Buch.-Blatt oder den Beleg kopiert, wenn Sie die Kontonummer auf der Zeile eingeben, aber Sie können den Code in der Zeile ändern oder löschen, falls erforderlich. Sie können eine Dimension auch erstellen, die für das Buchen eines Postens mit einem speziellen Konto benötigt wird.  

### <a name="translating-the-names-of-dimensions"></a>Übersetzen Sie die Namen von Dimensionen
Wenn Sie eine Dimension und insbesondere eine Shortcutdimension erstellen, was Sie tatsächlich erstellen, ist ein benutzerdefiniertes Feld oder eine Spaltenüberschrift. Wenn Ihr Geschäft international ist, können Sie Übersetzungen für den Namen der Dimension zur Verfügung stellen. Belege, die Dimensionen enthalten, verwenden den übersetzten Namen, soweit zutreffend.   

### <a name="example-of-dimension-setup"></a>Beispiel einer Dimensionseinrichtung
Nehmen wir an, dass Ihr Unternehmen Transaktionen auf Grundlage der Organisationsstruktur und der geografische Lagen verfolgen möchte. Sie können zwei Dimensionen im Fenster **Dimensionen** einrichten.

* **BEREICH**  
* **ABTEILUNG**  

| Code | Name | Code Caption | Filter Caption |
| --- | --- | --- | --- |
| BEREICH |Ursprungs- / Bestimmungsregion |Gebietscode |Filter "Bereich" |
| ABTEILUNG |Abteilung |Abteilungscode |Kostenstellenfilter |

Für **BEREICH** fügen Sie die folgenden Dimensionswerte hinzu:

| Code | Name | Dimensionswertart |
| --- | --- | --- |
| 10 |Amerika |Von-Summe |
| 2.0 |Nordamerika |Standard |
| 30 |Pazifik |Standard |
| 40 |Südamerika |Standard |
| 50 |Amerika, gesamt |Bis-Summe |
| 60 |Europa |Von-Summe |
| 70 |EU |Standard |
| 80 |Nicht-EU |Standard |
| 90 |Europa, gesamt |Bis-Summe |

Um die beiden hauptgeografischen Gebiete Amerika und Europa, fügen Sie bei Bedarf Unterkategorien für Bereiche hinzu, indem Sie die Dimensionswerte einrücken. Dadurch können Sie über Verkäufe oder Ausgaben in den Regionen berichten und Summen für die größeren geographischen Gebiete erhalten. Sie können auch wählen, dass Länder oder Regionen als Ihre Dimensionswerte oder Bundesregionen bzw. Städten gewählt werden, abhängig von Ihrem Geschäft.  
> [!NOTE]  
>   Um eine Hierarchie einzurichten, muss der Code in alphabetischer Reihenfolge sein. Dies umfasst die Codes der standardmäßigen Dimensionswerte in [!INCLUDE[d365fin](includes/d365fin_md.md)]  

Für **ABTEILUNG** fügen Sie die folgenden Dimensionswerte hinzu:

| Code | Name | Dimensionswertart |
| --- | --- | --- |
| ADMIN |Verwaltung |Standard |
| PROD |Produktion |Standard |
| VERKAUF |Verkauf |Standard |

Mit dieser Einrichtung fügen Sie dann Ihre zwei Dimensionen als zwei globalen Dimensionen im Fenster **Finanzbuchhaltung Einrichtung** hinzu. Das bedeutet, dass globale Dimensionen als Filter für Sachposten in allen Berichten, Kontenschemata und Stapelverarbeitungen benutzt werden können. Beide globalen Dimensionen stehen auch als Shortcutdimensionen in Buch.-Blattzeilen und Belegköpfen zur Verfügung.  

## <a name="using-dimensions"></a>Dimensionen verwenden
In einem Beleg, z. B. einem Verkaufsauftrag, können Sie Dimensionsinformationen sowohl für eine einzelne Belegzeile als auch für den Beleg selbst hinzufügen. Sie können beispielsweise im Fenster **Verkaufsauftrag** Dimensionswerte für die ersten beiden Shortcutdimensionen direkt in den Beleg eingeben und weitere Dimensionsinformationen hinzufügen, wenn Sie auf die Schaltfläche **Dimensionen** klicken.  

Wenn Sie stattdessen in einem Buch.-Blatt arbeiten, können Sie auf dieselbe Art und Weise Dimensionsinformationen hinzufügen, wenn Sie Shortcutdimensionen direkt als Felder in Buch.-Blattzeilen eingerichtet haben.  

Sie können Standarddimensionen für Konten oder Kontenarten festlegen, sodass Dimensionen und Dimensionswerte automatisch ausgefüllt werden.

## <a name="see-also"></a>Siehe auch
[Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Vorgehensweise: Analysieren von Daten nach Dimensionen](bi-how-analyze-data-dimension.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

