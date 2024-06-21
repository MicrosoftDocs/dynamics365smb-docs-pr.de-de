---
title: Wie Sie Serviceverträge konvertieren
description: 'Dieser Artikel beschreibt mehrere alternative Methoden, die Sie verwenden können, um Serviceverträge zu konvertieren, die Mehrwertsteuerbeträge enthalten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/07/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Dienstleistungsverträge konvertieren, die MwSt.-Beträge enthalten

Da das Werkzeug zum Ändern des MwSt.-Satzes keine Serviceverträge konvertieren, müssen diese Verträge manuell konvertiert werden. In diesem Artikel werden mehrere alternative Methoden beschrieben, die Sie für die Servicevertragkonvertierung verwenden können.  

> [!NOTE]  
> Dieser Artikel stellt einen allgemeinen Workflow bereit.  

 Nachfolgend wird beschrieben, wie eine Rechnung für einen vorausbezahlten Service-Vertrag korrigiert wird, die ein Jahr im Voraus erstellt wurde.  

> [!NOTE]  
> Für dieses Beispiel müssen Sie Ihr Arbeitsdatum in 01.01.2017 ändern.  

## So korrigieren Sie eine Rechnung für einen vorausbezahlten Servicevertrag  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Vertragsverwaltung** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie unter **Listen** die Option **Serviceverträge** aus.  
3. Erstellen Sie eines neuen vorausbezahlten Servicevertrags. Geben Sie als Startdatum **01.01.2017** und als Fakturierungsjahr für Debitor **20000** ein.  
4. Um den Vertrag zu unterzeichnen, wählen Sie die Aktion **Vertrag unterschreiben**.  
5. Erstellen Sie eine Servicerechnung.
6. Die Rechnung wird als nicht gebuchte Servicerechnung aufgelistet. Um die Servicerechnung anzuzeigen, wählen Sie die Aktion **Service**, wählen Sie die Aktion **Vertragsmanagement** und dann die Aktion **Serverechnungen**.  
7. Buchen Sie die Servicerechnung.  

> [!NOTE]  
> Ändern Sie die nicht gebuchte Servicerechnung nicht. Da die Serviceposten erstellt werden, wenn die Rechnung erstellt wird, ändert eine Änderung in der nicht gebuchten Rechnung nicht die bereits erstellten Serviceposten. Die MwSt.-Posten werden allerdings erstellt, wenn die Rechnung gebucht wird. So können Sie die allgemeine Produktbuchungsgruppe und die GSP-Produktbuchungsgruppe auf der nicht gebuchten Servicerechnung ändern.  

### So erstellen Sie eine Gutschrift für MwSt.-Differenzen 
 
Nachfolgend wird beschrieben, wie eine Gutschrift erstellt wird, die nur die MwSt.-Differenz für die bereits fakturierte Periode enthält, die am **01.07.2017** beginnt. In diesem Beispiel wird der MwSt.-Betrag nur auf das Finanzmanagement-Modul gebucht, nicht auf das Service-Modul. Die MwSt.-Posten, die mit dem Serviceposten verknüpft sind, werden nicht korrigiert.  

1. Erstellen Sie ein neues Sachkonto für die MwSt.-Differenz. Dieses Konto wird für die direkte Buchung der MwSt.-Korrektur verwendet.  
2. Fügen Sie der MwSt.-Buchung eine neue Zeile hinzu.  

## So erstellen Sie Vertragsablaufdaten in Vertragszeilen  

Die folgende Vorgehensweise beschreibt, wie Sie neue Verträge erstellen, indem sie in Servicevertragszeilen mit Kontaktablaufdaten arbeiten.  

1. Auf der Seite **Servicevertag** legen Sie das Vertragsablaufdatum auf **30.06.2017** fest.  
2. Wählen Sie die Aktionen **Verkaufsgutschrift erstellen** aus, um automatisch eine Gutschrift für Juli 2017 bis Dezember 2017 zu erstellen.  
3. Da der Vertrag abgelaufen ist, müssen Sie einen neuen Vertrag für die Periode mit dem neuen Mehrwertsteuersatz für 1. Juli 2017 bis 31. Dezember 2017 erstellen.  

### Eine neue Gutschrift erstellen:  

Nachfolgend wird beschrieben, wie eine neue Gutschrift mithilfe des Batchauftrags **Vorausbez. Vertragsposten holen** erstellt wird. Posten, die Sie nicht von Januar 2017 bis Juni 2017 korrigieren möchten, werden gelöscht.  

1. Führen Sie das Werkzeug zum Ändern des MwSt.-Satzes am 1. Juli 2017 aus. Die allgemeine Produktbuchungsgruppe oder die MwSt-Produktbuchungsgruppe werden geändert. Weitere Informationen Sie unter [Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md).  
2. Nachdem Sie das Werkzeug zum Ändern des MwSt.-Satzes ausgeführt haben, können Sie ein Vertragsablaufdatum für den Servicevertrag eingeben. Sie können die Servicevertragszeile jetzt löschen und eine neue Zeile erstellen, die mit der alten identisch ist.  
3. Erstellen Sie eine neue Rechnung für die Periode von Januar 2017 bis Dezember 2012 unter Verwendung des neuen Mehrwertsteuersatzes.  
4. Um eine weitere Gutschrift zu erstellen, wählen Sie auf der Seite **Servicegutschriften** die Aktion **Neu**, um eine neue Servicegutschrift zu erstellen.  
5. Wählen Sie die **Vorausbez. Vertragsposten holen** Aktion aus.  
6. Nachdem die Konvertierung abgeschlossen ist, sind MwSt.- und Serviceposten korrekt.  

## Siehe auch  

[Mit Dienstleistungsverträgen und Dienstleistungsvertragsangeboten arbeiten](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Finanzen](finance.md)  
[Melden von MwSt. an die Steuerbehörden](finance-how-report-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]