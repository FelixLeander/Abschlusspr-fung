### Projektbezeichnung
Programm zum Abfragen und Dokumentation von Sicherheitslücken, sowie Benachrichtigung betroffener. 
### Kurzbezeichnung der Aufgabenstellung
Ein Service welcher neue Informationen über Sicherheitslücken abruft, konvertiert und diese dann in Jira (Issue/Bug Tracking) als Ticket einpflegt.
Zusätzlich sollen Teams, welche für die Administration betroffener Systeme verantwortlich sind, benachrichtigt werden, wenn eine neue Sicherheitslücke als Ticket eingepflegt wurde.
Dadurch soll die generelle Cybersicherheit der Infrastruktur des Betriebes gestärkt werden, da öffentlich bekannte Sicherheitslücken schneller erkannt werden und relevante Informationen an einem zentralen Ort einsehbar sind.
### Ist-Analyse
Aktuell gibt es kein automatisierten Prozess, welcher sich um die Dokumentation von Sicherheitslücken sowie die Benachrichtigung der betroffenen Teams kümmert. Aktuell wird dieser Prozess manuell von einem Mitarbeiter ausgeführt. Dieser prüft händisch ob und in welchem Ausmaß die vorhandenen System betroffen sind und gibt diese Information an die entsprechenden Mitarbeiter weiter. Derzeit wird die Aufgabe von nur einem Mitarbeiter übernommen. Sollte dieser verhindert sein, kann es somit vorkommen, das bekannte Sicherheitslücken erst mit Verzögerung bearbeitet werden.
### Zielsetzung entwickeln Soll-Konzept (optional)
### Was soll am Ende des Projektes erreicht werden
Es soll ein Programm entwickelt werden, welches kontinuierlich oder in festgelegten Zyklen ausgeführt wird. Das Programm soll Informationen von Sicherheitslücken anhand von konfigurierbaren Kriterien abrufen und diese, wenn notwendig, an einem neu erstellten Jira-Ticket hinterlegen. Zusätzlich sollen die Teams, welche für die Verwaltung, der betroffenen Systeme verantwortlich sind, über die neuen Sicherheitslücken informiert werden. 

Das Programm soll Informationen über neu bekannte Sicherheitslücken abrufen und anhand konfigurierbarer Kriterien, Teams in unserem Unternehmen Benachrichtigen.
Für jede relevante Sicherheitslücke, soll automatisch ein Ticket in Jira erstellt werden, dass Informationen in einem strukturiertem Format zur dokumentiert.

Zusätzlich sollen die Teams, welche für die Verwaltung, der betroffenen Systeme verantwortlich sind, über die neue Sicherheitslücken informiert werden. 

### Welche Anforderungen müssen erfüllt sein
- Abfrage neuer Sicherheitslücken
- Konfigurierbare Kriterien
- Hinterlegen dieser in Jira
- Benachrichtigung der Teams, welche betroffene Systeme verwalten

### Welche Einschränkungen müssen berücksichtigt werden
- Verwendung der Programmiersprache C#
- Umsetzung mit .NET 8
- Einhaltung der betriebsinternen Coding-Guidelines
- Verwendung der vorhandenen Jira REST-API
- Nutzung der vorhandenen Infrastruktur
- Verwaltung des Quellcodes über die betriebsinterne Versionsverwaltung (GIT)
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
### Projektphasen mit Zeit-Planung in Stunden
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