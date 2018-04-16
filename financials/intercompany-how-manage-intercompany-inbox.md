---
title: Verarbeiten eingehender und ausgehender IC-Transaktionen | Microsoft Docs
description: Intercompanytransaktionen, die Sie von Intercompanypartnern empfangen, werden im IC-Eingang aufgelistet, in dem Sie sie manuell oder automatisch bearbeiten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: abeb3ee24434ca3549e7ed88ecfae54cc395002d
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="manage-the-intercompany-inbox-and-outbox"></a>Intercompany-Ein- und -Ausgangstransaktionen verwalten
Alle Intercompanytransaktionen, die Sie auf elektronischem Wege von Intercompanypartnern empfangen, werden im Intercompanyeingang aufgelistet.  

## <a name="organizing-the-inbox"></a>Strukturieren des Eingangs  
 Mit Hilfe der Filterfelder im oberen Bereich des Fensters Eingang können Sie festlegen, welche Transaktionen im Fenster angezeigt werden. Wenn Sie beispielsweise nur die von einem bestimmten Partner erstellten Transaktionen anzeigen möchten, können Sie die entsprechenden Filterkriterien in den Feldern **Transaktionsursprung** und **Intercompanypartnercode** festlegen.  

### <a name="transaction-source"></a>Transaktionsursprung  
Welche Möglichkeiten Sie bei der Verwendung einer Transaktion haben, ist davon abhängig ob es sich dabei um eine Transaktion handelt, die:  

- Vom intercompanypartner erstellt oder  
- Vom intercompanypartner abgelehnt und an Sie zurückgesandt wurde.  

Das Feld **Transaktionsursprung anzeigen** kann zum Filtern der Transaktionen im Fenster **Intercompany-Eingangstransaktionen** verwendet werden, sodass in diesem Fenster nur Transaktionen des festgelegten Typs angezeigt werden. (Darüber hinaus können Sie nach Intercompanypartner oder nach dem Inhalt des Feldes **Zeilenaktion** filtern.)  

#### <a name="created-by-intercompany-partner"></a>Vom Intercompanypartner erstellt  
 Wenn Sie eine neue Transaktion empfangen, die vom Partner erstellt wurde, haben Sie folgende Möglichkeiten:

- Transaktion akzeptieren  
- Transaktion ablehnen (an Partner zurücksenden)  
- Transaktion abbrechen (löschen, ohne sie an den Partner zurückzusenden)  

#### <a name="returned-from-intercompany-partner"></a>Von Intercompanypartner zurückgesendete Transaktion  
 Wenn die Transaktion vom Intercompanypartner abgelehnt wurde, können Sie sie nur im Eingang abbrechen. Anschließend müssen Sie Korrekturzeilen erstellen oder das Buch.-Blatt oder den Beleg im Unternehmen stornieren.  

## <a name="re-creating-inbox-entries"></a>Neuerstellen von Eingangsposten  
 Wenn Sie eine Transaktion im Eingang akzeptiert, anschließend aber den Beleg oder das Buch.-Blatt gelöscht haben, statt diese zu buchen, können Sie den Eingangsposten neu erstellen und erneut akzeptieren.  

## <a name="getting-an-overview-of-intercompany-transactions-for-a-period"></a>Anzeigen einer Übersicht über die Intercompanytransaktionen eines bestimmten Zeitraums  
 Die Intercompanytransaktionen, die Sie in einem bestimmten Zeitraum empfangen oder versendet haben, können in einer Übersicht angezeigt werden. Im Bericht **Intercompanytransaktionen** werden alle Intercompanysachposten, Debitorenposten und Kreditorenposten aufgelistet.

 > [!NOTE]  
 > Wenn die Intercompanypartner sich in derselben Datenbank befinden, werden Transaktionen übertragen, ohne dass Dateien oder E-Mail erforderlich sind. Siehe Feld **Transfertyp** im Fenster **Intercompanypartner**. <br /><br />
In diesem Fall können Sie eine Überbrückung des Eingangs und Ausgangs durch das System festlegen, indem Sie das Kontrollkästchen **Transaktionen autom. akzeptieren** im Fenster **Intercompanypartner** und das Kontrollkästchen **Transaktionen autom. senden** im Fenster **Intercompanyeinrichtung** auswählen.

## <a name="to-import-intercompany-transactions-from-a-file"></a>Intercompanytransaktionen aus einer Datei importieren  
Wenn einer der Intercompanypartner sich nicht in derselben Datenbank wie das eigene Unternehmen befindet, können die Intercompanytransaktionen von diesem Partner in einer XML-Datei empfangen werden. Anschließend werden die Transaktionen in den Eingang importiert.  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol "Nach Seite oder Bericht suchen"") aus, geben Sie **Unternehmensdaten** ein, und wählen Sie dann den verknüpften Link aus.
2. Speichern Sie die Datei in dem Verzeichnis, das Sie im Feld **Intercompanyeingangsdetails** im Fenster **Firmendaten** angegeben haben.  
3. Wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") und geben **Intercompany-Eingangstransaktionen** ein. Wählen Sie dann den zugehörigen Link aus.
4. Wählen Sie im Fenster **Intercompany-Eingangstransaktionen** die **Transaktionsdatei importieren**-Aktion aus.  
5. Wählen Sie in dem angezeigten Fenster die XML-Datei mit den Transaktionen aus, und wählen Sie dann **Öffnen**.  

Die Transaktionen werden in den Eingang importiert und können nun verarbeitet werden.

## <a name="to-process-incoming-intercompany-transactions"></a>So verarbeiten Sie eingehende Intercompanytransaktionen  
Wenn Intercompanypartner Intercompanytransaktionen an Sie senden, werden diese Transaktionen im Intercompanyeingang abgelegt. Sie müssen die einzelnen Transaktionen im Eingang bewerten und entsprechend verarbeiten.  

1. Wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") und geben **Intercompany-Eingangstransaktionen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie im Fenster **Intercompany-Eingangstransaktionen** eine Zeile aus, und wählen Sie anschließend eine Aktion, wie **Akzeptieren** aus, um die Zeile zu verarbeiten.
3. Füllen Sie im Fenster **IC-Eingangsvorgang abschl.** die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie die Schaltfläche **OK** aus.  

Für Zeilen, die bei der Aktion **Akzeptieren** verarbeitet wurden, werden Beleg- oder Buch.-Blattzeilen in Ihrem Unternehmen erstellt. Öffnen Sie die Belege oder Buch.-Blätter, nehmen Sie die erforderlichen Änderungen vor, und buchen Sie sie anschließend.  

Zeilen, die Sie mit der **n Partner zurück**-Aktion verarbeitet haben, werden in den Ausgang verschoben, von dem aus diese dann an Ihren Partner gesendet werden kann.

Für Zeilen, die Sie mit der Aktion **Zurückgesendet durch Partner** verarbeitet haben, müssen Sie nun eine Korrektur in die ursprünglich in Ihrem Unternehmen gebuchte Transaktion buchen.

## <a name="to-process-outgoing-intercompany-transactions"></a>So verarbeiten Sie ausgehende Intercompanytransaktionen  
Wenn Sie Intercompany-Buch.-Blätter oder -Belege buchen oder Intercompanybestellbestätigungen senden, werden die Transaktionen an den Intercompanyausgang gesendet. Damit sie an die Intercompanypartner gesendet werden, müssen Sie den Ausgang öffnen und die Transaktionen verarbeiten.  

1.  Wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") und geben **Intercompany-Ausgangstransaktionen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie im Fenster **Intercompany-Ausgangstransaktionen** eine Zeile aus, und wählen Sie anschließend eine Aktion, wie **Zurück in Eingang** aus, um die Zeile zu verarbeiten.

Zeilen, die Sie mit der **An Intercompanypartner senden**-Aktion verarbeiten, werden an den Eingang des Partners gesendet.

Zeilen, die Sie mit der **Zurück in Eingang**-Aktion verarbeiten, werden in den Eingang verschoben, wo Sie sie akzeptieren können, um Belege oder Buch.-Blattzeilen in Ihrem Unternehmen zu erstellen.  

Für Zeilen, die Sie mit der Aktion **Abbrechen** verarbeitet haben, müssen Sie nun eine Korrektur in die ursprünglich in Ihrem Unternehmen gebuchte Transaktion buchen.  

## <a name="to-recreate-intercompany-inbox-transactions"></a>So erstellen Sie Intercompanyeingangstransaktionen neu  
Gelegentlich sollten Sie eine Transaktion im Ein- oder Ausgang neu erstellen. Wenn Sie z. B. eine Transaktion im Eingang akzeptiert, den Beleg oder das Buch.-Blatt anschließend jedoch statt zu buchen gelöscht haben, können Sie den Eingangsposten erneut erstellen und akzeptieren.  

In der folgenden Schrittfolge wird beschrieben, wie Eingangstransaktionen neu erstellt werden. Bei Ausgangstransaktionen wird jedoch gleichermaßen verfahren.

  1.  Wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") und geben **Intercompany-Eingangstransaktionen** ein. Wählen Sie dann den zugehörigen Link aus.  

  2.  Wählen Sie im Fenster **Bearbeitete IC-Eingangstrans.** die Zeile mit der Transaktion aus, die im Eingang neu erstellt werden soll, und wählen Sie dann die Aktion **Eingangstransaktion neu erstellen** aus.  

## <a name="see-also"></a>Siehe auch
[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

