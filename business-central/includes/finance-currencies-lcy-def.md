---
author: brentholtorf
ms.topic: include
ms.date: 03/04/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
Wenn Ihr Unternehmen in mehr als einem Land oder einer Region tätig ist, ist es wahrscheinlich wichtig, dass Sie in mehr als einer Währung Geschäfte tätigen können. Sie legen Ihre lokale Währung (LW) auf der Seite **Finanzbuchhaltung Einrichtung** fest. Anschließend wird Ihre lokale Währung in Dokumenten und Transaktionen als leere Währung dargestellt. Wenn das Feld **Währung** leer ist, ist die Währung LW.

Das folgende Video erklärt, wie Sie Ihre lokale Währung einrichten.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1iM1n]

Als Nächstes müssen Sie Währungscodes für jede Währung einrichten, die Sie verwenden, wenn Sie in anderen Währungen als Ihrer lokalen Währung (LCY) kaufen oder verkaufen. Auch Bankkonten können mit Währungen erstellt werden. Es ist möglich, Sachtransaktionen in verschiedenen Währungen zu erfassen, diese werden jedoch immer in der Mandantenwährung (MW) gebucht.

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Ihre Finanzbuchhaltung wird in der Mandantenwährung (MW) eingerichtet. Sie können sie jedoch auch für die Verwendung einer anderen Währung einrichten, der Sie einen Währungswechselkurs zuweisen. Wird eine zweite Währung als Berichtswährung festgelegt, erfasst [!INCLUDE[prod_short](prod_short.md)] Beträge für jeden Sachposten und weitere Posten, wie zum Beispiel MwSt.-Posten, automatisch sowohl in der LW als auch in der Berichtswährung. Weitere Informationen finden Sie unter [Zusätzliche Berichtswährung einrichten](../finance-how-setup-additional-currencies.md). Die Berichtswährung wird am häufigsten verwendet, um die Finanzberichterstellung für Eigentümer zu erleichtern, die in Ländern/Regionen ansässig sind, die andere Währungen als die Mandantenwährung (MW) verwenden.  

> [!IMPORTANT]
> Wenn Sie eine zusätzliche Berichtswährung für die Finanzberichterstattung verwenden wollen, vergewissern Sie sich, dass Sie die Einschränkungen verstehen. Weitere Informationen finden Sie unter [Zusätzliche Berichtswährung einrichten](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Wenn Sie in einer Fremdwährung in das Hauptbuch buchen, rechnet [!INCLUDE [prod_short](prod_short.md)] die Transaktion anhand des Währungswechselkurses für das Buchungsdatum in LW um. Der Sachposten enthält keine Informationen darüber, welche Währung verwendet wurde, sondern nur deren Wert in LW. Um die ursprüngliche Währung nachzuverfolgen, verwenden Sie die Verkaufs- und Einkaufsbelege sowie Bankkonten, die Währungsinformationen für die Posten speichern.
