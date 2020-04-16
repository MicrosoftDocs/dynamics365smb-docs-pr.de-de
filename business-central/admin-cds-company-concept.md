---
title: Zuordnung von Unternehmen und Geschäftsbereichen | Microsoft Docs
description: Unternehmen sind sowohl ein rechtliches als auch ein geschäftliches Konstrukt, und sie werden zur Sicherung und Visualisierung von Geschäftsdaten verwendet.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: CDS, Common Data Service, integration, sync
ms.date: 01/17/2020
ms.author: bholtorf
ms.openlocfilehash: ccd371711a53c598279fcc981c5581be5ee9bdaf
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196865"
---
# <a name="data-ownership-models"></a>Modelle für Datenbesitz
[!INCLUDE[d365fin](includes/cds_long_md.md)] erfordert, dass Sie einen Eigentümer für die von Ihnen gespeicherten Daten angeben. Weitere Informationen finden Sie unter [Entitätseigentum](https://docs.microsoft.com/powerapps/maker/common-data-service/types-of-entities#entity-ownership) in der Power Apps-Dokumentation. Wenn Sie die Integration zwischen [!INCLUDE[d365fin](includes/cds_long_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] einrichten, müssen Sie eines von zwei Eigentumsmodellen für Datensätze wählen, die synchronisiert werden:

* Team 
* Person (Benutzer)

Aktionen, die mit diesen Datensätzen ausgeführt werden können, können auf Benutzerebene gesteuert werden. Weitere Informationen finden Sie unter [Benutzer- und Teamentitäten](https://docs.microsoft.com/powerapps/developer/common-data-service/user-team-entities). Wir empfehlen das Team-Eigentümermodell, da es die Verwaltung der Eigentümerschaft für mehrere Personen erleichtert.

## <a name="team-ownership"></a>Team-Eigentum
In [!INCLUDE[d365fin](includes/d365fin_md.md)] ist ein Unternehmen eine juristische und geschäftliche Entität, die Möglichkeiten zur Sicherung und Visualisierung von Geschäftsdaten bietet. Benutzer arbeiten immer im Kontext eines Unternehmens. Diesem Konzept kommt [!INCLUDE[d365fin](includes/cds_long_md.md)] am nächsten, da die Geschäftseinheit keine rechtlichen oder geschäftlichen Auswirkungen hat.

Da Geschäftseinheiten keine rechtlichen und geschäftlichen Auswirkungen haben, können Sie keine eins-zu-eins (1:1)-Abbildung erzwingen, um Daten zwischen einem Unternehmen und einer Geschäftseinheit zu synchronisieren, weder einseitig noch bidirektional. Um die Synchronisierung zu ermöglichen, geschieht, wenn Sie die Synchronisierung für ein Unternehmen in [!INCLUDE[d365fin](includes/d365fin_md.md)] aktivieren, Folgendes in [!INCLUDE[d365fin](includes/cds_long_md.md)]:

* Wir schaffen eine Unternehmenseinheit, die der Unternehmenseinheit in [!INCLUDE[d365fin](includes/d365fin_md.md)] entspricht. Der Name des Unternehmens wird mit dem Suffix „BC Unternehmens-ID“ versehen. Zum Beispiel Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Wir legen eine Standard-Geschäftseinheit an, die den gleichen Namen wie die Unternehmenseinheit hat. Zum Beispiel Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Wir legen ein separates Eigentümerteam mit demselben Namen wie das Unternehmen an und ordnen es der Geschäftseinheit zu. Dem Namen der Gruppe wird „BCI -“ vorangestellt. Beispielsweise BCI - Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Datensätze, die erstellt und mit [!INCLUDE[d365fin](includes/cds_long_md.md)] synchronisiert werden, werden dem „BCI-Besitzer“-Team zugeordnet, das mit dem Geschäftsbereich verbunden ist.

Die folgende Abbildung zeigt ein Beispiel für diese Dateneinrichtung in [!INCLUDE[d365fin](includes/cds_long_md.md)].

![Der Stamm-Geschäftsbereich steht oben, die Teams in der Mitte, und dann die Unternehmen ganz unten.](media/cds_bu_team_company.png)

In dieser Konfiguration werden Datensätze, die sich auf die Firma Cronus US beziehen, einem Team gehören, das mit dem Cronus US-Geschäftsbereich <ID> in [!INCLUDE[d365fin](includes/cds_long_md.md)] verbunden ist. Benutzer, die auf diese Geschäftseinheit über eine Sicherheitsrolle zugreifen können, die in [!INCLUDE[d365fin](includes/cds_long_md.md)] auf Sichtbarkeit auf Geschäftseinheitsebene eingestellt ist, können nun diese Datensätze sehen. Das folgende Beispiel zeigt, wie Teams eingesetzt werden können, um den Zugriff auf diese Datensätze zu ermöglichen.

* Die Rolle des Vertriebsleiters wird den Mitgliedern des US-Vertriebsteams von Cronus zugewiesen.
* Benutzer, die die Rolle Vertriebsleiter haben, können auf Kontoaufzeichnungen für Mitglieder derselben Geschäftseinheit zugreifen.
* Das US-Verkaufsteam von Cronus ist mit der bereits erwähnten Geschäftseinheit von Cronus US verbunden. Mitglieder des Cronus US-Verkaufsteams können jedes Konto sehen, das dem Cronus US-Benutzer <ID> gehört, das von der Cronus US-Firmeneinheit in [!INCLUDE[d365fin](includes/d365fin_md.md)] gekommen wäre.

Die 1:1-Abbildung zwischen Geschäftseinheit, Unternehmen und Team ist jedoch nur ein Ausgangspunkt, wie in der folgenden Abbildung gezeigt.

![Die Sicherheitsrolle steuert die Datentransparenz.](media/cds_bu_team_company_2.png)

In diesem Beispiel wird eine neue EUR (Europa) Stamm-Geschäftseinheit in [!INCLUDE[d365fin](includes/cds_long_md.md)] als Muttergesellschaft sowohl für Cronus DE (Gernamy) als auch für Cronus ES (Spanien) angelegt. Der EUR-Geschäftsbereich ist nicht mit der Synchronisation verbunden. Es kann jedoch Mitgliedern des EUR-Verkaufsteams Zugriff auf Kontodaten sowohl in Cronus DE als auch in Cronus ES geben, indem die Datensichtbarkeit auf **Übergeordnete/untergeordnete GE** auf die zugehörige Sicherheitsrolle in [!INCLUDE[d365fin](includes/cds_long_md.md)] gesetzt wird.

Die Synchronisation bestimmt, welches Team Datensätze besitzen soll. Dies wird durch das Feld **Standardeigentümerteam** auf dem BCI - <ID>-Datensatz gesteuert. Wenn ein BCI - <ID>-Datensatz für die Synchronisierung aktiviert wird, erstellen wir automatisch die zugehörige Geschäftseinheit und das Eigentümerteam (falls noch nicht vorhanden) und setzen das Feld **Standard Eigentümerteam**. Wenn die Synchronisierung für eine Entität aktiviert ist, können Administratoren das besitzende Team ändern, aber es muss immer ein Team zugewiesen werden.

> [!NOTE]
> Die Aufzeichnungen werden schreibgeschützt, nachdem eine Firma hinzugefügt und gespeichert wurde, also achten Sie darauf, die richtige Firma zu wählen.

### <a name="choosing-a-different-business-unit"></a>Auswahl einer anderen Geschäftseinheit
Sie können die Geschäftsbereichsauswahl ändern. Wenn Sie eine andere Einheit wählen, z.B. eine, die Sie zuvor im CDS angelegt haben, behält sie ihren ursprünglichen Namen. Das heißt, es wird nicht mit dem Suffix der Firmen-ID versehen. Wir werden ein Team zusammenstellen, das die Namenskonvention anwendet.

## <a name="person-ownership"></a>Eigentum der Person
Wenn Sie das Modell Personenbesitz wählen, müssen Sie jeden Verkäufer angeben, der neue Datensätze besitzen wird. Die Geschäftseinheit und das Team werden wie im vorherigen Abschnitt beschrieben angelegt.  

## <a name="see-also"></a>Siehe auch
[Über [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-common-data-service.md)