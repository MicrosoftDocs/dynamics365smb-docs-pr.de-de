---
title: Marketingkampagnen in Financials einrichten | Microsoft Docs
description: "Beschreibt, wie Sie Marketingkampagnen in Dynamics 365 for Financials einrichten und durchführen können"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 05/20/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 92c5fb75f4f3d3180ba67b89481beed2e58c3dbe
ms.openlocfilehash: 68359d2dd2c2e07463babda91d86d47998f0912a
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# <a name="managing-marketing-campaigns"></a>Verwaltung von Marketingkampagnen
Der Einsatz eines fundierten Marketingplans ermöglicht das Erkennen, Gewinnen und Binden von Debitoren. Ein Marketingplan setzt sich aus mehreren Kampagnen und anderen Aktivitäten rund um Ihre Verkaufs- und Marketingaktivitäten zusammen. Beim Planen einer Kampagne müssen Sie entscheiden, welche Kontakte Sie ansprechen möchten, welche Art von Kampagne (beispielsweise Messe oder Direktwerbung) Sie erstellen möchten und welche Verkäufer die einzelnen Aufgaben ausführen sollen.

Jede Kampagne besteht aus unterschiedlichen Aktionen oder Aufgaben. Sie können mehrere Aufgabe, zum Beispiel Tätigkeiten kombinieren, die jede einen Schritt darstellen in den Aktivitäten. Alle Schritte innerhalb einer Aktion sind durch ein Datenformular miteinander verbunden. Optionen können nur einzelnen Verkäufern zugewiesen werden. Aktivitäten können Verkaufschancen, Verkäufer, Gruppen von Vertriebsmitarbeitern und den Kontakten zugeordnet werden. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Verkaufschancen für Verkaufsprozesse und Prozess-Stufen](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="defining-individual-campaigns"></a>Einzelkampagne definieren
Damit eine Kampagne erstellt werden kann, müssen *Codes für den Kampagnenstatus* eingerichtet werden. Diese Codes vereinfachen das Verwalten der Kampagnen, indem der Kampagne ein Status zugeordnet wird. So können Sie den aktuellen Status der Kampagne sowie den nächsten Schritt der Kampagne ablesen, während die einzelnen Phasen einer Kampagne durchlaufen werden. Sie können Kampagnenstatuscodes im Fenster **Kampagnenstatus** einrichten.

Für jede Kampagne, die Sie nachverfolgen möchten, kann eine Kampagnenkarte erstellt werden. Auf diesen Kampagnenkarten finden Sie auch allgemeine Informationen zu den Kampagnen.
Sie können Kampagnenposten löschen, z. B. wenn der Posten eine Aktion speichert, die storniert wurde. Es können nur stornierte Kampagnenposten gelöscht werden.

### <a name="selecting-the-target-audience"></a>Auswählen der Zielgruppe
Nachdem eine Kampagne erstellt wurde, können Sie mit dem Erstellen von Segmenten für die Kampagnen beginnen und das Zielsegment festlegen. Weitere Informationen finden Sie unter [Segmente verwalten](marketing-segments.md).

### <a name="registering-discount-percentages"></a>Erfassen von Rabattprozentsätzen
Nachdem Sie Ihre Kampagne eingerichtet haben, entschieden haben, welche Segmente die Kampagne umfassen soll, und das Start- und Enddatum festgelegt haben, erfassen Sie den Rabattprozentsatz, den der Debitor auf die einzelnen Artikel in den Zeilen des Fensters **Verkaufszeilenrabatt** erhält. Sie können die Verkaufspreise der einzelnen Artikel in den Zeilen im Fenster **Verkaufspreise** auch erfassen. Sie können auf beide Fenster von der Kampagnenkarte zugreifen.

 Nachdem Sie die Verkaufspreise/Zeilenrabatte sowie die Segmente auf der Kampagnenkarte eingerichtet haben, müssen Sie sie aktivieren, so dass die Kampagnenpreise/Rabatte in den Zeilen wiedergegeben werden.

**Hinweis**: Um die Verkaufspreise/Zeilenrabatte zu aktivieren, müssen Sie das gesamte Segment oder nur einzelne Kontakte für die Kampagne markieren. Wenn die Verkaufspreise/Zeilenrabatte für alle Kontakte des Segments gelten sollen, wählen Sie im Fenster **Segment** auf dem Inforegister **Kampagne** das Feld **Kampagnenziel** aus.
Wenn die Verkaufspreise/Zeilenrabatte nicht für alle Kontakte des Segments gelten sollen, können Sie das Feld **Kampagnenziel** für die relevanten Kontakte. Wenn Sie dieses Feld nicht sehen, können Sie es zur Ansicht hinzuzufügen. Weitere Informationen finden Sie unter [Benutzer-Personalisierung](ui-user-personalization.md).

## <a name="conducting-campaigns"></a>Kampagnen durchführen
Während der gesamten Laufzeit der Kampagne werden alle Interaktionen mit den Kontakten bzw. mit dem Segment erfasst. Dadurch können Sie oder andere Gruppen eine Kampagne anzeigen und statistische oder andere Informationen zu Kosten und Erfolgsraten der Kampagne abrufen.

Kampagnen werden vom Verkäufer geleitet werden, und Sie müssen Aktivitäten erstellen, um jede Aufgabem  anzuzeigen und dem entsprechende Verkäufer zuzuordnen. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Verkaufschancen für Verkaufsprozesse und Prozess-Stufen](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="see-also"></a>Siehe auch
[Kontakte verwalten](marketing-contacts.md)  
[Verwalten von Segmenten](marketing-segments.md)  
[Verkaufschancen verwalten](marketing-manage-sales-opportunities.md)  
[Arbeiten mit Financials](ui-work-product.md)  

