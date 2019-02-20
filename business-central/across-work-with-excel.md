---
title: Anzeigen und Arbeit in Excel aus Business Central | Microsoft Docs
description: "Mehr erfahren, wie Sie die Finanzaufstellungen in Microsoft Excel von  Business Central für eine Analyse der Daten öffnen können."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 5d6d2d9527e81a92987f6b8fcdbe8e087c3c537a
ms.openlocfilehash: 27c137ea6309d40cddc94bc676ec7ea27d5c01fa
ms.contentlocale: de-de
ms.lasthandoff: 01/22/2019

---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Anzeigen und Arbeit in Excel aus Business Central 

Mit Seiten, die eine Liste der Datensätze in den Zeilen und Spalten anzeigen, wie eine Liste von Debitoren von Verkaufsaufträgen oder Rechnungen können Sie die Daten mithilfe von Microsoft Excel anzeigen. Dazu haben Sie zwei Optionen. Sie können entweder die **In Excel öffnen** Aktion oder die **Bearbeiten Sie in Excel** Aktion dieser Seite auswählen. Der Unterschied zwischen den beiden Methoden ist der folgende:  

## <a name="open-in-excel"></a>In Excel öffnen

-    Mit dieser Aktion berücksichtigt Excel sämtliche Filter auf der Seite, mit der die angezeigten Datensätze eingeschränkt werden. Das bedeutet, dass die Excel-Arbeitsmappe dieselben Zeilen und Spalten enthält, die auf der Seite unter [!INCLUDE[prodshort](includes/prodshort.md)] erscheinen.

-    Sie können Änderungen mit Datensätzen in Excel vornehmen, aber Sie können die Änderungen nicht auf  [!INCLUDE[prodshort](includes/prodshort.md)] veröffentlichen. Sie können die Änderungen in die Excel-Datei nur auf dem Computer speichern. 

-    Diese Aktion geht auf Windows und Mac Os. 

>[!NOTE]
>Für [!INCLUDE[prodshort](includes/prodshort.md)] lokal ist die **In Excel öffnen** Aktion nicht verfügbar, wenn die **Bearbeiten Sie in Excel** Aktion nicht verfügbar ist.

## <a name="edit-in-excel"></a>In Excel bearbeiten

-    Mit dieser Aktion berücksichtigt Excel sämtliche Filter auf der Seite, mit der die angezeigten Datensätze eingeschränkt werden. Das bedeutet, dass die Excel-Arbeitsmappe alle verfügbaren Datensätze und Spalten enthält, unabhängig davon, was auf der Seite angezeigt wird. 

-    Der Vorteil der **Bearbeiten Sie in Excel** Aktion ist, dass es Sie Änderungen mit Datensätzen in Excel vornimmt und die Änderungen zurück in [!INCLUDE[prodshort](includes/prodshort.md)] veröffentlichen können,

-    Das geht nur auf Windows; nicht Mac Os.

>[!NOTE]
>Für [!INCLUDE[prodshort](includes/prodshort.md)] lokal ist die **Bearbeiten Sie in Excel** Aktion nur verfügbar, wenn das Excel-Add-In vom Administrator speziell eingerichtet wurde. Für Administratoren wenn Sie erfahren möchten, wie das Excel-Add-In installiert wird gehen sie zu [Einrichten des Excel-Add-Ins](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

## <a name="see-also"></a>Siehe auch

[Arbeiten mit Business Central](ui-work-product.md)  

