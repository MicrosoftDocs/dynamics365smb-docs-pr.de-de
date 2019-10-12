---
title: So können Sie vorhandene Datenbank-Daten prüfen und anpassen | Microsoft Docs
description: Wenn Sie ein Konfigurationspaket für eine Lösung erstellen, können Sie die verfügbaren Datenbankdaten anzeigen und anpassen, um Ihren Debitoranforderungen entsprechen. Die Datenbanktabelle muss eine zugeordnete Seite haben.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: admin-how-to-create-custom-company-configuration-packages
ms.openlocfilehash: 295329bf7f665a9dd34194b211a5ef65a7a65d4c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308014"
---
# <a name="review-and-customize-existing-database-data"></a>So können Sie vorhandene Datenbank-Daten prüfen und anpassen.
Wenn Sie ein Konfigurationspaket für eine Lösung erstellen, können Sie die verfügbaren Datenbankdaten anzeigen und anpassen, um Ihren Debitoranforderungen entsprechen. Die Datenbanktabelle muss eine zugeordnete Seite haben.  

### <a name="to-customize-data-in-the-database"></a>So passen Sie Daten in der Datenbank an.  

1.  Identifizieren Sie im Konfigurationsarbeitsblatt die Tabellen, deren Daten Sie anzeigen oder anpassen möchten.  

    > [!NOTE]  
    >  Stellen Sie sicher, dass jede Tabelle eine Seiten-ID hat, die ihr zugeordnet ist. Für Standard [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabellen wird dieser Wert automatisch ausgefüllt. Für benutzerdefinierte Tabellen müssen Sie die ID zur Verfügung stellen  

2.  Wählen Sie auf der Registerkarte **Aktionen** in der Gruppe **Anzeigen** die Option **Datenbankdaten** aus.  

     Das [!INCLUDE[d365fin](includes/d365fin_md.md)]-Fenster für die Seite wird geöffnet.  

3.  Überprüfen Sie die verfügbaren Informationen. Ändern Sie sie bei Bedarf, indem Sie Datensätze löschen, die nicht relevant sind oder indem Sie neue hinzufügen.  

## <a name="see-also"></a>Siehe auch  
 [So verwalten Sie eine Mandantenkonfiguration in einem Arbeitsblatt](admin-how-to-manage-company-configuration-in-a-worksheet.md)
