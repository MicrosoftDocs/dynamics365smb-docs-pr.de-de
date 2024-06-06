---
title: Regulatorische Warnungen übermitteln
description: 'Wenn Sie von neuen Gesetzen wissen, die die Unterstützung von Funktionen in Business Central erfordern, können Sie diese Anleitung befolgen, um eine regulatorische Warnung an das Produktteam zu senden.'
author: sorenfriisalexandersen
ms.topic: conceptual
ms.reviewer: bholtorf
ms.search.keywords: null
ms.date: 12/07/2023
ms.author: soalex
ms.service: dynamics-365-business-central
---

# <a name="submit-alerts-about-countryregion-specific-regulatory-features"></a>Warnungen zu landes-/regionsspezifischen gesetzlichen Features übermitteln

Wir laden Sie ein, Microsoft Dynamics Lifecycle Services (LCS) zu verwenden, um gesetzliche Warnungen über den Dynamics-Übermittlungsdienst für Gesetzeswarnungen zu senden.  

## <a name="to-submit-a-regulatory-alert-in-lcs"></a>So übermitteln Sie regulatorische Warnungen in LCS

1. Gehen Sie zu [Lifecycle Services](https://lcs.dynamics.com) und melden Sie sich an.  

    Es werden die Projekte angezeigt, auf die Sie Zugriff habe.

2. Wählen Sie das Projekt **Gesetzeswarnungen – weltweit** aus.

    Dies öffnet das Projekt und zeigt eine Reihe von Dingen an, die mit diesem Projekt zusammenhängen.

3. Wählen Sie **Warndienst** auf der rechten Seite im Abschnitt **Mehr Tools**.

    Sie sehen eine Liste mit Warnmeldungen mit der Überschrift **Dynamics Übermittlungsdienst für Gesetzeswarnungen**.

4. Sie können eine neue Warnung hinzufügen, indem Sie auf das Pluszeichen **(+)** am oberen Rand der Liste gehen.

    Auf diese Weise erhalten Sie eine 4-stufige Anleitung zum Erstellen der Warnung. Das Handbuch hat folgende Schritte:
    - Nach vorhandenen Elementen suchen.

        Suchen Sie nach Informationen, die für die Warnung, die Sie erstellen werden, relevant sind. Wenn Sie keine entsprechenden Suchergebnisse erhalten, können Sie die Schaltfläche **Gesetzeswarnung übermitteln** am unteren Rand der Seite auswählen, um mit der Übermittlung der Warnung fortzufahren.
    - Geschäftsprozesse anfügen.

        Dieser Teil ist für Dynamics 365 Business Central nicht relevant. Wählen Sie **Überspringen**, um zum nächsten Schritt überzugehen.
    - Die Warnung beschreiben.

        Geben Sie die Informationen über die Warnung in die entsprechenden Felder ein. Pflichtfelder werden im Handbuch mit einem roten Sternchen (\*) gekennzeichnet.

        |Feld        |Description                               |
        |-------------|------------------------------------------|
        |Titel  | Geben Sie einen beschreibenden Titel ein, um den Bereich zu identifizieren. Beispielsweise geben Sie *Änderungen am Rechnungsbeleg seit dem 1. Juli 2019* ein. |
        |Description  | Geben Sie eine kurze Übersicht des Gesetzes ein. Die Beschreibung sollte sich auf Probleme konzentrieren, die für die Unternehmensressourcenplanung (ERP) relevant sind, damit Benutzer die Anforderungen auf hoher Ebene erkennen können, ohne erst die Gesetzestexte lesen zu müssen.|
        |Land  | Geben Sie das Land bzw. die Region des Gesetzes an.|
        |Branche| Geben Sie der Branche an, wenn die Anforderung nur für bestimmte Branchen gilt. Wählen Sie beispielsweise **Öffentlicher Sektor**, **Einzelhandel** oder **Produktion** aus.|
        |Funktionsreferenz  | Dies ist für Business Central nicht relevant, aber Sie können eine Funktionsreferenz eingeben, wenn Sie sie kennen. Die Liste der Funktionen für das bestimmte Land bzw. die Region finden Sie im [Lokalisierungsportal](/dynamics/s-e/) auf der CustomerSource Seite. |
        |Strafverfolgungsdatum  | Geben Sie das Datum an, wenn betroffene Debitoren starten müssen, das Gesetz einzuhalten.|
        |Regierungsankündigungsdatum  | Geben Sie das Datum an, an dem die Behörde die Änderung angekündigt hat.|
        |Letztes Archivierungsdatum  | Wählen Sie den Stichtag für die erste Übermittlung des neuen oder geänderten Berichts aus.|
        |Link zur Gesetzgebung  | Geben Sie ein oder mehrere Links zu veröffentlichten Gesetzen, zur Interpretationsrichtlinie, zur Implementierungsrichtlinie oder zu einer anderen nützlichen Dokumentation ein, die Benutzenden hilft, die Anforderung zu verstehen oder umzusetzen.|
        |Mandantenname  | Geben Sie den Firmennamen für die Person ein, die die Warnung übermittelt.|
        |Kontaktname  | Geben Sie den Namen für die Person ein, die die Warnung übermittelt. |
        |Kontakt-E-Mail  | Die E-Mail-Adresse der Person, die die Warnung übermittelt.|
        |Geschäftsprozess  | Die Geschäftsprozesse, die Sie über den Assistenten zur **Warnungsübermittlung** ausgewählt haben|
        |Kommentare  | Geben Sie beliebige zusätzliche Informationen ein, die Benutzern helfen, die Anforderungen zu verstehen oder zu implementieren. Wählen Sie zum Speichern Ihres Kommentars **Übermitteln** aus. Mehrere Kommentare können hinzugefügt werden und sollten separat übermittelt werden. Kommentare werden in der Reihenfolge gespeichert, in der sie übermittelt werden. |
        |Anhänge  | Wählen Sie auf die Schaltfläche **Hochladen** aus und suchen Sie dann nach der Datei, die Sie als Dateianhang hinzufügen möchten. Nachdem Sie die Datei ausgewählt haben, wird sie hochgeladen und als eine verknüpfte Datei angezeigt. Sie können bis zu drei Dateien hinzufügen, die jeweils eine Größe von 5 MB haben. Um angehängte Dateien zu löschen, wählen Sie **Löschen** unter dem Titel der Datei aus. Anhänge müssen öffentlich verfügbare Materialien sein. Sie dürfen nicht Eigentum von Kundschaft oder kundenspezifisch/partnerspezifisch sein.|

        Wählen Sie **Übermitteln** aus, um die Warnung zu speichern und zu übermitteln.

        Wenn Sie nicht alle erforderlichen Informationen haben oder wenn Sie noch nicht bereit sind, die Warnung zu übermitteln, können Sie eine teilweise abgeschlossene Warnung speichern.

    - Übermittlungsbestätigung.

      Nachdem Sie die Warnung gesendet haben, erhalten Sie eine Bestätigung, dass die Warnung erfolgreich an Microsoft gesendet wurde.

## <a name="see-also"></a>Siehe auch

[Lokale Funktion in [!INCLUDE[prod_long](includes/prod_long.md)]](about-localization.md)  
[Sprache und Gebiet ändern](about-locale-language.md)  
[Bereitschaft für die Geschäftsabwicklung](ui-get-ready-business.md)  
[Willkommen zu Business Central](welcome.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
