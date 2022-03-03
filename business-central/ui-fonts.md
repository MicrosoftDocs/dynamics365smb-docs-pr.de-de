---
title: Verfügbare Schriftarten
description: Erfahren Sie mehr über die vorinstallierten Schriftarten, die Sie für Ihr externe Berichte verwenden können.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 11/30/2021
ms.author: edupont
ms.openlocfilehash: faa581a88a6c7503c34177db459345a24638a95a
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2022
ms.locfileid: "8334947"
---
# <a name="available-fonts"></a>Verfügbare Schriftarten

Die Onlineversion von [!INCLUDE[prod_short](includes/prod_short.md)] enthält vorinstallierte Schriftarten auf den Servern, die beim Generieren von Berichten verwendet werden können. In den folgenden Abschnitten wird erläutert, welche Schriftarten verfügbar sind.

> [!NOTE]
> Aus Sicherheits- und rechtlichen Gründen können Sie keine benutzerdefinierten Schriftarten in die [!INCLUDE[prod_short](includes/prod_short.md)]-Umgebung hochladen.

## <a name="document-fonts"></a>Dokumentschriftarten

Die folgenden Schriftarten sind installiert und können in Word- und RDLC-Berichtlayouts verwendet werden:

* Arial
* Konsolen
* Courier New
* Lucida Console
* Segoe Print
* Segoe Script
* Segoe UI
* Segoe UI Light
* Segoe UI Semilight
* Times New Roman

## <a name="fonts-for-checks"></a>Schriftarten für Schecks

MICR-Schriftarten (Magnetic Ink Character Recognition) sind installiert und können verwendet werden. Es werden sowohl der E-13B- als auch der CMC-7-Standard unterstützt.  

Zusätzlich zu MICR-Schriftarten stehen spezielle Sicherheitsschriftarten zur Verfügung, mit denen Text, Namen, Beträge und die Währungssymbole Dollar, Euro, Pfund und Yen generiert werden können, die nach dem Drucken eines Schecks nur schwer zu manipulieren sind.  

Weitere Informationen finden Sie unter [Scheck-Layout auswählen](finance-how-define-check-layouts.md).  

## <a name="fonts-for-barcodes"></a>Schriftarten für Barcodes
Schriftarten zum Generieren von Barcodes sind installiert und können sowohl in Word- als auch in RDLC-Berichtslayouts verwendet werden.

Die folgenden eindimensionalen Barcode-Symbologien werden unterstützt:
* Code 3 von 9 (Code 39)
* Code 128
* Code 93
* Codabar
* MSI
* Interleaved 2 von 5

Die folgenden zweidimensionalen Barcode-Symbologien werden unterstützt:
* Aztekisch
* Datenmatrix
* Maxicode
* PDF417
* QR

Weitere Informationen finden Sie unter [Barcode-Schriftarten mit Business Central Online](/dynamics365/business-central/dev-itpro/developer/devenv-report-barcode-fonts).

## <a name="see-also"></a>Siehe auch

[Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
[Ein Prüflayout auswählen](finance-how-define-check-layouts.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
[Barcode-Schriften mit Business Central Online](/dynamics365/business-central/dev-itpro/developer/devenv-report-barcode-fonts)

[!INCLUDE[footer-include](includes/footer-banner.md)]
