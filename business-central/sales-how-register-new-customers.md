---
title: Eine Debitorenkarte erstellen, um einen neuen Debitor zu erfassen | Microsoft Docs
description: Beschreibt, wie eine Debitorenkarte erstellt wird, um Informationen zu jedem neuen Debitor oder Clients zu erfassen, an die Sie verkaufen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 0bdc559f04064e2b4d49ef4ed7a8759c68be3579
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194043"
---
# <a name="register-new-customers"></a>Neue Debitoren registrieren
Debitoren sind die Herkunft Ihres Einkommens. Sie müssen jeden Debitor, an den Sie verkaufen, als Debitorenkarte anlegen. Debitorenkarten enthalten die Informationen, die für den Verkauf von Produkten an Debitoren erforderlich sind." Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md) und [Neue Artikel registrieren](inventory-how-register-new-items.md).  

Bevor Sie neue Debitoren erfassen können, müssen Sie verschiedene Verkaufscodes einrichten, aus denen Sie auswählen können, wenn Sie Debitorenkarten ausfüllen. Weitere Informationen finden Sie unter [Einrichten von Verkäufen](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

> [!NOTE]  
> Wenn es Debitorenvorlagen für verschiedene Debitorenarten gibt, dann erscheint eine Seite automatisch, wenn Sie eine neue Debitorenkarte erstellen, von der aus Sie eine entsprechende Debitorenvorlage auswählen können. Wenn nur eine Debitorenvorlage vorhanden ist, verwenden neue Debitorenkarten immer diese Vorlage.  

## <a name="to-create-a-new-customer-card"></a>Erstellen Sie eine neue Debitorenkarte
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Debitoren** die Aktion **Neu** aus.

    Wenn nur eine Debitorenvorlage vorhanden ist, dann öffnet sich eine neue Debitorenkarte mit den Feldern, die mit Daten aus der Vorlage ausgefüllt werden.

    Wenn mehr als eine Debitorenvorlage vorhanden ist, dann öffnet sich eine Seite mit verfügbaren Debitorenvorlagen automatisch. In diesem Fall, folgen Sie den nächsten zwei Schritten.
3. Auf der Seite **Eine Vorlage für einen neuen Debitor auswählen** wählen Sie die Vorlage, die Sie für die neue Debitorenkarte verwenden möchten.
4. Wählen Sie die Schaltfläche **OK** aus. Eine neue Debitorenkarte wird geöffnet mit den Feldern, die mit Daten aus der Vorlage ausgefüllt werden.  
5. Fahren Sie fort, um Felder auf der Debitorenkarte bei Bedarf auszufüllen und zu ändern. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Definieren Sie im Inforegister **Verkaufspreise** spezielle Preise oder Rabatte, die Sie dem Debitor gewähren, wenn bestimmte Kriterien, wie z.B. Artikel, Mindestbestellmenge oder Enddatum erfüllt sind. Jede Zeile stellt einen Sonderpreis oder einen Zeilenrabatt dar. Jede Spalte stellt ein Kriterium an, das gelten muss, um den Sonderpreis, den Sie im **VK-Preis**-Feld eingeben, oder den Zeilenrabatt, den Sie im **Zeilenrabatt**-Feld eingeben, zu rechtfertigen. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Rabatt und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)

Der Debitor ist nun erfasst und die Debitorenkarte ist bereit, in Geschäftsbelegen verwendet zu werden, in denen Sie mit dem Debitor handeln.

Wenn Sie diese Debitorenkarte als Vorlage verwenden möchten, fahren Sie fort, um sie als Debitorenvorlage zu speichern. Weitere Informationen finden Sie im folgenden Abschnitt.

## <a name="to-save-the-customer-card-as-a-template"></a>Um die Debitorenkarte als Vorlage zu speichern
1. Wählen Sie auf der Seite **Debitorenkarte** die Aktion **Als Vorlage speichern** aus. Die Seite **Debitorenvorlage** wird geöffnet und zeigt die Debitorenkarte als Vorlage.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um Dimensionen in den Vorlagen wiederzuverwenden, wählen Sie die Aktion **Dimensionen**. Die Seite **Dimensionen Vorlagen** wird geöffnet und zeigt alle Dimensionscodes, die für den Debitor eingerichtet werden.
4. Bearbeiten Sie oder geben Sie Dimensionscodes ein, die für die neuen Debitorenkarten gelten, die mit der Vorlage erstellt wurden.  
5. Wenn Sie die neue Debitorenvorlage abgeschlossen haben, wählen Sie die Schaltfläche **OK**.

Die Debitorenvorlage wird der Liste von Debitorenvorlagen hinzugefügt, damit Sie diese verwenden können, um neue Debitorenkarten zu erstellen.

## <a name="see-also"></a>Siehe auch
[Zahlungsformen definieren](finance-payment-methods.md)  
[Doppelt Datensätze zusammenführen](sales-how-merge-duplicate-records.md)  
[Erstellen von Nummernkreisen](ui-create-number-series.md)  
[Verkauf](sales-manage-sales.md)    
[Einrichten von Verkäufen](sales-setup-sales.md)    
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
