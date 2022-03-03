---
title: Überprüfen von Seiten in Business Central
description: Verwenden Sie die Seitenüberprüfungsfunktion, um Details zum Seitenentwurf und zur Datenquelle anzuzeigen. Der Seiteninspektor eignet sich ideal zum Beheben von Problemen mit Ihren Daten.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
author: jswymer
ms.author: jswymer
ms.date: 04/01/2021
ms.openlocfilehash: d30b93942292e2f6a5a52831725ec06aed32820c
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8136504"
---
# <a name="inspecting-pages-in-business-central"></a>Überprüfen von Seiten in Business Central

Die Überprüfungsfunktion der Seite ermöglicht es Ihnen, Details zu einer Seite abzurufen und bietet Einblick in den Seitenentwurf, die verschiedenen Elemente, aus denen die Seite besteht und die Quelle hinter den angezeigten Daten. Seitenüberprüfung ist besonders für Administratoren und Superuser, Support-Mitarbeiter und Entwickler gedacht. Es eignet sich ideal, um mehr über das Datenmodells hinter einer Seite zu erfahren, und für die Fehlerbehebung. Wenn Sie beispielsweise ein Problem mit einer Seite haben, können Sie mit der Seitenüberprüfung Informationen erhalten, die Sie an den Systemadministrator oder den Supportmitarbeiter weitergeben.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]

## <a name="working-with-page-inspection"></a>Arbeiten mit der Seitenüberprüfung

Starten Sie die Seitenüberprüfung über die Seite **Hilfe und Support**. Wählen Sie ein Fragezeichen in der oberen rechten Ecke aus, wählen Sie **Hilfe und Support** und dann **Seiten und Daten prüfen** aus. Zudem besteht die Möglichkeit, die Tastenkombination **Strg+Alt+F1** zu verwenden.

Der Bereich **Seitenüberprüfung** wird auf der Seite geöffnet. Die folgende Abbildung zeigt den Bereich **Seitenüberprüfung** auf der Seite **Verkaufsauftrag**.

![Seite inspizieren.](media/page-inspection-example.png)

Wenn der Bereich **Seitenüberprüfung** erstmaligen geöffnet wird, werden Informationen zum Hauptseitenobjekt angezeigt.

Verwenden Sie die Tastatur oder ein Zeigegerät, um den Fokus auf verschiedene Elemente der Seite zu verschieben. Wenn Sie eine Infobox oder einen Teil der Hauptseite auswählen, wird der umgebende Bereich von einen Rahmen markiert und der Bereich **Seitenüberprüfung** zeigt Informationen zum ausgewählten Element. Beispielsweise zeigt die vorherige Abbildung Informationen über den Listenanteil auf der Seite **Verkaufsauftrag** an. Wenn Sie zu anderen Seiten in der Anwendung navigieren, wird der Bereich **Seitenüberprüfung** dabei automatisch mit Seiteninformationen aktualisiert.

Weitere Informationen darüber, was in der Seitenüberprüfung angezeigt wird, finden Sie in [Überprüfung und Fehlerbehebung von Seiten](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) in der Hilfe für Business Central-Entwickler und IT-Profis.

Wenn die erwarteten Details im Bereich **Seitenüberprüfung** nicht angezeigt werden, verfügen Sie möglicherweise nicht über die erforderlichen Berechtigungen, wie im nächsten Abschnitt erläutert.

## <a name="controlling-access-to-page-inspection-details"></a>Steuern des Zugriffs auf Seitenüberprüfungsdetails

Als ein Administrator können Sie den Zugriff auf die gesamten Details steuern, die im Bereich **Seitenüberprüfung** angezeigt werden, indem Sie die Berechtigungen konfigurieren, die Benutzer haben. Um einem Benutzer Berechtigung für alle Details zu gewähren, geben Sie Benutzern die Berechtigung **Ausführen** im **System**-Objekt **5330**. Sie können diese Berechtigungen gewähren, indem Sie einen Berechtigungssatz (beispielsweise **D365 Troubleshoot**) oder eine Benutzergruppe (beispielsweise **D365 Troubleshoot**) verwenden. Weitere Informationen zu Berechtigungen finden Sie unter [Zuweisen von Berechtigungen für Benutzer und Gruppen](ui-define-granular-permissions.md).

Benutzer, die keine Berechtigungen in **Systemobjekt 5330** haben, können dennoch auf den Bereich **Seitenüberprüfung** zugreifen, sehen allerdings nur die Felder **Seite** und **Tabelle**, die grundlegende Details anzeigen, die sie an ihr Support Team weitergeben können.

## <a name="see-also"></a>Siehe auch

[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]