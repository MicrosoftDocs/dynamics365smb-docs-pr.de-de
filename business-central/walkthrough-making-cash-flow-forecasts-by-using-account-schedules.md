---
title: Exemplarische Vorgehensweise - Erstellen von Cashflowplanungen mithilfe von Kontenschemata | Microsoft Docs
description: "In dieser exemplarischen Vorgehensweise wird beschrieben, wie Sie mit Kontenschemata arbeiten können, um Cashflowplanungen zu erstellen. Kontenschemata führen Berechnungen aus, die nicht direkt im Kontenplan für Cashflowkonten vorgenommen werden können. In Kontenschemata können Sie Zwischensummen für Cashflow-Auftragseingänge und -Auszahlungen einrichten. Diese Zwischensummen können in neue Summen einbezogen werden, die dann für Cashflowplanungen verwendet werden können."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 652a151ff50c8492b3dc7df5d17c04ff2d00faad
ms.contentlocale: de-de
ms.lasthandoff: 11/26/2018

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

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion Wie möchten Sie weiter verfahren geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie auf der Seite **Kontoschemaname** auf der Registerkarte **Neu** die Option Neu aus, um einen neuen Cashflow zu erstellen.  
3.  Geben Sie im Feld **Namen** **Planung** ein.  
4.  Geben Sie im Feld **Beschreibung** eine Beschreibung für die **Cashflowplanung** ein.  
5.  Lassen Sie die Felder **Standard Spaltenlayout** und **Analyseansichtsname** leer.  

## <a name="setting-up-account-schedule-lines"></a>Einrichten von Kontenschemazeilen  
Nachdem ein Kontenschemaname eingerichtet wurde, definiert Ken jede Zeile, die im Cashflow-Kontenschema angezeigt wird. Ken definiert Zeilen, die in Berichten zusätzlich zu den Zeilen angezeigt werden können, die nur Berechnungszwecken dienen.  

### <a name="to-set-up-account-schedule-lines"></a>So richten Sie Kontenschemazeilen ein  

1.  Wählen Sie auf der Seite **Kontoschemaname** den neuen **Planung**-Kontenschemanamen aus, den Sie erstellt haben. Wählen Sie auf der Registerkarte **Start** in der Gruppe **Vorgang** die Option **Kontenschema bearbeiten** aus.  
2.  Auf der Seite **Kontoplan** geben Sie jede Zeile genau wie in der folgenden Tabelle ein.  

    > [!NOTE]  
    >  Mithilfe der Funktion **CF-Konten einfügen** können Sie die Cashflowkonten aus dem Kontenplan für Cashflowkontos schnell markieren und sie in Kontenschemazeilen kopieren.  

    |Zeilennr.|Beschreibung|Total Art|Total|Zeile Art|Begtrag Art|Anzeigen|  
    |-------|-----------|-------------|--------|--------|---  ------|----| |C10|Betrag|Nettoveränderung|Einträge|Nettobetrag|Immer|  
    |C20|Betrag bis|Saldo am Datum|Einträge|Nettobetrag|Immer|  
    |C30|Gesamtes Finanzjahr|Gesamtes Finanzjahr|Einträge|Nettobetrg|Immer|  

4.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Das Spaltenlayout dem Kontenschemanamen zuweisen  
Ken kann das Spaltenlayout jetzt dem Kontenschemanamen zuweisen.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Das Spaltenlayout dem Kontenschemanamen zuweisen:  

1.  Wählen Sie auf der Seite **Kontoschemanamen** die **Planung**  im Feld **Name** aus.  
2.  Wählen Sie im Feld **Standardspaltenlayout** das Spaltenlayout **Cashflow** aus, um es als Standard-Spaltenlayout zuzuordnen.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>So können Sie die Cashflowplanung anzeigen und drucken  
1.  Wählen Sie auf der Seite **Kontoschemanamen** auf der Registerkarte **Übersicht** in der Gruppe Prozess die Option Übersicht aus, um die Cashflowplanung anzuzeigen.  
2.  Auf der Seite **Kontoschemaübersicht** können Sie einen Betrag auswählen und die Cashflowplanungs Posten dann anzeigen, aus denen sich der Betrag zusammensetzt. Darüber hinaus können Sie die Formel anzeigen, die verwendet wird, um den Betrag zu berechnen. Sie können die Beträge auch nach Datum und Dimension filtern.  
3.  Wählen Sie die Aktion **Drucken** aus, um die Cashflowplanung zu drucken.  

## <a name="see-also"></a>Siehe auch  
 [Arbeiten mit Kontenschemata](bi-how-work-account-schedule.md)   
 [Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

