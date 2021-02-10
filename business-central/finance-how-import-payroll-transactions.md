---
title: Lohntransaktionen importieren| Microsoft Docs
description: Um Gehalt zu verwalten, importieren Sie buchen und finanzieller Transaktionen von Ihrem Gehaltsabrechnungsanbieter auf Sach-, mithilfe einer Gehaltsabrechnungserweiterung wie Ceridian oder Quickbooks.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ca36be547224e0d401a05b63452420b88b0b7d1f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746966"
---
# <a name="import-payroll-transactions"></a>Lohntransaktionen importieren
Um Gehaltszahlungen und verwandte Transaktionen zu berücksichtigen, müssen Sie die Gehaltstransaktionen importieren und finanzielle Transaktionen buchen, die durch Ihr Gehaltsabrechnungsanbieter in die Finanzbuchhaltung gebucht werden. Dazu importieren Sie zuerst eine Datei, die Sie vom Gehaltsabrechnungsanbieter erhalten in die Seite **Fibur Buch.Blatt**. Anschließend ordnen Sie die externen Konten in der Gehaltsabrechnungsdatei den jeweiligen Sachkonten zu. Zuletzt buchen Sie die Gehaltsabrechnungstransaktionen entsprechend der Kontozuordnung.

> [!NOTE]  
>   Um diese Funktionalität nutzen zu können, muss für den Gehaltsabrechnungsimport eine Erweiterung eingerichtet und aktiviert werden. Die Ceridian-Gehaltsliste und die Quickbooks-Gehaltsabrechnungsdatei-Importerweiterungen werden in [!INCLUDE[prod_short](includes/prod_short.md)] vorinstalliert. Weitere Informationen finden Sie unter [Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe der Erweiterungen](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Um eine Lohndatei zu importieren
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Fibu Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie im relevanten Fibu Buch.-Blattname die Aktion **Gehaltsabrechnungstransaktionen importieren** aus. Ein unterstützter Einrichtungsleitfaden wird geöffnet.
3. Befolgen Sie die Schritte auf der Seite **Gehaltsabrechnungstransaktionen importieren**.

    > [!TIP]  
    >   Im Schritt zum Zuordnen der externen Lohn- und Gehaltsabrechnungsdatensätze zu den Sachkonten, erinnert sich das Programm an die Zuordnungen, die Sie erstellen, das nächste Mal, wenn dieselben Daten importiert werden. Das spart Zeit, weil Sie nicht jedes Mal manuell das Feld **Kontonr.** im Fibu Buch.-Blatt ausfüllen müssen, wenn Sie wiederkehrende Gehaltsabrechnungstransaktionen importiert haben.   

    Wenn Sie die Schaltfläche **OK** im unterstützten Einrichtungsleitfaden auswählen, wird die Seite **Fibu Buch.-Blatt** mit den Zeilen ausgefüllt, die die Transaktionen darstellen, die die Gehaltsabrechnungsdatei enthält und dabei werden die relevanten Konten in den Feldern **Sachkonto** vorausgefüllt, gemäß den Zuordnungen, die Sie im Leitfaden vorgenommen haben.
4. Bearbeiten oder buchen Sie die Buch.-Blattzeilen für andere Finanzbuchhaltungstransaktionen. Weitere Informationen finden Sie unter [Transaktionen direkt in der Finanzbuchhaltung buchen.](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen](ui-extensions.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
