---
title: Den E-Belegekonnektor mit externen Endpunkten einrichten
description: 'In diesem Artikel wird erläutert, wie Sie die E-Beleg-Funktionalität einrichten, wenn diese mit externen Endpunkten verbunden ist.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, access-point, endpoint'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 12/13/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Den E-Belegekonnektor mit externen Endpunkten einrichten

In diesem Artikel wird erläutert, wie Sie die E-Beleg-Funktionalität einrichten, wenn diese mit externen Endpunkten verbunden ist.

Bevor Sie die in diesem Artikel beschriebene Funktionalität verwenden, installieren Sie die App **E-Belegekonnektor mit externen Endpunkten** oben in der globalen **E-Beleg-Kern**-App. Diese App kann für die Standardintegration mit externen (Drittanbieter-)Zugriffspunkten verwendet werden, um den E-Beleg-Flow zu automatisieren. Da diese App nur einige der ausgewählten Konnektoren darstellt, müssen Sie sich nicht auf die darin vorhandenen Integrationen beschränken. Die meisten Konnektoren werden in Zukunft auf AppSource verfügbar sein.

## Die Verbindung einrichten

Um mit der Einrichtung zu beginnen, gehen Sie in der [E-Beleg-Kern-App](finance-how-setup-edocuments.md) wie folgt vor. Wenn Sie damit fertig sind, kehren Sie zu diesem Artikel zurück und führen Sie die folgenden Schritte aus:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol aus. Geben Sie **E-Belegdienste** ein und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie im Feld **Dienstintegration** einen der Integrationscodes aus, die für die Endpunkt-Diensteinrichtung angeboten werden.
3. Wählen Sie **Einrichten der Dienstintegration** aus.
4. Wählen Sie auf der Seite **Einrichtung der externen Verbindung für einen E-Beleg** die Option **Autorisierungscode anfordern** aus. Sie werden zur Autorisierungsseite für externe Dienste weitergeleitet und zur Eingabe Ihrer Anmeldedaten aufgefordert.
5. Kopieren Sie den Autorisierungscode in das Feld **Autorisierungscode eingeben**.
6. Wählen Sie **Zugriffstoken aktualisieren**, um sicherzustellen, dass Sie das Token aktualisieren können.

    > [!NOTE]
    > Für diese Verbindung ist die Kommunikation mit externen Dienstleistern erforderlich, die unter Umständen zuzahlungspflichtig sind und eigene Verträge verlangen. Um alle erforderlichen Anmeldeinformationen zu erhalten, wenden Sie sich an die Dienstanbieter.

7. Füllen Sie auf der Seite **Einrichtung der externen Verbindung für einen E-Beleg** die folgenden Felder aus:

    | Name des Felds | Beschreibung |
    |---|---|
    | FileAPI-URL | Geben Sie die Datei-API-URL an. |
    | Fileparts-URL | Geben Sie die Fileparts-URL an. |
    | DocumentAPI-URL | Geben Sie die URL der Beleg-API an. |
    | Mandanten-ID | Geben Sie die Mandanten-ID an. |
    | Sendemodus | Geben Sie den Sendemodus an. Sie haben die Wahl zwischen **Produktion**, **Test** und **Zertifizierung**. |

    > [!NOTE]
    > Fragen Sie Ihren Dienstanbieter nach allen vorherigen Details, um eine Verbindung mit seinem Zugriffspunkt herzustellen.

## Unternehmensinformationen einrichten

Bevor Sie damit beginnen, E-Belege zu verwenden, aktualisieren Sie Ihre Seite **Unternehmensinformationen** wie folgt:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Unternehmensdaten** ein und wählen Sie dann den zugehörigen Link aus.
2. Neben den üblichen Feldern müssen Sie auch die folgenden Felder ausfüllen:

    | Name des Felds | Beschreibung |
    |---|---|
    | SWIFT-Code | Geben Sie den SWIFT-Code (internationaler Bankidentifizierungscode) Ihrer ersten Bank an. |
    | BLZ | Geben Sie die vierstellige Bankleitzahl ein. |
    | Mehrwertsteuererfassungsnummer | Geben die USt-IdNr. des Unternehmens an. |

3. Schließen Sie die Seite.

## Debitoren für den Empfang von E-Belegen einrichten

Damit Debitoren Ihre E-Belege empfangen können, gehen Sie wie folgt vor:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Debitoren** ein, und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die **Debitorenkarte**.
3. Füllen Sie die üblichen Felder aus und geben Sie zusätzlich im Feld **GLN** den Debitor im Zusammenhang mit dem Versand elektronischer Belege an.
4. Setzen Sie ein Häkchen das Feld **GLN in elektronischen Belegen verwenden**, um anzugeben, ob die Global Location Number (GLN) als Parteiidentifikationsnummer in elektronischen Belegen verwendet werden soll.
5. Schließen Sie die Seite.

## Weitere Einrichtung

Bevor Sie mit der Arbeit mit E-Belegen beginnen, richten Sie die E-Beleg-**Workflows** und die **Belegsendeprofile** ein, die Sie in Ihren Workflows verwenden wollen. Nachdem die Dienstverbindung hergestellt ist, können Sie mit der Nutzung Ihrer E-Belegslösung beginnen.

## Verfügbare Dienstanbieter

Microsoft möchte Zugriffspunktanbieter dazu ermutigen, ihre Konnektoren unserem **E-Beleg-Kern**-Rahmen hinzuzufügen.

Derzeit ist Pagero der einzige Zugriffspunktanbieter, der von diesem System abgedeckt wird. Microsoft hat keine vertragliche Verpflichtung gegenüber Pagero. Daher müssen Sie selbst einen Vertrag mit ihm abschließen, um alle erforderlichen Anmeldeinformationen zu erhalten.

Wir werden diese Liste aktualisieren, sobald neue Zugriffspunktanbieter für den E-Belegaustausch dazustoßen.

## Siehe auch

[E-Belege in Business Central einrichten](finance-how-setup-edocuments.md)  
[E-Belege in Business Central verwenden](finance-how-use-edocuments.md)  
[E-Belege in Business Central erweitern](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Finanzmanagement](finance.md)  
[Verkäufe fakturieren](sales-how-invoice-sales.md)  
[Käufe mit Einkaufsrechnungen und Aufträgen erfassen](purchasing-how-record-purchases.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
