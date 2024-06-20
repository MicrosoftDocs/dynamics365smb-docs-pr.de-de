---
title: KPI-Webdienste auf der Grundlage von Finanzberichten festlegen und veröffentlichen
description: 'In diesem Artikel wird beschrieben, wie Sie die KPI-Daten von Finanzberichten auf der Grundlage von bestimmten Finanzberichten anzeigen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# KPI-Webdienste auf der Grundlage von Finanzberichten festlegen und veröffentlichen

Auf der Seite **KPI-Webdienste für Finanzberichte einrichten** legen Sie fest, wie die KPI-Daten (Key Performance Indicator) des Finanzberichts angezeigt werden sollen und auf welchen spezifischen Finanzberichten die KPIs basieren sollen. Wenn Sie **Webdienst veröffentlichen** wählen, werden die angegebenen Finanzbericht-KPI-Daten der Liste der veröffentlichten Webdienste auf der Seite **Webdienste** hinzugefügt.

> [!NOTE]
> Wenn Sie diesen Webdienst verwenden, werden Abschlussdaten nicht in Ihren Datensatz aufgenommen. Sie können die Filter in Power BI verwenden, um verschiedene Zeiträume zu analysieren.

## Einen KPI-Webservice auf der Basis von Finanzberichten festlegen und veröffentlichen
  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Finanzbericht KPI Web Service Einrichtung** ein, und wählen Sie dann den entsprechenden Link.
2. Füllen Sie auf der Registerkarte **Allgemein** die Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Füllen Sie die Felder im Inforegister **Zeilendefinitionen** aus.
4. Wiederholen Sie Schritt 3 für alle Finanzberichte, auf die Sie den KPI-Webservice für Finanzberichte stützen möchten.  
5. Um den ausgewählten Finanzbericht anzuzeigen oder zu bearbeiten, wählen Sie auf der Registerkarte **Zeilendefinitionen** des Inforegisters die Aktion **Zeilendefinition bearbeiten**.
6. Um die KPI-Daten des Finanzberichts anzuzeigen, die Sie festgelegt haben, wählen Sie die Aktion **Finanzbericht KPI Web Service**.
7. Um den KPI-Webdienst für den Finanzbericht zu veröffentlichen, wählen Sie die Aktion **Webdienst veröffentlichen**.

Sie können jetzt Finanzberichte in Power BI basierend auf dem oder den von Ihnen erstellten Webdiensten erstellen.

> [!NOTE]  
> Sie können den KPI-Webdienst auch veröffentlichen, indem Sie von der Seite **Webdienste** auf das Objekt **Finanzbericht KPI Webdienst Einrichtung** verweisen. Erfahren Sie mehr unter [Veröffentlichen eines Webdienstes](across-how-publish-web-service.md).

## Siehe auch

[Financial Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Das Hauptbuch und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
