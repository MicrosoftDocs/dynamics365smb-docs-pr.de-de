---
title: Exemplarische Vorgehensweise - Erstellen von Cashflowplanungen mithilfe von Kontenschemata | Microsoft Docs
description: In dieser exemplarischen Vorgehensweise wird beschrieben, wie Sie mit Kontenschemata arbeiten können, um Cashflowplanungen zu erstellen. Kontenschemata führen Berechnungen aus, die nicht direkt im Kontenplan für Cashflowkonten vorgenommen werden können. In Kontenschemata können Sie Zwischensummen für Cashflow-Auftragseingänge und -Auszahlungen einrichten. Diese Zwischensummen können in neue Summen einbezogen werden, die dann für Cashflowplanungen verwendet werden können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 67a6e963800bf5f0ce8e1a293463d53b51470ee5
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914785"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a>Exemplarische Vorgehensweise: Erstellen von Cashflowplanungen mithilfe von Kontenschemata
In dieser exemplarischen Vorgehensweise wird beschrieben, wie Sie mit Kontenschemata arbeiten können, um Cashflowplanungen zu erstellen. Kontenschemata führen Berechnungen aus, die nicht direkt im Kontenplan für Cashflowkonten vorgenommen werden können. In Kontenschemata können Sie Zwischensummen für Cashflow-Auftragseingänge und -Auszahlungen einrichten. Diese Zwischensummen können in neue Summen einbezogen werden, die dann für Cashflowplanungen verwendet werden können.  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise  
In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

- Einrichten eines neuen Cashflowkonto-Zeitplannamens.  
- Einrichten von Kontenschemazeilen.  
- Einrichten eines neuen Spaltenlayouts.  
- Zuweisen eines Spaltenlayouts zu einem Kontenschema.  
- Anzeigen und Drucken der Cashflowplanung.  

### <a name="prerequisites"></a>Voraussetzungen  
Für diese exemplarische Vorgehensweise gelten folgende Voraussetzungen:  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] installiert.  
- Die Cashflowvorschlagszeilen werden erfasst.  

## <a name="roles"></a>Rollen  
Die Aufgaben in dieser exemplarischen Vorgehensweise werden von den folgenden Benutzern ausgeführt:  

- CONTROLLER  

## <a name="story"></a>Hintergrund  
Ken ist ein Controller bei CRONUS , der Monatscashflowplanungen erstellt. Es schließt Finanzen, Verkauf, Einkauf und Anlagen in die Planung ein und zeigt sie dann CFO Sara für den Geschäfteseinblick.  

## <a name="setting-up-a-new-account-schedule-name"></a>Einrichten eines neuen Kontenschemanamens  
Ein Kontenschema besteht aus einem Cashflow-Kontenschemanamen mit einer Reihe von Zeilen und einem Spaltenlayout.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Einen neuen Kontenschemanamen einrichten:  

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Kontenschemata** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie auf der Seite **Kontoschemaname** auf der Registerkarte **Neu** die Option Neu aus, um einen neuen Cashflow zu erstellen.  
3.  Geben Sie im Feld **Namen** **Planung** ein.  
4.  Geben Sie im Feld **Beschreibung** eine Beschreibung für die **Cashflowplanung** ein.  
5.  Lassen Sie die Felder **Standard Spaltenlayout** und **Analyseansichtsname** leer.  

## <a name="setting-up-account-schedule-lines"></a>Einrichten von Kontenschemazeilen  
Nachdem ein Kontenschemaname eingerichtet wurde, definiert Ken jede Zeile, die im Cashflow-Kontenschema angezeigt wird. Ken definiert Zeilen, die in Berichten zusätzlich zu den Zeilen angezeigt werden können, die nur Berechnungszwecken dienen.  

### <a name="to-set-up-account-schedule-lines"></a>So richten Sie Kontenschemazeilen ein  

1.  Wählen Sie auf der Seite **Kontenplannamen** den neuen **Prognose** Kontenplannamen, den Sie erstellt haben, und wählen Sie dann die Aktion **Kontenplan bearbeiten** .  
2.  Auf der Seite **Kontoplan** geben Sie jede Zeile genau wie in der folgenden Tabelle ein.  

    > [!NOTE]  
    >  Mithilfe der Funktion **CF-Konten einfügen** können Sie die Cashflowkonten aus dem Kontenplan für Cashflowkontos schnell markieren und sie in Kontenschemazeilen kopieren.  

    |Rubrikennr.|Beschreibung|Zusammenzählungsart|Zusammenzählung|Zeilenart|Betragsart|Anzeigen|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |C10|Betrag|Bewegung|Posten|Nettobetrag|Immer|  
    |C20|Betrag bis Datum|Saldo bis Datum|Posten|Nettobetrag|Immer|  
    |C30|Gesamtes Geschäftsjahr|Gesamtes Geschäftsjahr|Posten|Nettobetrag|Immer|  

4.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Das Spaltenlayout dem Kontenschemanamen zuweisen  
Ken kann das Spaltenlayout jetzt dem Kontenschemanamen zuweisen.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Das Spaltenlayout dem Kontenschemanamen zuweisen:  

1.  Wählen Sie auf der Seite **Kontoschemanamen** die **Planung** im Feld **Name** aus.  
2.  Wählen Sie im Feld **Standardspaltenlayout** das Spaltenlayout **Cashflow** aus, um es als Standard-Spaltenlayout zuzuordnen.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>So können Sie die Cashflowplanung anzeigen und drucken  
1.  Wählen Sie auf der Seite **Kontoschemanamen** auf der Registerkarte **Übersicht** in der Gruppe Prozess die Option Übersicht aus, um die Cashflowplanung anzuzeigen.  
2.  Auf der Seite **Kontoschemaübersicht** können Sie einen Betrag auswählen und die Cashflowplanungs Posten dann anzeigen, aus denen sich der Betrag zusammensetzt. Darüber hinaus können Sie die Formel anzeigen, die verwendet wird, um den Betrag zu berechnen. Sie können die Beträge auch nach Datum und Dimension filtern.  
3.  Wählen Sie die Aktion **Drucken** aus, um die Cashflowplanung zu drucken.  

## <a name="see-also"></a>Siehe auch  
 [Arbeiten mit Kontenschemata](bi-how-work-account-schedule.md)   
 [Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
