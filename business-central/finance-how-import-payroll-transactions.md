---
title: Importieren von Lohn- und Gehaltsabrechnungen
description: 'Um das Gehalt zu verwalten, importieren und buchen Sie finanzielle Transaktionen von Ihrem Gehaltsabrechnungsanbieter in das Hauptbuch, indem Sie eine Gehaltsabrechnungserweiterung wie Ceridian verwenden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Ceridian, Quickbooks, salary'
ms.search.form: '1660, 1661, 36601'
ms.date: 08/09/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="import-payroll-transactions"></a>Importieren von Lohn- und Gehaltsabrechnungen

Um Gehaltszahlungen und verwandte Transaktionen zu berücksichtigen, müssen Sie die Gehaltstransaktionen importieren und finanzielle Transaktionen buchen, die durch Ihr Gehaltsabrechnungsanbieter in die Finanzbuchhaltung gebucht werden. Dazu importieren Sie zuerst eine Datei, die Sie vom Gehaltsabrechnungsanbieter erhalten in die Seite **Fibur Buch.Blatt**. Anschließend ordnen Sie die externen Konten in der Gehaltsabrechnungsdatei den jeweiligen Sachkonten zu. Zuletzt buchen Sie die Gehaltsabrechnungstransaktionen entsprechend der Kontozuordnung.

> [!NOTE]  
> Um diese Funktionalität nutzen zu können, muss für den Gehaltsabrechnungsimport eine Erweiterung eingerichtet und aktiviert werden. Die Ceridian-Gehaltsliste und die Quickbooks-Gehaltsabrechnungsdatei-Importerweiterungen werden in [!INCLUDE[prod_short](includes/prod_short.md)] vorinstalliert. Weitere Informationen finden Sie unter [Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe der Erweiterungen](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Um eine Lohndatei zu importieren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Allgemeine Erfassungen** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie im relevanten Fibu Buch.-Blattname die Aktion **Gehaltsabrechnungstransaktionen importieren** aus. Ein unterstützter Einrichtungsleitfaden wird geöffnet.
3. Befolgen Sie die Schritte auf der Seite **Gehaltsabrechnungstransaktionen importieren**.

    > [!TIP]  
    >   Im Schritt zum Zuordnen der externen Lohn- und Gehaltsabrechnungsdatensätze zu den Sachkonten, erinnert sich das Programm an die Zuordnungen, die Sie erstellen, das nächste Mal, wenn dieselben Daten importiert werden. Das spart Zeit, weil Sie nicht jedes Mal manuell das Feld **Kontonr.** im Fibu Buch.-Blatt ausfüllen müssen, wenn Sie wiederkehrende Gehaltsabrechnungstransaktionen importiert haben.   

    Wenn Sie die Schaltfläche **OK** im unterstützten Einrichtungsleitfaden auswählen, wird die Seite **Fibu Buch.-Blatt** mit den Zeilen ausgefüllt, die die Transaktionen darstellen, die die Gehaltsabrechnungsdatei enthält und dabei werden die relevanten Konten in den Feldern **Sachkonto** vorausgefüllt, gemäß den Zuordnungen, die Sie im Leitfaden vorgenommen haben.
4. Bearbeiten oder buchen Sie die Buch.-Blattzeilen für andere Finanzbuchhaltungstransaktionen. Weitere Informationen finden Sie unter [Transaktionen direkt in der Finanzbuchhaltung buchen](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Siehe auch

[Finanzen](finance.md)    
[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen](ui-extensions.md)    
[Mit Fibu Buch.-Blättern arbeiten](ui-work-general-journals.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
