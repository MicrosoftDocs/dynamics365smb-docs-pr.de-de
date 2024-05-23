---
title: Projektmontage
description: 'Erfahren Sie, wie Sie die Auftragsmontage für Projekte verwenden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 08/03/2022
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="assemble-to-project"></a>Projektmontage

Mit der Projektmontage können Sie die Bestandsverwaltung verbessern, indem Sie die Montage nur dann durchführen, wenn sie erforderlich ist.

Wenn Sie einen Artikel zur Auftragsmontage in einer Projektplanungszeile auswählen, erstellt [!INCLUDE [prod_short](includes/prod_short.md)] einen Montageauftrag. Der Montageauftrag basiert auf der Projektplanungszeile, und seine Zeilen basieren auf der Montagestückliste des Artikels. Weitere Informationen zu Montagestücklisten finden Sie unter [Arbeiten mit Montagestücklisten](assembly-how-work-assembly-boms.md). Die Menge der Komponenten in der Montagestückliste wird mit der Bestellmenge multipliziert. Die Seite **Auftragsmontagezeilen** zeigt Details zu den verknüpften Montageauftragszeilen. Die Details können Ihnen dabei helfen, den Montageartikel anzupassen. Wie im Verkauf können Sie verknüpfte Montageaufträge nicht direkt buchen. Weitere Informationen zu Montageaufträgen finden Sie unter [Verkaufen von Lagerartikeln in Auftragsmontage-Flows](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).

Montageaufträge sind für Projekte reserviert und [!INCLUDE [prod_short](includes/prod_short.md)] synchronisiert die Artikelverfolgung zwischen Projektplanungszeilen und Montageauftrag.

## <a name="integrate-with-warehouse-management"></a>In die Lagerverwaltung integrieren

Programmfertigung ist in Lagerverwaltungsfunktionen integriert, um die Montage und den Versand zu vereinfachen. Der Prozess trägt außerdem dazu bei, dass in den internen Lagerprozessen ein reibungsloser Ablauf von der Projektmontage bis zur Auslieferung gewährleistet ist. Weitere Informationen zu internen Lager-Flows für Projekte finden Sie unter [Flows für Produktion, Montage und Aufträge](design-details-internal-warehouse-flows.md#flows-to-and-from-assembly-in-a-basic-warehouse-configuration).

In der folgenden Tabelle werden die Lagerkonfigurationen beschrieben, die die Auftragsmontage unterstützen.

|Konfiguration  |Description  |
|---------|---------|
|**Keine Lagerabwicklung**|Verwenden Sie eine Projekterfassung, um die vollständige oder teilweise Nutzung zu buchen. Die Istmeldung und der Verbrauch von Komponenten werden automatisch für den Montageauftrag gebucht.         |
|**Lagerkommissionierung**|Verwenden Sie eine Lagerkommissionierung, um die vollständige oder teilweise Nutzung zu buchen. Die Istmeldung und der Verbrauch von Komponenten werden automatisch für den Montageauftrag gebucht.          |
|**Lagerkommissionierung**|Erstellen und registrieren Sie Lagerkommissionierungen für Komponenten und verwenden Sie dann eine Projekterfassung, um die Nutzung zu buchen. [!INCLUDE [prod_short](includes/prod_short.md)] prüft, ob die verbrauchten Montagekomponenten kommissioniert wurden. Die Istmeldung und der Verbrauch von Komponenten werden automatisch für den Montageauftrag gebucht.         |

## <a name="known-limitations"></a>Bekannte Einschränkungen

In diesem Abschnitt werden bekannte Einschränkungen für die Montage zu einem Projekt beschrieben.

* Das Feld **Menge für Auftragsmontage** ist für geschlossene Projekte nicht verfügbar.
* Für Lagerkommissionierungsszenarien kann **Menge für Auftragsmontage** entweder null oder gleich der Menge sein. Sie können Auftragsmontage und Lagermontage in einer Projektplanungszeile nicht kombinieren. Sie müssen separate Projektplanungszeilen erstellen.
* Die Auftragsmontage wirkt sich nicht auf abrechenbare Teile eines Projekts aus. In Verkaufsrechnungen ist eine Baugruppe enthalten, nicht jedoch ihre Komponenten. Sie können das Feld **Menge für Auftragsmontage** für abrechenbare Positionen nicht bearbeiten.
* Die Auftragsplanung und das Planungsarbeitsblatt sind hiervon nicht betroffen, da das Projekt als Eingabe für die Planung dient. Das Planungsmodul betrachtet die Montage als Bedarf.
* Sie können im Feld **Menge für Auftragsmontage** keine negative Menge eingeben.
* Sie können eine Montage nicht rückgängig machen.

## <a name="see-also"></a>Siehe auch

[Projektmanagement](projects-manage-projects.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Projekte erstellen](projects-how-create-jobs.md)
