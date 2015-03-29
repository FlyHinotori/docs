# 1. Zielbestimmung

Das zu entwickelnde Projekt soll der HINOTORI Executive die rechnergestützte Abarbeitung bei der Vercharterung von Geschäftsreiseflugzeugen ermöglichen. 
Der HINOTORI Executive soll ein "Werkzeug" zur Verfügung gestellt werden, mit dem die unterschiedlichen Status von der Aufnahme von Anfragen, das Versenden von Angeboten, Verträgen und Rechnung sowie ein intergriertes Mahnwesen abgebildet werden können. 

Die Software soll durch automatische Verfügbarkeitsprüfungen die Abarbeitung erleichtern und Doppelbuchungen verhindern.

## 1.1.  Musskriterien

- Der Kunde kann Charteranfragen erfassen, Angebote erstellen und nach Flugdurchführung entsprechende Rechnungen an den Kunden versenden. Dabei wird es dem Kunden zu jederzeit möglich sein Änderungen in den Daten vorzunehmen.
- Die Aufnahme einer Charteranfrage erfolgt in der Regel telefonisch. Hierbei sind mindestens folgende Daten zu erfassen:
 - Name und Kontaktdaten des Kunden
 - für Charteroption Einzelflug und Zwischenhalt (Abflugort, Ziel, evtl. Zwischenziel mit Aufenthaltsdauer, gewünschte Flugdaten, Anzahl Passagiere) 
 - für Charteroption über einen Zeitraum nur den Zeitraum
 - Sonderwünsche wie bestimmtes Flugzeug, Crew, Catering, flight attendants,... 
- Die Ausgabe des Angebotes, des Vertrages und der Rechnung für den Interessenten bzw. Kunden erfolgt als Brief per Word oder PDF oder direkt als e-Mail. Das Angebot und die Rechnung sollen zusätzlich ein Bild des Flugzeuges enthalten.
- Im Angebot sollen die Daten der Aufnahme, eine Aussage über die Ausführbarkeit, der Flugzeugtyp mit Bild, ein Flugplan, die Strecke in km sowie die Kosten in EUR enthalten sein.
- Das System soll die Fälligkeiten von Rechnungen überwachen und ein intergriertes Mahnwesen beinhalten. Kunden der Gruppe "VIP" werden jedoch nicht gemahnt. Desweiteren sollen vier Mahnstufen mit mahnstufenabhängigen Kosten ihre Anwendung finden.
- Dem Kunden soll es möglich sein, Stammdatenerfassung/ -änderung für Flugzeuge und Personal vorzunehmen.
- Eine Zuordnung von Flugbegleitern zu einem Flug soll bei kleinen Flugzeugen optional sein. Bei größeren Maschinen ist eine Zuordnung von Flugbegleitern obligatorisch.
- Dem Kunden soll es möglich sein verschiedene Charteroptionen anzubieten. 
 - Einzelflug von A nach B [Fixpreisangebot]
 - Einzelflug von A nach B mit Zwischenstopps [Fixpreisangebot]
 - Charter über einen Zeitraum [Fixpreisanteil und variabler Kostenanteil nach tatsächlicher Flugzeit]
- Die Anwendung soll die Möglichkeit bieten, Kunden in verschiedene Gruppen einzuteilen. Abhängig von der Kundengruppe sind die Optionen Vorkasse und Mahnstufen zu betrachten.
 - VIP [grundsätzlich keine Mahnung]
 - CORP [Dokumentation der Bonität, normales Mahnwesen]
 - PRE [unbekannte Bonität oder bei früheren Flügen (mind. 2) erst nach 2. Mahnung gezahlt, Vorkasse (Angebotspreis + 5%)]
- Mittels einer Terminverwaltung sollen anstehende und derzeitige Aufträge dargestellt werden. Außerdem soll im Hinblick auf die Flugzeugverfügbarkeit Termine wie Flug und Wartung und für die Crewverfügbarkeit Urlaub, Krankheit darstell- und editierbar sein.
- Das System soll selbständig eine Durchführbarkeitsprüfung anhand der Auftragsparameter (Ziel, Crew, Flugzeug,...) unter Berücksichtigung von Flugzeiten, Charterdauer und Zusatzzeiten bei Zwischenlandungen (pro Landung +45min) durchführen können.

## 1.2.  Wunschkriterien

keine

## 1.3.  Abgrenzungskriterien

- Die Anwendung ist kein umfassendes ERP, sondern nur für den konkreten Anwendungsfall ausgelegt.
- Die Anwendung ist weiterhin kein umfassendes ERM. Kunden werden manuell bearbeitet.
- Eine Anfragenaufnahme per Webseite wird nicht Teil dieses Projektes sein.

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
- Ziel: verschicktes Angebot
- Vorbedingung: Kundenanfrage liegt vor
- Nachbedingung Erfolg: alle notwendigen Daten sind erfasst, Angebot wird an Kunden versandt
- Nachbedingung Fehlschlag: Mitteilung an Benutzer, Angebot kann nicht erstellt werden
- Auslösendes Ereignis: eingehende Kundenanfrage
- Beschreibung: Eingabe alle notwendigen Daten zur Angebotserstellung

## /F12/
- Geschäftsprozess: Angebotsantwort erfassen
- Ziel: ausgefüllte Vertragsunterlagen, Reservierung von Crew und Flugzeug
- Vorbedingung: verschicktes Angebot
- Nachbedingung Erfolg: Vertrag erstellten und verschicken
- Nachbedingung Fehlschlag: Grund der Ablehnung erfassen
- Auslösendes Ereignis: eingehende Angebotsantwort
- Beschreibung: kommt es zu einer positiven Angebotsantwort, soll anschließend ein Vertrag erstellt und verschickt werden.

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
- Nachbedingung Fehlschlag: ???
- Auslösendes Ereignis: Meldung der Flugdurchführung durch Crew
- Beschreibung: um den Auftrag abzuschließen und somit eine Rechnung zu erstellen, sind noch einige Daten wie Maschinenlaufzeiten und Crewzeit notwendig.

## /F15/
- Geschäftsprozess: Kundenzufriedenheit erfassen
- Ziel: Kundenzufriedenheit
- Vorbedingung: abgeschlossener Auftrag
- Nachbedingung Erfolg: bereitgestellte Daten zur Auswertung
- Nachbedingung Fehlschlag: ---
- Auslösendes Ereignis: eingehende Antwort zur Kundenzufriedenheit
- Beschreibung: 

## /F16/
- Geschäftsprozess: bestehende Angebote anzeigen
- Ziel: Angebotsdaten einsehen
- Vorbedingung: Angebot wurde erfasst
- Nachbedingung Erfolg: Daten wurden angezeigt
- Nachbedingung Fehlschlag: ---
- Auslösendes Ereignis: ---
- Beschreibung: Visualisierung bestehender Angebote

## /F17/
- Geschäftsprozess: bestehendes Angebot ändern
- Ziel: Angebotsdaten ändern
- Vorbedingung: Angebot wurde erfasst
- Nachbedingung Erfolg: Daten wurden geändert und neues Angebot erstellt
- Nachbedingung Fehlschlag: Mitteilung an Benutzer
- Auslösendes Ereignis: ---
- Beschreibung: Anpassung bestehender Angebote

## /F18/
- Geschäftsprozess: bestehende Verträge anzeigen
- Ziel: Vertragsdaten einsehen
- Vorbedingung: Vertrag wurde erfasst
- Nachbedingung Erfolg: Daten wurden angezeigt
- Nachbedingung Fehlschlag: ---
- Auslösendes Ereignis: ---
- Beschreibung: Visualisierung bestehender Verträge

## /F19/
- Geschäftsprozess: bestehenden Vertrag ändern
- Ziel: Vertragsdaten ändern
- Vorbedingung: Vertrag wurde erfasst
- Nachbedingung Erfolg: Daten wurden geändert und neuer Vertrag erstellt
- Nachbedingung Fehlschlag: Mitteilung an Benutzer
- Auslösendes Ereignis: ---
- Beschreibung: Anpassung bestehender Verträge

## /F21/
- Geschäftsprozess: Zahlungseingang erfassen
- Ziel: Zuordnung von Zahlungen zu Aufträgen
- Vorbedingung: Rechnungslegung
- Nachbedingung Erfolg: Verringerung des fälligen Betrages
- Nachbedingung Fehlschlag: Zahlung als nicht zugeordnet gekennzeichnet
- Auslösendes Ereignis: Zahlungseingang durch Kunden
- Beschreibung: eingegangene Zahlungen sollen einem Auftrag zugeordnet werden. Kann keine Zuordnung erfolgen, bedarf es eines gesonderten Kennzeichen für diese Zahlung zur Recherche

## /F22/
- Geschäftsprozess: Mahnlauf
- Ziel: Liste offener Posten incl. entsprechender Mahnung bzw. offener Überzahlungen
- Vorbedingung: Auftrag abgeschlossen
- Nachbedingung Erfolg: je nach Kundengruppe entsprechende Mahnstufen an den Aufträgen
- Nachbedingung Fehlschlag: --- (keine offenen Posten)
- Auslösendes Ereignis: manuelles Auslösen
- Beschreibung: der Mahnlauf soll bei offenen Forderungen den jeweiligen Aufträgen eine entsprechende Mahnstufe (abhängig von der Kundengruppe) zuordnen. Zwei Zahlungserinnerungen sind kostenlos. Bei den nächsten zwei Mahnungen kommt ein Aufschlag von 5% bzw. 10% hinzu.

## /F31/
- Geschäftsprozess: Termin erfassen
- Ziel: Flugzeuge und Crewmitglieder in der Verfügbarkeit beschränken
- Vorbedingung: keine Terminkollision
- Nachbedingung Erfolg: entsprechender Termineintrag
- Nachbedingung Fehlschlag: Mitteilung an Benutzer
- Auslösendes Ereignis: eingehende Mitteilung
- Beschreibung: Crewmitglieder und Flugzeuge können durch unterschiedliche Termin (Wartung, Urlaub, Krankheit,...) nicht verfügbar sein. Diese Termine müssen erfasst werden.

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

## 8.1. Allgemeine Anforderungen

Standardmässig ist das Windows-Regelwerk anzuwenden. Das vorrangige Bedieninstrument soll die Maus darstellen. 

## 8.2. Komponenten

In den einzelnen Komponenten soll versucht werden, ein wiederkehrendes Grundgerüst zu erzeugen, um eine intuitive und selbsterklärende Benutzung zu ermöglichen.

-- Startmaske

-- Maske1

-- Maske2

# 9. Nichtfunktionale Anforderungen

In Bezug auf ergonomische Anforderungen sowie den Grundsätzen der Dialoggestaltung soll die ISO-Norm 9241-10 Beachtung finden. Die Software wird zusätzlich mit einem Handbuch in deutscher Sprache ausgeliefert. 

# 10. Technische Produktumgebung

Dieses Kapitel beschreibt in welcher Umgebung das Programm laufen soll.

## 10.1. Software

Die Software wird für die folgende Softwareumgebung entwickelt:


- Betriebssystem: Microsoft Windows 7 oder höher

- .NET Framework 4.5


## 10.2. Hardware

Die Software wird auf einem Computer mit den folgenden technischen Daten lauffähig sein:

- Prozessor: 1 GHz oder schneller

- RAM: 2 GB

- Festplattenspeicher: 20 GB

Zusätzliche Standardperipheriegeräte wie Maus, Tastatur und Monitor werden vorausgesetzt.

## 10.3. Produktschnittstellen

Um Angebote, Verträge und Rechnungen zu exportieren, wird eine Schnittstelle mit MS Word angestrebt. Diese Dritt-Software wird damit unabdingbar für die Nutzung des vollen Funktionsumfangs des hier beschriebenen Programms. Zudem wird es, zwecks der Verteilung oben genannter Dokumente, eine einfache Schnittstelle zu dem Standard-eMail-Programm geben.

# 11. spezielle Anforderungen an die Entwicklerumgebung

Für die Entwicklerumgebung gelten folgende Anforderungen:
- C# als Programmiersprache
- Microsoft SQL Server Compact als Datenbank
- SQL Server Compact Toolbox zur Datenbankverwaltung