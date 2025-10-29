# InfraNodus MCP Server - Komplette Anleitung mit 5 Praxisbeispielen für Marketing & HR

---

## **Teil 1: Was ist das und warum brauchen Sie es?**

### **Die Situation heute:**
Sie haben stapelweise Texte auf Ihrem Schreibtisch:
- 500 Mitarbeiterkommentare zur Unternehmenskultur
- 1.000 Kundenbewertungen auf verschiedenen Plattformen
- Dutzende Stellenanzeigen, die unterschiedlich gut performen
- Konkurrenz-Websites, die Sie analysieren müssen

**Problem:** Das manuelle Durcharbeiten dauert Tage, und Sie könnten wichtige Muster übersehen.

### **Die Lösung: InfraNodus + MCP Server**

InfraNodus wandelt jeden Text automatisch in einen Wissensgraphen um - eine visuelle Karte, die zeigt, welche Themen vorkommen, wie sie zusammenhängen und wo Lücken sind.

Der MCP Server verbindet dieses Tool mit Claude, sodass Sie in normalem Deutsch Fragen stellen können und Claude automatisch die Analyse durchführt.

**Einfach gesagt:** Sie sprechen mit Claude wie mit einem Kollegen, und Claude nutzt im Hintergrund ein Profi-Analysetool.

---

## **Teil 2: Technische Einrichtung (einmalig ca. 30 Minuten)**

### **Schritt 1: InfraNodus-Account erstellen**
1. Gehen Sie zu https://infranodus.com
2. Klicken Sie auf "Sign Up" und nutzen Sie die 14-tägige kostenlose Testphase
3. Notieren Sie sich Ihren API-Schlüssel (zu finden unter: Ihr Profil → API Access)

### **Schritt 2: MCP Server in Claude Desktop installieren**

**Für Windows:**
1. Öffnen Sie Claude Desktop
2. Gehen Sie zu: Einstellungen → Entwickler → Konfiguration bearbeiten
3. Fügen Sie folgenden Code ein:

```json
{
  "mcpServers": {
    "infranodus": {
      "command": "npx",
      "args": [
        "-y",
        "@smithery/cli@latest",
        "run",
        "@infranodus/mcp-server-infranodus"
      ]
    }
  }
}
```

4. Speichern und Claude Desktop neu starten
5. Sie sehen jetzt ein kleines Hammer-Symbol 🔨 - das zeigt, dass InfraNodus-Tools verfügbar sind

**Für Mac:** 
Gleicher Ablauf, die Konfigurationsdatei liegt unter:
`~/Library/Application Support/Claude/claude_desktop_config.json`

### **Schritt 3: Testen Sie die Installation**
Schreiben Sie in Claude Desktop:
```
"Hallo! Kannst du prüfen, ob InfraNodus verfügbar ist?"
```

Claude sollte antworten, dass die InfraNodus-Tools bereit sind.

---

## **Teil 3: Die 5 Praxisbeispiele für Ihren TK-Alltag**

---

## **PRAXISBEISPIEL 1: Mitarbeiterbefragung analysieren (HR)**

### **Ihr Szenario:**
Sie haben gerade die jährliche Mitarbeiterbefragung durchgeführt. 450 Mitarbeiter haben auf die Frage geantwortet: *"Was sollte die TK als Arbeitgeber verbessern?"*

### **Ohne InfraNodus:**
- 3-4 Tage manuelle Durchsicht
- Excel-Tabellen mit Kategorien
- Risiko, wichtige Themen zu übersehen

### **Mit InfraNodus MCP Server:**

**Schritt-für-Schritt:**

1. **Daten vorbereiten:** Kopieren Sie alle Antworten in eine Textdatei (z.B. `mitarbeiterbefragung_2025.txt`)

2. **In Claude hochladen:** Ziehen Sie die Datei in den Chat

3. **Analyseanfrage stellen:**
```
"Analysiere diese Mitarbeiterbefragung mit InfraNodus:
1. Welche sind die 5 Hauptthemen?
2. Welche Themenlücken gibt es (also Bereiche, die miteinander verbunden werden sollten)?
3. Erstelle eine Prioritätenliste für HR-Maßnahmen"
```

4. **Claude erstellt automatisch:**
   - Einen Wissensgraphen mit allen Themen
   - Cluster-Analyse (z.B. "Work-Life-Balance", "Entwicklung", "Kommunikation")
   - Lückenanalyse: Welche Themen werden oft genannt, aber nie zusammen erwähnt?

**Beispiel-Ergebnis:**
```
Hauptthemen gefunden:
1. Homeoffice-Regelung (45% der Nennungen)
2. Weiterbildung (32%)
3. Gehalt & Benefits (28%)
4. Führungskultur (22%)
5. Team-Events (18%)

KRITISCHE LÜCKE erkannt:
"Weiterbildung" und "Karriereentwicklung" werden oft einzeln genannt,
aber nie zusammen - hier fehlt ein strukturiertes Entwicklungsprogramm!

Empfehlung: Entwickeln Sie ein ganzheitliches Karriereprogramm,
das beide Aspekte verbindet.
```

**Zeitersparnis:** Von 4 Tagen auf 20 Minuten!

---

## **PRAXISBEISPIEL 2: Social Media Kampagnen-Analyse (Marketing)**

### **Ihr Szenario:**
Die TK hat im letzten Quartal 3 verschiedene Instagram-Kampagnen gefahren:
- "Fit ins Frühjahr" (Fitness-App)
- "Mental Health Matters" (Stressmanagement)
- "Familie & Vorsorge" (Kinderversicherung)

Sie haben 800 Kommentare gesammelt und möchten verstehen, welche Themen bei Ihrer Zielgruppe wirklich ankommen.

### **Schritt-für-Schritt:**

1. **Daten sammeln:** Exportieren Sie alle Kommentare in eine CSV-Datei

2. **Claude-Anfrage:**
```
"Analysiere diese Social-Media-Kommentare mit InfraNodus:
1. Welche Kampagne erzeugte die positivste Resonanz?
2. Welche Themen werden in Kommentaren erwähnt, die wir NICHT in der Kampagne hatten?
3. Welche Content-Ideen sollten wir für das nächste Quartal entwickeln?"
```

3. **Claude erstellt:**
   - Themenclusters für jede Kampagne
   - Sentiment-Analyse (positiv/negativ)
   - Strukturelle Lücken: Themen, die Nutzer ansprechen, die aber in Ihrem Content fehlen

**Beispiel-Ergebnis:**
```
Analyse der 800 Kommentare:

ÜBERRASCHUNG: Die meisten positiven Kommentare erwähnen "Prävention"
und "Bonus-Programm" - beides war NICHT Hauptthema der Kampagnen!

Top-Lücken für neue Content-Ideen:
1. "Prävention + Alltag" - Nutzer wollen praktische Tipps für den Alltag
2. "Familie + Digitale Tools" - Eltern suchen Apps für Kindergesundheit
3. "Mental Health + Arbeit" - Thema Work-Life-Balance fehlt komplett

EMPFEHLUNG: Starten Sie eine Serie "5-Minuten-Gesundheit im Büro"
```

**Nutzen:** Sie erkennen sofort, welcher Content wirklich resoniert - nicht was Sie DENKEN, sondern was Ihre Zielgruppe WIRKLICH will.

---

## **PRAXISBEISPIEL 3: Stellenanzeigen-Optimierung (HR)**

### **Ihr Szenario:**
Die TK schaltet monatlich 15-20 Stellenanzeigen. Manche bekommen 200 Bewerbungen, andere nur 10. Sie wollen verstehen: Was macht den Unterschied?

### **Schritt-für-Schritt:**

1. **Daten vorbereiten:**
   - Erstellen Sie 2 Dateien:
     - `top_performer_anzeigen.txt` (die 5 erfolgreichsten Anzeigen)
     - `low_performer_anzeigen.txt` (die 5 schwächsten Anzeigen)

2. **Zusätzlich:** Suchen Sie auf Google nach "Jobs Krankenkasse Hamburg" und kopieren Sie die ersten 10 Ergebnisse

3. **Claude-Anfrage:**
```
"Analysiere mit InfraNodus meine Stellenanzeigen:

Aufgabe 1: Vergleiche top_performer mit low_performer.
Welche Keywords und Themen kommen nur in erfolgreichen Anzeigen vor?

Aufgabe 2: Vergleiche meine Anzeigen mit dem, was Kandidaten
bei Google finden. Welche Begriffe fehlen in meinen Anzeigen?"
```

4. **Claude analysiert:**
   - Text-Vergleich: Welche Begriffe sind in erfolgreichen Anzeigen, aber nicht in schwachen?
   - Keyword-Gap zur Konkurrenz
   - Strukturelle Empfehlungen

**Beispiel-Ergebnis:**
```
KRITISCHE UNTERSCHIEDE gefunden:

Top-Performer verwenden:
✓ "Flexibles Arbeiten" (100% der Top-Anzeigen)
✓ "Weiterbildungsbudget" (80%)
✓ "30 Tage Urlaub" (100%)
✓ Konkrete Zahlen zum Gehalt (60%)

Low-Performer haben stattdessen:
✗ Vage Formulierungen ("attraktive Konditionen")
✗ Fokus auf "Herausforderungen" statt Benefits
✗ Lange Aufzählungen von Anforderungen

FEHLT KOMPLETT in Ihren Anzeigen (aber Kandidaten suchen danach):
- "Remote Work"
- "4-Tage-Woche"
- "Teilzeit-Optionen"
- "Einstieg ohne Erfahrung"

SOFORT-MASSNAHME:
Fügen Sie in alle Anzeigen einen Benefits-Block am Anfang ein
mit konkreten Zahlen (30 Tage Urlaub, 2.000€ Weiterbildung/Jahr etc.)
```

**Zeitersparnis:** Statt wochenlanges Trial-and-Error haben Sie datenbasierte Erkenntnisse in 30 Minuten.

---

## **PRAXISBEISPIEL 4: Content-Gap-Analyse für TK-Blog (Marketing)**

### **Ihr Szenario:**
Der TK-Blog hat 50 Artikel, aber die Traffic-Zahlen sind enttäuschend. Sie wollen herausfinden: Welche Themen fehlen, die Ihre Zielgruppe sucht?

### **Schritt-für-Schritt:**

1. **Ihre Content-Inventur:**
   - Exportieren Sie alle Blog-Titel und Zusammenfassungen in `tk_blog_content.txt`

2. **Recherche-Kombo:**
```
"Bitte führe folgende Analyse durch:

Schritt 1: Analysiere tk_blog_content.txt mit InfraNodus
und zeige mir die Themen-Cluster.

Schritt 2: Suche im Web nach den Top 10 Google-Ergebnissen für:
- 'Krankenkasse wechseln'
- 'Gesundheitsvorsorge Familie'
- 'Private vs. gesetzliche Krankenversicherung'

Schritt 3: Vergleiche mit InfraNodus:
Welche Themen sind in Google-Ergebnissen stark,
aber fehlen in unserem Blog komplett?"
```

3. **Claude macht automatisch:**
   - Analyse Ihrer bestehenden Inhalte
   - Web-Recherche zu relevanten Suchbegriffen
   - Content-Gap-Analyse: Was wird gesucht vs. was Sie anbieten

**Beispiel-Ergebnis:**
```
IHRE CONTENT-CLUSTER (was Sie HABEN):
1. Gesundheitstipps (35% des Contents)
2. Leistungen der TK (28%)
3. Digital-Services (22%)
4. Fitness & Sport (15%)

GOOGLE TOP-THEMEN (was Nutzer SUCHEN):
1. Kosten-Vergleiche (sehr stark)
2. Kassenwechsel-Prozess (sehr stark)
3. Familien-Tarife (stark)
4. Zahnarzt-Leistungen (stark)
5. Auslandskrankenversicherung (mittel)

MASSIVE CONTENT-LÜCKEN:
⚠️ Sie haben KEINEN Content zu "Kassenwechsel" - das ist aber
   eine der meistgesuchten Fragen!
⚠️ "Kosten-Vergleich" fehlt komplett - hier verlieren Sie Interessenten
⚠️ "Zahnersatz Kosten" wird oft gesucht, Sie haben nur 1 alten Artikel

CONTENT-PLAN für Q2 2025:
1. Serie: "Kassenwechsel leicht gemacht" (3 Artikel)
2. Interaktiver Kosten-Rechner (Landing Page)
3. Familien-Guide: "Welche Leistungen brauchen Eltern?" (1 Artikel)
4. Aktualisierung: Zahnarzt-Leistungen (1 Artikel)
```

**ROI:** Durch gezielten Content in Lücken-Bereichen können Sie Ihre Sichtbarkeit deutlich steigern.

---

## **PRAXISBEISPIEL 5: Multichannel-Kundenfeedback vereinen (Marketing + HR)**

### **Ihr Szenario:**
Die TK bekommt Feedback aus vielen Kanälen:
- E-Mail-Beschwerden (Kundenservice)
- Google-Bewertungen
- Trustpilot
- Social Media Kommentare
- App-Store-Reviews

Sie wollen alle Kanäle zusammen analysieren, um die wichtigsten Verbesserungspotenziale zu finden.

### **Schritt-für-Schritt:**

1. **Daten konsolidieren:**
   - Erstellen Sie 5 separate Textdateien (eine pro Kanal)
   - Jede Datei enthält Feedback aus dem letzten Quartal

2. **Multi-Datei-Analyse:**
```
"Ich lade jetzt 5 Dateien hoch mit Kundenfeedback aus verschiedenen Kanälen.

Bitte analysiere mit InfraNodus:
1. Welche Themen tauchen in ALLEN Kanälen auf? (= dringendste Probleme)
2. Welche Themen sind kanal-spezifisch?
3. Gibt es positive Themen, die wir mehr hervorheben sollten?
4. Erstelle einen Aktionsplan nach Priorität"
```

3. **Claude erstellt:**
   - Übergreifende Themenanalyse aller Kanäle
   - Sentiment-Verteilung
   - Prioritäten-Matrix

**Beispiel-Ergebnis:**
```
ANALYSE VON 2.350 FEEDBACKS AUS 5 KANÄLEN:

KRITISCH (in allen Kanälen negativ erwähnt):
🔴 Wartezeit Hotline (487 Erwähnungen)
🔴 App-Stabilität (312 Erwähnungen)
🔴 Erstattungsdauer (289 Erwähnungen)

KANAL-SPEZIFISCHE THEMEN:
📧 E-Mail: Komplizierte Formulare (nur hier ein Problem)
📱 App-Store: Login-Probleme (nur hier erwähnt)
⭐ Google: Geschäftsstellen-Öffnungszeiten (lokal relevant)

POSITIVE ÜBERRASCHUNG (wenig bekannt, aber sehr geschätzt):
✅ Bonusprogramm (234 positive Erwähnungen)
✅ Kostenübernahme für Zusatzleistungen (198 positive)
✅ Freundliches Personal (445 positive)

QUICK WINS für Marketing:
→ Bonusprogramm VIEL mehr bewerben (ist beliebt, aber unbekannt)
→ Erstattungsgeschwindigkeit kommunizieren ("Meist in 3 Tagen")
→ Case Studies mit zufriedenen Kunden (Personal-Freundlichkeit)

KRITISCHE HANDLUNGSFELDER für HR/Operations:
→ Hotline-Kapazität ausbauen (höchste Priorität)
→ App-Entwickler-Team verstärken
→ Formular-Prozess digitalisieren und vereinfachen
```

**Mehrwert:** Sie erhalten eine ganzheitliche Sicht statt isolierter Kanal-Silos und können Ressourcen gezielt einsetzen.

---

## **Teil 4: Best Practices für den Alltag**

### **1. Regelmäßige Analyse-Routinen einrichten**
- **Wöchentlich:** Social Media Kommentare
- **Monatlich:** Stellenanzeigen-Performance
- **Quartalsweise:** Große Feedback-Analysen

### **2. Datenqualität sicherstellen**
- Entfernen Sie personenbezogene Daten vor der Analyse
- Nutzen Sie den `doNotSave`-Parameter, damit Daten nicht gespeichert werden
- Besonders wichtig bei Versichertendaten!

### **3. Team-Schulung**
- Starten Sie mit einem Workshop (2 Stunden)
- Jeder probiert 1-2 Beispiele selbst aus
- Erstellen Sie ein internes Wiki mit Ihren TK-spezifischen Beispielen

### **4. Kosten-Management**
Für die TK empfehle ich:
- Start mit 2-3 Advanced-Lizenzen (32€/Monat) für Power-User
- Bei breiterer Nutzung: Enterprise-Version mit EU-Server (4.900€/Jahr + Setup) für DSGVO-Konformität

---

## **Teil 5: Troubleshooting & Häufige Fragen**

**F: "Claude sagt, InfraNodus ist nicht verfügbar"**
- Prüfen Sie, ob Claude Desktop neu gestartet wurde
- Kontrollieren Sie die Konfigurationsdatei (Schritt 2)
- Schauen Sie nach dem 🔨-Symbol in Claude

**F: "Die Analyse dauert sehr lange"**
- Große Dateien (>100 Seiten) können 2-3 Minuten brauchen
- Das ist normal - deutlich schneller als manuell!

**F: "Kann ich das auch mit Versichertendaten machen?"**
- Ja, aber: Nutzen Sie den `doNotSave`-Parameter
- Für Produktivbetrieb: Enterprise-Version mit EU-Server
- Anonymisieren Sie Daten vorher

**F: "Brauche ich Programmierkenntnisse?"**
- Nein! Sie sprechen einfach mit Claude in Deutsch
- Claude übernimmt die technische Kommunikation mit InfraNodus

---

## **Teil 6: Ihre ersten Schritte (Start heute!)**

**Woche 1: Setup & Kennenlernen**
- Tag 1: Installation (30 Min)
- Tag 2-3: Praxisbeispiel 1 ausprobieren
- Tag 4-5: Eigenes kleines Projekt

**Woche 2-3: Erste echte Projekte**
- Wählen Sie 1-2 der Praxisbeispiele
- Nutzen Sie echte TK-Daten (anonymisiert)
- Dokumentieren Sie Ihre Erkenntnisse

**Ab Woche 4: Rollout im Team**
- Präsentieren Sie Ihre Ergebnisse
- Schulen Sie 2-3 Kollegen
- Etablieren Sie Analyse-Routinen

---

## **Zusammenfassung: Warum sich das lohnt**

**Zeitersparnis:**
- Mitarbeiterbefragung: Von 4 Tagen auf 20 Minuten
- Social Media Analyse: Von 2 Tagen auf 30 Minuten
- Content-Gap-Analyse: Von 1 Woche auf 1 Stunde

**Bessere Entscheidungen:**
- Datenbasiert statt Bauchgefühl
- Objektive Muster erkennen
- Lücken entdecken, die manuell übersehen würden

**ROI für die TK:**
- Effizientere Recruiting-Prozesse
- Zielgenauere Marketing-Kampagnen
- Höhere Mitarbeiterzufriedenheit durch gezielte Maßnahmen

---


