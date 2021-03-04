---
title: Die Mehrwertsteuergruppenverwaltungserweiterung | Microsoft Docs
description: Sie können mit anderen Unternehmen zusammenarbeiten, um eine Mehrwertsteuergruppe zu bilden, und bei der Meldung der Mehrwertsteuer entweder als Mitglied oder als Vertreter der Gruppe fungieren.
author: bholtorf
manager: annbe
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: VAT, value added tax, report
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: ebe3c8748da04a2552f8f3d10967303459ba23c4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757042"
---
# <a name="the-vat-group-management-extension"></a>Die Mehrwertsteuergruppenverwaltungserweiterung

Sie können einem oder mehreren Unternehmen in Ihrem Land beitreten, um die Mehrwertsteuerberichterstattung unter einer einzigen Registrierungsnummer zu konsolidieren. Diese Art der Anordnung ist bekannt als *Mehrwertsteuergruppe*. Sie können mit der Gruppe als Mitglied oder als Gruppenvertreter zusammenarbeiten.

## <a name="forming-a-vat-group"></a>Bildung einer Mehrwertsteuergruppe
Mehrwertsteuergruppenmitglieder und der Gruppenvertreter können die Anleitung zur unterstützten Einrichtung für die **Mehrwertsteuergruppen-Verwaltungseinrichtung** verwenden, um ihre Zusammenarbeit mit der Gruppe zu definieren und eine Verbindung zwischen ihren [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten zu erstellen. Die Gruppenmitglieder verwenden die Verbindung, um ihre Mehrwertsteuererklärung an den Gruppenvertreter zu senden. Der Vertreter übermittelt die Mehrwertsteuer an die Steuerbehörden im Auftrag der Gruppe mithilfe einer einzigen Mehrwertsteuererklärung. 

## <a name="vat-group-constellations"></a>Mehrwertsteuergruppenkonstellationen
Die Kommunikation erfolgt von den Gruppenmitgliedern mit dem Vertreter. Der Gruppenvertreter stellt eine API zur Verfügung, mit der die Mitglieder ihre Mehrwertsteuererklärungen an den Mehrwertsteuergruppen-Vertreter übermitteln können. 
[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt die Übermittlung von Mehrwertsteuererklärungen innerhalb der Gruppe bei Unternehmen, die [!INCLUDE[prod_short](includes/prod_short.md)] lokal oder online verwenden oder irgendeine Kombination davon. Die Einrichtung der Kommunikation hängt von der Konstellation ab. In den folgenden Abschnitten wird beschrieben, wie Sie verschiedene Gruppenkonstellationen einrichten.

Die folgende Liste zeigt die empfohlene Reihenfolge der Schritte zum Einrichten einer Mehrwertsteuergruppe:

1. Erstellen Sie die Einrichtung in Azure Active Directory. Weitere Informationen finden Sie unter [Anforderungen für die Authentifizierung](ui-extensions-vat-group.md#requirements-for-authentication).
2. Teilen Sie die technischen Informationen, die Mehrwertsteuergruppen-Mitglieder und die Vertreter benötigen, um ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten zu verbinden. Normalerweise verfügt der Vertreter der Mehrwertsteuergruppe über diese Informationen, wie z. B. den Namen der Umgebung des Mehrwertsteuergruppenvertreters, an den die Mitglieder der Mehrwertsteuergruppe die Mehrwertsteuer übermitteln.
3. Erstellen Sie Benutzer im [!INCLUDE[prod_short](includes/prod_short.md)] des Mehrwertsteuergruppen-Vertreters, die Mehrwertsteuergruppen-Mitglieder verwenden können, um sich zu authentifizieren und eine Verbindung herzustellen.
4. Führen Sie die Anleitung zur unterstützten Einrichtung **Mehrwertsteuergruppenverwaltung einrichten** aus, um die Mitglieder der Mehrwertsteuergruppe zu verbinden.

  Für die Anleitung sind einige Informationen vom Vertreter der Mehrwertsteuergruppe erforderlich. Weitere Informationen finden Sie im Abschnitt [Einrichtung eines Mehrwertsteuergruppen-Mitglieds](#vat-group-member-setup). Notieren Sie sich die **Gruppenmitglieds-ID** für jedes Mitglied der Mehrwertsteuergruppe. Der Vertreter benötigt diese IDs, um die Unternehmen der Mehrwertsteuergruppe hinzuzufügen.
5. Richten Sie die Erweiterung „Mehrwertsteuergruppenverwaltung“ im [!INCLUDE[prod_short](includes/prod_short.md)] des Mehrwertsteuergruppen-Vertreters ein, indem Sie die Anleitung zur unterstützten Einrichtung **Mehrwertsteuergruppenverwaltung einrichten** verwenden. 

> [!NOTE]
> Um eine Verbindung zum Vertreter der Mehrwertsteuergruppe herzustellen, benötigen Gruppenmitglieder einen Benutzer mit Zugriff auf das [!INCLUDE[prod_short](includes/prod_short.md)] des Mehrwertsteuergruppenvertreters. Der Vertreter der Mehrwertsteuergruppe muss hierfür mindestens einen Benutzer erstellen. Aus Sicherheitsgründen empfehlen wir jedoch, für jedes Mitglied der Mehrwertsteuergruppe einen Benutzer zu erstellen. Stellen Sie sicher, dass Sie die Anmeldeinformationen für diese Benutzer auf sichere Weise an Mehrwertsteuergruppenmitglieder verteilen.

## <a name="understanding-the-vat-group-management-setup"></a>Grundlegendes zum Einrichten der Mehrwertsteuergruppenverwaltung

Der Vertreter der Mehrwertsteuergruppe stellt eine API bereit, mit der Mitglieder der Mehrwertsteuergruppe eine zu ihrem [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten herstellen können und Mehrwertsteuererklärungen übermitteln können. Mehrwertsteuergruppenmitglieder werden [!INCLUDE[prod_short](includes/prod_short.md)] häufig in separaten Azure Active Directory-Mandanten verwenden. Daher sind weitere Einrichtungsvorgänge erforderlich, um eine Verbindung zwischen dem Mehrwertsteuergruppenmitglied und dem [!INCLUDE[prod_short](includes/prod_short.md)] des Vertreters herzustellen. 
  
Mitglieder der Mehrwertsteuergruppe stellen eine Verbindung zum Vertreter her, indem sie einen Webdienst im Mandanten des Mehrwertsteuergruppen-Vertreters aufrufen. Der Aufrufer muss mithilfe von OAuth authentifiziert sein. Wenn die Erweiterung „Mehrwertsteuergruppenverwaltung“ eingerichtet ist, werden Sie aufgefordert, sich beim Vertreter der Mehrwertsteuergruppe zu authentifizieren, um einen Zugriffstoken abzurufen und zu speichern. Dieses Zugriffstoken wird verwendet, wenn Mehrwertsteuererklärungen an den Vertreter der Mehrwertsteuergruppe gesendet werden. 

Die Authentifizierung wird von Azure Active Directory abgewickelt. Daher muss Ihre Einrichtung im Azure Active Directory des Mehrwertsteuergruppen-Vertreters erfolgen, um Verbindungen zuzulassen. Eine Azure Active Directory-App-Registrierung muss mit Zugriff auf das [!INCLUDE[prod_short](includes/prod_short.md)] des Mehrwertsteuergruppenvertreters konfiguriert werden. Dies gilt auch, wenn der Vertreter der Mehrwertsteuergruppe [!INCLUDE[prod_short](includes/prod_short.md)] lokal verwendet. Darüber hinaus müssen Sie „Einmaliges Anmelden“ konfigurieren, wenn der Vertreter der Mehrwertsteuergruppe [!INCLUDE[prod_short](includes/prod_short.md)] lokal verwendet.

> [!NOTE]
> Für eine begrenzte Zeit wird auch die Authentifizierung mithilfe eines Webdienst-Zugriffsschlüssels unterstützt. Weitere Informationen finden Sie unter [Veraltete Funktionen in 2021 Veröffentlichungzyklus 1](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#deprecated-features-in-2021-release-wave-1).

## <a name="requirements-for-authentication"></a>Voraussetzungen für die Authentifizierung 
Wenn der Vertreter der Mehrwertsteuergruppe [!INCLUDE[prod_short](includes/prod_short.md)] online oder lokal verwendet, verwenden Mehrwertsteuergruppenmitglieder Azure Active Directory, um sich zu authentifizieren, wenn sie Mehrwertsteuererklärungen an den Vertreter der Mehrwertsteuergruppe übermitteln. Wenn die Mehrwertsteuergruppenmitglieder ebenfalls [!INCLUDE[prod_short](includes/prod_short.md)] online verwenden, kann sich das Mehrwertsteuergruppenmitglied mithilfe der angegebenen Benutzeranmeldeinformationen und der Endpunktinformationen authentifizieren. Weitere Informationen finden Sie unter [Mehrwertsteuergruppenmitglied-Einrichtung](ui-extensions-vat-group.md#vat-group-member-setup).

Mehrwertsteuergruppenmitglieder, die [!INCLUDE[prod_short](includes/prod_short.md)] lokal haben, müssen eine App-Registrierung in Azure Active Directory für den [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten des Vertreters der Mehrwertsteuergruppe einrichten. Die App-Registrierung ermöglicht es, dass mit [!INCLUDE[prod_short](includes/prod_short.md)] online des Mehrwertsteuergruppenvertreters das Gruppenmitglied authentifiziert werden kann. Weitere Informationen finden Sie unter [Schnellstart: Registrieren einer Anwendung mit der Microsoft-Identitätsplattform](/azure/active-directory/develop/quickstart-register-app).

Wenn Sie die App-Registrierung in Azure Active Directory erstellen, müssen Sie Folgendes angeben.

* Im Abschnitt **Authentifizierung** fügen Sie **Web** als Plattform hinzu und verwenden die folgende **Umleitungs-URL**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* Im Abschnitt **Authentifizierung** in der Option zur Auswahl **Unterstützte Kontoarten** wählen Sie **Konten in einem beliebigen Organisationsverzeichnis (Beliebiges Azure AD-Verzeichnis – mandantenfähig)**.
* Im Abschnitt **Zertifikate und Geheimschlüssel** erstellen Sie einen neuen geheimen Clientschlüssel und notieren den Wert. Die Mehrwertsteuergruppenmitglieder benötigen den Geheimschlüssel, wenn Sie die Verbindung zum Gruppenvertreter einrichten.
* Im Abschnitt **API-Berechtigungen** fügen Sie Berechtigungen zu [!INCLUDE[prod_short](includes/prod_short.md)] hinzu. Aktivieren Sie den stellvertretenden Zugriff auf **Financials.ReadWrite.All** und **user_impersonation**.
* Im Abschnitt **Übersicht** notieren Sie die **Anwendungs-(Client)-ID**. Die Mehrwertsteuergruppenmitglieder benötigen die ID, wenn Sie die Verbindung zum Gruppenvertreter einrichten. 

## <a name="vat-group-member-setup"></a>Einrichtung des Mehrwertsteuergruppenmitglieds
Richten Sie das Mehrwertsteuergruppenmitglied ein, indem Sie die Anleitung zur unterstützten Einrichtung **Mehrwertsteuergruppenverwaltung einrichten** starten. 

> [!NOTE]
> Bevor Sie beginnen, wenden Sie sich an den Vertreter der Mehrwertsteuergruppe für die folgenden Informationen über seinen [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten:
>
> * Die API-URL
> * Der Name seines Unternehmens 
> * Client-ID
> * Geheimer Clientschlüssel
> * Anmeldeinformationen für den dedizierten Benutzer 

1. Um die Mehrwertsteuer-Gruppenrolle des Unternehmens zu definieren, wählen Sie **Mitglied** und dann **Weiter** aus.
2. Kopieren Sie den Wert des Felds **Gruppenmitglieds-ID**, und telen Sie ihn dann mit dem Vertreter der Mehrwertsteuergruppe, damit dieser Ihr Unternehmen als genehmigtes Mitglied der Gruppe hinzufügen kann.
3. Fügen Sie die **API-URL** vom Vertreter der Mehrwertsteuergruppe hinzu. Normalerweise ist die URL wie folgt formatiert: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Zum Beispiel, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`. 
4. Fügen Sie den [!INCLUDE[prod_short](includes/prod_short.md)]-Unternehmensnamen des Vertreters der Mehrwertsteuergruppe hinzu, wie z. B. *CRONUS UK Ltd.*.
5. Wählen Sie **Authentifizierungsart**, wählen Sie **OAuth2** und wählen Sie dann **Weiter**.
6. Im Feld **Client-ID** geben Sie die vom Vertreter der Mehrwertsteuergruppe angegebene ID ein.
7. Im Feld **Vom Vertreter der Mehrwertsteuergruppe bereitgestellter geheimer Clientschlüssel** geben Sie den vom Vertreter der Mehrwertsteuergruppe bereitgestellten Geheimschlüssel an.
8. Im Feld **OAuth 2.0-Autoritätsendpunkt** geben Sie *https://login.microsoftonline.com/common/oauth2* ein.
9. Im Feld **OAuth 2.0-Ressourcen-URL** geben Sie *https://api.businesscentral.dynamics.com/* ein.
10. Im Feld **OAuth 2.0-Umleitungs-URL** geben Sie *https://businesscentral.dynamics.com/OAuthLanding.htm* ein. 
11. Wenn Sie die verschiedenen Felder angegeben haben, wählen Sie **Weiter** und geben Sie dann die Benutzeranmeldeinformationen ein, die vom Vertreter der Mehrwertsteuergruppe bereitgestellt wurden.
12. Wählen Sie die MwSt.-Berichtskonfiguration aus, die Sie verwenden, um die Mehrwertsteuer den Behörden in Ihrem Land zu melden.

  Im Vereinigten Königreich würde beispielsweise die Konfiguration des Mehrwertsteuerberichts so eingerichtet, dass die Mehrwertsteuer an die HMRC gemeldet wird. Die Erweiterung „Mehrwertsteuergruppenverwaltung“ kopiert diese Einrichtung, aber ersetzt die Übermittlungs-codeunit durch‌ eine solche, die die Übermittlung an den Vertreter der Mehrwertsteuergruppe anstelle an die Steuerbehörden unterstützt. Die codeunit wird von Microsoft bereitgestellt. Wenn Sie fertig sind, wählen Sie **Weiter**.

## <a name="using-the-vat-group-management-features"></a>Verwenden der Funktionen der Mehrwertsteuergruppenverwaltung

Mehrwertsteuergruppenmitglieder verwenden die Standardprozesse, um Mehrwertsteuererklärungen zu erstellen. Der einzige Unterschied ist die Auswahl der Berichtsversion **MEHRWERTSTEUERGRUPPE**, wodurch die Mehrwertsteuererklärung an den Vertreter der Mehrwertsteuergruppe und nicht an die Behörden übermittelt wird. Weitere Informationen finden sie unter [Informationen zum Mehrwertsteuererrückerstattungsbericht](finance-how-report-vat.md#about-the-vat-return-report).

In den folgenden Abschnitten werden die Aufgaben beschrieben, die Vertreter von Mehrwertsteuergruppen ausführen müssen.

### <a name="vat-group-submissions"></a>Übermittlungen der MwSt.-Gruppe

Auf der Seite **Übermittlungen der Mehrwertsteuergruppe** werden die von Mitgliedern übermittelten Mehrwertsteuererklärungen aufgelistet. Die Seite dient als Entwurfsspeicherort für die Übermittlungen, bis der Vertreter der Mehrwertsteuergruppe sie in eine Mehrwertsteuererklärung für die Gruppe einbezieht. Sie können die Übermittlungen öffnen, um die Mehrwertsteuer für die einzelnen vom Mehrwertsteuergruppenmitglied gemeldeten Felder zu überprüfen.

### <a name="creating-a-group-vat-return"></a>Erstellen einer Gruppenmehrwertsteuererklärung

Um die Mehrwertsteuer im Auftrag der Gruppe zu melden, erstellen Sie auf der Seite **Mehrwertsteuererklärungen** eine Mehrwertsteuererklärung nur für Ihr Unternehmen. Fügen Sie anschließend die neuesten Mehrwertsteuerübermittlungen von Mehrwertsteuergruppenmitgliedern ein, indem Sie die Aktion **Gruppenmehrwertsteuer einschließen** wählen.  

Wenn die Mehrwertsteuererklärung des Vertreters der Mehrwertsteuergruppe den Behörden im Auftrag der gesamten Gruppe übermittelt wurde, führen Sie normalerweise die Aktion **MwSt.-Abrechnung berechnen und buchen** aus. Die Aktion schließt offene MwSt.-Posten und überträgt Beträge zum MwSt.-Abrechnungskonto. Derzeit werden bei dieser Aktion die Gruppenübermittlungen nicht berücksichtigt. Dies bedeutet, dass nur die MwSt.-Posten des Unternehmens des Vertreters der Mehrwertsteuergruppe gebucht werden. Die Übermittlungsbeträge der Mehrwertsteuergruppenmitglieder müssen manuell zum MwSt.-Abrechnungsetrag hinzugebucht werden, damit das MwSt.-Abrechnungskonto des Vertreters der Mehrwertsteuergruppe die Verbindlichkeit dessen, was an die Behörden gemeldet wurde, widerspiegelt. Dieses Verhalten wird sich in einem bevorstehenden Update von [!INCLUDE[prod_short](includes/prod_short.md)] ändern, sodass die gesamte Gruppenmehrwertsteuer (der Totalbetrag der Berichtszeilen in der Mehrwertsteuererklärung) ausgeglichen wird. 

> [!NOTE]
> Mitglieder der Mehrwertsteuergruppe können übermittelte Mehrwertsteuererklärungen korrigieren, solange der Gruppenvertreter die Mehrwertsteuererklärung für die Gruppe noch nicht herausgegeben hat. Um eine Korrektur vorzunehmen, muss das Mitglied der Mehrwertsteuergruppe eine neue Mehrwertsteuererklärung für den Zeitraum der Mehrwertsteuererklärung erstellen und diese dem Vertreter der Mehrwertsteuergruppe übermitteln. Auf der Seite des Vertreters der Mehrwertsteuergruppe wird die aktuellste Mehrwertsteuererklärung auf der Seite **Mehrwertsteuererklärungen** eingefügt. 

## <a name="see-also"></a>Siehe auch
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Mehrwertsteuer einrichten](finance-setup-vat.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]