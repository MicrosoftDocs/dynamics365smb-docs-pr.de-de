---
title: Erkunden und Navigieren von Seiten pro Rolle
description: 'Mit dem Rollen-Explorer können Sie sich einen Überblick über alle Funktionen verschaffen, die für Ihre Rolle und für andere Rollen verfügbar sind.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'role explorer, find features, navigate'
ms.search.form: 'RoleExplorer, 9020, 9022, 9027, 9024'
ms.date: 08/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# <a name="finding-pages-with-the-role-explorer"></a>Suchen von Seiten mit dem Rollen-Explorer

Sie können sich einen Überblick über alle Geschäftsfunktionen verschaffen, die für Ihre Rolle und für andere Rollen verfügbar sind, wenn Sie einen Schritt weiter gehen. In der folgenden Dokumentation wird diese Funktionsübersicht als *Rollen-Explorer* bezeichnet.

Jedes Element im Rollen-Explorer ist eine Aktion, die eine Seite öffnet. Dementsprechend können Sie den Rollen-Explorer auch als Navigationsmittel in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="open-the-role-explorer"></a>Öffnen Sie den Rollen-Explorer

Sie können den Rollen-Explorer aus dem Rollencenter und allen Listenseiten sowie aus dem Fenster **Tell Me** öffnen.

- Wählen Sie in Ihrem Rollencenter oder auf einer beliebigen Listenseite die ![Menü-Schaltfläche.](media/ui_menu_button.png "Menütaste") Schaltfläche rechts neben der Navigationsleiste oder wählen Sie <kbd>Umschalt</kbd>+<kbd>F12</kbd> aus.
- In dem **Wie möchten Sie weiter verfahren** Fenster wählen Sie die **erforschen** Aktion am unteren Rand.

Wenn Sie das Rollenzentrum zum ersten Mal öffnen, zeigt es Links zu den meisten Funktionen an, die für Ihre Rolle verfügbar sind.

## <a name="navigate-features"></a>Funktionen navigieren

Die Aktionen, die Seiten öffnen, sind unter Knoten organisiert, die nach den Features oder Anwendungsbereichen benannt sind. Jeder Knoten kann einzeln komprimiert oder expandiert werden, und Sie können alle Knoten zusammen komprimieren/expandieren.

- Um einen einzelnen Knoten zu erweitern/einzuklappen, wählen Sie den Knoten. Dies gilt für Top-Level-Knoten und Unterknoten.
- Um alle Knoten der obersten Ebene auf der Seite zu erweitern/zu komprimieren, die Unterknoten jedoch unverändert zu lassen, wählen Sie oben **...** und dann **Erweitern** oder **Kolprimieren**.
- Um alle Knoten der obersten Ebene und alle darunter liegenden Unterknoten zu erweitern/zu komprimieren, wählen Sie oben **...** und dann die Aktion **Alle erweitern** oder **Alle komprimieren**.

## <a name="search-for-features"></a>Nach Funktionen suchen

Um Funktionen schnell zu finden, wählen Sie **Finden** und geben dann ein Wort oder einen Satz für die gesuchte Funktion ein. Das Rollenzentrum hebt jeden passenden Text hervor. Wenn eine Funktion in einem zugeklappten Knoten verborgen ist, wird der zugeklappte Knoten mit einem Punkt markiert. 

## <a name="explore-other-roles"></a>Andere Rollen erforschen

Um andere Rollen als Ihre eigene zu erkunden, wählen Sie **Weitere Rollen erkunden**. Das Rollenzentrum zeigt jede Rolle unter ihrer eigenen Überschrift an, mit Links zu ihren Funktionen. Sie können dann genauso navigieren und Funktionen finden, wie Sie es bei der Erkundung Ihrer Rolle tun.

> [!NOTE]
> Sie sehen nur Rollen, die so festgelegt sind, dass sie im Rollenexplorer angezeigt werden. Wenn Sie also eine Rolle, die Sie erwartet haben, nicht sehen, ist sie wahrscheinlich nicht dafür festgelegt. Weitere Informationen finden Sie unter [Profile verwalten](admin-users-profiles-roles.md). 

Wenn Sie andere Rollen erkunden, können Sie die Suche auch mit den Aktionen **Bericht & Analyse** und **Verwaltung** oben im Rollencenter eingrenzen.

- **Bericht & Analyse** zeigt nur die Funktionen an, die als Berichte und Analysefunktionen kategorisiert sind.
- **Verwaltung** zeigt nur die Funktionen an, die als Verwaltungsfunktionen kategorisiert sind.

> [!TIP]
> Für Entwickler kategorisieren Sie Seiten und Berichte, indem Sie die Eigenschaft [UsageCategory](/dynamics365/business-central/dev-itpro/developer/properties/devenv-usagecategory-property) im AL-Code des Objekts festlegen.
<!--
 
## <a name="role-explorer-actions"></a>Role explorer actions

There a several actions along the top of the role explorer to help you locate features of your role and other roles.

|Action|Description|
|------|------|
|**All**|Shows all features that are related to the role.|
|**Find**|Lets you enter a word or phrase to quickly locate feature names that match.|
|**Explore more roles**|All business features that are available for all roles including your own. When exploring all roles, the other actions work the same way, except for all roles shown. **NOTE:** You will only see roles that are set up to show in role explorer. For more information, see [Manage Profiles](admin-users-profiles-roles.md).  |
|**Report & Analysis**|This action Shows only those features that are categorized as reports and analysis features.|
|**Administration**|Shows only those features that are categorized as administration features.|



<!--
Choose the **Find** action at the top of the role explorer to quickly locate feature names that contain a certain term.

Choose the **Explore more roles** action at the top of the role explorer to get an overview of all business features that are available for all roles including your own.

> [!NOTE]
> Only Role Center actions for profiles where the **Show in Role Explorer** check box is selected will appear on the extended version of the role explorer (shown with the **Explore more roles** action). For more information, see [Manage Profiles](admin-users-profiles-roles.md).
-->

## <a name="expand-and-collapse-nodes-on-the-role-explorer"></a>Knoten im Rollen-Explorer erweitern und komprimieren

Die Aktionen, die Seiten öffnen, sind unter Knoten organisiert, die nach den Features oder Anwendungsbereichen benannt sind. Jeder Knoten kann einzeln komprimiert oder expandiert werden, und Sie können alle Knoten zusammen komprimieren/expandieren.

- Um einen Knoten zu expandieren/komprimieren, wählen Sie den Knoten aus. Dies gilt für Top-Level-Knoten und Unterknoten.
- Um alle Knoten der obersten Ebene auf der Seite auf- und zuklappen, wählen Sie die Aktion **Erweitern** oder **Komprimieren** in der rechten oberen Ecke.
- Führen Sie einen der folgenden Schritte aus, um alle Knoten der obersten Ebene und alle darunter liegenden Unterknoten zu erweitern/zu reduzieren:
  - Wählen Sie <kbd>Strg</kbd>+<kbd>Umschalt</kbd> aus, während Sie die Aktion **Erweitern** oder **Reduzieren** in der oberen rechten Ecke auswählen.
  - Wählen Sie **...** in der oberen rechten Ecke und wählen Sie dann die Aktion **Alle erweitern** oder **Alle reduzieren**.

## <a name="see-also"></a>Siehe auch
[Suche nach Seiten und Informationen mit „Sie wünschen...“](ui-search.md)  
[Profile verwalten](admin-users-profiles-roles.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
