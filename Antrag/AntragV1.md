### Projektbezeichnung

Sicherheitslücken Abfrage, Dokumentation und Benachrichtungs-System
### Kurzbezeichnung der Aufgabenstellung
Ein Service welcher neue Informationen über Sicherheitslücken abruft, konvertiert und diese dann in Jira (Issue/Bug Tracking) als Ticket einpflegt.
Zusätzlich sollen Teams, welche für die Administration betroffener Systeme verantwortlich sind, benachrichtigt werden, wenn eine neue Sicherheitslücke bekannt wird.
Dadurch soll die generelle Cybersicherheit der Infrastruktur des Betriebes gestärkt werden, da öffentlich bekannte Sicherheitslücken schneller erkannt werden und Informationen leichter und geordneter zugänglich sind.
### Ist-Analyse
Aktuell gibt es kein Automatisiertes Prozess welcher sich um Benachrichtigung von Teams oder die Dokumentation von Sicherheitslücken kümmert.
Es gibt einen Mitarbeiter, welcher sich neben seinen Hauptaufgaben, darum kümmert, es ist aber kein Ersatz für den Fall seiner Verhinderung eingeplant.
Das bedeutet, dass falls er ausfällt, niemand anders diese Aufgabe übernehmen kann.
Dann wird erstmal händisch überprüft, ob und in welchem Ausmaß unsere Systeme davon betroffen sind. Meist wird dazu nichts Dokumentiert, da es dafür kein Standard Prozedere gibt, falls doch, dann sind diese uneinheitlich und an verschiedenen orten verteilt.
### Zielsetzung entwickeln Soll-Konzept (optional)
### Was soll am Ende des Projektes erreicht werden
Es soll ein Programm entwickelt werden, welches kontinuierlich oder in festgelegten Zyklen ausgeführt wird. Das Programm soll Informationen über neu bekannte Sicherheitslücken abrufen und anhand Konfigurierbarer Kriterien, Teams in unserem Unternehmen Benachrichtigen.
Für jede relevante Sicherheitslücke, soll automatisch ein Ticket in Jira erstellt werden, dass Informationen in einem strukturiertem Format zur dokumentiert.

Zusätzlich sollen die Teams, welche für die Verwaltung, der betroffenen Systeme verantwortlich sind, über die neue Sicherheitslücken informiert werden. 

### Welche Anforderungen müssen erfüllt sein
- Abfrage neuer Sicherheitslücken.
- Dokumentation dieser in Jira.
- Benachrichtigung der Teams, welche betroffene Systeme verwalten.

### Welche Einschränkungen müssen berücksichtigt werden
Für die Versionsverwaltung, des Programms muss GIT verwendet werden. Das Projekt wird in einem Repository auf einem GitLab-Server verstaut.
Das Programm muss:
- mit der Programmiersprache C# geschrieben werden.
- Team internen Programmierrichtlinien entsprechen.
- Logging beinhalten.
- die Jira REST-API verwenden.
- die gegebene Infrastruktur verwenden.

Es muss eine Zuordnung geben, die definiert welches Teams für welche Systeme verantwortlich sind.
### Projektstrukturplan entwickeln (optional)
### Was ist zur Erfüllung der Zielsetzung erforderlich
Zur Erfüllung der Zielsetzung, ist es erforderlich, dass das Programm in der Lage ist zwischen alten und bereits dokumentierten Sicherheitslücken zu unterscheiden, um keine Duplikate zu erstellen und Teams nicht unnötigerweise zu alarmieren.

Da das Projekt unter Aufsicht des Backend-Development-Teams umgesetzt wird, muss es von diesem geprüft & abgenommen werden.
### Hauptaufgaben auflisten
1. Planung
2. Entwicklung
3. Testphase
4. Dokumentation
### Teilaufgaben auflisten
1. Planung
	1. Erstellung eines Pflichtenheftes
	2. Erstellung des Projektes in Jira
	3. Entscheidung einer passenden Quelle der Sicherheitslücken-Informationen
	4. Design des Programmablaufs-Plan
2. Entwicklung
	1. Datenabfrage realisieren
	2. Abfrage und Filtern von bereits dokumentierten Sicherheitslücken
	4. Konvertierung in passendes Format für Jiras API
	5. Jira-Tickets per API erstellen
	6. Teams der betroffenen Systeme benachrichtigen
3. Testphase
	1. Testlauf
	2. Testlauf-Analyse
	3. Eventuelle Fehlerdokumentation
	4. Ausarbeitung möglicher Verbesserungen
4. Dokumentation
	1. Grundstruktur erstellen
	2. Details Ausarbeiten
	3. Grafiken und Assets hinzufügen
	4. Revision
### Grafische oder tabellarische Darstellung (optional)
### Projektphasen mit Zeitplanung in Stunden
1. Planung - 20h
	1. Erstellung eines Pflichtenheftes - 6h
	2. Erstellung des Projektes in Jira -4h
	3. Entscheidung einer passenden Quelle der Sicherheitslücken-Informationen -8h
	4. Design des Programmablaufs-Plan - 2h
2. Entwicklung - 36h
	1. Datenabfrage realisieren - 6h
	2. Abfrage und Filtern von bereits dokumentierten Sicherheitslücken - 6h
	4. Konvertierung in passendes Format für Jiras API - 10h
	5. Jira-Tickets per API erstellen - 12h
	6. Teams der betroffenen Systeme benachrichtigen - 2h
3. Testphase - 12h
	1. Testlauf - 1h
	2. Testlauf-Analyse - 2h
	3. Testlauf Dokumentation - 5h
	4. Ausarbeitung von Optimierungen - 4h
4. Dokumentation 12h
	1. Grundstruktur erstellen - 1h
	2. Details Ausarbeiten - 8h
	3. Grafiken und Assets hinzufügen - 1h
	4. Revision - 2h