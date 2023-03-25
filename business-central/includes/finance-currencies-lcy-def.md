---
author: edupont04
ms.topic: include
ms.date: 03/15/2022
ms.author: edupont
---
Da die Anzahl der Länder, in denen Unternehmen Geschäftsbeziehungen unterhalten, wächst, wird es unerlässlich, dass Finanzdaten in mehreren Währungen erfasst und angezeigt werden können. Die Hauswährung (LCY) wird auf der Seite **Finanzbuchhaltungs-Einrichtung** definiert, wie im Artikel [Grundlegendes zum Sachkonto und zum Kontenplan](../finance-general-ledger.md) beschrieben. Sobald die Mandantenwährung (MW) definiert wurde, wird sie als leere Währung dargestellt. Wenn das Feld **Währung** also leer ist, bedeutet dies, dass es sich um MW handelt.  

Als Nächstes müssen Sie Währungscodes für jede Währung einrichten, die Sie verwenden, wenn Sie in anderen Währungen als Ihrer lokalen Währung (LCY) kaufen oder verkaufen. Auch Bankkonten können mit Währungen erstellt werden. Es ist möglich, Sachtransaktionen in verschiedenen Währungen zu erfassen, diese werden jedoch immer in der Mandantenwährung (MW) gebucht.

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Ihre Finanzbuchhaltung wird in der Mandantenwährung (MW) eingerichtet. Sie können sie jedoch auch für die Verwendung einer anderen Währung einrichten, der Sie einen Währungswechselkurs zuweisen. Wird eine zweite Währung als [!INCLUDE[prod_short](prod_short.md)] Berichtswährung festgelegt, werden Beträge automatisch für jeden Sachposten und weitere Posten, wie zum Beispiel MwSt.-Posten, in der Mandantenwährung und der Berichtswährung erfasst. Weitere Informationen finden Sie unter [Zusätzliche Berichtswährung einrichten](../finance-how-setup-additional-currencies.md). Die Berichtswährung wird am häufigsten verwendet, um die Finanzberichterstellung für Eigentümer zu erleichtern, die in Ländern/Regionen ansässig sind, die andere Währungen als die Mandantenwährung (MW) verwenden.  

> [!IMPORTANT]
> Wenn Sie eine zusätzliche Berichtswährung für die Finanzberichterstattung verwenden wollen, vergewissern Sie sich, dass Sie die Einschränkungen verstehen. Weitere Informationen finden Sie unter [Zusätzliche Berichtswährung einrichten](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Wenn Sie mit einem Währungscode auf Sachkonten buchen, z. B. um einen Aufwand in einem FibuBuch.-Blatt mit einem Währungscode buchen, wird die Transaktion mit dem Wechselkurs des Buchungsdatums in MW umgerechnet. Der Sachposten enthält keine Informationen darüber, welche Währung verwendet wurde, sondern nur deren Wert in MW. Wenn Sie die ursprüngliche Währung verfolgen möchten, z. B. für eine Rechnung, müssen Sie die Verkaufs- und Einkaufsbeleg sowie Bankkonten verwenden, die Währungscodeinformationen für die Einträge speichern.
