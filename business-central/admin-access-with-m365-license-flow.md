---
title: Benutzerzugriffsflow für Microsoft 365-Lizenzen
description: 'Verschaffen Sie sich einen Überblick darüber, was passiert, wenn ein Benutzer mit seiner Microsoft 365-Lizenz zum ersten Mal auf Business Central-Daten zugreift.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---
# <a name="user-access-flow-for-microsoft-365-licenses"></a><a name="user-access-flow-for-microsoft-365-licenses"></a><a name="user-access-flow-for-microsoft-365-licenses"></a>Benutzerzugriffsflow für Microsoft 365-Lizenzen

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Dieser Artikel beschreibt, was passiert, wenn ein Benutzer mit seiner Microsoft 365-Lizenz zum ersten Mal auf Business Central-Daten zugreift. Das Verständnis dieses Flows ermöglicht es Administratoren, ihren Ansatz zu planen und Business Central so zu konfigurieren, dass es ihren Geschäftsanforderungen entspricht.

1. Zuerst wird die Identität des Benutzers authentifiziert 
2. Business Central überprüft, ob alle [Mindestanforderungen](admin-access-with-m365-license.md#minimum-requirements) erfüllt sind.
3. Business Central überprüft, ob dieser Benutzer keine größere Lizenz hat, wie z. B. eine Business Central-Lizenz oder eine Administratorrolle, wie z. B. eine delegierte Administratorrolle. 
4. Business Central überprüft, ob der Benutzer auf Daten zugreift, die zu einer Umgebung gehören, für die der Zugriff mit Microsoft 365-Lizenzen aktiviert ist. 
5. Der Benutzerdatensatz wird in Business Central bereitgestellt, wobei die in der Microsoft 365-Lizenzkonfigurationsseite definierten Angaben zu Benutzergruppe, Profil und Berechtigungssätzen zugewiesen werden. Standardmäßig wird die Benutzergruppe „Teams-Benutzer“ zugewiesen, das Profil „Mitarbeiter“ wird zugewiesen und nur der Berechtigungssatz „Anmeldung“ wird zugewiesen. Alle anderen standardmäßigen Benutzereinstellungen werden ebenfalls angewendet, genau wie bei einem lizenzierten Business Central-Benutzer. 
6. Das vollständige Business Central-Sicherheitsmodell wird angewendet, um zu bestimmen, ob der Benutzer in der angegebenen Firma und in der angegebenen Umgebung auf den Datensatz oder die Seite zugreifen können soll. 

Wenn alle Schritte erfolgreich sind, kann der Benutzer diese Business Central-Daten jetzt in Teams anzeigen. Der Business Central-Dienst stellt automatisch einen schreibgeschützten Zugriff sicher und vereinfacht die Benutzeroberfläche. 

Das Benutzerkonto ist nun in Business Central registriert und kann wie jeder andere Business Central-Benutzer verwaltet werden.

> [!NOTE]
> Die Schritte können je nach zusätzlicher Sicherheitskonfiguration, die Sie in Microsoft 365 oder Business Central angegeben haben, variieren.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Business Central-Zugriff mit Microsoft 365-Lizenzen](admin-access-with-m365-license.md#minimum-requirements)  
[Zugriff mit Microsoft 365-Lizenzen einrichten](admin-access-with-m365-license-setup.md)  
