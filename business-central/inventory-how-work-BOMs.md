---
title: Mit Fertigungsstücklisten arbeiten
description: 'Sie erstellen eine Montagestückliste oder eine Fertigungsstückliste, um die Komponenten und Ressourcen anzuzeigeb, die benötigt werden, um den Artikel zusammenzufügen, die die Stückliste darstellt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bills of material, assembly BOM, production BOM,'
ms.search.form: null
ms.date: 09/26/2022
ms.author: bholtorf
---
# Mit Fertigungsstücklisten arbeiten

Verwenden Sie Stücklisten (BOMs), um beispielsweise Oberartikel zu strukturieren, die aus anderen Artikeln oder nach Ressourcen oder Arbeitsplätze aus Komponenten montiert oder gefertigt werden müssen.

## Montagestücklisten oder Fertigungsstücklisten

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt zwei verschiedene Arten von Stücklisten:

| Stücklistentyp | Allgemeine Kategorie | Beispiel |
| -------- | ---------------- | ------- |
| [Montagestücklisten](assembly-how-work-assembly-boms.md) | Lager/Montage | Artikel, die aus anderen Artikeln bestehen, die mit einfachen oder keinen Ressourcen zusammengesetzt sind. |
| [Produktionsstücklisten](production-how-to-create-production-boms.md) | Herstellung/Produktion | Artikel, die aus verschiedenen Komponenten und Unterbaugruppen bestehen und in einem Arbeits- oder Maschinenzentrum hergestellt werden. |

Montageaufträge werden für die Produktion von Endartikeln aus Komponenten in einem einfachen Prozess verwendet, der mit einer oder mehreren grundlegenden Ressourcen, die keine Maschinen oder Arbeitsplatzgruppen sind, oder ganz ohne Ressourcen durchgeführt werden kann. Beispielsweise könnte ein Montagevorgang lauten, zwei Weinflaschen und ein Paket Kaffee zu kommissionieren und sie als Geschenkartikel zu verpacken.  

Eine Montagestückliste liefert die Masterdaten, die festlegen, welche Komponentenartikel in einen montierten Endartikel enthalten sind und welche Ressourcen verwendet werden, um den Montageartikel zu montieren. Wenn Sie im Kopf eines neuen Montageauftrags den Montageartikel und die Menge eingeben, werden die Montageauftragszeilen automatisch aus der Montagestückliste übernommen und pro Komponente oder Ressource als eine Montageauftragszeile dargestellt. Erfahren Sie mehr unter [Montageverwaltung](assembly-assemble-items.md).

Fertigungsaufträge werden für die Produktion von Endartikeln aus Komponenten in einem komplexen Prozess verwendet, für den ein FA-Arbeitsplan und Arbeitsplätze oder Arbeitsplatzgruppen erforderlich sind, die Fertigungskapazitäten darstellen. Ein Fertigungsvorgang könnte beispielsweise darin bestehen, Stahlplatten in einem Arbeitsgang zuzuschneiden, sie im folgenden Arbeitsgang zu schweißen und den Endartikel im letzten Arbeitsgang zu lackieren. Erfahren Sie mehr unter [Herstellung](production-manage-manufacturing.md).

Eine Fertigungsstückliste liefert die Masterdaten, die einen Fertigungsartikel und die enthaltenen Komponenten definieren, die in diese einfließen. für Montageartikel muss die Fertigungsstückliste zertifiziert und dem Fertigungsartikel zugeordnet werden, bevor sie in einem Fertigungsauftrag verwendet werden kann. Wenn Sie den Fertigungsartikel entweder manuell in einer FA-Zeile eingeben oder indem Sie den Auftrag aktualisieren, wird der Inhalt der Fertigungsstückliste zu den Fertigungsauftragskomponenten. Erfahren Sie mehr unter [Produktionsstücklisten erstellen](production-how-to-create-production-boms.md).

Das Ressourcenkonzept ist in der Produktion weitergehender als in der Montageverwaltung. Arbeitsplatzgruppen und Arbeitsplätze arbeiten als Ressourcen und Produktionsschritte werden durch Arbeitsgänge dargestellt, die Ressourcen in den Arbeitsplänen zugeordnet sind. Erfahren Sie mehr unter [Weiterleitungen erstellen](production-how-to-create-routings.md).

Montageaufträge und Fertigungsaufträge können direkt mit Verkaufsaufträgen verknüpft sein. Sie können jedoch nur Montageaufträge nutzen, um den Endartikel direkt für eine Debitorenanfrage im Verkaufsauftrag anzupassen.

## Siehe auch

[Arbeiten mit Montagestücklisten](assembly-how-work-assembly-boms.md)  
[Fertigungsauftrag erstellen](production-how-to-create-production-boms.md)  
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Produktvarianten verwalten](inventory-item-variants.md)  
[Bestand](inventory-manage-inventory.md)  
[Produktion](production-manage-manufacturing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
