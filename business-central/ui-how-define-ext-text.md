---
title: Zusätzliche Zeilen hinzufügen, um Zusatztext für Beschreibungen zu definieren
description: Sie können zusätzliche Zeilen hinzufügen, um den Standardtext zu erweitern, der einen Artikel, ein Sachkonto oder andere Daten beschreibt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/08/2020
ms.author: sgroespe
ms.openlocfilehash: 0b611a4f2bcabec7cda408790ab659c6cf3f8e97
ms.sourcegitcommit: 8b2f02dd5189c46ecff33c07223ed62b36842d34
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2020
ms.locfileid: "3542567"
---
# <a name="add-extended-text"></a>Textbaustein hinzufügen

Sie können die Beschreibung für Artikel, Lagerhaltungsdaten, Sachkonten und Ressourcen erweitern, indem Sie zusätzliche Zeilen als Textbaustein hinzufügen. Sie können auch Bedingungen für die Verwendung der zusätzlichen Zeilen festlegen.  

Im folgenden Abschnitt wird beschrieben, wie Sie einer Beschreibung eines Elements einen Textbaustein hinzufügen. Die gleichen Schritte gelten jedoch für Lagerhaltungsdaten, Sachkonten und Ressourcen.  

## <a name="to-define-extended-text-for-an-description"></a>So definieren Sie Textbausteine für eine Beschreibung

1. Öffnen Sie die Karte eines Artikels, dem Sie den zusätzlichen Text hinzufügen möchten, und wählen Sie dann die Aktion **Textbaustein** aus.
2. Füllen Sie die Felder **Code** und **Beschreibung** aus.
3. Wählen Sie **Neu** aus.
4. Füllen Sie das Feld **Sprachcode** oder das Kontrollkästchen **Alle Sprachcodes** aus, wenn Sie mit Sprachcodes arbeiten.
5. Füllen Sie die Felder **Startdatum** und/oder **Enddatum** aus, wenn Sie die Verwendung des Textbausteins zeitlich einschränken möchten.
6. Geben Sie im Feld **Text** den erweiterten Text ein.
7. Wählen Sie die entsprechenden Kontrollkästchen für die Belegarten, für die die Textbausteine gedruckt werden sollen.
8. Schließen Sie die Seite.

Sie können diesen Textbaustein jetzt Dokumenten hinzufügen. Im folgenden Verfahren wird erläutert, wie Sie einem Verkaufsauftrag einen Textbaustein hinzufügen. Die gleichen Schritte gelten jedoch auch für alle anderen Dokumente, die Sie für den Textbaustein angegeben haben.  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a>Einen erweiterten Elementtext in einer Verkaufsauftragszeile hinzufügen

1. Öffnen Sie einen Verkaufsauftrag mit einer Verkaufszeile für einen Artikel, die den Textbaustein definiert hat. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)
2. Wählen Sie die betreffende Zeile aus, und wählen Sie die **Textbaustein einfügen** Aktion aus.

## <a name="see-also"></a>Siehe auch

[Bestand einrichten](inventory-setup-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
