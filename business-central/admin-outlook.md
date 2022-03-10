---
title: Holen Sie sich das Business Central-Add-in für Outlook
description: Erfahren Sie, wie Sie das Business Central-Add-in für Outlook für Ihr Unternehmen oder für den eigenen Gebrauch installieren.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365, Outlook
ms.search.form: 1831, 1832, 9020, 9022, 9027, 9030, 9004, 9005, 9018, 9006, 9007, 9010
ms.date: 08/13/2021
ms.author: jswymer
ms.openlocfilehash: 007d23bcb1d257402e33689ebe3ac57db10b84c2
ms.sourcegitcommit: 75a388b1d8917e2bbd49398ef76cf86cf37e6767
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323190"
---
# <a name="get-the-business-central-add-in-for-outlook"></a>Holen Sie sich das Business Central-Add-in für Outlook

Mit [!INCLUDE[prod_short](includes/prod_short.md)] können Sie geschäftliche Interaktionen mit Ihren Kunden und Kreditoren direkt in Microsoft Outlook verwalten. Mit dem Outlook-Add-in [!INCLUDE[prod_short](includes/prod_short.md)] können Sie Finanzdaten zu Kunden und Kreditoren einsehen. Sie können auch finanzielle Belege erstellen und versenden, z.B. Angebote und Rechnungen.  

Es gibt zwei Möglichkeiten, das Business Central-Add-in für Outlook zu installieren, je nach Ihrer Rolle im Unternehmen:

- Als Microsoft 365-Administrator verwenden Sie die Option *Zentrale Bereitstellung*, um das Add-in automatisch für das gesamte Unternehmen, für Gruppen oder für bestimmte Benutzer bereitzustellen.

- Als beliebiger Benutzer installieren Sie das Add-in für sich selbst, wenn Ihr Admin es nicht bereits für Sie bereitgestellt hat.

## <a name="about-the-business-central-add-in-for-outlook"></a>Über das Business Central-Add-in für Outlook

Das Business Central-Add-in für Outlook besteht aus zwei kleineren Add-ins:

- Contact Insights

    Dieses Add-In stellt Benutzern [!INCLUDE[prod_short](includes/prod_short.md)] Kunden- oder Kreditor-Informationen in Outlook-E-Mails und Kalenderterminen zur Verfügung. Außerdem ermöglicht es Ihnen, [!INCLUDE[prod_short](includes/prod_short.md)] geschäftliche Belege, wie Verkaufsangebote und Rechnungen, zu erstellen und an einen Kontakt zu senden. <!--To support these task, the add-in adds actions to the Outlook ribbon, in the **Business Central** group. --> 

- Beleg-Ansicht

    Wenn in einer E-Mail auf die Nummer eines Geschäftsdokuments verwiesen wird, bietet dieses Add-In einen direkten Inline-Link vom E-Mail-Text zu dem tatsächlichen Geschäftsdokument in [!INCLUDE[prod_short](includes/prod_short.md)].

Weitere Informationen darüber, was Sie mit den Add-Ins tun können, finden Sie unter [Benutzung von Business Central als geschäftlicher Posteingang in Outlook](work-outlook-addin.md).

Jedes Add-In wird in Form einer XML-Datei bereitgestellt, die als *Manifest* bezeichnet wird und die von jedem, der diese Funktionalität wünscht, in Outlook installiert werden muss. Diese Dateien beschreiben, wie die Add-Ins aktiviert und mit Business Central verbunden werden, wenn sie in Outlook verwendet werden. Die Arbeit mit diesen Dateien wird normalerweise von einem Admin durchgeführt. Als normaler Benutzer werden Sie in den meisten Fällen nicht direkt mit diesen Dateien arbeiten müssen. Entweder legt Ihr Admin fest, dass das Add-In automatisch für Sie installiert wird, oder Sie verwenden die integrierte unterstützte Einrichtung, um die Installation durchzuführen.

## <a name="deploy-the-add-in-by-using-centralized-deployment-as-an-admin"></a>Bereitstellen des Add-Ins über die zentrale Bereitstellung als Admin

Die zentrale Bereitstellung ist eine Funktion im Microsoft 365 Admin Center, mit der Sie Add-Ins automatisch in den Office-Apps der Benutzer, z. B. Outlook, bereitstellen können. Es ist die empfohlene Methode für Admins, Office Add-ins für Benutzer und Gruppen innerhalb Ihres Unternehmens bereitzustellen.

> [!NOTE]
> Für Business Central on-premises, siehe [Einrichten des Add-Ins für Outlook Integration mit Business Central On-Premises](/dynamics365/business-central/dev-itpro/administration/setting-up-office-add-ins-outlook-inbox) im Administrationsinhalt (nur auf Englisch).

### <a name="prerequisites"></a>Voraussetzungen

- Ein Microsoft 365-Abonnement  
- Benutzern wird eine Microsoft 365-Lizenz zugewiesen  
- Ihr Microsoft 365-Konto hat die Rolle *Global Administrator* oder *Exchange Administrator*.

### <a name="deploy-the-add-in"></a>Bereitstellen des Add-Ins

1. Wählen Sie in Business Central die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Unterstützte Einrichtung** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Outlook Add-in Zentrale Bereitstellung**, um die Anleitung zur unterstützten Einrichtung zu starten.
3. Überprüfen Sie die erste Seite und wählen Sie **Weiter**, um die Seite zum Herunterladen der Add-Ins zu öffnen.
4. Aktivieren Sie in der Spalte **Bereitstellen** das Kontrollkästchen für die Add-Ins, die Sie bereitstellen möchten, und wählen Sie dann **Herunterladen und weiter**.

    Eine Datei mit dem Namen *OutlookAddins.zip* wird auf Ihr Gerät heruntergeladen.

5. An diesem Punkt sind Sie mit der Arbeit in Business Central fertig, sodass Sie **Erledigt** wählen können.

   >[!TIP]
   > Bevor Sie **Weiter** auswählen, wählen Sie den Link **Zu Microsoft 365 (öffnet in einem neuen Fenster)** aus, um das Microsoft 365 Admin Center in einem neuen Browserfenster zu öffnen und sich dort anzumelden. Sie müssen das Microsoft 365 Admin Center ohnehin in einem späteren Schritt aufrufen.

6. Wechseln Sie in den Ordner, in dem die OutlookAddins.zip heruntergeladen wurde, und extrahieren Sie die Dateien **Contact Insights.xml** und **Document View.xml** aus der .zip-Datei in einen Ordner Ihrer Wahl.

    Weitere Informationen finden Sie unter [Zippen und Entpacken von Dateien und Ordnern](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).
7. Melden Sie sich beim Microsoft 365 Admin Center an, und wechseln Sie dann zu [Integrierte Apps](https://go.microsoft.com/fwlink/?linkid=2163967).

8. Wählen Sie **Angepasste Apps hochladen**.
9. Auf der Seite **Apps zum Bereitstellen hochladen** wählen Sie **Manifestdatei (.xml) vom Gerät hochladen** > **Datei auswählen**.
10. Wählen Sie eine der Zusatzdateien, die Sie zuvor extrahiert haben, z.B. **Kontakte Insights.xml**.
11. Folgen Sie den Anweisungen, um Benutzer zuzuweisen und das Add-In bereitzustellen.
12. Wiederholen Sie die Schritte 9 bis 11 für die andere Add-In-Datei, wenn Sie möchten.

> [!IMPORTANT]
> Ein grünes Häkchen erscheint, wenn das Add-In im Admin Center bereitgestellt ist. Es kann jedoch bis zu 24 Stunden dauern, bis die Benutzer das Add-In in der Outlook App sehen. Möglicherweise müssen die Benutzer auch Outlook neu starten.

Wenn Sie fertig sind, können Sie die Bereitstellung im Microsoft 365 Admin Center jederzeit ändern, z. B. weitere Benutzer zuweisen. Weitere Informationen über das Bereitstellen von Add-Ins im Admin Center finden Sie unter [Einsatz von Add-Ins im Admin Center](/microsoft-365/admin/manage/manage-deployment-of-add-in).

## <a name="install-the-add-in-for-your-own-use"></a><a name="install"></a>Installieren Sie das Add-In für Ihren eigenen Gebrauch

Wenn Ihr Unternehmen es zulässt, können Sie das Business Central Add-In auch für sich selbst installieren. Wenden Sie sich an Ihren Administrator, wenn Sie sich nicht sicher sind.

1. Gehen Sie in Business Central zu der ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Outlook Add-in abrufen** ein und wählen Sie dann den entsprechenden Link.
2. Lesen Sie die Seite und wählen Sie **Weiter**, wenn Sie fertig sind.
3. Wenn Sie eine Willkommensnachricht von Business Central mit einem Überblick über die Verwendung des Add-Ins erhalten möchten, aktivieren Sie **Beispielnachricht senden**.
4. Wählen Sie **Abschließen**, um die Installation abzuschließen.

Business Central wird eine Verbindung zu Ihrem E-Mail-Server herstellen und das Add-in in Ihrem Outlook installieren. Dies wird nicht lange dauern. Jetzt können Sie das Add-In in Outlook verwenden.

### <a name="for-business-central-on-premises"></a><a name="onprem"></a>Für Business Central On-Premises

Wenn Sie Business Central on-premises verwenden, kann die Installation des Add-Ins etwas anders ablaufen.

1. Gehen Sie in Business Central zu der ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Outlook Add-in abrufen** ein und wählen Sie dann den entsprechenden Link.
2. Lesen Sie die Seite und wählen Sie **Weiter**, wenn Sie fertig sind.
3. Führen Sie einen der folgenden Schritte aus, je nachdem, welche Seite Sie sehen:

    - Wenn Sie die Schaltfläche **In mein Outlook installieren** sehen, wählen Sie sie aus und Sie sind fertig.
    - Wenn Sie die Schaltfläche **Weiter** sehen, wählen Sie sie aus. Wenn Sie auf der nächsten Seite eine Willkommensnachricht von Business Central mit einem Überblick über die Verwendung des Add-Ins erhalten möchten, aktivieren Sie **Beispiel-E-Mail senden**. Wählen Sie dann **Abschließen** und Sie sind fertig.
    - Wenn Sie die Schaltfläche **Add-in herunterladen** sehen, wählen Sie sie aus und gehen dann zum nächsten Schritt.
4. Wenn Sie **Add-in herunterladen** wählen, wird eine Datei mit dem Namen *OutlookAddins.zip* auf Ihr Gerät heruntergeladen. Sie sollten die Datei im oberen Bereich des Browsers sehen.

   Gehen Sie in den Ordner, in den die OutlookAddins.zip heruntergeladen wurde, und extrahieren Sie die Dateien **Contact Insights.xml** und **Dokumentenansicht.xml** aus der .zip-Datei in einen Ordner Ihrer Wahl. Weitere Informationen über das Extrahieren von Dateien finden Sie unter [Zippen und Entpacken von Dateien und Ordnern](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).

5. Öffnen Sie Outlook und wählen Sie **Add-ins holen** aus dem Menüband. Oder, wenn Sie Outlook im Internet verwenden, wählen Sie das Dropdown-Menü einer neuen oder bestehenden Nachricht und wählen Sie dann **Add-ins abrufen**.
6. Wählen Sie **Meine Add-Ins** > **Ein angepasstes Add-In hinzufügen** > **Hinzufügen aus einer Datei**.
7. Wählen Sie eine der .xml-Dateien, die Sie extrahiert haben, z.B. **Contact Insights.xml**, und wählen Sie dann **Öffnen** > **Installieren**.
8. Wiederholen Sie die Schritte 6 und 7 für die andere .xml-Datei, wenn Sie eine heruntergeladen haben.

Jetzt können Sie das Add-In in Outlook verwenden.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Weitere Informationen

[Einrichten des Geschäftsbetriebs](ui-get-ready-business.md)  
[Abrufen von Business Central auf meinem mobilen Gerät](install-mobile-app.md)  
[Dokumente per E-Mail versenden](ui-how-send-documents-email.md)  
[Finanzen](finance.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Mindestanforderungen für die Verwendung von Outlook](product-requirements.md#outlook)  
[Add-Ins in Outlook im Internet nutzen](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]