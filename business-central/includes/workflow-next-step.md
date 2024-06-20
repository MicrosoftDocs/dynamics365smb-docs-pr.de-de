---
author: brentholtorf
ms.topic: include
ms.date: 03/27/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

> [!IMPORTANT]
> Wenn Sie das „Wenn“-Ereignis für einen Workflowschritt ändern, ändern sich auch die „Dann“-Antworten. Manchmal verweisen „Dann“-Antworten anderer „Wenn“-Ereignisse auf diese „Dann“-Antworten als nächsten Schritt im Workflow. Nachdem Sie ein „Wenn“-Ereignis geändert haben, überprüfen Sie, ob die nächsten Schritte für seine „Dann“-Ereignisse korrekt sind.  
>
> Beispielsweise verfügt die Workflow-Vorlage **Kreditoren-Genehmigungsworkflow** über ein primäres „Wenn“-Ereignis: **Die Genehmigung für einen Kreditor wird angefordert**. Dieses „Wenn“-Ereignis hat eine **Senden Sie eine Genehmigungsanfrage für den Datensatz und erstellen Sie eine Benachrichtigung**-„Dann“-Antwort, die auf etwas anderes als Antworten verweist. Wenn Sie das primäre **Die Genehmigung für einen Kreditor wird angefordert**-„Wenn“-Ereignis zum Beispiel in **Ein Kreditorendatensatz wird geändert** ändern, wird die Antwort dann zusammen mit den Referenzen gelöscht.
>
> Die „Dann“-Antworten für die „Wenn“-Ereignisse **Eine Genehmigungsanfrage wird delegiert** und **Ein Genehmigungsantrag wird genehmigt** (mit dem **Bei Bedingung** von **Ausstehende Genehmigungen >0**) sind Beispiele dafür, bei denen das Ändern eines primären „Wenn“-Ereignisses Probleme verursachen kann. Ihre „Dann“-Antworten haben einen nächsten Schritt, der sich auf die „Dann“-Antwort **Senden Sie eine Genehmigungsanfrage für den Datensatz und erstellen Sie eine Benachrichtigung** des „Wenn“-Ereignisses **Die Genehmigung für einen Kreditor wird angefordert**. Da die „Dann“-Antwort für das „Wenn“-Ereignis **Die Genehmigung für einen Kreditor wird angefordert** nicht mehr verfügbar ist, funktionieren die eingerückten „Wenn“-Ereignisse nicht wie erwartet.
>
> Sie müssen die nächsten Schritte für die „Dann“-Antworten für „Wenn“-Ereignisse angeben, die sich auf das geänderte „Wenn“-Ereignis beziehen.