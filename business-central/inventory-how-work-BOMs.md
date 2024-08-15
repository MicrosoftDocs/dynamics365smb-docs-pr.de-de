---
title: Mit Stücklisten arbeiten
description: 'Sie erstellen eine Montagestückliste oder eine Fertigungsstückliste, um die Komponenten und Ressourcen anzuzeigeb, die benötigt werden, um den Artikel zusammenzufügen, die die Stückliste darstellt.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bills of material, assembly BOM, production BOM,'
ms.search.form: null
ms.date: 06/06/2024
ms.service: dynamics-365-business-central
---
# <a name="work-with-bills-of-material"></a>Mit Stücklisten arbeiten

Verwenden Sie Stücklisten (BOMs), um beispielsweise Oberartikel zu strukturieren, die aus anderen Artikeln oder nach Ressourcen oder Arbeitsplätze aus Komponenten montiert oder gefertigt werden müssen.

## <a name="assembly-boms-or-production-boms"></a>Montagestücklisten oder Fertigungsstücklisten

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt zwei verschiedene Arten von Stücklisten:

| Stücklistentyp | Allgemeine Kategorie | Beispiel |
| -------- | ---------------- | ------- |
| [Montagestücklisten](assembly-how-work-assembly-boms.md) | Lager/Montage | Artikel, die aus anderen Artikeln bestehen, die mit einfachen oder keinen Ressourcen zusammengesetzt sind. |
| [Produktionsstücklisten](production-how-to-create-production-boms.md) | Herstellung/Produktion | Artikel, die aus verschiedenen Komponenten und Unterbaugruppen bestehen und in einem Arbeits- oder Maschinenzentrum hergestellt werden. |

Sie verwenden Montageaufträge zum Herstellen von Endprodukten aus Komponenten in einem einfachen Prozess, der von einer oder mehreren Basisressourcen ausgeführt werden kann, bei denen es sich nicht um Maschinen oder Arbeitsplätze handelt, oder der ohne Ressourcen auskommt. Beispielsweise könnte ein Montagevorgang lauten, zwei Weinflaschen und ein Paket Kaffee zu kommissionieren und sie als Geschenkartikel zu verpacken.  

Eine Montagestückliste liefert die Masterdaten, die festlegen, welche Komponentenartikel in einen montierten Endartikel enthalten sind und welche Ressourcen verwendet werden, um den Montageartikel zu montieren. Wenn Sie in der Kopfzeile eines neuen Montageauftrags den Montageartikel und die Menge eingeben, werden die Montageauftragszeilen automatisch aus der Montagestückliste übernommen und pro Komponente oder Ressource als eine Montageauftragszeile dargestellt. Erfahren Sie mehr unter [Montageverwaltung](assembly-assemble-items.md).

Fertigungsaufträge werden für die Produktion von Endartikeln aus Komponenten in einem komplexen Prozess verwendet, für den ein FA-Arbeitsplan und Arbeitsplätze oder Arbeitsplatzgruppen erforderlich sind, die Fertigungskapazitäten darstellen. Ein Fertigungsvorgang könnte beispielsweise darin bestehen, Stahlplatten in einem Arbeitsgang zuzuschneiden, sie im folgenden Arbeitsgang zu schweißen und den Endartikel im letzten Arbeitsgang zu lackieren. Erfahren Sie mehr unter [Herstellung](production-manage-manufacturing.md).

Eine Fertigungsstückliste liefert die Masterdaten, die einen Fertigungsartikel und die enthaltenen Komponenten definieren, die in diese einfließen. Für Montageartikel muss die Fertigungsstückliste zertifiziert und dem Fertigungsartikel zugeordnet werden, bevor sie in einem Fertigungsauftrag verwendet werden kann. Wenn Sie den Fertigungsartikel entweder manuell in einer FA-Zeile eingeben oder indem Sie den Auftrag aktualisieren, wird der Inhalt der Fertigungsstückliste zu den Fertigungsauftragskomponenten. Erfahren Sie mehr unter [Produktionsstücklisten erstellen](production-how-to-create-production-boms.md).

Das Ressourcenkonzept ist in der Produktion weitergehender als in der Montageverwaltung. Arbeitsplätze und Arbeitsplatzgruppen fungieren als Ressourcen. Die Vorgänge, die den Ressourcen in Produktionsarbeitsplänen zugeordnet sind, stellen Produktionsschritte dar. Erfahren Sie mehr unter [Weiterleitungen erstellen](production-how-to-create-routings.md).

Montageaufträge und Fertigungsaufträge können direkt mit Verkaufsaufträgen verknüpft sein. Sie können jedoch nur Montageaufträge nutzen, um den Endartikel direkt für eine Debitorenanfrage im Verkaufsauftrag anzupassen.

## <a name="see-also"></a>Siehe auch

[Arbeiten mit Montagestücklisten](assembly-how-work-assembly-boms.md)    
[Erstellen von Produktionsstücklisten](production-how-to-create-production-boms.md)    
[Neue Artikel registrieren](inventory-how-register-new-items.md)    
[Produktvarianten verwalten](inventory-item-variants.md)    
[Lagerbest](inventory-manage-inventory.md)    
[Fertigung](production-manage-manufacturing.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
