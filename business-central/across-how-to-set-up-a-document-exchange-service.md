---
title: 'Gewusst wie: Einrichten eine Belegaustauschdienstes | Microsoft Docs'
description: Sie verwenden einen externen Anbieter zum Austausch elektronischer Belege mit Ihren Handelspartnern.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6a9bba4d097ca24de094f153c91d7888811cdfd4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241192"
---
# <a name="set-up-a-document-exchange-service"></a>So richten Sie einen Belegaustauschdienst ein
Sie verwenden einen externen Anbieter zum Austausch elektronischer Belege mit Ihren Handelspartnern. Weitere Informationen finden Sie unter [Daten elektronisch austauschen](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>So richten Sie einen Belegaustauschdienst ein  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Dokumentenaustausch einrichten** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Benutzeragent**|Geben Sie beliebigen Text ein, über den Sie Ihr Unternehmen im Belegaustauschdienst identifizieren können|  
    |**Tenant-ID Belegaustausch**|Geben Sie den Tenant beim Belegaustauschdienst an, der Ihrem Unternehmen entspricht. Dieser wird vom Anbieter des Belegaustauschdienstes bereitgestellt.|  
    |**Aktiviert**|Legen Sie fest, ob der Belegaustauschdienst aktiviert ist. **Hinweis:**  Sobald Sie den Service aktivieren, werden mindestens zwei Aufgabenwarteschlangenposten erstellt, um den Verkehr von elektronischen Belegen zu und von [!INCLUDE[d365fin](includes/d365fin_md.md)] zu verarbeiten. Wenn Sie den Service deaktivieren, werden die Projektwarteschlangenposten gelöscht.|  
    |**Anmeldungs-URL**|Geben Sie die Webseite an, auf der Sie sich für den Belegaustauschdienst anmelden.|  
    |**Dienste-URL**|Geben Sie die Adresse des Belegaustauschdienst an, die aufgerufen wird, wenn Sie elektronische Belege versenden und erhalten.|  
    |**Anmelde-URL**|Geben Sie die Anmeldeseite für den Belegaustauschdienst an. Hier geben Sie den Benutzernamen und das Kennwort Ihres Unternehmens für die Anmeldung beim Service ein.|  
    |**Verbraucherschlüssel**|Geben Sie den dreiteiligen OAuth-Schlüssel für den Consumer-Schlüssel ein. Dieser wird vom Anbieter des Belegaustauschdienstes bereitgestellt.|  
    |**Verbrauchergeheimschlüssel**|Geben Sie das Geheimnis ein, das den Consumer-Schlüssel schützt. Dieser wird vom Anbieter des Belegaustauschdienstes bereitgestellt.|  
    |**Token**|Geben Sie den dreiteiligen OAuth-Schlüssel für das Token ein. Dieser wird vom Anbieter des Belegaustauschdienstes bereitgestellt.|  
    |**Tokengeheimschlüssel**|Geben Sie das Geheimnis ein, das das Token schützt. Dieser wird vom Anbieter des Belegaustauschdienstes bereitgestellt.|  

    > [!NOTE]  
    > Sie informieren Daten werden verschlüsselt automatisch an.

## <a name="see-also"></a>Siehe auch  
[Einrichten eines Datenaustauschs](across-set-up-data-exchange.md)  
[Daten elektronisch austauschen](across-data-exchange.md)
