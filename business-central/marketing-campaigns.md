---
title: Marketingkampagnen in Business Central einrichten | Microsoft Docs
description: "Beschreibt, wie Sie Marketingkampagnen in Business Central einrichten und ausführen, um potenzielle Kunden zu identifizieren und Kunden zu behalten."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 66d8bda9082754c4278a47e44529a30dea8eb39c
ms.contentlocale: de-de
ms.lasthandoff: 11/26/2018

---
# <a name="managing-marketing-campaigns"></a>Verwaltung von Marketingkampagnen
Der Einsatz eines fundierten Marketingplans ermöglicht das Erkennen, Gewinnen und Binden von Debitoren. Ein Marketingplan setzt sich aus mehreren Kampagnen und anderen Aktivitäten rund um Ihre Verkaufs- und Marketingaktivitäten zusammen. Beim Planen einer Kampagne müssen Sie entscheiden, welche Kontakte Sie ansprechen möchten, welche Art von Kampagne (beispielsweise Messe oder Direktwerbung) Sie erstellen möchten und welche Verkäufer die einzelnen Aufgaben ausführen sollen.

Jede Kampagne besteht aus unterschiedlichen Aktionen oder Aufgaben. Sie können mehrere Aufgabe, zum Beispiel Tätigkeiten kombinieren, die jede einen Schritt darstellen in den Aktivitäten. Alle Schritte innerhalb einer Aktion sind durch ein Datenformular miteinander verbunden. Optionen können nur einzelnen Verkäufern zugewiesen werden. Aktivitäten können Verkaufschancen, Verkäufer, Gruppen von Vertriebsmitarbeitern und den Kontakten zugeordnet werden. Weitere Informationen finden Sie unter [Einrichten von Verkaufschancen für Verkaufsprozesse und Prozess-Stufen](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="defining-individual-campaigns"></a>Einzelkampagne definieren
Damit eine Kampagne erstellt werden kann, müssen *Codes für den Kampagnenstatus* eingerichtet werden. Diese Codes vereinfachen das Verwalten der Kampagnen, indem der Kampagne ein Status zugeordnet wird. So können Sie den aktuellen Status der Kampagne sowie den nächsten Schritt der Kampagne ablesen, während die einzelnen Phasen einer Kampagne durchlaufen werden. Sie können Kampagnenstatuscodes auf der Seite **Kampagnenstatus** einrichten.

Für jede Kampagne, die Sie nachverfolgen möchten, kann eine Kampagnenkarte erstellt werden. Auf diesen Kampagnenkarten finden Sie auch allgemeine Informationen zu den Kampagnen.
Sie können Kampagnenposten löschen, z. B. wenn der Posten eine Aktion speichert, die storniert wurde. Es können nur stornierte Kampagnenposten gelöscht werden.

### <a name="selecting-the-target-audience"></a>Auswählen der Zielgruppe
Nachdem eine Kampagne erstellt wurde, können Sie mit dem Erstellen von Segmenten für die Kampagnen beginnen und das Zielsegment festlegen. Weitere Informationen finden Sie unter [Segmente verwalten](marketing-segments.md).

### <a name="registering-discount-percentages"></a>Erfassen von Rabattprozentsätzen
Nachdem Sie Ihre Kampagne eingerichtet haben, entschieden haben, welche Segmente die Kampagne umfassen soll, und das Start- und Enddatum festgelegt haben, erfassen Sie den Rabattprozentsatz, den der Debitor auf die einzelnen Artikel in den Zeilen der Seite **Verkaufszeilenrabatt** erhält. Sie können die Verkaufspreise der einzelnen Artikel in den Zeilen auf der Seite **Verkaufspreise** auch erfassen. Sie können auf beide Seiten von der Kampagnenkarte zugreifen.

 Nachdem Sie die Verkaufspreise/Zeilenrabatte sowie die Segmente auf der Kampagnenkarte eingerichtet haben, müssen Sie sie aktivieren, so dass die Kampagnenpreise/Rabatte in den Zeilen wiedergegeben werden.

> [!NOTE]  
>   Um die Verkaufspreise/Zeilenrabatte zu aktivieren, müssen Sie das gesamte Segment oder nur einzelne Kontakte für die Kampagne markieren. Wenn die Verkaufspreise/Zeilenrabatte für alle Kontakte des Segments gelten sollen, wählen Sie im Fenster **Segment** auf dem Inforegister **Kampagne** das Feld **Kampagnenziel** aus.

Wenn die Verkaufspreise/Zeilenrabatte nicht für alle Kontakte des Segments gelten sollen, können Sie das Feld **Kampagnenziel** für die relevanten Kontakte. Wenn Sie dieses Feld nicht sehen, können Sie es zur Ansicht hinzuzufügen. Weitere Informationen finden Sie unter [Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md).

## <a name="conducting-campaigns"></a>Kampagnen durchführen
Während der gesamten Laufzeit der Kampagne werden alle Interaktionen mit den Kontakten bzw. mit dem Segment erfasst. Dadurch können Sie oder andere Gruppen eine Kampagne anzeigen und statistische oder andere Informationen zu Kosten und Erfolgsraten der Kampagne abrufen.

Kampagnen werden vom Verkäufer geleitet werden, und Sie müssen Aktivitäten erstellen, um jede Aufgabem anzuzeigen und dem entsprechende Verkäufer zuzuordnen. Weitere Informationen finden Sie unter [Einrichten von Verkaufschancen für Verkaufsprozesse und Prozess-Stufen](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="see-also"></a>Siehe auch
[Kontakte verwalten](marketing-contacts.md)  
[Verwalten von Segmenten](marketing-segments.md)  
[Verkaufschancen verwalten](marketing-manage-sales-opportunities.md)  
[Arbeiten mit  Business Central](ui-work-product.md)  

