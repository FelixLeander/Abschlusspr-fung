### 1. Projektbezeichnung
Programm zum Abfragen und Dokumentation von Sicherheitslücken, sowie Benachrichtigung betroffener. 
### 1.1 Kurzbezeichnung der Aufgabenstellung
Ein Service welcher neue Informationen über Sicherheitslücken abruft, konvertiert und diese dann in Jira (Issue/Bug Tracking) als Ticket einpflegt.
Zusätzlich sollen Teams, welche für die Administration betroffener Systeme verantwortlich sind, benachrichtigt werden, wenn eine neue Sicherheitslücke als Ticket eingepflegt wurde.
Dadurch soll die generelle Cybersicherheit der Infrastruktur des Betriebes gestärkt werden, da öffentlich bekannte Sicherheitslücken schneller erkannt werden und relevante Informationen an einem zentralen Ort einsehbar sind.
### 1.2 Ist-Analyse
Aktuell gibt es kein automatisierten Prozess, welcher sich um die Dokumentation von Sicherheitslücken sowie die Benachrichtigung der betroffenen Teams kümmert. Aktuell wird dieser Prozess manuell von einem Mitarbeiter ausgeführt. Dieser prüft händisch ob und in welchem Ausmaß die vorhandenen System betroffen sind und gibt diese Information an die entsprechenden Mitarbeiter weiter. Derzeit wird die Aufgabe von nur einem Mitarbeiter übernommen. Sollte dieser verhindert sein, kann es somit vorkommen, das bekannte Sicherheitslücken erst mit Verzögerung bearbeitet werden.
### 2. Zielsetzung entwickeln Soll-Konzept (optional)
### 2.1 Was soll am Ende des Projektes erreicht werden
Es soll ein Programm entwickelt werden, welches kontinuierlich oder in festgelegten Zyklen ausgeführt wird. Das Programm soll Informationen von Sicherheitslücken abrufen und anhand von konfigurierbaren Kriterien Filtern. Diese Kriterien sollen, zwecks Anpassbarkeit durch IT-Fachpersonal, in einem strukturiertem & menschlich lesbarem Format als Datei hinterlegt werden (wie z.B. XML, JSON oder CSV). 
Für jede relevante Sicherheitslücke, soll automatisch ein Ticket in Jira erstellt werden, dass Informationen in einem strukturiertem Format zur Verfügung stellt.
Zusätzlich sollen die Teams, welche für die Verwaltung, der betroffenen Systeme verantwortlich sind, über die neuen Sicherheitslücken informiert werden. 

### 2.2 Welche Anforderungen müssen erfüllt sein
- Abfrage neuer Sicherheitslücken
- Hinterlegen dieser in Jira
- Konfigurierbare Kriterien
- Benachrichtigung der Teams, welche betroffene Systeme verwalten

### 2.3 Welche Einschränkungen müssen berücksichtigt werden
- Verwendung der Programmiersprache C#
- Umsetzung mit .NET 8
- Einhaltung der betriebsinternen Coding-Guidelines
- Verwendung der vorhandenen Jira REST-API
- Verwendung des "Atlassian Document Format" (ADF) 
- Nutzung der vorhandenen Infrastruktur
- Verwaltung des Quellcodes über die betriebsinterne Versionsverwaltung (GIT)
### 3 Projektstrukturplan entwickeln (optional)
### 3.1 Was ist zur Erfüllung der Zielsetzung erforderlich
Zur Erfüllung der Zielsetzung, ist es erforderlich, dass das Programm, Sicherheitslücken abfragen, nach bereits erstellten Tickets & anpassbaren konfigurierbaren Kriterien, filtern kann.

Da das Projekt unter Aufsicht des Backend-Development-Teams umgesetzt wird, muss es von diesem geprüft & abgenommen werden.
### 3.2 Hauptaufgaben auflisten
1. Planung
2. Entwicklung
3. Testphase
4. Dokumentation
### 3.3 Teilaufgaben auflisten
1. Planung
	1. Erstellung eines Pflichtenheftes
	2. Erstellung des Projektes in Jira
	3. Entscheidung einer passenden Quelle der Sicherheitslücken-Informationen
	4. Design des Programmablaufs-Plan
2. Entwicklung
	1. Abfrage der Sicherheitslücken
	2. Filtern der Sicherheitslücken anhand konfigurierten Kriterien
	3. Abgleich der bereits in Jira bekannten Sicherheitslücken
	4. Konvertierung der Daten in passendes Format für Jira's API
	5. Jira-Tickets per API erstellen
	6. Teams der betroffenen Systeme benachrichtigen
3. Testphase
	1. Testlauf
	2. Testlauf-Analyse
	3. Testlauf Dokumentation
	4. Ausarbeitung von Optimierungen
4. Dokumentation
	1. Grundstruktur erstellen
	2. Details Ausarbeiten
	3. Grafiken und Assets hinzufügen
	4. Revision
### 3.4 Grafische oder tabellarische Darstellung (optional)
### 4. Projektphasen mit Zeit-Planung in Stunden
1. Planung - 20h
	1. Erstellung eines Pflichtenheftes - 6h
	2. Erstellung des Projektes in Jira -4h
	3. Entscheidung einer passenden Quelle der Sicherheitslücken-Informationen -8h
	4. Design des Programmablaufs-Plan - 2h
2. Entwicklung - 36h
	1. Abfrage der Sicherheitslücken - 4h
	2. Filtern der Sicherheitslücken anhand konfigurierten Kriterien -8h
	3. Abgleich der bereits in Jira bekannten Sicherheitslücken - 4h
	4. Konvertierung der Daten in passendes Format für Jira's API - 8h
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


### Antwort auf den Hinweis des Prüfungsausschusses:
Die in Punkt 2.1 erwähnten Kriterien, sollen von IT-Fachpersonal konfiguriert werden, da hierzu noch kein extra Tool besteht, soll ein Strukturiertes & Menschlich lesbares Format verwendet werden sein, wie z.B. XML, JSON oder CSV.

Der hohe Zeitaufwand in der Entwicklungsphase in Punkt 2.5 entsteht durch die dynamischen Aufbau der Jira-Tickets, Zwecks Formatierung, welcher einen HTML ähnelt. Dieser Aufbau zieht sich durch zur REST API. Dies bedeutet das zum erstellen eines Tickets, über die API, eine Kombination aus JSON & HTML generiert werden muss. Es gab Firmenintern bereits Verzögerungen, wegen diesem Aufbau. Daher ergibt sich die großzügige Zeitlich Einschätzung.