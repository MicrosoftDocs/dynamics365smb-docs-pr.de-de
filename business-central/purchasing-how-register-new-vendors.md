---
title: Eine Lieferantenkarte erstellen, um einen neuen Lieferanten zu registrieren (enthält ein Video)
description: In diesem Thema erfahren Sie, wie Sie eine Kreditorenkarte erstellen, um einen neuen Kreditor oder Lieferanten zu registrieren und Kreditorenkarten als Vorlage zu speichern.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.search.form: 26, 27, 34, 461, 786, 1379, 1385, 1386, 1628
ms.date: 09/29/2021
ms.author: edupont
ms.openlocfilehash: 1cbdf85f08939aa05c013901239bbd390400f3e1
ms.sourcegitcommit: c05806689d289d101bd558696199cefbd989473e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2022
ms.locfileid: "8115502"
---
# <a name="register-new-vendors"></a>Registriert einen neuen Kreditor

Kreditoren stellen die Produkte bereit, die Sie verkaufen. Jeder Kreditor, von dem Sie kaufen, muss als Kreditorenkarte erfasst werden.

Bevor Sie neue Kreditoren erfassen können, müssen Sie verschiedene Einkaufscodes einrichten, aus denen Sie auswählen können, wenn Sie Kreditorenkarten ausfüllen. Nach der Erstellung aller erforderlichen Masterdaten können weitere Konfigurationsschritte für den Mandanten – wie Priorisieren des Kreditors zu Zahlungszwecken oder Aufführen von Artikeln, die von diesem und anderen Kreditoren geliefert werden – ausgeführt werden. Eine weitere Gruppe von Einrichtungsaufgaben bildet die Erfassung von Vereinbarungen zu Rabatten, Preisen und Zahlungsformen. Weitere Informationen finden Sie unter [Einrichten des Einkaufs](purchasing-setup-purchasing.md).

Kreditorenkarten verwahren die Informationen, die benötigt werden, um Produkte vom Kreditor einzukaufen. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md) und [Neue Artikel registrieren](inventory-how-register-new-items.md).

> [!NOTE]  
> Wenn es Kreditorenvorlagen für verschiedene Kreditorenarten gibt, dann erscheint eine Seite automatisch, wenn Sie eine neue Kreditorenkarte erstellen, von der aus Sie eine entsprechende Kreditorenvorlage auswählen können. Wenn nur eine Kreditorenvorlage vorhanden ist, verwenden neue Kreditorenkarten immer diese Vorlage.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a>Hinzufügen neuer Kreditoren
Sie können neue Kreditoren manuell hinzufügen, indem Sie die Felder auf der Seite **Kreditorkarte** ausfüllen, oder Sie können Vorlagen verwenden, die vordefinierte Informationen enthalten. Sie können zum Beispiel Vorlagen für verschiedene Arten von Lieferantenprofilen erstellen. Die Verwendung von Vorlagen spart Zeit beim Hinzufügen neuer Kreditor und hilft sicherzustellen, dass die Informationen jedes Mal korrekt sind. Wenn Sie Vorlagen für mehr als einen Kreditorentyp erstellen, können Sie die Vorlage auswählen, die Sie beim Hinzufügen eines Kreditors verwenden möchten. Wenn Sie nur eine Vorlage erstellen, wird diese für alle neuen Lieferanten verwendet. Nachdem Sie eine Vorlage erstellt haben, können Sie die Aktion **Vorlage anwenden** verwenden, um sie auf einen oder mehrere ausgewählte Kreditoren anzuwenden. Um eine Vorlage zu erstellen, geben Sie die Informationen, die Sie wiederverwenden möchten, auf der Seite Lieferantenkarte ein und speichern sie dann als Vorlage. Weitere Informationen finden Sie unter [Speichern der Kreditor Card Seite als Vorlage](purchasing-how-register-new-vendors.md#to-save-the-vendor-card-as-a-template).

> [!TIP]
> Es kann hilfreich sein, die Seite **Lieferantenvorlage** zu personalisieren, wenn Sie eine Vorlage erstellen. So können Sie beispielsweise ein Feld hinzufügen, das auf der Seite noch nicht angezeigt wird. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Sie können einen Kreditor auch aus einem Kontakt erstellen. Weitere Informationen finden Sie unter [Um einen Kunden, Kreditor, Mitarbeiter oder ein Bankkonto aus einem Kontakt zu erstellen](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact). 

### <a name="to-create-a-new-vendor"></a>So erstellen Sie einen neuen Kreditor

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

> [!TIP]  
> Falls Sie nicht im Voraus wissen, ob eine bestimmte Rechnungsadresse für jede Rechnung eines Kreditoren verwendet wird, füllen Sie das Feld **Kreditorennr.** auf der Kreditorenkarte nicht aus. Geben Sie stattdessen die Zahlung-an Kred.-Nr. später ein, wenn Sie eine Einkaufsanfrage, -bestellung oder -rechnung erstellen.

Der Kreditor ist nun erfasst und die Kreditorenkarte ist bereit, in Einkaufsbeleg verwendet zu werden, in denen Sie mit dem Kreditor handeln.

Wenn Sie diese Kreditorenkarte als Vorlage verwenden möchten, wenn Sie neue Kreditorenkarten erstellen, dann fahren sie fort, um sie als Kreditorenvorlage zu speichern. Weitere Informationen finden Sie im Abschnitt [So speichern Sie die Kreditorenkarte als Vorlage](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-and-editing-vendor-information"></a>Löschen und Bearbeiten von Kreditor-Informationen

Sie können die Informationen auf Kreditorenkarten jederzeit bearbeiten. Wenn Sie jedoch eine Transaktion für einen Kreditor gebucht haben, können Sie die Karte nicht löschen, da die Posten für die Buchprüfung benötigt werden könnten. Zum Löschen von Kreditorkarten wenden Sie sich an Ihren Microsoft-Partner, um dies über einen Code durchzuführen.

> [!TIP]
> Sie können die IBAN eines Kreditor-Bankkontos ändern, ohne dass sich die Änderung auf Ihre historischen Überweisungsregistereinträge auswirkt. Überweisungsregistereinträge speichern die Empfänger-IBAN und die Empfänger-Bankkontonummer, die beim Erstellen der Einträge in den Feldern Kreditor Bankkonto und Empfängername auf der Seite Kreditor-Karte angegeben wurden.


## <a name="to-save-the-vendor-card-as-a-template"></a>So speichern Sie die Kreditorenkarte als Vorlage

1. Wählen Sie auf der Seite **Kreditorenkarte** die Aktion **Als Vorlage speichern** aus. Die Seite **Kreditorenvorlage** wird geöffnet und zeigt die Kreditorenkarte als Vorlage.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um Dimensionen in den Vorlagen wiederzuverwenden, wählen Sie die Aktion **Dimensionen**. Die Seite **Dimensionen Vorlagen** wird geöffnet und zeigt alle Dimensionscodes, die für den Kreditor eingerichtet werden.
4. Bearbeiten Sie oder geben Sie Dimensionscodes ein, die für die neuen Kreditorenkarten gelten, die mit der Vorlage erstellt wurden.
5. Wenn Sie die neue Kreditorvorlage abgeschlossen haben, klicken Sie auf die Schaltfläche **OK**.  
   Die Kreditorvorlage wird der Liste von Kreditorvorlagen hinzugefügt, damit Sie diese verwenden können, um neue Kreditorenkarten zu erstellen.

## <a name="see-also"></a>Siehe auch

[Doppelt Datensätze zusammenführen](sales-how-merge-duplicate-records.md)  
[Erstellen von Nummernkreisen](ui-create-number-series.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Erfassen eines Einkaufs](purchasing-how-record-purchases.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]