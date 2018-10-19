---
title: "Bevorzugte Methoden der Übermittlung von Verkaufsbelegen einrichten | Microsoft Docs"
description: "Beschreibt, wie Sie die gewünschte Methode jedes Debitors der Übermittlung von Verkaufsbelegen eingerichtet, z Buchen, PDF-Dateien, elektronischer Beleg, usw."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c18edefc22d96f2c4037f7f51cca488e04c35d92
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-document-sending-profiles"></a>Belegsendeprofile einrichten
Sie können jeden Debitor mit einer bevorzugten Methode der Übermittlung von Verkaufsbelegen einrichten, sodass Sie nicht jedes Mal eine Sendeoptionen auswählen müssen, wenn Sie die Schaltfläche **Buchen und senden** auswählen.

Im Fenster **Belegsendeprofile** richten Sie verschiedene **Dokumente-Sendeprofile** ein, die Sie aus dem Feld von einer Debitorenkarte auswählen können. Im Kontrollkästchen **Standard** geben Sie an, dass das Belegsendprofil das Standardprofil für alle Debitoren gilt, außer Debitoren, bei denen das Feld **Dokument-Sendeprofil** mit einem anderen Sendeprofil ausgefüllt ist.

Wenn Sie die Schaltfläche **Buchen und senden** für einen Verkaufsbeleg auswählen, wird im Dialogfeld **Buchungs- und Sendebestätigung** das verwendete Sendeprofil angezeigt. Dabei handelt es sich entweder um das für den Debitor eingerichtete oder um Standardprofil für alle Debitoren. In diesem Dialogfeld können Sie das Sendeprofil für den Verkaufsbeleg ändern. Weitere Informationen finden Sie unter [Verkaufsrechnungen](sales-how-invoice-sales.md).

## <a name="to-set-up-a-document-sending-profile"></a>Einrichten von Belegsendeprofilen
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Belegsendeprofil** ein, und wählen dann den zugehörigen Link aus.
2. Im Feld **Dokumentsendeprofile** wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a>Sendeprofil für eine Debitorenkarte festlegen
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Debitor** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie die Karte des Debitors, für den ein Sendeprofil eingerichtet werden soll.
3. Wählen Sie im Inforegister **Belegsendeprofil** ein Profil aus, das sie eingerichtet haben wie im vorigen Verfahren beschrieben.

## <a name="see-also"></a>Siehe auch
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

