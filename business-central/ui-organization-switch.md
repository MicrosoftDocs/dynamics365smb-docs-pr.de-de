---
title: Wechseln zu einem anderen Unternehmen oder einer anderen Umgebung
description: 'Wenn Sie für mehrere Organisationen arbeiten, können Sie schnell zwischen den Umgebungen und Unternehmen wechseln.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'environments, companies, tenants, organization'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 08/16/2022
ms.author: bholtorf
---

# Wechseln zu einem anderen Unternehmen oder einer anderen Umgebung

[!INCLUDE [prod_short](includes/prod_short.md)] ist in vielen verschiedenen Ländern/Regionen verfügbar und unterstützt viele verschiedene Arten von Organisationen. Ihre Organisation kann sich dafür entscheiden, die Arbeit in [!INCLUDE [prod_short](includes/prod_short.md)] in mehrere *Firmen* und *Umgebungen* zu organisieren. Dieser Artikel hilft Ihnen, die Hauptunterschiede zu verstehen und zu verstehen, wie Sie mit ihnen umgehen können.

## Unternehmen und Umgebungen

[!INCLUDE [company_environment](includes/company_environment.md)]

> [!TIP]
> Wenn Sie häufig zwischen Unternehmen wechseln oder mit [!INCLUDE[prod_short](includes/prod_short.md)] über eine andere App wie Microsoft Teams arbeiten, kann es leicht sein, den Überblick zu verlieren, wo Sie sich befinden. Um den Überblick zu behalten, können Sie eine Markierung hinzufügen, die den Unternehmensnamen anzeigt, sodass Sie schnell überprüfen können, ob Sie sich am richtigen Ort befinden. Weitere Informationen finden Sie unter [Unternehmenskennkarte anzeigen](admin-company-information.md#badge).
> 
> Abhängig von Ihrem Browser können Sie die verschiedenen Unternehmen auch an Ihre Favoritenleiste anheften.  

<!--
[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]-->

## Funktionen zum Wechseln zu einem anderen Unternehmen oder einer anderen Umgebung

Es gibt einige Funktionen, mit denen Sie während der Arbeit das Unternehmen oder die Umgebung wechseln können. In der folgenden Tabelle werden die Funktionen der Funktion verglichen, die in den folgenden Abschnitten ausführlicher erläutert werden.

|Funktion|Unternehmen wechseln|Umgebung wechseln|Wechseln Sie in einen neuen Browser-Tab| Lokal verfügbar|
|-------|--------------|------------------|-------------------------|----------------------|
|[Firmenumschalter](#use-the-company-switcher)|![Häkchen](media/check.png "Aktivieren")|![Häkchen](media/check.png "Aktivieren")|![Häkchen](media/check.png "Aktivieren")|![Häkchen](media/check.png "Aktivieren")|
|[App-Startprogramm](#use-the-app-launcher)||![Häkchen](media/check.png "Aktivieren")|![Häkchen](media/check.png "Aktivieren")||
|[Meine Einstellungen](#use-my-settings)|![Häkchen](media/check.png "Aktivieren")|||![Häkchen](media/check.png "Aktivieren")|
|[Unternehmens-Hub](#use-company-hub)|![Häkchen](media/check.png "Aktivieren")|![Häkchen](media/check.png "Aktivieren")|![Häkchen](media/check.png "Aktivieren")||

## Verwenden Sie den Firmenumschalter

Die Verwendung des Firmenumschalter ist wahrscheinlich die schnellste und vielseitigste Art, die Firma zu wechseln. Der Firmenumschalter ist ein Bereich, der von jeder Seite aus leicht zugänglich ist. Der Bereich gibt einen Überblick über alle Unternehmen in allen Umgebungen, auf die Sie Zugriff haben, und ermöglicht Ihnen, direkt zu einem von ihnen zu wechseln&mdash; entweder im selben Browser-Tab oder einem neuen. Dies ist besonders nützlich, wenn Sie in vielen Unternehmen in unterschiedlichen Umgebungen arbeiten.

1. In der oberen rechten Ecke neben dem Suchsymbol sehen Sie entweder das Standard-Unternehmenssymbol, wie ![das Startprogramm für Firmen](media/ui-experience/company-icon.png "Zeigt das Symbol des Firmenumschalters an, das verwendet wird, wenn eine einzelne Umgebung vorhanden ist") und ![company-icon-multi-env](media/ui-experience/company-icon-multi-env.png "Zeigt das Symbol des Firmenumschalters an, das verwendet wird, wenn mehrere Umgebungen vorhanden sind"), oder ein [benutzerdefiniertes Abzeichen](admin-company-information.md#badge) für das Unternehmen, für das Sie derzeit arbeiten. Wählen Sie das Symbol aus, um das Firmenumschaltfenster zu öffnen.

   :::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Zeigt das Symbol für den Firmenwechsler in der Überschrift des Business Central Clients an.":::  

   > [!TIP]
   > Sie können auch die Tastenkombination <kbd>Strg</kbd>+<kbd>O</kbd> verwenden, um den Bereich zu öffnen.
2. Wählen Sie im Bereich **Verfügbare Unternehmen** das Unternehmen aus, zu dem Sie wechseln möchten, und wählen Sie den Pfeil **Umschalten**, und wählen Sie dann eine der folgenden Optionen aus:

   |Option|Description|
   |------|-----------|
   |Wechseln|Öffnet das Rollencenter für das ausgewählte Unternehmen in derselben Browserregisterkarte, in der Sie gerade arbeiten. Das Unternehmen wird das Standardunternehmen, das in Business Central geöffnet wird, bis Sie erneut wechseln oder das Unternehmen ändern, indem Sie **Meine Einstellungen** verwenden. |
   |In neuer Registerkarte öffnen|Öffnet das Rollencenter für das ausgewählte Unternehmen in einem neuen Browser-Tab, wobei das ursprüngliche Unternehmen auf dem anderen Tab geöffnet bleibt.|
   |In neuer Registerkarte öffnen und zu derselben Seite wechseln|Diese Option ist nur auf Listenseiten wie Kunden, Verkaufsaufträgen oder Artikeln aktiv. Es öffnet dieselbe Liste, jedoch für das ausgewählte Unternehmen, in einem neuen Browser-Tab. |

> [!TIP]
> Wählen Sie <kbd>F5</kbd>, um die Liste der Umgebungen und Unternehmen zu aktualisieren.

## App-Startfeld verwenden

Wenn Sie mit [!INCLUDE[prod_short](includes/prod_short.md)] angemeldet sind, stehen Ihnen die Umgebungen, auf die Sie zugreifen können, auf Office.com zur Verfügung.  

1. Wählen Sie das Symbol **App-Startfeld** ![App-Startfeld.](media/app-launcher-icon.png "Das App-Startfeld bietet Zugriff auf weitere Funktionen.").
2. Suchen Sie in dem sich öffnenden Bereich nach und wählen Sie [!INCLUDE[prod_short](includes/prod_short.md)]. Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] nicht sehen, wählen Sie **Alle Apps** und geben Sie **Business Central** in das Feld **Suchen** ein.

   :::image type="content" source="media/app-launcher-bc-tile.png" alt-text="Das Microsoft 365-App-Startprogramm mit der Business Central-Kachel.":::  

3. Wenn es mehr als eine Umgebung gibt, werden Sie aufgefordert, die Umgebung auszuwählen, auf die Sie zugreifen möchten.

<!--
The following image shows tiles for accessing production and sandbox environments on the Dynamics 365 Home page.

:::image type="content" source="media/app-picker-environments.png" alt-text="The Dynamics 365 Home page showing production and sandbox environments.":::
-->
## Meine Einstellungen verwenden

Wenn Sie bei [!INCLUDE[prod_short](includes/prod_short.md)] angemeldet sind, können Sie schnell zu einem anderen Unternehmen in derselben Umgebung wechseln. Nachdem Sie den Wechsel vorgenommen haben, wird das von Ihnen ausgewählte Unternehmen zu Ihrem Standardunternehmen und bei Ihrer nächsten Anmeldung geöffnet.

1. Wählen Sie in der oberen rechten Ecke das Symbol **Einstellungen** ![Einstellungen.](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollenzentrum") und dann die Aktion **Meine Einstellungen**.

    > [!TIP]
    > Sie können auch die Tastenkombination <kbd>Alt</kbd>+<kbd>T</kbd> verwenden, um die Seite „Meine Einstellungen“ schnell zu öffnen.

2. Wählen Sie auf der Seite **Meine Einstellungen** im Feld **Unternehmen** das Unternehmen aus.  
3. Wählen Sie die Schaltfläche **OK** aus.

> [!TIP]
> Eine gute Möglichkeit, beim Anmelden direkt zu Ihrem Standardunternehmen zu gelangen und keine Umgebung angeben zu müssen, besteht darin, die URL nach der Anmeldung Ihrer Favoritenliste hinzuzufügen.

## Unternehmens-Hub verwenden

*Unternehmens-Hub* ist ein hochspezialisiertes Rollencenter, das einen finanziellen Überblick über Unternehmen und Umgebungen gibt. Erhältlich als [Erweiterung](ui-extensions-company-hub.md) stellt Unternehmens-Hub ein Dashboard mit zusammenfassenden Daten für jedes Unternehmen bereit, auf das Sie Zugriff haben. Auf der Homepage werden finanzielle KPIs und ein direkter Link zu den einzelnen Umgebungen und Unternehmen angezeigt, um Benutzern dies zu ermöglichen. Weitere Informationen finden Sie unter [Arbeit über mehrere Unternehmen hinweg im Unternehmens-Hub verwalten](company-hub.md).

[![Zeigt die Unternehmens-Hub-Seite an, die alle Unternehmen auflistet.](media/company-hub.png)](media/company-hub.png#lightbox)  

## Siehe auch

[Neue Unternehmen anlegen in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Umgebungen und Unternehmen (Nur in englischer Sprache)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  
[Firmendaten](admin-company-information.md)  
[Das Business Central Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
