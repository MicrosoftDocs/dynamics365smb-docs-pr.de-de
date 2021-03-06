---
title: Teilen Sie Kontakte zwischen Business Central und Outlook| Microsoft Doc
description: Der Dienst ist tief in Microsoft 365 integriert, damit Sie Kontakten zwischen Outlook und Business Central freigeben können.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Microsoft 365
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1ccada415d506193e52ac37981252a47e6088971
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777166"
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Synchronisieren Sie Kontakte in Business Central mit Kontakten in Microsoft Outlook
Sie können die gleichen Kontakte sehen in [!INCLUDE[prod_short](includes/prod_short.md)] wie in Outlook, wenn Sie die Kontaktsynchronisierung einrichten. Wenn Sie beispielsweise ein Verkäufer sind, können Sie einige Arbeit in Outlook und einige Arbeit in [!INCLUDE[prod_short](includes/prod_short.md)] erledigen. Wenn die Kontakte an beiden Stellen identisch sind, wird die Arbeit einfacher.  

Ein dedizierter Ordner in Outlook macht es einfach, Kontakte zu finden, und Sie können einen Filter setzen, um nur die Kontakte von [!INCLUDE[prod_short](includes/prod_short.md)] synchronisierenen, die Sie in Outlook anzeigen möchten. Sobald die Kontaktsynchronisierung eingerichtet ist, können Sie die Synchronisierung manuell beginnen oder eine automatische Synchronisierung einrichten, die Kontakte nach einem Zeitplan synchronisiert.  

## <a name="set-up-synchronization"></a>Synchronisierung einrichten
Sie geben an, wie Sie die Synchronisierung der Kontakte mit Outlook einrichten möchten auf der Seite **Exchange Synchronisierung einrichten** in [!INCLUDE[prod_short](includes/prod_short.md)]. Als Voraussetzung muss Ihr Benutzerprofil in [!INCLUDE[prod_short](includes/prod_short.md)] Ihr E-Mail-Konto für Microsoft 365 angeben. Sie können dies im Abschnitt **Microsoft 365 Authentifizierung** Ihres Benutzerprofils in der Übersicht **Benutzer** überprüfen.  

Auf der Seite **Exchange Synchronisierung einrichten** können Sie die Verbindung mit Exchange überprüfen und die Synchronisierung von Kontakten festlegen. Öffnen Sie die Seite **Kontaktsynchronisierung einrichten** und starten Sie die Synchronisierung. Optional können Sie einen Filter für die Kontakte setzen, die Sie zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und Outlook synchronisieren möchten. Beispielsweise können Sie einen Filter für Namen, Art, Unternehmen oder ähnlichem festlegen. Sie können den Standardnamen des Ordners auch ändern, der die Kontakte in Outlook synchronisiert. Der Standardname ist *Business Central*.  

Sobald diese Synchronisierung eingerichtet wurde, werden Änderungen. die Sie an Kontakten entweder in Outlook oder in [!INCLUDE[prod_short](includes/prod_short.md)] erstellen, miteinander synchronisiert.  

Jeder Ihrer Mitarbeiter kann die eigene Exchange-Synchronisierung einrichten und die eigenen Filder für die Synchronisierung von Kontakten einrichten.  

## <a name="synchronize-contacts"></a>Kontakte synchronisieren
Wenn Sie es gewohnt sind, in [!INCLUDE[prod_short](includes/prod_short.md)] mit Kontakten zu arbeiten, dann werden Sie es einfach finden, die Synchronisierung manuell aus der Liste **Kontakte** zu starten, wenn es für Sie passt. Wählen Sie einfach **Synchronisierung mit Microsoft 365** aus, und entscheiden Sie sich dann, wenn Sie den Filter ändern möchten, den Sie eingerichtet haben. Wenn Sie die Schaltfläche OK auswählen, wird die Synchronisierung sofort gestartet und die letzten Änderungen werden Ihren Kontakten in Outlook hinzugefügt.  

In der Liste **Kontakte** können Sie Kontakte auf zwei Wege synchronisieren:

* **Mit Microsoft 365 synchronisieren**

  Diese Aktion synchronisiert alle Änderungen in [!INCLUDE[prod_short](includes/prod_short.md)] zu Microsoft 365 seit der letzten Synchronisierung, basierend auf dem letzten Änderungsdatum. Alle neuen Kontakte von Microsoft 365 werden auch wieder in [!INCLUDE[prod_short](includes/prod_short.md)] synchronisiert. Dies ist typischerweise schneller als eine vollständige Synchronisierung.  

* **Mit Microsoft 365 vollständig synchronisieren**

  Diese Aktion synchronisiert alle Kontakte in beide Richtungen unabhängig vom letzten Synchronisierungsdatum und der letzten Änderung.  

In beiden Fällen werden nur Kontakte von Outlook synchronisiert, wenn die erforderlichen Felder ausgefüllt sind. Die erforderlichen Felder für die Synchronisierung in Microsoft 365 sind **Name** und **E-Mail-Adresse**. Sie müssen vom Typ Person sein. [!INCLUDE[prod_short](includes/prod_short.md)] ist die Mastertabelle der Kontaktinformationen, sodass [!INCLUDE[prod_short](includes/prod_short.md)] die Kontaktinformationen im Fall der Dubletten gespeichert.  

In Outlook werden die Kontakte [!INCLUDE[prod_short](includes/prod_short.md)] in einem Ordner unter **Andere Kontakte** in der Ansicht **Personen** angezeigt. Wenn Sie nicht mit den Personen-Ansicht in Outlook vertraut sind, können Sie diese von den Navigationsoptionen in der unteren linken Ecke von Outlook erhalten.  

## <a name="see-also"></a>Siehe auch
[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  
[Finanzen](finance.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Mittels der Kontakte (Personen) in Outlook im Netz](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]