---
title: Ein Shopify-Konto erstellen und festlegen
description: 'Erfahren Sie, wie Sie ein Shopify-Konto erhalten, damit Sie den Workflow für die Integration von Shopify und Business Central demonstrieren können.'
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102'
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
---

# Ein Shopify-Konto erstellen und festlegen

Wenn Sie überlegen, ob Sie Shopify als Ihre E-Commerce-Lösung verwenden sollen und ein Shopify-Konto benötigen, um den integrierten Workflow zu validieren, haben Sie folgende Möglichkeiten:

- Holen Sie sich eine Testversion. Dies ist der typische Ausgangspunkt für Endbenutzer.  
- Erstellen Sie Entwicklungs-Stores. Dieser Ansatz ist für Partner gedacht, die wiederkehrende Demos und Schulungen durchführen und Support anbieten.

## Testversion (Endbenutzer)

Rufen Sie die [Shopify-Website](https://www.shopify.com) auf und verwenden Sie Ihr E-Mail-Konto für das Administratorkonto, um sich für einen kostenlosen Test zu registrieren. Erfahren Sie im [Shopify Help Center](https://help.shopify.com/) mehr darüber, wie Sie Ihren Online Store erstellen und personalisieren können.

Im **Shopify Admin** des erstellten Shops wenden Sie die folgenden **Einstellungen** an:

- Deaktivieren Sie **Die Bestellung automatisch archivieren** im Abschnitt **Bestellverarbeitung** der [**Kasse**](https://www.shopify.com/admin/settings/checkout)-Einstellungen in Ihrem **Shopify Admin**.
- Aktivieren Sie die Option *Anmeldelink im Schaufenster und in der Kasse anzeigen* im Abschnitt **Kundenkontoeinstellungen** der Kasseneinstellungen.
- Erwägen Sie die Auswahl der Option *Firmenname - Optional* im Abschnitt **Kundeninformationen** der Kasseneinstellungen.
- Aktivieren Sie die Option **Trinkgeldoptionen an der Kasse anzeigen** im Abschnitt **Trinkgeld** der Kasseneinstellungen, wenn Sie planen, Trinkgeld zu demonstrieren.
- Aktivieren Sie Testzahlungen. Sie haben zwei Möglichkeiten. Beginnen Sie, indem Sie auf [**Zahlungen**](https://www.shopify.com/admin/settings/payments) Einstellungen gehen:  
  1. *(zum Testen) Bogus Gateway*. Weitere Informationen finden Sie unter [Aktivieren Sie Bogus Gateway für Tests](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* im Testmodus. Weitere Informationen finden Sie unter [Test von Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Wählen Sie in den Einstellungen [**Plan**](https://www.shopify.com/admin/settings/plan) einen Plan aus, um den Checkout-Prozess testen zu können.

> [!Important]  
> Um Zahlungen zu vermeiden, denken Sie daran, Ihren Shopify-Test zu kündigen.

## Entwicklung des Stores

Beginnen Sie damit, dem [Shopify Partnerprogramm](https://help.shopify.com/partners/about) beizutreten. Anschließend erstellen Sie über das **Partner Dashboard** den Entwicklungs-Store. Erfahren Sie mehr unter [Erstellen von Development Stores](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

Nachdem Sie den Store erstellt haben, wenden Sie im **Shopify Admin** des erstellten Shops die folgenden **Einstellungen** an:

- Deaktivieren Sie **Die Bestellung automatisch archivieren** im Abschnitt **Bestellverarbeitung** der [**Kasse**](https://www.shopify.com/admin/settings/checkout)-Einstellungen in Ihrem **Shopify Admin**.
- Aktivieren Sie die Option *Anmeldelink im Schaufenster und in der Kasse anzeigen* im Abschnitt **Kundenkontoeinstellungen** der Kasseneinstellungen.
- Erwägen Sie die Auswahl der Option *Firmenname - Optional* im Abschnitt **Kundeninformationen** der Kasseneinstellungen.
- Wenn Sie vorhaben, Trinkgeld zu zeigen, aktivieren Sie die Option **Tipp-Optionen an der Kasse anzeigen** im Abschnitt **Tipp** der Kasseneinstellungen.
- Aktivieren Sie Testzahlungen. Sie haben zwei Möglichkeiten. Beginnen Sie, indem Sie auf [**Zahlungen**](https://www.shopify.com/admin/settings/payments) Einstellungen navigieren:  
  1. *(zum Testen) Bogus Gateway*. Weitere Informationen finden Sie unter [Aktivieren Sie Bogus Gateway für Tests](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* im Testmodus. Erfahren Sie mehr unter [Testen von Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

> [!Note]  
> Entwicklungsshops sind normalerweise passwortgeschützt. Wenn Sie versuchen, eine bestimmte Seite in Ihrem Onlineshop von [!INCLUDE [prod_short](../includes/prod_short.md)] aus zu öffnen, zum Beispiel, um zu einem bestimmten Produkt oder Auftrag zu gelangen, müssen Sie Ihr Passwort eingeben. Um die Eingabe Ihres Passworts zu vermeiden, melden Sie sich während des Tests bei Ihrem Shopify Administrierenden an und öffnen Sie Ihrem Shop von dort aus. Sie müssen das Shop-Passwort erst eingeben, wenn Sie Ihren Browser schließen oder Ihre Sitzung abläuft.  

## Siehe auch

[Erste Schritte mit dem Shopify-Konnektor](get-started.md)  
[Beispielhafte Vorgehensweise: Einrichten und Verwenden des Shopify Konnektors](walkthrough-setting-up-and-using-shopify.md)
