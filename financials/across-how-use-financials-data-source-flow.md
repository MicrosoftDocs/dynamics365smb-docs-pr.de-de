---
title: Nutzung Ihres Dynamics 365 for Financials in Microsoft Flow | Microsoft Docs
description: "Sie können die Finanzdaten als Datenquelle in PowerApps bereitstellen."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 03/15/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 76d24ed80adb08083c6167040be8cc6a4bcc3167
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# <a name="using-dynamics-365-for-financials-in-microsoft-flow"></a>Nutzung Ihres Dynamics 365 for Financials in Microsoft Flow
Sie können die Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)] als Teil eines Workflows in Microsoft-Flow verwenden.  

**Hinweis**: Sie müssen ein gültiges Konto mit [!INCLUDE[d365fin](includes/d365fin_md.md)] und Flow haben.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Um [!INCLUDE[d365fin](includes/d365fin_md.md)] als Datenquelle in Flow hinzufügen
1. In Ihrem Browser navigieren Sie zu [flow.microsoft.com](https://flow.microsoft.com/en-us/) und melden sich dann an.
2. Wählen Sie **My Flows** im Menüband oben auf der Seite.
3. Im Fenster **My Flows** wählen Sie die Option **Aus Leer erstellen** aus.
4. Wählen Sie aus der Liste der verfügbaren Triggern eine der beiden [!INCLUDE[d365fin](includes/d365fin_md.md)] verfügbaren Trigger aus: *Wenn ein Datensatz erstellt wird* oder *Wenn ein Datensatz geändert wird*.
5. Flow zeigt eine Verbindungsseite an, die Sie zur Eingabe der Informationen auffordert, die benötigt werden, um sich mit Ihren [!INCLUDE[d365fin](includes/d365fin_md.md)] Daten zu verbinden. Zum Verbinden müssen Sie eine OData URL, Benutzername, Mandantenname und Kennwort angeben.

   Für *OData-URL* können Sie das OData V4 URL eines der Web Services, der in ***Webdienste** auf der Seite angezeigt wird in [!INCLUDE[d365fin](includes/d365fin_md.md)]kopieren, beispielsweise `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Für den *Unternehmensname* verwenden Sie den Namen, der im Feld **Name** im Fenster **Firmendaten** in [!INCLUDE[d365fin](includes/d365fin_md.md)] angezeigt wird. Wenn Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] mehrere Unternehmen enthält, wählen Sie den entsprechenden Namen aus der Liste im Fenster **Unternehmen** aus. In beiden Fällen prüfen Sie, ob dem Namen, den Sie im Power Apps Assistenten angeben haben genau dem Text entspricht, der angezeigt wird in [!INCLUDE[d365fin](includes/d365fin_md.md)], wie z. B. `My Company`

   Für den Benutzernamen und das Kennwort verwenden Sie die Felder Name und Webdiensttastenkombination, die für Ihr Konto im **Benutzer** in [!INCLUDE[d365fin](includes/d365fin_md.md)] angegeben werden. Beispielsweise ist der Benutzername *ADMINISTRATOR* und die Webdiensttastenkombination, die als Passwort dient *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*. Weitere Informationen finden Sie unter [So geht's: Verwalten von Benutzern und Berechtigungen](ui-how-users-permissions.md).
6. Wählen Sie die Schaltfläche **Erstellen** im unteren Bereich der Seite, um den Vorgang fortzusetzen.

   Flow zeigt eine Liste der Tabellen, die in [!INCLUDE[d365fin](includes/d365fin_md.md)]verfügbar sind. Diese Tabellen oder Endpunkte stehen für alle Webdienste, die Sie von [!INCLUDE[d365fin](includes/d365fin_md.md)] veröffentlicht haben.

   Sie können einen neuen Webdienst URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen, indem Sie die **Erstellen Dataset** Aktion der Seite **Webdienste** nutzen, indem Sie die unterstütze Hilfe ** Bericht einrichten** verwenden oder die Aktion**Bearbeiten in Excel** in einer beliebigen Liste wählen.
7. Wählen Sie die Daten aus, die Sie in Flow nutzen möchten.

Zu diesem Zeitpunkt haben Sie erfolgreich Ihre Dynamics 365 Daten verbunden und sind bereit, Ihren Flow zu bauen. Weitere Informationen finden Sie in der [Flow Dokumentation](https://flow.microsoft.com/documentation/getting-started/).

## <a name="see-also"></a>Siehe auch
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](upload-data.md)  
[Vorgehensweise: Verwalten Sie Benutzer und Berechtigungen](ui-how-users-permissions.md)    
[Einrichten von [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  

