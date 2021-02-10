---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dcfc54d36b212b296747d28945324ac46c38cada
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753617"
---
Personen unterstützen manchmal mehrere Unternehmen und müssen in [!INCLUDE [prod_short](prod_short.md)] problemlos zwischen Unternehmen wechseln. Ein Unternehmen kann beispielsweise Verkaufsbüros in Städten und mehreren Ländern haben, sodass für jedes Büro eine separate Geschäftseinheit eingerichtet wurde. Die Büros, die sich im selben Land befinden, werden als separate Unternehmen in einer gemeinsamen Umgebung eingerichtet. Andere Büros werden als Unternehmen in separaten Umgebungen erstellt, da sie geografisch in anderen Ländern ansässig sind.<br><br>  

Was ist eine Umgebung? Unternehmen in [!INCLUDE[prod_short](prod_short.md)] befinden sich in sogenannten *Umgebungen*. Es gibt zwei Typen von Umgebungen, **Produktion** und **Sandbox**. Kurz gesagt, Produktionsumgebungen enthalten Live-Geschäftsdaten und Sandbox-Umgebungen werden als sicherer Ort zum Testen neuer Geschäftsprozesse oder Funktionen verwendet. Weitere Informationen finden Sie unter [Umgebungstypen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments). Wenn Sie Zugriff auf ein Unternehmen haben, haben Sie auch Zugriff auf die Umgebung, in der es sich befindet. Wenn Sie Zugriff auf mehrere Unternehmen haben und sich diese Unternehmen in unterschiedlichen Umgebungen befinden, müssen Sie bei der Anmeldung bei [!INCLUDE[prod_short](prod_short.md)] die Umgebung angeben, in der Sie arbeiten möchten. Umgebungen sind für ein bestimmtes Land spezifisch. Wenn Ihre Organisation also in mehreren Ländern tätig ist, benötigen Sie für jedes Land separate Umgebungen.<br><br>  

Was ist ein Unternehmen? Stellen Sie sich ein *Unternehmen* als Container vor, der Informationen über eine juristische Person enthält. Im obigen Beispiel verfügt das Unternehmen über ein Verkaufsbüro in Seattle und ein weiteres in New York, daher erstellt es in [!INCLUDE[prod_short](prod_short.md)] ein Unternehmen für jedes Büro, sodass es den Betrieb für jedes Büro separat verwalten kann.  
