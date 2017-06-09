---
title: 'So gehts: Neue Kunden registrieren | Microsoft Docs'
description: 'Vorgehensweise: Einen neuen Debitor registrieren'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6789e6a4129789e950c7f71ff86e62263ae9c087
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-register-new-customers"></a>Vorgehensweise: Einen neuen Debitor registrieren
Debitoren sind die Herkunft des Erträge. Jeder Debitor, an den Sie verkaufen, muss als Debitorenkarte erfasst werden. Debitorenkarten verwahren die Informationen, die benötigt werden, um dem Debitoren Produkte zu verkaufen. Weitere Informationen finden Sie unter [Vorgehensweise: Fakturieren von Verkäufen](sales-how-invoice-sales.md) und [Vorgehensweise: Neue Artikel erfassen](inventory-how-register-new-items.md).  

Bevor Sie neue Debitoren erfassen können, müssen Sie verschiedene Verkaufscodes einrichten, aus denen Sie auswählen können, wenn Sie Debitorenkarten ausfüllen. Weitere Informationen finden Sie unter [Einrichten von Verkäufen](sales-setup-sales.md).

**Hinweis**: Wenn es Debitorenvorlagen für verschiedene Debitorenarten gibt, dann erscheint ein Fenster automatisch, wenn Sie eine neue Debitorenkarte erstellen, von der aus Sie eine entsprechende Debitorenvorlage auswählen können. Wenn nur eine Debitorenvorlage vorhanden ist, verwenden neue Debitorenkarten immer diese Vorlage.

## <a name="to-create-a-new-customer-card"></a>Erstellen Sie eine neue Debitorenkarte
1. Auf der Startseite wählen Sie **Debitoren**, um die Liste der Bestandsdebitorenkarten zu öffnen.  
2. Wählen Sie im Fenster **Kunden** die Aktion **Neu** aus.

    Wenn nur eine Debitorenvorlage vorhanden ist, dann öffnet sich eine neue Debitorenkarte mit den Feldern, die mit Daten aus der Vorlage ausgefüllt werden.

    Wenn mehr als eine Debitorenvorlage vorhanden ist, dann öffnet sich ein Fenster mit verfügbaren Debitorenvorlagen automatisch. In diesem Fall, folgen Sie den nächsten zwei Schritten.
3. Im Fenster **Vorlage für neuen Kunden wählen** wählen Sie die Vorlage, die Sie für die neue Debitorenkarte verwenden möchten.
4. Wählen Sie die Schaltfläche **OK** aus. Eine neue Debitorenkarte wird geöffnet mit den Feldern, die mit Daten aus der Vorlage ausgefüllt werden.  
5. Fahren Sie fort, um Felder auf der Debitorenkarte bei Bedarf auszufüllen und zu ändern. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Definieren Sie im Inforegister **Verkaufspreise und VK-Zeilenrabatte** spezielle Preise oder Skontowerte, die Sie dem Debitor gewähren, wenn bestimmte Kriterien, wie z.B. Artikel, Mindestbestellmenge oder Enddatum erfüllt sind. Jede Zeile stellt einen Sonderpreis oder einen Zeilenrabatt dar. Jede Spalte stellt ein Kriterium an, das gelten muss, um den Sonderpreis, den Sie im **Einheitenpreis**-Feld eingeben, oder den Zeilenrabatt, den Sie im **Zeilenrabatt**-Feld eingeben, zu rechtfertigen. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)

Der Debitor ist nun erfasst und die Debitorenkarte ist bereit, in Geschäftsbelegen verwendet zu werden, in denen Sie mit dem Debitor handeln.

Wenn Sie diese Debitorenkarte als Vorlage verwenden möchten, wenn Sie neue Debitorenkarten erstellen, dann fahren sie fort, um sie als Debitorenvorlage zu speichern. Weitere Informationen finden Sie im folgenden Abschnitt.

## <a name="to-save-the-customer-card-as-a-template"></a>Um die Debitorenkarte als Vorlage zu speichern
1. Im Fenster **Debitorenkarte** wählen Sie die Aktion **Als Vorlage** aus. Das Fenster **Debitorenvorlage** wird geöffnet und zeigt die Debitorenkarte als Vorlage.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um Dimensionen in den Vorlagen wiederzuverwenden, wählen Sie die Aktion **Dimensionen**. Das Fenster **Dimensionen Vorlagenübersicht** wird geöffnet und zeigt alle Dimensionscodes, die für den Artikel eingerichtet werden.
4. Bearbeiten Sie oder geben Sie Dimensionscodes ein, die für die neuen Debitorenkarten gelten, die mit der Vorlage erstellt wurden.  
5. Wenn Sie die neue Debitorenvorlage abgeschlossen haben, wählen Sie die Schaltfläche **OK**.

Die Debitorenvorlage wird der Liste von Debitorenvorlagen hinzugefügt, damit Sie diese verwenden können, um neue Debitorenkarten zu erstellen.

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)    
[Einrichten von Verkäufen](sales-setup-sales.md)    
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]

