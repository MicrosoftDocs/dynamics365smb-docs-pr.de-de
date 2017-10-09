---
title: "So werden MwSt.-Registrationsnummern überprüft | Microsoft Docs"
description: "Sie können einen EU-Webdienst verwenden, um sicherzustellen, dass die USt-IdNr., die Sie auf Debitoren-, Kreditoren- oder Kontaktkarten eingeben, gültig sind."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a>Vorgehensweise: Überprüfen der USt-IdNr.
Sie können einen EU-Webdienst verwenden, um sicherzustellen, dass die MwSt-IdNr., die Sie auf Debitoren-, Kreditoren- oder Kontaktkarten eingeben, gültig sind.  

 Wenn Sie das **MwSt-Identifikationsnr.** auf einer Karte ändern, auf der der Wert im Feld **Land/Regionencode** ein EU-Land/Region ist, wird die neue MwSt-Identifikationsnummer und Ihre Benutzer-ID im Feld **MwSt-Identifikationsnr.** protokolliert. Überpürfen Sie die MwSt-IdNr., indem Sie die **Steuernummer** prüfen-Schaltfläche im **MwSt Identifikations-Protokoll**-Fenster auswählen. Eine neue Zeile wird jedes Mal erzeugt, wenn Sie die Überprüfungsfunktion verwenden. Wenn die Nummer verifiziert werden konnte, enthält das **Status**-Feld **Gültig**. Wenn die Zahl nicht verifiziert werden konnte, enthält das **Status**-Feld **Ungültig**, und Sie müssen die Zahl im **MwSt Identifikationsnr.**-Feld auf der Karte ändern und die Überprüfungsfunktion erneut starten.  

 Die URL des Standardwebdiensts wird im Feld **MwSt Reg. Nr Prüfung URL** im Feld **Finanzbuchhaltung Einrichtung** eingerichtet.  

 In der **MwSt Registrierungsnummer-Format**-Tabelle können Sie für jedes Land/jede Region die verschiedenen Formate der MwSt-IdNr. ändern, die Benutzer im **MwSt-Registrierungsnummer**-Feld eingeben können.  

> [!WARNING]  
>  Dieser Webdienst verwendet das HTTP-Protokoll, d. h., dass die Daten, die durch den Service übertragen werden, nicht verschlüsselt werden.  

> [!NOTE]  
>  Möglicherweise treten Ausfallzeiten für diesen Service auf, für die Microsoft nicht verantwortlich ist, da der Service Teil eines breiten EU-Netzwerks nationaler MwSt.-Register ist.  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a>Überprüfen der USt-IdNr. aus einer Debitorenkarte  
Nachfolgend wird erläutert, wie einer MwSt-IdNr. eines Debitors überprüft wird. Die Schritte sind für einen Debitior ähnlich.   
1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kunden** ein. Wählen Sie dann den zugehörigen Link aus.  

2.  Öffnen Sie die Karte eines Debitors, auf der Sie die USt-IdNr. prüfen möchten.  

    > [!NOTE]  
    >  Das -Feld **Land-/Regionencode** der Debitorenkarte muss ein EU-Land/Region enthalten.  
3.  Wählen Sie im Inforegister **Rechnungsstellung** die Dropdownschaltfläche neben dem Feld **MwSt-Registrierungsnummer**aus.  

    Das **Protokoll MwSt-Registrierungs**-Fenster wird geöffnet und zeigt eine Zeile, in der das Feld **Status** **Nicht überprüft** enthält.  
4.  Wählen Sie die **Steuernummer prüfen** Aktion aus.  

     Eine neue Zeile wird erstellt, wo das Feld **Status** entweder **Gültig** oder **Ungültig** enthält.  
5.  Wenn das -**Status**Feld  **Ungültig** enthält, ändern Sie die Nummer im **MwSt**-Feld auf der Karte, und wiederholen Sie dann die Schritte 3 bis 4.  

## <a name="see-also"></a>Siehe auch  
[Finanzen](finance.md)  
[Vorgehensweise: Einen neuen Debitor registrieren](sales-how-register-new-customers.md)  
[Vorgehensweise: Einen neuen Kreditor registrieren](purchasing-how-register-new-vendors.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

