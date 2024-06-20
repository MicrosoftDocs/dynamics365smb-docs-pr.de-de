---
title: E-Belege einrichten
description: 'Erfahren Sie, wie Sie die Funktionalität für E-Belege einrichten.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 05/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# E-Belege einrichten

> [!IMPORTANT]
> Das E-Beleg-Kernmodul ist ein Framework. Standardmäßig gibt es kein Feld **Dienstintegration**. Wenn Sie standardmäßig die **Belegformat**-Optionen finden, beachten Sie, dass diese als Beispiel angeboten werden und dass die Lokalisierung ein detailliertes Format bereitstellen muss. Diese Details gehören zu Lokalisierungs-Apps, da sie für lokale Anforderungen spezifisch sind.

> [!NOTE]
> Ab Version 23.2 wird ein Standard-PEPPOL-Belegformat als globales Format im Format **Belegformat** hinzugefügt. Bedenken Sie, dass Sie dieses Format wahrscheinlich nicht so verwenden können, wie es ist. Es handelt sich um ein W1-Format, das bereitgestellt wird, um die Verwendung dieses Features zu veranschaulichen. Wir empfehlen Ihnen, das vorhandene PEPPOL-Format zu testen, bevor Sie mit der Verwendung dieses Formats beginnen.

Der erste Schritt bei der Konfiguration elektronischer Belege (E-Beleg) besteht in der Einrichtung des E-Beleg-Dienstes, in dem Sie das gesamte Verhalten Ihres Systems in Bezug auf die E-Beleg-Kommunikation konfigurieren.

## Den E-Belegdienst einrichten

Gehen Sie wie folgt vor, um den E-Beleg-Dienst einzurichten.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol aus. Geben Sie **E-Belegdienste** ein und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie **Neu** und dann auf der Seite **E-Belegdienste** auf dem Inforegister **Allgemein** die Felder wie in der folgenden Tabelle beschrieben aus.

    | Feld | Beschreibung |
    |-------|-------------|
    | Code | Wählen Sie den Einrichtungscode für den elektronischen Beleg aus. |
    | Beschreibung | Geben Sie eine kurze Beschreibung für die Einrichtung des elektronischen Exports an. |
    | Belegformat | <p>Das Exportformat für die Einrichtung des elektronischen Exports.</p><p>Standardmäßig gibt es in diesem Feld zwei Optionen. Sie können **PEPPOL BIS 3** als generisches codebasiertes Format oder **Datenaustausch** wählen, wenn Sie Vorabdokumente bestimmter Formate im Inforegister **Datenaustauschdefinition** einrichten müssen.</p> |
    | Dienstintegration | Wählen Sie den Integrationscode für die Einrichtung des elektronischen Exports aus. In Zyklus 1 ist die einzige Option **Keine Integration**. |
    | Stapelverarbeitung verwenden | Geben Sie an, ob der Dienst für den Export die Stapelverarbeitung verwendet. |

3. Konfigurieren Sie auf dem Inforegister **Importierte Parameter** die in der folgenden Tabelle beschriebenen Felder.

    | Feld | Beschreibung |
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

4. Wenn Sie **Datenaustausch** im Feld **Dokumentformat** im Inforegister **Allgemein** ausgewählt haben, verwenden Sie das Inforegister **Datenaustauschdefinition**, um die folgenden Felder festzulegen.

    | Feld | Beschreibung |
    |-------|-------------|
    | Belegtyp | Geben Sie den Belegtyp an, der den Datenaustausch zum Importieren und Exportieren der Daten verwendet. Beispiele hierfür sind **Verkaufsrechnung**, **Verkaufsgutschrift** und **Einkaufsrechnung**. |
    | Datenaustausch-Definitionscode importieren | Geben Sie den Datenaustauschcode an, der zum Importieren der Daten verwendet wird. Nutzen Sie dieses Feld nur, um im Kaufprozess einen Beleg zu erhalten. |
    | Datenaustausch-Definitionscode exportieren | Geben Sie den Datenaustauschcode an, der zum Exportieren der Daten verwendet wird. Verwenden Sie dieses Feld nur, um Belege im Verkaufsprozess zu liefern. |

> [!NOTE]
> Es gibt vorbereitete Datenaustauschdefinitionen für das PEPPOL-Format, die sich auf den Standardverkaufs- und Einkaufsbeleg beziehen. Allerdings können Sie diese Definitionen wahrscheinlich nicht so verwenden, wie sie sind. Es handelt sich dabei ausschließlich um W1-Formate, die bereitgestellt werden, um die Verwendung dieses Features zu veranschaulichen. Wir empfehlen Ihnen, das vorhandene PEPPOL-Format zu testen, bevor Sie mit ihrer Verwendung beginnen.

Wenn Sie das **Datenaustauschdefinition**-Format in Ihrer Lokalisierung konfiguriert haben, können Sie für jeden Belegtyp, den Sie benötigen, eine Zeile hinzufügen. Fügen Sie Zeilen hinzu, die dem Standarddatenaustauschbeispiel für das W1-PEPPOL-Format entsprechen. Wählen Sie jedoch zuerst die Option **Belegtyp** für jede Zeile aus, die Sie benötigen. Wählen Sie für jeden Datentyp die Werte **Datenaustauschdefinitionscode importieren** oder **Datenaustauschdefinitionscode exportieren**, die Sie verwenden möchten.

Wenn Sie das Format **Datenaustauschdefinition** nicht verwenden, können Sie Formate mithilfe der [Schnittstelle](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments) erstellen und konfigurieren. Passen Sie die Informationen in den Zeilen **Exportzuordnung** und **Importzuordnung** an, in denen Sie die Tabellen und Felder zur Konfiguration von Transformationsregeln finden. In diesem Fall müssen Sie im Feld **Dokumentformat** eine neue Option hinzufügen, die sich auf Ihr Format bezieht.  

### Unterstützte Belegtypen 

Unterstützte Dokumenttypen basieren auf dem ausgewählten **Belegformat**. Um zu überprüfen, welche Belegtypen unterstützt werden, wählen Sie auf der Seite **E-Belegdienste** die Aktion **Unterstützte Belegtypen** aus. Die **Unterstützten Quellbelegtypen des E-Belegdienstes** öffnen sich und in der Spalte **Quellbelegtyp** können Sie verschiedene Belegtypen auswählen, um Sie für das Format, dass Sie verwenden möchten, als unterstützt festzulegen. Stellen Sie sicher, dass Sie den Belegtyp nicht verwenden, wenn dieser Beleg auf dieser Seite nicht ausgewählt ist.   

## Ein Belegsendeprofil einrichten

Sie können für jeden Debitor eine bevorzugte Methode zum Senden von Verkaufsbelegen einrichten. So müssen Sie nicht jedes Mal eine Sendeoption auswählen, wenn Sie die Aktion **Buchen und senden** auswählen. Auf der Seite **Belegsendeprofile** können Sie verschiedene Sendeprofile einrichten und dann Ihre Auswahl aus den **Belegsendeprofilen** auf der Debitorenkarte treffen. Im Kontrollkästchen **Standard** können Sie auswählen, dass das Belegsendeprofil das Standardprofil für alle Debitoren gilt, außer Debitoren, bei denen das Feld **Belegsendeprofil** auf ein anderes Sendeprofil eingestellt ist.

Diese Funktionalität wird zum Einrichten der Automatisierung der elektronischen Fakturierung verwendet. Wenn Sie die Schaltfläche **Buchen und senden** für einen Verkaufsbeleg auswählen, wird im Dialogfeld **Buchungs- und Sendebestätigung** das verwendete Sendeprofil angezeigt: entweder das für den Debitor eingerichtete oder das Standardprofil für alle Debitoren.

Gehen Sie wie folgt vor, um ein Belegsendeprofil einzurichten.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Belegsendeprofil** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Dokumentsendeprofile** **Neu** aus.
3. Geben Sie auf dem Inforegister **Allgemein** alle erforderlichen Feldinformationen ein.
4. Konfigurieren Sie im Inforegister **Sendeoptionen** die Felder gemäß der Beschreibung in der folgenden Tabelle.

    | Feld | Beschreibung |
    |-------|-------------|
    | Elektronischer Beleg | Geben Sie an, ob dieser Beleg als E-Beleg gesendet wird, den der Debitor in sein System importieren kann, wenn Sie die Schaltfläche **Buchen und senden** auswählen. Um diese Option zu verwenden, müssen Sie auch das Feld **Format** oder **Serviceflowcode für elektronischen Beleg** festlegen. Alternativ kann die Datei auf einem Datenträger gespeichert werden. |
    | Format | Geben Sie das Format an, das zum Senden eines E-Belegs verwendet werden soll. Wenn Sie **Über Belegaustauschdienst** im Feld **Elektronischer Beleg** auswählen, handelt es sich hierbei um ein Pflichtfeld. |
    | Serviceflowcode für elektronischen Beleg | Geben Sie den elektronischen Serviceflow an, der zum Senden von Belegen verwendet wird. Wenn Sie **Erweiterter E-Beleg-Serviceflow** im Feld **Elektronischer Beleg** auswählen, handelt es sich hierbei um ein Pflichtfeld. |

    > [!NOTE]
    > Wenn Sie **Erweiterter E-Beleg-Serviceflow** im Feld **Elektronischer Beleg** auswählen, muss der Workflow bereits für Ihre E-Belege konfiguriert sein.

## Den Workflow einrichten

Gehen Sie wie folgt vor, um den Workflow einzurichten, der in der E-Beleg-Funktionalität verwendet wird.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Workflowvorlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wenn Sie **Workflow-Vorlagen für E-Belege** auf der Seite **Workflow-Vorlagen** nicht finden können, wählen Sie **Microsoft-Vorlagen zurücksetzen**. **Workflow-Vorlagen für E-Belege** sollte dann erscheinen. Schließen Sie die Seite.
3. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Workflows** ein und wählen Sie dann den entsprechenden Link.
4. Wählen Sie die Aktion **Neuen Workflow aus Vorlage** aus, um eine Vorlage für den E-Belegprozess auszuwählen. Die verfügbaren Vorlagen sind **An einen Dienst senden** und **An mehrere Dienste senden**.
5. Wählen Sie **OK**, um die Einrichtung des Workflows abzuschließen.
6. Wählen Sie im Feld **Dann Antwort** **E-Beleg mit Einrichtung senden** aus, um die Workflowreaktionen zu konfigurieren.
7. Wählen Sie den von Ihnen erstellten E-Belegdienst als Option aus, wählen Sie **OK** und aktivieren Sie dann den Workflow.

> [!NOTE]
> Sie können Ihren eigenen Workflow für E-Belege erstellen, ohne vordefinierte Workflow-Vorlagen zu verwenden. Wenn Sie mehr Dienste haben, können Sie unterschiedliche Workflows nutzen.

Um weitere Workflows zu nutzen, konfigurieren Sie diese über die Belegsendeprofile für verschiedene Debitoren. Wenn Sie den Workflow einrichten, geben Sie das Belegsendeprofil in der Spalte **Bei Bedingung** auf der Registerkarte **Workflowschritte** an, da Sie nicht über zwei Dienste verfügen können, die dasselbe Belegsendeprofil in Workflows verwenden.

Wenn Sie Ihren Workflow auf der Seite **Workflows** konfigurieren, zeigen Sie auf das Feld **Bei Bedingung** auf dem Inforegister **Workflowschritte**. Wählen Sie auf der Seite **Ereignisbedingungen** im Feld **Filter** das Belegsendeprofil aus, das Sie verwenden möchten.

## Richten Sie eine Aufbewahrungsrichtlinie für E-Belege ein

E-Belege können im Hinblick darauf, wie lange die E-Belege aufbewahrt werden müssen, verschiedenen lokalen Gesetzen unterliegen. Aus diesem Grund haben wir eine Aufbewahrungsrichtlinie für alle wichtigen Informationen im Zusammenhang mit E-Belegen hinzugefügt. Administrierende können Aufbewahrungsrichtlinien festlegen, die bestimmen, wie häufig Dynamics 365 Business Central veraltete Datensätze im Zusammenhang mit E-Belegen gelöscht werden. Weitere Informationen zu Aufbewahrungsrichtlinien finden Sie unter [Aufbewahrungsrichtlinien definieren](admin-data-retention-policies.md).

Führen Sie die folgenden Schritte aus, um Aufbewahrungsrichtlinien für E-Belege einzurichten.

1. Wählen Sie auf der Seite **E-Belegdienste** die Aktion **Aufbewahrungsrichtlinie** aus.
2. Wenn die Aktion abgeschlossen ist, wählen Sie eine der folgenden Aufbewahrungsrichtlinien zum Einrichten aus:

    - E-Beleg-Protokoll
    - Integrationsprotokoll für E-Belege
    - E-Beleg-Zuordnungsprotokoll
    - E-Beleg-Datenspeicherung

## E-Belegdemodaten  

> [!NOTE]
> Ab Business Central Version 24.0 ist es möglich, Demodaten für E-Belege einzurichten.

Um einfachere Möglichkeiten zum Testen und Vorführen der Fähigkeiten von **E-Belegen** zu bieten, hat Microsoft ein neues Demomodul für elektronische Belege erstellt. Um dieses Modul zu aktivieren, gehen Sie wie folgt vor:  

1.  Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Contoso-Demo-Tool** ein und wählen Sie dann den zugehörigen Link aus.  
2.  Bevor Sie das **E-Beleg-Contoso-Modul** aktivieren, müssen Sie aufgrund von Abhängigkeiten die folgenden Module aktiviert haben: **Allgemeines Modul** und **Lagermodul**. 
3.  Nachdem Sie diese Module aktiviert haben, wählen Sie das **E-Belege-Contoso-Modul** und anschließend die Aktion **Generieren** aus. 
4.  Gehen Sie wie folgt vor.  
5.  Schließen Sie die Seite.   

Sobald Sie ein aktiviertes Modul haben, haben Sie neue Demoartikel erstellt, sechs elektronische Belege (basierend auf Peppol BIS 3) importiert und bereits den **E-Belegdienste** mit erstellten Workflows konfiguriert.  

## Siehe auch

[E-Belege im Verkauf verwenden](finance-how-use-edocuments.md)    
[E-Belege im Einkauf verwenden](finance-how-use-edocuments-purchase.md)  
[E-Belege in Business Central erweitern](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Finanzmanagement](finance.md)    
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)    
[Käufe mit Einkaufsrechnungen und Bestellungen erfassen](purchasing-how-record-purchases.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
