---
title: Benutzerdefinierte Berichtslayouts aktualisieren
description: 'Erfahren Sie, wie Sie ein angepasstes Berichtslayout, das in einem Bericht verwendet wird, aktualisieren können, wenn es z.B. Designänderungen am Dataset des Berichts gibt.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9652, 9650'
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="legacy-update-custom-report-layouts" />(Legacy) Benutzerdefinierte Berichtslayouts aktualisieren

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Gelegentlich müssen Sie möglicherweise ein benutzerdefiniertes Berichtslayout aktualisieren, das in einem Bericht verwendet wird. Dies ist obligatorisch, wenn es eine Entwurfsänderung an dem Datensatz des Berichts gegeben hat, wenn zum Beispiel ein Feld, das im Layout verwendet wird, aus dem Berichtsdatensatz entfernt wurde. Wenn ein Berichtlayout eine Aktualisierung benötigt, erhalten Sie eine Fehlermeldung, wenn Sie versuchen, die Berichtvorschau anzeigen, zu drucken oder zu speichern.  

Um Berichtlayout aus der Fehlermeldung automatisch zu aktualisieren, die angezeigt wird, wenn Sie diesen Bericht ausführen, wählen Sie die Schaltfläche **Ja** auf der Fehlermeldung. Oder im Voraus, wenn Sie Berichte ausführen, können Sie bestimmte Berichtslayouts oder alle benutzerdefinierten Berichtslayouts aktualisieren, auf die sich Datasetänderungen auswirken können.  

Sie haben auch die Option, Aktualisierungen zu testen, ohne die erforderlichen Änderungen für die benutzerdefinierten Berichtslayouts zu übernehmen. Dies ermöglicht Ihnen, festzustellen, welche Änderungen für das Berichtslayout übernommen werden, und mögliche Probleme im Verfahren zu identifizieren. Aus den Testergebnissen können Sie die benutzerdefinierten Berichtslayouts direkt zur Bearbeitung öffnen, um Probleme zu beheben. Es ist empfehlenswert, dass Sie das Berichtslayoutupdate testen, bevor Sie die Updates übernehmen.  

Nicht alle Berichtsdatasetänderungen können automatisch aktualisiert werden in den Berichtslayouts. Einige Änderungen erfordern, dass Sie das Berichtslayout manuell bearbeiten. Weitere Informationen finden Sie unter [Einschränkungen des Updates des benutzerdefinierten Berichtslayouts](ui-update-report-layouts.md#UpdateLimitations).  

## <a name="to-update-one-or-more-custom-report-layouts" />Um eine oder mehrere benutzerdefinierten Berichtslayouts zu aktualisieren

1.  Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Auswahl des Berichtslayouts** ein und wählen Sie dann den entsprechenden Link.  

2.  Auf der Seite **Auswahl des Berichtslayouts**, wenn Sie einen bestimmten Bericht aktualisieren möchten, wählen Sie das Layout aus der Liste, und wählen die **Layout aktualisieren** Aktion aus. Oder, wenn alle benutzerdefinierten Berichtslayouts des Unternehmens aktualisieren möchten, wählen Sie die Aktion **Alle Layouts aktualisieren** aus.  

Wenn keine Fehler auftreten, wird die Aktualisierung für die Berichtslayouts übernommen. Wenn Fehler auftreten, dann erscheint eine Meldung, die die Fehler enthält. Sie müssen dann manuell das benutzerdefinierte Berichtslayout bearbeiten, um den Fehler zu beheben. Weitere Informationen finden Sie unter [Beheben von Fehlern](ui-update-report-layouts.md#FixErrors).  

## <a name="to-test-custom-report-layout-updates" />Updates zu benutzerdefinierten Berichtslayouts testen

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Auswahl des Berichtslayouts** ein und wählen Sie dann den entsprechenden Link.  

2.  Auf der Seite **Auswahl des Berichtslayouts** wählen Sie die **Testlayout-Aktualisierungen** Aktion aus.  

 Änderungen der Berichtslayouts werden getestet, jedoch nicht auf die tatsächlichen Berichtslayouts angewendet. Eine **Aktualisierungsprotokoll Berichtlayout**-Seite wird angezeigt, das den Status potenzieller Aktualisierungen für jedes Berichtslayout bereitstellt. Gibt es Fehler für ein Berichtslayout, können Sie auf das Berichtslayout zwecks Bearbeitung direkt aus der Meldung zugreifen, um sämtliche Probleme zu beheben. Weitere Informationen finden Sie unter [Beheben von Fehlern](ui-update-report-layouts.md#FixErrors).  

## <a name="limitations-of-the-custom-report-layout-update" /><a name="UpdateLimitations"></a> Einschränkungen des Updates des benutzerdefinierten Berichtslayouts
 Es gibt verschiedene Arten von Änderungen, die die automatische Aktualisieren für benutzerdefinierte Berichtslayouts übernehmen kann, zum Beispiel ein Feld, das im Layout verwendet wird, das aus dem Berichtsdataset entfernt wurde. Jedoch kann das automatische Aktualisieren die folgenden Änderungen an einem Berichtsdataset nicht verarbeiten.  

1.  Gelöschte Felder, Beschriftungen oder Datenelemente.  

2.  Kopieren von Feldnamen im Berichtslayout, nachdem ein Feld im Dataset umbenannt wurde. Dieses sollte als Designfehler behandelt werden.  

3.  Aktualisieren von Szenarien, in denen es noch mehrere Iterationen eines Berichtslayouts gibt, das mehrere Umbenennungsaktionen bei denselben Feldern, Beschriftungen oder Datenelementen verursacht.  

 Wenn der Aktualisierungsvorgang eines dieser Probleme erkennt, kann die Aktualisierung nicht angewendet werden. Sie müssen die Probleme manuell korrigieren, indem Sie beispielsweise das Berichtslayout in Word bearbeiten, oder programmgesteuert, indem Sie Upgrade-Codeunits verwenden.  

## <a name="fixing-errors" /><a name="FixErrors"></a> Beheben von Fehlern
 Wenn Sie eine Fehlermeldung bei der Aktualisierung oder dem Testen von Berichtslayoutupdates erhalten, dann müssen Sie wahrscheinlich das Berichtlayout ändern, um das Problem zu korrigieren. Lesen sie die Fehlermeldung, um den Grund des Problems zu ermitteln.  

 Das häufigste Problem ist, wenn ein Feld, das im Layout verwendet wird, dem Berichtsdataset entfernt wurde. In diesem Fall sehen Sie eine Zeile in der Fehlermeldung, die angibt, dass ein Artikel entfernt wurde. Um dieses Problem zu beheben, müssen Sie das Layout bearbeiten und das betreffende Feld entfernen.  

 Weitere Informationen finden Sie unter [Erstellen und bearbeiten eines benutzerdefinierten Berichts- oder Dokumentenlayout](ui-how-create-custom-report-layout.md#ModifyCustomLayout).  

Nachdem Sie das Layout ändern, versuchen Sie, das Layout erneut zu aktualisieren.  

## <a name="see-related-microsoft-training" />Siehe verwandte [Microsoft Schulungen](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also" />Siehe auch
 [Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
 [Arbeiten mit Berichten, Batchaufträgen und XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
