---
title: Verkaufssteuer sowie Steuergruppen in den USA und in Kanada| Microsoft Docs
description: "Mehr erfahren über das Einrichten von Verkaufssteuern, Steuergruppen, Steuergebieten, Steuerzuständigkeiten und Steuereinzelheiten."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ff1981a428a2cd3b3864b7f0cc795a1abeab7a10
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# <a name="sales-tax-and-tax-groups-in-the-us-and-canada"></a>Verkaufssteuer sowie Steuergruppen in den USA und in Kanada
Wenn Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] zum ersten Mal starten, können Sie eine unterstützte Einrichtung in Anspruch nehmen, um Verkaufssteuersteuerinformationen für Ihre Firma, Debitoren und Kreditoren schnell und einfach zu einrichten. In Minutenschnelle sind Sie bereit, Verkaufsbelege und Einkaufsbelege mit der Verkaufssteuer zu erstellen, die richtig berechnet werden kann. Dies wird erklärt [in unserem Blogeintrag](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy).
Wenn Sie auf das leere "Mein Unternehmen" umlagern, empfiehlt es sich, dass Sie beginnen, jedes einzelne der unterstützen Setuphandbücher zu verwenden, einschließlich demjenigen für die Verkaufssteuer. Wenn Sie es vorziehen, die Verkaufssteuer selber einzurichten, beschreibt dieser Artikel, was Sie berücksichtigen müssen.  

## <a name="tax-groups-tax-areas-and-tax-jurisdictions"></a>Steuergruppen, Steuergebiete und Steuerzuständigkeiten
In [!INCLUDE[d365fin](includes/d365fin_md.md)] besteht eine Steuergruppe aus einer Gruppe von Artikeln oder Ressourcen, die den gleichen Steuersätzen unterliegen. Beispielsweise können Sie eine Steuergruppe für steuerpflichtige Artikel und eine weitere für nicht zu versteuernde Artikel einrichten. Sie müssen Steuergruppencodes den Lagerartikeln und den Sachkonten zuweisen. Ebenso müssen Sie Steuergebietscodes, Lagerorte und Ihren eigenen Mandanteneinstellungen den Debitoren zuweisen. Das unterstützende Setuphandbuch hilft Ihnen dabei.  

Jedes Steuergebiet ist ein Gruppierung von Verkaufssteuerzuständigkeitsbereichen auf Grundlage einer bestimmten geografischen Lage. Beispielsweise hat das Steuergebiet in Miami, Florida, drei Verkaufssteuerzuständigkeitsbereiche: Stadt (Miami), Gemeinde (Dade) und Staat (Florida). [!INCLUDE[d365fin](includes/d365fin_md.md)] schließt eine begrenzte Zahl von Steuergebieten mit einer Standardkonfiguration ein, Sie können sie aber ändern und neue Steuergebiete hinzufügen.  

Wenn Sie neue Steuergebiete und Steuerzuständigkeiten einrichten, müssen Sie sicherstellen, dass Sie die richtig Felder ausfüllen. In den Vereinigten Staaten von Amerika können Staaten, Gemeinden, Orte und Lokale Verkaufssteuern belasten. In Kanada verlangen die Bundesregierung und die Provinzen Verkaufssteuern. Unternehmen erheben und leisten Verkaufssteuern an diese Regierungsbehörden für die Produkte, die an Endbenutzer verkauft werden. Verkaufssteuer kann auch zur vorhandenen Verkaufssteuer berechnet werden. Beispielsweise kann Steuer auf einem Verkaufsrechnungsbetrag berechnet werden, der bereits die Steuerbeträge von anderen Zuständigkeitsbereichen umfasst.  

In Kanada müssen Steuerbeträge für jede Steuerzuständigkeit detailliert dokumentiert sein. Bis zu vier Zuständigkeiten können in einem Beleg angezeigt werden und die Zuständigkeiten, die die gleiche Druckreihenfolge haben, werden zusammengefasst, wenn diese gedruckt werden.  

## <a name="tax-details"></a>Steuerdetails
Das Fenster **Steuerdetails** zeigt verschiedene Kombinationen von Verkaufssteuerzuständigkeitsbereichen und Mehrwertsteuergruppen an, um Verkaufssteuersätze einzurichten. Für jede Steuerzuständigkeit empfiehlt es sich, dass Sie eine Steuergruppe für normale Verkaufssteuer, eine andere Steuergruppe für Artikel oder Services, die nicht besteuert werden, und eine Nachsteuergruppe für jede Art Artikel oder Service einrichten, die mit einem anderen Verkaufssteuersteuersatz in diesem Steuerzuständigkeitsbereich vorhanden ist.  

Wenn Sie in den USA einem Debitor an einem Lagerort verkaufen, in dem Sie keinen *Status* oder gültigen Lagerort haben, erheben Sie keine Verkaufssteuer. Bei Lagerorten, in denen Sie keinen Status haben, ist sichergestellt, dass sowohl die Felder **Steuer unter dem Minimum** und die **Steuer über dem Maximum** 0.00 aufweisen.  

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Verkaufssteuer sowie Steuern auf Waren und Dienstleistungen in Kanada](ca-finance-tax.md)  
[Einfaches Einrichten der Verkaufssteuer](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]  

