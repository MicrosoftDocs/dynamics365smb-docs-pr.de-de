---
title: Dynamics 365 for Financials als PowerApps-Datenquelle nutzen | Microsoft Docs
description: "Sie können die Finanzdaten als Datenquelle in PowerApps bereitstellen."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 12/02/2016
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: cedc95b23481b8cb76da85e8459a97b1880a4218
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Dynamics 365 for Financials als PowerApps-Datenquelle nutzen
<a id="using-dynamics-365-for-financials-as-a-powerapps-data-source" class="xliff"></a>
Sie können die Daten [!INCLUDE[d365fin](includes/d365fin_md.md)] als Datenquelle in PowerApps bereitstellen.  

**Hinweis**: Sie müssen ein gültiges Konto mit [!INCLUDE[d365fin](includes/d365fin_md.md)] PowerApps haben.  

## Als [!INCLUDE[d365fin](includes/d365fin_md.md)] Datenquelle in PowerApps hinzufügen
<a id="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps" class="xliff"></a>
1. In Ihrem Browser navigieren und zu [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) gehen und sich dann anmelden.
2. Wählen Sie im linken Navigationsbereich **Neue App**.
3. Wählen Sie den Editor, PowerApps-Studio für Windows oder PowerApps-Studio für Internet aus.

   PowerApps-Studio für Windows ist eine Desktop-Anwendung, die verwendet wird, um PowerApps zu erstellen und zu veröffentlichen. PowerApps-Studio für Internet ist eine Online-Lösung, die verwendet wird, um PowerApps zu erstellen und zu veröffentlichen.
4. Der nächste Schritt, um ein PowerApp zu erstellen ist die Auswahl der Daten. Wählen Sie das Pfeilsymbol aus und wählen Sie dann die Option **Neue Verbindung** in der oberen linken Seite der Seite aus.
5. In der Liste der verfügbaren Verbindungscodes, wählen Sie **Dynamics 365 for Financials** aus.
6. PowerApps zeigt eine Verbindungsseite an, die Sie zur Eingabe der Informationen auffordert, die benötigt werden, um sich mit Ihren [!INCLUDE[d365fin](includes/d365fin_md.md)] Daten zu verbinden. Zum Verbinden, müssen Sie eine OData URL, Benutzername, Mandantenname und Kennwort angeben.

   Für *OData-URL* können Sie das OData V4 URL eines der Web Services, der in **Webdienste** auf der Seite angezeigt wird in [!INCLUDE[d365fin](includes/d365fin_md.md)] kopieren, beispielsweise `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Für den *Unternehmensname* verwenden Sie den Namen, der im Feld **Name** im Fenster **Firmendaten** in [!INCLUDE[d365fin](includes/d365fin_md.md)] angezeigt wird. Wenn Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] mehrere Unternehmen enthält, wählen Sie den entsprechenden Namen aus der Liste im Fenster **Unternehmen** aus. In beiden Fällen prüfen Sie, ob dem Namen, den Sie im Power Apps Assistenten angeben haben genau dem Text entspricht, der angezeigt wird in [!INCLUDE[d365fin](includes/d365fin_md.md)], wie z. B. `My Company`

   Für den Benutzernamen und das Kennwort verwenden Sie die Felder Name und Webdiensttastenkombination, die für Ihr Konto im **Benutzer** in [!INCLUDE[d365fin](includes/d365fin_md.md)] angegeben werden. Beispielsweise ist der Benutzername *ADMINISTRATOR* und die Webdiensttastenkombination, die als Passwort dient *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
7. Klicken Sie auf die Schaltfläche **Verbinden** zum Fortfahren. PowerApps zeigt ein Standarddataset an für [!INCLUDE[d365fin](includes/d365fin_md.md)]. Wählen Sie den Datensatz **Standard** aus.

   PowerApps wird eine Liste der Tabellen anzeigen, die in [!INCLUDE[d365fin](includes/d365fin_md.md)]verfügbar sind. Diese Tabellen oder Endpunkte stehen für alle Webdienste, die Sie von [!INCLUDE[d365fin](includes/d365fin_md.md)] veröffentlicht haben.

   Sie können einen neuen Webdienst URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen, indem Sie die **Erstellen Dataset** Aktion der Seite **Webdienste** nutzen, indem Sie die unterstütze Hilfe **Bericht einrichten** verwenden oder die Aktion **Bearbeiten in Excel** in einer beliebigen Liste wählen.
8. Wählen Sie diese Tabelle, die Sie für Ihr PowerApp verwenden möchten, und wählen Sie dann die Schaltfläche **Verbinden** aus.
9. Wiederholen Sie die vorherigen Schritte, um zusätzliche [!INCLUDE[d365fin](includes/d365fin_md.md)] Daten Ihrem Power BI Datenmodell hinzuzufügen.

   **Hinweis**: Sobald Sie sich erfolgreich verbunden haben mit [!INCLUDE[d365fin](includes/d365fin_md.md)], werden Sie nicht erneut nach OData URL, Benutzername oder Kennwort gefragt.

Zu diesem Zeitpunkt haben Sie erfolgreich Ihre Dynamics 365 Daten verbunden und sind bereit, Ihre PowerApp zu bauen. Weitere Informationen finden Sie in der [PowerApps Dokumentation](https://powerapps.microsoft.com/tutorials/getting-started/).

## Siehe auch
<a id="see-also" class="xliff"></a>
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](upload-data.md)  
[Einrichten von [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  

