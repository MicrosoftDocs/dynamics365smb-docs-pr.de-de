---
title: So konfigurieren Sie einen Mandanten mit dem RapidStart-Assistenten | Microsoft Docs
description: Sie können einen neuen Mandanten, den Sie erstellt haben, schnell konfigurieren, indem Sie den RapidStart Services-Konfigurations-Assistenten verwenden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: 63120671100b7caac7f3cb08bd3fbbcd1d29ff5c
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798814"
---
# <a name="configure-a-company-with-the-rapidstart-wizard"></a>So konfigurieren Sie einen Mandanten mit dem RapidStart-Assistenten.
Sie können einen neuen Mandanten, den Sie erstellt haben, schnell konfigurieren, indem Sie den RapidStart Services-Konfigurations-Assistenten verwenden.

Im folgenden Verfahren haben Sie dem Debitor das Konfigurationspaket bereitgestellt, das dann auf einem Computer installiert wird. Der Debitor öffnet den neuen Mandanten, der keine Debitorendaten enthält. Sie oder der Debitormandant folgt den Schritten im RapidStart Services-Assistenten, die in diesem Verfahren beschrieben werden, um grundlegende Informationen über den Mandanten bereitzustellen. Der Assistent importiert das Konfigurationspaket und überträgt das Paket Buchungen auf den Mandanten.  

## <a name="to-configure-a-new-company"></a>So konfigurieren Sie einen neuen Mandanten.  
1. Im Feld RapidStart-Dienste-Implementierungs-Rollencenter wählen Sie die **RapidStart-Assistent** Aktion aus.  
2. Erweitern Sie das Inforegister **Schritt 1**, das allgemeine Informationen über den neuen Mandanten enthält. Geben Sie die entsprechenden Daten über den neuen Mandanten in die Felder ein. Es gibt ein Feld, das ausgefüllt werden muss, **Name**. Die restlichen Felder sind optional.  
3. Erweitern Sie das Inforegister **Schritt 2**, das Kommunikations- und Kontaktinformationen über den neuen Mandanten enthält. Geben Sie die entsprechenden Daten über den neuen Mandanten in die Felder ein.
4. Erweitern Sie das Inforegister **Schritt 3**, das Bankkonto- und Zahlungsinformationen über den neuen Mandanten enthält. Geben Sie die entsprechenden Daten über den neuen Mandanten in die Felder ein.  
5. Erweitern Sie das Inforegister **Schritt 4**. Wählen Sie die Schaltfläche **AssistEdit**, um das Konfigurationspaket auszuwählen, das Sie ausgleichen möchten. Der Name des Konfigurationspakets wird angezeigt. Sie können folgende Aktionen in der aufgeführten Reihenfolge durchführen:  

    1. Wenden Sie die Konfiguration an, indem Sie die **Paket übernehmen** Aktion auswählen. Dadurch wird das Konfigurationspaket importiert und übernimmt die Paketdatenbankdaten alle gleichzeitig.  

    2. Überprüfen Sie die Konfiguration, nachdem sie angewendet wurde. Mit dieser Option können Sie die Konfigurationsdetails und -fragebögen überprüfen, die aus vom Partner bereitgestellt wurden, und Stammdaten importieren, die für Ihren Mandanten erforderlich sind. Wählen Sie die Aktion **Arbeitsblatt konfigurieren** aus. Weitere Informationen finden Sie unter [So füllen Sie den Konfigurationsfragebogen aus](admin-gather-customer-setup-values.md#to-complete-the-configuration-questionnaire).  

6. Erweitern Sie das Inforegister **Schritt 5**. Geben Sie an, welches Rollencenter die Standardeinstellung für den neuen Mandanten sein soll.  

    > [!IMPORTANT]  
    >  Ändern Sie das Rollencenter erst, nachdem Sie die Konfiguration des Mandanten abgeschlossen haben. Wenn Sie weitere Einrichtungsdetails zu berücksichtigen haben, verwenden Sie erst das Konfigurationsarbeitsblatt, um mit Ihrer Arbeit fortzufahren. Kehren Sie dann zu dem Assistenten zurück, um Ihr Rollencenterprofil zu aktualisieren, oder wählen Sie auf der Registerkarte Start die Option **Vollständiges Setup** aus.

7. Wählen Sie die Schaltfläche **OK** aus.  
8. Um sicherzustellen, dass die Konfigurationsinformationen für den neuen Mandanten übernommen wurden, geben Sie im Feld ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") ein, wählen **Unternehmensinformation**und wählen Sie dann den zugehörigen Link aus.

Das Fenster **Firmendaten** enthält Informationen, die Sie festgelegt haben.   

Jetzt haben Sie den Mandanten konfiguriert und Daten für ihn übernommen.  

## <a name="see-also"></a>Siehe auch  
[Übernehmen von Konfiguration in neue Mandanten](admin-apply-configuration-to-new-companies.md)  
[Einrichten von Mandanten mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)
