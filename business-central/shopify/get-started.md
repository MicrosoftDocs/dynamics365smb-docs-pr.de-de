---
title: Erste Schritte mit Konnektor für Shopify
description: Erste Schritte beim Konfigurieren der Verbindung zwischen Business Central und Shopify
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: brentholtorf
ms.author: bholtorf
---

# Erste Schritte mit dem Shopify-Konnektor

Verbinden Sie Ihre(n) Shopify Store(s) mit [!INCLUDE [prod_short](../includes/prod_short.md)], um maximieren Sie die Produktivität Ihres Unternehmens. Sie können Erkenntnisse aus Ihrem Unternehmen und Ihrem Shopify Store als eine Einheit verwalten und anzeigen.

Um Shopify mit [!INCLUDE [prod_short](../includes/prod_short.md)] zu verwenden, müssen Sie zunächst einige Dinge erledigen. Dieser Artikel dient als Anleitung für die Integration Ihres Shopify-Shops mit [!INCLUDE [prod_short](../includes/prod_short.md)].

## Voraussetzungen für Shopify

Sie benötigen Folgendes:

- Ein Shopify-Konto
- Ein Shopify-Online-Store

Erfahren Sie mehr, wie Sie Shopify-Tests erstellen, und über die empfohlenen Einstellungen unter [Erstellen und Einrichten eines Shopify-Kontos](shopify-account.md).

## Voraussetzungen für Business Central

- Stellen Sie sicher, dass die **[Shopify Connector](https://go.microsoft.com/fwlink/?linkid=2196238)**-App installiert ist.

  Die App ist für alle Neuanmeldungen und Testversionen vorinstalliert. Erfahren Sie mehr über die Installation von Apps aus AppSource unter [Installieren und Deinstallieren von Erweiterungen](../ui-extensions-install-uninstall.md#install). Führen Sie die unten aufgeführten Schritte aus, wenn Sie nicht über [!INCLUDE[prod_short](../includes/prod_short.md)] verfügen.

- Stellen Sie sicher, dass der Benutzer über die Berechtigungen verfügt. Der Konnektor Shopify wird durch die auf **Shopify - Admin (SHPFY - ADMIN)** festgelegte Berechtigung abgedeckt. Weitere Informationen finden Sie unter [Benutzer entsprechend den Lizenzen erstellen](../ui-how-users-permissions.md) und [Benutzern und Gruppen Berechtigungen zuweisen](../ui-define-granular-permissions.md).

## Installieren Sie die Dynamics 365 Business Central App in Ihrem Shopify Online Store

Für die bestehende Instanz [!INCLUDE[prod_short](../includes/prod_short.md)] ist dieser Schritt optional und kann übersprungen werden.

1. Suchen Sie die [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central)-App im [Shopify Appstore](https://apps.shopify.com/)
2. Wählen Sie die Schaltfläche **App hinzufügen** aus. Melden Sie sich bei Ihrem Shopify-Konto an, wenn Sie dazu aufgefordert werden. Wählen Sie den gewünschten Onlineshop aus, falls Sie über mehrere verfügen.
3. Nachdem Sie den Datenschutz und die Berechtigungen überprüft haben, wählen Sie die Schaltfläche **App installieren** aus.

   Sie können die installierte **Dynamics 365 Business Central** App im Bereich **Apps** in der Seitenleiste der **Shopify Admin** Seite finden und öffnen.
4. Wählen Sie **Jetzt anmelden**, um den Test von [!INCLUDE[prod_short](../includes/prod_short.md)] zu starten oder **Anmelden**, wenn Sie bereits [!INCLUDE[prod_short](../includes/prod_short.md)] haben. Sie werden zu Ihrer [Business Central](https://businesscentral.dynamics.com) Seite weitergeleitet.
5. Führen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] die nächsten Schritte aus.

## Verbinden Sie Business Central mit dem Shopify-Online-Store

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") , geben Sie **Shopify-Shop** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie die Aktion **Neu**.  
3. Geben Sie in das Feld **Code** einen Code ein, der das Auffinden in [!INCLUDE[prod_short](../includes/prod_short.md)] erleichtert. Der Name könnte zum Beispiel widerspiegeln, was ein Geschäft verkauft, wie Möbel oder Kaffee oder das Land oder die Region, in der es tätig ist.
4. Geben Sie in das Feld **Shopify URL** die URL des Online-Shops ein, mit dem Sie sich verbinden möchten. Verwenden Sie das folgende Format: `https://{shop}.myshopify.com/`.
5. Aktivieren Sie den Schalter **Aktiviert**, lesen und akzeptieren Sie die dann die Bestimmungen.
6. Melden Sie sich bei Ihrem Shopify-Konto an, falls Sie dazu aufgefordert werden. Nachdem Sie den Datenschutz und die Berechtigungen überprüft haben, wählen Sie die Schaltfläche **App installieren**.

Wiederholen Sie die Schritte 2–6 für alle Onlineshops, die Sie verbinden möchten.

### Bekannte Probleme

- Der Browser blockiert das Popup-Fenster. Wenn Sie den Schalter **Aktiviert** aktivieren, öffnet [!INCLUDE [prod_short](../includes/prod_short.md)] die Seite **Warte auf Antwort - diese Seite nicht schließen**, die auf einen Zugriffstoken von Shopify wartet. Wenn diese Seite geschlossen oder blockiert ist, können Sie keine Verbindung zu Shopify herstellen. Erfahren Sie mehr unter [Anforderung des Zugriffstokens](troubleshoot.md#request-the-access-token)
- Es könnte eine gute Idee sein, die Shopify-Verwaltung im selben Browser wie [!INCLUDE [prod_short](../includes/prod_short.md)] zu öffnen
- [Fehler: Oauth Fehler invalid_request: Konnte Shopify API-Anwendung mit api_key nicht finden](troubleshoot.md#error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Fehler: Oauth error invalid_request: Ihr Konto verfügt nicht über die Berechtigung, den angeforderten Zugriff für diese App zu gewähren.](troubleshoot.md#error-oauth-error-invalid_request-your-account-does-not-have-permission-to-grant-the-requested-access-for-this-app)
- [Kann keine Verbindung von der Sandbox aus herstellen](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment)

## Nächste Schritte

Jetzt ist Ihr Onlineshop mit [!INCLUDE[prod_short](../includes/prod_short.md)] verbunden. In den nächsten Schritten definieren Sie, wie und was synchronisiert werden soll.

- [Artikel synchronisieren](synchronize-items.md)
- [Debitoren synchronisieren](synchronize-customers.md)
- [Bestellungen synchronisieren](synchronize-orders.md)

## Teststrategien

Es gibt verschiedene Ansätze zum Testen einer Integration, und jeder Ansatz hat seine Vor- und Nachteile.

Sie können [!INCLUDE[prod_short](../includes/prod_short.md)] und Shopify Konten so oft verbinden, wie Sie möchten. Der Shopify Connector wirkt sich nur auf die Umgebung aus, genauer gesagt auf das Unternehmen, in dem er aktiviert ist. Sie können sich von mehreren Umgebungen oder Unternehmen aus mit demselben Shopify Online-Shop verbinden. Sie können den Connector deaktivieren und erneut aktivieren.

Es ist einfach, Synchronisationstests erneut auszuführen. Mit dem Konnektor können Sie importierte Daten wie Produkte, Kunden und Bestellungen löschen und anschließend erneut importieren. Einfach [Synchronisierung zurücksetzen](troubleshoot.md#reset-sync).

### Shopify Sandbox und Business Central-Sandbox

Dies ist wahrscheinlich der sicherste Weg, um die Integration zu testen. Anstatt eine Shopify Sandbox zu verwenden, können Sie auch ein Testabonnement oder einen Development Store verwenden. In [!INCLUDE[prod_short](../includes/prod_short.md)] können Sie auch ein Testunternehmen in einer Produktionsumgebung verwenden.

Um mehr über [!INCLUDE[prod_short](../includes/prod_short.md)] Sandboxes zu erfahren, gehen Sie zu [Neue Umgebung erstellen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

### Shopify Sandbox und Business Central-Produktion

Dies ist *keine* empfohlene Konfiguration zum Testen, da der Shopify Connector Artikel und Kunden erstellen oder ändern kann. Es kann auch Verkaufsdokumente wie Bestellungen und Rechnungen erstellen. Es kann schwierig sein, diese Dokumente rückgängig zu machen.
 
Wenn Sie diese Konfiguration verwenden müssen, empfehlen wir Ihnen, die folgenden Einstellungen zu überprüfen und möglicherweise zu deaktivieren:

* **Unbekanntes Element automatisch erstellen**, um keine Elemente zu erstellen
* **Shopify kann Elemente aktualisieren**, um zugeordnete Elemente nicht zu aktualisieren
* **Unbekannten Kunden automatisch erstellen**, um keine Kunden und Kontakte zu erstellen
* **Shopify kann Kunden aktualisieren**, um bestehende Kunden nicht zu aktualisieren
* **Verkaufsauftrag automatisch erstellen**, um keine Verkaufsaufträge und Ausgangsrechnungen zu erstellen

Weitere Informationen finden Sie unter [Wiederherstellen einer Umgebung](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).

### Shopify Produktion und Business Central-Sandbox

Es ist vielleicht eine gute Idee, Ihre Daten zu sichern. Exportieren Sie beispielsweise Ihre Produkte und Kunden. Weitere Informationen finden Sie unter [CSV-Dateien zum Sichern von Shopinformationen verwenden](https://help.shopify.com/en/manual/shopify-admin/duplicate-store#using-csv-files-to-back-up-store-information).

Deaktivieren Sie den Schalter **Datensynchronisierung zulassen auf Shopify**, sodass [!INCLUDE[prod_short](../includes/prod_short.md)] nicht auf Shopify schreibt. In diesem Fall können Sie Produkte, Bilder, Kunden und Bestellungen aus Shopify importieren. Sie können jedoch keine Artikel, Preise, Lagerbestände, Kunden und Erfüllungsinformationen an Shopify senden.

Wenn Sie die Umschaltfläche **Datensynchronisierung zulassen Shopify** aktiviert lassen, gelten folgende zusätzliche Schutzmaßnahmen:

*   Wählen Sie **Entwurf** im Feld **Status für Produkt erstellen** aus, um sicherzustellen, dass exportierte Produkte nicht für Käufer verfügbar sind. Sie können überprüfen, wie Produkte im Online-Shop aussehen, Preise, Optionen und Lagerbestände synchronisieren. Stellen Sie einfach sicher, dass Sie auf der Seite **Element hinzufügen zu Shopify** Filter verwenden, um die Anzahl der exportierten Elemente zu begrenzen.
* Deaktivieren Sie den Schalter **Kunden exportieren nach Shopify** , damit Sie keine Kunden zu Shopify senden.

## Siehe auch

[Beispielhafte Vorgehensweise: Einrichten und Verwenden des Shopify Konnektors](walkthrough-setting-up-and-using-shopify.md)  

