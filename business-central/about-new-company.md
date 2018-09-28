---
title: "Erstellen Sie neue Unternehmen, die ein unterstütztes Einrichtungshandbuch verwenden | Microsoft Docs"
description: "Es ist einfach, ein neues, leeres Unternehmen in Business Central. zu erstellen. Ein unterstütztes Einrichtungshandbuch hilft Ihnen Schritte für Schritt und Sie können Ihre vorhandenen Geschäftsdaten importieren."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: ce2fd5c5027fc54c92bf5ffc63b70c84d81f26b3
ms.contentlocale: de-de
ms.lasthandoff: 05/17/2018

---
# <a name="creating-new-companies-in-included365finincludesd365finmdmd"></a>Neue Unternehmen anlegen in [!INCLUDE[d365fin](includes/d365fin_md.md)]
In [!INCLUDE[d365fin](includes/d365fin_md.md)] bezeichnet die Container für Geschäftsdaten, die einem Konzernmandanten oder einer juristischen Person angehören als *Unternehmen*. Wenn Sie sich anmelden [!INCLUDE[d365fin](includes/d365fin_md.md)], werden Ihnen Demomandanten und ein leeres Unternehmen, *Mein Unternehmen* zugeordnet. Umschaltung zwischen den Mandanten ist einfach. Gehen Sie zu **Meine Einstellungen** und gehen Sie zum anderen Unternehmen. Wenn Sie können neue Unternehmen, abhängig von Ihren [!INCLUDE[d365fin](includes/d365fin_md.md)]Geschäftsanforderungen auch anlegen. Wenn Sie einen neuen Mandanten erstellen, hilft Ihnen ein unterstütztes Einrichtungshandbuch, die Grundlagen einzurichten. Dann können Sie relevante Daten aus dem Legacysystem oder einem anderen Mandanten in [!INCLUDE[d365fin](includes/d365fin_md.md)] importieren.  

## <a name="create-new-company"></a>Neues Unternehmen erstellen
Wenn Sie sich entscheiden, einen Mandanten Ihrem [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzuzufügen, können Sie den unterstützten Einrichtungsassistenten **Neues Unternehmen erstellen** verwenden. Der Setup-Assistent wird im Fenster **Unternehmen** und der Suche unter **Unternehmen** im Feld **Meine Einstellungen** angezeigt.  

Der Setup-Assistent bietet drei Vorlagen an:

-   **Bewertung - Beispieldatei**  
    Dies erstellt einen Mandanten, der gleich ist wie das Demounternehmen mit Beispieldaten und Einrichtungsdaten.  
-   **Produktion - nur Einrichtungsdaten**  
    Dies erstellt einen Mandanten, der gleich ist wie **Mein Unternehmen** mit Einrichtungsdaten aber ohne Beispieldaten.
-   **Erweiterte Auswertung - vollständiger Beispieldaten** Erstellt einen Mandanten mit Einrichtungsdaten und vollständigen Beispieldaten für alle Funktionen, einschließlich Produktion und Dienstleistungs-Verwaltung.
-   **Neue Chargennr. erstellen**  
    Dies erstellt einen leeren Mandanten ohne Einrichtungsdaten.  

Wenn Sie mit einem neuen Mandanten einfach anfangen möchten, wählen Sie **Produktion - nur Daten einrichten** und importieren dann Ihre eigenen Geschäftsdaten, beispielsweise Debitoren, Kreditoren und Artikel. Wählen Sie die Vorlage aus **Neu**, wenn Sie etwas von Grund auf neu einrichten möchten. In diesem Fall können Sie den unterstützten Einrichtungs-Assistent **Unternehmenseinrichtung** verwenden, um Ihnen zu helfen, mit wesentlichen Einrichtungsdaten anzufangen.  

> [!NOTE]  
>   Wenn Sie einen neuen Mandanten erstellen, dauert es mehrere Minuten, bevor Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)]zugreifen können. Der Einrichtungsstatus im **Unternehmen** zeigt an, ob das neue Unternehmen für Sie bereit ist. Dann können Sie zum neuen Mandanten wechseln, indem Sie **Meine Einstellungen** verwenden.  

Während Ihrer 30-Tage-Testphase können Sie eine beliebige Anzahl neuer Unternehmen erstellen, allerdings sind diese nur innerhalb der Testphase verfügbar. Weitere Informationen erhalten Sie von Ihrem [!INCLUDE[d365fin](includes/d365fin_md.md)]-Partner.  

## <a name="company-setup"></a>Unternehmenseinrichtung
Wenn Sie sich in einem neuen Mandanten annmelden, wird der Assistent **Unternehmenseinrichtung** automatisch ausgeführt und hilft Ihnen mit den ersten Schritten. Sie werden um Informationen zu Ihrem Unternehmen, wie zur Adresse, zu den Bankdetails und zur Lagerbestandmethode gebeten. Wir bitten um diese Information, da sie als Grundlage für eine Vielzahl von Bereichen in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet werden, die Sie dann später nicht manuell einrichten müssen.  

Beispielsweise wird Ihre Mandantenadresse in Rechnungen und in anderen Belegen enthalten, werden Ihre Bankinformationen in den Zahlungen verwendet, die Lagerabgangsmethode und wird verwendet, um Preise zu berechnen und auf Lager Bewertung.  

Sobald Sie die Grundlagen bereit haben, können Sie die übrigen Kernbereiche einrichten. Anschließend sind Sie bereit, Geschäftsdaten, beispielsweise Debitoren und Kreditoren einzugeben. Weitere Informationen finden Sie unter [Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  

## <a name="see-also"></a>Siehe auch
[Business Central anpassen](ui-customizing-overview.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Erste Schritte](product-get-started.md)  

