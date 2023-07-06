---
title: Fehlerbehebung bei Synchronisationsfehlern
description: 'Dieses Thema enthält einige Anleitungen zur Identifizierung, Problembehandlung und Behebung von Synchronisationsfehlern.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/14/2021
ms.author: bholtorf
---
# <a name="troubleshooting-synchronization-errors"></a><a name="troubleshooting-synchronization-errors"></a><a name="troubleshooting-synchronization-errors"></a>Fehlerbehebung bei Synchronisationsfehlern


Bei der Integration von [!INCLUDE[prod_short](includes/prod_short.md)] mit [!INCLUDE[prod_short](includes/cds_long_md.md)] sind viele bewegliche Teile beteiligt und manchmal laufen die Dinge schief. In diesem Thema werden einige der typischen Fehler aufgeführt, die auftreten, und es werden einige Hinweise zu deren Behebung gegeben.

Fehler treten häufig auf, wenn ein Benutzer gekoppelte Datensätze bearbeitet hat oder wenn ein Fehler bei der Einrichtung der Integration aufgetreten ist. Bei Fehlern im Zusammenhang mit gekoppelten Datensätzen können Benutzer diese selbst beheben. Diese Fehler werden durch Aktionen verursacht, z. B. Löschen von Daten, jedoch nicht in beiden Geschäftsanwendungen und anschließendes Synchronisieren. Weitere Informationen finden Sie unter [Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md).

Fehler im Zusammenhang mit der Einrichtung der Integration erfordern in der Regel die Aufmerksamkeit eines Administrators. Sie können diese Fehler auf der Seite **Integration von Synchronisationsfehlern** anzeigen. 

Die folgende Tabelle enthält Beispiele für typische Probleme:  

|Problem  |Auflösung  |
|---------|---------|
|Die dem Integrationsbenutzer zugewiesenen Berechtigungen und Rollen sind nicht korrekt. | Dieser Fehler kommt von [!INCLUDE[prod_short](includes/cds_long_md.md)] und enthält oft den folgenden Text "Hauptbenutzer (ID=\<user id>, type=8) fehlt Berechtigung \<privilegeName>". Dieser Fehler tritt auf, weil dem Integrationsbenutzer eine Berechtigung fehlt, die ihm den Zugriff auf eine Entität ermöglicht. Dieser Fehler tritt normalerweise auf, wenn Sie benutzerdefinierte Entitäten synchronisieren oder eine App in [!INCLUDE[prod_short](includes/cds_long_md.md)] installiert haben, die die Erlaubnis erfordert, auf andere [!INCLUDE[prod_short](includes/cds_long_md.md)] Entitäten zuzugreifen. Um diesen Fehler zu beheben, weisen Sie dem Integrationsbenutzer in [!INCLUDE[prod_short](includes/cds_long_md.md)] die Berechtigung zu.<br><br> Den Integrationsbenutzernamen finden Sie auf der **Dataverse Verbindungsaufbau** Seite. Die Fehlermeldung enthält den Namen der Berechtigung, der Ihnen helfen kann, die Entität zu identifizieren, für die Sie eine Berechtigung benötigen. Um die fehlende Berechtigung hinzuzufügen, melden Sie sich bei [!INCLUDE[prod_short](includes/cds_long_md.md)] mit einem Administratorkonto und bearbeiten Sie die dem Integrationsbenutzer zugewiesene Sicherheitsrolle. Weitere Informationen finden Sie unter [Erstellen und Bearbeiten einer Sicherheitsrolle zur Zugriffsverwaltung](/power-platform/admin/create-edit-security-role). |
|Sie koppeln einen Datensatz, der einen anderen nicht gekoppelten Datensatz verwendet. Beispiel: ein Kunde, dessen Währung nicht gekoppelt ist, oder eine Position, für die die Mengeneinheit nicht gekoppelt ist. | Sie müssen zuerst den abhängigen Datensatz, z.B eine Währung oder Einheit, koppeln und dann die Kopplung erneut versuchen. |

Im Folgenden finden Sie einige Tools auf der Seite Fehler bei der Integrationssynchronisierung, mit denen Sie diese Probleme manuell beheben können.  

* Die Felder **Quelle** und **Ziel** können Links zu dem Zeilen enthalten, in dem der Fehler gefunden wurde. Klicken Sie auf den Link, um den Fehler zu untersuchen.  
* Die Aktion **Einträge löschen, die älter als 7 Tage sind** und die Aktion **Alle Einträge löschen** wird die Liste bereinigen. In der Regel verwenden Sie diese Aktionen, nachdem Sie die Ursache eines Fehlers behoben haben, der viele Datensätze betrifft. Vorsicht walten lassen. Durch diese Aktionen werden möglicherweise noch relevante Fehler gelöscht.
* Die Aktion **Fehleraufrufstapel anzeigen** zeigt Informationen an, die helfen können, die Ursache des Fehlers zu identifizieren. Wenn Sie den Fehler nicht selbst beheben können und sich entscheiden, eine Supportanfrage zu stellen, fügen Sie die Informationen in die Supportanfrage ein.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Weitere Informationen
[Integration in Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Einrichten des Benutzerkontos für die Integration in Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Richten Sie eine Verbindung mit Microsoft Dataverse ein](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md)  
[Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
