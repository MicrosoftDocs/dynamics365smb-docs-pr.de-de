---
title: Den Kontenplan einrichten oder ändern (enthält ein Video)
description: 'Erfahren Sie, wie Sie Ihren Kontenplan so einrichten, dass er die Sachkonten anzeigt, die Finanzdaten speichern.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 12/19/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>Einrichten oder Ändern des Kontenplans

Der Kontenplan zeigt die Sachkonten an, die Finanzdaten speichern. [!INCLUDE[prod_short](includes/prod_short.md)] umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht. Sie können jedoch die Standardkonten ändern und neue Konten hinzufügen.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Hinzufügen oder Ändern von Konten

Im Kontenplan können Sie jedes Sachkonto öffnen und Einstellungen hinzufügen oder ändern. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

Falls erforderlich, können Sie mehr als eine Zeile für den Namen eines Sachkontos im Hauptbuch verwenden. Wählen Sie auf der Seite **Sachkontoausweis** in der Gruppe **Konto** die Option **Erweiterte Texte**, und füllen Sie dann eine oder mehrere Zeilen mit dem kopierten Text und dem Kontonamen aus.  

Für Konten des Kontotyps **Summe** müssen Sie das Feld **Summe** ausfüllen. Bei Konten vom Typ **Endsumme** wird dieses Feld automatisch von der Funktion Einrücken ausgefüllt. Nachdem Sie alle Konten festgelegt haben, wählen Sie die Aktion **Verarbeiten**, und wählen Sie dann **Kontenplan einrücken**.  

> [!IMPORTANT]
> Wenn Sie vor dem Ausführen der Funktion Einrücken Definitionen in den Feldern **Summe** für **Endsumme** Konten eingegeben haben, müssen Sie diese erneut eingeben, da die Funktion die Werte in allen **Endsumme** Feldern überschreibt.

## <a name="delete-accounts"></a>Konten löschen

Sie können ein Sachkonto löschen. Bevor es gelöscht wird, müssen allerdings folgende Bedingungen erfüllt sein:  

* Der Saldo des Kontos muss Null betragen.  
* Das Feld **Löschen v. Sachkonten zul. vor** auf der Seite **Finanzbuchhaltungs-Einrichtung:** muss ausgefüllt sein, und das Konto darf keine Posten an oder nach diesem Datum enthalten.  
* Ist das Feld **Sachkontoverwendung prüfen** auf der Seite **Finanzbuchhaltungs-Einrichtung:** ausgewählt, darf dieses Konto nicht in Buchungsgruppen oder der Buchungsmatrix-Einrichtung verwendet werden.  

[!INCLUDE[prod_short](includes/prod_short.md)] verhindert, dass Sie ein Sachkonto löschen, in dem Daten gespeichert werden, die im Kontenplan erforderlich sind.  

Sie können auch festlegen, wann jemand Konten löschen dürfen soll. Auf der Seite **Finanzbuchhaltungs-Einrichtung** sorgt der Umschalter **Löschen von Sachkonten sperren** gemeinsam mit dem Datum im Feld **Sachkontolöschung prüfen nach** für eine zusätzliche Überprüfung. Wenn Sie den Umschalter **Löschen von Sachkonten blockieren** aktivieren, können Sie keine Sachkonten löschen, deren Hauptbucheinträge nach dem Datum im Feld **Sachkontolöschung prüfen nach** liegen. Um ein solches Konto zu löschen, muss jemand mit Zugriff auf die Seite **Finanzbuchhaltungs-Einrichtung** den Umschalter **Löschen von Sachkonten blockieren** deaktivieren.  

Es hat sich bewährt, das Feld **Löschen von Sachkonten sperren** zu aktivieren und das Datum im Feld **Sachkontolöschung prüfen nach** zum Beispiel auf das Datum festzulegen, bis zu dem Sie Ihre Finanzdaten laut den Vorschriften speichern müssen.  

### <a name="video-guidance"></a>Videoanleitung

In diesem Video wird gezeigt, wie Sie festlegen, ob und wann Personen Sachkonten löschen können.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1g3oY]

## <a name="see-also"></a>Siehe auch

[Das Hauptbuch und der Kontenplan](finance-general-ledger.md)  
[Abstimmen von Bankkonten](bank-manage-bank-accounts.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Daten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Mit Finanzberichten arbeiten](bi-how-work-account-schedule.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[GuV-Konten Nullstellung in der französischen Version](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Gewinn- und Verlustrechnungen drucken in der australischen Version](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Drucken von Gewinn- und Verlustrechnungen in der neuseeländischen Version](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Einrichten und GuV-Konten Nullstellung in der spanischen Version](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Einrücken und Validieren des Kontenplans in der spanischen Version](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
