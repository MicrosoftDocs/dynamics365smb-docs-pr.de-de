---
title: Verwenden einen Power Automate Flow für Warnungen zu Entitätsänderungen
description: Erfahren Sie, wie Sie einen Flow in Power Automate erstellen, der Sie benachrichtigt, wenn eine Entität geändert wird in der Dataverse Umgebung.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power Automate, Flow, Dataverse
ms.search.form: ''
ms.date: 09/05/2022
ms.author: bholtorf
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: fb5b2fa88289ff3d9d491f9b8ee7d73706740020
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9461267"
---
# <a name="use-a-power-automate-flow-for-alerts-to-dataverse-entity-changes"></a>Verwenden einen Power Automate Flow für Warnungen zu Dataverse Entitätsänderungen

> [!IMPORTANT]
> Dieser Artikel beschreibt Funktionen, die in der 2. Veröffentlichungswelle 2022 verfügbar sein werden. Bis diese Version verfügbar ist, können Sie keinen Power Automate Flow verwenden, um benachrichtigt zu werden, wenn eine Entität in Dataverse geändert wird.

Administratoren können einen automatisierten Flow in Power Automate erstellen, der [!INCLUDE[prod_short](includes/prod_short.md)] über Änderungen an Datensätzen in Ihrer [!INCLUDE [cds_long_md](includes/cds_long_md.md)] Organisation benachrichtigt.

> [!NOTE]
> Dieser Artikel geht davon aus, dass Sie Ihre Online-Version von [!INCLUDE[prod_short](includes/prod_short.md)] mit [!INCLUDE [cds_long_md](includes/cds_long_md.md)] verbunden haben und eine  Synchronisierung zwischen den beiden Anwendungen geplant haben.

## <a name="define-the-flow-trigger"></a>Flowtrigger definieren

1. Anmelden bei [Power Automate](https://flow.microsoft.com).
2. Erstellen Sie einen automatisierten Cloud-Flow, der startet, wenn eine Zeile für eine[!INCLUDE [cds_long_md](includes/cds_long_md.md)] Entität hinzugefügt, geändert oder gelöscht wird. Weitere Informationen finden Sie unter [Lösen Sie Flows aus, wenn eine Zeile hinzugefügt, geändert oder gelöscht wird](/power-automate/dataverse/create-update-delete-trigger). Dieses Beispiel verwendet die Entität **Konten**. Die folgende Abbildung zeigt die Einstellungen für den ersten Schritt beim Definieren eines Flow-Triggers.

:::image type="content" source="media/power-automate-flow-dataverse-trigger.png" alt-text="Einstellungen für den Trigger des Flows":::

3. Verwenden Sie **AssistEdit (...)** in der oberen rechten Ecke, um die Verbindung zu Ihrer Umgebung [!INCLUDE [cds_long_md](includes/cds_long_md.md)] hinzuzufügen.
4. Wählen Sie **Erweiterte Optionen anzeigen**, und geben Sie im Feld **Zeilen filtern** **customertypecode eq 3** oder **customertypecode eq 11** und **statecode eq 0** ein. Diese Werte bedeuten, dass der Trigger nur reagiert, wenn Änderungen an aktiven Konten des Typs **Debitor** oder **Kreditor** vorgenommen werden.

## <a name="define-the-flow-condition"></a>Flowbedingung definieren

Daten werden zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE [cds_long_md](includes/cds_long_md.md)] über ein Integrationsbenutzerkonto synchronisiert. Um die durch die Synchronisierung vorgenommenen Änderungen zu ignorieren, erstellen Sie einen Bedingungsschritt in Ihrem Schema, der Änderungen ausschließt, die vom Integrationsbenutzerkonto vorgenommen wurden.  

1. Fügen Sie den Schritt **Zeile aus Dataverse nach ID abrufen** nach dem Flow-Trigger mit den folgenden Einstellungen hinzu. Weitere Informationen finden Sie unter [Zeile aus Dataverse nach ID abrufen](/power-automate/dataverse/get-row-id).
    1. Wählen Sie im Feld **Tabellenname** die Option **Benutzer** aus.
    2. Wählen Sie im Feld **Zeilen-ID** wählen Sie **Geändert von (Wert)** vom Flow-Trigger aus.  
2. Fügen Sie einen Bedingungsschritt wie mit den folgenden **oder** Einstellungen zum Identifizieren des Integrationsbenutzerkontos hinzu.
    1. Die **Haupt-Email-Adresse** des Benutzers enthält **contoso.com** 
    2. Der **Vollständige Name** des Benutzers enthält **[!INCLUDE[prod_short](includes/prod_short.md)]**. 
3. Fügen Sie ein Terminate-Steuerelement hinzu, um den Flow zu stoppen, wenn die Bedingung erfüllt ist. Das heißt, wenn die Bedingung erfüllt ist und eine Entität durch das Integrationsbenutzerkonto geändert wurde.

Die folgende Abbildung zeigt die Informationen, die hinzugefügt werden müssen, um den Flow-Trigger und die Flow-Bedingung zu definieren.

:::image type="content" source="media/power-automate-flow-dataverse.png" alt-text="Übersicht über Flow-Trigger und Bedingungseinstellungen":::

## <a name="notify-business-central-about-a-change"></a>Benachrichtigen Sie Business Central über eine Änderung

Wenn der Flow nicht durch die Bedingung gestoppt wird, müssen Sie [!INCLUDE[prod_short](includes/prod_short.md)] benachrichtigen, dass eine Änderung eingetreten ist. Verwenden Sie dazu den Connector [!INCLUDE[prod_short](includes/prod_short.md)].

1. In der Verzweigung **Nein** des Bedingungsschritts, fügen Sie eine Aktion hinzu und suchen Sie nach **Dynamics 365[!INCLUDE[prod_short](includes/prod_short.md)]**. Wählen Sie das Connector-Symbol in der Liste. 
2. Wählen Sie die Aktion **Datensatz erstellen (V3)** aus.

:::image type="content" source="media/power-automate-flow-dataverse-connector.png" alt-text="Einstellungen für den [!INCLUDE[prod_short](includes/prod_short.md)]-Konnektor":::

3. Verwenden Sie **AssistEdit (...)** in der oberen rechten Ecke, um die Verbindung zu Ihrer [!INCLUDE[prod_short](includes/prod_short.md)] hinzuzufügen.
4. Wenn Sie verbunden sind, füllen Sie **Umgebungsname** und **Unternehmensname** aus.
5. Geben Sie im Feld **API-Kategorie** **microsoft/dataverse/v1.0** ein.
6. Geben Sie im Feld **Tabellenname** **dataverseEntityChanges** ein.
7. Geben Sie im Feld **entityName** **Konto** ein.
8. Speichern Sie den Flow.

Ihr Workflow sollte nun wie im Bild unten aussehen.

:::image type="content" source="media/power-automate-flow-dataverse-summary.png" alt-text="Übersicht aller Einstellungen für den Flow":::

Wenn Sie ein Konto in Ihrer [!INCLUDE [cds_long_md](includes/cds_long_md.md)] Umgebung hinzufügen, löschen oder ändern, führt dieser Flow die folgenden Aktionen aus:

1. Rufen Sie die [!INCLUDE[prod_short](includes/prod_short.md)] Umgebung auf, die Sie im Connector [!INCLUDE[prod_short](includes/prod_short.md)] angegeben haben. 
2. Verwenden Sie die [!INCLUDE[prod_short](includes/prod_short.md)] API zum Einfügen eines Datensatzes mit **Entitätsname** gesetzt auf **Konto** in der Tabelle **Dataverse-Eintragsänderung** Tisch. 3. [!INCLUDE[prod_short](includes/prod_short.md)] startet den Auftragswarteschlangeneintrag, der Debitoren mit Konten synchronisiert.

## <a name="see-also"></a>Siehe auch

[Business Central in Power Automate-Flows verwenden](across-how-use-financials-data-source-flow.md)  
[Automatisierte Workflows einrichten](/business-central/dev-itpro/powerplatform/automate-workflows)  
[Integrieren in Microsoft Dataverse](admin-common-data-service.md)  
[Synchronisieren von Daten in Business Central mit Microsoft Dataverse](admin-synchronizing-business-central-and-sales.md)  
