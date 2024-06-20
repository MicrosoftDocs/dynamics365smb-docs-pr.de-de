---
author: brentholtorf
ms.topic: include
ms.date: 04/01/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
[!INCLUDE[prod_short](prod_short.md)]-Benutzer unterstützen manchmal mehrere Abteilungen oder Unterorganisationen innerhalb eines Konzernmandanten. Ein Unternehmen kann beispielsweise Verkaufsbüros in verschiedenen Städten und mehreren Ländern/Regionen haben, sodass für jedes Büro eine separate Geschäftseinheit eingerichtet wurde. Die Büros, die sich im selben Land/in derselben Region befinden, werden als separate *Unternehmen* in einer gemeinsamen *Umgebung* eingerichtet. Andere Büros werden als Unternehmen in separaten Umgebungen erstellt, da sie geografisch in anderen Ländern/Regionen ansässig sind.

- Was ist ein Unternehmen?

  Stellen Sie sich ein *Unternehmen* als Container vor, der Informationen über eine juristische Person enthält. Im obigen Beispiel verfügt das Unternehmen über ein Verkaufsbüro in Seattle und ein weiteres in New York, daher erstellt es in [!INCLUDE[prod_short](prod_short.md)] ein Unternehmen für jedes Büro, sodass es den Betrieb für jedes Büro separat verwalten kann.

- Was ist eine Umgebung?

  Unternehmen in [!INCLUDE[prod_short](prod_short.md)] Online befinden sich in sogenannten *Umgebungen*. Es gibt zwei Typen von Umgebungen, **Produktion** und **Sandbox**. Kurz gesagt, Produktionsumgebungen enthalten Live-Geschäftsdaten und Sandbox-Umgebungen werden als sicherer Ort zum Testen neuer Geschäftsprozesse oder Funktionen verwendet. Weitere Informationen finden Sie unter [Umgebungstypen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments) (nur in englischer Sprache). Wenn Sie Zugriff auf ein Unternehmen haben, haben Sie auch Zugriff auf die Umgebung, in der es sich befindet. Wenn Sie Zugriff auf mehrere Unternehmen haben und sich diese Unternehmen in unterschiedlichen Umgebungen befinden, müssen Sie bei der Anmeldung bei [!INCLUDE[prod_short](prod_short.md)] die Umgebung angeben, in der Sie arbeiten möchten. Umgebungen sind für ein bestimmtes Land bzw. eine bestimmte Region spezifisch. Wenn Ihre Organisation also in mehreren Ländern/Regionen tätig ist, benötigen Sie für jedes Land/jede Region separate Umgebungen. Weitere Informationen finden Sie unter [Umgebungen und Unternehmen](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology#environments-and-companies) (nur in englischer Sprache).
