---
title: Info zu Kosten des beendeten FA
description: Die Fertigstellung des Produktionsauftrags ist der Schlüssel zur Vervollständigung der Kalkulation eines Elements der Produktion. Die endgültigen Kosten werden im Batchauftrag „Lagerreg. fakt. Einst. Preise“ kalkuliert.
author: SorenGP
ms.topic: conceptual
ms.search.form: 99000867
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="about-finished-production-order-costs"></a><a name="about-finished-production-order-costs"></a><a name="about-finished-production-order-costs"></a>Info zu Kosten des beendeten FA

Das Beenden eines Fertigungsauftrages ist eine wichtige Aufgabe beim Abschließen der Gesamtkostenbewertung des Artikels, der gefertigt wird. Endeinstandspreise einschließlich Abweichungen in einer Einstandspreisumgebung; Ist-Kosten in einer FIFO-, Durchschnitt- oder LIFO-Einstandspreisumgebung, werden mit der Stapelverarbeitung **Artikelkosteneinträge anpassen** berechnet, die eine finanzielle Abstimmung der Kosten der Artikelfertigung ermöglicht. Damit ein Fertigungsauftrag für die Einstandspreisregulierung berücksichtigt wird, muss er den Status **Beendet** haben. Es ist daher unbedingt erforderlich, dass nach Beendigung die Änderung des Status eines Fertigungsauftrags in **Beendet** erfolgt.  

## <a name="example"></a><a name="example"></a><a name="example"></a>Beispiel

Wenn Sie z. B. in einer Einstandspreis-Umgebungen Material verbrauchen, um einen Artikel zu fertigen, gehen, einfach gesagt, der Einstandspreis des Artikels sowie die Bearbeitungs- und die Gemeinkosten in die WIP ein. Wenn der Artikel gefertigt wird, wird WIP um den Betrag Einstandspreises des Artikels verringert. Normalerweise sind diese Kosten nicht gleich Null. Damit diese Kosten sich zu Null saldieren können, müssen Sie die Stapelverarbeitung **Artikelkosteneinträge anpassen**, wobei zu beachten ist, dass nur Fertigungsaufträge mit dem Status **Beendet** für die Regulierung berücksichtigt werden.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Weitere Informationen

[Verwalten der Bestandsregulierung](finance-manage-inventory-costs.md)  
[Produktion](production-manage-manufacturing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
