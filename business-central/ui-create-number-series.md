---
title: Erstellen von Nummernkreisen
description: 'Erfahren Sie, wie Sie Nummernserien einrichten, die Konten und Belegen in Business Central eindeutige ID-Codes zuweisen.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'numbers, numbering'
ms.search.form: '456, 457, 458, 459, 460, 461, 21, 22, 26, 27, 31'
ms.date: 03/24/2022
ms.author: edupont
---
# <a name="create-number-series"></a><a name="create-number-series"></a><a name="create-number-series"></a>Erstellen von Nummernkreisen

Für jeden eingerichteten Mandanten müssen eindeutige Identifizierungscodes für Elemente wie Sachkonten, Debitor-/Kreditorkonten, Rechnungen und andere Belege zugeordnet werden. Die Nummerierung dient jedoch nicht nur zur Identifizierung. Ein durchdachtes Nummerierungssystem trägt zur einfacheren Verwaltung und besseren Analysierbarkeit des Mandanten bei, was eine Verringerung von Eingabefehlern zur Folge hat.

> [!Important]
> Standardmäßig sind Lücken in Zahlenreihen nicht zulässig, da der genaue Verlauf von Finanztransaktionen gesetzlich für die Prüfung verfügbar sein muss und daher eine ununterbrochene Reihenfolge ohne gelöschte Zahlen einhalten muss.
> 
> Wenn Sie Lücken in bestimmten Nummernserien zulassen möchten, wenden Sie sich zuerst an Ihren Wirtschaftsprüfer oder Buchhaltungsleiter, um sicherzustellen, dass Sie die gesetzlichen Anforderungen in Ihrem Land/Ihrer Region einhalten. Weitere Informationen finden Sie im Abschnitt [Lücken in Nummernserien](#gaps-in-number-series).

> [!NOTE]  
> Es ist empfehlenswert, dass Sie dieselben Nummernseriencodes verwenden, die Sie auf der Seite **Nummernserienübersicht** im CRONUS-Demomandanten sehen. Codes wie *P-INV+* ergeben möglicherweis nicht sofort einen Sinn, aber [!INCLUDE[prod_short](includes/prod_short.md)] hat eine einige Standardeinstellungen, die von diesen Nummernseriencodes abhängen.

Ein Nummerierungssystem wird durch Einrichten mindestens eines Codes für die einzelnen Arten von Masterdaten oder Belegen eingerichtet. So können Sie beispielsweise einen Code für die Nummerierung von Debitoren, einen weiteren Code für die Nummerierung von Verkaufsrechnungen und einen weiteren Code für die Nummerierung von Belegen in Fibu Buch.-Blättern einrichten. Nachdem Sie einen Code eingerichtet haben, müssen Sie mindestens eine Nummernserienzeile einrichten. Die Nummernserienzeile enthält Informationen wie die erste und die letzte Nummer der Serie sowie das Startdatum. Pro Nummernseriencode lassen sich mehrere Nummernserienzeilen mit unterschiedlichem Startdatum einrichten. Die Serie wird fortlaufend verwendet, wobei jede Serie zum entsprechenden Startdatum beginnt.

> [!NOTE]
> Die maximale Länge einer Zahl in einer Zahlenreihe beträgt 20 Zeichen. Es gibt einige Situationen, in denen [!INCLUDE[prod_short](includes/prod_short.md)] eine Nummer mit einer vom System generierten ID hinzufügt. Wenn beispielsweise Dokumente wie Rechnungen zum Anwenden von Transaktionen wie Zahlungen verwendet werden, generiert [!INCLUDE[prod_short](includes/prod_short.md)] Bezeichner für die angewendeten Transaktionen. Die Kennung besteht aus einer Nummer aus einer Nummernreihe und einer vom System zugewiesenen sechsstelligen ID, z. B. „-12345“. Wenn Sie erwarten, mehr als 9999 Dokumente in Bank‑ oder GIRO-Journalen oder Kassenbelegen zu verarbeiten, richten Sie Nummernserien für diese Dokumenttypen mit weniger als 14 Zeichen ein.

Sie legen in der Regel die Nummernserie fest, um automatisch die nächste fortlaufende Nummer auf neuen Karten oder Dokumente einzusetzen, die Sie erstellen. Sie können eine Nummernserie festlegen, bei der Sie manuell die neue Nummer eingeben können. Sie definieren dies mit dem Kontrollkästchen **Manuelle Nr.**

Verwenden Sie Nummernserienbeziehungen, wenn Sie für eine Masterdatenart mehrere Nummernseriencodes verwenden möchten – beispielsweise, um für unterschiedliche Artikelkategorien unterschiedliche Nummernserien zu verwenden.

## <a name="gaps-in-number-series"></a><a name="gaps-in-number-series"></a><a name="gaps-in-number-series"></a>Lücken in Nummernserien
Nicht alle Datensätze, die Sie in [!INCLUDE[prod_short](includes/prod_short.md)] erstellen sind Finanztransaktionen, die fortlaufend nummeriert werden müssen. Debitorenkarten, Verkaufsangebote und Lageraktivitäten sind Beispiele für Datensätze, denen eine Nummer aus einer Nummernreihe zugewiesen wurde, die jedoch keiner Finanzprüfung unterliegen und/oder die gelöscht werden können. Für solche Nummernserien können Sie das Kontrollkästchen **Lücken in Nr. zulassen** auf der Seite **Serienlinien** auswählen. Diese Einstellung kann auch nach dem Erstellen der Nummernserie geändert werden. Weitere Informationen zum Erstellen einer Vorlage finden Sie unter [Eine neue Nummernserie erstellen](ui-create-number-series.md#to-create-a-new-number-series).

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a><a name="behavior-of-the-no-field-on-documents-and-cards"></a><a name="behavior-of-the-no-field-on-documents-and-cards"></a>Verhalten des Nr.- Felder auf Belegen und Karten

In den Feldern „Vertrieb“, „Einkauf“ und „Übergangsbelege“ und auf allen Karten kann die **Nr.** Feld kann automatisch aus einer vordefinierten Nummernserie ausgefüllt werden. Sie können es auch manuell hinzufügen. Allerdings kann unter bestimmten Umständen das **Nr.**- Feld unsichtbar sein, damit Sie es nicht bearbeiten können.  

Das Feld **Nr.** Feld kann auf drei Arten ausgefüllt werden:

1. Wenn nur eine Nummernserie für die Art des Belegs oder der Karte vorhanden ist und das Feld **Standardnummern** ausgewählt und das Feld **Manuelle Nr.** nicht für die Nummernserie ausgewählt ist, wird das Feld automatisch mit der nächsten Nummer der Serie ausgefüllt. Das Feld **Nr.** ist auf der Karte oder dem Beleg nicht sichtbar.  

    Auch wenn Sie Vorlagen mit verschiedenen Nummernserien für Debitoren definieren, wenn die Nummernserie, die auf der **Einrichtung von Verkäufen und Forderungen**-Seite auf diese Weise eingerichtet ist, ist das **Nr.**- Feld ist auf der Debitorenkarte sichtbar, egal welche Vorlage Sie verwenden. Gleiches gilt für andere Arten von Karten und Dokumenten.  

    > [!NOTE]  
    > Wenn die Nummernserie nicht funktioniert, z. B. weil keine Nummern mehr vorhanden sind, dann ist das **Nr.**- Feld wird sichtbar und Sie können eine Nummer manuell eingeben oder die Probleme auf der Seite **Nummernserienübersicht** lösen.

2. Wenn mehr als eine Nummernserie für die Art des Belegs oder der Karte vorhanden ist und das Kontrollkästchen **Standardnr.** nicht für die Nummernserie aktiviert ist, die gerade zugewiesen ist, ist das **Nr.**- Feld sichtbar und Sie können auf der Seite **Nummernserienübersicht** nachschauen und dann die Nummernserie auswählen, die Sie verwenden möchten. Dann wird die nächste Nummer der Serie in das **Nr.**- Feld eingetragen.

3. Wenn Sie keine Nummernserie für diese Art von Beleg oder Karte eingerichtet haben oder das Feld **Manuelle Nr.** ausgewählt ist, ist das **Nr.**- Feld sichtbar und Sie müssen eine Nummer manuell eingeben. Sie können maximal 20 Zeichen, sowohl Zahlen als auch Buchstaben, eingeben.

Wenn Sie einen neuen Beleg oder eine Karte öffnen, für den bzw. die eine Nummernserie vorhanden ist, dann wird die relevante Seite **Einrichtung Verkaufsnummernserien** geöffnet, damit Sie eine Nummernserie für diese Art des Belegs oder der Karte einrichten können, bevor Sie andere Daten eingeben.

> [!NOTE]  
> Wenn Sie eine manuelle Nummerierung z. b. für neue Artikelkarten aktivieren müssen, die mit einem Datenmigrationsvorgang erstellt wurden, bei dem die **Nr.** standardmäßig ausgeblendet wird, gehen Sie zur Seite **Lagereinrichtung** und wählen Sie das Feld **Artikelnummern** aus, um alle zugehörigen Nummernserien zu öffnen und auf **Manuelle Nr.** festzulegen.

## <a name="to-create-a-new-number-series"></a><a name="to-create-a-new-number-series"></a><a name="to-create-a-new-number-series"></a>Erstellen von Nummernserien

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Nummernserie** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu**.  
3. Auf der neuen Zeile füllen Sie die Felder wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Wählen Sie die Aktion **Zeilen** aus.  
5. Auf der Seite **Serienlinien** füllen Sie die Felder aus, um die tatsächliche Verwendung und den Inhalt der in Schritt 2 erstellten Nummernserie zu definieren.  
6. Wiederholen Sie Schritt 5 für beliebig viele Verwendungen der von Ihnen benötigten Nummernserie. Das Feld **Startdatum** legt fest, welche Nummernserienzeile aktiv ist.  

> [!TIP]
> Um Benutzern zu erlauben, Nummern manuell anzugeben, wenn sie z.B. einen neuen Debitor oder Kreditor registrieren, wählen Sie das Feld **Manuelle Nummern** in der Nummernserie selbst. Um manuelle Nummern nicht zuzulassen, deaktivieren Sie das Feld.

Sie können den Vorlagen, die Sie für die verschiedenen Arten von Kunden und Kreditoren festgelegt haben, Nummernserien zuweisen, die Ihre Vertriebsmitarbeiter und Einkäufer am häufigsten in Ihre [!INCLUDE [prod_short](includes/prod_short.md)] eintragen. Legen Sie in diesem Fall die entsprechenden Zahlenserien fest, verknüpfen Sie sie über Beziehungen und fügen Sie dann die erste Zahlenserie in der entsprechenden Beziehung auf der entsprechenden Einrichtungsseite hinzu. Wenn ein Benutzer dann einen Debitor erstellt, wählt er die relevante Vorlage aus, und dem neuen Debitor wird eine Nummer aus der Nummernserie zugewiesen, die für diese Vorlage definiert ist.  

## <a name="to-create-relationships-between-number-series"></a><a name="to-create-relationships-between-number-series"></a><a name="to-create-relationships-between-number-series"></a>Verbindungen zwischen Nummernserien herstellen:

Wenn Sie mehr als einen Nummernseriencode für dieselbe Art von grundlegenden Daten oder Geschäftsvorfällen eingerichtet haben, können Sie Verbindungen zwischen diesen Codes herstellen. Dann können Sie zwischen den verschiedenen Codes auswählen, wenn Sie eine Nummer verwenden wollen. Wenn Sie eine Beziehung zwischen einer Gruppe von Zahlenreihen festlegen, ordnen Sie alle zugehörigen Reihen einem Zahlenreihencode zu. Dann können Sie diesen Code in ein Feld auf dem Inforegister **Nummerierung** auf einer der entsprechenden Einrichtungsseite eingeben, z.B. **Einrichtung Debitoren & Verkauf**.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Nummernserie** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Zeile mit der Nummernserie, für die Sie Verbindungen herstellen wollen und wählen Sie **Beziehungen**.
3. Geben Sie im Feld **Seriencode** den Code für die Nummernserie ein, für die Sie eine Verbindung mit der in Schritt 2 ausgewählten Nummernserie herstellen möchten.
4. Fügen Sie für jeden Code, für den eine Verbindung mit der ausgewählten Nummernserie hergestellt werden soll, eine neue Zeile hinzu.
5. Schließen Sie die Seite.

Wenn Sie jetzt etwas einrichten, was eine Nummer benötigt, können Sie die von Ihnen erzeugten Verbindungen verwenden, um zwischen den verbundenen Nummernserien auszuwählen.

## <a name="to-set-up-where-a-number-series-is-used"></a><a name="to-set-up-where-a-number-series-is-used"></a><a name="to-set-up-where-a-number-series-is-used"></a>Einrichten, ob eine Nummernserie verwendet wird

Der folgende Ablauf zeigt, wie Nummernserien für den Verkaufsbereich eingerichtet werden. Die Schritte sind gleich wie bei anderen Bereichen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkäufe & Debitoren** ein und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Debitoren & Verkauf** im Inforegister **Nummernserie**, wählen Sie die gewünschte Serie für jede Verkaufs- Karte oder jeden Beleg aus.

Die ausgewählten Anzahl wird nun verwendet, um **Nr.** auszufüllen Feld auf der fraglichen Karte oder auf dem fraglichen Dokument entsprechend den Einstellungen, die Sie in der Nummernserie erstellt haben.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/number-series-trail-codes-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
