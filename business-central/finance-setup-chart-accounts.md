---
title: Die Kontenpläne einrichten
description: Der Kontenplan zeigt die Sachkonten an, die Finanzdaten speichern. Sie können die Standardkonten im COA ändern und neue Konten hinzufügen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 506aae83d19c8b04102760017302e83d523f77e8
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "6327038"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Einrichten oder Ändern des Kontenplans

Der Kontenplan zeigt die Sachkonten an, die Finanzdaten speichern. [!INCLUDE[prod_short](includes/prod_short.md)] umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.
Sie können jedoch die Standardkonten ändern und neue Konten hinzufügen.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="adding-or-changing-accounts"></a>Hinzufügen oder Ändern von Konten

Im Kontenplan können Sie jedes Sachkonto öffnen und Einstellungen hinzufügen oder ändern. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Falls erforderlich, können Sie mehr als eine Zeile für den Namen eines Sachkontos im Hauptbuch verwenden. Wählen Sie auf der Seite **Sachkontoausweis** in der Gruppe **Konto** die Option **Erweiterte Texte**, und füllen Sie dann eine oder mehrere Zeilen mit dem zu kopierenden Text und dem Kontonamen aus.  

Für Konten des Kontotyps **Summe** müssen Sie das Feld **Summe** ausfüllen. Bei Konten vom Typ **Endsumme** wird dieses Feld automatisch von der Funktion Einrücken ausgefüllt. Nachdem Sie alle Konten festgelegt haben, wählen Sie die Aktion **Verarbeiten**, und wählen Sie dann **Kontenplan einrücken**.  

> [!IMPORTANT]
> Wenn Sie vor dem Ausführen der Funktion Einrücken Definitionen in den Feldern **Summe** für **Endsumme** Konten eingegeben haben, müssen Sie diese erneut eingeben, da die Funktion die Werte in allen **Endsumme** Feldern überschreibt.

## <a name="deleting-accounts"></a>Löschen von Konten

Sie können ein Sachkonto löschen. Bevor es gelöscht wird, müssen allerdings folgende Bedingungen erfüllt sein:  

* Der Saldo des Kontos muss Null betragen.  
* Das Feld **Löschen v. Sachkonten zul. vor** auf der Seite **Finanzbuchhaltungs-Einrichtung:** muss ausgefüllt sein, und das Konto darf keine Posten an oder nach diesem Datum enthalten.  
* Ist das Feld **Sachkontoverwendung prüfen** auf der Seite **Finanzbuchhaltungs-Einrichtung:** ausgewählt, darf dieses Konto nicht in Buchungsgruppen oder der Buchungsmatrix Einrichtung verwendet werden.  

[!INCLUDE[prod_short](includes/prod_short.md)] verhindert, dass Sie ein Sachkonto löschen, in dem Daten gespeichert werden, die im Kontenplan erforderlich sind.  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Abstimmen von Bankkonten](bank-manage-bank-accounts.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Daten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Arbeiten mit Kontenschemata](bi-how-work-account-schedule.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[GuV-Konten Nullstellung in der französischen Version](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Gewinn- und Verlustrechnungen drucken in der australischen Version](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Drucken von Gewinn- und Verlustrechnungen in der neuseeländischen Version](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Einrichten und GuV-Konten Nullstellung in der spanischen Version](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Einrücken und Validieren des Kontenplans in der spanischen Version](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]