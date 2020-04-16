---
title: Zahlungsabstimmung mit der Envestnet Yodlee Bank Feeds Erweiterung | Microsoft Docs
description: Beschreibt die Envestnet Yodlee Bank Feeds Erweierung, die die Bankkonten verknüpft, sodass Sie schnell Zahlungen abgleichen können.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ca384d58046bd0c798038878a3ed93f5a00eeec5
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189843"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a>Die Envestnet Yodlee Bank Feeds-Erweiterung
Um die Zahlungen schnell abzustimmen, die an Ihre Bankkonten getätigt werden, kann der Envestnet Yodlee Bank Feeds Service Ihre Systembankkonten mit Ihrem Online Bankkonto verknüpfen. Das bedeutet, dass der letzte Bankkontoauszug automatisch oder manuell in Ihr Abstimmungsbuch.-Blatt gespeist wird und stellt sicher, dass immer die aktuelle Zahlungen mit minimalem Fehlerrisiko verarbeitet werden.

Der Envestnet Yodlee Bank Feeds-Service wird nur in den Vereinigten Staaten und Kanada unterstützt.

> [!NOTE]
> Der Envestnet Yodlee Bank Feeds Service wird nur in der Online-Version von Business Central unterstützt. Um diese Funktionalität lokal nutzen zu können, müssen Sie ein Co-Brand-Konto von Envestnet Yodlee erhalten.<br /><br />
> Der Envestnet Yodlee Bank Feeds-Service wird nur in den Vereinigten Staaten und Kanada unterstützt.
> Es werden nur Banken mit Wohnsitz in diesen Ländern unterstützt, auch wenn Banken aus anderen Ländern im Bankenauswahlfenster Envestnet Yodlee Bank Feeds unter [!INCLUDE[d365fin](includes/d365fin_md.md)] erscheinen können.

> [!IMPORTANT]
> Aufgrund der neuen Zahlungsdiensterichtlinie in Europa (PSD2) können Sie nach dem 14. September 2019 nicht mehr automatisch Kontoauszüge von Banken in Großbritannien importieren in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Wir prüfen, ob wir dieses Funktion in Zukunft wieder anbieten können.

Der Envestnet Yodlee Bank Feeds Service bietet die folgenden Vorteile:

* Entfernt die Anforderung zur manuellen Eingabe.
* Verbessert Effektivität und die Genauigkeit, wenn die Zahlungsabstimmung erfolgt.
* Unterstützt viele Banken.
* Hier aktuelle Informationen über Banktransaktionen in [!INCLUDE[d365fin](includes/d365fin_md.md)]
* Unterstützt manuelle sowie automatische Bankfeeds.
* Aktiviert das Outsourcing der Zahlungsabstimmung zu einem Buchhalter, indem das Bieten des Lagerzugang zu den Bankkontoauszügen bereitgestellt wird.

Weitere Informationen finden Sie unter [Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md).

## <a name="see-also"></a>Siehe auch
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)    
[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
