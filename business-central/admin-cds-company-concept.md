---
title: Zuordnung von Unternehmen und Geschäftsbereichen | Microsoft Docs
description: Unternehmen sind sowohl ein rechtliches als auch ein geschäftliches Konstrukt, und sie werden zur Sicherung und Visualisierung von Geschäftsdaten verwendet.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: CDS, , integration, sync
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 22411c8392cf81b25b1f11f221bbd98942f653f4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754092"
---
# <a name="data-ownership-models"></a>Modelle für Datenbesitz
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

[!INCLUDE[prod_short](includes/cds_long_md.md)] erfordert, dass Sie einen Eigentümer für die von Ihnen gespeicherten Daten angeben. Weitere Informationen finden Sie unter [Entitätseigentum](https://docs.microsoft.com/powerapps/maker/common-data-service/types-of-tables#table-ownership) in der Power Apps-Dokumentation. Wenn Sie die Integration zwischen [!INCLUDE[prod_short](includes/cds_long_md.md)] und [!INCLUDE[prod_short](includes/prod_short.md)] einrichten, müssen Sie eines von zwei Eigentumsmodellen für Datensätze wählen, die synchronisiert werden:

* Team 
* Person (Benutzer)

Aktionen, die mit diesen Datensätzen ausgeführt werden können, können auf Benutzerebene gesteuert werden. Weitere Informationen finden Sie unter [Benutzer- und Teamtabellen](https://docs.microsoft.com/powerapps/developer/common-data-service/user-team-tables). Wir empfehlen das Team-Eigentümermodell, da es die Verwaltung der Eigentümerschaft für mehrere Personen erleichtert.

## <a name="team-ownership"></a>Team-Eigentum
In [!INCLUDE[prod_short](includes/prod_short.md)] ist ein Unternehmen eine juristische und geschäftliche Tabelle, die Möglichkeiten zur Sicherung und Visualisierung von Geschäftsdaten bietet. Benutzer arbeiten immer im Kontext eines Unternehmens. Diesem Konzept kommt [!INCLUDE[prod_short](includes/cds_long_md.md)] am nächsten, da die Geschäftseinheitstabelle keine rechtlichen oder geschäftlichen Auswirkungen hat.

Da Geschäftseinheiten keine rechtlichen und geschäftlichen Auswirkungen haben, können Sie keine eins-zu-eins (1:1)-Abbildung erzwingen, um Daten zwischen einem Unternehmen und einer Geschäftseinheit zu synchronisieren, weder einseitig noch bidirektional. Um die Synchronisierung zu ermöglichen, geschieht, wenn Sie die Synchronisierung für ein Unternehmen in [!INCLUDE[prod_short](includes/prod_short.md)] aktivieren, Folgendes in [!INCLUDE[prod_short](includes/cds_long_md.md)]:

* Wir schaffen eine Unternehmenstabelle, die der Unternehmenstabelle in [!INCLUDE[prod_short](includes/prod_short.md)] entspricht. Der Name des Unternehmens wird mit dem Suffix „BC Unternehmens-ID“ versehen. Zum Beispiel Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Wir legen eine Standard-Geschäftseinheit an, die den gleichen Namen wie die Unternehmenseinheit hat. Zum Beispiel Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Wir legen ein separates Eigentümerteam mit demselben Namen wie das Unternehmen an und ordnen es der Geschäftseinheit zu. Dem Namen der Gruppe wird „BCI -“ vorangestellt. Beispielsweise BCI - Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Datensätze, die erstellt und mit [!INCLUDE[prod_short](includes/cds_long_md.md)] synchronisiert werden, werden dem „BCI-Besitzer“-Team zugeordnet, das mit dem Geschäftsbereich verbunden ist.

> [!NOTE]
> Wenn Sie ein Unternehmen in [!INCLUDE[prod_short](includes/prod_short.md)] umbenennen, werden die Namen des Unternehmens, des Konzernmandanten und des Teams, die wir automatisch in [!INCLUDE[prod_short](includes/cds_long_md.md)] erstellen, nicht aktualisiert. Da nur die Unternehmens-ID für die Integration verwendet wird, wirkt sich dies nicht auf die Synchronisierung aus. Wenn die Namen übereinstimmen sollen, müssen Sie das Unternehmen, den Konzernmandant und das Team in [!INCLUDE[prod_short](includes/cds_long_md.md)] aktualisieren.

Die folgende Abbildung zeigt ein Beispiel für diese Dateneinrichtung in [!INCLUDE[prod_short](includes/cds_long_md.md)].

![Der Stamm-Geschäftsbereich steht oben, die Teams in der Mitte, und dann die Unternehmen ganz unten.](media/cds_bu_team_company.png)

In dieser Konfiguration werden Datensätze, die sich auf die Firma Cronus US beziehen, einem Team gehören, das mit dem Cronus US-Geschäftsbereich <ID> in [!INCLUDE[prod_short](includes/cds_long_md.md)] verbunden ist. Benutzer, die auf diese Geschäftseinheit über eine Sicherheitsrolle zugreifen können, die in [!INCLUDE[prod_short](includes/cds_long_md.md)] auf Sichtbarkeit auf Geschäftseinheitsebene eingestellt ist, können nun diese Datensätze sehen. Das folgende Beispiel zeigt, wie Teams eingesetzt werden können, um den Zugriff auf diese Datensätze zu ermöglichen.

* Die Rolle des Vertriebsleiters wird den Mitgliedern des US-Vertriebsteams von Cronus zugewiesen.
* Benutzer, die die Rolle Vertriebsleiter haben, können auf Kontoaufzeichnungen für Mitglieder derselben Geschäftseinheit zugreifen.
* Das US-Verkaufsteam von Cronus ist mit der bereits erwähnten Geschäftseinheit von Cronus US verbunden. Mitglieder des Cronus US-Verkaufsteams können jedes Konto sehen, das dem Cronus US-Benutzer <ID> gehört, das von der Cronus US-Firmentabelle in [!INCLUDE[prod_short](includes/prod_short.md)] gekommen wäre.

Die 1:1-Abbildung zwischen Geschäftseinheit, Unternehmen und Team ist jedoch nur ein Ausgangspunkt, wie in der folgenden Abbildung gezeigt.

![Die Sicherheitsrolle steuert die Datentransparenz.](media/cds_bu_team_company_2.png)

In diesem Beispiel wird eine neue EUR (Europa) Stamm-Geschäftseinheit in [!INCLUDE[prod_short](includes/cds_long_md.md)] als Muttergesellschaft sowohl für Cronus DE (Gernamy) als auch für Cronus ES (Spanien) angelegt. Der EUR-Geschäftsbereich ist nicht mit der Synchronisation verbunden. Es kann jedoch Mitgliedern des EUR-Verkaufsteams Zugriff auf Kontodaten sowohl in Cronus DE als auch in Cronus ES geben, indem die Datensichtbarkeit auf **Übergeordnete/untergeordnete GE** auf die zugehörige Sicherheitsrolle in [!INCLUDE[prod_short](includes/cds_long_md.md)] gesetzt wird.

Die Synchronisation bestimmt, welches Team Datensätze besitzen soll. Dies wird durch das Feld **Standardeigentümerteam** auf dem BCI - <ID> Zeile gesteuert. Wenn ein BCI - <ID>-Datensatz für die Synchronisierung aktiviert wird, erstellen wir automatisch die zugehörige Geschäftseinheit und das Eigentümerteam (falls noch nicht vorhanden) und setzen das Feld **Standard Eigentümerteam**. Wenn die Synchronisierung für eine Tabelle aktiviert ist, können Administratoren das besitzende Team ändern, aber es muss immer ein Team zugewiesen werden.

> [!NOTE]
> Die Aufzeichnungen werden schreibgeschützt, nachdem eine Firma hinzugefügt und gespeichert wurde, also achten Sie darauf, die richtige Firma zu wählen.

## <a name="choosing-a-different-business-unit"></a>Auswahl einer anderen Geschäftseinheit
Sie können die Auswahl des Konzernmandanten ändern, wenn Sie das Modell „Team-Eigentum“ verwenden. Wenn Sie das Modell „Personenbesitz“ verwenden, wird immer der Standard-Konzernmandant ausgewählt. 

Wenn Sie einen anderen Konzernmandanten auswählen, z. B. einen, den Sie zuvor in [!INCLUDE[prod_short](includes/cds_long_md.md)] angelegt haben, behält er seinen ursprünglichen Namen. Das heißt, es wird nicht mit dem Suffix der Firmen-ID versehen. Wir werden ein Team zusammenstellen, das die Namenskonvention anwendet.

Beim Ändern eines Konzernmandanten können Sie nur die Konzernmandanten auswählen, die eine Ebene unter dem Stamm-Konzernmandanten liegen.

## <a name="person-ownership"></a>Eigentum der Person
Wenn Sie das Modell Personenbesitz wählen, müssen Sie jeden Verkäufer angeben, der neue Datensätze besitzen wird. Der Konzernmandant und das Team werden wie im vorherigen Abschnitt [Team-Besitz](admin-cds-company-concept.md#team-ownership) beschrieben angelegt.

Der Standard-Konzernmandant wird verwendet, wenn das Modell „Personenbesitz“ ausgewählt ist, und Sie können keinen anderen Konzernmandanten auswählen. Das Team, das dem Standard-Konzernmandanten zugeordnet ist, besitzt Datensätze für allgemeine Tabellen, z. B. die Produkttabellen, die nicht mit bestimmten Verkäufern verknüpft sind.

Wenn Sie Verkäufer in [!INCLUDE[prod_short](includes/prod_short.md)] mit Benutzern in [!INCLUDE[prod_short](includes/cds_long_md.md)] koppeln, fügt [!INCLUDE[prod_short](includes/prod_short.md)] den Benutzer dem Standardteam in [!INCLUDE[prod_short](includes/cds_long_md.md)] hinzu. Sie können überprüfen, ob Benutzer hinzugefügt wurden, indem Sie sich die Spalte **Standardteam-Mitglied** auf der Seite **Benutzer - Common Data Service** ansehen. Wenn der Benutzer nicht hinzugefügt wurde, können Sie ihn manuell mithilfe der Aktion **Gekoppelte Benutzer dem Team hinzufügen** hinzufügen. Weitere Informationen finden Sie unter [Synchronisieren von Daten in Business Central mit Dataverse](admin-synchronizing-business-central-and-sales.md).

## <a name="see-also"></a>Siehe auch
[Über [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-common-data-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]