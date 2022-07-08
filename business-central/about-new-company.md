---
title: Neue Unternehmen mithilfe der Anleitung für die unterstützte Einrichtung erstellen
description: Es ist einfach, ein neues, leeres Unternehmen in Business Central. zu erstellen. Ein unterstütztes Einrichtungshandbuch hilft Ihnen Schritte für Schritt und Sie können Ihre vorhandenen Geschäftsdaten importieren.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.search.form: 1803, 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4fcc6d93c234e6c7a5b7b62514f53157878fee81
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079428"
---
# <a name="create-new-companies-in-prod_short"></a>Neue Unternehmen in [!INCLUDE[prod_short](includes/prod_short.md)] erstellen

In [!INCLUDE[prod_short](includes/prod_short.md)] wird der Container für Geschäftsdaten, die zu einem Konzernmandanten oder einer juristischen Person gehören, als *Unternehmen* bezeichnet. Wenn Sie sich für [!INCLUDE[prod_short](includes/prod_short.md)] registrieren, erhalten Sie ein Demounternehmen und ein leeres Unternehmen, *Mein Unternehmen*. Der Wechsel zwischen den Unternehmen ist einfach: Gehen Sie einfach zu **Meine Einstellungen** und wechseln Sie zu dem anderen Unternehmen. Sie können aber auch neue Unternehmen in [!INCLUDE[prod_short](includes/prod_short.md)] gründen, je nach Ihren Geschäftsanforderungen.  

Wenn Sie einen neuen Mandanten erstellen, hilft Ihnen ein unterstütztes Einrichtungshandbuch, die Grundlagen einzurichten. Dann können Sie relevante Daten aus dem Legacysystem oder einem anderen Mandanten in [!INCLUDE[prod_short](includes/prod_short.md)] importieren.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="choose-the-right-template"></a>Die richtige Vorlage auswählen

Wenn Sie sich entscheiden, einen Mandanten Ihrem [!INCLUDE[prod_short](includes/prod_short.md)] hinzuzufügen, können Sie den Leitfaden für das unterstützte Setup für **Neues Unternehmen erstellen** verwenden. Der Einrichtungsassistent ist auf der Seite **Firmen** und über die Suche im Feld **Firma** auf der Seite **Meine Einstellungen** verfügbar.  

Der Setup-Assistent stellt zwei Vorlagen und eine leere Option zur Verfügung:

- **Bewertung - Beispieldatei**  
    Dies erstellt einen Mandanten, der gleich ist wie das Demounternehmen mit Beispieldaten und Einrichtungsdaten. Dieser Unternehmenstyp steht Ihnen im Gegensatz zu den anderen Typen ohne Wechsel zu einem 30-tägigen Testzeitraum zur Verfügung.  
- **Produktion - nur Einrichtungsdaten**  
    Dies erstellt einen Mandanten, der gleich ist wie **Mein Unternehmen** mit Einrichtungsdaten aber ohne Beispieldaten. Sie können dieses Unternehmen für einen 30-tägigen Testzeitraum verwenden.  
- **Neue Chargennr. erstellen**  
    Dies erstellt einen leeren Mandanten ohne Einrichtungsdaten. Sie können dieses Unternehmen für einen 30-tägigen Testzeitraum verwenden.  

Wenn Sie mit einem neuen Mandanten einfach anfangen möchten, wählen Sie **Produktion - nur Daten einrichten** und importieren dann Ihre eigenen Geschäftsdaten, beispielsweise Debitoren, Kreditoren und Artikel. Wählen Sie die Vorlage aus **Neu**, wenn Sie etwas von Grund auf neu einrichten möchten. In diesem Fall können Sie den unterstützten Einrichtungs-Assistent **Unternehmenseinrichtung** verwenden, um Ihnen zu helfen, mit wesentlichen Einrichtungsdaten anzufangen.  

> [!NOTE]  
> Wenn Sie einen neuen Mandanten erstellen, dauert es mehrere Minuten, bevor Sie in [!INCLUDE[prod_short](includes/prod_short.md)]zugreifen können. Der Einrichtungsstatus auf der Seite **Unternehmen** zeigt an, ob das neue Unternehmen für Sie bereit ist. Dann können Sie zum neuen Mandanten wechseln, indem Sie **Meine Einstellungen** verwenden.  

Während Ihrer 30-Tage-Testphase können Sie eine beliebige Anzahl neuer Unternehmen erstellen, allerdings sind diese nur innerhalb der Testphase verfügbar. Weitere Informationen erhalten Sie von Ihrem [!INCLUDE[prod_short](includes/prod_short.md)]-Partner. Weitere Informationen finden Sie im Artikel [FAQ zur Dynamics 365 Business Central-Testversion](trial-faq.md).  

[Hier](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions) kann Ihr Administrator mehr über Testversionen und Abonnements erfahren.  

## <a name="copy-a-company"></a>Unternehmen kopieren

Auf der Seite **Firmen** können Sie mit der Aktion **Kopieren** eine zweite Firma basierend auf den Inhalten einer bestehenden Firma anlegen. Dies ist z.B. nützlich, wenn Sie ein Unternehmen testen möchten, ohne die Produktionsdaten zu stören.

> [!Important]
> Diese Funktion kann nicht verwendet werden, um ein Backup eines Unternehmens zu erstellen. Die Erstellung eines Firmen-Backups beginnt mit dem Export der Datenbank als .bacpac-Datei. Weitere Informationen finden Sie unter [Datenbanken exportieren](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) in der Hilfe zu Entwicklung und Verwaltung.

## <a name="set-up-the-company"></a>Unternehmen einrichten

Wenn Sie sich in einem neuen Mandanten annmelden, wird der Assistent **Unternehmenseinrichtung** automatisch ausgeführt und hilft Ihnen mit den ersten Schritten. Sie werden um Informationen zu Ihrem Unternehmen, wie zur Adresse, zu den Bankdetails und zur Lagerbestandmethode gebeten. Wir bitten um diese Information, da sie als Grundlage für eine Vielzahl von Bereichen in [!INCLUDE[prod_short](includes/prod_short.md)] verwendet werden, die Sie dann später nicht manuell einrichten müssen.  

[!INCLUDE [prod_short](includes/prod_short.md)] enthält beispielsweise Ihre Firmenadresse in Rechnungen und anderen Dokumenten und Ihre Bankdaten in Zahlungen. Die Kostenmethode wird zur Preiskalkulation und Bestandsbewertung verwendet.  

Sobald Sie die Grundlagen bereit haben, können Sie die übrigen Kernbereiche einrichten. Anschließend sind Sie bereit, Geschäftsdaten, beispielsweise Debitoren und Kreditoren, einzugeben. Weitere Informationen finden Sie unter [[!INCLUDE[prod_short](includes/prod_short.md)]](setup.md) einrichten.  

## <a name="companies-and-environments"></a>Unternehmen und Umgebungen

[!INCLUDE [company_environment](includes/company_environment.md)]

Weitere Informationen finden Sie unter [Wechseln zu einem anderen Unternehmen oder einer anderen Umgebung ](ui-organization-switch.md). Weitere Informationen zu Umgebungen finden Sie unter [Grundlegendes zur Infrastruktur von Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology) (nur in englischer Sprache).  

## <a name="changing-a-companys-name"></a>Ändern des Namens eines Unternehmens

Sobald ein Unternehmen erstellt wurde, können Sie seinen Namen nicht mehr ändern. Aber Sie können den **Anzeigename** ändern. Dies ist ein Text, der für das Unternehmen in der gesamten Anwendung angezeigt wird.  

> [!TIP]
> Sie können eine Firma umbenennen, wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] lokal verwenden.

## <a name="add-contoso-coffee"></a>Contoso Coffee hinzufügen

Die Contoso Coffee-App stellt Demonstrationsdaten bereit, anhand derer Sie die erweiterten Funktionen von [!INCLUDE [prod_short](includes/prod_short.md)] erkunden können. Suchen Sie die App in AppSource, und installieren Sie sie in einem leeren Unternehmen, beispielsweise einem Unternehmen in einer Sandkastenumgebung. Weitere Informationen finden Sie unter [Einführung in die Demodaten für Contoso Coffee](contoso-coffee/contoso-coffee-intro.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Siehe zugehörige Schulung unter [Microsoft Learn](/learn/modules/create-new-companies-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Business Central anpassen](ui-customizing-overview.md)  
[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Importieren von Geschäftsdaten aus anderen Finance-Systemen](across-import-data-configuration-packages.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Vorbereiten auf die Geschäftsabwicklung](ui-get-ready-business.md)  
[Grundlegendes zur Infrastruktur von Business Central Online (nur in englischer Sprache)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  


[!INCLUDE[footer-include](includes/footer-banner.md)]