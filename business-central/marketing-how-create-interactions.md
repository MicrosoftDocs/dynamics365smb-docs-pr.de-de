---
title: "Erstellen von Aktivitäten zu Kontakten und Segmenten | Microsoft Docs"
description: "Sie erstellen Aktivitäten, um die Aktivitäten und Kommunikationen (z. B. E-Mails) mit Ihren Kontakten und Segmenten in Business Central zu erfassen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/15/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: aa6be34f1b43dfe0b1f82cbb6a2cefd06edb0f83
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="create-interactions-on-contacts-and-segments"></a>Erstellen von Aktivitäten zu Kontakten und Segmenten
Sie erstellen Aktivitäten, um die Aktivitäten und Kommunikationen (z. B. E-Mails) mit Ihren Kontakten und Segmenten zu erfassen.

Bevor Sie Aktivitäten erstellen, müssen Sie Aktivitätenvorlagen einrichten. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Aktivitätvorlagen](marketing-interactions.md).

## <a name="to-create-an-interaction"></a>So erstellen Sie eine Aktivität
1. Öffnen Sie den Kontakt, den Verkäufer oder den Aktivitätenprotokollposten.
2. Wählen Sie die Aktion **Aktivität erstellen** aus.
3. Füllen Sie die Felder aus, und wählen Sie dann die Schaltfläche **OK** aus.

> [!NOTE]  
>   Wenn Sie eine andere Aufgabe ausführen müssen, bevor Sie die Aktivität abgeschlossen haben, können Sie **Abbrechen** auswählen und den Assistenten schließen und die Aktivität später abschließen. Dieses verschiebt die Aktivität.

## <a name="to-finish-and-delete-postponed-interactions"></a>Beenden und Löschen von zurückgestellten Aktivitäten
1. Öffnen Sie den Kontakt, den Verkäufer oder den Aktivitätenprotokollposten.
2. Wählen Sie **Zurückgestellte Aktivitäten**.
3. Wählen Sie die fertig zu stellende Aktivität aus, und klicken Sie anschließend auf die Aktion **Fortsetzen**.

## <a name="to-create-an-interaction-on-a-segment"></a>So erstellen Sie eine Aktivität für ein Segment
1. Oder wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Segmente** ein. Wählen Sie dann den zugehörigen Link aus.
2. Füllen Sie im Fenster **Segment** die Felder im Abschnitt **Aktivität** aus, um zu anzugeben, welche Aktivität Sie dem Segment zuordnen möchten.

    Nachdem Sie dem Segment eine Aktivität zugeordnet haben, können Sie die Aktivität für jeden einzelnen Kontakt personalisieren z. B., indem Sie eine andere Aktivitätenvorlage in den Zeilen des Fensters **Segment** auswählen.  
3. Um das Segment und Aktivitäten zu protokollieren, wählen Sie die **Protokoll**-Aktion. Das Fenster **Segment protokollieren** wird geöffnet.
4. Wenn Sie ein neues Segment erstellen möchten, das dieselben Kontakte enthält, aktivieren Sie das Kontrollkästchen **Anschluss-Segment erstellen**. Um ein Anschluss-Segment zu erstellen, müssen Sie im Fenster **Marketing Vertrieb Einr.** bereits Nummernserien für Segmente angegeben haben.

Eine Aktivität wird für jeden Kontakt im Segment in der Tabelle **Aktivitätenprotokollposten** erfasst, und das Segment wird protokolliert. Protokollierte Segmente finden Sie im Fenster **Protokollierte Segmente**.

Wenn Sie im Feld **Anschluss-Segment erstellen** ein Häkchen gesetzt haben, wird ein neues Segment erstellt, das dieselben Kontakte enthält wie das von Ihnen protokollierte Segment.

## <a name="see-also"></a>Siehe auch
[Aktivitäten aufzeichnen](marketing-interactions.md)  
[Kontakte verwalten](marketing-contacts.md)  
[Verkaufschancen verwalten](marketing-manage-sales-opportunities.md)  
[Marketing & Vertrieb einrichten](marketing-setup-marketing.md)  
[Arbeiten mit  Business Central](ui-work-product.md)

