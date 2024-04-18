---
author: brentholtorf
ms.topic: include
ms.date: 04/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

## Bewährte Methoden für die Arbeit mit Spaltendefinition

Spaltendefinition sind nicht versioniert. Wenn Sie eine Spaltendefinition ändern, wird die alte Version ersetzt, wenn Ihre Änderung in der Datenbank gespeichert wird. Die folgende Liste enthält einige bewährte Vorgehensweisen für die Arbeit mit Spaltendefinition:

- Wenn Sie eine Spaltendefinition hinzufügen, wählen Sie einen guten Code und geben Sie im Beschreibungsfeld einen aussagekräftigen Text ein, solange Sie noch wissen, wofür Sie die Spaltendefinition verwenden. Diese Informationen helfen Ihren Mitarbeitenden (und Ihnen selbst in der Zukunft) bei der Arbeit mit Finanzberichten und falls notwendig beim Ändern der Spaltendefinition.
- Bevor Sie eine Spaltendefinition ändern, sollten Sie eine Sicherungskopie davon erstellen, für den Fall, dass die Änderung nicht wie erwartet funktioniert. Sie können die Definition entweder einfach kopieren (geben Sie ihr einen guten Namen) oder exportieren. Mehr erfahren Sie unter [Spaltendefinitionen importieren oder exportieren](#import-or-export-financial-report-column-definitions).
- Wenn Sie eine neue Kopie einer Definition benötigen, die [!INCLUDE [prod_short](prod_short.md)] bereitstellt, erhalten Sie diese ganz einfach, indem Sie ein neues Unternehmen erstellen, das nur die Einrichtungsdaten enthält. Exportieren Sie dann die Definition und importieren Sie sie in das Unternehmen, wo die Definition aktualisiert werden muss.