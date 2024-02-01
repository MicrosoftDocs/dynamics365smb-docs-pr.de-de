---
author: brentholtorf
ms.topic: include
ms.date: 05/30/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Wenn Sie Benutzer für Genehmigungsworkflows einrichten, ist es wichtig, dass derselbe Benutzer nicht sowohl Anforderer als auch Genehmiger in einer Workflow-Benutzergruppe ist. Wenn ein Benutzer sowohl Anforderer als auch Genehmiger ist, funktionieren Genehmigungen für ihn wie folgt:

* Seine Anforderungen werden immer automatisch genehmigt.
* Wenn es mehrere Genehmiger gibt, können nur die Genehmiger mit einer höheren Sequenznummer in der Workflow-Benutzergruppe den Status einer Anforderung in „Genehmigt“ ändern. Genehmiger mit einer niedrigeren Sequenznummer können Anforderung genehmigen, ihre Genehmigungen haben jedoch keinen Einfluss auf den Status einer Anforderung.