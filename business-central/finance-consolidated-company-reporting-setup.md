---
title: Unternehmenskonsolidierung einrichten
description: 'Erfahren Sie, wie Sie konfigurieren können, wie Daten von verschiedenen Unternehmen in Business Central an ein Konsolidierungsunternehmen gemeldet werden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 06/12/2024
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# <a name="set-up-company-consolidation"></a>Unternehmenskonsolidierung einrichten

Bevor Sie die Sachposten von zwei oder mehr Unternehmen (Niederlassungen) in ein konsolidiertes Unternehmen zusammenführen können, müssen Sie die Kontenpläne und das Konsolidierungsunternehmen vorbereiten.  

Je nach Komplexität Ihrer Unternehmen, gibt es zwei Arten, die Konsolidierung einzurichten:

* Wenn Sie nicht erweiterte Einstellungen benötigen, wie Einschließen eines Unternehmens, dessen Sie nur ein Teil anlegen, können Sie die Felder **Mandanten-Konsolidierung** Setup um raschen Einrichten einer Konsolidierung nutzen. Der Leitfaden führt Sie durch die grundlegenden Schritte durch.
* Wenn Sie erweitertere Einstellungen benötigen, können Sie den Konsolidierungsmandanten und die Konzernmandanten einrichten.
  * Geben Sie in jeder Geschäftseinheit die Hauptbuchkonten an, die in die Konsolidierung einbezogen werden sollen, sowie die Umrechnungsmethode für jedes Konto.
  * Richten Sie in der konsolidierten Gesellschaft für jede Gesellschaft, die in die Konsolidierung einbezogen werden soll, eine Geschäftsbereichskarte ein. Auf der Konzernmandantenkarte befinden sich Informationen wie Datumswerte für das Geschäftsjahr des Konzernmandanten und der Prozentsatz jedes Kontos, das in die Konsolidierung einbezogen werden muss.

## <a name="simple-consolidation-setup"></a>Einfache Konsolidierungseinrichtung

Wenn die Konsolidierung einfach ist, weil Sie beispielsweise die Geschäftseinheit als Ganzes besitzen, führt Sie die **Mandanten-Konsolidierung** durch die folgenden Schritte:

* Erstellen Sie ein neues konsolidiertes Unternehmen oder konsolidieren Sie ein bereits erstelltes Unternehmen. Der Mandant sollte keine Transaktionen beinhalten.
* Ergebnisse in Vorschau anzeigen. [!INCLUDE[prod_short](includes/prod_short.md)] überprüft, dass die Masterdaten und die Transaktionen in den Konsolidierungsmandanten erfolgreich übertragen werden können.

Um die unterstützte Einrichtung zu starten, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Unterstützte Einrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie **Prozesskonsolidierungen** und schließen Sie dann jeden Schritt im unterstützten Setup der Unternehmenskonsolidierung ab.

## <a name="advanced-consolidation-setup"></a>Erweiterte Konsolidierungseinrichtung

Wenn Sie erweitertere Einstellungen für die Konsolidierung benötigen, können Sie die Konsolidierung manuell einrichten. Wenn Sie Unternehmen haben, die Sie nur teilweise besitzen, oder Sie haben Mandanten, die nicht enthalten sein soll.  

### <a name="set-up-the-consolidated-company"></a>Richten Sie den Konsolidierungsmandanten ein.

Zuerst müssen Sie das konsolidierte Unternehmen einrichten. Die Einrichtung des konsolidierten Unternehmens erfolgt auf die gleiche Weise wie die Einrichtung anderer Unternehmen. Weitere Informationen über die Einrichtung eines Unternehmens finden Sie unter [Bereitschaft für die Geschäftsabwicklung](ui-get-ready-business.md).  

Die folgende Liste veranschaulicht wichtige Aspekte des konsolidierten Unternehmens.

1. Die Kontenpläne einrichten

    Weitere Informationen zum Einrichten eines Kontenplans finden Sie unter [Einrichten oder Ändern des Kontenplans](finance-setup-chart-accounts.md).  

    Die Kontenpläne können in einem gesamten Konzernmandanten und dem konsolidierten Unternehmen identisch sein, oder das konsolidierte Unternehmen kann einen anderen Kontenplan haben. Wenn sich der Kontenplan eines Konzernmandanten von dem des konsolidierten Unternehmens unterscheidet, müssen Sie die Zuordnung zwischen Konten in den Konten im Konzernmandanten angeben. Weitere Informationen finden Sie im Abschnitt [Sachkonten für die Konsolidierung vorbereiten](#glacc).

2. Konzernmandanten hinzufügen.

    Um die Daten mehrerer Unternehmen zu konsolidieren, müssen Sie die Tochtergesellschaften als Geschäftseinheiten einrichten und angeben, wie viel von ihren Salden einbezogen werden soll. Um mehr über Geschäftsbereiche zu erfahren, gehen Sie zum Abschnitt [Konzernmandanten hinzufügen](#busunit).

3. Geben Sie bei Bedarf Wechselkurse an.

    Geben Sie Wechselkurse an, wenn Sie Daten für Konzernmandanten konsolidieren, die unterschiedliche Währungen verwenden. Die drei benutzten Wechselkurse sind **Durchschnittskurs (manuell)**, **Ultimokurs** und **Letzter Ultimokurs**. Weitere Informationen zu Wechselkursen finden Sie unter [Wechselkurse für Konsolidierungen angeben](#exchrates).

4. Konsolidierung von Dimensionsinformationen und Hauptbuchkonten.

    Weitere Informationen finden Sie im Abschnitt [Dimensionen ein- oder ausschließen](#dim).

### <a name="add-business-units"></a><a name="busunit"></a>Konzernmandanten hinzufügen

Richten Sie im Konsolidierungskreis jede Gesellschaft, deren Daten Sie konsolidieren wollen, als Konzernmandanten ein. Bevor Sie eine Konsolidierung durchführen und Ihren Konsolidierungsbericht erstellen, sollten Sie die Finanzdaten in jedem Konzernmandanten überprüfen.

Ein wesentlicher Teil der Einrichtung eines Konzernmandanten besteht darin, festzulegen, wie der Konzernmandant seine Finanzdaten mit dem konsolidierten Unternehmen austauscht. Es gibt manuelle und automatische Optionen:

* Um einen manuellen Prozess zu verwenden, können Sie für [!INCLUDE [prod_short](includes/prod_short.md)] online und vor Ort eine .xml-Datei exportieren, die die Hauptbucheinträge der Einheit enthält. Anschließend importieren Sie die Datei in das konsolidierte Unternehmen.
* Um den Datenaustausch zu automatisieren, können Sie für [!INCLUDE [prod_short](includes/prod_short.md)] online eine API verwenden, die [!INCLUDE [prod_short](includes/prod_short.md)] für die gemeinsame Nutzung von Daten in verschiedenen Umgebungen bereitstellt. Wenn sich Ihre Unternehmen in der gleichen Umgebung befinden, können Sie die Option **Datenbank** verwenden.

> [!NOTE]
> Mit der API-Option können Sie auch Hauptbucheinträge von anderen [!INCLUDE [prod_short](includes/prod_short.md)] Umgebungen teilen. Um die API-Option nutzen zu können, muss der Benutzer, der die Konsolidierung konfiguriert, über die Berechtigung zum Zugriff auf Sachposten verfügen. Beispielsweise gewähren die Berechtigungssätze „D365 Basic“ und „D365 Read“ Zugriff.

#### <a name="set-up-business-unit-currencies"></a>Konzernmandantenwährungen einrichten

Achten Sie auf die Wechselkurse, die in verschiedenen Teilen des Prozesses verwendet werden, wenn Sie die Konsolidierung für Geschäftseinheiten in einer Fremdwährung durchführen. Dies gilt insbesondere, wenn Sie die Konsolidierung erneut ausführen. Verwenden Sie die Seite **Konzernmandantenwährungen einrichten**, um die Kurse einfach im Auge zu behalten.

Auf der Seite **Konzernmandantenwährungen einrichten** werden Ihnen die letzten Kurse für den Durchschnittskurs, den Ultimokurs und den letzten Ultimokurs angezeigt. Sie können die Wechselkurse in der Währungswechselkurstabelle entnehmen, was die Überprüfung der Kurse erleichtert. Sie können die Kurse für die aktuelle Ausführung ändern, indem Sie die Werte eingeben oder aus vorherigen Ausführungen kopieren. Um Kurse zu kopieren, wählen Sie **Aus früheren Konsolidierungen auswählen**. Diese Seite ist hilfreich, wenn Sie eine frühere Konsolidierung erneut ausführen möchten und einen früheren Ultimokurs verwenden. Dieser Schritt hilft bei der korrekten Neubewertung Ihrer Bilanzpositionen. Die Seite **Aus früheren Konsolidierungen auswählen** ist auch hilfreich, wenn Sie nur die verwendeten Kurse anzeigen möchten, beispielsweise bei der Problembehandlung. Die Seite wird auf Ausführungen gefiltert, welche den ausgewählten Konzernmandanten enthalten.

Sie starten den Batchauftrag **Konsolidierung ausführen** von der Listenseite **Konzernmandanten** aus. Sie können die Seite **Konzernmandantenwährungen einrichten** auch aufrufen, indem Sie die Aktion **Wechselkurse** auswählen.

> [!NOTE]
> Die derzeit auf der Karte **Konzernmandant** verfügbaren Wechselkurseinrichtungsseiten für den Durchschnitts-, Ultimo- und letzten Ultimokurs werden ab einer zukünftigen Version nicht mehr unterstützt. Sie können diese Kurse jedoch weiterhin beibehalten, wenn Sie über Konzernmandanten verfügen, die Sie über Dateien importieren.

#### <a name="create-a-business-unit"></a>Einen Konzernmandanten erstellen

1. Melden Sie sich im Konsolidierungsmandanten an.
2. Wählen Sie das ![Glühbirne, welche die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") Symbol. Geben Sie **Konzernmandanten** ein und wählen Sie dann den zugehörigen Link.  
3. Wählen Sie die Aktion **Neu** aus, und füllen Sie dann bei Bedarf die Felder im Inforegister **Allgemein** und **Sachkonten** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Wenn Sie die Felder **Startdatum** und **Enddatum** ausfüllen, stellen Sie sicher, in die GAAP-Regeln zu Abrechnungszeiträumen des Konzernmandanten gegenüber der Muttergesellschaft einzuwilligen.
4. Geben Sie auf dem Inforegister **Datenimport** im Feld **Standarddatenimport** an, wie Sie die Hauptbucheinträge mit der konsolidierten Gesellschaft austauschen wollen:

   * Um Daten zwischen Unternehmen in derselben Umgebung auszutauschen, wählen Sie **Datenbank**.
   * Um Daten zwischen Unternehmen in unterschiedlichen Umgebungen auszutauschen, wählen Sie **API**, und füllen Sie dann das aus Feld **Endpunkt der API** aus.
        
        Um die Endpunkt-URL zu erhalten, müssen Sie in [!INCLUDE [prod_short](includes/prod_short.md)] des Unternehmens des Konzernmandanten die **Seite „Konsolidierungseinrichtung“**, und überprüfen Sie den Feldwert „API-Endpunkt“ der aktuellen Umgebung. 
   * Um eine .xml-Datei zu exportieren und manuell freizugeben, wählen Sie **Dateiformat**.

### <a name="prepare-general-ledger-accounts-for-consolidation"></a><a name="glacc"></a>Sachkonten für die Konsolidierung vorbereiten

Der Kontenplan eines Mandanten, den Sie konsolidieren, muss Konten für die Konsolidierung enthalten. Für jedes buchende Hauptbuchkonto in jeder Gesellschaft müssen Sie das Hauptbuchkonto in der konsolidierten Gesellschaft angeben, auf das der Saldo übertragen werden soll. Mit dieser Zuordnung können Sie Unternehmen mit unterschiedlichen Kontenplänen konsolidieren.

Wenn der Kontenplan des Konzernmandanten aus dem Konsolidierungsmandanten abweicht, müssen Sie die Sachkonten vorbereiten für die Konsolidierung. Sie können Konten definieren, um Soll- und Habenposten zu buchen und die Methode festlegen, die verwendet wird, um Währungen im Konsolidierungsmandanten zu übersetzen.

1. Wählen Sie in der [!INCLUDE [prod_short](includes/prod_short.md)] jeder Einheit die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die Karte für das Konto, und füllen Sie dann die Felder im Inforegister **Konsolidierung** aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Wenn Sie die Felder **Konsol. Sollkonto** und **Konsol. Habenkonto** leer lassen, geht [!INCLUDE [prod_short](includes/prod_short.md)] davon aus, dass sie im konsolidierten Unternehmen denselben Konten zugeordnet sind.

> [!TIP]
> Es kann Szenarien geben, in denen Sie ein Konto nicht in eine Konsolidierung einbeziehen möchten. Dies kann zum Beispiel dann der Fall sein, wenn Sie möchten, dass Ihr Konsolidierungsunternehmen nur die Bilanzen der Tochterunternehmen widerspiegelt. Um ein Konto von der Konsolidierung auszuschließen, aktivieren Sie für das Konto den Umschalter **Von Konsolidierung ausschließen**.

### <a name="specify-exchange-rates-for-consolidations"></a><a name="exchrates"></a>Wechselkurse für Konsolidierungen angeben

Richten Sie Wechselkurse für die Konsolidierung ein, wenn für die Finanzauswertungen eines Konzernmandanten nicht die Währung des konsolidierten Mandanten verwendet wird. Für jedes Konto bestimmt der Inhalt des Feldes **Konsol. Umrechnungsmethode** den Wechselkurses. Geben Sie im konsolidierten Unternehmen auf jeder Konzernmandantenkarte im Feld **Währungswechselkurstabelle** an, ob die Konsolidierung Wechselkurse des Konzernmandanten oder des konsolidierten Unternehmens verwendet. Bei Verwendung von Wechselkursen des konsolidierten Mandanten können die Wechselkurse für einen Konzernmandanten geändert werden. Enthält bei einer Geschäftseinheit das Feld **Wechselkurstabelle** (auf der Konzernmandantenkarte) den Wert **Lokal**, kann der Wechselkurs auf der Konzernmandantenkarte geändert werden. Zwar werden die Wechselkurse aus der Tabelle **Währungswechselkurs** kopiert, Sie haben jedoch die Möglichkeit, diese Wechselkurse vor der Konsolidierung zu ändern.

Die folgende Tabelle beschreibt die Wechselkursmethoden, die Sie für Konten verwenden können.

|Wechselkurs | Typische Nutzung |
|---|---|
|Durchschnittskurs (manuell) | Der Durchnittskurs für den zu konsolidierenden Zeitraum berechnen Sie manuell. Sie berechnen den Durchschnitt entweder als arithmetisches Mittel oder als bestmögliche Schätzung und geben ihn für jeden Konzernmandanten ein. Für GuV-Konten verwenden,|
|Ultimokurs | Für Kontenschema für Bilanz verwendet.|
|Letzter Ultimokurs | Schlusskurs: Der Schlusskurs am Devisenmarkt für den Tag, für den die Bilanz oder Gewinn- und Verlustrechnung erstellt wird. Sie geben diesen Kurs für jeden Konzernmandanten ein. Für Kontenschema für Bilanz verwenden.|
|Historischer Kurs | Der Wechselkurs, der galt, als die Transaktion erfolgte.|
|Gemischter Wechselkurs | Mischkurs: Die Beträge der laufenden Periode werden zum Durchschnittskurs umgerechnet und zum zuvor erfassten Saldo für den konsolidierten Mandanten addiert. Normalerweise verwenden Sie diese Methode für Gewinnrücklagenkonten. Diese Konten umfassen Beträge aus unterschiedlichen Zeiträumen und enthalten daher Beträge, die mit unterschiedlichen Wechselkursen umgerechnet wurden.|
|Eigenkapitalkurs | Diese Option ist ähnlich wie der **Mischkurs**. Differenzen werden gebucht, um Sachkonten zu trennen.|

Um Wechselkurse für einen Konzernmandanten anzugeben, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Konzernmandanten** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Konzernmandantenübersicht** die Konzernmandanten und dann die Aktion **Wechselkurse** aus.  
3. Füllen Sie auf der Seite **Konzernmandantenwährungen einrichten** die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="include-or-exclude-dimensions"></a><a name="dim"></a>Dimensionen ein- oder ausschließen

Sie können Dimensionsinformationen und Sachkonten konsolidieren.

* Machen Sie bei den Dimensionen Angaben im Feld **Konsolidierungscode** oder lassen Sie es leer.
  * Um eine Dimension in der Konsolidierung auszuschließen, lassen Sie das Feld **Konsolidierungscode** bei der Dimension leer, und wählen Sie keine Dimensionen in den Feldern **Dimensionen kopieren** in irgendwelchen Konsolidierungsfunktionen oder Berichten.
  * Lassen Sie das Feld **Konsolidierungscode** leer, um Dimensionsinformationen in die Konsolidierung aufzunehmen. Die Konsolidierung funktioniert jedoch nur dann, wenn die Dimensionswerte in dem Konzernmandanten genau mit denen des konsolidierten Unternehmens übereinstimmen.
  * Um den Dimensionswertcode im Konzernmandanten mit einem anderen Dimensionswertcode im konsolidierten Unternehmen zu konsolidieren, füllen Sie das Feld **Konsolidierungscode** bei den Dimensionen aus.  
* Fügen Sie die Dimensionen zu den Sachkonten hinzu.

### <a name="exclude-a-company-from-consolidation"></a><a name="exclude"></a>Ein Unternehmen aus der Konsolidierung ausschließen

Wenn Sie keinen Konzernmandanten in die Konsolidierung einbeziehen, können Sie sie ausschließen. Um das zu tun, wechseln Sie zur Konzernmandantenkarte, und löschen Sie das Kontrollkästchen **Konsolidieren**.

### <a name="include-a-partially-owned-company-in-consolidation"></a><a name="include"></a>Schließen Sie Unternehmen in die Konsolidierung ein, das teilweise im Besitz ist

Wenn Sie nur einen Teil eines Unternehmens besitzen, können Sie für jede Transaktion einen Prozentsatz angeben, der Ihrem Anteil entspricht. Wenn beispielsweise 70% des Unternehmen anlegen, enthält $70 Konsolidierung einer Rechnung für $100. Um den Prozentsatz des Unternehmens anzugeben, den Sie anlegen, wechseln Sie zur Konzernmandantenkarte, und geben Sie den Prozentsatz im Feld **Konsolidierung %** ein.  

## <a name="see-also"></a>Siehe auch

[Konsolidieren von Finanzdaten aus mehreren Unternehmen](finance-consolidated-company-reporting.md)  
[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportieren Ihrer Geschäftsdaten nach Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
