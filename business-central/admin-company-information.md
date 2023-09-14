---
title: Übersicht über Unternehmensdaten
description: 'Auf der Seite „Unternehmensdaten“ werden grundlegende Informationen für eine Geschäftseinheit angegeben, z. B. Name, Adressen und Versandinformationen.'
author: brentholtorf
ms.topic: conceptual
ms.search.form: 1
ms.date: 08/31/2022
ms.author: bholtorf
---

# Übersicht über Unternehmensdaten

[!INCLUDE[prod_short](includes/prod_short.md)] organisiert Geschäftseinheiten in *Unternehmen*. Für jede Firma müssen Sie einige grundlegende Unternehmensdaten und relevante Informationen auf der Seite **Unternehmensdaten** ausfüllen. Die Informationen auf der Seite [**Unternehmensdaten**](https://businesscentral.dynamics.com/?page=1) werden in Dokumenten verwendet, z.B. in den Kopfzeilen von Rechnungen. Sie können mehrere Unternehmen einrichten, z. B. eine Muttergesellschaft und eine Tochtergesellschaft.  

Wenn sich das Lagerort-Lager der Firma an einer anderen Adresse befindet als der Firmensitz, können Sie die verschiedenen Lieferanschrift-Felder und das Feld **Standort-Code** auf der Seite **Versand** Inforegister ausfüllen. Die Informationen in diesen Feldern werden dann z.B. auf Bestellungen gedruckt, damit die Lieferanten die Artikel an den richtigen Ort liefern.  

Für jede Firma, die Sie festlegen, müssen Sie die Seite **Unternehmensdaten** ausfüllen, zusammen mit der Seite **Hauptbuchhaltung Einrichtung**. Sie müssen auch jeden Bereich in [!INCLUDE [prod_short](includes/prod_short.md)] einrichten, z. B. die Seite **Debitoren Verkauf Einr.** für jedes Unternehmen. Erfahren Sie mehr unter [Übersicht der Aufgaben zum Festlegen von [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

Die Seite **Unternehmensdaten** enthält je nach Land/Region unterschiedliche Felder und Inforegister. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Die folgende Tabelle beschreibt die allgemeinsten Inforegister.

[!INCLUDE [admin-company-info-fasttabs](includes/admin-company-info-fasttabs.md)]

Sobald Sie die Informationen ausgefüllt haben, können Sie die Seite schließen.  

## Arbeiten mit mehreren Firmen

Wenn Ihr [!INCLUDE [prod_short](includes/prod_short.md)] mehrere Firmen umfasst, möchten Ihre Benutzer vielleicht *Firmen-Badges* verwenden, damit sie schnell erkennen und im Auge behalten können, in welcher Firma sie gerade arbeiten. Weitere Informationen finden Sie unter [Anzeigen eines Firmen-Badges](#badge).

Es gibt einige Funktionen, mit denen Sie während der Arbeit zwischen den Firmen wechseln können, z.B. den Firmenwechsler (<kbd>Strg</kbd>+<kbd>+O</kbd>). Erfahren Sie mehr unter [Zu einer anderen Firma oder Umgebung wechseln](ui-organization-switch.md).

## <a name="badge"></a>Ein Abzeichen für eine Firma anzeigen

Wenn es mehr als eine Firma oder eine Umgebung gibt, sehen Sie den Firmenwechsler oben rechts in der App-Leiste, in der Nähe des Symbols für die Suche in der App-Leiste. Standardmäßig verwendet der Firmenwechsler ein standardmäßiges Symbol der Firma, wie ![Firmensymbol Launcher.](media/ui-experience/company-icon.png "Zeigt das Symbol für den Wechsel der Firma an, das verwendet wird, wenn es nur eine Umgebung gibt") und ![Firmen-Symbol-mult-env](media/ui-experience/company-icon-multi-env.png "Zeigt das Symbol für den Wechsler der Firma an, wenn es mehrere Umgebungen gibt").

:::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Zeigt das Symbol für den Firmenwechsler in der Überschrift des Business Central Clients an.":::  

Auf der Seite **Unternehmensdaten** können Sie das standardmäßige Symbol für die Firma durch ein angepasstes Symbol für jedes Unternehmen ersetzen, wenn es für die Benutzer einfacher ist, die Firma zu identifizieren, in der sie arbeiten.

1. Füllen Sie im Inforegister **Unternehmenskennkarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
2. Wenn Sie fertig sind, aktualisieren Sie den Browser (wählen Sie <kbd>Strg</kbd>+<kbd>F5</kbd>), um das Abzeichen im Client zu aktualisieren.  

> [!NOTE]
> Der Wechsel der Firma wurde mit der Veröffentlichungswelle 2022, Version 21, eingeführt. In früheren Versionen wird das Firmenabzeichen nicht für den Wechsel der Firma verwendet. Es wird in der oberen rechten Ecke der meisten Seiten angezeigt, auch wenn es nur eine Firma gibt. Wenn Sie es auswählen, werden der vollständige Name der Firma und der Name der Umgebung angezeigt.

## Anzeigename der Firma ändern

Der Firmenname wird immer in der oberen linken Ecke angezeigt und fungiert als Aktion, die Sie auswählen können, um zum Rollencenter zurückzukehren. Diesen Namen können Sie auf der Seite **Firmeninformation** ändern.

1. Wählen Sie das Symbol ![, um das Menü „Einstellungen“ zu öffnen.](media/ui-experience/settings_icon_small.png) Symbol, und wählen Sie dann die Aktion **Unternehmensdaten**.
2. Geben Sie im Feld **Namen** den neuen Namen des Unternehmens ein.
3. Verlassen Sie die Seite. Das System startet neu und zeigt die neue Firma in der oberen linken Ecke an.

## Erfahrung

Die Standardbenutzeroberfläche in einem [!INCLUDE [prod_short](includes/prod_short.md)]-Test zeigt nicht alle Funktionalitäten an. Sie können den vollen Funktionsumfang auf der Seite **Unternehmensdaten** einschalten. Weitere Informationen finden Sie unter [Ändern, welche Funktionen angezeigt werden](ui-experiences.md).  

## Siehe verwandte [Microsoft Schulungen](/training/modules/create-new-companies-dynamics-365-business-central/)

## Siehe auch

[Übersicht über die Aufgaben zum Einrichten von [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Unternehmensdaten-Schnellstart](quick-start-company-information.md)  
[Einrichten der Unternehmensdaten in Italien](LocalFunctionality/Italy/how-to-set-up-company-information.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  
[Neue Unternehmen anlegen](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
