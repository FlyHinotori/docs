# 1. Zielbestimmung

Das zu entwickelnde Projekt soll der HINOTORI Executive die rechnergestützte Angebotserstellung zur Vercharterung von Geschäftsreiseflugzeugen ermöglichen.

## 1.1.  Musskriterien

Funktionalität

- Charteraufträge erfassen, bearbeiten und abrechnen incl. Fälligkeitsüberwachung und Mahnwesen
- Stammdatenerfassung/ -änderung für Flugzeuge
- Stammdatenerfassung/ -änderung für Personal
- optionale Buchung von "flight attendants" bei kleinen Flugzeugen; bei den größeren müssen " flight attendants" gebucht werden
- Abdecken verschiedener Charteroptionen (Einzelflug von A nach B [Fixpreisangebot], Einzelflug von A nach B mit Zwischenstopp [Fixpreisangebot], Charter über einen Zeitraum [Fixpreisanteil und variabler Kostenanteil nach tatsächlicher Flugzeit])
- Einteilung der Kunden in Gruppen (VIP [grundsätzlich keine Mahnung], CORP [Dokumentation der Bonität, normales Mahnwesen],  PRE [unbekannte Bonität oder bei früheren Flügen (mind. 2) erst nach 2. Mahnung gezahlt, Vorkasse (Angebotspreis + 5%)]
- Telefonische Aufnahme einer Anfrage mit mind. folgenden Daten (Name und Kontaktdaten des Kunden, Art der Charteroption; für Einzelflug und Zwischenhalt zusätzlich Abflugort, Ziel, evtl. Zwischenziel mit Aufenthaltsdauer, gewünschte Flugdaten, Anzahl Passagiere; für Charteroption über einen Zeitraum nur den Zeitraum; Sonderwünsche wie bestimmtes Flugzeug, Crew, Catering, flight attendants,... )
- Angebot soll enthalten (Daten der Aufnahme, Aussage über Ausführbarkeit, Flugzeugtyp mit Bild, Flugplan, Strecke in km, Kosten in EUR)
- Terminverwaltung (anstehende, derzeitige Aufträge; Flugzeugverfügbarkeit [Flug, Wartung, ...], Crewverfügbarkeit)
- Programmgestützte Durchführbarkeitsprüfung anhand Auftragsparametern (Ziel, Crew, Flugzeug,...) unter Berücksichtigung von Flugzeiten, Charterdauer und Zusatzzeiten bei Zwischenlandungen (pro Landung +45min)


## 1.2.  Wunschkriterien
Anfrage des Kunden per Webseite ist optional

## 1.3.  Abgrenzungskriterien

# 2. Produkteinsatz

## 1.1.  Anwendungsbereiche

## 2.1.  Zielgruppen

## 2.2.  Betriebsbedingungen

# 3. Produktübersicht

# 4. Geschäftsprozesse

# 5. Produktdaten
- Flugzeugdaten 
 - Hersteller
 - Typ
 - Flugbetriebsmannschaft
 - Stewardessen
 - Reichweite in km
 - Anzahl Passagiere
 - Reisegeschwindigkeit
 - Anzahl der Triebwerke
 - Triebwerksart
 - jährliche Fixkosten (nach Typ)
 - variable Kosten pro Stunde
 - Status (aktiv/inaktiv)
- Personaldaten
 - Name
 - Vorname
 - Position (Captain, Copilot, Cabin, Crew)
 - Lizenzen (Hier eine Liste der Flugzeuge, für die die Person qualifiziert ist)
 - Gehalt nach Position
 - Status (aktiv/inaktiv)
- Flugziele
 - Bezeichnung (Flughafen)
 - Ort
 - Land
 - Geo-Koordinaten
- Termine
 - Art (Charter, Urlaub Crew, Wartung, Jahresscheck Flugzeug, etc)
 - von (Datum, Zeit)
 - bis (Datum, Zeit)
- Auftrag
 - Auftraggeber (Kontaktdaten)
 - Termin (Link zu Termine)
 - Art (Option 1,2 oder 3)
 - Von (Flughafen/Ort) bei Option 1 und 2
 - Nach (Flughafen/Ort) bei Option 1 und 2
 - Zwischenziele (Flughäfen/Orte) bei Option 1 und 2
 - Anzahl der Passagiere bei Option 1 und 2
 - Charterdauer bei Option 3
 - Wunschflugzeug
 - Wunschcrew (Flight)
 - Wunschcrew (Cabin)
 - Weitere Wünsche (Textfeld)
 - Preis
 - Status (geplant, beauftragt, in Durchführung, beendet, abgebrochen)
 - Anmerkungen (z.B. Abbruchgrund)
- Produktleistungen
- 
 

# Qualitätsanforderungen

# Benutzeroberfläche

# Allgemeine Anforderungen

# Komponenten

# Startmaske

# Projektübersicht

# Mitarbeiterdetails

# Nichtfunktionale Anforderungen

# Technische Produktumgebung

Dieses Kapitel beschreibt in welcher Umgebung das Programm laufen soll.

## Software ##

Die Software wird für die folgende Softwareumgebung entwickelt:


- Betriebssystem: Microsoft Windows 7 oder höher

- .NET Framework 4.5
 

## Hardware ##

Die Software wird auf einem Computer mit den folgenden technischen Daten lauffähig sein:

- Prozessor: 1 GHz oder schneller 

- RAM: 2 GB

- Festplattenspeicher: 20 GB 

## Orgware ##

## Produktschnittstellen ##


# spezielle Anforderungen an die Entwicklerumgebung
