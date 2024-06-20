---
title: Fehlerbehebung bei Synchronisationsfehlern
description: 'Dieser Artikel enthält Anleitungen zur Identifizierung, Problembehandlung und Behebung von Synchronisierungsfehlern.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/04/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="troubleshoot-synchronization-errors"></a>Synchronisierungsfehler beheben

Bei der Integration von [!INCLUDE[prod_short](includes/prod_short.md)] mit [!INCLUDE[prod_short](includes/cds_long_md.md)] sind viele bewegliche Teile beteiligt und manchmal laufen die Dinge schief. Dieser Artikel geht einige typische Fehler durch, die auftreten, und enthält einige Hinweise zu deren Behebung.

Fehler treten häufig auf, wenn Benutzende gekoppelte Datensätze bearbeitet haben oder wenn ein Fehler bei der Einrichtung der Integration aufgetreten ist. Bei Fehlern im Zusammenhang mit gekoppelten Datensätzen können Benutzende diese selbst beheben. Ursachen für diese Fehler sind häufig Aktionen, z. B. wenn Daten gelöscht werden, jedoch nicht in beiden Geschäftsanwendungen, und anschließend eine Synchronisierung vorgenommen wird. Weitere Informationen finden Sie unter [Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md).

Fehler im Zusammenhang mit der Einrichtung der Integration erfordern in der Regel die Aufmerksamkeit eines Administrators. Sie können diese Fehler auf der Seite **Integration von Synchronisationsfehlern** anzeigen. 

Die folgende Tabelle enthält Beispiele für typische Probleme:  

|Problem  |Auflösung  |
|---------|---------|
|Die den Integrationsbenutzenden zugewiesenen Berechtigungen und Rollen sind nicht korrekt. | Dieser Fehler kommt von [!INCLUDE[prod_short](includes/cds_long_md.md)] und enthält oft den folgenden Text: **Hauptbenutzender (Id=\<user id>, type=8) fehlt Berechtigung \<privilegeName>**. Dieser Fehler tritt auf, weil dem Integrationsbenutzer eine Berechtigung fehlt, die ihm den Zugriff auf eine Entität ermöglicht. Dieser Fehler tritt normalerweise auf, wenn Sie benutzerdefinierte Entitäten synchronisieren oder eine App in [!INCLUDE[prod_short](includes/cds_long_md.md)] installiert haben, welche die Berechtigung erfordert, auf andere [!INCLUDE[prod_short](includes/cds_long_md.md)] Entitäten zuzugreifen. Um diesen Fehler zu beheben, weisen Sie dem Integrationsbenutzer in [!INCLUDE[prod_short](includes/cds_long_md.md)] die Berechtigung zu.<br><br> Den Integrationsbenutzernamen finden Sie auf der **Dataverse Verbindungsaufbau** Seite. Die Fehlermeldung enthält den Namen der Berechtigung, der Ihnen helfen kann, die Entität zu identifizieren, für die Sie eine Berechtigung benötigen. Um die fehlende Berechtigung hinzuzufügen, melden Sie sich bei [!INCLUDE[prod_short](includes/cds_long_md.md)] mit einem Administratorkonto und bearbeiten Sie die dem Integrationsbenutzer zugewiesene Sicherheitsrolle. Weitere Informationen finden Sie unter [Erstellen und Bearbeiten einer Sicherheitsrolle zur Zugriffsverwaltung](/power-platform/admin/create-edit-security-role). |
|Sie koppeln einen Datensatz, der einen anderen nicht gekoppelten Datensatz verwendet. Beispiel: ein Debitor, dessen Währung nicht gekoppelt ist, oder ein Artikel, dessen Einheit nicht gekoppelt ist. | Sie müssen zuerst den abhängigen Datensatz, z.B eine Währung oder Einheit, koppeln und dann die Kopplung erneut versuchen. |
|Ihre Verbindung zu Dataverse wurde während der Synchronisierung angehalten. Zum Beispiel weil Ihre Sitzung abgelaufen ist. Wenn das passiert, wird beim Fortsetzen Ihrer Sitzung der folgende Fehler angezeigt: _Die Tabellenverbindung für den Tabellentyp CRM muss mit RegisterTableConnection oder dem Cmdlet New-NAVTableConnection registriert werden, bevor sie verwendet werden kann._|* Aktualisieren Sie bei Sitzungstimeouts die Seite, um die Verbindung mit Dataverse wiederherzustellen. Die Fehlermeldung verschwindet.<br><br>* Wenden Sie sich bei einem Problem im Code, z. B. wenn Sie eine benutzerdefinierte Seite verwenden, um Daten einer Dataverse-Entität anzuzeigen, an Ihren Microsoft-Partner oder den Microsoft-Support. Verwenden Sie in diesem Fall die Aktion **Details kopieren**, um Details zum Fehler weiterzugeben. |

Im Folgenden finden Sie einige Tools auf der Seite Fehler bei der Integrationssynchronisierung, mit denen Sie diese Probleme manuell beheben können.  

* Die Felder **Quelle** und **Ziel** können Links zu dem Zeilen enthalten, in dem der Fehler gefunden wurde. Wählen Sie den Link, um den Fehler zu untersuchen.  
* Die Aktion **Einträge löschen, die älter als 7 Tage sind** und die Aktion **Alle Einträge löschen** bereinigt die Liste. In der Regel verwenden Sie diese Aktionen, nachdem Sie die Ursache eines Fehlers behoben haben, der viele Datensätze betrifft. Vorsicht walten lassen. Durch diese Aktionen werden möglicherweise noch relevante Fehler gelöscht.
* Die Aktion **Fehleraufrufstapel anzeigen** zeigt Informationen an, die helfen können, die Ursache des Fehlers zu identifizieren. Wenn Sie den Fehler nicht selbst beheben können und sich entscheiden, eine Supportanfrage zu stellen, fügen Sie die Informationen in die Supportanfrage ein.

## <a name="see-also"></a>Siehe auch

[Integration in Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Einrichten des Benutzerkontos für die Integration in Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Richten Sie eine Verbindung mit Microsoft Dataverse ein](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md)  
[Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
