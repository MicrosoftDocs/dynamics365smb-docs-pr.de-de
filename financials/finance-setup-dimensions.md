---
title: Einrichten von Dimensionen | Microsoft Docs
description: "Sie können die Dimensionen und die Dimensionswerte, die Sie verwenden möchten, definieren, um Buch.-Blätter und Belege zu kategorisieren, wie Verkaufsaufträge und Bestellungen einrichten."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/28/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0da77c5be3b49f715384752ad61fc072aea8525c
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-dimensions"></a>Einrichtung von Dimensionen
Sie können die Dimensionen und die Dimensionswerte, die Sie verwenden möchten, definieren, um Buch.-Blätter und Belege zu kategorisieren, wie Verkaufsaufträge und Bestellungen einrichten. Sie errichten Dimensionen im Fenster **Dimensionen**, wo Sie eine Zeile für jede Dimension erstellen, wie *Projekt*,*Abteilung*, *Bereich* und *Verkaufsperson*.

Sie erstellen auch Einrichtungswerte für Dimensionen. Beispielsweise könnten Werte Abteilungen Ihres Unternehmens darstellen. Dimensionswerte können in einer hierarchischen Struktur eingerichtet werden, die der Struktur des Kontenplans gleicht, sodass die Daten in unterschiedlichen Granularitätsstufen aufgeschlüsselt und Untergruppen von Dimensionswerten summiert werden können. Sie können beliebig viele Dimensionen und Dimensionswerte in Ihrem Mandanten definieren und Sie können eine unbegrenzte Anzahl von Dimensionswerten für jede Dimension festlegen.

Sie können mehrere globale und Shortcutdimensionen einrichten:  

* ***** Globale Dimensionen ***** werden als Filter (beispielsweise in Berichten und Stapelverarbeitungen verwendet. Sie können nur zwei globale Dimensionen verwenden, also wählen Sie Dimensionen, die Sie häufig verwenden.
* **Shortcutdimensionen** sind verfügbar als Felder in Buch.-Blattzeilen und Belegzeilen. Sie können bis zu sechs davon erstellen.  

**Hinweis: ** Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter] [Benutzeroberfläche [!INCLUDE[d365fin](includes/d365fin_md.md)] (ui-experiences.md) anpassen.

## <a name="set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Standarddimensionen für Debitoren, Kreditoren und andere Konten einrichten
Sie können eine Standarddimension für ein bestimmtes Konto einrichten. Die Dimension wird in das Buch.-Blatt oder den Beleg kopiert, wenn Sie die Kontonummer auf der Zeile eingeben, aber Sie können den Code in der Zeile ändern oder löschen, falls erforderlich. Sie können eine Dimension auch erstellen, die für das Buchen eines Postens mit einem speziellen Konto benötigt wird.  

## <a name="translate-the-names-of-dimensions"></a>Übersetzen Sie die Namen von Dimensionen
Wenn Sie eine Dimension und insbesondere eine Shortcutdimension erstellen, was Sie tatsächlich erstellen, ist ein benutzerdefiniertes Feld oder eine Spaltenüberschrift. Wenn Ihr Geschäft international ist, können Sie Übersetzungen für den Namen der Dimension zur Verfügung stellen. Belege, die Dimensionen enthalten, verwenden den übersetzten Namen, soweit zutreffend.   

## <a name="example"></a>Beispiel
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
**Hinweis**: Um eine Hierarchie einzurichten, muss der Code in alphabetischer Reihenfolge sein. Dies umfasst die Codes der standardmäßigen Dimensionswerte in [!INCLUDE[d365fin](includes/d365fin_md.md)]  

Für **ABTEILUNG** fügen Sie die folgenden Dimensionswerte hinzu:

| Code | Name | Dimensionswertart |
| --- | --- | --- |
| ADMIN |Verwaltung |Standard |
| PROD |Produktion |Standard |
| VERKAUF |Verkauf |Standard |

Mit dieser Einrichtung fügen Sie dann Ihre zwei Dimensionen als zwei globalen Dimensionen im Fenster **Finanzbuchhaltung Einrichtung** hinzu. Das bedeutet, dass globale Dimensionen als Filter für Sachposten in allen Berichten, Kontenschemata und Stapelverarbeitungen benutzt werden können. Beide globalen Dimensionen stehen auch als Shortcutdimensionen in Buch.-Blattzeilen und Belegköpfen zur Verfügung.  

Mit dieser Einrichtung können Sie das Hinzufügen von Dimensionen für Dokumente und Buch.-Blättern starten. Weitere Informationen finden Sie unter [Dimensionen](finance-dimensions.md).  

## <a name="see-also"></a>Siehe auch
[Dimensionen](finance-dimensions.md)  
[Finance einrichten](finance-setup-finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]

