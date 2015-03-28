# 1. Zielbestimmung

Das zu entwickelnde Projekt soll der HINOTORI Executive die rechnergestützte Angebotserstellung zur Vercharterung von Geschäftsreiseflugzeugen ermöglichen.

## 1.1.  Musskriterien

- Charteraufträge erfassen und bearbeiten (Daten ändern, Auftrag löschen)
- Rechnung erstellen
    - export als pdf
    - editierbare Vorlage
- Angebotsausgabe als Brief incl. Bild
    - per Word oder 
	- per PDF oder
	- per Mail
- Vertragsausgabe wie Angebotsausgabe (ohne Bild)
- Rechnungsausgabe wie Angebotsausgabe
- Überwachung der Fälligkeit von Rechnungen
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

Wird der Flug gebucht, werden die jeweiligen Ressourcen für den gewünschten Zeitraum als belegt markiert. Eventuelle Buchungskonflikte, die sich aus gleichzeitiger Buchung oder Änderungen einer Buchung ergeben, werden in einer Mitteilung im Programm deutlich gemacht.

### 2.1.2. Charterflugabrechnung

Rechnungserstellung für fertige Aufträge von Charterflügen wird automatisch vom Programm vorgenommen. Sie wird nach einer Vorlage in PDF-Form ausgegeben und enthält die wesentlichen Eckdaten des Flugs, die Kosten, Steuern und Kontoverbindungsdaten. Für die Zuordnung der Papierabschrift wird auch die Buchungsnummer mit aufgeführt.

### 2.1.3. Ressourcenplanung

Grundsätzlich ist davon auszugehen, dass Flugpersonal jederzeit einsatzfähig ist. Nachtflüge oder Langstreckenflüge werden also nicht ausgeschlossen. Entsprechend werden die jeweiligen Beteiligten nur als gebucht gekennzeichnet, wenn sie einer Buchung zugeordnet sind. Feste Arbeitszeiten oder Feiertage bleiben unberücksichtigt.

Personal und Fluggerät werden nur einer Buchung zugeordnet. Mehrere Buchungen miteinander zu verbinden (z.B. Hin- und Rückflug am gleichen Tag in verschiedenen Buchungen) wird ausdrücklich ausgeschlossen.

## 2.2. Zielgruppen

Die Software wird ausschließlich von Mitarbeitern des Kunden bedient. Zu diesen Mitarbeitern gehören primär Bürofachkräfte sowie Manager. 

Erstere sind für die Charterflugplanung, Angebots- und Vertragserstellung sowie dem Mahnwesen zuständig. Letztere für die Pflege der Stammdaten (Personal, Flugzeug, etc.).

Endkunden werden explizit von der Zielgruppe ausgeschlossen, da die Erstellung einer Internetpräsenz kein Teil dieses Projekts ist.

## 2.3. Betriebsbedingungen

Die Lauffähigkeit der Software erfordert Computer-Hardware sowie zusätzliche Software. Auf Details zu diesen Anforderungen wird später in dem Kapitel "Technische Produktumgebung" eingegangen.

Es wird davon ausgegangen, dass die Software in einer Büroumgebung zum Einsatz kommt. Sie wird zu den Geschäftszeiten des Kunden betrieben, ist aber nicht für den Dauerbetrieb (24/7) gedacht. 

Nach der Installation auf dem Kunden-Computer, wird die Software nur auf diesem betrieben. Ein zentraler Datenbankserver, der das parallele Arbeiten auf mehreren Klientensystemen erlaubt, ist nicht Teil dieses Projekts.

# 3. Produktübersicht

# 4. Geschäftsprozesse

## /F11/
- Geschäftsprozess: Neues Angebot erfassen
- Ziel: Erstellung des Angebots in oben genannter Form
- Vorbedingung: Kundenanfrage liegt vor
- Nachbedingung Erfolg: alle notwendigen Daten sind erfasst, Angebot wurde erstellt
- Nachbedingung Fehlschlag: Mitteilung an Benutzer (inkl. Begründung), Angebot kann nicht erstellt werden
- Auslösendes Ereignis: eingehende Kundenanfrage
- Beschreibung: Eingabe aller notwendigen Daten zur Angebotserstellung

## /F12/
- Geschäftsprozess: Angebotsantwort erfassen
- Ziel: Vorbereitung der Vertragsunterlagen, Reservierung von Crew und Flugzeug
- Vorbedingung: verschicktes Angebot
- Nachbedingung Erfolg: Vertrag vorbereitet (basierend auf der Vorlage aus der Ausschreibung) 
- Nachbedingung Fehlschlag: Vertrag nicht erstellt, Grund der Ablehnung wird erfasst
- Auslösendes Ereignis: eingehende Angebotsantwort
- Beschreibung: kommt es zu einer positiven Angebotsantwort, soll anschließend ein Vertrag vorbereitet werden

## /F13/
- Geschäftsprozess: Vertragsantwort erfassen
- Ziel: Rechnungslegung und Terminierung von Crew, Catering und Flugzeug
- Vorbedingung: verschickter Vertrag
- Nachbedingung Erfolg: Rechnung wird an Kunden verschickt
- Nachbedingung Fehlschlag: Dokumentation der negativen Antwort
- Auslösendes Ereignis: eingehende Vertragsantwort
- Beschreibung: bei einer positiven Vertragsantwort soll es zur festen Terminierung von Crew, Catering und Flugzeug sowie zur Rechnungslegung kommen.

## /F14/
- Geschäftsprozess: Flugnachbereitung
- Ziel: Endabrechnung des Auftrages - Rechnung
- Vorbedingung: durchgeführter Flug
- Nachbedingung Erfolg: Rechnung und Abfrage der Kundenzufriedenheit
- Nachbedingung Fehlschlag: ---
- Auslösendes Ereignis: Meldung der Flugdurchführung durch Crew
- Beschreibung: um den Auftrag abzuschließen und somit eine Rechnung zu erstellen, sind noch einige Daten wie Maschinenlaufzeiten und Crewzeit notwendig.

## /F15/
- Geschäftsprozess: Kundenzufriedenheit erfassen
- Ziel: Dokumentation der Kundenzufriedenheit
- Vorbedingung: durchgeführter Flug
- Nachbedingung Erfolg: bereitgestellte Daten zur Auswertung
- Nachbedingung Fehlschlag: ---
- Auslösendes Ereignis: Meldung der Flugdurchführung durch Crew
- Beschreibung: Durch einen Fragebogen wird die Kundenzufriedenheit erfasst

## /F16/
- Geschäftsprozess: bestehende Angebote anzeigen
- Ziel: Angebotsdaten einsehen
- Vorbedingung: Angebot wurde erfasst
- Nachbedingung Erfolg: Daten werden angezeigt
- Nachbedingung Fehlschlag: ---
- Auslösendes Ereignis: ---
- Beschreibung: Visualisierung bestehender Angebote inkl. deren Status

## /F17/
- Geschäftsprozess: bestehendes Angebot ändern
- Ziel: Angebotsdaten ändern
- Vorbedingung: Angebot wurde erfasst
- Nachbedingung Erfolg: Daten werden geändert und Angebotsstatus zurück gesetzt
- Nachbedingung Fehlschlag: Mitteilung an Benutzer (inkl. Begründung)
- Auslösendes Ereignis: ---
- Beschreibung: Anpassung bestehender Angebote

## /F18/
- Geschäftsprozess: bestehende Verträge anzeigen
- Ziel: Vertragsdaten einsehen
- Vorbedingung: Vertrag wurde erfasst
- Nachbedingung Erfolg: Daten werden angezeigt
- Nachbedingung Fehlschlag: ---
- Auslösendes Ereignis: ---
- Beschreibung: Visualisierung bestehender Verträge

## /F19/
- Geschäftsprozess: bestehenden Vertrag ändern
- Ziel: Vertragsdaten ändern
- Vorbedingung: Vertrag wurde erfasst
- Nachbedingung Erfolg: Daten werden geändert und neuer Vertrag erstellt
- Nachbedingung Fehlschlag: Mitteilung an Benutzer
- Auslösendes Ereignis: ---
- Beschreibung: Anpassung bestehender Verträge

## /F21/
- Geschäftsprozess: Zahlungseingang erfassen
- Ziel: Zuordnung von Zahlungen zu Rechnungen
- Vorbedingung: Rechnungslegung
- Nachbedingung Erfolg: Verringerung des fälligen Betrages einer Rechnung
- Nachbedingung Fehlschlag: Zahlung als nicht zugeordnet gekennzeichnet
- Auslösendes Ereignis: Zahlungseingang durch Kunden
- Beschreibung: eingegangene Zahlungen sollen einer Rechnung zugeordnet werden. Kann keine Zuordnung erfolgen, bedarf es eines gesonderten Kennzeichens für diese Zahlung zur Recherche

## /F22/
- Geschäftsprozess: Mahnlauf
- Ziel: Liste offener Posten inkl. entsprechender Mahnung bzw. offener Überzahlungen
- Vorbedingung: Auftrag abgeschlossen
- Nachbedingung Erfolg: je nach Kundengruppe entsprechende Mahnstufen an den Aufträgen
- Nachbedingung Fehlschlag: --- (keine offenen Posten)
- Auslösendes Ereignis: ---
- Beschreibung: der Mahnlauf soll bei offenen Forderungen den jeweiligen Aufträgen eine entsprechende Mahnstufe (abhängig von der Kundengruppe) zuordnen. Zwei Zahlungserinnerungen sind kostenlos. Bei den nächsten zwei Mahnungen kommt ein Aufschlag von 5% bzw. 10% hinzu.

## /F31/
- Geschäftsprozess: Termin erfassen
- Ziel: Flugzeuge und Crewmitglieder in der Verfügbarkeit beschränken
- Vorbedingung: keine Terminkollision
- Nachbedingung Erfolg: entsprechender Termineintrag
- Nachbedingung Fehlschlag: Mitteilung an Benutzer
- Auslösendes Ereignis: eingehende Mitteilung
- Beschreibung: Crewmitglieder und Flugzeuge können durch unterschiedliche Termin (Wartung, Urlaub, Krankheit,...) nicht verfügbar sein. Diese Termine müssen erfasst werden.

## /F???/
- Geschäftsprozess:
- Ziel:
- Vorbedingung: 
- Nachbedingung Erfolg:
- Nachbedingung Fehlschlag:
- Auslösendes Ereignis:
- Beschreibung:

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

Eine einfach zu bedienende und übersichtliche Software wird vom Auftraggeber gefordert. Dies impliziert die folgenden Qualitätsanforderungen an die Benutzerschnittstelle.

Die Benutzeroberfläche wird sinnvoll aufgeteilt, indem zusammengehörige Informationen gruppiert und dadurch optisch vom Rest abgrenzbar sind. Durch verständliche Symbole oder Beschreibungen wird dem Benutzer die Funktion eines Bedienelementes vermittelt.  

Wiederkehrende Aufgaben werden einfach und in wenigen Schritten bearbeitbar sein. Gängige Tastaturkürzel (Shortcuts) helfen dabei, einfache, wie auch komplexere Aufgaben, in möglichst kurzer Zeit zu bewältigen.

Bei der Bearbeitung einer Aufgabe wird auf die Darstellung wie auch Erfassung redundanter Informationen verzichtet. Dem Benutzer sind nur die relevanten Informationen und Bedienelemente direkt dargestellt. Zusatzfunktionen, sofern diese dem Zweck des jeweiligen Kontextes dienen, werden nur über Menüs oder den besagten Shortcuts erreichbar sein.

Hinweise, Warn- oder Fehlermeldungen, die für den Benutzer von Interesse sind, werden klar präsentiert. Deutsch wird dabei, wie in der restlichen Oberfläche, die verwendete Sprache sein. 

Das Verhalten der Software wird in sich konsistent und an vergleichbare Anwendungen im Windows-Umfeld angelehnt sein.


# 8. Benutzeroberfläche

- Allgemeine Anforderungen

Standardmässig ist das Windows-Regelwerk anzuwenden. Das vorrangige Bedieninstrument soll die Maus darstellen. Außerdem soll die ISO-Norm 9241-10 in Bezug auf ergonomische Anforderungen sowie den Grundsätzen der Dialoggestaltung Beachtung finden.

- Komponenten

In den einzelnen Komponenten soll versucht werden, ein wiederkehrendes Grundgerüst zu erzeugen, um eine intuitive und selbsterklärende Benutzung zu ermöglichen.

-- Startmaske

-- Maske1

-- Maske2

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
