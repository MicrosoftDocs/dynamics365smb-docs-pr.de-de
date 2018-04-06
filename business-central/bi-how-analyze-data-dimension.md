---
title: Analysieren Sie Daten nach Dimensionen| Microsoft Docs
description: "Beschreibt, wie verschiedene Geschäftsdaten nach Dimensionen analysiert werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 94d783a806b56e972f16ebe1e0d383582cd72126
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
#  <a name="analyze-data-by-dimensions"></a>Analysieren von Daten nach Dimensionen
Bei den Dimensionen der Finanzanalyse handelt es sich um Daten, die Sie einem Posten als eine Art Markierung hinzufügen können. Diese Daten dienen zum Gruppieren von Posten mit ähnlichen Merkmalen – beispielsweise Debitoren, Regionen, Produkte oder Verkäufer – sowie zum einfachen Abrufen dieser Gruppen zur Analyse. Dimensionen können für Posten in Buch.-Blättern, Belegen und Budgets verwendet werden. Der Begriff "Dimension" beschreibt, wie eine Analyse ausgeführt wird. Ein Beispiel für eine zweidimensionale Analyse sind Verkäufe pro Bereich. Durch die Verwendung zusätzlicher Dimensionen bei der Postenerstellung lassen sich komplexere Analysen ausführen, beispielsweise Verkäufe pro Verkaufskampagne pro Debitorengruppe pro Bereich. Weitere Informationen finden Sie unter [Arbeiten mit Dimensionen](finance-dimensions.md)

Die dimensionsgestützte Analyse von Daten ermöglicht einen tieferen Einblick in das Unternehmen sowie eine bessere Bewertung von Informationen: Wie gut funktioniert der operative Bereich des Unternehmens? Wo liegen Stärken, wo Schwächen? Welche Bereiche benötigen mehr Ressourcen?

> [!TIP]
> Als schnelle Möglichkeit, Transaktionsdaten nach Dimensionen zu analysieren, können Sie Summen im Kostenplan und Posten in allen **Posten**-Fenstern nach Dimensionen filtern. Suchen Sie nach der Aktion **Dimensionsfilter festlegen**.

## <a name="to-set-up-an-analysis-view"></a>So richten Sie eine Analyseansicht ein  
Eine Analyse nach Dimensionen zeigt eine ausgewählte Kombination von Dimensionen an. Sie können jede Analyseansicht, die Sie eingerichtet haben, speichern und wieder aufrufen. Die Informationen zum Einrichten einer Analyse werden auf einer **Analyseansichtskarte** gespeichert, um künftige Analysen zu vereinfachen.  

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Analyseansicht** ein und wählen den zugehörenden Link aus.  
2. Wählen Sie im Fenster **Analyseansichtsliste** die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Um den vier Dimensionscodes im Inforegister **Dimensionen** weitere Dimensionscodes hinzuzufügen. Füllen Sie die **Filter** aus, und klicken Sie anschließend auf **OK**  
5. Um die Ansicht zu aktualisieren, wählen Sie die **Aktualisieren** Aktion.

## <a name="to-analyze-by-dimensions"></a>Analysieren von Daten nach Dimensionen
In der Matrix **Verkaufsanalyse nach Dim.** können Sie die Beträge in der Finanzbuchhaltung unter Verwendung der bereits eingerichteten Analyseansichten anzeigen. Füllen Sie das Fenster **Analysen nach Dimensionen** aus, um festzulegen, was in der Matrix angezeigt wird. Wählen Sie dann **Matrix anzeigen** zum Anzeigen der Matrix.  

- Die Spalten auf der linken Seite enthalten Informationen, die auf Ihrer Auswahl im Feld **Zeilenansicht** im Kopf basieren.  
- Die Spalten auf der rechten Seite enthalten Informationen, die auf Ihrer Auswahl im Feld **Spaltenansicht** im Kopf basieren.  

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Analyse nach Dimension** ein und wählen den zugehörenden Link aus.  
2. Wählen Sie die entsprechende Analyseansicht aus, und klicken Sie auf **Analyseansicht bearbeiten**.
3. Im Fenster **Verkaufsanalyse nach Dim.** füllen Sie die Felder aus, um die Analyseansicht zu definieren.
4. 5. Um die Spezifikation eines Betrags im Matrixfenster anzuzeigen, wählen Sie den Betrag aus.  

> [!IMPORTANT]  
>   Die ausgewählte Periodenlänge muss mindestens der Länge der Periode entsprechen, die auf der Karte **Analyseansicht** für die Datumskomprimierung angegeben ist. Die Befehle **Nächster Satz** und **Vorheriger Satz** sind inaktiv, wenn im Feld **Periode** oder im Feld **Als Zeile anzeigen** oder das Feld **Als Spalten anzeigen** gewählt wurde.  

> [!NOTE]  
>   Sie können den Bericht **Dimensionen - Detail** auswählen, um eine detaillierte Aufstellung anzuzeigen, wie über eine ausgewählte Periode Dimensionen in den Posten angewendet wurden. Mit dem Bericht **Dimensionen - Total** können Sie die Anzeige auf die Gesamtbeträge beschränken.  

> [!TIP]  
>   Sie können die Ansicht auch verändern, indem Sie die Inhalte der Felder **Zeilenansicht** und **Spaltenansicht** verändern. Um eine Ansichtseinstellung auszutauschen, wählen Sie die **Zeilen- und Spaltenansicht vertauschen**.

## <a name="to-update-an-analysis-view"></a>Eine Analyseansicht analysieren:  
Die Beträge, die im Fenster **Analyse nach Dimensionen** angezeigt werden, geben Aufschluss über den Zustand des Mandanten zum Zeitpunkt der letzten Aktualisierung. Um einen Eindruck über den aktuellen Zustand zu erhalten, müssen Sie die Analyseansicht mit der Aktualisierungsfunktion aktualisieren.

Der folgende Ablauf bezieht sich auf die Aktualisierung einer Analyseansicht im Fenster **Analyse nach Dimensionen** . Die Schritte sind **Analyseansichtskartenansicht** und **Artikelanalyseansichtenübersicht** ähnlich.  

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Analyse nach Dimension** ein und wählen den zugehörenden Link aus.  
2. Im Fenster **Analyse nach Dimensionen** wählen Sie das Feld **Analyseansichtscode**, um die Optionen anzuzeigen aus.  
3. Wählen Sie die Zeile mit der relevanten Analyseansicht aus.  
4. Wählen Sie die Aktion **Kapazität aktualisieren** aus.  

> [!TIP]  
>   Wenn Sie das Kontrollkästchen **Bei Buchung aktualisieren** in einer Analyseansichtskarte auswählen, wird die Ansicht aktualisiert, wenn eine beteiligte Transaktion gebucht wird.

> [!NOTE]  
>   Um eine oder alle Analyseansichten gleichzeitig zu aktualisieren, müssen Sie die Stapelverarbeitung **Analyseansichten aktualisieren** verwenden.  

## <a name="see-also"></a>Siehe auch
[Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

