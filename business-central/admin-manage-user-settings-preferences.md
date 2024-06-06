---
title: Verwalten Sie Benutzereinstellungen und Präferenzen als Administrator
description: Verwalten Sie Benutzereinstellungen und Präferenzen in Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.topic: get-started
ms.devlang: al
ms.reviewer: bholtorf
ms.search.keywords: 'user settings, preferences, language, region, time zone, regional settings'
ms.search.form: '9204,'
ms.date: 04/01/2021
ms.author: soalex
ms.service: dynamics-365-business-central
---
# <a name="manage-user-settings-and-preferences"></a>Benutzereinstellungen und Präferenzen verwalten

Als Administrator können Sie Benutzereinstellungen in [!INCLUDE[prod_short](includes/prod_short.md)] konfigurieren, ähnlich wie einzelne Benutzer ihre eigenen Einstellungen auf der Seite **Meine Einstellungen** verwalten können.  

Verschaffen Sie sich einen Überblick über alle Benutzer in der Liste **Benutzer**, und ändern Sie einzelne Einstellungen durch Auswahl der Aktion **Benutzereinstellungen** für den jeweiligen Benutzer.

> [!TIP]
> Die Liste **Benutzereinstellungen** zeigt die aktuellen Einstellungen für jeden Benutzer. Um einzelne Benutzer anzuzeigen oder zu bearbeiten, wählen Sie die Aktionen **Ansicht** oder **Bearbeiten**.

Die Seite **Karte für Benutzereinstellungen** ist ähnlich wie die Seite **Meine Einstellungen** auf die jeder Benutzer Zugriff hat, und es ist ein leistungsstarkes Tool für Sie als Administrator, mit dem Sie beispielsweise Standardeinstellungen festlegen und personalisierte Seiten löschen können.  

## <a name="types-of-user-settings"></a>Typen von Benutzereinstellungen

Die Option *Benutzereinstellungen*, bei der es um den Benutzer als Entität und den Zugriff des Benutzers im System geht, ist nicht mit der Option *Benutzereinrichtung* identisch. Darüber hinaus haben Benutzereinstellungen nichts mit der Personalisierung eines Benutzers zu tun, wie z. B. geringfügige Änderungen an der Benutzeroberfläche. Benutzereinstellungen bestimmen vordefinierten Einstellungen für jeden Benutzer in verschiedenen Aspekten der Art und Weise, wie sich die Anwendung dem Benutzer präsentiert. Im folgenden Absatz werden die fünf Typen von Benutzereinstellungen und Präferenzen aufgeführt, die von der Person oder zentral vom Administrator festgelegt werden können:

* **Unternehmen**  

  Diese Einstellung bestimmt das Unternehmen, bei dem sich bei der nächsten Anmeldung angemeldet werden soll. Ein Benutzer kann Zugriff auf mehrere Unternehmen haben und in mehreren Unternehmen aktiv sein.

* **Rolle**  

  Die Rolle oder das Profil beschreibt die Funktion des Benutzers im Unternehmen, z. B. *Verkaufsleiter*, *Buchhalter* oder *Einkäufer*. Das Profil bestimmt dann das Rollencenter des Benutzers, die Startseite, die Benutzern bei der Anmeldung angezeigt wird. Das Profil hat keine Auswirkungen auf die Zugriffsrechte auf Funktionen in [!INCLUDE[prod_short](includes/prod_short.md)].  

* **Sprache**  

  Definiert die Anwendungssprache, in der [!INCLUDE[prod_short](includes/prod_short.md)] Text, Beschriftungen und Fehlermeldungen darstellt. Beim Synchronisieren von [!INCLUDE[prod_short](includes/prod_short.md)]-Benutzern über Microsoft 365 werden die Spracheinstellungen von Microsoft 365 verwendet, wobei davon ausgegangen wird, dass der Benutzer dieselben Einstellungen in Office-Produkten und [!INCLUDE[prod_short](includes/prod_short.md)] verwenden möchte. Der Administrator kann die Standardeinstellung ändern und jeder Benutzer kann auf der Seite „Meine Einstellungen“ zwischen verfügbaren Sprachen wählen. Sie werden jedoch bei der nächsten Synchronisierung auf den Wert von Microsoft 365 zurückgesetzt.

  Wenn die Spracheinstellung von Microsoft 365 einer unterstützten Sprache in [!INCLUDE[prod_short](includes/prod_short.md)] entspricht, wird diese Sprache für den Benutzer ausgewählt.  

  > [!NOTE]
  > Möglicherweise müssen Sie eine Sprach-App für [!INCLUDE[prod_short](includes/prod_short.md)] installieren, um die Sprache ordnungsgemäß anzuzeigen. Daher empfiehlt es sich, die erforderlichen Sprach-Apps zu installieren, bevor sich ein Benutzer zum ersten Mal anmeldet, sodass ihm vom ersten Tag an eine benutzerfreundliche Umgebung zur Verfügung steht. Weitere Informationen finden Sie in der Liste der [unterstützte Sprachen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
* **Region**  

  Definiert, wie Daten und Zahlen im [!INCLUDE[prod_short](includes/prod_short.md)]-Client angezeigt werden, z. B., ob europäische oder amerikanische Datumsformate verwendet werden sollen oder wie das Dezimalzeichen und Tausendertrennzeichen in Beträgen angezeigt werden sollen. Beim Synchronisieren von [!INCLUDE[prod_short](includes/prod_short.md)]-Benutzern über Microsoft 365 werden die regionalen Einstellungen von Microsoft 365 verwendet, wobei davon ausgegangen wird, dass der Benutzer dieselben Einstellungen in Office-Produkten und [!INCLUDE[prod_short](includes/prod_short.md)] verwenden möchte. Ein Administrator oder Benutzer kann diese Einstellungen manuell in [!INCLUDE[prod_short](includes/prod_short.md)] ändern, diese werden jedoch von Microsoft 365 zurückgesetzt, sobald die nächste Synchronisation durchgeführt wurde.

* **Zeitzone**  

  Definiert die Zeitzone, in der sich der Benutzer befindet. Derzeit wird diese nicht von Microsoft 365 synchronisiert und muss manuell eingestellt werden.  

* **Unterrichtstipps**

  [!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)] Als Administrator können Sie Unterrichtstipps für alle Benutzer deaktivieren, z. B. wenn Sie gerade Benutzer einbinden, mit denen Sie bereits vertraut sind [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> Wenn eine Microsoft 365-Benutzersynchronisierung durchgeführt wird, während Benutzer bei [!INCLUDE[prod_short](includes/prod_short.md)] angemeldet sind, müssen diese Benutzer den Browser aktualisieren oder sich bei [!INCLUDE[prod_short](includes/prod_short.md)] ab- und wieder anmelden, um eine potenziell andere Sprache anzuzeigen, die durch die Synchronisierungsaktion festgelegt wurde.

## <a name="overview-of-all-user-specific-changes"></a>Übersicht aller benutzerspezifischen Änderungen

Als Administrator erhalten Sie einen Überblick über einzelne Änderungen von [!INCLUDE [prod_short](includes/prod_short.md)], was jeder Benutzer möglicherweise zu verschiedenen Seiten in [!INCLUDE [prod_short](includes/prod_short.md)] gemacht hat. Wenn Benutzer Änderungen an ihrer Erfahrung in [!INCLUDE [prod_short](includes/prod_short.md)] gemacht haben, werden diese Änderungen in der Liste **Benutzerpersonalisierungen** wiedergegeben. <!--Administrators can also set these settings for users before they log in the first time, so users do not have to do it themselves, providing them a better *getting started* experience.-->

<!-- >[!NOTE]
> User personalizations do not have anything to do with the *personal* lightweight changes a user can make to the user experience.-->

## <a name="to-review-or-delete-user-personalizations"></a>Zum Überprüfen oder Löschen von Benutzerpersonalisierungen

1. Wählen Sie das ![Suchen Sie nach Seite oder Bericht.](media/ui-search/search_small.png "Nach dem Symbol für „Seite“ oder „Bericht“ suchen") Symbol. Geben Sie **Personalisierte Seiten** ein und wählen Sie dann den entsprechenden Link.
2. Dadurch werden die Liste der Benutzer und ihrer personalisierten Seiten angezeigt. Um die Personalisierung eines Benutzers zu löschen, klicken Sie auf die entsprechende Zeile oder wählen Sie **Verwalten** und dann **Löschen** aus.

Dadurch wird die Personalisierung gelöscht und die Benutzererfahrung mit der relevanten Seite kehrt zum Standardstatus zurück.

## <a name="see-also"></a>Siehe auch

[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  
[Verfügbarkeit nach Ländern/Regionen und unterstützte Sprachen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Sprache und Gebiet ändern](about-locale-language.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
