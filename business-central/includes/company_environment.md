---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 77a6d87d56475aa9e649ece545764f3f362d055b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914489"
---
Personen unterstützen manchmal mehrere Unternehmen und müssen in [!INCLUDE [prodshort](prodshort.md)] problemlos zwischen Unternehmen wechseln. Ein Unternehmen kann beispielsweise Verkaufsbüros in Städten und mehreren Ländern haben, sodass für jedes Büro eine separate Geschäftseinheit eingerichtet wurde. Die Büros, die sich im selben Land befinden, werden als separate Unternehmen in einer gemeinsamen Umgebung eingerichtet. Andere Büros werden als Unternehmen in separaten Umgebungen erstellt, da sie geografisch in anderen Ländern ansässig sind.  

Was ist eine Umgebung? Unternehmen in [!INCLUDE[prodshort](prodshort.md)] befinden sich in sogenannten *Umgebungen* . Es gibt zwei Typen von Umgebungen, **Produktion** und **Sandbox** . Kurz gesagt, Produktionsumgebungen enthalten Live-Geschäftsdaten und Sandbox-Umgebungen werden als sicherer Ort zum Testen neuer Geschäftsprozesse oder Funktionen verwendet. Weitere Informationen finden Sie unter [Umgebungstypen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments). Wenn Sie Zugriff auf ein Unternehmen haben, haben Sie auch Zugriff auf die Umgebung, in der es sich befindet. Wenn Sie Zugriff auf mehrere Unternehmen haben und sich diese Unternehmen in unterschiedlichen Umgebungen befinden, müssen Sie bei der Anmeldung bei [!INCLUDE[prodshort](prodshort.md)] die Umgebung angeben, in der Sie arbeiten möchten. Umgebungen sind für ein bestimmtes Land spezifisch. Wenn Ihre Organisation also in mehreren Ländern tätig ist, benötigen Sie für jedes Land separate Umgebungen.  

Was ist ein Unternehmen? Stellen Sie sich ein *Unternehmen* als Container vor, der Informationen über eine juristische Person enthält. Im obigen Beispiel verfügt das Unternehmen über ein Verkaufsbüro in Seattle und ein weiteres in New York, daher erstellt es in [!INCLUDE[prodshort](prodshort.md)] ein Unternehmen für jedes Büro, sodass es den Betrieb für jedes Büro separat verwalten kann.  
