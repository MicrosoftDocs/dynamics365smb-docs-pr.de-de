---
title: Anpassen von Seiten für Rollen
description: 'Erfahren Sie, wie Sie die Benutzeroberfläche für ein Profil (eine Rolle) anpassen, sodass allen Benutzern, die diese Rolle zugewiesen haben, ein benutzerdefinierter Arbeitsbereich angezeigt wird.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: 9171
ms.date: 08/25/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="customize-pages-for-profiles"></a>Seiten für Profile anpassen

Business Central bietet sowohl [Personalisierung](ui-personalization-user.md) für Benutzer als auch Anpassung für Administratoren. Durch die Personalisierung können Benutzer ihren Arbeitsbereich individuell gestalten, indem sie die Seitenlayouts an ihre eigenen Vorlieben anpassen. Administratoren können Seitenlayouts für ein bestimmtes Profil anpassen, entsprechend den Geschäftsrollen oder Abteilungen, sodass allen zugewiesenen Benutzern dieselbe angepasste Seite angezeigt wird. Während die Personalisierung es Benutzern ermöglicht, Felder und Aktionen auf einer Seite anzuzeigen, auszublenden und zu verschieben, bietet die Anpassung zusätzliche Funktionen. Durch die Anpassung können Sie beispielsweise Felder anzeigen, die sich in der Quelltabelle oder in Erweiterungstabellen der Seite befinden, aber nicht im Seitenobjekt definiert sind, was keine mögliche Personalisierung ist.  <!--For more information, see [Personalize Your Workspace](ui-personalization-user.md).-->

<!--Similarly, administrators can customize pages for a profile, according to the related business role or department, so that all users assigned the profile see the customized page layout. As an administrator, you customize pages by using the same functionality as users do when they personalize pages, except with few extra capabilities. Like personalization, you can show, hide, and move fields, actions, or parts on a page. But while personalization only allows you to work with fields that are defined on the page object, customization allows you add fields that are in the source table or table extension, but not defined on the page object. -->

> [!NOTE]
> Die typische geschäftliche Verwendung eines Profils ist eine Rolle. Ein Profil wird daher *Profil (Rolle)* benannt in der Benutzeroberfläche.

Die Seitenanpassung beginnt mit **Profile (Rollen)** Seite, Ausgangspunkt des Administrators für die Verwaltung der Benutzerprofile auf einzelnen Profilkarten. Zusätzlich zum Anpassen des Seitenlayouts steuern Sie verschiedene andere Einstellungen für Profile in der **Profil (Rolle)** Seite für jedes Profil. Weitere Informationen finden Sie unter [Profile verwalten](admin-users-profiles-roles.md).

## <a name="prerequisites"></a>Voraussetzungen

- Ihr Business Central-Konto muss über den Berechtigungssatz **D365-Profil verw.** oder entsprechende Berechtigungen verfügen. 

   Der Berechtigungssatz **D365-Profil verw.** umfasst die Ausführungsberechtigung für das Systemobjekt **9026 Feld zur Tabelle hinzufügen**. Wenn Sie nicht über diese Berechtigung verfügen, dürfen Sie der Seite keine Felder hinzufügen, es sei denn, sie sind im Seitenobjekt definiert. 

## <a name="customize-pages-for-a-profile"></a>Seiten für ein Profil anpassen

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Profile (Rollen)** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie dir Zeile für die Personalisierungsseite, die Sie löschen möchten, und wählen die Aktion **Bearbeiten** aus.
3. Wählen Sie die Aktion **Seiten anpassen**.

    [!INCLUDE[prod_short](includes/prod_short.md)] öffnet eine neue Browser-Registerkarte für das ausgewählte Profil mit dem Banner **Anpassen** Banner aktiviert. Das **Anpassen** Banner bietet die gleiche Funktionalität wie das **Personalisierung** Banner, das den Benutzern zur Verfügung steht.

4. Passen Sie die Seiten an die Anforderungen der jeweiligen Rolle oder Abteilung an, so wie es ein Benutzer bei der Personalisierung tun würde. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

    > [!NOTE]
    > Um während der Personalisierung zu navigieren, verwenden Sie <kbd>Strg</kbd>+<kbd>Klicken</kbd> auf eine Aktion, wenn diese durch die Pfeilspitze hervorgehoben ist.

5. Wenn Sie das Layout einer oder mehrerer Seiten geändert haben, wählen Sie die Schaltfläche **Fertig** im Banner **Anpassen**.
6. Schließen Sie die Browser-Registerkarte.

Die Anpassung von Seiten wird jetzt für das Profil aufgezeichnet.

## <a name="view-all-customized-pages-for-a-profile"></a>Alle angepassten Seiten für ein Profil anzeigen

Sie können sich einen Überblick darüber verschaffen, welche Seiten für ein Profil angepasst wurden, um beispielsweise zu planen, welche Seiten weiter angepasst oder gelöscht werden sollen.

- Auf der Seite **Profil (Rolle)** wählen Sie die Aktion **Angepasste Seiten verwalten**.

Auf der Seite **Benutzerdefinierte Seiten** können Sie Anpassungen löschen und Fehler beheben, indem Sie nach potenziellen Problemen suchen.  

## <a name="delete-all-customizations-for-a-profile"></a>Alle Anpassungen für ein Profil löschen

Sie können alle Anpassunge, die Sie für ein Profil vorgenommen haben, stornieren. Mit einer Erweiterung eingeführte Anpassungen und von einem Benutzer vorgenommene Personalisierungen werden nicht gelöscht. Sie können alle Personalisierungen mit einer anderen Aktion löschen. Weitere Informationen finden Sie unter [Löscht alle von einem Benutzer vorgenommenen Personalisierungen](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).

- Auf der **Profil (Rolle)** Seite wählen Sie auf der Seite für ein benutzerdefiniertes Profil die Option **Löschen Sie benutzerdefinierte Seiten** Aktion.

Das Seitenlayout für das Profil wird auf das Standardlayout zurückgesetzt.  

## <a name="delete-customization-for-specific-pages-for-a-profile"></a>Die Anpassung für bestimmte Seiten eines Profils löschen

Sie können auch alle individuellen Seitenanpassungen löschen, die Sie für ein gemacht haben. Mit einer Erweiterung eingeführte Anpassungen und von einem Benutzer vorgenommene Personalisierungen werden nicht gelöscht. Sie können eine bestimmte Seitenpersonalisierung mit einer anderen Aktion löschen. Weitere Informationen finden Sie unter [So löschen Sie alle Personalisierungen für bestimmte Seiten](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).

1. Auf der Seite **Profil (Rolle)** wählen Sie die Aktion **Angepasste Seiten verwalten**.
2. Auf der Seite **Angepasste Seiten** wählen Sie mindestens eine Zeile für Seitenanpassungen aus, die Sie löschen möchten, und wählen Sie dann die Aktion **Löschen** aus.

Das Layout der ausgewählten Seiten wird an die von Ihnen vorgenommenen Änderungen angepasst.

## <a name="add-a-field"></a>Ein Feld hinzufügen

Sie fügen der Seite Felder über den Bereich **Feld zur Seite hinzufügen** hinzu, den Sie durch Auswahl der Aktion **+ Feld** im Anpassungsmodus öffnen. Es ist wichtig zu verstehen, dass der Bereich **Feld zur Seite hinzufügen** verwendet wird, um Felder anzuzeigen, die bereits vorhanden sind&mdash;entweder auf der Seite und in ihren Quelltabellen,&mdash;aber derzeit nicht sichtbar sind. Sie können keine neuen Felder erstellen.

Der Bereich **Feld zur Seite hinzufügen** zeigt alle Felder an, die auf der Seite angezeigt werden können. Felder sind in die folgenden Kategorien unterteilt, je nach dem zugrunde liegenden Design der Seite selbst, ihrer Quelltabelle und Erweiterungen:

|Kategorie|Description|
|-|-|
|Tabellenfelder, die nicht im Seitenobjekt enthalten sind|Umfasst Felder, die in der Basistabelle oder den Erweiterungstabellen definiert sind, aber nicht auf der Seite definiert sind. Der Tooltip für diese Felder enthält die Beschriftung **Durch die Tabelle definiert**.<br><br>|
|An eine Tabelle gebundene Seitenfelder|Enthält Felder, die in der Basistabelle oder in Tabellenerweiterungen definiert sind und auch auf der Seite als entweder angezeigt oder ausgeblendet definiert sind. Der Tooltip für diese Felder enthält die Beschriftung **Durch die Seite definiert**.|
|Nicht an eine Tabelle gebundene Seitenfelder| Felder, die nur auf der Seite definiert sind, aber nicht in der Basistabelle oder den Erweiterungstabellen. Diese Felder werden normalerweise für Variablen oder Berechnungen verwendet. Der Tooltip für diese Felder enthält die Beschriftung **Durch die Seite definiert**.|

<!--
- Table fields not on the page object. Includes fields that are defined in the base table or extension tables, but aren't defined on the page, either as shown or hidden.   
- Page fields bound to a table. Includes fields that are defined in the base table or table extensions and are also defined on the page as either shown or hidden. 
 - Page fields that are not bound to a table. Fields that are Includes fields that are only defined on the page, not in base table or extension table. These fields typically used for variable or calculation. -->

Verwenden Sie die Filterschaltfläche über der Liste, um zu ändern, welche Kategorie von Feldern im Bereich **Feld zur Seite hinzufügen** angezeigt wird.  

:::image type="content" source="media/customization-filter.svg" alt-text="Zeigt die Filterschaltfläche im Bereich „Ein Feld hinzufügen“ im Anpassungsmodus an.":::
 
### <a name="add-table-field-thats-not-on-the-page-object"></a>Tabellenfeld hinzufügen, das nicht im Seitenobjekt enthalten ist

Wenn Sie den Benutzern ein reines Tabellenfeld auf einer Seite zur Verfügung stellen möchten, müssen Sie es zunächst zur Seite hinzufügen. Sobald Sie das Feld hinzugefügt haben, können Benutzer das Feld mithilfe der Personalisierung nach Belieben anzeigen oder ausblenden. Es gibt mehrere Möglichkeiten, ein Feld hinzuzufügen.

- Eine Möglichkeit besteht darin, es aus dem Bereich **Feld zur Seite hinzufügen** an die gewünschte Position zu ziehen.
- Eine andere Möglichkeit besteht darin, das Feld im Bereich auszuwählen, um die empfohlene Position auf der Seite anzuzeigen. Gehen Sie dann zur Feldposition auf den Seiten, wählen Sie die Pfeilspitze und dann **Hinzufügen** aus. 

Sobald das Feld hinzugefügt wurde, wechselt der Tooltip für das Feld im Bereich **Feld zur Seite hinzufügen** zu **Durch die Seite definiert**. Das hinzugefügte Feld ist für die Bearbeitung gesperrt und kann nicht entsperrt werden.

## <a name="remove-a-field"></a>Ein Feld entfernen

Wenn Sie ein Tabellenfeld hinzugefügt haben, das ursprünglich nicht im Seitenobjekt enthalten war, können Sie es wieder entfernen. Das Entfernen eines Feldes ist etwas anderes als das Ausblenden. Wenn Sie ein Feld ausblenden, können Benutzer es durch Personalisierung weiterhin in ihrem Arbeitsbereich anzeigen. Wenn Sie jedoch ein Feld entfernen, steht es Benutzern nicht mehr zum Ein- oder Ausblenden des Felds zur Verfügung. Wenn das Feld derzeit im Arbeitsbereich eines Benutzers angezeigt wird, verschwindet es aus diesem Arbeitsbereich, wenn Sie es entfernen. 

Um ein Feld zu entfernen, wählen Sie die Pfeilspitze auf dem Feld auf der Seite und dann **Entfernen** aus. Wenn Sie das Feld nicht finden können, wählen Sie es im Bereich **Feld zur Seite hinzufügen** aus, um seine versteckte Position anzugeben. 

> [!IMPORTANT]
> Durch das Entfernen eines Felds werden keine Daten gelöscht, die im Feld oder seinen Quelltabellen gespeichert sind. Es entfernt lediglich das Feld aus der Ansicht. 

## <a name="lock-and-unlock-editing"></a>Bearbeitung sperren und entsperren

Durch die Anpassung können Sie die Bearbeitung der meisten Felder auf einer Seite sperren (Bearbeiten zulassen) oder entsperren (Bearbeiten verhindern). Um die Bearbeitung zu sperren oder zu entsperren, wählen Sie das Feld auf der Seite aus, wählen Sie die Pfeilspitze aus, und wählen Sie dann **Bearbeitung sperren** oder **Bearbeitungssperre aufheben** aus. Es ist wichtig, einige Regeln zum Sperren und Entsperren von Feldern zu beachten:

- Felder, die sich ursprünglich nicht im Seitenobjekt befanden, aber durch Anpassung zur Seite hinzugefügt wurden, sind immer gesperrt und können nicht durch Anpassung oder Personalisierung entsperrt werden.
- Auch die Gestaltung des Feldes kann eine Bearbeitung verhindern. Wenn der AL-Entwickler die [Eigenschaft „Bearbeitbar“](/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) des Felds auf `false` festlegt hat, ist es immer gesperrt und kann nicht entsperrt werden.
- Es ist wichtig zu beachten, dass die Bearbeitungssperrfunktion dazu dienen soll, die Genauigkeit, Konsistenz und Zuverlässigkeit der Daten zu verbessern. Es ist nicht dazu gedacht, die Datenintegrität zu gewährleisten.


<!--However, whatever option you choose for a field, users can always change the setting on their own workspace using personalization. For this reason, it's important to consider locking as a deterrence measure and not a preventative measure.--> 
## <a name="important-information-and-tips"></a>Wichtige Informationen und Tipps

- Möglicherweise sind nicht alle Tabellenfelder für die Anpassung im Bereich **Feld zur Seite hinzufügen** verfügbar. Der Entwickler einer Tabelle kann verhindern, dass ein Feld in der Anpassung angezeigt wird, indem er die [AllowInCustomization-Eigenschaft](/dynamics365/business-central/dev-itpro/developer/properties/devenv-allowincustomizations-property) des Felds auf `false` setzt.
- Sie können eine Seite nicht anpassen, die im [Analysemodus](analysis-mode.md) ist. Der Schalter **Analysieren** ist deaktiviert. Wenn Sie in den Anpassungsmodus wechseln, während sich die Seite im Analysemodus befindet, wird der Analysemodus automatisch ausgeschaltet. 
- Einige Seiten verfügen über mehrere Seitenfelder, die derselben Quelltabelle zugeordnet sind. Im Bereich **Feld zur Seite hinzufügen** werden alle diese Seitenfelder unabhängig voneinander angezeigt. Sie können diese Felder unabhängig voneinander anzeigen, ausblenden oder verschieben, ohne dass sich dies auf die anderen auswirkt.
- Wenn ein Teil oder eine Gruppe ausgeblendet ist, können Sie weiterhin ausgeblendete Felder innerhalb des Teils oder der Gruppe identifizieren, Sie können jedoch keine Felder im Teil oder in der Gruppe hinzufügen, verschieben oder anzeigen, bis sie sichtbar gemacht werden. 
## <a name="see-also"></a>Siehe auch

[Ihren Arbeitsbereich personalisieren](ui-personalization-user.md)  
[Profile verwalten](admin-users-profiles-roles.md)  
[Grundlegende Einstellungen ändern](ui-change-basic-settings.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
