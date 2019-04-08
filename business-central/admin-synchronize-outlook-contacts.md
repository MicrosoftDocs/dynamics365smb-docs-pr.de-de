---
title: Teilen Sie Kontakte zwischen Business Central und Outlook| Microsoft Doc
description: Der Service hat eine tiefe Integration mit Office 365, damit Sie Kontakten zwischen Outlook und Business Central freigeben können.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Office 365
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: 5e4bd35edea680c46cb0df753b50916b1aeb93be
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "799264"
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Synchronisieren Sie Kontakte in Business Central mit Kontakten in Microsoft Outlook
Sie können die gleichen Kontakte sehen in [!INCLUDE[d365fin](includes/d365fin_md.md)] wie in Outlook, wenn Sie die Kontaktsynchronisierung einrichten. Wenn Sie beispielsweise ein Verkäufer sind, können Sie einige Arbeit in Outlook und einige Arbeit in [!INCLUDE[d365fin](includes/d365fin_md.md)] erledigen. Wenn die Kontakte an beiden Stellen identisch sind, wird die Arbeit einfacher.  

Ein dedizierter Ordner in Outlook macht es einfach, Kontakte zu finden, und Sie können einen Filter setzen, um nur die Kontakte von [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisierenen, die Sie in Outlook anzeigen möchten. Sobald die Kontaktsynchronisierung eingerichtet ist, können Sie die Synchronisierung manuell beginnen oder eine automatische Synchronisierung einrichten, die Kontakte nach einem Zeitplan synchronisiert.  

## <a name="set-up-synchronization"></a>Synchronisierung einrichten
Sie geben an, wie Sie die Synchronisierung der Kontakte mit Outlook einrichten möchten auf der Seite **Exchange Synchronisierung einrichten** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Als Voraussetzung muss Ihr Benutzerprofil [!INCLUDE[d365fin](includes/d365fin_md.md)] Ihr E-Mail-Konto in Office 365 angeben. Sie können dies im Abschnitt **Office 365 Authentifizierung** des Benutzerprofils in der Übersicht **Benutzer** überprüfen.  

Auf der Seite **Exchange Synchronisierung einrichten** können Sie die Verbindung mit Exchange überprüfen und die Synchronisierung von Kontakten festlegen. Öffnen Sie die Seite **Kontaktsynchronisierung einrichten** und starten Sie die Synchronisierung. Optional können Sie einen Filter für die Kontakte setzen, die Sie zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und Outlook synchronisieren möchten. Beispielsweise können Sie einen Filter für Namen, Art, Unternehmen oder ähnlichem festlegen. Sie können den Standardnamen des Ordners auch ändern, der die Kontakte in Outlook synchronisiert. Der Standardname ist *Business Central*.  

Sobald diese Synchronisierung eingerichtet wurde, werden Änderungen. die Sie an Kontakten entweder in Outlook oder in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen, miteinander synchronisiert.  

Jeder Ihrer Mitarbeiter kann die eigene Exchange-Synchronisierung einrichten und die eigenen Filder für die Synchronisierung von Kontakten einrichten.  

## <a name="synchronize-contacts"></a>Kontakte synchronisieren
Wenn Sie es gewohnt sind, in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Kontakten zu arbeiten, dann werden Sie es einfach finden, die Synchronisierung manuell aus der Liste **Kontakte** zu starten, wenn es für Sie passt. Wählen Sie einfach **Synchronisierung mit Office 365** aus, und entscheiden Sie sich dann, wenn Sie den Filter ändern möchten, den Sie eingerichtet haben. Wenn Sie die Schaltfläche OK auswählen, wird die Synchronisierung sofort gestartet und die letzten Änderungen werden Ihren Kontakten in Outlook hinzugefügt.  

In der Liste **Kontakte** können Sie Kontakte auf zwei Wege synchronisieren:

* **Mit Office 365** synchronisieren

  Diese Aktion synchronisiert alle Änderungen in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu Office 365 seit der letzten Synchronisierung, basierend auf dem letzten Änderungsdatum. Alle neuen Kontakte von Office 365 werden auch wieder in [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisiert. Dies ist typischerweise schneller als eine vollständige Synchronisierung.  

* **Vollständig synchronisieren mit Office 365**

  Diese Aktion synchronisiert alle Kontakte in beide Richtungen unabhängig vom letzten Synchronisierungsdatum und der letzten Änderung.  

In beiden Fällen werden nur Kontakte von Outlook synchronisiert, wenn die erforderlichen Felder ausgefüllt sind. Die erforderlichen Felder zur Synchronisieren in Office 365 sind **Name**, **E-Mail-Adresse** und sie müssen vom Typ Person sein. [!INCLUDE[d365fin](includes/d365fin_md.md)] ist die Mastertabelle der Kontaktinformationen, sodass [!INCLUDE[d365fin](includes/d365fin_md.md)] die Kontaktinformationen im Fall der Dubletten gespeichert.  

In Outlook werden die Kontakte [!INCLUDE[d365fin](includes/d365fin_md.md)] in einem Ordner unter **Andere Kontakte** in der Ansicht **Personen** angezeigt. Wenn Sie nicht mit den Personen-Ansicht in Outlook vertraut sind, können Sie diese von den Navigationsoptionen in der unteren linken Ecke von Outlook erhalten.  

## <a name="see-also"></a>Siehe auch
[Erste Schritte](product-get-started.md)  
[Finanzen](finance.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Mittels der Kontakte (Personen) in Outlook im Netz](https://support.office.com/en-us/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  
