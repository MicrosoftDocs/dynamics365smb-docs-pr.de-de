---
title: Warnungen und Fehlermeldungen
description: 'Erfahren Sie, wie Sie Fehler beheben und Lösungen für Fehlermeldungen finden können, wenn Sie in Business Central arbeiten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-temeplate
---
# Warnungen und Fehlermeldungen

Während Ihres Arbeitstages werden möglicherweise Benachrichtigungen in [!INCLUDE [prod_short](includes/prod_short.md)] angezeigt, dass zum Beispiel etwas schief gelaufen ist oder es nicht möglich war, etwas zu buchen. In vielen Fällen erleichtert die Benachrichtigung das Beheben der Angelegenheit oder das Zurücksetzen von Änderungen, die Sie vorgenommen haben. In anderen Fällen haben Sie möglicherweise die Informationen, die Sie zum Entsperren brauchen, nicht. Dieser Artikel enthält Tipps dazu, wie Sie Fortschritte erzielen können.  

## Produktinterne Benutzerunterstützung

Die Standardversion von [!INCLUDE [prod_short](includes/prod_short.md)] enthält Beschreibungen für die meisten Felder, Spalten und Aktionen, auf die bei Auswahl des Namens zugegriffen werden kann. In Kombination mit Unterrichtstipps für wichtige Seiten, beschreibenden Beschriftungen und Anweisungstexten sind diese QuickInfos oder Callouts unsere aktuelle Implementierung von *eingebetteter Benutzerunterstützung*. Dies ist ein wichtiges Prinzip in der heutigen Welt des Softwaredesigns.  

Wenn Sie eine Frage zu einem Feld oder einem anderen Element der Benutzeroberfläche haben, wählen Sie den Namen, um sich eine kurze Beschreibung anzeigen zu lassen. Wählen Sie den Link **Copilot fragen** aus, wenn das nicht genug ist. Sie können auch den produktinternen Hilfebereich verwenden, um Antworten auf Ihre Fragen zu finden.  

Weitere Informationen finden Sie unter [Dynamics 365 Business Central-Benutzerunterstützungsmodell](/dynamics365/business-central/dev-itpro/user-assistance) im Verwaltungsinhalt für [!INCLUDE [prod_short](includes/prod_short.md)].  

## Seite „Hilfe und Support“

In [!INCLUDE[prod_short](includes/prod_short.md)] gibt das Hilfemenüelement (das Fragezeichen in der oberen rechten Ecke) Ihnen Zugriff auf die Seite **Hilfe und Support** in der Sie Links zu Ressourcen finden, die Ihnen dabei helfen, Antworten auf Ihre Fragen zu finden. Weitere Informationen finden Sie unter [Ressourcen für Hilfe und Support](product-help-and-support.md).  

## Anderen helfen

Wenn Sie ein Administrator oder Superuser sind, können Sie anderen helfen, indem Sie Fehlermeldungen auf der Seite **Fehlermeldungsregister** oder im Admin Center nachschlagen. In vielen Fällen geht es bei der Warnung oder Fehlermeldung um die Einrichtung oder fehlende Berechtigung und ähnliche Probleme, bei denen der Superuser oder Administrator leicht helfen kann. In anderen Fällen müssen Sie möglicherweise die Seiten überprüfen, um die Ursache zu ermitteln. Weitere Informationen finden Sie unter [Technische Informationen finden](/dynamics365/business-central/dev-itpro/administration/manage-technical-support#finding-technical-information) im Administrationsinhalt für [!INCLUDE [prod_short](includes/prod_short.md)].  

## Fehlerdetails weitergeben, um schneller Hilfe zu erhalten

Um Hindernisse zu überwinden und Ausfallzeiten zu minimieren, nutzen Sie das Fachwissen anderer Teammitglieder oder Fachexperten bzw. Fachexpertinnen. Wenn Sie auf einen Fehler treffen, können Sie die Fehlerdetails einfach weitergeben, wenn Sie Hilfe erhalten.

Zu den Details gehören die Fehlermeldung, der Fehlercode und weitere Informationen, die bei der Fehlerbehebung hilfreich sind. Durch die Weitergabe der Fehlerdetails können Sie Ihr konkretes Problem effektiv kommunizieren, sodass Ihre Kollegschaft Ihnen leichter helfen kann.  

Sie können Details kopieren, indem Sie **Symbol „Freigeben“** in Inline-Validierungsdialogen oder im Menü **Details teilen** in Fehlerdialogen auswählen.  

Zusätzlich zum Kopieren von Fehlerdetails können Sie Details auch über Microsoft Teams durch Auswählen von **Details für Teams freigeben** freigeben, um Folgendes zu tun:

* Kopieren Sie die Fehlerdetails.
* Öffnen Sie das Fenster **Für Teams freigeben**, in dem Sie die von Ihnen kopierten Fehlerdetails einfügen und angeben können, wen Sie um Hilfe bitten möchten. [!INCLUDE [prod_short](includes/prod_short.md)] fügt einen Link zu der Seite hinzu, auf der der Fehler aufgetreten ist, um die Fehlerbehebung zu erleichtern.

Sie können die Details auch per E-Mail teilen, indem Sie auf **Details per E-Mail teilen** klicken, um Folgendes zu tun:

* Kopieren Sie die Fehlerdetails.
* Öffnen Sie Ihren Standard-E-Mail-Editor, in dem Sie die von Ihnen kopierten Fehlerdetails einfügen und angeben können, wen Sie um Hilfe bitten möchten. [!INCLUDE [prod_short](includes/prod_short.md)] fügt einen Link zu der Seite hinzu, auf der Sie Ihr Erlebnis hatten.

## Sich selbst helfen

Fehlermeldungen liefern Informationen und Aktionen, mit denen Fehler, die von der Plattform ausgehen, leichter verstanden, gefunden und behoben werden können.

Die Fehlermeldungen, die die [!INCLUDE [prod_short](includes/prod_short.md)]-Plattform generiert, enthalten die vollständigen technischen Details, einschließlich Feldnamen, im Abschnitt **Detaillierte Fehlermeldung**. Wählen Sie das Symbol **Details kopieren** bei Inline-Validierungsfehlern oder in einer Fehlermeldung aus, um auf die technischen Informationen zuzugreifen.

Aktionen zu Fehlermeldungen führen Sie direkt zu der Seite, auf der ein Feld den Fehler verursacht. Sie müssen sich nicht die Zeit nehmen, die Seite oder das Feld selbst zu suchen. Um den Fehler zu beheben, wählen Sie einfach die Aktion in der Fehlermeldung aus und [!INCLUDE [prod_short](includes/prod_short.md)] führt Sie zur richtigen Stelle.

Im folgenden Video wird gezeigt, wie Sie die Blockierung mithilfe umsetzbarer Fehlermeldungen aufheben.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1l2sM]

### Tipp für Entwickelnde

Wenn Sie Entwicklungsfachkraft sind und die Methode [TestField](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-testfield-joker-joker-errorinfo-method) aufrufen und das |`ErrorInfo`-Objekt nicht übergeben, generiert [!INCLUDE [prod_short](includes/prod_short.md)] automatisch den Link zu einer Seite, auf der Benutzende das Problem beheben können. [!INCLUDE [prod_short](includes/prod_short.md)] ruft zunächst die Nachschlage- oder Drilldown-Seite für den Datensatz ab, sucht dann die Kartenseite oder Nachschlageseite und fügt dieser Kartenseite einen Navigationslink hinzu. [!INCLUDE [prod_short](includes/prod_short.md)] fügt in den folgenden Situationen keinen Link hinzu:

* Wenn der Fehler auf der aktuell geöffneten Seite auftritt.
* Wenn der Benutzende nicht über die Berechtigungen zum Ändern des zugrunde liegenden Datensatzes verfügt.

## Siehe auch

[Ressourcen für Hilfe und Support](product-help-and-support.md)  
[Häufig gestellte Fragen](across-faq.yml)  
[Häufig gestellte Fragen zu „Wie möchten Sie weiter verfahren“](ui-search-faq.md)  
[Suchen und Filtern FAQ](ui-search-filter-faq.yml)  
[Kopieren und einfügen FAQ](faq-copy-paste.yml)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]