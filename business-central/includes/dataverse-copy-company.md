---
author: brentholtorf
ms.topic: include
ms.date: 03/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

> [!NOTE]
> Wenn Sie ein Unternehmen in einer Umgebung kopieren, in der die Dataverse oder Sales-Integration aktiviert ist, löscht [!INCLUDE [prod_short](prod_short.md)] beim Kopieren in das Zielunternehmen die folgenden Einstellungen:
>
> * Dataverse- und Dynamics-Verbindungseinstellungen, um sicherzustellen, dass die Integration im Zielunternehmen korrekt erneut gestartet wird.
> * Integrationsdatensätze, um sicherzustellen, dass das Zielunternehmen nicht auf Datensätze verweist, die im Quellunternehmen gekoppelt sind.
> * Integrationssynchronisierungsaufträge, um Synchronisierungshintergrundaufträge anzuhalten.
> * Synchronisierungsfehler, sofern sie existieren, deuten auf Fehler im Quellunternehmen hin und werden im Zielunternehmen lediglich als Rauschen betrachtet.