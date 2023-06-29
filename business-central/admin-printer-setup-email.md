---
title: E-Mail-Drucker einrichten
description: Anleitungsbeschreibung
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---
# <a name="set-up-email-printers"></a><a name="set-up-email-printers"></a>E-Mail-Drucker einrichten

In diesem Artikel wird erläutert, wie Sie E-Mail-fähige Drucker in [!INCLUDE[prod_short](includes/prod_short.md)] einrichten. Mit diesen Druckern sendet [!INCLUDE[prod_short](includes/prod_short.md)] anschließend die Druckaufträge unter Verwendung der E-Mail-Adresse des Druckers an einen Drucker.

> [!TIP]
> Informationen zu anderen Druckermöglichkeiten finden Sie unter [Übersicht über die Druckerverwaltung](admin-printer-setup-overview.md). 

## <a name="prerequisites"></a><a name="prerequisites"></a>Voraussetzungen

- [!INCLUDE[prod_short](includes/prod_short.md)] 2020 Veröffentlichungszyklus 1 oder höher
- Erweiterung **E-Mail an Drucker senden** ist installiert

    Diese Erweiterung wird standardmäßig eingerichtet. Weitere Informationen zum Installieren von Erweiterungen finden Sie unter [Installieren und Deinstallieren von Erweiterungen in Business Central](ui-extensions-install-uninstall.md).
- Die E-Mail-Funktionalität ist eingerichtet.

   Erfahren Sie mehr unter [E-Mail einrichten](admin-how-setup-email.md).

## <a name="add-an-email-printer"></a><a name="add-an-email-printer"></a>Einen E-Mail-Drucker hinzufügen

Die Seite **Druckerverwaltung** zeigt Drucker an, die derzeit eingerichtet sind. Die Seite gibt Ihnen auch Zugriff auf die Seite **Einstellungen** für jeden Drucker, um eine vorhandene Einrichtung zu bearbeiten oder einen neuen Drucker einzurichten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Druckerverwaltung** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie **E-Mail-Druck** und dann **Einen E-Mail-Drucker hinzufügen** aus.
3. Füllen Sie auf der Seite **E-Mail-Drucker-Einstellungen** die Felder wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Sie müssen das geeignete Papierformat für einen Drucker manuell auswählen, da keine lokalen Drucker- oder Benutzereinstellungen gespeichert werden können.
    >
    > Beachten Sie, dass die E-Mail-Drucker-Erweiterung standardmäßig auf **A4** Papierformat eingestellt ist, was z.B. in Nordamerika nicht geeignet ist.

## <a name="privacy-notice"></a><a name="privacy-notice"></a>Datenschutzhinweis

Wenn Sie die E-Mail-Drucker-Erweiterung verwenden, dann werden alle oder einige Druckaufträge an die E-Mail-Adresse gesendet wie bei der Konfiguration des Druckers angegeben. Wir empfehlen dringend, dass eine eindeutige E-Mail-ID an ein Druckergerät gebunden wird, das nur die offiziellen Dienste des Hardware-Herstellers nutzt, wie z.B. HP ePrint, KonicaMinolta EveryonePrint oder Epson E-Mail-Druck.

Treffen Sie alle erforderlichen Datenschutzvorkehrungen, einschließlich der Sicherstellung, dass die E-Mail-Drucklösung über ordnungsgemäß konfigurierte Berechtigungen, Datenschutzeinstellungen und Aufbewahrungsrichtlinien verfügt. Es liegt in Ihrer Verantwortung, eine korrekte, verifizierte und funktionsfähige E-Mail-Adresse anzugeben. Erfahren Sie mehr unter [Microsoft-Datenschutzbestimmungen](https://privacy.microsoft.com/privacystatement).

## <a name="next-steps"></a><a name="next-steps"></a>Nächste Schritte

[Standarddrucker einrichten](ui-specify-printer-selection-reports.md)

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Druckerverwaltung – Übersicht](admin-printer-setup-overview.md)  
[Universal Print-Drucker einrichten](admin-printer-setup-universal-print.md)
[Bericht drucken](ui-work-report.md#PrintReport)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ausführen von Stapelverarbeitungen](ui-how-run-batch-jobs.md)  
