# Projekt-Dokumentation

**Stevkov**

| Datum | Version | Zusammenfassung                                              |
| ----- | ------- | ------------------------------------------------------------ |
|  12.01.2023     | 0.0.1   | Ich habe die Projektdokumentation erstellt und mich für eine Technologie entschieden, mit der ich das Projekt programmieren werde. |
|       | 0.0.2   |                                                              |
|       | 0.0.3   |                                                              |
|       | 0.0.4   |                                                              |
|       | 0.0.5   |                                                              |
|       | 0.0.6   |                                                              |
|       | 1.0.0   |                                                              |

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
(Tier 3) Um die Schnittstelle zwischen den Datenbanken und dem Frontend zu machen, verwende ich Node, damit Daten übertragen, verarbeitet und gespeichert werden.
(Tier 4) Für die Arbeit mit Dataservern verwende ich MySQL um die Datenbanken aufzusetzen 

# 3) Datenbank

Datenbank:
Die Datenbanken soll mithilfe von MySQL geführt werden, wobei es drei verschiedene Datenbanken gibt. Userinformationen, Spielinformationen (Phrasen), Bankinformationen (evtl. unter User)

Interface:
Das Interface besteht aus einem Login bevor man auf das Spiel zugreifen kann. Das Interface des Spiels selber gibt dem Benutzer eine Auswahl aus verschiedenen Kategorien für Wörter, den Play Button, der Weiterleitung auf das Leaderboard und einen Button zur Weiterleitung auf die Bank Page. Alle Funktion und das sonst unsichtbare Adminpanel wir via Seitenleiste angezeigt. Das Spiel selbst ist im Rest des Screens sichtbar. Auf dem Leaderboard sieht man das aktuelle Leaderboard. Auf dem Adminpanel sind alle Adminfunktionen. Auf der Bank Page wird der aktuelle Betrag an Geld angezeigt. *Evtl. kann auf Shop zugegriffen werden, um mit dem erspielten Geld, Dinge zu kaufen.

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
| 13  |        Muss         |   Qualität   |    Als Spieler möchte ich, dass die Highscore-Liste nach Rang, bestimmt durch die Höhe des Geldbetrags, aufsteigend sortiert wird, um die besten Ergebnisse schnell zu finden.                                |
| A | Kann | Funktional | Als Spieler möchte ich die History meines Bankkonto sehen, um zu sehen wie viel Geld ich an einem vorherigen Zeitpunkt hatte |
| B | Kann | Funktional | Als Benutzer der Webseite möchte ich einen Dark und Lightmode haben, um einen dünkleren Modus zu haben der besser ist am Abend. |
| C | Kann | Funktional | Als Spieler möchte ich in einem Shop verschiedene Items kaufen können, um mein erspieltes GEld |
| D | Kann | QUalität | Als Admin möchte ich bei meinem Namen eine andere Farbe haben, um mich beim Leaderboard von Spieler unterscheiden zu können. |

# 4.2) Testfälle

| TC-№ | Vorbereitung | Eingabe | Erwartete Ausgabe |
| ---- | ------------ | ------- | ----------------- |
| 1.1 | Website ist auf 1. Seite geöffnet | Administrator gibt Benutzername und Passwort ein | Administrator erhält Zugang zu den Verwaltungsfunktionen|
| 2.1 | Website ist auf Adminpanel geöffnet | Administrator gibt Phrase und Lösungswort ein | Phrase wird erfolgreich angelegt|
| 2.2 | Website ist auf Adminpanel geöffnet  | Administrator gibt neue Phrase und Lösungswort ein | Phrase wird erfolgreich geändert|
| 2.3 | Website ist auf Adminpanel geöffnet | Administrator bestätigt Löschvorgang | Phrase wird erfolgreich gelöscht|
| 3.1 |  Website ist auf Adminpanel geöffnet | Administrator gibt Kategoriebezeichnung ein | Kategorie wird erfolgreich angelegt|
| 3.2 |  Website ist auf Adminpanel geöffnet | Administrator wählt Wort/Frage und Kategorie aus | Wort/Frage wird erfolgreich der Kategorie zugeordnet|
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
| B.1 | Website ist auf 2. Seite geöffnet; Lightmode ist aktiviert | Benutzer klickt auf Sonne | Webseite wechselt zum Darkmode|
| B.2 | Website ist auf 2. Seite geöffnet; Darkmode ist aktiviert | Benutzer klickt auf Mond | Webseite wechselt zum Lightmode|
| C.1 | Website ist auf 2. Seite geöffnet | Spieler klickt auf "Shop" | Shop wird geöffnet|
| C.2 | Website ist auf Shop Seite geöffnet | Spieler wählt Item aus und drückt auf Kaufen | Item wird erfolgreich gekauft und vom Kontostand abgezogen|
| D.1 | Man ist als Admin angemeldet; Admin spielt ein Spiel und speichert Highscore; Website ist auf Leaderboard geöffnet   | Admin wählt Farbe aus der Liste | Farbe des Namens im Leaderboard wird geändert.|

# 5) Prototyp

![image](https://user-images.githubusercontent.com/47601770/212045017-5b7a8362-50da-4ae9-a2ab-2874db684ce3.png)

![image](https://user-images.githubusercontent.com/47601770/212046295-5e4814d8-e2cc-455b-aaf7-04eee33c7b5d.png)


# 6 Implementation

✍️ Halten Sie fest, wann Sie welche User Story bearbeitet haben

| User Story | Datum | Beschreibung |
| ---------- | ----- | ------------ |
| ...        |       |              |

# 7 Projektdokumentation

| US-№ | Erledigt? | Entsprechende Code-Dateien oder Erklärung |
| ---- | --------- | ----------------------------------------- |
| 1    | ja / nein |                                           |
| ...  |           |                                           |

# 8 Testprotokoll

✍️ Fügen Sie hier den Link zu dem Video ein, welches den Testdurchlauf dokumentiert.

| TC-№ | Datum | Resultat | Tester |
| ---- | ----- | -------- | ------ |
| 1.1  |       |          |        |
| ...  |       |          |        |

✍️ Vergessen Sie nicht, ein Fazit hinzuzufügen, welches das Test-Ergebnis einordnet.

# 9 `README.md`

✍️ Beschreiben Sie ausführlich in einer README.md, wie Ihre Applikation gestartet und ausgeführt wird. Legen Sie eine geeignete Möglichkeit (Skript, Export, …) bei, Ihre Datenbank wiederherzustellen.

# 10 Allgemeines

- [ ] Ich habe die Rechtschreibung überprüft
- [ ] Ich habe überprüft, dass die Nummerierung von Testfällen und User Stories übereinstimmen
- [ ] Ich habe alle mit ✍️ markierten Teile ersetzt
