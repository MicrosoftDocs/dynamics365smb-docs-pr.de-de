---
title: Verwenden Sie die Daten, um eine App zu erstellen| Microsoft Docs
description: "Sie können Daten aus Business Central zur Verfügung stellen und eine OData URL Ihrer Webdienste festlegen, um eine Geschäfts-App mithilfe PowerApps zu erstellen."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: add32e82465610830b68a979e238103bfa10d438
ms.openlocfilehash: 5c07daf590fb87d318d2d3dc656e17838f23de8a
ms.contentlocale: de-de
ms.lasthandoff: 11/29/2018

---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Verknüpfung mit Business Central, um eine Geschäfts-App mithilfe PowerApps zu erstellen
Sie können die Daten [!INCLUDE[d365fin](includes/d365fin_md.md)] als Datenquelle in PowerApps bereitstellen.  

> [!NOTE]  
>   Sie müssen ein gültiges Konto mit [!INCLUDE[d365fin](includes/d365fin_md.md)] mit PowerApps haben.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>Als [!INCLUDE[d365fin](includes/d365fin_md.md)] Datenquelle in PowerApps hinzufügen
1. In Ihrem Browser navigieren und zu [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) gehen und sich dann anmelden.
2. Wählen Sie im linken Navigationsbereich **Neue App**.
3. Wählen Sie den Editor, PowerApps-Studio für Windows oder PowerApps-Studio für Internet aus.

   PowerApps-Studio für Windows ist eine Desktop-Anwendung, die verwendet wird, um PowerApps zu erstellen und zu veröffentlichen. PowerApps-Studio für Internet ist eine Online-Lösung, die verwendet wird, um PowerApps zu erstellen und zu veröffentlichen.
4. Der nächste Schritt, um ein PowerApp zu erstellen ist die Auswahl der Daten. Wählen Sie das Pfeilsymbol aus und wählen Sie dann die Option **Neue Verbindung** in der oberen linken Seite der Seite aus.
5. In der Liste der verfügbaren Verbindungscodes, wählen Sie **Dynamics 365 Business Central** aus.
6. PowerApps zeigt eine Verbindungsseite an, die Sie zur Eingabe der Informationen auffordert, die benötigt werden, um sich mit Ihren [!INCLUDE[d365fin](includes/d365fin_md.md)] Daten zu verbinden. Zum Verbinden, müssen Sie eine OData URL, Benutzername, Mandantenname und Kennwort angeben.

   Für *OData-URL* können Sie das OData V4 URL eines der Web Services, der in **Webdienste** auf der Seite angezeigt wird in [!INCLUDE[d365fin](includes/d365fin_md.md)] kopieren, beispielsweise `https://mycompany.businesscentral.dynamics.com:7048/MS/ODataV4/`.  

   Für den *Unternehmensname* verwenden Sie den Namen, der im Feld **Name** auf der Seite **Firmendaten** in [!INCLUDE[d365fin](includes/d365fin_md.md)] angezeigt wird. Wenn Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] mehrere Unternehmen enthält, wählen Sie den entsprechenden Namen aus der Liste auf der Seite **Unternehmen** aus. In beiden Fällen prüfen Sie, ob dem Namen, den Sie im PowerApps Assistenten angeben haben genau dem Text entspricht, der angezeigt wird in [!INCLUDE[d365fin](includes/d365fin_md.md)], wie z. B. `My Company`

   Für den Benutzernamen und das Kennwort verwenden Sie die Felder Name und Webdiensttastenkombination, die für Ihr Konto auf der Seite **Benutzer** in [!INCLUDE[d365fin](includes/d365fin_md.md)] angegeben werden. Beispielsweise ist der Benutzername *ADMINISTRATOR* und die Webdiensttastenkombination, die als Passwort dient *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
7. Klicken Sie auf die Schaltfläche **Verbinden** zum Fortfahren. PowerApps zeigt ein Standarddataset an für [!INCLUDE[d365fin](includes/d365fin_md.md)]. Wählen Sie den Datensatz **Standard** aus.

   PowerApps wird eine Liste der Tabellen anzeigen, die in [!INCLUDE[d365fin](includes/d365fin_md.md)]verfügbar sind. Diese Tabellen oder Endpunkte stehen für alle Webdienste, die Sie von [!INCLUDE[d365fin](includes/d365fin_md.md)] veröffentlicht haben.

   Sie können einen neuen Webdienst URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen, indem Sie die **Erstellen Dataset** Aktion der Seite **Webdienste** nutzen, indem Sie die unterstütze Hilfe **Bericht einrichten** verwenden oder die Aktion **Bearbeiten in Excel** in einer beliebigen Liste wählen.
8. Wählen Sie diese Tabelle, die Sie für Ihr PowerApp verwenden möchten, und wählen Sie dann die Schaltfläche **Verbinden** aus.
9. Wiederholen Sie die vorherigen Schritte, um zusätzliche [!INCLUDE[d365fin](includes/d365fin_md.md)] Daten Ihrem Power BI Datenmodell hinzuzufügen.

   > [!NOTE]  
   >    Sobald Sie sich erfolgreich verbunden haben mit [!INCLUDE[d365fin](includes/d365fin_md.md)] werden Sie nicht erneut nach OData URL, Benutzername oder Kennwort gefragt.

Zu diesem Zeitpunkt haben Sie erfolgreich Ihre Business Central Daten verbunden und sind bereit, Ihre PowerApp zu bauen. Weitere Informationen finden Sie in der [PowerApps Dokumentation](https://powerapps.microsoft.com/tutorials/getting-started/).

## <a name="see-also"></a>Siehe auch
[Erste Schritte](product-get-started.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  

