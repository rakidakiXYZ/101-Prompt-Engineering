# KI-Gesprächsanalyse für Finanzberatung

## Vollständige Anleitung für Einsteiger

---

# Teil 1: Einführung und Anleitung

## Was ist dieser Prompt und wofür wird er verwendet?

Dieser Prompt ist eine detaillierte Anweisung für eine Künstliche Intelligenz (KI), um Beratungsgespräche aus dem Finanzdienstleistungsbereich systematisch zu analysieren. Die KI wertet dabei ein Gesprächstranskript (verschriftlichtes Gespräch) aus und erstellt eine strukturierte Auswertung mit Bewertungen, Zusammenfassungen und konkreten Handlungsempfehlungen.

### Typische Anwendungsfälle

- Qualitätssicherung in der Finanzberatung
- Coaching und Weiterbildung von Berater:innen
- Dokumentation von Beratungsgesprächen
- Identifikation von Verbesserungspotenzialen
- Nachverfolgung von Vereinbarungen und To-Dos

---

## Voraussetzungen

### Was Sie benötigen

1. **Eine Audio-Aufnahme** des Beratungsgesprächs (mit Einverständnis aller Beteiligten!)
2. **Ein Transkriptionstool** zur Umwandlung von Audio in Text
3. **Zugang zu einer KI** wie Claude, ChatGPT oder ähnliche

### Empfohlene Transkriptionstools

| Tool | Beschreibung | Kosten |
|------|--------------|--------|
| **OpenAI Whisper** | Sehr genaue Transkription, auch für Deutsch | Kostenlos (lokal) oder günstig (API) |
| **Amberscript** | Deutscher Anbieter, DSGVO-konform | Kostenpflichtig |
| **Happy Scribe** | Gute Qualität, viele Sprachen | Kostenpflichtig |
| **Microsoft Word** | Integrierte Diktierfunktion | In Microsoft 365 enthalten |
| **Trint** | Professionelle Lösung | Kostenpflichtig |

---

## Schritt-für-Schritt-Anleitung

### Schritt 1: Audio-Aufnahme vorbereiten

Stellen Sie sicher, dass:
- Die Aufnahme eine gute Tonqualität hat
- Alle Gesprächsteilnehmer hörbar sind
- Sie die Einwilligung zur Aufnahme und Verarbeitung haben
- Die Datei in einem gängigen Format vorliegt (MP3, WAV, M4A)

### Schritt 2: Transkription erstellen

Wandeln Sie die Audio-Aufnahme in Text um:

1. Laden Sie die Audio-Datei in Ihr Transkriptionstool hoch
2. Wählen Sie "Deutsch" als Sprache
3. Aktivieren Sie (falls verfügbar) die Sprechererkennung
4. Starten Sie die Transkription
5. Überprüfen und korrigieren Sie das Ergebnis bei Bedarf

**Tipp:** Kennzeichnen Sie die Sprecher im Transkript deutlich, z.B.:
```
Berater: Guten Tag, schön dass Sie da sind...
Kunde: Danke, ich freue mich auch...
```

### Schritt 3: KI-Tool öffnen

Öffnen Sie Ihr bevorzugtes KI-Tool:
- **Claude** (claude.ai)
- **ChatGPT** (chat.openai.com)
- **Andere KI-Assistenten**

### Schritt 4: Prompt eingeben

1. Kopieren Sie den vollständigen Prompt (siehe Teil 2 dieser Anleitung)
2. Fügen Sie ihn in das Eingabefeld der KI ein
3. Fügen Sie direkt darunter Ihr Transkript ein

**Wichtig:** Trennen Sie Prompt und Transkript deutlich, z.B.:

```
[HIER DEN PROMPT EINFÜGEN]

---

TRANSKRIPT DES GESPRÄCHS:

[HIER DAS TRANSKRIPT EINFÜGEN]
```

### Schritt 5: Analyse starten

Senden Sie die Nachricht ab. Die KI wird nun:
- Das Transkript analysieren
- Alle 11 Analysebereiche durcharbeiten
- Eine strukturierte Auswertung erstellen

**Bearbeitungszeit:** Je nach Länge des Transkripts 30 Sekunden bis 2 Minuten.

### Schritt 6: Ergebnis prüfen und nutzen

Überprüfen Sie die Analyse:
- Sind alle Vereinbarungen korrekt erfasst?
- Stimmen die identifizierten Kundenziele?
- Sind die Bewertungen nachvollziehbar?

---

## Häufige Fragen (FAQ)

### Wie lang darf das Transkript sein?

Die meisten KI-Tools können Texte von 10.000 bis 100.000 Zeichen verarbeiten. Ein typisches 30-minütiges Gespräch umfasst etwa 4.000-6.000 Wörter, was problemlos verarbeitet werden kann.

### Was tun bei sehr langen Gesprächen?

Bei Gesprächen über 60 Minuten können Sie:
- Das Gespräch in Teile aufteilen und separat analysieren
- Nur die relevantesten Abschnitte analysieren lassen
- Eine Zusammenfassung des Transkripts erstellen lassen und diese dann analysieren

### Wie genau sind die Bewertungen?

Die KI-Bewertungen sind Orientierungswerte. Sie basieren auf dem, was im Transkript steht. Nonverbale Kommunikation (Mimik, Gestik, Tonfall) kann nur begrenzt erfasst werden, wenn sie im Transkript nicht beschrieben ist.

### Kann ich den Prompt anpassen?

Ja! Sie können den Prompt an Ihre Bedürfnisse anpassen:
- Fügen Sie branchenspezifische Kriterien hinzu
- Entfernen Sie nicht benötigte Abschnitte
- Passen Sie die Bewertungskriterien an Ihre Standards an

### Ist die Nutzung datenschutzkonform?

Beachten Sie:
- Holen Sie Einwilligungen für Aufnahme und Verarbeitung ein
- Prüfen Sie die Datenschutzrichtlinien Ihres KI-Tools
- Anonymisieren Sie sensible Daten bei Bedarf vor der Analyse
- Speichern Sie Ergebnisse sicher und löschen Sie sie nach Gebrauch

---

## Tipps für bessere Ergebnisse

### Transkriptqualität verbessern

- Korrigieren Sie offensichtliche Transkriptionsfehler
- Ergänzen Sie fehlende Satzzeichen
- Kennzeichnen Sie unverständliche Passagen mit [unverständlich]

### Kontext hinzufügen

Geben Sie der KI zusätzlichen Kontext, z.B.:
```
Kontext: Der Kunde ist 28 Jahre alt, Berufseinsteiger im IT-Bereich, 
ledig, Nettoeinkommen ca. 3.200€. Erstes Beratungsgespräch.
```

### Spezifische Fragen stellen

Nach der Analyse können Sie Folgefragen stellen:
- "Welche konkreten Formulierungen hätte der Berater besser wählen können?"
- "Erstelle einen Entwurf für die Zusammenfassungs-E-Mail an den Kunden."
- "Welche Themen wurden möglicherweise vergessen?"

---

## Fehlerbehebung

### Problem: Die KI gibt keine vollständige Analyse

**Lösung:** Bitten Sie die KI, die Analyse fortzusetzen:
"Bitte führe die Analyse ab Abschnitt 7 fort."

### Problem: Bewertungen erscheinen unfair

**Lösung:** Bitten Sie um Begründung:
"Erkläre bitte, warum du Empathie & Beziehung nur mit 6/10 bewertet hast. Welche konkreten Stellen im Gespräch haben zu dieser Bewertung geführt?"

### Problem: Wichtige Inhalte fehlen

**Lösung:** Weisen Sie die KI darauf hin:
"Im Gespräch wurde auch über eine Haftpflichtversicherung gesprochen. Bitte ergänze dies in der Analyse."

---

# Teil 2: Der vollständige Prompt

Kopieren Sie den folgenden Prompt vollständig und fügen Sie ihn vor Ihrem Transkript ein:

---

```markdown
Du bist ein Experte für die Analyse von Beratungsgesprächen im Finanzdienstleistungsbereich. Analysiere das folgende Gesprächstranskript und erstelle eine strukturierte Auswertung nach dem unten beschriebenen Schema.

---

## 1. KURZZUSAMMENFASSUNG

Fasse das Gespräch in 2-3 Sätzen zusammen. Beschreibe:
- Was hat der/die Berater:in vorgestellt?
- Welche Kundensituation liegt vor (z.B. Berufseinsteiger, Familie, Rentner)?
- Welchen Maßnahmen hat der Kunde zugestimmt?
- Wurden Folgetermine vereinbart?

---

## 2. REDEANTEILE

Berechne den prozentualen Redeanteil:
- Berater:in: X%
- Kunde: X%

Hinweis: Ein ausgewogenes Verhältnis liegt bei ca. 60-70% Berater und 30-40% Kunde. Starke Abweichungen (>80% Berater) können auf mangelnde Kundeneinbindung hindeuten.

---

## 3. KOMMUNIKATIONSQUALITÄT

### Gesamtbewertung: X/10

Bewerte die Gesamtqualität des Gesprächs und begründe kurz (2-3 Sätze), was gut lief und wo Verbesserungspotenzial besteht.

---

## 4. STIMMUNG

Kategorisiere die Gesamtstimmung des Gesprächs:
- **Positiv**: Konstruktive Atmosphäre, Kunde wirkt zufrieden und engagiert
- **Neutral**: Sachlich, weder besonders positiv noch negativ
- **Negativ**: Angespannte Atmosphäre, Unzufriedenheit erkennbar

---

## 5. DETAILBEWERTUNGEN (jeweils X/10 mit Begründung)

### 5.1 Klarheit & Verständlichkeit (X/10)

Bewerte:
- Wurden Inhalte und Empfehlungen klar vermittelt?
- Wurden Fachbegriffe erklärt?
- Gab es Wiederholungen oder unpräzise Formulierungen?

### 5.2 Empathie & Beziehung (X/10)

Bewerte:
- Wurde auf persönliche Situation/Ängste/Präferenzen eingegangen?
- Gab es unterstützende, wertschätzende Formulierungen?
- Wurde aktiv zugehört und nachgefragt?

### 5.3 Struktur & Gesprächsführung (X/10)

Bewerte:
- War das Gespräch logisch strukturiert?
- Gab es einen roten Faden (z.B. Dreischritt-Ansatz: Absicherung → Altersvorsorge → Vermögensaufbau)?
- Wurden Zwischenzusammenfassungen gegeben?
- Gab es eine abschließende Zusammenfassung mit Next Steps?

### 5.4 Kundenorientierung (X/10)

Bewerte:
- Waren die Empfehlungen auf die individuellen Ziele des Kunden abgestimmt?
- Wirkten Produktvorschläge standardisiert oder individuell angepasst?
- Wurde das Budget/die finanzielle Situation des Kunden berücksichtigt?

---

## 6. HAUPTTHEMEN

Liste die Hauptthemen des Gesprächs als Tags auf. Typische Kategorien:
- Berufsunfähigkeitsversicherung (Absicherung)
- Altersvorsorge: Fondssparplan / fondsgebundene Rentenversicherung
- Eigentumswohnung / Immobilie: Bausparvertrag & Eigenkapitalaufbau
- Termine, benötigte Unterlagen und nächste Schritte
- Risikoabsicherung (Haftpflicht, Hausrat, etc.)
- Krankenversicherung
- Sonstige

---

## 7. GESPRÄCHSERGEBNISSE / ECKPUNKTE

Liste alle konkreten Vereinbarungen und Ergebnisse auf:
- Welche Produkte/Maßnahmen wurden vereinbart?
- Mit welchen Beträgen/Konditionen?
- Welche Vergleiche/Angebote werden erstellt?
- Wann ist der Folgetermin?

Format:
- Vereinbarung: [Beschreibung]
- Vereinbarung: [Beschreibung]
- Folgetermin: [Datum/Uhrzeit] – [Zweck]

---

## 8. TO-DOS & VEREINBARUNGEN

### Für Berater:in:

Liste alle Aufgaben, die der/die Berater:in übernimmt:
- Dokumente vorbereiten und versenden
- Vergleiche erstellen
- Angebote ausarbeiten
- Termine koordinieren
- etc.

### Für Kunde:

Liste alle Aufgaben, die der Kunde übernimmt:
- Unterlagen bereitstellen (z.B. Gehaltsabrechnungen, Arbeitsvertrag)
- Informationen prüfen (z.B. Förderfähigkeit)
- Entscheidungen vorbereiten
- etc.

### Termine/Fristen:

- Folgetermin: [Datum, Uhrzeit, Zweck]
- Empfehlungen: z.B. Reminder per E-Mail einen Tag vorher

---

## 9. NÄCHSTE SCHRITTE

Beschreibe chronologisch die nächsten Schritte bis zum Folgetermin:
1. Was macht der Berater als Erstes?
2. Was muss der Kunde vorbereiten?
3. Was passiert beim Folgetermin?

---

## 10. KUNDENZIELE & BEDARFE

Liste die identifizierten Kundenziele:
- Absicherung des Einkommens (Berufsunfähigkeitsschutz)
- Langfristiger Vermögensaufbau / Altersvorsorge mit Renditechancen
- Kurz- bis mittelfristiges Ziel: z.B. Immobilienkauf in X Jahren
- Beibehaltung von Liquidität / monatliche Belastbarkeit
- Sonstige individuelle Ziele

---

## 11. PRODUKTANALYSE

### Angebotene Produkte:

Liste alle im Gespräch vorgestellten Produkte/Lösungen.

### Akzeptierte Produkte:

Liste alle Produkte, denen der Kunde zugestimmt hat, inkl. vereinbarter Beträge.

### Bedenken:

Liste alle vom Kunden geäußerten Bedenken, Fragen oder Einwände:
- Preisbezogene Bedenken
- Verständnisfragen
- Alternative Optionen, die der Kunde erwähnt hat
- Fehlende Exploration von Nachteilen/Alternativen durch den Berater

---

## AUSGABEFORMAT

Strukturiere deine Analyse exakt nach den oben genannten 11 Abschnitten. Verwende:
- Klare Überschriften
- Bewertungen im Format X/10
- Stichpunktartige Aufzählungen für Listen
- Kurze, prägnante Formulierungen

Bei fehlenden Informationen im Transkript: Kennzeichne mit "[Nicht im Gespräch erwähnt]"

---

## WICHTIGE HINWEISE FÜR DIE ANALYSE

1. **Objektivität**: Bewerte fair und konstruktiv. Nenne sowohl Stärken als auch Verbesserungspotenziale.

2. **Konkretheit**: Beziehe dich auf spezifische Aussagen oder Situationen aus dem Gespräch.

3. **Praxisbezug**: Die Analyse soll dem/der Berater:in helfen, sich zu verbessern.

4. **Datenschutz**: Verwende keine echten Namen in der Ausgabe, sondern "Berater:in" und "Kunde".

5. **Branchenkontext**: Berücksichtige Standards der Finanzberatung (z.B. Dokumentationspflichten, Bedarfsanalyse, Geeignetheitsprüfung).

---

TRANSKRIPT DES GESPRÄCHS:

[Fügen Sie hier Ihr Transkript ein]
```

---

# Teil 3: Praxisbeispiele

## Praxisbeispiel 1: Berufseinsteiger – Erstberatung

### Ausgangssituation

Ein 26-jähriger Berufseinsteiger (Software-Entwickler) kommt zur Erstberatung. Er verdient 3.500€ netto, ist ledig und möchte in 3-4 Jahren eine Eigentumswohnung kaufen.

### Beispiel-Transkript (gekürzt)

```
Berater: Guten Tag Herr Müller, schön dass Sie heute Zeit gefunden haben. 
Nehmen Sie doch Platz. Möchten Sie etwas trinken?

Kunde: Danke, ein Wasser wäre super.

Berater: Sehr gerne. Also, Sie haben mir ja am Telefon schon kurz erzählt, 
dass Sie gerade Ihren ersten Job angefangen haben. Erzählen Sie mir doch 
mal ein bisschen mehr über Ihre Situation und was Sie sich von unserem 
Gespräch erhoffen.

Kunde: Ja, also ich bin jetzt seit drei Monaten als Softwareentwickler 
tätig. Verdiene ganz gut, 3.500 Euro netto. Ich wohne noch zur Miete, 
aber mein Ziel ist es, in drei bis vier Jahren eine Eigentumswohnung zu 
kaufen. Meine Eltern haben mir geraten, dass ich mich jetzt mal um 
Versicherungen und so kümmern soll.

Berater: Das ist ein sehr guter Zeitpunkt dafür. Mit 26 und einem 
soliden Einkommen haben Sie wirklich beste Voraussetzungen. Lassen Sie 
mich Ihnen meinen Dreischritt-Ansatz vorstellen, mit dem wir Ihre 
finanzielle Zukunft strukturiert angehen können.

Kunde: Okay, da bin ich gespannt.

Berater: Der erste Schritt ist die Absicherung. Dabei geht es vor allem 
um die Berufsunfähigkeitsversicherung. Stellen Sie sich vor, Sie könnten 
aus gesundheitlichen Gründen nicht mehr arbeiten. Ohne BU-Versicherung 
stehen Sie dann praktisch ohne Einkommen da.

Kunde: Ja, das macht Sinn. Was kostet so eine Versicherung denn?

Berater: Bei Ihrem Alter und Beruf rechne ich mit etwa 60 bis 80 Euro 
pro Monat für eine vernünftige Absicherung. Ich würde Ihnen drei 
verschiedene Tarife zum Vergleich zusammenstellen.

Kunde: Okay, das klingt machbar.

Berater: Der zweite Schritt ist die Altersvorsorge. Ich empfehle Ihnen 
einen Fondssparplan, mit dem Sie langfristig Vermögen aufbauen und von 
den Renditechancen am Kapitalmarkt profitieren können. Wie viel könnten 
Sie sich vorstellen, monatlich zu sparen?

Kunde: Ich denke, 150 Euro wären okay.

Berater: Sehr gut. Und der dritte Schritt betrifft Ihr Ziel, die 
Eigentumswohnung. Hier würde ich einen Bausparvertrag empfehlen. 
Damit bauen Sie gezielt Eigenkapital auf und sichern sich günstige 
Zinsen für später.

Kunde: Wie viel sollte ich da einzahlen?

Berater: Bei Ihrem Ziel von drei bis vier Jahren würde ich 300 Euro 
monatlich empfehlen. Dann hätten Sie in vier Jahren etwa 15.000 Euro 
plus Zinsen und staatliche Förderung.

Kunde: Das klingt gut. Aber das wären ja zusammen fast 500 Euro im 
Monat. Ist das nicht zu viel?

Berater: Ich verstehe Ihre Bedenken. Lassen Sie uns das mal durchrechnen. 
Bei 3.500 Euro netto und angenommenen Fixkosten... Hätten Sie noch 
genug Puffer für den Alltag?

Kunde: Ja, ich denke schon. Ich gebe nicht so viel aus.

Berater: Wunderbar. Dann fasse ich zusammen: Wir beantragen eine 
Berufsunfähigkeitsversicherung, starten einen Fondssparplan mit 150 Euro 
monatlich und einen Bausparvertrag mit 300 Euro monatlich. Ich bereite 
die Unterlagen vor und wir treffen uns nächsten Dienstag um 15 Uhr 
wieder. Bringen Sie bitte Ihre letzten drei Gehaltsabrechnungen und 
eine Kopie Ihres Arbeitsvertrags mit.

Kunde: Alles klar, das mache ich.

Berater: Haben Sie noch Fragen?

Kunde: Nein, ich glaube, ich habe alles verstanden. Vielen Dank!

Berater: Sehr gerne. Dann bis Dienstag!
```

### Beispiel-Analyse der KI

---

## 1. KURZZUSAMMENFASSUNG

Berater stellte einem jungen Berufseinsteiger (26, Softwareentwickler, 3.500€ netto) einen strukturierten Dreischritt-Plan vor: Absicherung durch BU-Versicherung, Altersvorsorge durch Fondssparplan (150€/Monat) und Eigenkapitalaufbau durch Bausparvertrag (300€/Monat) für geplanten Immobilienkauf in 3-4 Jahren. Der Kunde stimmte allen Maßnahmen zu; Folgetermin am Dienstag um 15:00 Uhr vereinbart.

---

## 2. REDEANTEILE

- Berater:in: **72%**
- Kunde: **28%**

Das Verhältnis liegt im akzeptablen Bereich, wobei der Kunde etwas mehr eingebunden werden könnte.

---

## 3. KOMMUNIKATIONSQUALITÄT

### Gesamtbewertung: 8/10

Das Gespräch war klar strukturiert, zielorientiert und führte zu konkreten Vereinbarungen. Der Berater erklärte die Konzepte verständlich und ging auf die Budgetbedenken des Kunden ein. Verbesserungspotenzial besteht bei der tieferen Exploration der persönlichen Situation und Präferenzen des Kunden.

---

## 4. STIMMUNG

**Positiv**

Die Atmosphäre war freundlich und konstruktiv. Der Kunde wirkte interessiert und zufrieden mit den Empfehlungen.

---

## 5. DETAILBEWERTUNGEN

### 5.1 Klarheit & Verständlichkeit: 8/10

Inhalte wurden gut erklärt, der Dreischritt-Ansatz war nachvollziehbar. Fachbegriffe wie "BU-Versicherung" und "Fondssparplan" wurden im Kontext erklärt. Leichte Abzüge: Die genaue Funktionsweise des Bausparvertrags hätte detaillierter erläutert werden können.

### 5.2 Empathie & Beziehung: 7/10

Der Berater begann mit Small Talk und bot Getränke an. Er lobte den Kunden für den guten Zeitpunkt und ging auf die Budgetbedenken ein. Allerdings wurden keine tiefergehenden Fragen zu persönlichen Ängsten, Risikotoleranz oder Lebensplänen gestellt.

### 5.3 Struktur & Gesprächsführung: 9/10

Sehr gute Struktur durch den klar kommunizierten Dreischritt-Ansatz. Logischer Aufbau von Absicherung über Altersvorsorge zu Vermögensaufbau. Abschließende Zusammenfassung mit Next Steps vorhanden.

### 5.4 Kundenorientierung: 8/10

Die Empfehlungen waren auf die Ziele des Kunden (Eigentumswohnung) abgestimmt. Die Beträge wurden an das Budget angepasst. Leichter Abzug: Alternative Produkte (z.B. ETF-Sparplan statt klassischer Fondssparplan) wurden nicht diskutiert.

---

## 6. HAUPTTHEMEN

- Berufsunfähigkeitsversicherung (Absicherung)
- Altersvorsorge: Fondssparplan
- Eigentumswohnung: Bausparvertrag & Eigenkapitalaufbau
- Termine, benötigte Unterlagen und nächste Schritte

---

## 7. GESPRÄCHSERGEBNISSE / ECKPUNKTE

- Vereinbarung: Berufsunfähigkeitsversicherung soll beantragt werden; Tarifvergleich mit 3 Optionen wird erstellt
- Vereinbarung: Fondssparplan über 150€ monatlich starten; Depot wird eingerichtet
- Vereinbarung: Bausparvertrag mit 300€ monatlich zur Eigenkapitalbildung
- Folgetermin: Dienstag 15:00 Uhr zur Antragsstellung und Abschlussvorbereitung

---

## 8. TO-DOS & VEREINBARUNGEN

### Für Berater:in:
- Vergleich von drei BU-Tarifen erstellen
- Depot-Eröffnungsunterlagen vorbereiten
- Fondssparplan mit Asset-Allokation ausarbeiten
- Bausparvertrag-Angebot mit Konditionen erstellen
- Termin am Dienstag 15:00 Uhr vorbereiten

### Für Kunde:
- Letzte drei Gehaltsabrechnungen bereitstellen
- Kopie des Arbeitsvertrags mitbringen

### Termine/Fristen:
- Folgetermin: Dienstag um 15:00 Uhr (Abschlussvorbereitung)

---

## 9. NÄCHSTE SCHRITTE

1. Berater erstellt BU-Tarifvergleich, Depot-Unterlagen und Bausparvertrag-Angebot
2. Kunde sammelt Gehaltsabrechnungen und Arbeitsvertrag
3. Am Dienstag: Gemeinsame Durchsicht der Angebote, Auswahl der Tarife und Antragsstellung

---

## 10. KUNDENZIELE & BEDARFE

- Absicherung des Einkommens (Berufsunfähigkeitsschutz)
- Langfristiger Vermögensaufbau / Altersvorsorge mit Renditechancen
- Kurz- bis mittelfristiges Ziel: Kauf einer Eigentumswohnung in 3-4 Jahren
- Beibehaltung von Liquidität / monatliche Belastbarkeit (ca. 500€ Gesamtinvestition im Budget)

---

## 11. PRODUKTANALYSE

### Angebotene Produkte:
- Berufsunfähigkeitsversicherung (geschätzt 60-80€/Monat)
- Fondssparplan für Altersvorsorge
- Bausparvertrag für Eigenkapitalaufbau

### Akzeptierte Produkte:
- BU-Versicherung: Zustimmung zur Beantragung (Tarifauswahl beim Folgetermin)
- Fondssparplan: 150€/Monat
- Bausparvertrag: 300€/Monat

### Bedenken:
- Kunde äußerte Bedenken zur Gesamtbelastung von fast 500€/Monat → wurde vom Berater durch Budgetrechnung adressiert
- Keine weiteren Bedenken geäußert
- Nicht exploriert: Alternative Anlageformen, Vor-/Nachteile der empfohlenen Produkte, Risikotoleranz des Kunden

---

---

## Praxisbeispiel 2: Schwieriges Gespräch – Skeptischer Kunde

### Ausgangssituation

Eine 35-jährige Kundin (Lehrerin, verbeamtet) kommt auf Empfehlung einer Freundin. Sie ist skeptisch gegenüber Finanzberatern und hat bereits schlechte Erfahrungen gemacht.

### Beispiel-Transkript (gekürzt)

```
Berater: Guten Tag Frau Schmidt, willkommen bei uns. Schön, dass Sie 
den Weg zu uns gefunden haben.

Kundin: Ja, meine Freundin hat Sie empfohlen. Aber ich sage Ihnen 
gleich: Ich bin da sehr vorsichtig. Ich hatte schon mal einen Berater, 
der mir Produkte aufgeschwatzt hat, die überhaupt nicht zu mir passten.

Berater: Das kann ich absolut verstehen. Schlechte Erfahrungen prägen 
natürlich. Darf ich fragen, was damals genau passiert ist?

Kundin: Der hat mir eine fondsgebundene Lebensversicherung verkauft. 
Mit hohen Kosten und schlechter Performance. Ich habe viel Geld verloren.

Berater: Das tut mir leid zu hören. Solche Produkte waren früher leider 
weit verbreitet und oft nicht im besten Interesse der Kunden. Ich möchte 
Ihnen heute einen anderen Ansatz zeigen. Wir schauen erst mal, was Sie 
wirklich brauchen, und dann finden wir passende Lösungen. Einverstanden?

Kundin: Na gut, ich höre mir das mal an.

Berater: Prima. Erzählen Sie mir doch erstmal von Ihrer Situation. 
Sie sind Lehrerin, richtig?

Kundin: Ja, verbeamtet seit fünf Jahren. Ich verdiene etwa 3.800 Euro 
netto. Verheiratet, ein Kind.

Berater: Und was sind Ihre finanziellen Ziele oder Sorgen?

Kundin: Eigentlich geht es mir ganz gut. Aber ich mache mir Sorgen um 
die Altersvorsorge. Als Beamtin kriege ich ja Pension, aber ob das reicht?

Berater: Eine berechtigte Sorge. Lassen Sie mich Ihnen die Zahlen zeigen. 
Die Beamtenpension liegt bei etwa 71% der letzten Bezüge. Das ist mehr 
als die gesetzliche Rente, aber eine Lücke bleibt trotzdem.

Kundin: Und wie soll ich die schließen? Aber bitte keine teuren 
Versicherungsprodukte!

Berater: Verstanden. Ich würde Ihnen einen einfachen ETF-Sparplan 
empfehlen. Niedrige Kosten, transparent, gute langfristige Rendite. 
Keine Versicherungskonstruktion.

Kundin: ETFs... davon habe ich schon gehört. Ist das nicht riskant?

Berater: Es gibt Schwankungen, ja. Aber bei einem Anlagehorizont von 
30 Jahren bis zur Pension ist das Risiko sehr gut beherrschbar. Ich 
zeige Ihnen mal eine Grafik...

[Erklärung folgt]

Kundin: Das klingt schon besser als das, was ich bisher kannte.

Berater: Wie viel könnten Sie sich vorstellen, monatlich zu investieren?

Kundin: Ich weiß nicht... vielleicht 200 Euro?

Berater: Das ist ein guter Betrag. Damit können wir arbeiten. Soll ich 
Ihnen einen konkreten Vorschlag zusammenstellen?

Kundin: Ja, aber ich möchte mir das in Ruhe anschauen, bevor ich 
unterschreibe.

Berater: Selbstverständlich. Ich schicke Ihnen den Vorschlag per E-Mail, 
und Sie können sich alles in Ruhe durchlesen. Wenn Sie dann noch Fragen 
haben, besprechen wir die beim nächsten Termin. Kein Druck.

Kundin: Das finde ich gut. So machen wir das.

Berater: Haben Sie noch andere Themen, die Sie beschäftigen?

Kundin: Naja, mein Mann und ich überlegen, ob wir noch ein zweites 
Kind bekommen. Da frage ich mich, ob wir dann noch genug Geld haben.

Berater: Das ist ein wichtiger Punkt. Wollen wir das heute noch 
besprechen oder beim nächsten Termin?

Kundin: Lieber beim nächsten Mal. Das ist mir heute zu viel.

Berater: Absolut verständlich. Dann machen wir für heute Schluss. 
Ich schicke Ihnen den ETF-Vorschlag, und wir sehen uns in zwei Wochen?

Kundin: Ja, das passt.

Berater: Wunderbar. Vielen Dank für Ihr Vertrauen, Frau Schmidt.

Kundin: Danke, das Gespräch war wirklich anders als erwartet. Im 
positiven Sinne.
```

### Beispiel-Analyse der KI

---

## 1. KURZZUSAMMENFASSUNG

Berater führte ein Erstgespräch mit einer skeptischen, verbeamteten Lehrerin (35), die aufgrund negativer Vorerfahrungen mit Finanzberatern zunächst zurückhaltend war. Durch empathischen Umgang und transparente Kommunikation konnte Vertrauen aufgebaut werden. Die Kundin stimmte zu, einen ETF-Sparplan-Vorschlag (200€/Monat) für die Altersvorsorge zu prüfen. Das Thema Familienplanung wird im Folgetermin in zwei Wochen besprochen.

---

## 2. REDEANTEILE

- Berater:in: **58%**
- Kunde: **42%**

Sehr ausgewogenes Verhältnis. Der Berater hat der Kundin viel Raum gegeben, was angesichts ihrer Skepsis genau richtig war.

---

## 3. KOMMUNIKATIONSQUALITÄT

### Gesamtbewertung: 9/10

Hervorragende Gesprächsführung in einer schwierigen Ausgangssituation. Der Berater hat die Bedenken der Kundin ernst genommen, keine aggressiven Verkaufstaktiken angewendet und durch Transparenz Vertrauen aufgebaut. Das positive Feedback der Kundin am Ende bestätigt den Erfolg.

---

## 4. STIMMUNG

**Positiv**

Entwicklung von anfänglicher Skepsis zu Vertrauen und Zufriedenheit. Die Kundin äußerte explizit, dass das Gespräch "anders als erwartet" und positiv war.

---

## 5. DETAILBEWERTUNGEN

### 5.1 Klarheit & Verständlichkeit: 9/10

Komplexe Themen wie Beamtenpension und ETFs wurden verständlich erklärt. Der Berater verwendete konkrete Zahlen (71% Pensionsniveau) und bot visuelle Unterstützung (Grafik). Die Kundin konnte folgen und stellte gezielte Nachfragen.

### 5.2 Empathie & Beziehung: 10/10

Ausgezeichnet. Der Berater hat sofort auf die negative Vorerfahrung reagiert, Verständnis gezeigt und nachgefragt. Er hat Druck vermieden, der Kundin Bedenkzeit eingeräumt und ihre Grenzen respektiert ("Das ist mir heute zu viel").

### 5.3 Struktur & Gesprächsführung: 8/10

Gute Struktur, auch wenn sie flexibel an die Situation angepasst wurde. Der Berater hat sich auf die Hauptsorge (Altersvorsorge) konzentriert und weitere Themen bewusst vertagt. Leichter Abzug: Ein systematischerer Überblick über mögliche weitere Bedarfe hätte angeboten werden können.

### 5.4 Kundenorientierung: 10/10

Der Berater hat auf den expliziten Wunsch der Kundin (keine teuren Versicherungsprodukte) gehört und eine passende, kostengünstige Alternative vorgeschlagen. Er hat keinen Druck ausgeübt und die Kundin zur Bedenkzeit ermutigt.

---

## 6. HAUPTTHEMEN

- Altersvorsorge: ETF-Sparplan
- Vertrauensaufbau / Umgang mit negativen Vorerfahrungen
- Familienplanung (vertagt auf Folgetermin)
- Termine und nächste Schritte

---

## 7. GESPRÄCHSERGEBNISSE / ECKPUNKTE

- Vereinbarung: ETF-Sparplan-Vorschlag wird per E-Mail zugesandt
- Vereinbarung: Sparrate ca. 200€/Monat angedacht
- Vereinbarung: Thema Familienplanung/Finanzen beim nächsten Termin
- Folgetermin: In zwei Wochen

---

## 8. TO-DOS & VEREINBARUNGEN

### Für Berater:in:
- ETF-Sparplan-Vorschlag erstellen und per E-Mail senden
- Vorschlag mit konkreten Produkten, Kosten und erwarteter Entwicklung
- Termin in zwei Wochen vorbereiten inkl. Thema Familienplanung

### Für Kunde:
- ETF-Vorschlag in Ruhe durchlesen
- Fragen notieren für Folgetermin
- Über Familienplanung und finanzielle Auswirkungen nachdenken

### Termine/Fristen:
- Folgetermin: In zwei Wochen (genaues Datum nicht genannt)

---

## 9. NÄCHSTE SCHRITTE

1. Berater erstellt individuellen ETF-Sparplan-Vorschlag mit Kostenaufstellung
2. Berater sendet Vorschlag per E-Mail
3. Kundin prüft den Vorschlag in Ruhe zu Hause
4. Beim Folgetermin: Besprechung des Vorschlags, Klärung von Fragen, ggf. Abschluss, plus Gespräch über Familienplanung

---

## 10. KUNDENZIELE & BEDARFE

- Langfristiger Vermögensaufbau / Altersvorsorge (Schließung der Pensionslücke)
- Transparenz und Vertrauen (aufgrund negativer Vorerfahrung)
- Familienplanung: Finanzielle Absicherung bei möglichem zweiten Kind
- Kostenbewusstsein: Keine teuren Versicherungskonstruktionen gewünscht

---

## 11. PRODUKTANALYSE

### Angebotene Produkte:
- ETF-Sparplan für Altersvorsorge (ca. 200€/Monat)

### Akzeptierte Produkte:
- ETF-Sparplan: Kundin möchte Vorschlag prüfen (noch keine finale Zusage)

### Bedenken:
- Generelle Skepsis gegenüber Finanzberatern aufgrund schlechter Vorerfahrung → erfolgreich adressiert
- Frage nach Risiko von ETFs → durch Erklärung (Anlagehorizont 30 Jahre) beantwortet
- Wunsch nach Bedenkzeit → respektiert und eingeplant
- Noch nicht besprochen: Konkrete Kosten des ETF-Sparplans, steuerliche Aspekte, Ehepartner in Entscheidung einbeziehen

---

---

# Teil 4: Anhang

## Checkliste für die Nutzung

- [ ] Audio-Aufnahme mit guter Qualität erstellen
- [ ] Einwilligung aller Beteiligten einholen
- [ ] Transkription erstellen und prüfen
- [ ] Sprecher im Transkript kennzeichnen
- [ ] Prompt und Transkript in KI-Tool eingeben
- [ ] Analyse prüfen und bei Bedarf nachfragen
- [ ] Ergebnisse dokumentieren und für Coaching nutzen
- [ ] Sensible Daten nach Nutzung löschen

## Glossar

| Begriff | Erklärung |
|---------|-----------|
| **Transkript** | Verschriftlichung einer Audio- oder Videoaufnahme |
| **Prompt** | Anweisung oder Eingabe an eine KI |
| **BU-Versicherung** | Berufsunfähigkeitsversicherung |
| **ETF** | Exchange Traded Fund (börsengehandelter Indexfonds) |
| **Fondssparplan** | Regelmäßiges Sparen in Investmentfonds |
| **Bausparvertrag** | Sparvertrag mit Option auf zinsgünstiges Darlehen |

## Weiterführende Ressourcen

- [Anthropic Claude](https://claude.ai) – KI-Assistent für Analysen
- [OpenAI Whisper](https://github.com/openai/whisper) – Kostenloses Transkriptionstool
- [BaFin-Richtlinien](https://www.bafin.de) – Regulatorische Anforderungen für Finanzberatung

---

*Erstellt für die Nutzung in der Qualitätssicherung und im Coaching von Finanzberater:innen.*
