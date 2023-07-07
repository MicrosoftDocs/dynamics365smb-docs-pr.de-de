---
title: Business Central-Zugriff mit Microsoft 365-Lizenzen
description: 'Erfahren Sie, wie Benutzer Zugriff auf Business Central-Daten erhalten können, beispielsweise in Microsoft Teams-Chats und -Kanälen, mit nur einer Microsoft 365-Lizenz, aber keiner Business Central-Lizenz.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.date: 11/22/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# <a name="business-central-access-with-microsoft-365-licenses"></a>Business Central-Zugriff mit Microsoft 365-Lizenzen

[!INCLUDE[prod_short](includes/prod_short.md)]-Benutzern wird eine Dynamics 365 Business Central-Lizenz zugewiesen, die es ihnen ermöglicht, ihre Geschäftsdaten von jeder Benutzeroberfläche aus anzuzeigen, zu ändern und zu bearbeiten. Für alle anderen Mitarbeiter in der gesamten Organisation, die nur gelegentlich Daten anzeigen müssen, bietet Business Central einen Zugriff durch Microsoft 365.  

Wenn eine Organisation sowohl ein Dynamics 365 Business Central- und Microsoft 365-Abonnement hat, können Administratoren Umgebungen konfigurieren, um den Zugriff mit Microsoft 365-Lizenzen zu ermöglichen und genau zu wählen, auf welche Tabellen und andere Objekte diese Benutzerkategorie Zugriff haben soll. Wenn konfiguriert, können Mitarbeiter, die über eine Microsoft 365 Lizenz, aber keine [!INCLUDE [prod_short](includes/prod_short.md)]-Lizenz verfügen, [!INCLUDE [prod_short](includes/prod_short.md)]-Datensätze anzeigen, die für sie in Microsoft Teams-Chat und -Kanälen freigegeben wurden.

## <a name="why-enable-access-with-microsoft-365-licenses"></a>Warum Zugriff mit Microsoft 365-Lizenzen ermöglichen

- Schalten Sie Stammdaten frei, auf die jeder Mitarbeiter in der gesamten Organisation Zugriff haben sollte.

- Ermöglichen Sie Abteilungen, die nicht auf [!INCLUDE [prod_short](includes/prod_short.md)] laufen, die Selbstbedienung, indem sie auf Schlüsseldaten zugreifen, die für die erfolgreiche Ausführung ihrer Aufgaben erforderlich sind, wodurch die Notwendigkeit entfällt, ständig Daten von anderen anzufordern.

- Erhöhen Sie die Effizienz der Zusammenarbeit, damit Aufgaben und Projekte, die sich über Abteilungen erstrecken, rechtzeitig abgeschlossen werden, indem Sie die Reibung beseitigen, die normalerweise mit Fehlern aufgrund von Zugriffsverweigerungen aufgrund von Lizenzen verbunden ist.

- Erhöhen Sie die Teamleistung, damit Mitarbeiter datengesteuerte Entscheidungen treffen können, die alle in der Gruppe einbeziehen, auch wenn sie nicht in [!INCLUDE [prod_short](includes/prod_short.md)] arbeiten.

- Erfüllen Sie die Budgetziele für die Lizenzierung, indem Sie Lizenzen zuweisen, die den Anforderungen der Mitarbeiter nach und nach entsprechen, mit Microsoft 365-Lizenzen für Nur-Lese-Zugriff, Dynamics 365 Business Central Team Mitglieder-Lizenzen für eingeschränkten Schreibzugriff und Dynamics 365 Business Central Essentials oder Premium für vollen Schreibzugriff.

- Verbessern Sie die Datensicherheit, indem Sie die Notwendigkeit verringern, Bildschirmausschnitte von Geschäftsdaten außerhalb der Data-Governance-Grenzen einzufügen.

## <a name="use-rights"></a>Nutzungsrechte

Wenn eine Person mit einer Microsoft 365-Lizenz auf [!INCLUDE [prod_short](includes/prod_short.md)] zugreift, berechtigt diese Lizenz den Benutzer, Business Central-Daten über eine vereinfachte Microsoft Teams Benutzeroberfläche in [!INCLUDE [prod_short](includes/prod_short.md)] zu lesen (aber nicht zu schreiben). In diesem Abschnitt werden diese Nutzungsrechte und Einschränkungen erläutert, die Ihnen bei der Planung der Konfiguration und optimalen Nutzung dieser Funktion helfen. Weitere Informationen zu diesem Lizenztyp im Vergleich zu anderen [!INCLUDE [prod_short](includes/prod_short.md)]-Lizenzen finden Sie im [Dynamics 365-Lizenzierungshandbuch](https://go.microsoft.com/fwlink/?LinkId=866544).
 
### <a name="client-access"></a>Clientzugriff

Benutzer sind berechtigt, auf [!INCLUDE [prod_short](includes/prod_short.md)]-Daten in Microsoft Teams zuzugreifen. Die folgende Tabelle fasst zusammen, welche der unterschiedlichen Methoden des Zugriffs auf den [!INCLUDE [prod_short](includes/prod_short.md)] mit dieser Lizenz erlaubt sind.

|Client, der auf den Business Central-Dienst zugreift |Zugriff|
|-|-|
|Business Central-App für Microsoft Teams|![Ja](media/check.png)|
|Business Central-Webclient |![Nein](media/x-icon.png ) |
|Business Central-Apps für Mobilgeräte|![Nein](media/x-icon.png )|
|Business Central-APIs|![Nein](media/x-icon.png )|
|Business Central-Integrationen mit anderen Office-Anwendungen|![Nein](media/x-icon.png )|
|Business Central ist in andere Anwendungen eingebettet |![Nein](media/x-icon.png )|

### <a name="data-access"></a>Datenzugriff

Benutzer sind berechtigt, Tabellendaten zu lesen, können jedoch keine Datensätze ändern, erstellen oder löschen. Die [!INCLUDE [prod_short](includes/prod_short.md)]-Plattform verhindert automatisch das Schreiben in Datentabellen.  

### <a name="use-of-objects"></a>Verwendung von Objekten

Zugriff mit Microsoft 365-Lizenzen schränken nicht ein, auf welche Business Central-Objekte oder -Objektbereiche zugegriffen werden kann. Benutzer sind berechtigt, auf die Microsoft-Basisanwendung und alle Erweiterungen wie Anpassungen und Add-On-Apps zuzugreifen.

## <a name="simplified-user-interface"></a>Vereinfachte Benutzeroberfläche

Benutzer haben Anspruch auf einen reduzierten Satz von Features und Funktionen, die von [!INCLUDE [prod_short](includes/prod_short.md)] in Microsoft Teams bereitgestellt werden. Die folgenden Tabellen zeigen bemerkenswerte Funktionen. Dies ist keine vollständige Liste und kann sich ändern.

Funktionen der [!INCLUDE [prod_short](includes/prod_short.md)]-App für Teams:

|Funktion  |Verfügbar|
|-|-|
|[!INCLUDE [prod_short](includes/prod_short.md)] Karten ansehen|![Ja](media/check.png)|
|Kartendetails anzeigen |![Ja](media/check.png) |
|Kartendetails als Registerkarte anheften |![Ja](media/check.png)|
|[!INCLUDE [prod_short](includes/prod_short.md)] Registerkarten anzeigen|![Ja](media/check.png)|
|Eine [!INCLUDE [prod_short](includes/prod_short.md)] Registerkarte hinzufügen|![Nein_](media/x-icon.png )|
|Nach Geschäftskontakten suchen |![Nein](media/x-icon.png )|
|Eine Linkvorschau als Karte einfügen und teilen|![Nein](media/x-icon.png )|

Funktionen des [!INCLUDE [prod_short](includes/prod_short.md)] Client, der in Teams eingebettet ist:

|Funktion |Verfügbar|Beispielfunktionen|
|-|-|-|
|Aktionen des Datenmanipulationssystems |![Nein](media/x-icon.png )|Bearbeiten, Erstellen, Löschen|
|Grundfunktionen in Listen|![Ja](media/check.png)|Suchen, sortieren, Layout ändern|
|Erweiterte Funktionen in Listen|![Nein](media/x-icon.png )|Bereich, Ansichten filtern|
|Drilldown von Liste zu Karte ausführen |![Ja](media/check.png)||
|Auf Daten aus verwandten Tabellen zugreifen|![Nein](media/x-icon.png )|Infobox-Bereich, Feld-Drilldown, Einsehen, Suche |
|Aktionen|![Nein](media/x-icon.png )|Aktionsleiste, Aktionsmenüs, Seitenbenachrichtigungsaktionen|
|Systemweite Verknüpfungen|![Nein](media/x-icon.png )|Meine Einstellungen, Rollen-Explorer, Tell-Me-Suche  |
|Kopie|![Ja](media/check.png)|Zeilen kopieren, Feldwert kopieren, Link zur Seite kopieren|
|Benutzeroberflächenanpassung|![Nein](media/x-icon.png )|Personalisieren| 
|Inline-Anpassung|![Ja](media/check.png)|Spaltengröße ändern, Erweitern/Reduzieren, Mehr anzeigen |
|Datenfreigabe |![Nein](media/x-icon.png )|In Excel öffnen oder bearbeiten, für Teams freigeben|
|Inline-Benutzerhilfe|![Ja](media/check.png) |Tooltips, Links zur Dokumentation|
|Erweiterte Benutzerunterstützung |![Nein](media/x-icon.png )|Seiten- und Feldunterrichtstipps, Hilfebereich|

## <a name="minimum-requirements"></a>Mindestanforderungen

In diesem Abschnitt werden die Mindestanforderungen beschrieben, die Ihre Organisation erfüllen muss, um den Zugriff mit Microsoft 365-Lizenzen zu ermöglichen, und für einzelne Microsoft Teams-Benutzer den Zugriff auf [!INCLUDE [prod_short](includes/prod_short.md)] Daten ohne eine [!INCLUDE [prod_short](includes/prod_short.md)] Lizenz.

### <a name="requirements-to-enable-access"></a>Anforderungen für den Zugriff

- [!INCLUDE [prod_short](includes/prod_short.md)] Online (SaaS).

- Umgebungen müssen die Plattformversion 21.1 oder höher aufweisen.

### <a name="requirements-for-individual-users-to-access-data-in-teams"></a>Anforderungen für einzelne Benutzer für den Zugriff auf Daten in Teams

- Der Zugriff auf die Daten muss über die [!INCLUDE [prod_short](includes/prod_short.md)] App für Teams erfolgen. Benutzer müssen die [!INCLUDE [prod_short](includes/prod_short.md)]-App für Teams installiert haben und einen der unterstützten Teams-Clients verwenden. Eine Liste der von [!INCLUDE [prod_short](includes/prod_short.md)] unterstützten Teams Clients finden Sie unter [Mindestanforderungen für die Verwendung von Business Central](product-requirements.md#teams).

- Benutzer müssen organisationsintern sein, was bedeutet, dass eine Benutzeridentität von demselben Home-Mandanten stammt, auf dem [!INCLUDE [prod_short](includes/prod_short.md)] bereitgestellt wird und auf dem der Zugriff aktiviert ist. Externe Identitäten werden nicht unterstützt. [!INCLUDE [prod_short](includes/prod_short.md)] verhindert automatisch den Zugriff für Gäste.

- Benutzern muss eine Microsoft 365-Lizenz aus einem der folgenden Pläne zugewiesen werden.
  
  |Unterstützter Plan|Produkt-ID |
  |-|-|
  |Microsoft 365 Business Basic|3b555118-da6a-4418-894f-7df1e2096870|
  |Microsoft 365 Business Standard|f245ecc8-75af-4f8e-b61f-27d8114de5f3|
  |Microsoft 365 Business Premium |cbdc14ab-d96c-4c30-b9f4-6ada7cdc1d46|
  |Microsoft 365 E3 |05e9a617-0261-4cee-bb44-138d3ef5d965 |
  |Microsoft 365 E5|06ebc4ee-1bb5-47dd-8120-11324bc54e06|
  |Microsoft 365 F1|50f60901-3181-4b75-8a2c-4c8e4c1d5a72|
  |Microsoft 365 F3|66b55226-6b4f-492c-910c-a3b7a3c9d993|
  |Office 365 E1|18181a46-0d4e-45cd-891e-60aabd171b4e|
  |Office 365 E2 |6634e0ce-1a9f-428c-a498-f84ec7b8aa2e|
  |Office 365 E3|6fd2c87f-b296-42f0-b197-1e91e994b900|
  |Office 365 E5|c7df2760-2c81-4ef7-b578-5b5392b571df|
  |Office 365 F2|131fd665-5752-4995-a628-bcba5c889745|
  |Office 365 F3|4b585984-651b-448a-9e53-3b10f069cf7f|
  |Microsoft Teams Essentials (Azure AD-Identität) |3ab6abff-666f-4424-bfb7-f0bc274ec7bc|
  
  Die meisten Angebote, die auf diesen Plänen basieren, werden ebenfalls unterstützt. Wenn Sie z.B. Microsoft 365 Business Premium (Nonprofit Staff Pricing) abonnieren, handelt es sich um ein spezielles Angebot für gemeinnützige Organisationen, das auf dem Plan Microsoft 365 Business Premium basiert und daher unterstützt wird.

  > [!NOTE]
  > Sie können Ihren Plan nicht in der Liste finden? Microsoft ist ständig auf der Suche nach Feedback dazu, wie wir unseren Service verbessern und unser Angebot erweitern können, damit mehr Kunden diese Funktion nutzen können. Teilen Sie uns Ihre Idee mit, welche Pläne wir als nächstes unterstützen sollten, unter [https://aka.ms/bcIdeas](https://aka.ms/bcIdeas).

- Benutzern muss eine Microsoft 365-Lizenz zugewiesen werden, die die Microsoft Teams-App in der Liste der Apps für diese Lizenz aktiviert hat.

  |Unterstützte Apps|Serviceplan-ID|
  |-|-|
  |Microsoft Teams|57ff2da0-773e-42df-b2af-ffb7a2317929 |

- Die Organisation muss mindestens einen anderen Benutzer haben, dem eine Dynamics 365 Business Central-Lizenz zugewiesen ist.

## <a name="next-steps"></a>Nächste Schritte

- Machen Sie sich mit dem Benutzerzugriffsflow vertraut, um Ihren Ansatz und Ihre Konfiguration von Business Central so zu planen, dass sie den Geschäftsanforderungen entsprechen. Siehe [Benutzerzugriffsflow](admin-access-with-m365-license-flow.md).
- Richten Sie Ihre Umgebung und Benutzer für den Zugriff mit Microsoft 365-Lizenzen ein. Siehe [Zugriff mit Microsoft 365-Lizenzen einrichten](admin-access-with-m365-license-setup.md).

## <a name="see-also"></a>Siehe auch

[Integration von Business Central und Microsoft Teams](across-teams-overview.md)  
