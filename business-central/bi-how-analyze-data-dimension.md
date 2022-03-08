---
title: Analysieren Sie Daten nach Dimensionen| Microsoft Docs
description: Beschreibt, wie verschiedene Geschäftsdaten nach Dimensionen analysiert werden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: bed657fd2694dc3c1adc44a7dddfd857ab60f3bf
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783488"
---
#  <a name="analyze-data-by-dimensions"></a>Analysieren von Daten nach Dimensionen
Bei den Dimensionen der Finanzanalyse handelt es sich um Daten, die Sie einem Posten als eine Art Markierung hinzufügen können. Diese Daten dienen zum Gruppieren von Posten mit ähnlichen Merkmalen – beispielsweise Debitoren, Regionen, Produkte oder Verkäufer – sowie zum einfachen Abrufen dieser Gruppen zur Analyse. Dimensionen können für Posten in Buch.-Blättern, Belegen und Budgets verwendet werden. Der Begriff "Dimension" beschreibt, wie eine Analyse ausgeführt wird. Ein Beispiel für eine zweidimensionale Analyse sind Verkäufe pro Bereich. Durch die Verwendung zusätzlicher Dimensionen bei der Postenerstellung lassen sich komplexere Analysen ausführen, beispielsweise Verkäufe pro Verkaufskampagne pro Debitorengruppe pro Bereich. Weitere Informationen finden Sie unter [Arbeiten mit Dimensionen](finance-dimensions.md)

Die dimensionsgestützte Analyse von Daten ermöglicht einen tieferen Einblick in das Unternehmen sowie eine bessere Bewertung von Informationen: Wie gut funktioniert der operative Bereich des Unternehmens? Wo liegen Stärken, wo Schwächen? Welche Bereiche benötigen mehr Ressourcen?

> [!TIP]
> Als schnelle Möglichkeit, Transaktionsdaten nach Dimensionen zu analysieren, können Sie Summen im Kostenplan und Posten in allen **Posten**-Seiten nach Dimensionen filtern. Suchen Sie nach der Aktion **Dimensionsfilter festlegen**.

## <a name="to-set-up-an-analysis-view"></a>So richten Sie eine Analyseansicht ein  
Eine Analyse nach Dimensionen zeigt eine ausgewählte Kombination von Dimensionen an. Sie können jede Analyseansicht, die Sie eingerichtet haben, speichern und wieder aufrufen. Die Informationen zum Einrichten einer Analyse werden auf einer **Analyseansichtskarte** gespeichert, um künftige Analysen zu vereinfachen.  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Analyseübersichten** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Analyseansichtsliste** die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Um den vier Dimensionscodes im Inforegister **Dimensionen** weitere Dimensionscodes hinzuzufügen. Füllen Sie die **Filter** aus, und klicken Sie anschließend auf **OK**  
5. Um die Ansicht zu aktualisieren, wählen Sie die **Aktualisieren** Aktion.

## <a name="to-analyze-by-dimensions"></a>Analysieren von Daten nach Dimensionen
In der Matrix **Verkaufsanalyse nach Dim.** können Sie die Beträge in der Finanzbuchhaltung unter Verwendung der bereits eingerichteten Analyseansichten anzeigen. Füllen Sie die Seite **Analysen nach Dimensionen** aus, um festzulegen, was in der Matrix angezeigt wird. Wählen Sie dann **Matrix anzeigen** zum Anzeigen der Matrix.  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Analyseübersichten** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die entsprechende Analyseansicht aus, und klicken Sie auf **Analyse nach Dimension bearbeiten**.
3. auf der Seite  **Verkaufsanalyse nach Dimension** füllen Sie die Felder aus, um zu definieren, welche Daten wie angezeigt werden.
4. Wählen Sie die **Matrix anzeigen** Aktion aus, um die für die jeweilige Matrixseite definierte Analyseansicht zu öffnen.
5. Um die Spezifikation eines Betrags auf der Matrixseite anzuzeigen, wählen Sie den Betrag aus.  

- Die Spalten auf der linken Seite enthalten Informationen, die auf Ihrer Auswahl im Feld **Zeilenansicht** im Kopf basieren.  
- Die Spalten auf der rechten Seite enthalten Informationen, die auf Ihrer Auswahl im Feld **Spaltenansicht** im Kopf basieren.

> [!IMPORTANT]  
>   Die ausgewählte Periodenlänge muss mindestens der Länge der Periode entsprechen, die auf der Karte **Analyseansicht** für die Datumskomprimierung angegeben ist. Die Befehle **Nächster Satz** und **Vorheriger Satz** sind inaktiv, wenn im Feld **Periode** oder im Feld **Als Zeile anzeigen** oder das Feld **Als Spalten anzeigen** gewählt wurde.  

> [!NOTE]  
>   Sie können den Bericht **Dimensionen - Detail** auswählen, um eine detaillierte Aufstellung anzuzeigen, wie über eine ausgewählte Periode Dimensionen in den Posten angewendet wurden. Mit dem Bericht **Dimensionen - Total** können Sie die Anzeige auf die Gesamtbeträge beschränken.  

> [!TIP]  
>   Sie können die Ansicht auch verändern, indem Sie die Inhalte der Felder **Zeilenansicht** und **Spaltenansicht** verändern. Um eine Ansichtseinstellung auszutauschen, wählen Sie die **Zeilen- und Spaltenansicht vertauschen**.

## <a name="to-update-an-analysis-view"></a>Eine Analyseansicht analysieren:  
Die Beträge, die auf der Seite **Analyse nach Dimensionen** angezeigt werden, geben Aufschluss über den Zustand des Mandanten zum Zeitpunkt der letzten Aktualisierung. Um einen Eindruck über den aktuellen Zustand zu erhalten, müssen Sie die Analyseansicht mit der Aktualisierungsfunktion aktualisieren.

Der folgende Ablauf bezieht sich auf die Aktualisierung einer Analyseansicht  auf der Seite **Analyse nach Dimensionen** . Die Schritte sind **Analyseansichtskartenansicht** und **Artikelanalyseansichtenübersicht** ähnlich.  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Analyseübersichten** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die entsprechende Analyseansicht aus, und klicken Sie auf **Analyse nach Dimension bearbeiten**.
2. Auf der Seite **Analyse nach Dimensionen** wählen Sie das Feld **Analyseansichtscode**, um die Optionen anzuzeigen aus.  
3. Wählen Sie die Zeile mit der relevanten Analyseansicht aus.  
4. Wählen Sie auf der Seite **Analyseansicht** die entsprechende Analyseansicht aus, und klicken Sie auf **Aktualisieren**.  

> [!TIP]  
>   Wenn Sie das Kontrollkästchen **Bei Buchung aktualisieren** in einer Analyseansichtskarte auswählen, wird die Ansicht aktualisiert, wenn eine beteiligte Transaktion gebucht wird.

> [!NOTE]  
>   Um eine oder alle Analyseansichten gleichzeitig zu aktualisieren, müssen Sie die Stapelverarbeitung **Analyseansichten aktualisieren** verwenden.  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/dimensions-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch
[Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
