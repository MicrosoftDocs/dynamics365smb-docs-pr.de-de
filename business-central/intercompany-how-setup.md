---
title: Buchung von Intercompany-Transaktionen festlegen
description: 'Erfahren Sie, wie Sie eine unternehmensübergreifende Partnerschaft aufbauen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 09/27/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621, 653_Primary'
ms.service: dynamics-365-business-central
---
# Intercompany-Transaktionen einrichten

Unternehmensgemeinschaften erleichtern die Abwicklung buchhalterischer Prozesse, wenn zwei oder mehrere Tochtergesellschaften eines Unternehmens häufig miteinander Geschäfte tätigen. Partner können Transaktionen wie Verkäufe und Käufe austauschen und entweder manuell oder automatisch abwickeln. Wenn beispielsweise ein Partner eine Buchungsblattzeile an einen anderen Partner sendet, wird eine Buchungsblattzeile für den empfangenden Partner erstellt.

Bei dem Intercompanykontenplan kann es sich beispielsweise um eine vereinfachte Version des Kontenplans des synchronisierenden Partners handeln. Jeder Partner weist den Intercompany-Kontenplan ihren Konen zu. Jeder Partner ordnet auch seine Dimensionen und Dimensionswerte den Intercompany-Dimensionen zu.

> [!NOTE]
> In der 1. Veröffentlichungswelle 2023 haben wir eine verbesserte Seite **Unternehmensübergreifende Einrichtung** eingeführt. Die neue Seite erleichtert das Einrichten einer Intercompanypartnerschaft, indem alle eingerichteten Aufgaben auf einer einzigen Seite zusammengefasst werden. Wenn Sie bei [!INCLUDE [prod_short](includes/prod_short.md)] neu sind, nutzen Sie die neue Erfahrung bereits. Wenn Sie bereits Kunde sind, kann Ihr Administrator den Funktionsschalter **Firmenübergreifende allgemeine Journalbuchungen automatisch akzeptieren** in der Seite **Funktionsverwaltung** aktivieren.
>
> Bei den Aufgaben in diesem Artikel wird davon ausgegangen, dass der Funktionsschalter aktiviert ist. Wenn Sie bereits eine Intercompanypartnerschaft eingerichtet haben, können Sie diese weiterhin verwenden.

## Bevor Sie beginnen

Bevor Sie mit dem Aufbau Ihrer Intercompanypartnerschaft beginnen, sind einige Entscheidungen zu treffen.

|Entscheidung  |Beschreibung  |
|---------|---------|
|Welcher Kontenplan soll die Grundlage für den Intercompany-Kontenplan sein?     | Alle Unternehmen in der Partnerschaft müssen denselben Intercompany-Kontenplan verwenden. Sie können Ihren Intercompany-Kontenplan auf dem Kontenplan eines der Unternehmen der Partnerschaft basieren oder einen neuen Intercompany-Kontenplan erstellen. Sie ordnen die in der Partnerschaft zu verwendenden Konten auf beide Arten zu, sodass jeder Partner Transaktionen auf den richtigen Konten sendet und empfängt. Weitere Informationen zum Einrichten des Intercompany-Kontenplans finden Sie unter [Intercompany-Kontenpläne einrichten](#set-up-the-intercompany-charts-of-accounts).         |
|Welche Dimensionen sollen die Basis für die Intercompany-Dimensionen sein?     | Wenn Sie Intercompany-Dimensionen verwenden, müssen diese für alle Unternehmen in der Partnerschaft gleich sein. Nachdem Sie Ihre Intercompany-Dimensionen angegeben haben, ordnen Sie deren Dimensionswerte zu. Weitere Informationen zum Zuordnen von Dimensionswerten finden Sie unter [Intercompany-Dimensionen einrichten](#set-up-intercompany-dimensions).        |
|Welche Partner sind Kunden oder Lieferanten oder beides?     |  Erfahren Sie mehr über das Einrichten von Kunden- und Lieferantenunternehmen in einer Intercompany-Partnerschaft unter [Intercompany-Partner als Kunden und Lieferanten einrichten](#set-up-intercompany-partners-as-customers-and-vendors).       |
|Möchten Sie Bankkonten angeben, die in der Partnerschaft verwendet werden sollen?| Sie können den Prozess der Registrierung von Zahlungstransaktionen beschleunigen, indem Sie das Bankkonto angeben, das für jedes Partnerunternehmen verwendet werden soll. Erfahren Sie mehr unter [Geben Sie die Bankkonten an, die für Intercompanypartner verwendet werden sollen](#specify-the-bank-accounts-to-use-for-intercompany-partners). |
|Wie möchten Sie die Unternehmen in der Partnerschaft identifizieren?     | Alle Parteien müssen sich auf einen eindeutigen Intercompanypartner-Identifikationscode für jedes Unternehmen einigen. Sie weisen den Code Debitoren- und Kreditorenkarten zu, um zugehörige Transaktionen zu identifizieren. Weitere Informationen zu Kennungen finden Sie unter [Nummernserien erstellen](ui-create-number-series.md).        |
|Wie möchten Sie mit Nummernelementen umgehen?     | Wenn Intercompanyzeilen Artikeln enthalten, können Sie entweder eigene Artikelnummern verwenden oder für die betreffenden Artikel jeweils die Artikelnummern des Partners einrichten, indem Sie das **Feld Kred.-Artikelnr.** oder das Feld **Gemeinsame Artikelnr.** auf der Artikelkarte verwenden. Sie können auch die Aktion **Artikelreferenz** verwenden, um die Nummern Ihrer Artikel den Artikelbeschreibungen Ihrer Intercompanypartner zuzuordnen. Weitere Informationen zu Artikelreferenzen finden Sie unter [Artikelreferenzen verwenden](inventory-how-use-item-cross-refs.md).        |
|Sind Ressourcen involviert?     | Wenn Sie Intercompany-Verkaufstransaktionen vornehmen, die Ressourcen beinhalten, müssen Sie auf der Ressourcenkarte der entsprechenden Ressourcen das Feld **IC-Partner Eink.-Sachkontonr.** ausfüllen. Das Feld enthält die Nummer des Intercompanysachkontos, auf das der Betrag für diese Ressource im Partnerunternehmen gebucht wird. Um mehr über Ressourcen zu erfahren, gehen Sie zu [Ressourcen einrichten](projects-how-setup-resources.md).<br><br>**HINWEIS**<br>Intercompany-Einkaufstransaktionen, die Ressourcen, Anlagevermögen und Artikelgebühren enthalten, werden nicht vollständig unterstützt. Im Partnerunternehmen bleibt das Feld **Positionstyp** in Einkaufsbelegzeilen leer, die diese Entitäten enthalten. Sie müssen sie das Feld manuell aktualisieren.        |

## Übersicht über die ersten Schritte

Verwenden Sie die Seite **Intercompany-Einrichtung**, um die folgenden Komponenten von Intercompany-Transaktionen einzurichten:

* Die Intercompany-Einstellungen Ihres Unternehmens.
* Das Unternehmen, das der Synchronisierungspartner sein wird.
* Der Intercompany-Kontenplan, den alle Partner zum Austausch von Transaktionen verwenden.
* Die Zuordnungen zwischen Konten im Kontenplan und dem Intercompany-Kontenplan für eingehende und ausgehende Transaktionen für jeden Partner.
* Die zu verwendenden Intercompany-Dimensionen und die Dimensionswerte und wie die Dimensionen jedem Partner zugeordnet werden sollen.
* Die Unternehmen, die die Intercompanypartner sind.
* Die Unternehmen, die Lieferanten oder Kunden oder beides sind.

## Einen Synchronisierungspartner einrichten

Alle Partner müssen denselben Intercompany-Kontenplan und ggf. dieselben Intercompany-Dimensionen verwenden. Sie können Zeit sparen, wenn Sie die Partnerschaft einrichten, indem Sie den Kontenplan und die Dimensionen für einen der Partner als Grundlage für den Intercompany-Kontenplan und die Dimensionen verwenden. Das Unternehmen, das Sie als Baseline verwenden, wird als *Synchronisierungspartner* bezeichnet. Typischerweise ist der Synchronisationspartner das Unternehmen der Zentrale, muss es aber nicht sein.

Auf der Seite **Unternehmensübergreifende Einrichtung** gibt jeder Partner den Synchronisierungspartner im Feld **Synchronisierungspartner** an. Danach werden der Intercompany-Kontenplan und die Intercompany-Dimensionen automatisch für sie festgelegt, basierend auf der Einrichtung für den Synchronisierungspartner. Die Partner verwenden dann die Seiten **Intercompany-Kontenplanzuordnung** und **Intercompany-Dimensionszuordnung**, um ihren Kontenplan zuzuordnen und Dimensionen in den Intercompany-Kontenplan und Dimensionen und umgekehrt. 

> [!NOTE]
> Es ist wichtig, Konten und Dimensionen in beide Richtungen zuzuordnen. Das heißt, sowohl zum Intercompany-Kontenplan und zu den Dimensionen als auch von dort zu Ihren eigenen Konten und Dimensionen.

### Verbinden Sie sich mit Partnern in einem anderen Mandanten oder einer anderen Umgebung

Wenn sich [!INCLUDE [prod_short](includes/prod_short.md)] von einem oder mehreren Partnern in einem anderen Mandanten oder einer anderen Umgebung befinden, sind einige zusätzliche Schritte zum Erstellen der Verbindung erforderlich. Die Schritte gelten für alle Partner in einem anderen Mandanten oder einer anderen Umgebung.

* Richten Sie [!INCLUDE [prod_short](includes/prod_short.md)] als registrierte App im Azure-Portal ein.
* In [!INCLUDE [prod_short](includes/prod_short.md)] fügen Sie die App-Registrierung hinzu und aktivieren sie.
* Tauschen Sie Informationen über ihre unternehmensübergreifenden Einrichtungen aus. Jeder Partner kann diese Informationen aus dem Leitfaden für unterstützte Einrichtung **Umgebungsübergreifende Einrichtung des IC-Partners** erhalten.

   |Aus der Einrichtung des Partners kopieren  |Kopieren Sie es in Ihre Einrichtung  |
   |---------|---------|
   |Aktuelle Verbindungs-URL     |Verbindungs-URL des IC-Partners         |
   |Aktuelle Unternehmens-ID     |Unternehmens-ID des IC-Partners         |
   |Intercompany-ID     |Intercompany-ID des IC-Partners         |
   |Firmenname     |Unternehmensname des IC-Partners         |

* Tauschen Sie die folgenden Authentifizierungseinstellungen aus, damit [!INCLUDE [prod_short](includes/prod_short.md)] bei der Verbindung authentifiziert werden kann. Jeder Partner kann diese Informationen über seine registrierte App abrufen. Weitere Informationen zum Erstellen einer registrierten App finden Sie unter [Registrierte App im Azure-Portal erstellen](#create-a-registered-app-in-azure-portal).  

  * Client-ID
  * Geheimer Clientschlüssel
  * Token-Endpunkt
  * Umleitungs-URL

Führen Sie in allen Unternehmen den Leitfaden für unterstützte Einrichtung **Umgebungsübergreifende Einrichtung des IC-Partners** aus, um die Informationen anzugeben. Um den Leitfaden zu starten, verwenden Sie auf der Seite **Intercompanypartner** die Aktion **Externes Einrichten verbinden**.

#### Erstellen Sie eine registrierte App im Azure-Portal

Dieser Vorgang ist nur erforderlich, wenn Sie eine Verbindung mit einem Partner herstellen möchten, dessen [!INCLUDE [prod_short](includes/prod_short.md)] sich in einem anderen Mandanten oder einer anderen Umgebung befindet.

> [!TIP]
> Es empfiehlt sich, beim Erstellen Ihrer registrierten App einen Texteditor wie Notepad geöffnet zu haben. Sie benötigen einige Informationen, wenn Sie den Leitfaden für unterstützte Einrichtung **Umgebungsübergreifende Einrichtung des IC-Partners** ausführen. Daher ist es hilfreich, die Informationen zur Hand zu haben.

1. Gehen Sie zum [Azure-Portal](https://portal.azure.com/#home).
2. Wählen Sie den **Microsoft Entra-ID**-Service aus.
3. Wählen Sie im linken Navigationsbereich **App-Registrierungen** aus.
4. Wählen Sie auf der Seite **App-Registrierungen** die Option **Neue Registrierung** aus.
5. Benennen Sie die Anwendung.
6. Wählen Sie den Kontotyp **Konten in einem beliebigen Organisationsverzeichnis (Beliebiger Microsoft Entra-ID-Mandant – mehrmandantenfähig)** aus.
7. Wählen Sie für den Umleitungs-URI im Feld **Plattform auswählen** die Option **Web** aus und geben Sie dann den URI an. Zum Beispiel \**https://businesscentral.dynamics.com/OAuthLanding.htm**.

  Wenn Sie mit einem eingebetteten ISV arbeiten, benötigen Sie möglicherweise einen anderen URI.

8. Registrieren Sie die App.
9. Wählen Sie auf der Seite **Intercompany-App** im Navigationsbereich **API-Berechtigungen** aus.
10. Wählen Sie die Aktion **Berechtigung hinzufügen**.
11. Wählen Sie auf der Registerkarte **Microsoft-APIs** die Option **Dynamics 365 Business Central** aus.
12. Wählen Sie im Bereich **API-Berechtigungen anfordern** die Option **Anwendungsberechtigungen** und dann die Berechtigung **API.ReadWrite.All** aus.
13. Wählen Sie auf der Seite **Intercompany-App | API-Berechtigungen** die Aktion **Administratorzustimmung für Contoso erteilen** aus und erteilen Sie dann die Zustimmung.
14. Wählen Sie im Navigationsbereich **Zertifikate und geheime Schlüssel** aus.
15. Wählen Sie die Registerkarte **Geheimer Clientschlüssel** und dann **Neuer geheimer Clientschlüssel** aus.
16. Geben Sie im Bereich **Geheimen Clientschlüssel hinzufügen** einen Namen für den geheimen Schlüssel ein und geben Sie an, wann er ablaufen soll.

  > [!NOTE]
  > Alle Partner, die sich in unterschiedlichen Umgebungen befinden, müssen den geheimen Schlüssel erneuern, bevor er abläuft.

  > [!IMPORTANT]
  > Kopieren Sie die ID in das Feld **Wert**, bevor Sie die Seite **Intercompany-App | Zertifikate & geheime Schlüssel** verlassen. Sie benötigen sie in einem späteren Schritt und sie ist nicht mehr verfügbar, nachdem Sie die Seite verlassen haben. Fügen Sie den Wert beispielsweise in einen Texteditor ein.

17. Im Navigationsbereich wählen Sie **Übersicht** aus.
18. Kopieren Sie den Wert in das Feld **Anwendungs-(Client-)ID**. Fügen Sie den Wert beispielsweise in einen Texteditor ein.
19. Wählen Sie die Aktion **Endpunkte** und kopieren Sie dann den Wert in das Feld **OAuth 2.0-Token-Endpunkt (v2)**. Fügen Sie den Wert beispielsweise in einen Texteditor ein.
20. Kopieren Sie den Wert in das Feld **Verzeichnis-(Mandant-)ID**. Fügen Sie den Wert beispielsweise in einen Texteditor ein.
21. Ersetzen Sie im kopierten Tokenwert **Organisationen** durch den Wert, den Sie aus dem Feld **Verzeichnis-(Mandant-)ID** im vorherigen Schritt kopiert haben.

#### Ihre registrierte App in Business Central hinzufügen und aktivieren

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Microsoft Entra-Anwendungskarte** ein und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie im **Status**-Feld **Aktiviert** aus. 
4. Wählen Sie die Aktion **Zustimmung erteilen** aus. 
5. Wählen Sie im Feld **Berechtigungssatz** den Berechtigungssatz **API – Umgebungsübergreifende Intercompany** aus.

## Richten Sie den Intercompanykontenplan ein

Alle Partner müssen denselben Intercompanykontenplan verwenden und ihm die Konten in ihrem eigenen Kontenplan zuordnen. Wenn der Kontenplan für Ihr Unternehmen den Intercompanykontenplan für Ihre Partnerunternehmen definiert, befolgen Sie die Schritte in diesem Abschnitt.

Wenn Sie eine XML-Datei verwenden, die den Intercompanykontenplan enthält, befolgen Sie die Schritte in [Importieren oder exportieren Sie einen Intercompanykontenplan](intercompany-how-setup.md#import-or-export-an-intercompany-chart-of-accounts).  

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Intercompanyeinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **IC-Kontenplan einfügen** aus.
3. Um Konten hinzuzufügen, geben Sie auf der Seite **Intercompany-Kontenplan** ein:
    * Wählen Sie **Neu** aus und geben Sie dann jedes Konto in einer Zeile auf der Seite ein.  
    * Wenn der Intercompanykontenplan dem üblichen unternehmenseigenen Kontenplan gleicht oder ähnelt, können Sie die Werte automatisch in das Fenster eingeben, indem Sie die Aktion **Aus Kontenplan kopieren** wählen. Sie können die neuen Zeilen bei Bedarf bearbeiten.
    * Wenn Sie für einen Synchronisationspartner einen Intercompanykontenplan eingerichtet haben, verwenden Sie die **Synchronisationseinrichtung**-Aktion zum Kopieren dieser Konten.

    > [!TIP]
    > Wenn Sie den Intercompany-Kontenplan von einem Synchronisationspartner kopieren, können Sie die **Synchronisationseinrichtung**-Aktion zum Aktualisieren Ihrer Intercompany-Konten mit allen Änderungen, die der Partner an seinen vornimmt verwenden.

Im nächsten Schritt ordnen Sie die Kontenpläne den Intercompanykontenplan zu. Mehr erfahren unter [Intercompanykontenplan dem unternehmenseigenen Kontenplan zuordnen](#map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts).

### So exportieren oder importieren Sie einen Intercompanykontenplan

Das Synchronisationsunternehmen kann seinen Kontenplan mit Partnern teilen, indem es ihn in eine Datei exportiert. Partner können die Datei importieren, um den Kontenplan zu erhalten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Intercompanyeinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **IC-Kontenplan einfügen** aus.
3. Wählen Sie auf der Seite **Intercompany-Kontenplan** die Aktion **Importieren/Exportieren** aus, und wählen Sie dann die Schaltfläche **Importieren** oder **Exportieren** aus.
4. Wählen Sie die zu importierende oder zu exportierende Datei aus.  

Die Seite **Intercompany-Kontenplan** wird mit den neuen oder bearbeiteten Sachkontozeilen entsprechend dem Intercompanykontenplan in der Datei ausgefüllt. Jede möglicherweise vorhandene Zeile auf der Seite bleibt unverändert.

## Den Intercompanykontenplan dem unternehmenseigenen Kontenplan zuordnen  

Wenn Sie den Intercompany-Kontenplan definiert oder importiert haben, ordnen Sie jedes Intercompany-Konto einem Ihrer Konten zu. auf der Seite **Intercompany-Kontenplan** legen Sie fest, wie Intercompanysachkonten bei eingehenden Transaktionen in Sachkonten des unternehmenseigenen Kontenplans übersetzt werden.

Wenn die Intercompany-Konten und Ihre Konten die gleichen Nummern haben, können Sie die Konten automatisch zuordnen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Intercompanyeinrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **IC-Kontenplan einfügen** aus.

    > [!TIP]
    > Um auf die Aktionen auf der Seite zugreifen zu können, müssen Sie die Seite möglicherweise auf die breite Layoutansicht erweitern.

3. Wählen Sie auf der Seite **Intercompany-Kontenplan** die Aktion **Kontenplan zuordnen** aus.
4. Sie können die Konten automatisch oder manuell neu zuordnen.

    * Um die Zuordnung manuell zu erstellen, wählen Sie auf der Seite **Intercompany-Kontenplan** und **Sachkontenplan** ein Konto aus, und wählen Sie dann ein Konto unter **Sachkonto-Nr.** und **IC-Nummer** aus Felder.
    * Um Konten mit gleichen Nummern automatisch zuzuordnen, markieren Sie die Zeilen, die Sie zuordnen möchten, wählen Sie die Aktion **Karte nach Acc. mit gleicher Nr** und wählen Sie dann den zu aktualisierenden Kontenplan aus.

    > [!TIP]
    > Wenn Sie viele oder vielleicht alle Konten abbilden möchten, wählen Sie eine Zeile, wählen Sie :::image type="icon" source="media/show-more-options-icon.png" border="false"::: und wählen Sie dann **Wählen Sie Mehr aus**.

## So richten Sie Intercompanydimensionen ein

Wenn Partner Transaktionen mit entsprechend verknüpften Dimensionen übertragen werden sollen, müssen Sie die Dimensionen vereinbaren, die Sie nutzen werden. Die synchronisierende Gesellschaft kann eine vereinfachte Version ihres eigenen Dimensionssatzes erstellen und diese in eine XML-Datei exportieren und dann die Datei an jeden Partner weitergeben. Jeder Partner kann die XML-Datei auf der Seite **Intercompanydimensionen** importieren und dann die Intercompanydimension ihren Dimensionen zuordnen. Mehr erfahren unter [Intercompanydimensionen Ihren unternehmenseigenen Dimensionen zuordnen](#map-intercompany-dimensions-to-your-companys-dimensions).

> [!NOTE]
> Jedes Unternehmen muss seine Dimensionen den Intercompany-Dimensionen für ausgehende und eingehende Dokumente zuordnen. Die Zuordnung von Konten in beide Richtungen ist wichtig und trägt dazu bei, die Konsistenz zwischen den Unternehmen aufrechtzuerhalten.

Wenn Partner die Intercompanydimensionen des Synchronisierungspartners verwenden, befolgen Sie die Schritte in diesem Abschnitt. Wenn Sie eine verwendete XML-Datei teilen möchten, die die Intercompanydimensionen enthält, befolgen Sie die Schritte in [Importieren oder exportieren Sie einen Intercompanydimension](#import-or-export-intercompany-dimensions).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Intercompanyeinrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **IC-Dimensionen** aus.
3. Um Dimensionen hinzuzufügen, gehen Sie zur Seite **Intercompanydimensionen**:
    * Wählen Sie **Neu** und geben Sie dann jede Dimension in einer Zeile ein.  
    * Wenn die Intercompanydimensionen gleich oder ähnlich sind wie Ihre reguläre Dimensionen, können Sie die Seite automatisch in das Fenster eingeben, indem Sie die Aktion **Aus Dimensionen kopieren** wählen. Danach können Sie Zeilen nach Bedarf bearbeiten.
    * Wenn Sie für einen Synchronisationspartner eine bestimmte Intercompanydimension eingerichtet haben, verwenden Sie die **Synchronisationseinrichtung**-Aktion zum Kopieren dieser Dimensionen.

    > [!TIP]
    > Wenn Sie die Intercompanydimensionen von einem Synchronisationspartner kopieren, können Sie die **Synchronisationseinrichtung**-Aktion zum Aktualisieren Ihrer Intercompany-Dimensionen mit allen Änderungen, die der Partner an seinen vornimmt verwenden.  

### Importieren oder exportieren von Intercompanydimensionen  

Das Synchronisationsunternehmen kann seine Dimensionen mit Partnern teilen, indem es sie in eine Datei exportiert. Partner können die Datei importieren, um die Dimensionen abzurufen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Intercompanyeinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **IC-Dimensionen** aus.  
3. Wählen Sie auf der Seite **Intercompanydimensionen** die Aktion **Importieren/Exportieren** aus, und wählen Sie dann die Schaltfläche **Importieren** oder **Exportieren** aus.
4. Wählen Sie die zu importierende oder zu exportierende Datei aus.

Im nächsten Schritt ordnen Sie die Dimensionen den Intercompanydimensionen zu. Mehr erfahren unter [Intercompanydimensionen Ihren unternehmenseigenen Dimensionen zuordnen](#map-intercompany-dimensions-to-your-companys-dimensions).

### Intercompanydimensionen Ihren unternehmenseigenen Dimensionen zuordnen

Nachdem Sie die Dimensionen definiert haben, die Sie verwenden, ordnen Sie jede Intercompanydimension einer Ihrer unternehmenseigenen Dimensionen zu und umgekehrt. Verwenden Sie die Seite **Intercompany-Dimensionszuordnung** , um die Zuordnung anzugeben. Wiederholen Sie anschließend den Vorgang für die Dimensionswerte.

* Geben Sie an, wie Intercompany-Dimensionen bei eingehenden Transaktionen Dimensionen aus der Dimensionsliste Ihres Unternehmens zugeordnet werden.
* Unter *Ausgehende Transaktionen* legen Sie fest, wie die unternehmenseigenen Dimensionen in Intercompanydimensionen übersetzt werden.

Wenn Intercompanydimensionen bezüglich ihres Codes mit unternehmenseigenen Dimensionen aus der Dimensionentabelle übereinstimmen, können diese Dimensionen durch das Programm automatisch einander zugeordnet werden.  

In den folgenden Schritten ordnen Sie zunächst konzerninterne Dimensionen Dimensionen für eingehende Dokumente im Bereich **Intercompany-Dimensionen** zu. Anschließend ordnen Sie Dimensionen Intercompany-Dimensionen für ausgehende Dokumente im Bereich **Aktuelle Unternehmensdimensionen** zuordnen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Intercompanyeinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **IC-Dimensionen** aus.
3. Wählen Sie auf der Seite **Intercompany-Dimensionen** die **Dimensionen-Zuordnung**-Aktion aus.
4. Sie können die Dimensionen automatisch oder manuell neu zuordnen.

    * Um die Zuordnung manuell zu erstellen, wählen Sie in den Bereichen **Unternehmensübergreifende Dimensionen** und **aktuelle Unternehmensdimensionen** eine Dimension aus und dann Wählen Sie eine Abmessung in den Feldern **Dim. Code** und **IC Dim. Code**.
    * Um Konten mit gleichen Codes automatisch zuzuordnen, markieren Sie die Zeilen, die Sie zuordnen möchten, wählen Sie die Aktion **Dimensionen mit gleichem Cod zuordnen** und wählen Sie dann die zu aktualisierende Dimensionen aus. 

    > [!TIP]
    > Wenn Sie viele oder vielleicht alle Dimensionen abbilden möchten, wählen Sie eine Zeile, wählen Sie :::image type="icon" source="media/show-more-options-icon.png" border="false"::: und wählen Sie dann **Wählen Sie Mehr aus**.

5. Wählen Sie die Aktion **Dimensionswerte-Zuordnung** aus.
6. Auf der Seite **Zuordnung von Intercompany-Dimensionswerten** ähneln die Schritte zum Erstellen der Zuordnung denen, die Sie gerade für Dimensionen ausgeführt haben.

## So richten Sie allgemeine Intercomapny-FibuBuch.-Blattzeilenvorlagen und -chargen ein

Sie müssen eine allgemeine Erfassungsvorlage und einen allgemeinen Erfassungsstapel einrichten, die standardmäßig für Intercompany-Transaktionen verwendet werden. Die Vorlage und der Stapel sind besonders wichtig, wenn Sie automatisch Intercompany-Transaktionen von Ihren Partnern akzeptieren. Weitere Informationen zum automatischen Akzeptieren von Transaktionen finden Sie unter [Transaktionen von Intercompany-Partnern automatisch akzeptieren](#auto-accept-transactions-from-intercompany-partners).   

* Fibu Buch.-Blätter dienen zum Buchen auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditorenkonten. Bei der Buchung mit einem Fibu Buch.-Blatt werden immer Posten für Sachkonten erstellt.  Verwenden Sie die Seite **Intercompany-Hauptbuch.-Blatt** , um das zu verwendenden Hauptbuch-Blatt einzurichten. Die für Intercompany-Transaktionen spezifischen Einstellungen sind die Konten, die Sie in den Feldern **IC-Kontotyp** und **IC-Kontonummer** angeben.
* Buch.-Blattvorlagen ermöglichen es Ihnen, in einer Buch.-Blatt Seite zu arbeiten, das für einen bestimmten Zweck entworfen wurde. So entsprechen die in der Buch.-Blattvorlage angezeigten Felder genau denen, die für einen bestimmten Bereich der Anwendung benötigt werden. Verwenden Sie die Seite **Allgemeine Buchungsvorlagen**, um eine Vorlage für Intercompany-Transaktionen einzurichten.

Um mehr über allgemeine Journalvorlagen und Batches zu erfahren, gehen Sie zu [Journalvorlagen und Batches verwenden](ui-work-general-journals.md#use-journal-templates-and-batches).

## Unternehmen für Intercompanytransaktionen einrichten

Bei den folgenden Schritten wird davon ausgegangen, dass ein Synchronisierungspartner mit dem Kontenplan und den Dimensionen eingerichtet ist, auf denen der Intercompany-Kontenplan und die Dimensionen basieren. Sie können sie selbst einrichten, aber in der Regel ist der Einstieg schneller und die Wartung einfacher, wenn Sie einen Synchronisierungspartner verwenden. Weitere Informationen zum Synchronisierungspartner finden Sie unter [Synchronisierungspartner einrichten](#set-up-a-synchronization-partner).

> [!TIP]
> Es empfiehlt sich, die Felder auf dem Inforegister **Allgemein** auf der Seite **Unternehmensübergreifende Einrichtung** vorher für jeden Partner auszufüllen, bevor Sie die Partner hinzufügen. Wenn Sie Partnerunternehmen hinzufügen, die sich im selben Mandanten befinden, ruft [!INCLUDE [prod_short](includes/prod_short.md)] ruft ihren IC-Code und Firmennamen aus ihrer Einrichtung auf dem Inforegister Allgemein ab. Das Feld **Firmenname** prüft, ob der IC-Code eindeutig ist.

> [!NOTE]
> Wenn Sie einen Synchronisierungspartner verwenden, lassen Sie das Feld **Synchronisierungspartner** leer, wenn Sie dieses Unternehmen für die Partnerschaft einrichten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Intercompanyeinrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie auf der Seite **Intercompany-Einrichtung** die Felder auf dem Inforegister **Allgemein** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Unter [!INCLUDE[prod_short](includes/prod_short.md)] online können Sie keine Dateispeicherorte verwenden, um Transaktionen an Ihre Partner zu übertragen, da [!INCLUDE[prod_short](includes/prod_short.md)] keinen Zugriff auf Ihr lokales Netzwerk hat. Daher ist bei Auswahl von **Dateispeicherort** im Feld **Transfertyp** das Feld **Ordnerpfad** nicht verfügbar. Stattdessen wird die Datei in den Ordner **Downloads** auf Ihrem Computer heruntergeladen. Anschließend senden Sie die Datei per E-Mail an eine Person in der Partnerfirma. Für einen direkteren Prozess empfehlen wir stattdessen die Auswahl von **E-Mail**.

Der nächste Schritt ist das Einrichten der Partnerunternehmen.

## Intercompanypartner einrichten

Jeder Partner muss alle anderen Unternehmen in der Partnerschaft als Partner hinzufügen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Intercompanyeinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf dem Inforegister **Intercompanypartner** und **Hinzufügen** aus.
3. Füllen Sie auf der Seite **Intercompanypartner** die Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wiederholen Sie die Schritte 2 und 3 für alle Unternehmen der Partnerschaft.

> [!NOTE]
> Wenn Sie für Intercompany-Buchungen **Transaktion automatisch akzeptieren** einschalten auf der Seite **Intercompany-Partnerkarte**, unterdrückt [!INCLUDE[prod_short](includes/prod_short.md)] Meldungen, die vor Einkaufsrechnungen warnen, die die ursprüngliche Bestellung duplizieren. Es ist wichtig, einen Geschäftsprozess für die Verwaltung von Duplikaten zu haben. Zum Beispiel durch Löschen solcher Bestellungen, wenn die Einkaufsrechnung vom Intercompany-Partner eingegangen ist.

### Einrichten von Intercompanypartner als Kunden und Kreditoren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Intercompanyeinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie auf dem Inforegister **Intercompanypartner** und öffnen Sie die die Kartenseite für den Partner.
3. Wählen Sie je nachdem, was Sie tun möchten, den Kunden oder Partner unter **Kundennummer** oder **Lieferanten-Nr.** Felder.

    > [!NOTE]
    > Wenn der Kunde oder Lieferant noch nicht erstellt wurde, können Sie **+Neu** im Dropdown-Menü auswählen, um sie einzurichten. Um mehr über das Erstellen von Kunden und Lieferanten zu erfahren, gehen Sie zu [Neue Kunden registrieren](sales-how-register-new-customers.md) und [Neue Lieferanten registrieren](purchasing-how-register-new-vendors.md).

    > [!TIP]
    > Sie können auch einen Debitor oder Kreditor als Intercompany-Partner definieren, inem Sie das Feld **IC-Partnercode** auf den Seiten **Debitorenkarte** und **Kreditorenkarte** ausfüllen.

### Vorgegebene IC-Partner-Sachkonten einrichten  

Bei der Erstellung von Intercompanyverkaufs- oder -einkaufszeilen, die als ausgehende Transaktion gesendet werden sollen, geben Sie ein Konto aus dem Intercompanykontenplan vor, auf das der Betrag im Partnerunternehmen gebucht werden soll. Auf der Seite **Sachkonto-Karte** können Konten, die Sie regelmäßig für ausgehende Intercompanyverkaufs- oder -einkaufszeilen verwenden, als vorgegebene Intercompanypartner-Sachkonten festgelegt werden. Für Debitorensammelkonten können beispielsweise die zugeordneten Kreditorensammelkonten aus dem Intercompanykontenplan als vorgegebene Konten festgelegt werden. Die Forderungs- und Verbindlichkeitskonten werden als Gegenkonto für den Intercompanypartner verwendet, wenn Sie Transaktionen in Intercompany-Hauptbuchungen buchen.  

Wenn Sie jetzt im Feld **Gegenkontonr.** in einer Intercompanyzeile mit dem Eintrag **Intercompanypartner** im Feld **Kontoart** ein Sachkonto eingeben, wird das Feld **SachkontoIC-Partner** automatisch ausgefüllt.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie das Sachkonto, das für Intercompanytransaktionen verwendet wird und geben Sie im Feld **Vorgegebene IC-Partner-Sachkonten** das Intercompanysachkonto ein, auf das Ihr Partner buchen soll, wenn Sie auf das Sachkonto in der Zeile buchen.
3. Wiederholen Sie Schritt 2 für jedes Konto, das Sie häufig im Feld **Gegenkontonr.** einer Zeile in einem Intercompany-Buch.-Blatt oder -Beleg eingeben.

### Transaktionen von Intercompanypartnern automatisch akzeptieren

Um Intercompanytransaktionen rascher zu verarbeiten, können Sie angeben, ob Sie automatisch Buchungszeilen basierend auf den Buchungen eines Intercompany-Partners auf der Seite **IC-Fibu Buch.-Blatt** erstellen möchten. Um eingehende und ausgehende Transaktionen automatisch zu erstellen, müssen Sie die folgenden Schalter für jeden Partner aktivieren:

* Aktivieren Sie auf der Seite **Unternehmensübergreifende Einrichtung** die Umschaltung **Automatisch. Senden-Transaktionen** für den Synchronisationspartner. Geben Sie dann an, wo empfangene Intercompany-Buchungsbuchungen erstellt werden sollen, indem Sie die Felder **Standard-IC Gen. Jnl. Vorlage** und **Standard IC Gen. Jnl. Charge** ausfüllen.

    > [!TIP]
    > Wenn das Feld **Standard-IC Gen. Jnl. Vorlage** leer ist, müssen Sie eine allgemeine Erfassungsvorlage einrichten, die Sie für Ihre zwischenbetrieblichen allgemeinen Erfassungen verwenden. Um mehr über allgemeine Journalvorlagen und Batches zu erfahren, gehen Sie zu [Allgemeine Intercompany-Journalvorlagen und Batches einrichten](#set-up-intercompany-general-journal-templates-and-batches)    

* Aktivieren Sie auf der Seite **Intercompany-Partner** die Umschaltung **Transaktionen automatisch annehmen**.

Die Buch.-Blattzeilen werden für Sie erstellt, aber nicht gebucht.

> [!NOTE]
> Wenn Ihre Organisation Intercompany-Features in [!INCLUDE [prod_short](includes/prod_short.md)] vor der 1. Veröffentlichungswelle 2022 verwendet hatm muss Ihr Administrator **Akzeptieren Sie automatisch unternehmensübergreifende allgemeine Buchungsbuchungen** auf der Seite **Funktionsverwaltung** aktivieren, um Transaktionen automatisch zu akzeptieren.

### Geben Sie die Bankkonten an, die für Intercompanypartner verwendet werden sollen

Um schnelle Zahlungen zu ermöglichen, geben Sie ein oder mehrere Bankkonten an, die für Intercompany-Partner verwendet werden sollen. Wenn ein Partner ein Intercompany-Hauptbuch für eine Zahlung verwendet, kann er das Bankkonto in der Zeile angeben. Das Bankkonto wird als Ausgleichskonto im empfangenden Unternehmen verwendet, wodurch die Notwendigkeit der manuellen Eingabe von Transaktionen minimiert wird.

* Um das zu verwendende Bankkonto anzugeben, wählen Sie auf der Seite **Unternehmensübergreifende Partner** die Aktion **Bankkonten** aus. Geben Sie auf der **Intercompany-Bankkontokarte** die Kontoinformationen ein.

## Fehlerbehandlung für Ihre Intercompany-Einrichtung

Auf der Seite **Unternehmensübergreifende Einrichtung** enthält der Bereich **Diagnose der unternehmensübergreifenden Einrichtung** Kacheln, die angeben, ob Sie alle eingerichtet haben die Komponenten, die für den Austausch konzerninterner Transaktionen erforderlich sind. Die Kacheln sind auch im Business-Manager-Rollencenter verfügbar. Wählen Sie die Kacheln aus, um herauszufinden, was fehlt. Eine Übersicht über die erforderlichen Komponenten finden Sie unter [Übersicht über die Schritte für die ersten Schritte](#overview-of-the-steps-to-get-started).

## Weitere Informationen

[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
