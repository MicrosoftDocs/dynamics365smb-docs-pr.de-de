---
title: Verkaufssteuer Warensteuer sowie Services-Steuer in Kanada| Microsoft Docs
description: Informationen zu GST und HST.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 03/23/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e1866f5047a826f3d527267d901eb30279d5b4e4
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# <a name="sales-tax-and-goods-and-services-tax-in-canada"></a>Verkaufssteuer sowie Steuern auf Waren und Dienstleistungen in Kanada
Wenn ein Kreditor in Kanada keine Geschäftspräsenz in der Provinz hat, in der die Einkäufe getätigt werden, berechnet der Kreditor nur Steuern auf Waren und Dienstleistungen (Goods and Services Tax, GST) oder Harmonised Sales Tax (HST). Wenn jedoch die Provinz eine Provincial Sales Tax (PST) erhebt, dann muß der Einkäufer noch die PST berechnen und sie direkt an die Provinz bezahlen. Wenn ein Steuergebietscode für Provinzen aktiviert ist, verwendet [!INCLUDE[d365fin](includes/d365fin_md.md)]  diesen, um die PST zu berechnen und zu buchen, sodass sowohl im Sachkonto als auch in den Steuerpostendatensätzen Steuerverbindlichkeiten vermerkt sind. Daher sollte der Steuergebietscode, der hier aktiviert ist, nur die PST enthalten, nicht die GST.  

Weitere Informationen zur Verkaufssteuer, finden Sie unter [Verkaufssteuer sowie Steuergruppen in den USA und in Kanada](us-finance-sales-tax.md).  

## <a name="submitting-the-gsthst-file"></a>Übermitteln der GST-/HST-Datei
Die Steuerdaten in Einkaufsbelegen werden verwendet, um eine GST/HST-Online-Dateiübertragung (GIFT) zu generieren, die Sie dem Finanzamt bereitstellen müssen. Diese Datei umfasst Steuern auf Waren und Dienstleistungen (GST) und die Harmonised Sales Tax (HST). Die Datei wird in einem .tax-Dateiformat erstellt, das online übertragen werden kann.  

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Finance einrichten](us-finance-sales-tax.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]

