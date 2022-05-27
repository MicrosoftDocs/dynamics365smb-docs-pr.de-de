---
author: edupont04
ms.topic: include
ms.date: 05/09/2022
ms.author: edupont
ms.openlocfilehash: f002086780e694ad80f2b5c80e942ab411de1948
ms.sourcegitcommit: 2fa712d0aabe4287ebd4454c28d142d6baf045a0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/09/2022
ms.locfileid: "8732964"
---
Möglicherweise werden in der Liste **Benutzer** andere Benutzer als die Ihres eigenen Unternehmens angezeigt. Wenn sich ein delegierter Administrator eines Wiederverkaufspartnerunternehmens in einer [!INCLUDE [prod_short](prod_short.md)]-Umgebung im Auftrag seines Debitors anmeldet, wird dieser automatisch als Benutzer in [!INCLUDE [prod_short](prod_short.md)] erstellt. Auf diese Weise werden die von einem delegierten Administrator ausgeführten Aktionen in [!INCLUDE [prod_short](prod_short.md)] protokolliert, z. B. Buchungsbelege, und mit ihrer Benutzer-ID verknüpft.  

Mit der Funktion *Granular delegated admin privileges (GDAP)* wird der Benutzer in der Liste **Benutzer** angezeigt und kann beliebigen Berechtigungen zugewiesen werden. Sie werden nicht mit Namen und anderen personenbezogenen Informationen angezeigt, sondern mit hrem Unternehmensnamen und einer eindeutigen ID. Sowohl interne als auch externe Administratoren können diese Benutzer in der Liste **Benutzer** anzeigen, und sie haben einen umfassenden Einblick in die Aktionen, die diese Benutzer beispielsweise über das [Änderungsprotokoll](../across-log-changes.md) durchführen. Der tatsächliche Name dieser Benutzer wird jedoch nicht angezeigt. GDAP-Benutzer werden mit Benutzernamen im folgenden Format aufgelistet: `User123456@partnerdomain.com`. Sie haben möglicherweise einen Benutzernamen, der den Unternehmensnamen des Partners widerspiegelt, und die E-Mail-Adresse ist nicht die tatsächliche E-Mail-Adresse der Person. Auf diese Weise geben die GDAP-Benutzerkonten keine personenbezogenen Informationen preis. Wenn Sie herausfinden möchten, wer hinter einem solchen Pseudonym steckt, müssen Sie sich an das Unternehmen wenden, für das dieser Benutzer arbeitet oder gearbeitet hat.  
