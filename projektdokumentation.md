# Projekt-Dokumentation

**Stevkov**

| Datum | Version | Zusammenfassung                                              |
| ----- | ------- | ------------------------------------------------------------ |
|  12.01.2023     | 0.0.1   | Ich habe die Projektdokumentation erstellt und mich für eine Technologie entschieden, mit der ich das Projekt programmieren werde. |
|   26.01.2023    | 1.0.1   |    Ich habe ein React Programm erstellt und die Fullstack umgebung eingerichtet                                                          |
|   02.02.2023    | 1.0.2   |    Ich habe eine Verbindung zu einer Datenbank via SQL im Express Backend erstellt.                                                           |
|   14.02.2023    | 1.0.3   |    Ich habe provisorische Daten in meine Datenbank eingefügt und habe versucht einen Fehler mit der Verbindung zur Datenbank zu beheben.                                                         |
|   19.02.2023    | 1.1.1   |    Ich habe die Hauptseite des Spiels begonnen zu erstellen und eine Navigation erstellt für die Seiten                                                        |
|   23.02.2023    | 2.0.1   |    Ich habe neu Begonnen und habe ein neues Projekt mit einer Firebase Datenbank erstellt                                                     |
|   28.02.2023    | 2.0.1   |    Ich habe das Login fertiggestellt und das Adminpanel begonnen, auch konnte ich den Darkmode implementieren                                                     |
|   01.03.2023    | 2.0.1   |    Ich habe das UI erstellt und das Adminpanel mit Buttons erstellt                                                          |
|    02.03.2023   | 2.0.2   |    Ich habe die letzten Dinge probiert zu retten wie die löschfunktion, jedoch konnte ich nicht viel umsetzen                                                           |

# 0) Ihr Projekt

Mein Projekt ist eine Webapplikation basiert auf die Fernsehshow "Glücksrad", welche in den 90er Jahren weltweit bekannt war, und das Hauptziel ist es Wörter zu erraten und so möglichst viel Geld zu ergattern! 

# 1) Analyse

* Tier 1 (Presentation): Website, Spieloberfläche, Loginoberfläche, Highscore-Liste
* Tier 2 (Webserver): Input von Buchstaben, Input Logindaten, Spielfunktionen, Bankfunktionen
* Tier 3 (Application Server): Logindaten an Datenbank senden, Auswertung Spielereingaben, Highscore Liste updaten, Bank Werte mit Datenbank verbinden
* Tier 4 (Dataserver): Benutzerdaten, Admindaten, Bankdaten, Phrasen und Wörter 

# 2) Technologie

(Tier 1) Für das Frontend verwende ich React, um Dinge darzustellen und das UI zu kreieren. 
(Tier 2) Dies ist auch noch hauptsächlich Teil vom Frontend weshalb ich auch hier React verwenden kann.
(Tier 3) Um die Schnittstelle zwischen den Datenbanken und dem Frontend zu machen, verwende ich Firebase, damit Daten übertragen, verarbeitet und gespeichert werden.
(Tier 4) Für die Arbeit mit Dataservern verwende ich Firebase um die Datenbanken aufzusetzen 

# 3) Datenbank

Datenbank:
Die Datenbanken soll mithilfe von Firebase geführt werden, wobei es drei verschiedene Datenbanken gibt. Userinformationen, Spielinformationen (Phrasen), Bankinformationen (evtl. unter User)

Interface:
Das Interface besteht aus einem Login bevor man auf das Spiel zugreifen kann. Das Interface des Spiels selber gibt dem Benutzer eine Auswahl aus verschiedenen Kategorien für Wörter, den Play Button, der Weiterleitung auf das Leaderboard und einen Button zur Weiterleitung auf die Bank Page. Alle Funktion und das Adminpanel werden via Seitenleiste angezeigt. Das Spiel selbst ist im Rest des Screens sichtbar. Auf dem Leaderboard sieht man das aktuelle Leaderboard. Auf dem Adminpanel sind alle Adminfunktionen. Auf der Bank Page wird der aktuelle Betrag an Geld angezeigt. *Evtl. kann auf Shop zugegriffen werden, um mit dem erspielten Geld, Dinge zu kaufen.

# 4.1) User Stories

| US-№ | Verbindlichkeit | Typ  | Beschreibung                       |
| ---- | --------------- | ---- | ---------------------------------- |
| 1    |        Muss         |   Funktional   | Als Administrator möchte ich mich durch Eingabe von Benutzername und Passwort authentifizieren können, um auf die Verwaltungsfunktionen zugreifen zu können. |
| 2  |         Muss        |   Funktional   |  Als Administrator möchte ich Phrasen und Rätselwörter anlegen, ändern und löschen können, um die Inhalte des Spiels zu verwalten.                                  |
| 3 |        Muss         |    Funktional  | Als Administrator möchte ich Kategorien anlegen und die Wörter und Fragen einer Kategorie zuordnen können, um das Spiel zu organisieren.                                   |
| 4  |     Muss            |   Funktional   | Als Administrator möchte ich einzelne Einträge der Highscore-Liste löschen können, um unerwünschte Einträge zu entfernen.                                   |
| 5  |        Muss         |    Funktional  |  Als Administrator möchte ich Spieler Accounts löschen können, um inaktive oder spam Accounts zu löschen                                  |
| 6  |        Muss         |    Funktional  |   Als Spieler möchte ich mittels eines Webbrowsers auf das Spiel zugreifen können, um es spielen zu können.                                 |
| 7 |       Muss          |  Funktional    |  Als Spieler möchte ich meinen Benutzernamen und Passwort eingeben können, um die Spieloberfläche zu öffnen.                                  |
| 8  |        Muss         |    Funktional  |   Als Spieler möchte ich meine Ergebnisse speichern können, damit ich in der Highscore-Liste erfasst werde.                                 |
| 9  |         Muss        |   Qualität   |   Als Spieler möchte ich zu jeder Zeit meinen Kontostand einsehen können, um den Fortschritt des Spiels zu verfolgen.                                 |
| 10  |       Muss          |   Qualität   |  Als Spieler möchte ich zu jeder Zeit meine Lebenspunkte einsehen können, um den Fortschritt des Spiels zu verfolgen.                                  |
| 11  |        Muss         |   Qualität   |  Als Spieler möchte ich erfahren, ob meine Antwort richtig oder falsch war, um meine Leistung einschätzen zu können.                                  |
| 12  |        Muss         |   Qualität   |     Als Spieler möchte ich in der Highscore-Liste Rang, Namen des Spielers, Zeitpunkt des Spiels, Geldbetrag und Anzahl der Spielrunden einsehen können, um meine Leistung mit anderen zu vergleichen.                               |
| A | Kann | Funktional | Als Spieler möchte ich die History meines Bankkonto sehen, um zu sehen wie viel Geld ich an einem vorherigen Zeitpunkt hatte |
| B | Kann | Funktional | Als Benutzer der Webseite möchte ich einen Dark und Lightmode haben, um einen dünkleren Modus zu haben der besser ist am Abend. |
| C | Kann | Funktional | Als Spieler möchte ich in einem Shop verschiedene Items kaufen können, um mein erspieltes Geld |
| D | Kann | Qualität | Als Admin möchte ich bei meinem Namen eine andere Farbe haben, um mich beim Leaderboard von Spieler unterscheiden zu können. |

# 4.2) Testfälle

| TC-№ | Vorbereitung | Eingabe | Erwartete Ausgabe |
| ---- | ------------ | ------- | ----------------- |
| 1.1 | Website ist auf 1. Seite geöffnet | Administrator gibt Benutzername und Passwort ein | Administrator erhält Zugang zu den Verwaltungsfunktionen|
| 2.1 | Website ist auf Adminpanel geöffnet | Administrator gibt Phrase oder Lösungswort ein | Phrase wird erfolgreich angelegt|
| 2.2 | Website ist auf Adminpanel geöffnet | Administrator bestätigt Löschvorgang | Phrase wird erfolgreich gelöscht|
| 3.1 |  Website ist auf Adminpanel geöffnet | Administrator gibt Kategoriebezeichnung ein | Kategorie wird erfolgreich angelegt|
| 4.1 |  Man ist als Admin angemeldet; Website ist auf Leaderboard geöffnet | Administrator wählt Eintrag und bestätigt Löschvorgang | Eintrag wird erfolgreich gelöscht|
| 5.1 |  Website ist auf Adminpanel geöffnet | Administrator wählt Account und bestätigt Löschvorgang | Account wird erfolgreich gelöscht|
| 6.1 | Webbrowser wird geöffnet | Benutzer gibt URL des Spiels ein | Loginpage wird im Webbrowser geöffnet|
| 7.1 | Website ist auf 1. Seite geöffnet | Spieler gibt Benutzername und Passwort ein | Spieler erhält Zugang zur Spieloberfläche|
| 8.1 | Website ist auf 2. Seite geöffnet; Kategorie wird ausgewählt | Spieler gibt Antworten ein | Ergebnis wird erfolgreich gespeichert|
| 9.1 | Website ist auf Bank Seite geöffnet | Keine Eingabe | Kontostand wird angezeigt|
| 10.1 | Website ist auf 2. Seite geöffnet | Keine Eingabe | Lebenspunkte werden angezeigt|
| 11.1 | Spieler erhält Rückmeldung nach Antwort | Spieler gibt Antwort ein | Rückmeldung ob Antwort richtig oder falsch wird angezeigt|
| 12.1 | Website ist auf Highscore Seite geöffnet | Keine Eingabe | Highscore-Liste wird angezeigt|
| Testfall A.1 | Website ist auf Bank Seite geöffnet | Spieler klickt auf "History" | Spieler sieht die Historie des Bankkontos|
| B.1 | Website ist auf 2. Seite geöffnet; Lightmode ist aktiviert | Benutzer klickt auf Darkmode Symbol | Webseite wechselt zum Darkmode|
| B.2 | Website ist auf 2. Seite geöffnet; Darkmode ist aktiviert | Benutzer klickt auf Darkmode Symbol | Webseite wechselt zum Lightmode|
| C.1 | Website ist auf 2. Seite geöffnet | Spieler klickt auf "Shop" | Shop wird geöffnet|
| C.2 | Website ist auf Shop Seite geöffnet | Spieler wählt Item aus und drückt auf Kaufen | Item wird erfolgreich gekauft und vom Kontostand abgezogen|
| D.1 | Man ist als Admin angemeldet; Admin spielt ein Spiel und speichert Highscore; Website ist auf Leaderboard geöffnet   | Admin wählt Farbe aus der Liste | Farbe des Namens im Leaderboard wird geändert.|

# 5) Prototyp

![image](https://user-images.githubusercontent.com/47601770/212045017-5b7a8362-50da-4ae9-a2ab-2874db684ce3.png)

![image](https://user-images.githubusercontent.com/47601770/212046295-5e4814d8-e2cc-455b-aaf7-04eee33c7b5d.png)


# 6 Implementation

| User Story | Datum | Beschreibung |
| ---------- | ----- | ------------ |
|  1  |    1.3.2023   |    Ich habe hier implementiert, dass man sich mit dem Admin user anmelden kann         |
|  2  |    1.3.2023   |     Ich habe hier die Option eingefügt Wörter den Kategorien anzufügen        |
|  3  |    1.3.2023   |     Ich habe auf der Seite wo man Wörter einfügt, ermöglicht es neue Kategorien zu erstellen       |
|  5  |    2.3.2023   |     Ich habe eine Seite erstellt um Benutzer zu löschen mit einer E-Mail eingabe      |
|  6  |    16.2.2023   |      -       |
|  7  |    23.2.2023   |  Ich habe die Firebase Benutzer mit dem Programm verlinkt und ein Log-in Form erstellt           |
|  10  |    1.3.2023   |    Ich habe eine simple Healthbar implementiert         |
|  B  |    28.3.2023   |  Ich habe den Darkmode mithilfe von contexts implementiert.            |


# 7 Projektdokumentation

| US-№ | Erledigt? | Entsprechende Code-Dateien oder Erklärung |
| ---- | --------- | ----------------------------------------- |
| 1    | ja   |         /pages/login                                  |
| 2  |         ja  |                      /pages/newcategory                     |
| 3  |          ja |                                           |
| 4  |          nein |         Nicht geschafft.                                  |
| 5  |          nein |         Implementiert aber nicht funktionsfähig                                  |
| 6  |          ja |         Projekt wird auf Google geöffnet                                  |
| 7  |          ja |          /pages/login                                 |
| 8  |         nein  |         Nicht geschafft.                                  |
| 9  |        nein   | Nicht geschafft.                                          |
| 10  |        ja   |             components/healthbar                              |
| 11  |          nein |Nicht geschafft.                                           |
| 12  |          nein |                Nicht geschafft.                           |
| A  |          nein |                                 Nicht geschafft.          |
| B  |      ja     |                                          /context/darkmodecontext und reducer|
| C  |     nein      |                                         Nicht geschafft.  |
| D  |     nein      |  Nicht geschafft.                                         |

# 8 Testprotokoll

✍️ Fügen Sie hier den Link zu dem Video ein, welches den Testdurchlauf dokumentiert.

| TC-№ | Datum | Resultat | Tester |
| ---- | ----- | -------- | ------ |
| 1.1  |       |          |        |
|   |       |          |        |

Insgesamt muss ich sagen, dass ich mit dem Projekt sehr unzufrieden bin. Wegen vielen Schwierigkeiten und Meinungsänderungen habe ich ein sehr schwaches Endresultat und ich konnte nur die hälfte der Testfälle realisieren. Ich hatte mühe, da ich spät im Projekt einen grossen Fehler mit der SQL Datenbank hatte und somit, praktisch von Neu beginnen musste vor 1-2 Wochen. Das Spiel ist nicht funktionsfähig und es wurden nur einige Admin Befehle und ein Login umgesetzt, mit einem teilweise funktionsfähigen UI.

# 9 `README.md`

[README.md](https://github.com/machko1/StevkovEdward_LB151/files/10872271/README.md)


# 10 Allgemeines

- [✅] Ich habe die Rechtschreibung überprüft
- [✅] Ich habe überprüft, dass die Nummerierung von Testfällen und User Stories übereinstimmen
- [✅ ] Ich habe alle mit ✍️ markierten Teile ersetzt
