---
title: Verwenden der AMC Banking 365 Fundamentals-Erweiterung
description: 'Erfahren Sie, wie Sie auf einfache Weise Daten mit Ihren Banken austauschen können, indem Sie die Daten in das von ihnen benötigte Format umwandeln.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bank, format, data'
ms.search.form: '20100, 20101, 20102, 20105, 20106, 20107, 20109,'
ms.date: 09/20/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="use-the-amc-banking-365-fundamentals-extension"></a>Die AMC Banking 365 Fundamentals-Erweiterung verwenden

Die AMC Banking 365 Fundamentals-Erweiterung macht es einfacher und genauer, Daten an Ihre Banken zu senden. Die Erweiterung verbindet [!INCLUDE[prod_short](includes/prod_short.md)] mit dem AMC Banking 365 Fundamentals for Microsoft Dynamics 365 Business Central-Dienst, der Bankdaten von [!INCLUDE[prod_short](includes/prod_short.md)] in Formate konvertieren kann, die von über 600 Banken weltweit benötigt werden. Dies erleichtert z.B. die Übertragung von Zahlungen und Gutschriften an Lieferanten, indem Sie die Zahlungen auf [!INCLUDE[prod_short](includes/prod_short.md)] eingeben und dann auf Ihre Bank hochladen. Die Formate können auch die Prozesse der Bankabstimmung glätten. Weitere Informationen finden Sie unter [AMC Banking für Microsoft Dynamics 365 Business Central](https://www.amcbanking.com/bc-fundamentals/).

> [!NOTE]
> AMC Banking hat zusätzliche Erweiterungen gebaut, die mit [!INCLUDE[prod_short](includes/prod_short.md)] funktionieren. Dieses Thema beschreibt nur die grundlegende Erweiterung.

> [!NOTE]
> In der generischen Version von [!INCLUDE[prod_short](includes/prod_short.md)]  wird ein globaler Diensteanbieter eingerichtet und verbunden, der Bankdaten in das Dateiformat konvertiert, das Ihre Bank verlangt. In den nordamerikanischen Versionen kann derselbe Dienst verwendet werden, um Zahlungsdateien als Electronic Funds Transfer (EFT) zu senden, z.B. über das allgemein verwendete Automated Clearing House (ACH) Netzwerk, allerdings mit einem etwas anderen Verfahren.

## <a name="use-our-demonstration-account"></a>Unser Demonstrationskonto verwenden

[!INCLUDE[prod_short](includes/prod_short.md)] wird mit einem Demokonto geliefert, mit dem Sie die AMC Banking 365 Fundamentals-Erweiterung ausprobieren können. Wir bieten Standardeinstellungen für die Verbindung mit AMC Banking, die Angabe der Bankkonten, von denen die Daten in [!INCLUDE[prod_short](includes/prod_short.md)] bezogen werden sollen, sowie einige Datenaustauschdefinitionen. Sie können die Verbindungseinstellungen auf der Seite **AMC Banking Setup** einsehen. Für Bankkonten bezieht die Erweiterung Werte in den Feldern **Bankname**, **Überweisung Msg. Nr.**, **Kontoauszug Importformat** und **Zahlungsexportformat** Felder auf Bankkontokarten.

Wir stellen die Einstellungen zur Verfügung, aber um die Erweiterung auszuprobieren, müssen Sie die unterstützte Installationsanleitung ausführen, um sie anzuwenden. Um die Anleitung auszuführen, wählen Sie auf der Seite **AMC Banking Setup** die Aktion **Unterstütztes Setup**.

> [!NOTE]
> Es gibt einige Einschränkungen für das Demo-Konto. Wenn Sie beispielsweise Zahlungen konvertieren, stimmt der Betrag in der konvertierten Datei nicht mit dem tatsächlichen Betrag überein. Stattdessen beträgt der Betrag immer fünf Einheiten der Währung, die Sie für Zahlungen verwenden.  

## <a name="setting-up-the-extension"></a>Einrichten der Erweiterung

Der Einstieg in die Erweiterung ist mit wenigen Handgriffen erledigt, und eine unterstützte Installationsanleitung stellt die Verbindung her und schaltet die Erweiterung ein. Der Leitfaden wird Dinge wie die Installation der Datenaustauschdefinitionen für Kontoauszugsexport und -import-Setups durchführen und die Nummernserie für Überweisungsnachrichten initiieren.  

### <a name="to-set-up-the-required-permission-sets"></a>So richten Sie die erforderlichen Berechtigungsgruppen ein

Bevor Personen diese Erweiterung verwenden können, muss Ihr Administrator die folgenden Berechtigungen kopieren, bearbeiten und die neuen Berechtigungen dann den Benutzern statt dem Original zuweisen:

* **D365 Basic**
* **D365 Team Member**
* **D365 Read**
* **Intelligente CloudBC**

Weitere Informationen finden Sie unter [Kopieren eines Berechtigungssatzes](ui-define-granular-permissions.md#copy-a-permission-set).

Erteilen Sie für jeden neuen Berechtigungssatz nur die Berechtigung **Lesen** für die **AMC Banking Setup-Tabelle (20101)**. Weitere Informationen finden Sie unter [Berechtigungen manuell erstellen oder ändern](ui-define-granular-permissions.md#create-a-permission-set).

### <a name="to-connect-the-extension-to-amc-banking"></a>So verbinden Sie die Erweiterung mit AMC Banking.

1. Besorgen Sie sich ein Modul und einen Serviceplan für AMC Banking. Um dies zu tun, besuchen Sie die Seite [AMC Lizenz](https://license.amcbanking.com/register).
2. Wählen Sie in [!INCLUDE[prod_short](includes/prod_short.md)] die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **AMC Banking Einrichtung** ein und wählen Sie dann das zugehörige Link.  
3. Wählen Sie auf der Seite **AMC Banking Setup** die Aktion **Unterstütztes Setup**.
4. Schliessen Sie die Schritte im unterstützten Setup ab.

### <a name="to-connect-bank-accounts-to-the-extension"></a>So verbinden Sie Bankkonten mit der Erweiterung

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Bankkonten** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Karte für das Bankkonto, das Sie mit dem Dienst verbinden möchten.
3. Wählen Sie im Feld **Bankname** das Format, das Ihre Bank benötigt.  

   Die Formate sind so gefiltert, dass nur diejenigen angezeigt werden, die für das Land/die Region relevant sind, die für das Bankkonto angegeben ist.
4. Wählen Sie im Feld **Überweisung Msg. Nr.** die Nummernserie aus, die für Nachrichten, die Zahlungen begleiten, verwendet werden soll.
5. Wählen Sie in den Feldern **Kontoauszugsimportformat** und **Zahlungsexportformat** die Datenaustauschdefinitionen, die Ihre Bank benötigt.

## <a name="use-the-extension"></a>Die Erweiterung verwenden

Die Verwendung dieser Erweiterung ist nur eine Frage des Exports von Daten auf der Seite **Zahlungsjournale** und des Hochladens auf den Webservice Ihrer Bank. Weitere Informationen finden Sie unter [Zahlungen mit Bankdatenumstellung oder SEPA-Überweisung](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).

> [!NOTE]
> Sie müssen die Felder **SWIFT Code** und **IBAN** für jedes Bankkonto ausfüllen.

### <a name="to-export-data-and-submit-it-to-your-bank"></a>So exportieren Sie Daten und übermitteln sie an Ihre Bank

> [!CAUTION]  
> Wenn Sie Daten mithilfe der AMC Banking 365 Fundamentals-Erweiterung exportieren, werden einige Ihrer Geschäftsdaten dem Anbieter des Dienstes zugänglich gemacht. Der Dienstanbieter, AMC Consult A/S, ist für den Schutz dieser Daten verantwortlich. Weitere Informationen finden Sie unter [AMC-Datenschutzrichtlinie](https://go.microsoft.com/fwlink/?LinkId=510158).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zahlungsausgangs Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
2. Erstellen Sie die Journalzeilen, die Sie exportieren möchten.  

   > [!NOTE]
   > Denken Sie daran, für jede Zeile **Elektronische Zahlung** im Feld **Bankzahlungsart** zu wählen.
3. Wählen Sie die Aktion **Exportieren** aus.

### <a name="to-import-and-apply-the-converted-file"></a>So importieren und wenden Sie die konvertierte Datei an

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zahlungsabstimmungs Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Banktransaktion importieren** und dann die konvertierte Datei.  

   [!INCLUDE[prod_short](includes/prod_short.md)] erstellt ein neues Zahlungsabgleichsjournal, das die Daten in der Datei enthält. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

## <a name="see-also"></a>Siehe auch

[Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe von Erweiterungen](ui-extensions.md)  
[Bereitschaft für die Geschäftsabwicklung](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
