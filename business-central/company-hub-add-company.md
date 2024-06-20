---
title: Fügen Sie Unternehmen zu Ihrem Unternehmens-Hub hinzu
description: 'Erfahren Sie, wie Sie Unternehmen aus anderen Business Central-Umgebungen zu Ihrem Unternehmens-Hub hinzufügen, damit Sie die Arbeit in verschiedenen Umgebungen verwalten können.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, company hub'
ms.search.form: '1151, 1155, 1166, 1165'
ms.date: 09/28/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Fügen Sie Unternehmen zu Ihrem Unternehmens-Hub hinzu

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Mit dem Unternehmens-Hub können Sie von mehreren Unternehmen aus von mehreren [!INCLUDE [prod_short](includes/prod_short.md)]-Umgebungen aus auf Ihre Arbeit zugreifen. Sie können Umgebungen und Unternehmen manuell hinzufügen, wenn Ihre Unternehmen nicht automatisch im Unternehmens-Hub angezeigt werden.  

Direkt auf der Landing Page des Unternehmens-Hubs finden Sie das Menü **Setup**, von wo aus Sie auf die Seite **Umgebungslinks** zugreifen können. Wählen Sie einfach **Neu** aus, und füllen Sie dann die relevanten Felder aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

> [!NOTE]
> Sie können den Unternehmens-Hub mit so vielen Unternehmen verbinden, wie Sie benötigen. Sie können den Unternehmens-Hub jedoch nur mit Unternehmen verbinden, die in [!INCLUDE [prod_short](includes/prod_short.md)] online gehostet werden.

## Umgebungs-Links

Ein Umgebungslink ist eine Karte, auf der Sie die die [!INCLUDE [prod_short](includes/prod_short.md)]-Umgebung angeben, die mindestens ein Unternehmen, in dem Sie arbeiten, hostet. Die Daten in der Karte für jede Umgebung werden von Ihnen angegeben, und Sie können diese bei Bedarf ändern. Jedoch ist das Feld **Umgebungslink** wesentlich – damit können Sie auf jedes Unternehmen in [!INCLUDE [prod_short](includes/prod_short.md)] zugreifen. Verwenden Sie die Aktion **Die Verbindung testen** im Menüband, um zu prüfen, ob Sie den richtigen Link eingegeben haben. Der Link, den Sie eingeben müssen, zeigt auf eine Umgebung, die das Unternehmen hostet, das Sie hinzufügen, und er muss die Microsoft Entra-ID oder den Domänenname der Organisation enthalten. Wenn Sie beispielsweise eine bestimmte Domäne wie MyBusiness.com angegeben haben, dann ist der Link zu dessen [!INCLUDE [prod_short](includes/prod_short.md)] nämlich ```https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1```. Andernfalls sieht er ungefähr so aus: ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```  

Der Link wird verwendet, wenn Sie das Unternehmen im Unternehmens-Hub auswählen.  

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Aktionen für eine Firma, die im Hub der Firma aufgeführt ist":::

> [!TIP]
> Wenn Sie in der kostenlosen Testversion von [!INCLUDE [prod_short](includes/prod_short.md)] arbeiten, ist es einfach, die Unternehmen in Ihrem Mandanten hinzuzufügen. Sie finden den Umgebungslink, indem Sie die Microsoft Entra-ID aus dem Abschnitt **Problembehandlung** der Seite „Hilfe und Support“ kopieren. Der Umgebungsname ist wahrscheinlich der Standardwert PRODUKTION. Fügen Sie diese Informationen dem Feld **Umgebungslink** hinzu, wie z. B. ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```, und wählen Sie dann **Die Verbindung testen**. Das Bewertungsunternehmen wird der Liste hinzugefügt.
>
> Wenn Sie zum 30-Tage-Testunternehmen „My Company“ gewechselt sind, können Sie dieses zur Liste hinzufügen, indem Sie die Aktion **Neu laden / Alle Unternehmen neu laden** in der Liste auswählen.

## Unternehmen laden

Wenn Sie Ihre Umgebungen hinzugefügt haben, werden Ihre Unternehmen automatisch angezeigt. Wenn Sie jedoch wissen, dass einer Umgebung ein neues Unternehmen hinzugefügt wurde, können Sie die Aktion **Alle Unternehmen neu laden** auswählen zum Aktualisieren der Liste. Verwenden Sie dieselbe Aktion, um Daten aus allen Ihren Unternehmen zu aktualisieren.  

> [!TIP]
> Um die Daten im Unternehmens-Hub zu aktualisieren, müssen Sie Zugriff auf die Daten in den Unternehmen haben, von denen die Daten stammen.

## Siehe auch

[Arbeit über mehrere Unternehmen hinweg im Unternehmens-Hub verwalten](company-hub.md)  
[Ressourcen für Hilfe und Support](product-help-and-support.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
