---
title: Geben Sie das Layout eines Schecks an| Microsoft Docs
description: Sie können Ihre Checks entwerfen und srucken in unterschiedliche Formaten, um Standardwerten zu entsprechen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 8346e8a868f73d3de729a56e86530048c58229aa
ms.sourcegitcommit: 3945f16d6d9c9853651e6291ce1465a44fd71fc8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "3458922"
---
# <a name="select-a-check-layout"></a>Ein Prüflayout auswählen
Sie können Ihre Schecks entwerfen, um sie den Vorgaben anzupassen, die von den lokalen Behörden festgelegt werden. Scheckbilder können in Englisch, Französisch oder Spanisch gedruckt werden.

Schecks können sowohl im USA- als auch im Kanada-Schecklayout, entweder im Scheck/Formular/Scheck-Format oder im Formular/Formular/Scheck-Format gedruckt werden.

## <a name="to-select-a-check-layout"></a>Ein Prüflayout auswählen
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Berichtsauswahlen – Bankkonto** ein, und wählen Sie dann den entsprechenden Link.
2. Auf der Seite **Berichts-Auswahl - Bankkonto** unter **Verwendung** wählen Sie **Scheck**.
3. Wählen Sie eine der folgenden Berichts-IDs:

| Berichts-ID | Berichtsname | Beschreibung |
| --- | --- | --- |
| 1401 |Aktivieren |Dieser Bericht wird standardmäßig verwendet. |
| 10411 |Scheck (Formular/Formular/Scheck) |Dieser Bericht dient dazu, Schecks im Formular/Formular/Scheck-Format zu drucken. |
| 10412 |Scheck (Formular/Scheck/Formular) |Dieser Bericht dient dazu, Schecks im Formular/Scheck/Formular-Format zu drucken. |
| 10413 |Drei Schecks pro Seite |Dieser Bericht ist dafür ausgelegt, drei Schecks auf jeder Seite zu drucken. |

Wenn Sie Schecklayouts eingerichtet haben, können Sie Schecks auf de Seite **Zahlung Buch.-Blatt** drucken. Weitere Informationen finden Sie unter [Arbeiten mit Schecks](payables-how-work-checks.md).

Verwenden Sie dazu entweder die Word- oder die RDLC-Integration, um eines dieser Standardprüflayouts zu ändern. Weitere Informationen finden Sie unter [Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md).

## <a name="using-micr-and-security-fonts"></a>Verwenden von MICR- und Sicherheitsschriftarten
Die Onlineversion von [!INCLUDE[d365fin](includes/d365fin_md.md)] enthält vorinstallierte Schriftarten auf den Servern, die beim Definieren von Prüflayouts verwendet werden können. Im Folgenden wird erläutert, welche Schriftarten verfügbar sind, und es werden Links zu detaillierten Informationen der Drittanbieter der Schriftarten angezeigt.

> [!Important]
> MICR- und Schecksicherheits-Schriftarten in Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)] sind in einem Schriftartpaket von IDAutomation.com, Inc. lizenziert. Diese Produkte dürfen nur als Teil von und in Verbindung mit Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet werden.

In Update 15.3 und höher sind MICR-Schriftarten (Magnetic Ink Character Recognition) installiert und können verwendet werden. Es werden sowohl der E-13B- als auch der CMC-7-Standard unterstützt. Zusätzlich zu MICR-Schriftarten stehen spezielle Sicherheitsschriftarten zur Verfügung, mit denen Text, Namen, Beträge und die Währungssymbole Dollar, Euro, Pfund und Yen generiert werden können, die nach dem Drucken eines Schecks nur schwer zu manipulieren sind.

> [!NOTE]
> Aus Sicherheits- und rechtlichen Gründen können Sie keine benutzerdefinierten Schriftarten in die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Umgebung hochladen.

### <a name="micr-e-13b-specifications"></a>MICR E-13B-Spezifikationen
Im Folgenden werden die Spezifikationen für die MICR E-13B-Schriftarten zusammengefasst, die beim Kalibrieren von Schriftarten für Schecklayouts mit bestimmten MICR-Druckern hilfreich sein können.

![MICR E-13B-Spezifikationen](media/font_MICR_E-13B_Specifications.png "MICR E-13B-Spezifikationen")

### <a name="delimiter-characters"></a>Trennzeichen
![Trennzeichen](media/font-micr-letters.png "Trennzeichen")

Die vollständige Spezifikation der MICR E-13B-Schriftarten finden Sie in der Dokumentation des Lieferanten auf dieser Website: (https://www.idautomation.com/micr-fonts/e13b/).

### <a name="micr-cmc-7-specifications"></a>MICR CMC-7-Spezifikationen
Die folgenden CMC-7-Schriftarten sind in [!INCLUDE[d365fin](includes/d365fin_md.md)] online verfügbar:

- IDAutomationCMC7
- IDAutomationCMC7n10
- IDAutomationCMC7n25
-   IDAutomationCMC7n40

Im Folgenden werden die Spezifikationen für die MICR CMC-7-Schriftarten zusammengefasst, die beim Kalibrieren von Schriftarten für Schecklayouts mit bestimmten MICR-Druckern hilfreich sein können.

![MICR CMC-7-Spezifikationen](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7-Spezifikationen")

### <a name="delimiter-characters"></a>Trennzeichen
![Trennzeichen](media/font-cmc7-letters.png "Trennzeichen")

Die vollständige Spezifikation der MICR CMC-7-Schriftarten finden Sie in der Dokumentation des Lieferanten auf dieser Website: (http://www.idautomation.com/micr-fonts/cmc7/).

### <a name="secure-font-specifications"></a>Spezifikationen für sichere Schriftarten
Im Folgenden werden die Spezifikationen für die Schecksicherheits-Schriftarten zusammengefasst, die beim Kalibrieren von Schriftarten für Schecklayouts mit bestimmten MICR-Druckern hilfreich sein können.

![Spezifikationen für Schecksicherheits-Schriftarten](media/font_check-security-font_Specifications.png "Spezifikationen für Schecksicherheits-Schriftarten")

Die vollständige Spezifikation der Schecksicherheits-Schriftarten finden Sie in der Dokumentation des Lieferanten auf dieser Website: (https://www.idautomation.com/security-fonts/).

Schriftarten für andere Zwecke sind auch in [!INCLUDE[prodshort](includes/prodshort.md)] verfügbar. Weitere Informationen finden Sie unter [Verfügbare Schriftarten](ui-fonts.md)

## <a name="see-also"></a>Siehe auch
[Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md)  
[Schriftarten in Business Central](ui-fonts.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Abstimmen von Bankkonten](bank-manage-bank-accounts.md)   
[Abschließen von Periodenabschlüssen](year-how-complete-period-end-processes.md)  
[Arbeiten mit [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)
