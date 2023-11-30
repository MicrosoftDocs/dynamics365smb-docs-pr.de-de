---
title: E-Belege einrichten
description: 'Erfahren Sie, wie Sie die Funktionalität für E-Belege einrichten.'
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 10/05/2023
ms.author: altotovi
---

# <a name="set-up-e-documents"></a>E-Belege einrichten

> [!IMPORTANT]
> Das E-Beleg-Kernmodul ist ein Framework. Standardmäßig gibt es kein Feld **Belegformat** oder **Belegintegration**. Diese Details gehören zu Lokalisierungs-Apps, da sie beide spezifisch für lokale Anforderungen sind.

> [!NOTE]
> Ab Version 23.1 wird ein Standard-PEPPOL-Belegformat als globales Format im Format **Belegformat** hinzugefügt.

Der erste Schritt bei der Konfiguration elektronischer Belege (E-Beleg) besteht in der Einrichtung des E-Beleg-Dienstes, in dem Sie das gesamte Verhalten Ihres Systems in Bezug auf die E-Beleg-Kommunikation konfigurieren.

## <a name="set-up-the-e-document-service"></a>Den E-Beleg-Dienst einrichten

Gehen Sie wie folgt vor, um den E-Beleg-Dienst einzurichten.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol aus. Geben Sie **E-Belegdienste** ein und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie **Neu** und dann auf der Seite **E-Belegdienst** auf dem Inforegister **Allgemein** die Felder wie in der folgenden Tabelle beschrieben aus.

    | Feld | Description |
    |-------|-------------|
    | Code | Wählen Sie den Einrichtungscode für den elektronischen Beleg aus. |
    | Description | Geben Sie eine kurze Beschreibung für die Einrichtung des elektronischen Exports an. |
    | Belegformat | <p>Das Exportformat für die Einrichtung des elektronischen Exports.</p><p>Standardmäßig gibt es in diesem Feld in Zyklus 1 keine Optionen.</p> |
    | Dienstintegration | Wählen Sie den Integrationscode für die Einrichtung des elektronischen Exports aus. In Zyklus 1 ist die einzige Option **Keine Integration**. |
    | Stapelverarbeitung verwenden | Geben Sie an, ob der Dienst für den Export die Stapelverarbeitung verwendet. |

4. Konfigurieren Sie auf dem Inforegister **Importierte Parameter** die in der folgenden Tabelle beschriebenen Felder.

    | Feld | Description |
    |-------|-------------|
    | Empfangendes Unternehmen überprüfen | Geben Sie an, ob eingehende Unternehmensinformationen während des Imports überprüft werden müssen. |
    | Einheit auflösen | Geben Sie an, ob die Einheit während des Imports aufgelöst werden soll. |
    | Artikelreferenz nachschlagen | Geben Sie an, ob ein Artikel während des Imports anhand der Artikelreferenz gesucht werden soll. |
    | Artikel-GTIN suchen | Geben Sie an, ob ein Artikel während des Imports anhand der Global Trade Item Number (GTIN) gesucht werden soll. |
    | Kontozuordnung nachschlagen | Geben Sie an, ob während des Imports ein Konto anhand des eingehenden Textes in der **Kontozuordnung** gesucht werden soll. |
    | Zeilenrabatt überprüfen | Geben Sie an, ob während des Imports ein Zeilenrabatt überprüft werden soll. |
    | Rechnungsrabatt anwenden | Geben Sie an, ob während des Imports ein Rechnungsrabatt angewendet werden soll. |
    | Summen überprüfen | Geben Sie an, ob während des Imports eine Rechnungssumme überprüft werden soll. |
    | Auftrag aktualisieren | Geben Sie an, ob die entsprechende Bestellung aktualisiert werden muss. |
    | Buch.-Blattzeilen erstellen | Geben Sie an, ob anstelle eines Einkaufsbelegs eine Buchungsblattzeile erstellt werden muss. Wählen Sie diese Option, wenn Sie Buchungsblätter als Ziel für Ihre Rechnungen verwenden möchten. |
    | Fibu Buch.-Blattvorlagenname | Geben Sie den Namen der Fibu Buch.-Blattvorlage an, der für die Erstellung der Buchungsblattzeile verwendet wird. Dieses Feld gilt, wenn Sie Buchungsblätter als Ziel für Ihre Rechnungen verwenden möchten. |
    | Fibu Buch.-Blattname | Geben Sie den Namen des Fibu Buch.-Blatts an, der für die Erstellung der Buchungsblattzeile verwendet wird. Dieses Feld gilt, wenn Sie Buchungsblätter als Ziel für Ihre Rechnungen verwenden möchten. |
    | Automatischer Import | Geben Sie an, ob Belege automatisch aus dem Dienst importiert werden sollen. |
    | Stapel-Startzeit | Geben Sie die Startzeit für Importaufträge an. |
    | Minuten zwischen Ausführungen | Geben Sie die Anzahl der Minuten zwischen den Ausführungen von Importaufträgen an. |

Wenn Sie das **Datenaustauschdefinition**-Format in Ihrer Lokalisierung konfiguriert haben, können Sie für jeden Belegtyp, den Sie benötigen, eine Zeile hinzufügen. Sie müssen jedoch zuerst die Option **Belegtyp** für jede Zeile, die Sie benötigen, auswählen. Wählen Sie für jeden Datentyp die Werte **Datenaustauschdefinitionscode importieren** oder **Datenaustauschdefinitionscode exportieren**, die Sie verwenden möchten.

Wenn Sie das Format **Datenaustauschdefinition** nicht verwenden, können Sie schließlich Formate über die Zeilen **Zuordnung exportieren** und **Zuordnung importieren** konfigurieren, in denen Sie die zu verwendenden Tabellen und Felder finden und ggf. Transformationsregeln konfigurieren können.

## <a name="set-up-a-document-sending-profile"></a>Ein Belegsendeprofil einrichten

Sie können für jeden Debitor eine bevorzugte Methode zum Senden von Verkaufsbelegen einrichten. so müssen Sie nicht jedes Mal eine Sendeoption auswählen, wenn Sie die Aktion **Buchen und senden** auswählen. Auf der Seite **Belegsendeprofile** können Sie verschiedene Sendeprofile einrichten und dann Ihre Auswahl aus den **Belegsendeprofilen** auf der Debitorenkarte treffen. Im Kontrollkästchen **Standard** können Sie auswählen, dass das Belegsendeprofil das Standardprofil für alle Debitoren gilt, außer Debitoren, bei denen das Feld **Belegsendeprofil** auf ein anderes Sendeprofil eingestellt ist.

Diese Funktionalität wird zum Einrichten der Automatisierung der elektronischen Fakturierung verwendet. Wenn Sie die Schaltfläche **Buchen und senden** für einen Verkaufsbeleg auswählen, wird im Dialogfeld **Buchungs- und Sendebestätigung** das verwendete Sendeprofil angezeigt: entweder das für den Debitor eingerichtete oder Standardprofil für alle Debitoren.

Gehen Sie wie folgt vor, um ein Belegsendeprofil einzurichten.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Belegsendeprofil** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Dokumentsendeprofile** **Neu** aus.
3. Geben Sie auf dem Inforegister **Allgemein** alle erforderlichen Feldinformationen ein.
4. Konfigurieren Sie im Inforegister **Sendeoptionen** die Felder gemäß der Beschreibung in der folgenden Tabelle.

    | Feld | Description |
    |-------|-------------|
    | Elektronischer Beleg | Geben Sie an, ob dieser Beleg als E-Beleg gesendet wird, den der Debitor in sein System importieren kann, wenn Sie die Schaltfläche **Buchen und senden** auswählen. Um diese Option zu verwenden, müssen Sie auch das Feld **Format** oder **Serviceflowcode für elektronischen Beleg** festlegen. Alternativ kann die Datei auf einem Datenträger gespeichert werden. |
    | Format | Geben Sie das Format an, das zum Senden eines E-Belegs verwendet werden soll. Wenn Sie **Über Belegaustauschdienst** im Feld **Elektronischer Beleg** auswählen, handelt es sich hierbei um ein Pflichtfeld. |
    | Serviceflowcode für elektronischen Beleg | Geben Sie den elektronischen Serviceflow an, der zum Senden von Belegen verwendet wird. Wenn Sie **Erweiterter E-Beleg-Serviceflow** im Feld **Elektronischer Beleg** auswählen, handelt es sich hierbei um ein Pflichtfeld. |

    > [!NOTE]
    > Wenn Sie **Erweiterter E-Beleg-Serviceflow** im Feld **Elektronischer Beleg** auswählen, muss der Workflow bereits für Ihre E-Belege konfiguriert sein.

## <a name="set-up-the-workflow"></a>Den Workflow einrichten

Gehen Sie wie folgt vor, um den Workflow einzurichten, der in der E-Beleg-Funktionalität verwendet wird.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Workflowvorlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wenn Sie **Workflow-Vorlagen für E-Belege** auf der Seite **Workflow-Vorlagen** nicht finden können, wählen Sie **Microsoft-Vorlagen zurücksetzen**. **Workflow-Vorlagen für E-Belege** sollte dann erscheinen. Schließen Sie die Seite.
3. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Workflows** ein und wählen Sie dann den entsprechenden Link.
4. Führen Sie die Aktion **Neuen Workflow aus Vorlage** aus, um eine Vorlage für den E-Beleg-Prozess auszuwählen. Die verfügbaren Vorlagen sind **An einen Dienst senden** und **An mehrere Dienste senden**.
5. Wählen Sie **OK**, um die Einrichtung des Workflows abzuschließen.
6. Wählen Sie im Feld **Dann Antwort** **E-Beleg mit Einrichtung senden** aus, um die Workflowreaktionen zu konfigurieren.
7. Wählen Sie den von Ihnen erstellten E-Beleg-Dienst als Option aus, wählen Sie **OK** und aktivieren Sie dann den Workflow.

> [!NOTE]
> Sie können Ihren eigenen Workflow für E-Belege erstellen, ohne vordefinierte Workflow-Vorlagen zu verwenden. Wenn Sie mehr Dienste haben, können Sie unterschiedliche Workflows nutzen.

## <a name="set-up-a-retention-policy-for-e-documents"></a>Richten Sie eine Aufbewahrungsrichtlinie für E-Belege ein

E-Belege können im Hinblick darauf, wie lange die E-Belege aufbewahrt werden müssen, verschiedenen lokalen Gesetzen unterliegen. Aus diesem Grund haben wir eine Aufbewahrungsrichtlinie für alle wichtigen Informationen im Zusammenhang mit E-Belegen hinzugefügt. Administrierende können Aufbewahrungsrichtlinien festlegen, die bestimmen, wie häufig Dynamics 365 Business Central veraltete Datensätze im Zusammenhang mit E-Belegen gelöscht werden. Weitere Informationen zu Aufbewahrungsrichtlinien finden Sie unter [Aufbewahrungsrichtlinien definieren](admin-data-retention-policies.md).

Führen Sie die folgenden Schritte aus, um Aufbewahrungsrichtlinien für E-Belege einzurichten.

1. Führen Sie auf der Seite **E-Belegdienste** die Aktion **Aufbewahrungsrichtlinie** aus.
2. Wenn die Aktion abgeschlossen ist, wählen Sie eine der folgenden Aufbewahrungsrichtlinien zum Einrichten aus:

    - E-Beleg-Protokoll
    - Integrationsprotokoll für E-Belege
    - E-Beleg-Zuordnungsprotokoll
    - E-Beleg-Datenspeicherung

## <a name="see-also"></a>Siehe auch

[E-Belege in Business Central verwenden](finance-how-use-edocuments.md)  
[E-Belege in Business Central erweitern](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Finanzmanagement](finance.md)  
[Verkäufe fakturieren](sales-how-invoice-sales.md)  
[Käufe mit Einkaufsrechnungen und Aufträgen erfassen](purchasing-how-record-purchases.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]