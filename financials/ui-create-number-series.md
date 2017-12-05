---
title: 'So geht es: Nummernserien herstellen | Microsoft Docs'
description: Erfahren Sie, wie Nummernserieb errichtet werden, die eindeutigen ID Codes zu Konten und Belegen in Dynamics 365 Business edition zugewiesen werden.
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 8605c5273ac69ff7a5b8b8dab59b0856795ed706
ms.contentlocale: de-de
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-create-number-series"></a>So geht es: Erstellen von Nummernserien
Für jeden eingerichteten Mandanten müssen eindeutige Identifizierungscodes für Elemente wie Sachkonten, Debitor-/Kreditorkonten, Rechnungen und andere Belege zugeordnet werden. Die Nummerierung dient jedoch nicht nur zur Identifizierung. Ein durchdachtes Nummerierungssystem trägt zur einfacheren Verwaltung und besseren Analysierbarkeit des Mandanten bei, was eine Verringerung von Eingabefehlern zur Folge hat.

> [!NOTE]  
>   Es ist empfehlenswert, dass Sie dieselben Nummernseriencodes verwenden, die Sie im Fenster **Nummernserienübersicht** im CRONUS-Demomandanten sehen. Codes wie *P-INV+* ergeben möglicherweis nicht sofort einen Sinn, aber [!INCLUDE[d365fin](includes/d365fin_md.md)] hat eine einige Standardeinstellungen, die von diesen Nummernseriencodes abhängen.

Ein Nummerierungssystem wird durch Einrichten mindestens eines Codes für die einzelnen Arten von Masterdaten oder Belegen eingerichtet. So können Sie beispielsweise einen Code für die Nummerierung von Debitoren, einen weiteren Code für die Nummerierung von Verkaufsrechnungen und einen weiteren Code für die Nummerierung von Belegen in Fibu Buch.-Blättern einrichten. Nachdem ein Code eingerichtet wurde, muss mindestens eine Nummernserienzeile eingerichtet werden. Die Nummernserienzeile enthält Informationen wie die erste und die letzte Nummer der Serie sowie das Startdatum. Pro Nummernseriencode lassen sich mehrere Nummernserienzeilen mit unterschiedlichem Startdatum einrichten. Die Serie wird fortlaufend verwendet, wobei jede Serie zum entsprechenden Startdatum beginnt.

Sie legen in der Regel die Nummernserie fest, um automatisch die nächste fortlaufende Nummer auf neuen Karten oder Dokumente einzusetzen, die Sie erstellen. Sie können eine Nummernserie festlegen, bei der Sie manuell die neue Nummer eingeben können. Sie definieren dies mit dem Kontrollkästchen **Manuelle Nr.**

Verwenden Sie Nummernserienbeziehungen, wenn Sie für eine Masterdatenart mehrere Nummernseriencodes verwenden möchten – beispielsweise, um für unterschiedliche Artikelkategorien unterschiedliche Nummernserien zu verwenden.

## <a name="to-create-a-new-number-series"></a>Erstellen von Nummernserien
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Seriennummer** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Auf der neuen Zeile füllen Sie die Felder wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**TIPP**: Um manuelle Eingabe einer neuen Nummer auf Karten oder Belegen zu ermöglichen, wählen Sie das Kontrollkästchen **Standardnr.** aus und wählen Sie das Kontrollkästchen **Manuelle Nr.**.

Wenn Sie nun eine neue Karte oder einen neuen Beleg erstellen, der eingerichtet ist, die gewünschten Nummernserien zu verwenden, können Sie die **Nr.** manuell ausfüllen Feld mit beliebigem Wert.  

## <a name="to-set-up-where-a-number-series-is-used"></a>Einrichten, ob eine Nummernserie verwendet wird
Der folgende Ablauf zeigt, wie Nummernserien für den Verkaufsbereich eingerichtet werden. Die Schritte sind gleich wie bei anderen Bereichen.
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kredioren und Debitoren** ein. Wählen Sie dann den zugehörigen Link aus.
2. Im Fenster **Debitoren & Verkauf** im Inforegister **Nummernserie**, wählen Sie die gewünschte Serie für jede Verkaufs- Karte oder jeden Beleg aus.

Die ausgewählten Anzahl wird nun verwendet, um **Nr.** auszufüllen Feld auf der fraglichen Karte oder auf dem fraglichen Dokument entsprechend den Einstellungen, die Sie in der Nummernserie erstellt haben.

## <a name="to-create-relationships-between-number-series"></a>Verbindungen zwischen Nummernserien herstellen:
Wenn Sie mehr als einen Nummernseriencode für dieselbe Art von grundlegenden Daten oder Geschäftsvorfällen eingerichtet haben, können Sie Verbindungen zwischen diesen Codes herstellen. Dann können Sie zwischen den verschiedenen Codes auswählen, wenn Sie eine Nummer verwenden wollen.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Seriennummer** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Zeile mit der Nummernserie, für die Sie Verbindungen herstellen wollen und wählen Sie **Beziehungen**.
3. Geben Sie im Feld **Seriencode** den Code für die Nummernserie ein, für die Sie eine Verbindung mit der in Schritt 2 ausgewählten Nummernserie herstellen möchten.
4. Fügen Sie für jeden Code, für den eine Verbindung mit der ausgewählten Nummernserie hergestellt werden soll, eine neue Zeile hinzu.
5. Schließen Sie das Fenster.

Wenn Sie jetzt etwas einrichten, was eine Nummer benötigt, können Sie die von Ihnen erzeugten Verbindungen verwenden, um zwischen den verbundenen Nummernserien auszuwählen.

## <a name="see-also"></a>Siehe auch
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

