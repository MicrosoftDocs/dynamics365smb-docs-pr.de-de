---
title: Erstellen Sie eine Sandkastenumgebung| Microsoft Docs
description: "Erstellen Sie somit eine Umgebung für das Untersuchen, Lernen, Entwickeln und Testen."
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 08/18/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b3ee160e2c38107aea1342b51d729aa172bbbc3e
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="create-a-sandbox-environment"></a>Erstellen Sie eine Sandkastenumgebung
Eine Sandboxumgebung (Vorschau) ist eine Nichtvorlegungsinstanz von[!INCLUDE[d365fin](includes/d365fin_md.md)]. Isoliert von der Produktion ist eine Sandboxumgebung der Ort, um den Dienst sicher zu untersuchen, erfahren, testen und entwickeln, ohne das Risiko des Beeinflussens der Daten und Einstellungen Ihrer Fertigungsumgebungen zur riskieren.

## <a name="to-create-a-sandbox-environment"></a>Erstellen Sie eine Sandkastenumgebung
Sie müssen ein Abonnement haben, um [!INCLUDE[d365fin](includes/d365fin_md.md)] in der zu Lage sein, eine Sandboxumgebung zu erstellen. Es kann nur eine Sandboxumgebung pro Abonnement geben.

1. Melden Sie sich in Ihrer Produktionsinstanz des [!INCLUDE[d365fin](includes/d365fin_md.md)] Services an.
2. Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seiten- oder Berichtsymbol suchen") und geben **Sandkasten-Umgebung** ein und wählen dann den zugehörigen Link aus.
![Sandkastenumgebung einrichten.](./media/across-sandbox/sandbox-environment-setup.png)
3. Wählen Sie **Erstellen** aus.  
  Eine andere Registerkarte in Ihrem Browser wird geöffnet für das Abschließen der Einrichtung der Sandkastenumgebung.
> [!NOTE]  
>  Wenn Sie Popupblocker aktiviert haben in Ihrem Browser, bearbeiten sie diese, um URLs der *.financials.dynamics.com-Adresse zu ermöglichen.   

4. Wenn die Sandkastenumgebung bereitsteht, werden Sie zum Begrüßung-Assistenten der Sandkastenumgebung umgeleitet.
![Sandkasten-Begrüßung-Assistent](./media/across-sandbox/sandbox-wizard.png)

5. Wählen Sie **Weitere Informationen**, um über Szenarien zu lesen, die Sie in einer Sandkastenumgebung versuchen können. Oder, wählen Sie **Schließen**, um zum Rollencenter Ihrer Sandkastenumgebung[!INCLUDE[d365fin](includes/d365fin_md.md)] zu gehen.
6. Oben im Rollencenters wird eine Benachrichtigung angezeigt, die bestätigt, dass dies eine Sandkastenumgebung ist. Der Typ dieser Umgebung wird in der Titelleiste des Clients anzeigen.
![Sandkasten-Rollencenter-Benachrichtigung](./media/across-sandbox/sandbox-rolecenter-notification.png)  
In der Sandboxumgebung wurde ein neuer Tenant erstellt. Dieser Tenant wird mit Vorgabe-Demodaten für den CRONUS-Mandanten geladen. Keine Daten werden kopiert oder anderswie von der Fertigungsumgebungen während der Sandkastenerstellung transferiert.
7.  Jederzeit können Sie zur Seite **Sandkastenumgebung** zurückkehren und die Sandkastenumgebung zurücksetzen.
> [!NOTE]  
>  Das Zurücksetzen der Sandkastenmgebung, wird sie komplett entfernen und dann wieder erstellt mit den Vorgabe-Demodaten.  

8.  Um zwischen Produktions- und Sandkastenumgebung zu wechseln, können Sie das App-Startprogramm Finance and Operations, Business edition verwenden.
![Sandkasten Dynamics365 Menü](./media/across-sandbox/sandbox-dynamics365-menu.png)

9.  Es ist für einen Administrator oder einen anderen Benutzer möglich, den Zugriff für mehrere Benutzer auf der Sandkastenumgebung herzustellen oder zu sperren. Dies kann geschehen, indem die Standardsicherheitsfunktionen des Produkts, wie die Benutzerkarte, der Benutzergruppen und die Zugriffsrechtsätze verwendet wird.

![Berechtigungssätze für Sandkasten](./media/across-sandbox/sandbox-permission-sets.png)

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Erweiterte Funktionen der Sandkastenumgebung
### <a name="the-in-client-designer"></a>In-Client Designer.
In einer Sandkastenumgebung finden Sie die In-Client Designerfunktion aktiviert, die Sie durch Klicken auf das Design-Symbol aktivieren können ![Designerin](./media/across-sandbox/sandbox-inclient-design-icon.png) auf einer Seite.

![In-Client Designer](./media/across-sandbox/sandbox-inclient-designer.png)

### <a name="enable-the-advanced-user-experience"></a>Aktivieren Sie die erweiterte Benutzererfahrung
Es ist möglich, die erweiterte (vollständige) Funktion eines Sandkastentenants in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu aktivieren,  indem Sie das Feld **Erfahrung** auf der Seite**Firmendaten** einrichten.

![Erweiterte Sandkastenumgebung](./media/across-sandbox/sandbox-advanced.png)

![Sandkasten-Produktion](./media/across-sandbox/sandbox-production.png)

Nachdem Sie die Funktion "Erweiterter Funktionalität in einem Sandkastentenant" aktiviert haben, erhalten Sie Zugriff auf alle Standardprofile und Rollencenter. Sie können einen Auswertungsmandanten erstellen, der vollständig eingerichtet wird, einschließlich Demodaten und Zugriff in den erweiterten Bereichen des Produkts.

![Sandkasten neues Unternehmen](./media/across-sandbox/sandbox-newcompany.png)


## <a name="see-also"></a>Siehe auch
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

