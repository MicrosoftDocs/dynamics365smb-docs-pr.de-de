---
title: Erstellen Sie neue Unternehmen, die ein unterstütztes Einrichtungshandbuch verwenden | Microsoft Docs
description: Es ist einfach, ein neues, leeres Unternehmen in Business Central. zu erstellen. Ein unterstütztes Einrichtungshandbuch hilft Ihnen Schritte für Schritt und Sie können Ihre vorhandenen Geschäftsdaten importieren.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fc318d3de70cb56e722bd02c868fc570fb62692b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385049"
---
# <a name="creating-new-companies-in-prod_short"></a>Neue Unternehmen anlegen in [!INCLUDE[prod_short](includes/prod_short.md)]

In [!INCLUDE[prod_short](includes/prod_short.md)] wird der Container für Geschäftsdaten, die zu einem Konzernmandanten oder einer juristischen Person gehören, als *Unternehmen* bezeichnet. Wenn Sie sich anmelden [!INCLUDE[prod_short](includes/prod_short.md)], werden Ihnen Demomandanten und ein leeres Unternehmen, *Mein Unternehmen* zugeordnet. Der Wechsel zwischen den Unternehmen ist einfach: Gehen Sie einfach zu **Meine Einstellungen** und wechseln Sie zu dem anderen Unternehmen. Sie können aber auch neue Unternehmen in [!INCLUDE[prod_short](includes/prod_short.md)] gründen, je nach Ihren Geschäftsanforderungen. Wenn Sie einen neuen Mandanten erstellen, hilft Ihnen ein unterstütztes Einrichtungshandbuch, die Grundlagen einzurichten. Dann können Sie relevante Daten aus dem Legacysystem oder einem anderen Mandanten in [!INCLUDE[prod_short](includes/prod_short.md)] importieren.  

## <a name="creating-a-new-company"></a>Erstellen einer neuen Firma

Wenn Sie sich entscheiden, einen Mandanten Ihrem [!INCLUDE[prod_short](includes/prod_short.md)] hinzuzufügen, können Sie den Leitfaden für das unterstützte Setup für **Neues Unternehmen erstellen** verwenden. Der Einrichtungsassistent ist auf der Seite **Firmen** und über die Suche im Feld **Firma** auf der Seite **Meine Einstellungen** verfügbar.  

Der Setup-Assistent bietet drei Vorlagen und eine leere Option:

- **Bewertung - Beispieldatei**  
    Dies erstellt einen Mandanten, der gleich ist wie das Demounternehmen mit Beispieldaten und Einrichtungsdaten.  
- **Produktion - nur Einrichtungsdaten**  
    Dies erstellt einen Mandanten, der gleich ist wie **Mein Unternehmen** mit Einrichtungsdaten aber ohne Beispieldaten.
- **Erweiterte Auswertung - vollständiger Beispieldaten** Erstellt einen Mandanten mit Einrichtungsdaten und vollständigen Beispieldaten für alle Funktionen, einschließlich Produktion und Dienstleistungs-Verwaltung.
- **Neue Chargennr. erstellen**  
    Dies erstellt einen leeren Mandanten ohne Einrichtungsdaten.  

Wenn Sie mit einem neuen Mandanten einfach anfangen möchten, wählen Sie **Produktion - nur Daten einrichten** und importieren dann Ihre eigenen Geschäftsdaten, beispielsweise Debitoren, Kreditoren und Artikel. Wählen Sie die Vorlage aus **Neu**, wenn Sie etwas von Grund auf neu einrichten möchten. In diesem Fall können Sie den unterstützten Einrichtungs-Assistent **Unternehmenseinrichtung** verwenden, um Ihnen zu helfen, mit wesentlichen Einrichtungsdaten anzufangen.  

> [!NOTE]  
> Wenn Sie einen neuen Mandanten erstellen, dauert es mehrere Minuten, bevor Sie in [!INCLUDE[prod_short](includes/prod_short.md)]zugreifen können. Der Einrichtungsstatus auf der Seite **Unternehmen** zeigt an, ob das neue Unternehmen für Sie bereit ist. Dann können Sie zum neuen Mandanten wechseln, indem Sie **Meine Einstellungen** verwenden.  

Während Ihrer 30-Tage-Testphase können Sie eine beliebige Anzahl neuer Unternehmen erstellen, allerdings sind diese nur innerhalb der Testphase verfügbar. Weitere Informationen erhalten Sie von Ihrem [!INCLUDE[prod_short](includes/prod_short.md)]-Partner.  

## <a name="copying-a-company"></a>Kopieren einer Firma

Auf der Seite **Firmen** können Sie mit der Aktion **Kopieren** eine zweite Firma basierend auf den Inhalten einer bestehenden Firma anlegen. Dies ist z.B. nützlich, wenn Sie ein Unternehmen testen möchten, ohne die Produktionsdaten zu stören.

> [!Important]
> Diese Funktion kann nicht verwendet werden, um ein Backup eines Unternehmens zu erstellen. Die Erstellung eines Firmen-Backups beginnt mit dem Export der Datenbank als .bacpac-Datei. Weitere Informationen finden Sie unter [Datenbanken exportieren](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) in der Hilfe zu Entwicklung und Verwaltung.

## <a name="company-setup"></a>Unternehmenseinrichtung

Wenn Sie sich in einem neuen Mandanten annmelden, wird der Assistent **Unternehmenseinrichtung** automatisch ausgeführt und hilft Ihnen mit den ersten Schritten. Sie werden um Informationen zu Ihrem Unternehmen, wie zur Adresse, zu den Bankdetails und zur Lagerbestandmethode gebeten. Wir bitten um diese Information, da sie als Grundlage für eine Vielzahl von Bereichen in [!INCLUDE[prod_short](includes/prod_short.md)] verwendet werden, die Sie dann später nicht manuell einrichten müssen.  

Beispielsweise wird Ihre Mandantenadresse in Rechnungen und in anderen Belegen enthalten, werden Ihre Bankinformationen in den Zahlungen verwendet, die Lagerabgangsmethode und wird verwendet, um Preise zu berechnen und auf Lager Bewertung.  

Sobald Sie die Grundlagen bereit haben, können Sie die übrigen Kernbereiche einrichten. Anschließend sind Sie bereit, Geschäftsdaten, beispielsweise Debitoren und Kreditoren einzugeben. Weitere Informationen finden Sie unter [Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  

## <a name="companies-and-environments"></a>Unternehmen und Umgebungen

[!INCLUDE [company_environment](includes/company_environment.md)]

Weitere Informationen finden Sie unter [Wechseln zu einem anderen Unternehmen oder einer anderen Umgebung ](ui-organization-switch.md). 

## <a name="changing-a-companys-name"></a>Ändern des Firmennamens

Sobald ein Unternehmen erstellt wurde, können Sie seinen Namen nicht mehr ändern. Aber Sie können den **Anzeigename** ändern. Dies ist ein Text, der für das Unternehmen in der gesamten Anwendung angezeigt wird.  

> [!TIP]
> Sie können eine Firma umbenennen, wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] lokal verwenden.

## <a name="see-also"></a>Siehe auch

[Business Central anpassen](ui-customizing-overview.md)  
[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Importieren von Geschäftsdaten aus anderen Finanzsystemen](across-import-data-configuration-packages.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Erste Schritte](product-get-started.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]