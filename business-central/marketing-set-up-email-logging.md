---
title: E-Mail-Protokollierung einrichten | Microsoft Docs
description: Erfahren Sie, wie Sie E-Mail-Interaktionen zwischen Verkäufern und Kunden in echte Verkaufschancen verwandeln können.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 13699c002402b6b6d32edc13dca3710fefff2129
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181258"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Verfolgen Sie den Austausch von E-Mail-Nachrichten zwischen Verkäufern und Kontakten
Machen Sie mehr aus der Kommunikation zwischen Verkäufern und Ihren bestehenden oder potenziellen Kunden, indem Sie den E-Mail-Austausch nachverfolgen und diese dann in umsetzbare Gelegenheiten umwandeln. [!INCLUDE[d365fin](includes/d365fin_md.md)] kann mit Exchange Online arbeiten, um ein Protokoll der eingehenden und ausgehenden Nachrichten zu erhalten. Sie können den Inhalt jeder Nachricht auf der Seite **Aktivitätenprotokollposten** anzeigen und analysieren.

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085401]

## <a name="setting-up-d365fin-to-log-email-messages"></a>Einrichten von [!INCLUDE[d365fin](includes/d365fin_md.md)], um E-Mail-Nachrichten zu protokollieren
Beginnen Sie mit der E-Mail-Protokollierung in zwei einfachen Schritten:

1. Verbinden Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Exchange Online für Ihr Office 365-Abonnement. Exchange Online verarbeitet Ihre E-Mail-Nachrichten. Wir haben diesen Schritt vereinfacht, indem wir eine Anleitung für Unterstützte Einrichtung bereitgestellt haben. Sie benötigen lediglich Ihre Administratoranmeldeinformationen für Ihr Administratorkonto in Office 365. Um die Anleitung zu starten, gehen Sie zu **Unterstützte Einrichtung**, und wählen Sie dann **E-Mail-Protokollierung einrichten** aus. 
2. Stellen Sie sicher, dass in [!INCLUDE[d365fin](includes/d365fin_md.md)] gültige E-Mail-Adressen für Ihre Verkäufer und Kontakte eingegeben wurden, je nachdem, ob es sich um potenzielle oder bestehende Kunden handelt. Öffnen Sie dazu für jeden Kunden oder Verkäufer die Karte **Kontakt**oder **Verkäufer/Käufer**, und überprüfen Sie das Feld **E-Mail**.

> [!Tip]
> Nachdem Sie die Schritte in der Anleitung ausgeführt haben, können Sie überprüfen, ob die Verbindung erfolgreich war. Suchen Sie nach **Marketingeinrichtung**, wählen Sie **Verarbeiten** aus, dann **Funktionen**, und dann **E-Mail-Protokollierungseinr. überprüfen** aus.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Anzeigen des E-Mail-Nachrichtenaustauschs im Aktivitätenprotokoll
[!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt einen Eintrag auf der Seite **Aktivitätenprotokoll**, jedes Mal, wenn ein Verkäufer und ein Kontakt eine E-Mail-Nachricht austauschen. Um das Aktivitätenprotokoll anzuzeigen, öffnen Sie die Karte **Kontakt** oder **Verkäufer/Einkäufer** für die Person, und wählen Sie dann **Navigieren**, **Historie** und dann **Aktivitätenprotokollposten** aus. Es gibt einige Dinge, die wir mit jedem Eintrag im Protokoll tun können, zum Beispiel:

* Zeigen Sie den Inhalt der E-Mail-Nachricht an, die ausgetauscht wurde, indem Sie auf die Aktion **Dateianhänge anzeigen** klicken.
* Verwandeln Sie einen E-Mail-Austausch in eine Verkaufschance: Wenn ein Eintrag vielversprechend aussieht, können Sie ihn in eine Verkaufschance verwandeln und dann den Fortschritt in Richtung Verkauf steuern. Wählen Sie hierzu den Eintrag aus, und wählen Sie dann die Aktion **Verkaufschance erstellen** aus. Weitere Informationen finden Sie unter [Verkaufschancen verwalten](marketing-manage-sales-opportunities.md).

## <a name="see-also"></a>Siehe auch
[Verwalten von Beziehungen](marketing-relationship-management.md)

