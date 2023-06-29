---
title: 'Designdetails: Artikelverfolgung und -planung | Microsoft Docs'
description: 'Da sie im Reservierungssystem gespeichert werden, werden Artikelverfolgungsnummern vollständig mit Auftragsnachverfolgungsdatensätzen abgestimmt.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-and-planning"></a><a name="design-details-item-tracking-and-planning"></a>Designdetails: Artikelverfolgung und Planung
Da sie im Reservierungssystem gespeichert werden, werden Artikelverfolgungsnummern vollständig mit Auftragsnachverfolgungsdatensätzen abgestimmt. Dies bedeutet, dass Artikel mit Auftragsnachverfolgungsdatensätzen Artikelnachverfolgungsnummern zugeordnet werden können. Andererseits können Artikel, die Artikelverfolgungsnummern haben, zu Auftragsnachverfolgungsdatensätzen werden. Weitere Informationen finden Sie unter [Designdetails: Artikelverfolgungsdesign](design-details-item-tracking-design.md).

Weitere Informationen zu den integrierten Systemen finden Sie unter [Designdetails: Reservierungen, Auftragsnachverfolgung und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md).

Da die Auftragsnachverfolgung sich nur auf bestimmte Artikelausgleiche bezieht, gilt die Koordination mit Artikelverfolgungsnummern nur für Artikel, die zur Verwendung einer bestimmten Artikelverfolgung eingerichtet wurden. Dies wird durch die Felder **Seriennr.-spezifische Verf.** und **Chargennr.-spezifische Verf.** auf der Artikelkarte festgelegt, die Folgendes angeben:

- Der Artikel muss eine Seriennummer oder Chargennummer tragen, wenn er gebucht wird.
- Der Artikel muss dieselbe Seriennummer oder Chargennummer anwenden, wenn er als ausgehend gebucht wird.

In Anlehnung an Standardangebot-/-nachfrage-Ausgleichsprinzipien gleichen das Planungssystem und die zugehörige Auftragsnachverfolgungsfunktion nur Angebot und Nachfrage mit Artikelverfolgungsnummern ab, wenn der jeweilige Artikel eine spezifische Artikelverfolgung benutzt. In allen anderen Fällen ignorieren die Planungs- und Auftragsverfolgungsfunktionen Artikelverfolgungsnummern, wenn sie das Prinzip Vorrat zur Nachfragedeckung oder Nachfragedeckung für den Vorrat anwenden. Weiter Informationen finden Sie unter [Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md)

Wenn beispielsweise die Auftragsnachverfolgung für einen bestimmten Artikel aktiv ist, bedeutet dies, dass Datensätze für den Artikel bereits in der Tabelle **Reservierungsposten** vorhanden sind, die der Kern des Reservierungssystems ist, bevor die Artikelverfolgungsnummern definiert sind. Daher gelten die folgenden Kopplungseinschränkungen für die Artikelverfolgungsnummern, um eine Auftragsnachverfolgung durchzuführen:

- Bedarf mit einer Seriennummer oder einer Chargennummer kann nur Vorrat mit derselben Seriennummer oder Chargennummer abdecken.
- Bedarf ohne Seriennummer oder Chargennummer kann Vorrat mit oder ohne Seriennummer oder Chargennummer abdecken.

Abgesehen von ihren Auswirkungen auf die dynamische Auftragsnachverfolgung beeinflussen die Artikelnachverfolgungs-Kopplungseinschränkungen das Planungssystem nicht erheblich.

Auf der Zugangsseite wird eine Serien- oder Chargennummer normalerweise nicht direkt vor dem Buchen eines Auftrags eingegeben, wie z. B. eine Einkaufslieferung in das Lager. Wenn eine Serien- oder Chargennummer auf der Bedarfsseite, etwa auf einem Verkaufsauftrag, eingegeben wird, ist diese Serien- oder Chargennummer bereits im Lagerbestand. Entsprechend sind Artikelverfolgungsnummern in der Regel kein Problem in der Beschaffungsplanung.

Für Artikel, die eine bestimmte Artikelverfolgung verwenden, müssen alle Bedarfe mit Serien- oder Chargennummern durch entsprechenden Vorrat abgeglichen werden. In den meisten Fällen ist es nicht sinnvoll, eine bestimmte Serien- oder Chargennummer neu zu sortieren; daher wird die Planung von Einkaufs- oder Produktionsvorräten wahrscheinlich nicht beeinflusst. Wenn Artikel aus einem Lagerort in einen anderen übertragen werden, ist es jedoch wahrscheinlich, dass die Übertragung spezifisch für eine bestimmte Charge ist, sodass Planungsübertragungsvorräte durch die spezifische Kopplungseinschränkung beeinflusst werden.

Weitere Informationen finden Sie unter [Designdetails: Übertragung in der Planung](design-details-transfers-in-planning.md)

## <a name="balancing-demand-and-supply"></a><a name="balancing-demand-and-supply"></a>Ausgleich von Bedarf und Vorrat
Wenn ein Artikel eine bestimmte Artikelverfolgung erfordert, dann wird ein Auftragsnachverfolgungslink aus allen Verfolgungsbedarfen des Artikels zu allen entsprechenden Artikelverfolgungsvorräten erstellt, mit der einzigen Einschränkung, dass der Vorrat vor dem Bedarf kommen muss. Wenn unter diesen Umständen kein Artikelverfolgungsvorrat gefunden werden kann, der dem nachverfolgungsspezifischen Bedarf des Artikels entspricht, wird sofort neuer Nachverfolgungsvorrat ohne Berücksichtigung der Bestellmenge, Planungsparameter oder Neuplanung für vorhandenen Vorrat derselben Serien- oder Chargennummer erstellt.

Wenn Artikelverfolgungsnummern auf der Bedarfsseite oder auf der Vorratsseite zugewiesen werden, ohne dass eine bestimmte Artikelverfolgung erforderlich ist, dann wird ein Auftragsnachverfolgungslink von dem Bedarf zu diesem Vorrat erstellt, basierend auf dem passendsten Timing und der geeignetsten Menge, wie im normalen Ausgleichsverfahren. Die angegebene Artikelverfolgungsnummer geht in den Auftragsnachverfolgungsdatensatz in der gleichen Weise ein, wie eine angegebene Artikelnachverfolgungsmenge ein Ende des Auftragsnachverfolgungslinks definiert. Das bedeutet, dass die Artikelverfolgungsnummer, die eingetragen wird, beibehalten wird, während sie auch Teil des Bedarfsverursacherdatensatzes ist.

Wenn Artikelverfolgungsnummern auf der Vorratsseite zugeordnet werden, ohne dass eine bestimmte Artikelverfolgung erforderlich ist, wird dieser Vorrat als vom Planungssystem korrigiert betrachtet. Größenanpassungen oder Neuplanungen werden nicht für diesen Vorrat vorgeschlagen, doch wird dieser berücksichtigt, wenn das Planungssystem versucht, dem Bruttobedarf zu genügen.

Weitere Informationen finden Sie unter [Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)  

## <a name="see-also"></a><a name="see-also"></a>Siehe auch
[Designdetails: Artikelverfolgungsdesign](design-details-item-tracking-design.md)  
[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)  
[Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
