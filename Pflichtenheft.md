# 1. Zielbestimmung

Das zu entwickelnde Projekt soll der HINOTORI Executive die rechnergestützte Angebotserstellung zur Vercharterung von Geschäftsreiseflugzeugen ermöglichen.

## 1.1.  Musskriterien

- Charteraufträge erfassen und bearbeiten (Daten ändern, Auftrag löschen)
- Rechnung erstellen
    - export als pdf
    - editierbare Vorlage
- Überwachnung der Fälligkeit von Rechnungen
- automatische Mahnungserstellung
- Stammdatenerfassung/ -änderung für Flugzeuge
- Stammdatenerfassung/ -änderung für Personal
- Zuordnung von Flugbegleitern zu einem Flug
    - optional bei kleinen Flugzeugen
    - obligatorisch bei größeren Maschinen
- Abdecken verschiedener Charteroptionen (Einzelflug von A nach B [Fixpreisangebot], Einzelflug von A nach B mit Zwischenstopp [Fixpreisangebot], Charter über einen Zeitraum [Fixpreisanteil und variabler Kostenanteil nach tatsächlicher Flugzeit])
- Einteilung der Kunden in Gruppen (VIP [grundsätzlich keine Mahnung], CORP [Dokumentation der Bonität, normales Mahnwesen],  PRE [unbekannte Bonität oder bei früheren Flügen (mind. 2) erst nach 2. Mahnung gezahlt, Vorkasse (Angebotspreis + 5%)]
- Telefonische Aufnahme einer Anfrage mit mind. folgenden Daten (Name und Kontaktdaten des Kunden, Art der Charteroption; für Einzelflug und Zwischenhalt zusätzlich Abflugort, Ziel, evtl. Zwischenziel mit Aufenthaltsdauer, gewünschte Flugdaten, Anzahl Passagiere; für Charteroption über einen Zeitraum nur den Zeitraum; Sonderwünsche wie bestimmtes Flugzeug, Crew, Catering, flight attendants,... )
- Angebot soll enthalten (Daten der Aufnahme, Aussage über Ausführbarkeit, Flugzeugtyp mit Bild, Flugplan, Strecke in km, Kosten in EUR)
- Terminverwaltung (anstehende, derzeitige Aufträge; Flugzeugverfügbarkeit [Flug, Wartung, ...], Crewverfügbarkeit)
- Programmgestützte Durchführbarkeitsprüfung anhand Auftragsparametern (Ziel, Crew, Flugzeug,...) unter Berücksichtigung von Flugzeiten, Charterdauer und Zusatzzeiten bei Zwischenlandungen (pro Landung +45min)

## 1.2.  Wunschkriterien
- Anfrage des Kunden per Webseite
- WF01-Charterflug kann komplett per Webseite ablaufen. Jedoch muss die Funktion des Druckens des Vertrages gegeben sein.

## 1.3.  Abgrenzungskriterien
- kein umfassendes ERP, das System ist nur für den konkreten Anwendungsfall ausgelegt
- kein umfassendes ERM, Kunden werden manuell bearbeitet

# 2. Produkteinsatz

Die HINOTORI Executive beauftragt die Erstellung des Programms zur internen Verwendung. Ein Weiterverkauf oder eine Weitergabe ist ausgeschlossen.

## 2.1. Anwendungsbereiche

### 2.1.1. Charterflugplanung

Erstellung eines Charterfluges mit Rückmeldung über Verfügbarkeit der Crew, des Flugzeugs, und aller anderen Ressourcen die dafür erforderlich sind. Dabei wird auch der Zeitraum und die Flugroute, sowie Start- und Zielpunkte festgelegt und die Kosten errechnet.

Wird der Flug gebucht wird für den Kunden automatisch eine Rechnung erstellt und die Ressourcen werden für den gewünschten Zeitraum als belegt markiert. Eventuelle Buchungskonflikte, die sich auch gleichzeitiger Buchung oder Änderungen einer Buchung ergeben werden in einer Mitteilung im Programm deutlich gemacht.

### 2.1.2. Charterflugabrechnung

Rechnungserstellung für fertige Aufträge von charterflügen wird automatisch vom Programm vorgenommen. Sie wird nach einer Vorlage in PDF-Form ausgegeben und enthält die wesentlichen Eckdaten des Flugs, die Kosten, Steuern und Kontoverbindungsdaten. Für die Zuordnung der Papierabschrift wird auch die Buchungsnummer mit aufgeführt.

Wenn sich ein Charterflugauftrag sich ändert und der Rechnungsbetrag sich dabei ebenfalls ändert, wird am Ende der Änderung eine neue Rechnung erstellt. Diese enthält zusätzlich zu einer neuen Rechnungsnummer auch einen Verweis auf die bereits erstellte, und mit der neuen Rechnung nun unwirksame, Rechnung.

### 2.1.3. Resourcenplanung

Grundsätzlich ist davon auszugehen das Flugpersonal jederzeit einsatzfähig ist. Nachtflüge oder Langstreckenflüge werden also nicht ausgeschlossen. Entsprechend werden die jeweiligen Beteiligten nur als gebucht gekennzeichnet wenn sie einer Buchung zugeordnet sind. Feste Arbeitszeiten oder Feiertage bleiben unberücksichtigt.

Personal und Fluggerät wird nur einer Buchung zugeordnet. Mehrere Buchungen miteinander zu Verbinden (z.B. Hin- und Rückflug am gleichen Tag in verschiedenen Buchungen) wird ausdrücklich ausgeschlossen.

### 2.1.4. Rechnungserstellung

Für jede vollständig asugefüllte Buchung die eingeht wird eine Rechnung erstellt. Ändert sich eine Buchung und die Kosten ändern sich dabei ebenfalls wird eine neue Rechnung für die gleiche Buchung erstellt.

Jede Rechnung wird dem Kunden in PDF Form zur Verfügung gestellt. Wenn sich Buchungen ändert wird eine weitere PDF Rechnung erstellt, die zusätzlich zu den üblichen Rechnungsdaten auch den Hinweis enthält das alle vorherigen Rechnungen ihre Gültigkeit verlieren.

## 2.2. Zielgruppen

### 2.2.1. Kunde

### 2.2.2. Verwaltung

## 2.3. Betriebsbedingungen

# 3. Produktübersicht

# 4. Geschäftsprozesse
- WF01-Charterflug
 - Anfrage aufnehmen
 - Prüfen der Durchführbarkeit zum Termin
  - Flugzeug verfügbar?
  - FlightCrew verfügbar?
  - CabinCrew verfügbar?
 - nicht durchführbar --> Benachrichtigung incl. Begründung --> Ende
 - durchführbar --> Angebotserstellung --> verschicken --> warten auf Antwort
 - Bei Vorliegen der Antwort
  - positiv --> Vertrag vorbereiten (siehe Vertragsvordruck) --> verschicken --> warten auf Antwort
  - negativ --> Grund erfragen --> Ende
 - Vertrag unterschrieben zurück --> Flugzeug, Crew, Catering bereitstellen --> Rechnung erstellen und verschicken, Zahlung verfolgen --> Flug durchführen --> Flugnachbereitung (Abfrage von Motorenlaufzeiten und Crewzeit) --> Kundenzufriedenheit erfragen --> Ende
 - Vertrag nicht zurück --> Dokumentation --> Ende

FRAGE: Workflow passt nicht zu den Charteroptionen! Anpassung?

- WF02-Kostenverfolgung
 - Zahlungseingänge verfolgen
 - Zahlung überfällig
  - Mahnwesen (je nach Kundengruppe)
  - 2 Zahlungserinnerungen kostenlos --> 2 Mahnstufen (+5%, +10%)
 - evtl. Überzahlung bei Kundenstatus PRE zurückerstatten

FRAGE: Bisher gab es keine Statuus für Kunden! Ist hier die Kundengruppe gemeint?

# 5. Produktdaten

## 5.1. Flugzeugdaten
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

## 5.2. Personaldaten
 - Name
 - Vorname
 - Position (Captain, Copilot, Cabin, Crew)
 - Lizenzen (Hier eine Liste der Flugzeuge, für die die Person qualifiziert ist)
 - Gehalt nach Position
 - Status (aktiv/inaktiv)

## 5.3. Flugziele
 - Bezeichnung (Flughafen)
 - Ort
 - Land
 - Geo-Koordinaten

## 5.4. Termine
 - Art (Charter, Urlaub Crew, Wartung, Jahresscheck Flugzeug, etc)
 - von (Datum, Zeit)
 - bis (Datum, Zeit)

## 5.5. Auftrag
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

## 5.6. Mahnwesen
 - Auftrag (Link zum Auftrag)
 - Status (Rechnung erstellt, verschickt, bezahlt; Erinnerung 1, 2; Mahnung 1,2; Rechnung nicht bezahlt)
 - Zusatzkosten

# 6. Produktleistungen

## 6.1. Analyse
 - Kundenzufriedenheit analysieren
 - Ablehnungsgründe der Angebote analysieren
 - Profitabilität der Flugzeuge analysieren (Annahme: 2000h pro Flugzeug pro Jahr = Profitabilität)

## 6.2. Berechnungen bei Angebotserstellung
 - Anzahl der nötigen Zwischenlandungen (pro Landung +45min Charterdauer)
 - Kosten (Anteil Fixkosten + Anteil Personalkosten + Stundensatz * Flugzeit)

# 7. Qualitätsanforderungen

# 8. Benutzeroberfläche

- Allgemeine Anforderungen
 - einfache Bedienung
 - übersichtlich
 - erweiterbar

- Komponenten
 - Angebotsausgabe als Brief auf Word oder PDF oder per Mail incl. Bild
 - Vertragsausgabe wie Angebotsausgabe (ohne Bild)
 - Rechnungsausgabe wie Angebotsausgabe

- Startmaske

- Projektübersicht

- Mitarbeiterdetails

# 9. Nichtfunktionale Anforderungen

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

Zusätzliche Standardperipheriegeräte wie Maus, Tastatur und Monitor werden vorausgesetzt.

## Produktschnittstellen ##

Keine externen Schnittstellen zu anderer Software geplant.

# 11. spezielle Anforderungen an die Entwicklerumgebung
