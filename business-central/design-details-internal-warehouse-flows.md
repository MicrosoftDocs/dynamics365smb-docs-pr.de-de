---
title: Designdetails - Interner Lagerfluss | Microsoft Docs
description: An einem Unternehmensstandort konzentriert sich der Warenfluss zwischen Lagerplätzen auf die Kommissionierung von Komponenten und die Einlagerung von Endartikeln für Produktions oder Montageaufträge und Ad-hoc-Verschiebungen, wie etwa Lagerplatzauffüllungen, ohne Bezug auf Herkunftsbelege.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 7fa2f139935e279af47548b5c8e8a28b84845521
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185324"
---
# <a name="design-details-internal-warehouse-flows"></a>Designdetails: Interner Lagerfluss
An einem Unternehmensstandort konzentriert sich der Warenfluss zwischen Lagerplätzen auf die Kommissionierung von Komponenten und die Einlagerung von Endartikeln für Produktions oder Montageaufträge und Ad-hoc-Verschiebungen, wie etwa Lagerplatzauffüllungen, ohne Bezug auf Herkunftsbelege. Der Umfang und die Art der einbezogenen Tätigkeiten variiert zwischen der grundlegenden und der erweiterten Logistik.  

 Einige interne Ströme überschneiden sich mit eingehenden oder ausgehenden Strömen. Ein Teil dieser Überschneidung wird als die Schritte 4 und 5 im grafischen Diagramm für erweiterte ein- und ausgehende Ströme angezeigt. Weitere Informationen finden Sie unter [Designdetails: Eingehender Lagerfluss](design-details-outbound-warehouse-flow.md).  

## <a name="internal-flows-in-basic-warehousing"></a>Interne Ströme in der einfachen Logistik  
 In der Basis-Lagerkonfiguration konzentriert sich der Warenfluss zwischen Lagerplätzen in den Debitorenzentren auf die Kommissionierung von Komponenten und die Einlagerung von Endartikeln für Produktion oder Montage und Ad-hoc-Verschiebungen, wie etwa Lagerplatzauffüllungen, ohne Bezug auf Herkunftsbelege.  

### <a name="flows-to-and-from-production"></a>Fließt zu und von Produktion  
 Die Hauptintegration zwischen Fertigungsaufträgen und grundlegenden Logistikaktivitäten wird durch die Möglichkeit repräsentiert, Produktionskomponenten mit den Seiten **Kommissionierung** und **Lagerbestandsumlagerung** zu kommissionieren.  

> [!NOTE]  
>  Auf der Seite **Lagerkommissionierung** wird der Komponentenverbrauch zusammen mit der Kommissionierungsbuchung gebucht. Bei Verwendung der Seite **Lagerbestandsumlagerung** werden nur Lagerplatzregulierungen registriert, ohne dass Artikelpostenbuchungen stattfinden.  

 Zusätzlich zur Komponentenbehandlung wird die Integration durch die Möglichkeit, Fertigungsartikel einzulagern, mit der Seite **Lagereinlagerung** dargestellt.  

 Die Felder **Fert.-Bereitst.-Lagerplatzcode**, **Fert.-Ausgangslagerplatzcode** und **Off. Fert.-Ber.-Lagerpl.-Code** auf der Lagerortkarte oder den Arbeitsplatz/Arbeitsplatzgruppenkarten definieren Standardströme nach und von Fertigungsbereichen.  

 Weitere Informationen darüber, wie der Komponentenverbrauch aus Zu-Produktion- oder Off. Fert.-Ber.-Lagerplätzen gebucht wird, finden Sie im Abschnitt „Buchungen von Produktionskomponenten in Lager“ in diesem Thema.  

### <a name="flows-to-and-from-assembly"></a>Fließt zu und von Montage  
 Die Hauptintegration zwischen Montageaufträgen und grundlegenden Logistikaktivitäten wird durch die Möglichkeit repräsentiert, Montagekomponenten zum Montagebereich zu verschieben.  

 Während keine bestimmten Lagerfunktionen für die Einlagerung von Montageartikeln vorhanden sind, kann der Lagerplatzcode im Montageauftragskopf zu einem standardmäßigen Einlagerungs-Lagerplatz festgelegt werden. Das Buchen des Montageauftrags erfolgt dann wie das Buchen einer Einlagerung. Die Lageraktivität, um Montageartikeln in das Lager zu verschieben, kann auf der Seite **Interne Umlagerung** verwaltet werden, ohne Verknüpfung zum Montageauftrag.  

 Die folgenden Montageflüsse sind vorhanden.  

|Workflow|Beschreibung|  
|----------|---------------------------------------|  
|Lagermontage|Die Komponenten werden auf einem Montageauftrag benötigt, bei dem die Ausgabe im Lager gespeichert wird.<br /><br /> Der Warenfluss der Logistik wird auf der Seite **Lagerbestandsumlagerung** verwaltet. Eine Entnahmezeile gibt an, wo die Komponenten entnommen werden sollen. Eine Einlagerungszeile gibt an, wo die Komponenten platziert werden sollen.|  
|Programmfertigung|Die Komponenten werden auf einem Montageauftrag benötigt, der mit einem Verkaufsauftrag verbunden ist, der geliefert wird, wenn der verkaufte Artikel montiert wird.|  

> [!NOTE]  
>  Wenn Artikel auftragsgemäß montiert werden, löst die Kommissionierung des verknüpften Verkaufsauftrags eine Lagerbestandsumlagerung für alle beteiligten Montagekomponenten aus, nicht nur für den Verkaufsartikel wie beim Liefern von Lagerartikeln.  

 Die Felder **Zu Mont.-Bereitst.-Lagerplatzcode**, **Von Mont.-Bereitst.-Lagerplatzcode** und **Montage-Ausgangslagerplatzcode** auf der Lagerortkarte legen Standardströme nach und von Montagebereichen fest.  

> [!NOTE]  
>  Das Feld **LP-Code f. Prog.fert.lief.** fungiert als Montagelagerplatz in Auftragsmontageszenarien.  

### <a name="ad-hoc-movements"></a>Ad-hoc-Lagerplatzumlagerungen  
 In der einfachen Lagerverwaltung geschieht die Verschiebung von Artikeln von Lagerplatz zu Lagerplatz ohne Beziehung zu Herkunftsbelegen auf der Seite **Interne Umlagerung** zusammen mit der Seite **Lagerbestandsumlagerung**.  

 Eine andere Art, Artikel ad hoc zwischen Lagerplätzen umzulagern, besteht darin, positive Posten im **Neuer Lagerplatzcode** -Feld auf der Seite **Umlagerung Buch.-Blatt** buchen.  

## <a name="internal-flows-in-advanced-warehousing"></a>Interne Ströme in der erweiterten Logistik  
 In erweiterten Lagerkonfigurationen, der Warenfluss zwischen Lagerplätzen in den Mandantencentern hinsichtlich Entnahmekomponenten und dem Einlagern von Endartikeln für Fertigungsaufträge und dem Kommissionieren von Komponenten für Montageaufträge. Darüber hinaus treten interne Ströme als Ad-hoc-Lagerplatzumlagerungen, wie Lagerplatzauffüllungen ohne Beziehung zu Herkunftsbelegen auf.  

### <a name="flows-to-and-from-production"></a>Fließt zu und von Produktion  
 Die Hauptintegration zwischen Fertigungsaufträgen und erweiterten Logistikaktivitäten wird durch die Möglichkeit repräsentiert, Produktionskomponenten, auf der Seite **Kommissionierung** und auf der Seite **Kommissioniervorschlag**, zu kommissionieren, sowie durch die Möglichkeit, Fertigungsartikel auf der Seite **Interne Einlagerung** einzulagern.  

 Ein weiterer Integrationspunkt in der Produktion wird mit dem **Lagerplatzumlagerung** Fenster, zusammen mit der Lagerplatzumlagerungs-Seite bereitgestellt, womit Sie Komponenten platzieren und produzierte Artikel für freigegebene Fertigungsaufträge nehmen können.  

 Die Felder **Fert.-Bereitst.-Lagerplatzcode**, **Fert.-Ausgangslagerplatzcode** und **Off. Fert.-Ber.-Lagerpl.-Code** auf der Lagerortkarte oder den Arbeitsplatz/Arbeitsplatzgruppenkarten definieren Standardströme nach und von Fertigungsbereichen.  

 Weitere Informationen darüber, wie der Komponentenverbrauch aus Zu-Produktion- oder Off. Fert.-Ber.-Lagerplätzen gebucht wird, finden Sie im Abschnitt „Buchungen von Produktionskomponenten in Lager“ in diesem Thema.  

### <a name="flows-to-and-from-assembly"></a>Fließt zu und von Montage  
 Die Hauptintegration zwischen Montageaufträgen und erweiterten Logistikaktivitäten wird durch die Möglichkeit repräsentiert, Montagekomponenten, mit der Seite **Kommissionierung** und der Seite **Kommissioniervorschlag**, zu kommissionieren. Diese Funktionen funktionieren genauso, wie beim Kommissionieren von Komponenten für Fertigungsaufträge.  

 Während keine bestimmten Lagerfunktionen für die Einlagerung von Montageartikeln vorhanden sind, kann der Lagerplatzcode im Montageauftragskopf zu einem standardmäßigen Einlagerungs-Lagerplatz festgelegt werden. Das Buchen des Montageauftrags erfolgt dann wie das Buchen einer Einlagerung. Die Lageraktivität, um von Montageartikeln in das Lager zu verschieben, kann auf der **Lagerplatzumlagerungsvorschlag**-Seite oder auf der **Interne Einlag.-Anforderung**-Seite verwaltet werden, ohne Verknüpfung zum Montageauftrag.  

> [!NOTE]  
>  Wenn Artikel auftragsgemäß montiert werden, löst die Lagerlieferung des verknüpften Verkaufsauftrags eine Kommissionierung für alle beteiligten Montagekomponenten aus, nicht nur für den Verkaufsartikel wie beim Liefern von Lagerartikeln.  

 Die Felder **Mont.-Bereitst.-Lagerplatzcode** und **Montage-Ausgangslagerplatzcode** auf der Lagerortkarte legen Standardströme nach und von Montagebereichen fest.  

### <a name="ad-hoc-movements"></a>Ad-hoc-Lagerplatzumlagerungen  
 In erweiterten Lagerfunktionen werden die Artikelbewegungen von Lagerplatz zu Lagerplatz ohne Beziehung zu Herkunftsbelegen auf der Seite **Lagerplatzumlagerungsarbeitsblatt** verwaltet und auf der Seite Lagerplatzumlagerungsvorschlag registriert.  

## <a name="flushing-production-components-in-the-warehouse"></a>Buchungen von Produktionskomponenten in Lager  
 Wenn auf der Artikelkarte eingerichtet, werden Komponenten, die mit Kommissionierungen kommissioniert werden, als durch den Fertigungsauftrag verbraucht gebucht, wenn die Kommissionierung registriert wird. Bei Verwendung der **Kommiss. + Vorwärts**-Methode und der **Kommiss. + Rückwärts**-Buchungsmethode löst die Kommissionierungsregistrierung die zugehörige Verbrauchsbuchung aus, wenn die erste Operation beginnt oder die letzte Operation endet.  

 Bedenken Sie das folgende Szenario basierend auf der [!INCLUDE[d365fin](includes/d365fin_md.md)] Demodatenbank, WHITE-Standort.  

 Ein Fertigungsauftrag für 15 STÜCK des Artikels LS-100 ist vorhanden. Einige der Artikel auf der Komponentenliste müssen manuell in ein FA-Verbrauchs Buch.-Blatt gebucht werden, und andere Artikel auf der Liste können mithilfe der **Kommiss. + Rückwärts**-Buchungsmethode automatisch kommissioniert und gebucht werden.  

> [!NOTE]  
>  **Kommiss. + Vorwärts** arbeitet nur, wenn der zweite FA-Arbeitsplan-Zeilenarbeitsgang einen Verbindungscode verwendet. Die Freigabe eines geplanten Fertigungsauftrags initiiert die Vorwärtsbuchung von Komponenten, die auf **Kommiss. + Vorwärts** festgelegt sind. Die Buchung kann jedoch erst stattfinden, wenn die Kommissionierung der Komponenten erfasst ist, was wiederum erst geschehen kann, wenn der Auftrag freigegeben wurde.  

 Die folgenden Schritte beschreiben die entsprechenden Aktionen verschiedener Benutzer und die entsprechende Reaktion:  

1.  Der Fertigungsbereichsvorgesetzte gibt den Fertigungsauftrag frei. Artikel mit der Buchungsmethode **Vorwärts** und keinem Verbindungscode werden vom Off. Fert.-Ber.-Lagerplatz. abgezogen.  
2.  Der Fertigungsbereichsvorgesetzte wählt die Schaltfläche **Kommissionierung erstellen** auf dem Fertigungsauftrag aus. Ein Lager-Kommissionierbeleg wird für die Kommissionierung von Artikel mit den Buchungsmethoden **Manuell**, **Kommiss. + Rückwärts** und **Kommiss. + Vorwärts** erstellt. Diese Artikel werden in den Fert.-Bereitst.-Lagerplatzcode aufgeführt.  
3.  Der Lagermanager weist einem Lagermitarbeiter die Kommissionierungen zu.  
4.  Der Lagermitarbeiter kommissioniert die Artikel aus den jeweiligen Lagerplätzen und platziert sie im Fert.-Bereitst.-Lagerplatzcode oder in dem Lagerplatz, der in der Kommissionierung angegeben ist.  
5.  Der Lagermitarbeiter registriert die Kommissionierung. Die Menge wird von den Kommissionierlagerplätzen abgezogen und dem Verbrauchslagerplatz hinzugefügt. Das Feld **Menge kommissioniert** auf der Komponentenliste für alle kommissionierten Artikel wird aktualisiert.  

    > [!NOTE]  
    >  Nur die Menge, die kommissioniert wurde, kann verbraucht werden.  

6.  Der Maschinist informiert den Produktionsleiter, dass die Endartikel fertig sind.  
7.  Der Fertigungsbereichsvorgesetzte verwendet das Verbrauchs Buch.-Blatt oder das Produktions Buch.-Blatt, um den Verbrauch von Komponenten zu buchen, die entweder die Buchungsmethode **Manuell**, **Vorwärts** oder **Kommiss. + Vorwärts** zusammen mit Arbeitsplanlinkcodes verwenden.  
8.  Der Produktionsleiter bucht die Ausgabe des Fertigungsauftrags, und ändert den Status zu **Beendet**. Die Menge der Komponenten, die die Buchungsmethode **Rückwärts** verwenden, wird vom Off. Fert.-Ber.-Lagerplatz.abgezogen, und die Menge der Komponenten, die die Buchungsmethode **Kommiss. + Rückwärts** verwenden wird vom Fert.-Bereitst.-Lagerplatz abgezogen.  

 Die folgende Abbildung zeigt, wann das Feld **Lagerplatzcode** auf der Komponentenliste entsprechend Ihrer Lagerort- oder Arbeitsplatzeinrichtung gefüllt wird.  

 ![Übersicht darüber, wann/wie das Feld Lagerortcode ausgefüllt wird](media/binflow.png "Übersicht darüber, wann/wie das Feld Lagerortcode ausgefüllt wird")  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Lagerverwaltung](design-details-warehouse-management.md)
