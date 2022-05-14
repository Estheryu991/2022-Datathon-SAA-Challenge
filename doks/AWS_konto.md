# AWS-Konto
Um an der Herausforderung zu arbeiten, muss jedes Team über **ein** AWS-Konto verfügen.

## Erstellen Sie ein AWS-Konto
Sie können sich für ein neues AWS-Konto anmelden
[hier](https://portal.aws.amazon.com/billing/signup).

Während der Kontoerstellung werden Sie aufgefordert, eine Supportstufe auszuwählen. Bitte
Wählen Sie den **Grundlegenden Support**.

## IAM-Benutzer erstellen
Mit der E-Mail-Adresse erhalten Sie Zugriff auf den Root-Benutzer des Kontos. Das
Benutzer hat die höchsten Privilegien im Konto und sollte nur für verwendet werden
Managementaufgaben. Für alle täglichen Aufgaben und besonders für diese Herausforderung
IAM-Benutzer sollten verwendet werden (falls nicht anders angegeben).

Um IAM-Benutzer zu erstellen, gehen Sie zu [Identity and Access Management
(IAM)](https://us-east-1.console.aws.amazon.com/iamv2)-Dienst. Auf die Benutzer
Seite können Sie neue IAM-Benutzer erstellen. Sie müssen für jeden Ihrer einen Benutzer erstellen
Teamkollegen und auch ein Benutzer für Sie.

1. Wählen Sie links den Menüpunkt **Benutzer**
1. Klicken Sie auf **Benutzer hinzufügen**
1. Legen Sie Benutzerdetails fest
   * Geben Sie den **Benutzernamen** an

     **HINWEIS:** Sie können alle Benutzer auf einmal erstellen, indem Sie auf **Weiteren Benutzer hinzufügen** klicken.
   * Wählen Sie für **AWS-Anmeldetyp auswählen** beide aus
     * ✅ Zugriffsschlüssel - Programmgesteuerter Zugriff

       Wird für den Zugriff auf die AWS-APIs verwendet
     * ✅ Passwort – Zugriff auf die AWS Management Console

       Wird verwendet, um sich bei der AWS-Web-Benutzeroberfläche anzumelden, auch Management Console oder AWS Console genannt
     * **Konsolenpasswort:** Automatisch generiertes Passwort
     * **Zurücksetzen des Passworts erforderlich:** ✅ Der Benutzer muss als Nächstes ein neues Passwort erstellen
       Anmelden
1. Berechtigungen festlegen
   * Wählen Sie **Vorhandene Richtlinien direkt anhängen**
   * ✅ **Administratorzugriff**. Dies gibt Ihnen allen und Ihren Teamkollegen Zugriff
     zu allen Diensten.

Für diese Herausforderung müssen Sie keine Tags erstellen. Nach doppelter Überprüfung
dass alle Informationen korrekt sind, können Sie dann mit der Erstellung der Benutzer fortfahren.

Nach erfolgreicher Erstellung werden Sie auf die letzte Seite der weitergeleitet
Magier. Auf dieser Seite können Sie die CSV-Datei mit den Anmeldeinformationen herunterladen.
Verteilen Sie diese Datei an Ihre Teamkollegen.

## Credits einlösen
Für die Herausforderung sponserte AWS Credits für jedes der Teams. Sie erhalten die
Code vom SAA-Team vor Ort.

**HINWEIS:** Diese Aufgabe muss als Root-Benutzer des AWS-Kontos ausgeführt werden.

Nachdem Sie das Konto erstellt haben, können Sie die im [Abrechnungsservice ->
Kredite] (https://us-east-1.console.aws.amazon.com/billing/home?region=eu-west-1#/credits).

## AWS Single Sign-On (SSO) aktivieren
Um Kendra Experiences verwenden zu können, müssen Sie AWS SSO aktivieren und SSO erstellen
Benutzer. Wenn Sie die Funktion Kendra Experiences verwenden möchten, müssen Sie sie ausführen
die folgenden Schritte.

### AWS SSO aktivieren
* Melden Sie sich als Ihr Root-Benutzer an
* SSO in der EU (Irland) aktivieren | Region eu-west-1
  https://eu-west-1.console.aws.amazon.com/singlesignon/identity/home

### Gruppe und Benutzer erstellen
Sie können die SSO-Gruppe und Benutzer mit jedem der zuvor erstellten Benutzer erstellen.
1. Wählen Sie im linken Menü **Gruppen** aus
   * Erstellen Sie die *Gruppe* mit einem Namen Ihrer Wahl
1. Nachdem die Gruppe erstellt wurde, können Sie die Benutzer erstellen
1. Wählen Sie im linken Menü **Benutzer** aus
   * Gib ihm einen Namen
   * Wählen Sie *E-Mail mit Anweisungen zur Kennworteinrichtung an den Benutzer senden.*
   * Geben Sie eine gültige E-Mail-Adresse ein
   * Geben Sie den Vor- und Nachnamen an
   * Fügen Sie den Benutzer der zuvor erstellten Gruppe hinzu
1. Gehen Sie zu Ihrem E-Mail-Client
1. *Akzeptieren Sie die Einladung** und geben Sie ein Passwort für den Benutzer an

Danach kann der Benutzer während der Konfiguration der Kendra Experiences ausgewählt werden
Merkmal.
