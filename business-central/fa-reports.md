---
title: Berichte und Analysen zu Anlagen
description: Sehen Sie, welche Berichte und Analysen in der Standardversion von Business Central verfügbar sind, damit Sie den Überblick über Ihre Anlagen behalten können.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: c28e62a2de51323e0a7dcd2f4b5ea26d5896d718
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543344"
---
# <a name="fixed-assets-reports-and-analytics-in-business-central"></a>Berichte und Analysen zu Anlagen in Business Central

Um Sie bei der Verwaltung Ihrer Anlagen in [!INCLUDE [prod_short](includes/prod_short.md)] zu unterstützen, sind Standardberichte und Analysen integriert. Sie gehen über die traditionellen Beschränkungen der Berichterstattung hinaus und helfen Ihnen, verschiedene Arten von Berichten effizient zu gestalten.  

## <a name="reports"></a>Berichte

Die folgende Tabelle beschreibt einige der wichtigsten Berichte im Anlagen-Reporting.

| Bericht | Objekt-ID | Beschreibung |
|--|--|--|
| **Anlagen-Liste** | 5601 | Zeigt die Liste der Anlagen und deren Einrichtung für ein bestimmtes Abschreibungsbuch. |
| **Anlage – Anschaffungsliste** | 5608 | Listet alle Anlagen auf, die innerhalb eines bestimmten Datumsbereichs angeschafft wurden. Sie können auch Anlagen einschließen, die erstellt, aber noch nicht erworben wurden. |
| **Anlagen-Details** | 5604 | Zeigt die Einträge im Sachkonto für Anlagen an. |
| **Anlagen-Analyse** | 5600 | Ein Analysebericht, bei dem Sie zwei Datumsspalten und drei Datenspalten angeben können, die im Bericht angezeigt werden sollen. Um z.B. einen Bericht für die Abstimmung mit dem Sachkonto zu erstellen, fügen Sie Spalten für Anschaffungskosten zum Enddatum, Abschreibung zum Enddatum und Buchwert zum Enddatum hinzu. Ein Prüfbericht könnte Zugänge/Nettoveränderung, Abschreibung/Nettoveränderung und Abschreibung/Nettoveränderung haben, sodass jede Änderung der Anlage bei Bedarf geprüft werden kann. Wenn Sie das Feld **Budgetbericht** auswählen und ein Enddatum in der Zukunft angeben, berechnet der Bericht die zukünftigen Abschreibungen und kann Schätzungen für zukünftige Abschreibungen und Buchwerte abgeben, wenn Sie diese Felder als Berichtsspalten ausgewählt haben. |
| **Anlagenvorschau-Wert** | 5607 | Zeigt die projizierten Abschreibungsbeträge und Buchwerte für eine zukünftige Periode für Anlagen an. Der Bericht ist nützlich, wenn Sie verschiedene Abschreibungsmethoden für Ihre Anlagen verwenden und z. B. die Abschreibung für das nächste Jahr schätzen wollen. Verwenden Sie den Report, um die Budgetbeträge für die Abschreibung zu erstellen, indem Sie ein Budget und das Feld **Kopieren in Sachkontenbudget** auswählen. |
| **Anlage Buchwert 01** | 5605 | Zeigt detaillierte Informationen zu Anschaffungskosten, Abschreibungswert und Buchwert sowohl für einzelne Anlagen als auch für Anlagengruppen. Für jede dieser drei Betragsarten werden Beträge zu Beginn und am Ende einer bestimmten Periode sowie für die Periode selbst berechnet. Wenn Sie das Feld **Budgetbericht** markieren, berechnet der Bericht die erwartete Abschreibung für die Periode. Geben Sie einen *Gruppentyp* ein, wenn Sie möchten, dass der Bericht die Anlagen gruppiert und Gruppensummen ausgibt. Wenn Sie z.B. sechs FA-Klassen festgelegt haben, wählen Sie die Option *FA-Klasse*, um Gruppensummen für jeden der sechs Klassencodes drucken zu lassen.|
| **Anlagenspiegel-Buchwert 02** | 5606 |Zeigt die Aufschlüsselung des Buchwerts der Anlage nach Änderungen in Anschaffung, Abschreibung und Aufwertung innerhalb der Periode mit einer weiteren Aufschlüsselung nach Zugängen und Abgängen innerhalb der Periode. Verwenden Sie diesen Bericht, um die Änderungen im Anlagevermögen einer bestimmten Periode zu beschreiben, wenn viele verschiedene Änderungen in der Gruppierung des Anlagevermögens auftreten. Wenn Sie das Feld **Budgetbericht** markieren, berechnet der Bericht die erwartete Abschreibung für die Periode. Geben Sie einen *Gruppentyp* ein, wenn Sie möchten, dass der Bericht die Anlagen gruppiert und Gruppensummen ausgibt. Wenn Sie z.B. sechs FA-Klassen festgelegt haben, wählen Sie die Option *FA-Klasse*, um Gruppensummen für jeden der sechs Klassencodes drucken zu lassen. |
| **Anlagen-Sachkontoanalyse**| 5610 |Zeigt eine Analyse Ihres Anlagevermögens (FA) mit verschiedenen Datentypen für einzelne Anlagen und/oder Gruppen von Anlagen. Auf der Inforegisterkarte Anlagen können Sie Filter festlegen, wenn der Bericht nur bestimmte Anlagen enthalten soll. Auf der Inforegister-Registerkarte „Optionen“ können Sie den Bericht an Ihre speziellen Anforderungen anpassen. Der Bericht ähnelt dem Bericht **Anlagenanalyse**, aber speziell für das Abstimmen mit dem Hauptbuch und speziell für die Überprüfung der Abgangsbuchungen. Der Bericht setzt voraus, dass Sie die Sachkonten kennen, die in der Einrichtung für Buchungen angegeben sind. |
| **Anlagenregister** |5603  |Zeigt gebuchte Sachkonto-Einträge, die nach Registernummern sortiert und unterteilt sind. Sie können festlegen, welche Einträge der Register angezeigt werden, indem Sie einen Filter festlegen. Es ist wichtig, einen Filter festzulegen; andernfalls zeigt der Bericht möglicherweise eine sehr große Menge an Informationen an. |

## <a name="see-also"></a>Siehe auch

[Analysieren von Finanzberichten in Microsoft Excel](finance-analyze-excel.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Verwaltung von Anlagen](fa-manage.md)  
[Lokale Funktionen – Übersicht](about-localization.md)  
[Buchhalter-Erfahrung in [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]