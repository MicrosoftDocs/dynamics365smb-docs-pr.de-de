---
title: Erste Schritte mit einer Business Central-Vorschauversion für Copilot
description: 'Erläutert, wie Sie eine Business Central-Umgebung mit der neuen KI-Funktion zum Generieren von Textvorschlägen für Artikel-/Produktbeschreibungen erhalten.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/16/2023
ms.custom: bap-template
---

# Erste Schritte mit einer Business Central-Vorschauversion für Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Sie können die KI-gestützten Artikelmarketingtexte mit Copilot ausprobieren, unabhängig davon, ob Sie bereits Business Central-Kunde oder ein potenzieller Kunde sind, also jemand, der nur daran interessiert ist, Business Central kennenzulernen und die neue Funktion auszuprobieren. Um loszulegen, benötigen Sie Zugriff auf eine Vorschauversion von Business Central Online, die die neue Funktion unterstützt. Füllen Sie den auf Sie zutreffenden Abschnitt unten aus.

## Ihre Organisation verwendet Business Central bereits

Als bestehender Kunde oder Partner benötigen Sie einen Administrator mit Zugriff auf das Business Central Admin Center, um eine Umgebung einzurichten, die die Vorschauversion mit Copilot ausführt. Sobald die Umgebung eingerichtet ist und läuft, können Benutzende die neue Funktion ausprobieren.

Wenn Sie ein Umgebungsadministrator sind, führen Sie die folgenden Schritte aus:

1. Melden Sie sich beim Business Central Admin Center an.
2. Wählen Sie **Umgebungen** > **Neu** aus.
3. Geben Sie im Bereich **Umgebung erstellen** einen Namen für die neue Umgebung im Feld **Umgebungsname** ein.
4. Legen Sie den **Umgebungstyp** auf **Sandbox** oder **Produktion** est.
5. Legen Sie **Land** auf ein beliebiges Land/eine beliebige Region in der Liste fest, aber beachten Sie, dass der KI-generierte Marketingtext von Copilot in der Vorschau nur auf Englisch ist.
6. Wählen Sie im Feld **Version** eine Version 22 oder höher aus der Liste aus.

   <!--
   > [!IMPORTANT]
   > You must use **22.0.54157.54311 (Preview - Copilot edition)** to experience Copilot.
   -->
7. Wählen Sie **Erstellen** aus.  

Weitere Informationen zum Erstellen von Umgebungen finden Sie unter [Umgebung erstellen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

> [!IMPORTANT]
> Wenn Sie Vorschau-Sandboxen haben, die auf **22.0.54157.54311 (Vorschauversion – Copilot-Edition)** ausgeführt werden, beachten Sie, dass diese Umgebungen nur bis zum 1. Mai 2023 verfügbar sind. Nach diesem Datum müssen Sie eine neue Umgebung bereitstellen oder eine Ihrer anderen Umgebungen auf Version 22.0 oder höher aktualisieren, um die Vorschauversion von KI-gestützten Marketingtexten von Artikeln weiterhin auszuprobieren.

## Ihre Organisation verwendet Business Central nicht

Wenn Sie Business Central noch nicht verwenden, melden Sie sich für eine kostenlose Testversion an, um die neuen KI-Funktionen auszuprobieren. Die Anmeldung für die Testversion ist ganz einfach. Sie werden durch einige Schritte geführt, in denen Sie einige Informationen wie Ihre E-Mail-Adresse, Telefonnummer und Ihren Namen angeben müssen. Gehen Sie wie folgt vor, um eine Testversion zu erhalten:

1. Gehen Sie zu [dieser Testversionsseite](https://go.microsoft.com/fwlink/?linkid=2227167), um mit der Anmeldung zu beginnen.
2. Folgen Sie den Anweisungen auf dem Bildschirm.

   Sie werden gebeten, Informationen wie Ihre E-Mail-Adresse, Ihren Namen und Ihre Telefonnummer anzugeben. Die genaue Erfahrung kann je nach den von Ihnen bereitgestellten Informationen variieren. <!--But here are a couple important points to be aware of as you run through the sign-up process:--> Verwenden Sie als E-Mail-Adresse Ihre Geschäfts-, Schul- oder Uni-E-Mail-Adresse. Wir richten Ihre Testversion auf dem Konto Ihrer Organisation ein. Sie können keine E-Mail-Adressen verwenden, die von E-Mail-Diensten für Endverbraucher oder Telekommunikationsanbietern wie outlook.com, hotmail.com, gmail.com und anderen bereitgestellt werden.
   
   <!-- When you get to the option for **Country or region** be sure to set this **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  -->
3. Wenn Sie zum Schritt **Bestätigungsdetails** gelangen, können Sie mit der Testversion beginnen.

   - Um direkt zu Business Central zu gehen, wählen Sie **Überspringen und weiter zu Dynamics 365 Business Central** > **Erste Schritte**.
   - Sie haben auch die Möglichkeit, andere in Ihrer Organisation in die kostenlose Testversion einzuladen. Geben Sie einfach die E-Mail-Adressen aller Personen ein und wählen Sie dann **Einladungen senden** aus. Wählen Sie **Erste Schritte** aus, um zu Business Central zu wechseln.  

   Sie werden zu Ihrer Testversion unter [https://businesscentral.dynamics.com/](https://businesscentral.dynamics.com/) weitergeleitet. Bei der ersten Anmeldung kann es einige Minuten dauern, bis die Testversion fertig ist.

<!--
1. On the **Let's get you started** step, enter your work or school email address, then select **Next**.

   Use your work or school email address. We'll establish your trial on your organization's account. You can't use email addresses provided by consumer email services or telecommunication providers, such as outlook.com, hotmail.com, gmail.com, and others.
3. When asked what kind of email you have, select **I got it from my organization** > **Next**.
4. On the **Create your account** step, you provide information that will help use set up a trial version of Business Central that you can sign in to.

   1. Provide a telephone number that we can use to send you a verification code. Enter a country code and number that isn't VoIP or toll free.
   2. Choose how you want us to send the verification code:
      - Select **Text me** to get the verification code in a text message.
      - Select **Call me** to get the code in a voice message.
   3. Select **Send verification code**. 
   4. When you get the code, type it in the **Enter your verification code** box, then select **Verify**.

      Once you're verified, we'll send you an email with another verification code that you'll use in the next step to complete creating your account.
   5. Fill in your first and last name.
   6. Set **Country or region** to **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  

   7. Enter a valid phone umber in the **Business telephone number** box.
   8. In the **Create password** and **Confirm password** boxes, enter a password that you want to use to sign in to Business Central. The password must at least eight characters and include at least one number, an uppercase letter, and a lower case letter.
   9. In the **Verification code** box, enter the verification code we sent you in an email, then select **Next**.
   10. When you get a prompt that your account is successfully created, select **Sign in**.
-->

4. Sobald Sie angemeldet sind, sehen Sie die Business Central-Startseite, das sogenannte Rollencenter, das so ähnlich wie in der folgenden Abbildung aussieht:

   [![Zeigt das Business Central-Rollencenter und die Checkliste für Copilot an](media/copilot-checklist.png)](media/copilot-checklist.png#lightbox)

5. Um eine geführte Einführung in die Erstellung von KI-gestützten Marketingtexten für Artikel mit Copilot zu erhalten, wählen Sie unter **Ihre Checkliste** oben auf der Seite **Mit Copilot erstellen** > **Tour starten** aus. Folgen Sie dann einfach den Anweisungen auf dem Bildschirm.

   > [!TIP]
   > Wenn Sie **Ihre Checkliste** nicht sehen, wählen Sie zuerst die Schaltfläche **Demotouren anzeigen** aus.

## Nächste Schritte

Die von Copilot bereitgestellten KI-Funktionen müssen aktiviert werden, bevor Sie oder andere Copilot verwenden können. Um die KI-Funktionen zu aktivieren, muss ein Administrator den Nutzungsbedingungen der [Vorschauversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) und den [Microsoft-Datenschutzbestimmungen](https://go.microsoft.com/fwlink/?LinkId=521839) im Namen der Organisation zustimmen.

> [!NOTE]
> Wenn Sie eine Testversion verwenden, sind Sie der Administrator. Wenn Sie während der Anmeldung andere Personen in Ihrer Organisation zur Testversion eingeladen haben, können diese Copilot erst verwenden, wenn Sie den Nutzungsbedingungen zustimmen.

Es gibt zwei Möglichkeiten, als Administrator zuzustimmen:

- Der einfachste Weg ist die Verwendung von Copilot. Wenn Sie Copilot zum ersten Mal als Administrator verwenden, werden Sie aufgefordert, die Nutzungsbedingungen zu lesen und dann zuzustimmen oder abzulehnen. Informationen zur Verwendung von Copilot finden Sie unter [Marketingtext zu Artikeln hinzufügen](item-marketing-text.md).  

- Die andere Möglichkeit besteht darin, die Seite  **Status der Datenschutzhinweise**  in Business Central zu verwenden und der  **Azure OpenAI** Integration für alle Benutzer zuzustimmen. Um mehr zu erfahren, gehen Sie zu [Den Nutzungsbedingungen zustimmen](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

## Siehe auch

[Überblick über KI-gestützte Marketingtexte für Artikel mit Copilot](ai-overview.md)  
[KI-gestützten Marketingtext für Artikel mit Copilot als Administrator konfigurieren](enable-ai.md)  
[Mit Copilot Marketingtext für Artikel erstellen](item-marketing-text.md)  
[FAQ zu KI-gestützten Marketingtext für Artikel (Vorschauversion) mit Copilot](ai-faq.md)  