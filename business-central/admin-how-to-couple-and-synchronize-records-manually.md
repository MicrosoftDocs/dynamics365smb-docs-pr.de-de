---
title: Koppeln und Synchronisieren (enthält Video)
description: 'Die Synchronisierung einer Integrationstabellenzuordnung ermöglicht die Datensynchronisierung in allen Datensätzen in einer Tabelle in Business Central und der Dynamics 365 Sales-Tabellen, die gekoppelt sind.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'crm, sales, couple, decouple, synchronize'
ms.search.form: '6250,'
---

# <a name="couple-and-synchronize-records-between-dataverse-and-business-central"></a>Datensätze zwischen Dataverse und Business Central koppeln und synchronisieren

Dieses Thema beschreibt, wie man einen oder mehrere Datensätze in [!INCLUDE[prod_short](includes/prod_short.md)] mit Datensätzen in Dataverse oder [!INCLUDE[crm_md](includes/crm_md.md)] koppelt. Durch das Koppeln der Datensätze können Sie Dataverse-Informationen aus [!INCLUDE[prod_short](includes/prod_short.md)] anzeigen und umgekehrt. Die Kopplung ermöglicht Ihnen außerdem, Daten zwischen den Datensätzen zu synchronisieren. Sie können vorhandene Datensätze koppeln, oder Sie erstellen und koppeln neue Datensätze.

> [!NOTE]
> Die Kopplung und Synchronisierung von Daten ist nur verfügbar, wenn Ihr Systemadministrator eine Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und Dataverse oder [!INCLUDE[crm_md](includes/crm_md.md)] hergestellt hat. Eine schnelle Art dies sicherzustellen ist, die Karte **Debitor** zu öffnen und nach der **Kopplung einrichten**-Aktion zu suchen. Wenn die Aktion verfügbar ist, sind die Apps verbunden.

## <a name="video-example"></a>Video-Beispiel

Dieses Video zeigt die Kopplung und Synchronisierung von Daten im Rahmen einer Integration in [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>So koppeln Sie einen Datensatz

1. In [!INCLUDE[prod_short](includes/prod_short.md)] öffnen Sie die Karte für den Datensatztyp, den Sie koppeln möchten. Zum Beispiel den die Debitor- oder Kontaktkarte.  

    Sie können auch einfach die Listenseite öffnen und den Datensatz auswählen, den Sie koppeln möchten.  

2. Wählen Sie die **Kopplung einrichten**-Aktion aus.  
3. Füllen Sie die Felder aus, und wählen Sie dann **OK** aus.  

## <a name="to-synchronize-a-single-record"></a>So synchronisieren Sie einen einzelnen Datensatz

1. In [!INCLUDE[prod_short](includes/prod_short.md)] öffnen Sie die Karte für den Datensatztyp, den Sie koppeln möchten. Zum Beispiel den die Debitor- oder Kontaktkarte.  
2. Wählen Sie die **Jetzt synchronisieren**-Aktion aus.  
3. Wenn ein Datensatz in eine Richtung synchronisiert werden kann, wählen Sie die Option, die die Richtung der Datenaktualisierung angibt, und wählen Sie dann **OK**.  

## <a name="to-synchronize-a-single-record-from-"></a>So synchronisieren Sie einen einzelnen Datensatz von [!INCLUDE[crm_md](includes/crm_md.md)] aus

1. Öffnen Sie in [!INCLUDE[crm_md](includes/crm_md.md)] das Formular für den Datensatz, den Sie koppeln möchten. Zum Beispiel das Formular „Kontokarte“ oder „Kontaktkarte“.  
2. Wählen Sie die Aktion **[!INCLUDE[prod_short](includes/prod_short.md)]** in der Multifunktionsleiste, um den Datensatz automatisch zu öffnen und zu koppeln.

    > [!Note]
    > Sie können einen einzelnen Datensatz von [!INCLUDE[crm_md](includes/crm_md.md)] nur dann automatisch synchronisieren, wenn **Nur gekoppelte Datensätze synchronisieren** deaktiviert ist und die Synchronisierungsrichtung auf der Seite **Integrationstabellenzuordnung** für den Datensatz auf **Bidirektional** oder **Aus Integrationstabelle** eingestellt ist. Weitere Informationen finden Sie unter [Zuordnen der zu synchronisierenden Tabellen und Felder](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

## <a name="to-couple-multiple-records-using-match-based-coupling"></a>So koppeln Sie mehrere Datensätze mithilfe der abgleichsbasierten Kopplung

Definieren Sie die zu synchronisierenden Daten einer Entität, z.B. einen Debitor oder einen Kontakt, indem Sie Datensätze auf der Grundlage von Übereinstimmungen koppeln. Sie können die Übereinstimmungen verfeinern, indem Sie bei der Suche zwischen Groß- und Kleinschreibung unterscheiden und jeder Übereinstimmung eine Priorität zuweisen. Wenn keine Übereinstimmung gefunden wird, können Sie auch angeben, dass Sie die Entität in Dataverse erstellen möchten. Weitere Informationen finden Sie unter [Anpassen Kopplung basierend auf Übereinstimmung](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

> [!NOTE]
> Der Prozess „Kopplung basierend auf Übereinstimmung“ überspringt Datensätze, die bereits abgeglichen sind. Um diese Datensätze einzubeziehen, wenn Sie „Kopplung basierend auf Übereinstimmung“ ausführen, entkoppeln Sie die Datensätze, und versuchen Sie es dann erneut. Weitere Informationen zum Entkoppeln von Datensätzen finden Sie unter [Entkoppeln von Datensätzen](#uncoupling-records).

1. Öffnen Sie in [!INCLUDE[prod_short](includes/prod_short.md)] die Listenseite für den Datensatz, beispielsweise die Listenseiten "Debitoren" oder "Kontakte".
2. Wählen Sie die Aktion **Abgleichsbasierte Kopplung**.
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-synchronize-multiple-records"></a>So synchronisieren Sie mehrere Datensätze

1. Öffnen Sie in [!INCLUDE[prod_short](includes/prod_short.md)] die Listenseite für den Datensatz, beispielsweise die Seiten Debitoren oder Kontakte.  
2. Wählen Sie die Datensätze aus, die Sie synchronisieren möchten, und wählen Sie die Aktion **Jetzt synchronisieren** aus.  
3. Wenn Datensätze in eine Richtung synchronisiert werden können, wählen Sie die Option, die die Richtung angibt, und wählen Sie dann **OK**.  

## <a name="bulk-insert-and-couple-records"></a>Masseneinfügung und Koppeln von Datensätzen

Wenn Sie über eine große Anzahl von Dataverse-Entitäten verfügen, die Datensätzen in [!INCLUDE [prod_short](includes/prod_short.md)] entsprechen, können Sie sie in großen Mengen einfügen und koppeln. Beispielsweise möchten Sie möglicherweise Datensätze massenhaft einfügen und koppeln, wenn Sie die Synchronisierung zum ersten Mal einrichten.

Sie verwenden den **Datenimport-Assistenten** im **Microsoft Power Platform Admin Center**.

Im folgenden Beispiel wird beschrieben, wie Sie Debitoren per Massenvorgang einfügen und mit Konten in Dataverse koppeln. Verwenden Sie denselben Prozess für andere Typen von Entitäten, wie z. B. Kreditoren, Artikel und Ressourcen.

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Kunden** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **In Excel öffnen**, um Debitorendaten in Excel zu öffnen. <!--Don't they need to choose the customers that they want to import to Dataverse?-->
3. Um Daten der Entität **Konto** in Dataverse zuzuordnen und zu importieren, befolgen Sie die unter [Importieren Sie alle Daten (Datensatztypen) aus verschiedenen Quellen](/power-platform/admin/import-data-all-record-types) beschriebenen Schritte.  

    Wenn die Konto-Entität eine **bcbi_companyid**-Spalte hat, stellen Sie beim Zuordnen der Datenspalten sicher, dass der Import die entsprechende Unternehmens-ID in der Spalte für jeden importierten Datensatz zuweist. Gehen Sie folgendermaßen vor, um die Unternehmens-ID in [!INCLUDE [prod_short](includes/prod_short.md)] zu finden:

    1. Öffnen Sie die Seite **Integrationstabellenzuordnungen**.
    2. Wählen Sie die Zuordnung **DEBITOR** und dann **Liste bearbeiten** aus.
    3. Scrollen Sie nach rechts und wählen Sie die Schaltfläche Bearbeiten unterstützen :::image type="icon" source="media/assist-edit-icon.png" border="false"::: im Feld **Integrationstabellenfilter** aus. Dies zeigt den Standardfilter für die Debitorenzuordnung und enthält die Firmen-ID. Die Unternehmens-ID ist der erste Teil des Werts. Kopieren Sie nur diesen Teil und ignorieren Sie die Nullen. Das folgende Beispiel hebt den zu kopierenden Teil hervor.

    :::image type="content" source="media/dataverse-company-id-guid.png" alt-text="Zeigt den zu kopierenden Teil der Firmen-ID an.":::

    > [!NOTE]
    > Nicht alle Namen von Dataverse-Entitäten und Business Central-Datensätzen stimmen überein. Überprüfen Sie je nachdem, was Sie importieren, ob die folgenden Spalten nach dem Import die folgenden Werte aufweisen:
    >
    >* Für Debitoren sollte die Spalte **CustomerTypeCode** **Debitor** enthalten.
    >* Für Kreditoren sollte die Spalte **CustomerTypeCode** **Kreditor** enthalten. 
    >* Für Artikel sollte die Spalte **ProductTypeCode** **Verkaufsbestand** enthalten.
    >* Für Ressourcen sollte die Spalte **ProductTypeCode** **Service** enthalten.
 
4. Nachdem Sie Daten in die Dataverse-Umgebung importiert haben, führen Sie in [!INCLUDE [prod_short](includes/prod_short.md)] die Schritte [So koppeln Sie mehrere Datensätze mithilfe der abgleichsbasierten Kopplung](#to-couple-multiple-records-using-match-based-coupling) aus, um die Dataverse-Entitäten mit [!INCLUDE [prod_short](includes/prod_short.md)]-Datensätzen zu koppeln. 

## <a name="uncoupling-records"></a>Kopplung von Datensätzen aufheben

Sie können einen oder mehrere Datensätze von Listenseiten oder der Seite **Fehler bei der Synchronisierung gekoppelter Daten** durch Auswahl einer oder mehrerer Zeilen und Auswahl von **Kopplung löschen** entkoppeln. Sie können auch alle Kupplungen für eine oder mehrere Tabellenzuordnungen auf der Seite **Zuordnungen der Integrationstabelle** entfernen.

## <a name="see-also"></a>Siehe auch

[Dynamics 365 Sales von Business Central aus verwenden](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
