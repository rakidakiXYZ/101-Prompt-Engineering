# 🤖 KI-Protokolle & Claude Skills 

**Verständnisleitfaden für Marketing & HR**  
*Ohne Technik-Kauderwelsch – Mit echten Praxisbeispielen*

---

## 📖 Worum geht es hier?

Diese Anleitung erklärt Ihnen:
- Was **MCP, ACP und A2A** wirklich sind
- Was **Claude Skills** sind und wie sie sich unterscheiden
- **Konkrete Beispiele** aus Ihrem TK-Arbeitsalltag
- **Keine** Installationsanleitungen (das macht Ihre IT)

**Ziel:** Sie verstehen, was möglich ist und können entscheiden, was für Ihre Arbeit nützlich wäre.

---

## 🎯 Die Basics: Was sind Protokolle?

### Die Telefon-Analogie

Stellen Sie sich vor, Sie wollen mit jemandem sprechen:

```
┌─────────────────────────────────────────────────────────┐
│  Ohne gemeinsames "Protokoll" (Sprache):                │
│                                                         │
│  Sie (Deutsch) ──X──> Kollege (Japanisch)              │
│  → Kommunikation funktioniert nicht                    │
└─────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────┐
│  Mit gemeinsames "Protokoll" (Sprache):                 │
│                                                         │
│  Sie (Deutsch) ──✓──> Kollege (Deutsch)                │
│  → Kommunikation funktioniert                          │
└─────────────────────────────────────────────────────────┘
```

**Ein Protokoll** = Eine Vereinbarung, wie zwei Systeme miteinander sprechen

---

## 🤖 MCP: Model Context Protocol

### Was ist MCP in einem Satz?

**MCP gibt Claude Zugriff auf Daten und Werkzeuge außerhalb des Chat-Fensters.**

### Die Büro-Analogie

Stellen Sie sich Claude als neuen Praktikanten vor:

#### OHNE MCP (Standard-Claude)

```
┌────────────────────────────────────────────────────────┐
│  Claude sitzt in einem leeren Büro                     │
│                                                        │
│  ❌ Kein Zugang zum Aktenschrank                       │
│  ❌ Kein Zugang zum Computer-Netzwerk                  │
│  ❌ Keine Telefon-Durchwahl                            │
│  ❌ Keine E-Mail-Adresse                               │
│                                                        │
│  → Sie müssen Claude alles physisch vorbeibringen     │
└────────────────────────────────────────────────────────┘
```

**Ihr Arbeitsablauf:**
1. Sie öffnen die Datenbank
2. Sie kopieren Daten
3. Sie fügen sie in Claude ein
4. Claude analysiert
5. Sie kopieren das Ergebnis zurück

⏱️ **Zeit:** 10-15 Minuten pro Aufgabe

---

#### MIT MCP (Erweiterter Claude)

```
┌────────────────────────────────────────────────────────┐
│  Claude hat volle Büro-Ausstattung                     │
│                                                        │
│  ✅ Zugang zum Aktenschrank (Datenbanken)              │
│  ✅ Zugang zum Netzwerk (SharePoint/Drive)             │
│  ✅ Telefon-Durchwahl (APIs)                           │
│  ✅ E-Mail-Adresse (E-Mail-System)                     │
│                                                        │
│  → Claude holt sich selbst, was gebraucht wird        │
└────────────────────────────────────────────────────────┘
```

**Ihr Arbeitsablauf:**
1. Sie sagen Claude, was Sie brauchen
2. Claude macht den Rest

⏱️ **Zeit:** 30 Sekunden

---

### 💼 MCP-Praxisbeispiele für die TK

#### Beispiel 1: HR – Bewerbungsanalyse

**Szenario:** Sie möchten wissen, welche Qualifikationen Bewerber für "Sachbearbeiter Krankenversicherung" typischerweise mitbringen.

**OHNE MCP:**
```
1. Bewerbermanagement-System öffnen
2. Filter setzen: "Sachbearbeiter" + "letzten 6 Monate"
3. 47 Bewerbungen manuell durchklicken
4. Stichpunkte zu Qualifikationen notieren
5. Notizen in Claude-Chat kopieren
6. "Fasse diese Qualifikationen zusammen"

⏱️ Dauer: 45-60 Minuten
🧠 Aufwand: Hoch
😫 Frustrationslevel: Mittel
```

**MIT MCP:**
```
Sie: "Claude, analysiere die Bewerbungen für 
     'Sachbearbeiter Krankenversicherung' der letzten 
     6 Monate. Welche Qualifikationen bringen die 
     Kandidaten mit?"

Claude: [Greift via MCP auf Bewerberdatenbank zu]
        [Analysiert 47 Bewerbungen automatisch]
        
        "Analyse von 47 Bewerbungen:
        
        Top 5 Qualifikationen:
        1. Ausbildung Sozialversicherungsfachangestellte (38 von 47)
        2. Mindestens 2 Jahre Berufserfahrung (31 von 47)
        3. SAP-Kenntnisse (24 von 47)
        4. Kenntnisse im SGB V (22 von 47)
        5. Erfahrung mit KV-Software (19 von 47)
        
        Auffälligkeiten:
        - 15 Bewerber haben zusätzliche Zertifikate
        - Durchschnittsalter: 34 Jahre
        - 85% weiblich, 15% männlich"

⏱️ Dauer: 30 Sekunden
🧠 Aufwand: Minimal
😊 Frustrationslevel: Null
```

---

#### Beispiel 2: HR – Compliance-Check Stellenanzeigen

**Szenario:** Sie müssen alle aktuellen Stellenanzeigen auf AGG-Konformität prüfen (Allgemeines Gleichbehandlungsgesetz).

**OHNE MCP:**
```
1. Website öffnen → Karriereseite
2. Jede Stellenanzeige einzeln öffnen (23 Stück)
3. Text in Word-Dokument kopieren
4. Dokument zu Claude hochladen
5. Einzeln prüfen lassen
6. Ergebnisse manuell zusammentragen

⏱️ Dauer: 2-3 Stunden
📊 Fehlerquote: Hoch (Sie übersehen möglicherweise etwas)
```

**MIT MCP:**
```
Sie: "Claude, prüfe alle aktuellen Stellenanzeigen auf 
     der TK-Karriereseite auf AGG-Konformität. Erstelle 
     einen Report mit kritischen Formulierungen."

Claude: [Greift via MCP auf Website-Inhalte zu]
        [Analysiert alle 23 Stellenanzeigen]
        
        "AGG-Compliance-Check - 23 Stellenanzeigen geprüft
        
        🟢 KONFORM (19 Anzeigen)
        Keine Beanstandungen
        
        🟡 ACHTUNG (3 Anzeigen)
        - Anzeige 'IT-Projektleiter': 
          'Muttersprachler Deutsch' → Besser: 'Fließend Deutsch'
        - Anzeige 'Teamassistenz':
          'Junges Team' → Könnte Altersdiskriminierung sein
        - Anzeige 'Außendienst':
          'Belastbar' ohne Kontext → Präzisieren
        
        🔴 PROBLEMATISCH (1 Anzeige)
        - Anzeige 'Pflegefachkraft':
          'Deutschstämmig bevorzugt' → AGG-Verstoß!
          
        Empfehlung: 4 Anzeigen überarbeiten"

⏱️ Dauer: 2 Minuten
📊 Fehlerquote: Minimal (systematische Prüfung)
```

---

#### Beispiel 3: HR – Onboarding-Automatisierung

**Szenario:** Ein neuer Mitarbeiter (Max Mustermann, Abteilung Marketing) startet am 02.12.2025.

**OHNE MCP:**
```
1. E-Mail-Vorlage aus SharePoint suchen
2. Vorlage herunterladen
3. Namen/Datum manuell eintragen
4. E-Mail versenden
5. Outlook öffnen → Termin erstellen "Erster Arbeitstag"
6. SharePoint öffnen → Onboarding-Checkliste kopieren
7. Word öffnen → Checkliste personalisieren
8. IT-Ticket-System öffnen → Ticket für Equipment erstellen
9. HR-System öffnen → Personalakte anlegen

⏱️ Dauer: 30-40 Minuten
📋 Checklisten-Items: 12
🤯 Fenster/Systeme: 6
```

**MIT MCP:**
```
Sie: "Claude, neuer Mitarbeiter Max Mustermann startet 
     am 02.12.2025 in der Marketing-Abteilung. 
     Führe das Standard-Onboarding durch."

Claude: [Greift via MCP auf verschiedene Systeme zu]

        "Onboarding für Max Mustermann gestartet:
        
        ✅ Welcome-E-Mail versendet (aus Vorlage M-001)
        ✅ Kalendertermine erstellt:
           - 02.12. 09:00: Begrüßung HR
           - 02.12. 11:00: IT-Einweisung
           - 02.12. 14:00: Team-Vorstellung Marketing
        ✅ Onboarding-Checkliste erstellt und in SharePoint 
           abgelegt (Ordner: HR/Onboarding/2025-12)
        ✅ IT-Ticket #23847 erstellt:
           - Laptop (Dell Latitude)
           - Headset
           - 2x Monitor
           - Handy (iPhone)
        ✅ Zugänge beantragt:
           - E-Mail: max.mustermann@tk.de
           - SAP-Zugang
           - Intranet
        ✅ HR-System aktualisiert
        ✅ Vorgesetzte (Sarah Schmidt) informiert
        
        Nächster Schritt: Personalakte vervollständigen"

⏱️ Dauer: 45 Sekunden
📋 Alle Items erledigt: Automatisch
🤯 Sie öffnen: Nur Claude
```

---

#### Beispiel 4: Marketing – Content-Recherche mit Datenanalyse

**Szenario:** Sie planen eine neue Social-Media-Kampagne zum Thema "Psychische Gesundheit" und brauchen Insights aus vergangenen Kampagnen.

**OHNE MCP:**
```
1. Google Drive öffnen
2. Ordner "Kampagnen 2023-2024" durchsuchen
3. 15 PowerPoint-Präsentationen herunterladen
4. Jede einzeln öffnen und relevante Slides suchen
5. Google Analytics öffnen
6. Kampagnen-Performance manuell notieren
7. Social Media Dashboard öffnen (Hootsuite)
8. Engagement-Raten für Posts notieren
9. Alles in Excel zusammentragen
10. Zu Claude kopieren für Analyse

⏱️ Dauer: 2-3 Stunden
📊 Datenquellen: 4 verschiedene
🤷 Vollständigkeit: Unsicher (haben Sie alles gefunden?)
```

**MIT MCP:**
```
Sie: "Claude, analysiere unsere vergangenen 
     Social-Media-Kampagnen zum Thema 'Psychische 
     Gesundheit'. Was hat gut funktioniert?"

Claude: [Greift auf Google Drive, Analytics, Social Media zu]

        "Analyse von 7 Kampagnen (2023-2024):
        
        📊 TOP-PERFORMER:
        
        1. Kampagne 'Mentale Stärke' (März 2024)
           - Reichweite: 2,3 Mio.
           - Engagement-Rate: 8,4%
           - Beste Plattform: Instagram
           - Beste Uhrzeit: Dienstag 18-20 Uhr
           - Top-Content: Persönliche Stories von Betroffenen
        
        2. Kampagne 'Burnout-Prävention' (Sept 2023)
           - Reichweite: 1,8 Mio.
           - Engagement-Rate: 6,2%
           - Beste Plattform: LinkedIn
           - Top-Content: Experten-Interviews
        
        🎯 ERFOLGSFAKTOREN:
        - Authentische Geschichten (+45% Engagement)
        - Visuelle Elemente (Videos > Bilder > Text)
        - Hashtags: #MentalHealth #Achtsamkeit #TKgesund
        - Call-to-Action: 'Teile deine Geschichte'
        
        📉 FLOP-PERFORMER:
        - Reine Fakten-Posts (-23% Engagement)
        - Stock-Foto-Content (-31% Engagement)
        - Freitags gepostet (-18% Reichweite)
        
        💡 EMPFEHLUNG NEUE KAMPAGNE:
        - Fokus auf Instagram & LinkedIn
        - User-Generated-Content einbinden
        - Video-Format (max. 60 Sek.)
        - Posting-Zeiten: Di-Do, 18-20 Uhr
        - Budget-Fokus: Instagram Reels (+70% ROI)"

⏱️ Dauer: 3 Minuten
📊 Vollständig: Alle Datenquellen analysiert
💡 Insights: Sofort umsetzbar
```

---

#### Beispiel 5: Marketing – Konkurrenzanalyse

**Szenario:** Sie wollen wissen, wie andere Krankenkassen das Thema "Digitale Gesundheit" kommunizieren.

**OHNE MCP:**
```
1. Websites von 8 Krankenkassen öffnen
2. Relevante Seiten manuell durchklicken
3. Screenshots machen
4. Social-Media-Kanäle durchsuchen
5. Notizen in Word-Dokument
6. YouTube nach Videos suchen
7. Alles zusammentragen
8. Zu Claude für Analyse

⏱️ Dauer: 3-4 Stunden
📊 Systematik: Niedrig
😓 Mühsam: Sehr
```

**MIT MCP:**
```
Sie: "Claude, analysiere wie Barmer, AOK, DAK und 
     TechnikerKrankenkasse das Thema 'Digitale 
     Gesundheit' auf ihren Websites und Social Media 
     kommunizieren. Wo stehen wir im Vergleich?"

Claude: [Greift via MCP auf Websites & Social Media zu]

        "Konkurrenzanalyse 'Digitale Gesundheit' (4 KKs):
        
        🏆 BEST PRACTICE: Barmer
        
        Website:
        - Eigene Landingpage 'Digital Health'
        - Interaktive App-Übersicht
        - Video-Tutorials für jede App
        - Chatbot-Integration
        
        Social Media:
        - 3x pro Woche Content
        - User-Testimonials prominent
        - Hashtag: #BarmerDigital (12.400 Posts)
        
        ---
        
        📊 AOK:
        - Fokus auf Datensicherheit
        - Wenig App-Promotion
        - Eher konservative Kommunikation
        
        ---
        
        🎯 DAK:
        - Starker Fokus auf Mental-Health-Apps
        - Influencer-Kooperationen
        - Junge Zielgruppe (18-35)
        
        ---
        
        💚 TK (WIR):
        
        Stärken:
        ✅ TK-App sehr prominent platziert
        ✅ Umfangreiches Angebot (12 Apps)
        ✅ Moderne Website-Gestaltung
        
        Potenzial:
        ⚠️ Wenig User-Stories/Testimonials
        ⚠️ Video-Content unterrepräsentiert
        ⚠️ Social Media: nur 1x pro Woche
        ⚠️ Kein einheitlicher Hashtag
        
        📈 EMPFEHLUNGEN:
        1. Hashtag-Strategie: #TKDigital etablieren
        2. User-Stories-Serie starten (1x/Woche)
        3. App-Tutorial-Videos produzieren (je 60 Sek.)
        4. Posting-Frequenz erhöhen (3x/Woche)
        5. Influencer-Kooperation prüfen
        
        Quick Win:
        → Barmer's interaktive App-Übersicht adaptieren"

⏱️ Dauer: 5 Minuten
📊 Systematik: Hoch
💎 Insights: Konkret & umsetzbar
```

---

#### Beispiel 6: HR – Gehaltsvergleich & Benchmarking

**Szenario:** Sie verhandeln Gehälter für drei offene Stellen und brauchen Marktdaten.

**OHNE MCP:**
```
1. Gehaltsdatenbanken-Logins suchen
2. StepStone Gehaltsreport öffnen
3. Kununu Gehaltsübersichten checken
4. LinkedIn Salary Insights
5. Interne Gehaltsdatenbank
6. Alles in Excel-Tabelle übertragen
7. Manuell vergleichen

⏱️ Dauer: 1-2 Stunden
💰 Risiko: Veraltete Daten
```

**MIT MCP:**
```
Sie: "Claude, recherchiere aktuelle Gehaltsdaten für:
     1. Social Media Manager (3 Jahre Erfahrung)
     2. Personalreferent (5 Jahre Erfahrung)
     3. IT-Projektmanager (8 Jahre Erfahrung)
     
     Vergleiche mit unseren internen Daten."

Claude: [Greift auf Gehaltsdatenbanken & interne DB zu]

        "Gehaltsvergleich (Stand: Oktober 2025):
        
        1️⃣ SOCIAL MEDIA MANAGER (3J Erfahrung)
        
        Markt (Deutschland):
        - Median: 42.000 €/Jahr
        - 25%-75% Quartil: 38.000-48.000 €
        - Hamburg Großraum: +8% (45.500 €)
        
        TK aktuell:
        - Durchschnitt: 44.000 € (3 Personen)
        - Range: 41.000-47.000 €
        
        ✅ EMPFEHLUNG: 43.000-46.000 € (wettbewerbsfähig)
        
        ---
        
        2️⃣ PERSONALREFERENT (5J Erfahrung)
        
        Markt (Deutschland):
        - Median: 52.000 €/Jahr
        - Hamburg Großraum: +5% (54.600 €)
        - Krankenkassen-Sektor: +3% (53.600 €)
        
        TK aktuell:
        - Durchschnitt: 51.000 € (8 Personen)
        - Range: 48.000-55.000 €
        
        ⚠️ EMPFEHLUNG: 53.000-56.000 €
           (unter Markt, Anpassung empfohlen)
        
        ---
        
        3️⃣ IT-PROJEKTMANAGER (8J Erfahrung)
        
        Markt (Deutschland):
        - Median: 75.000 €/Jahr
        - Hamburg Großraum: +12% (84.000 €)
        - Healthcare IT: +8% (81.000 €)
        
        TK aktuell:
        - Durchschnitt: 72.000 € (4 Personen)
        - Range: 68.000-78.000 €
        
        🔴 KRITISCH: Deutlich unter Markt (-11%)
        💡 EMPFEHLUNG: 78.000-85.000 €
           (sonst Recruiting-Probleme)
        
        📊 ZUSATZ-INFO:
        - IT-Gehälter +6% YoY (starke Inflation)
        - Krankenkassen verlieren IT-Talente an Startups
        - Remote-Möglichkeit erhöht Attraktivität
        
        Verhandlungstipps:
        → Bei Position 3: Benefits (Remote, Weiterbildung) 
          kommunizieren"

⏱️ Dauer: 2 Minuten
📊 Datenqualität: Aktuell & mehrqualiitativ
💼 Verhandlungsposition: Gestärkt
```

---

## 🛠️ Claude Skills – Die neue Alternative

### Was sind Claude Skills?

**Skills sind vorgefertigte "Fähigkeiten", die Sie Claude beibringen können – OHNE MCP!**

Denken Sie an Skills wie an **Kochrezepte für Claude**.

### Skills vs. MCP – Der Unterschied

```
┌───────────────────────────────────────────────────────────┐
│  MCP = Claude bekommt Zugang zu EXTERNEN Datenquellen     │
│                                                           │
│  Claude ←→ Ihre Datenbank                                 │
│  Claude ←→ Ihr Google Drive                               │
│  Claude ←→ Ihre APIs                                      │
│                                                           │
│  ⚙️ Einrichtung: IT-Support nötig                         │
│  🔌 Verbindung: Zu externen Systemen                      │
└───────────────────────────────────────────────────────────┘

┌───────────────────────────────────────────────────────────┐
│  SKILLS = Claude bekommt INTERNE Anleitungen              │
│                                                           │
│  Sie ←→ Claude (mit Rezept/Anleitung)                     │
│                                                           │
│  📝 Einrichtung: Sie selbst, in Sekunden                  │
│  💡 Funktion: Claude folgt Ihren Anweisungen              │
└───────────────────────────────────────────────────────────┘
```

### Konkret: Was ist ein Skill?

Ein **Skill** ist eine gespeicherte Anleitung, die Claude automatisch befolgt.

**Beispiel-Skill: "TK-Stellenanzeigen-Prüfer"**

```
Skill-Name: TK-Stellenanzeigen-Prüfer

Anweisung:
"Wenn ich dir eine Stellenanzeige gebe, prüfe:

1. AGG-Konformität:
   - Keine Altersangaben
   - Keine Geschlechts-Präferenzen
   - Keine Herkunfts-Bezüge
   - Inklusive Sprache

2. TK-Tonalität:
   - Duzen (nicht Siezen)
   - Modern & nahbar
   - Nicht zu förmlich

3. Pflichtangaben:
   - Bewerbungsfrist
   - Ansprechpartner
   - Standort
   - Arbeitszeitmodell

4. SEO-Optimierung:
   - Relevante Keywords
   - Strukturierte Formatierung

Erstelle einen Report mit:
✅ Was ist gut
⚠️ Was sollte angepasst werden
📝 Konkrete Textvorschläge"
```

**Nutzung:**

```
Sie: [Aktivieren den Skill "TK-Stellenanzeigen-Prüfer"]
     [Kopieren eine Stellenanzeige in den Chat]

Claude: [Befolgt automatisch die Skill-Anleitung]
        
        "AGG-Check der Stellenanzeige:
        
        ✅ GUT:
        - Geschlechtsneutral formuliert
        - Keine Altersangaben
        - Inklusive Sprache verwendet
        
        ⚠️ ANPASSEN:
        
        1. Zeile 3: 'Muttersprachler Deutsch'
           → Ersetzen durch: 'Fließend Deutsch (mind. C1)'
        
        2. Zeile 12: 'Junges, dynamisches Team'
           → Ersetzen durch: 'Innovatives Team'
           (Vermeidet implizite Altersdiskriminierung)
        
        3. Fehlt: Arbeitszeitmodell
           → Ergänzen: 'Vollzeit, 38,5 Std./Woche'
        
        ..."
```

---

### 💼 Skills-Praxisbeispiele für die TK

#### Skill-Beispiel 1: "TK-E-Mail-Vorlagen-Generator"

**Was der Skill macht:**
Erstellt E-Mails im TK-Ton (Du-Form, modern, empathisch)

**Ihr Skill:**
```
Name: TK-E-Mail-Generator

Anweisung:
"Erstelle E-Mails im TK-Stil:
- Duzen (niemals Siezen)
- Persönlich & warm
- Kurze Sätze
- Emojis okay (maximal 2)
- Immer: Grüße vom TK-Team
- Bei Absagen: Empathisch, motivierend"
```

**Anwendung:**

```
Sie: [Skill aktiviert] "Erstelle eine Absage an einen Bewerber"

Claude: "Betreff: Deine Bewerbung bei der TK

Hallo Max,

vielen Dank für deine Bewerbung und das nette Gespräch letzte Woche! 

Wir haben uns intensiv mit deinem Profil beschäftigt. Leider 
müssen wir dir mitteilen, dass wir uns für einen anderen 
Kandidaten entschieden haben, dessen Profil noch etwas besser 
zur Position passt.

Das war wirklich keine leichte Entscheidung – deine Bewerbung 
hat uns überzeugt! 💚

Bewirb dich gerne bei zukünftigen Positionen wieder. Wir würden 
uns freuen, von dir zu hören!

Alles Gute für deinen weiteren Weg,

Dein TK-Team"
```

---

#### Skill-Beispiel 2: "Social-Media-Post-Optimierer"

**Was der Skill macht:**
Optimiert Social-Media-Posts für maximale Reichweite

**Ihr Skill:**
```
Name: TK-Social-Media-Optimierer

Anweisung:
"Analysiere Social-Media-Posts und optimiere für:

Instagram:
- Max 150 Zeichen im ersten Absatz (Vorschautext)
- 8-15 Hashtags
- Call-to-Action
- Emoji-Nutzung (3-5)

LinkedIn:
- Professioneller Ton
- 1-3 Hashtags
- Frage am Ende (Engagement)
- Keine übertriebenen Emojis

Allgemein:
- Lesbarkeit Score: Flesch-Reading-Ease >60
- Aktive Sprache
- Klare Botschaft in ersten 3 Sekunden"
```

**Anwendung:**

```
Sie: [Skill aktiviert] 
     "Optimiere: 'Wir haben eine neue App! 
     Sie hilft bei Rückenschmerzen. Probiert sie aus!'"

Claude: "📊 ANALYSE Original-Post:
        - Zu kurz (keine Details)
        - Keine Emotionalität
        - Kein Call-to-Action
        - Keine Hashtags
        
        ✨ OPTIMIERT FÜR INSTAGRAM:
        
        'Rückenschmerzen? 😓 Du bist nicht allein!
        
        Unsere neue App hilft dir mit:
        ✅ Täglichen 7-Min-Übungen
        ✅ Persönlichem Trainingsplan
        ✅ Schmerztagebuch
        
        Über 1.000 TK-Versicherte nutzen sie schon 💚
        
        👉 Link in Bio oder App Store: "TK-RückenFit"
        
        Hast du es schon probiert? Erzähl uns in den 
        Kommentaren! 👇
        
        #Rückengesundheit #GesundheitsTipps #RückenFit 
        #TKGesund #SelbstfürsorgeTipps #GesundeRücken 
        #Prävention #TechnikerKrankenkasse #Gesundheit'
        
        ---
        
        ✨ OPTIMIERT FÜR LINKEDIN:
        
        'Rückenschmerzen sind Volkskrankheit Nr. 1 in 
        Deutschland. 80% aller Menschen sind betroffen.
        
        Deshalb haben wir die TK-RückenFit App entwickelt:
        
        → Evidenzbasierte Übungen (geprüft von Physios)
        → Individueller Trainingsplan
        → Schmerztracking für Verlaufskontrolle
        
        Das Ergebnis? Nach 4 Wochen berichten 73% der 
        Nutzer von weniger Schmerzen.
        
        Kostenlos für alle TK-Versicherten.
        
        Wie geht ihr das Thema Mitarbeitergesundheit 
        an? 
        
        #Gesundheitsmanagement #DigitalHealth #Prävention'"
```

---

#### Skill-Beispiel 3: "Kampagnen-Brief-Generator"

**Was der Skill macht:**
Erstellt strukturierte Briefings für Kampagnen nach TK-Standard

**Ihr Skill:**
```
Name: TK-Kampagnen-Briefing

Anweisung:
"Erstelle Kampagnen-Briefings nach diesem Template:

1. KAMPAGNEN-NAME & CLAIM
2. ZIELGRUPPE (detailliert)
3. ZIEL (messbar, SMART)
4. KERNBOTSCHAFT (1 Satz)
5. KANÄLE (mit Budget-Empfehlung)
6. TIMELINE (Meilensteine)
7. KPIs (3-5 Metriken)
8. BUDGET (geschätzt)
9. RISIKEN & MITIGATION
10. QUICK WINS

Halte dich strikt an diese Struktur."
```

**Anwendung:**

```
Sie: [Skill aktiviert]
     "Erstelle ein Briefing für eine Kampagne zur 
     Förderung unserer Mental-Health-Apps bei 
     Studenten."

Claude: "📋 KAMPAGNEN-BRIEFING
        
        1. KAMPAGNEN-NAME & CLAIM
        Name: #MindMatters
        Claim: 'Dein Kopf. Dein Leben. Deine App.'
        
        ---
        
        2. ZIELGRUPPE
        Primär:
        - Studierende (18-28 Jahre)
        - Besonders: Master-/Bachelor-Endphase
        - Belastungsfaktoren: Prüfungsstress, Zukunftsangst
        - Mediennutzung: Instagram (täglich), TikTok (3x/Woche)
        - Pain Points: Überforderung, Schlafprobleme, Einsamkeit
        
        Sekundär:
        - Eltern von Studierenden
        - Universitäts-Beratungsstellen
        
        ---
        
        3. ZIEL (SMART)
        - 10.000 App-Downloads bis Ende Q1 2026
        - 500 aktive Nutzer (min. 3x/Woche Nutzung)
        - 2.500 TK-Neuversicherungen (Studenten)
        - Engagement-Rate Instagram: >5%
        
        ---
        
        4. KERNBOTSCHAFT
        'Mental Health ist kein Luxus – unsere Apps 
        unterstützen dich kostenlos durch stressige 
        Studienphasen.'
        
        ---
        
        5. KANÄLE
        🎯 PRIMÄR (70% Budget):
        - Instagram (Reels, Stories, Ads)
        - TikTok (Organic + Influencer)
        - Campus-Plakatierung (Top 20 Unis)
        
        📱 SEKUNDÄR (20% Budget):
        - LinkedIn (Eltern-Targeting)
        - YouTube (Langform-Content)
        - Hochschul-Newsletter
        
        🌐 SUPPORTIVE (10% Budget):
        - Website-Landing-Page
        - PR (Hochschul-Magazine)
        
        ---
        
        6. TIMELINE
        📅 November 2025: Konzept & Content-Produktion
        📅 Dezember 2025: Soft-Launch (2 Test-Unis)
        📅 Januar 2026: Full-Launch (alle Kanäle)
        📅 Februar 2026: Optimierung basierend auf Daten
        📅 März 2026: Abschluss & Evaluation
        
        ---
        
        7. KPIs
        📊 Awareness:
        - 5 Mio. Impressions
        - 250.000 Reichweite
        
        📊 Consideration:
        - 50.000 Landing-Page-Besuche
        - 15.000 App-Store-Clicks
        
        📊 Conversion:
        - 10.000 Downloads
        - 20% Aktivierungsrate
        
        📊 Retention:
        - 500 aktive Nutzer (nach 4 Wochen)
        
        📊 Business:
        - 2.500 Neuversicherungen
        
        ---
        
        8. BUDGET (geschätzt)
        💰 GESAMT: 85.000 €
        
        - Social Media Ads: 45.000 €
        - Influencer-Kooperationen: 20.000 €
        - Content-Produktion: 10.000 €
        - Campus-Plakate: 5.000 €
        - Landing-Page: 3.000 €
        - PR-Arbeit: 2.000 €
        
        ---
        
        9. RISIKEN & MITIGATION
        
        ⚠️ RISIKO 1: Geringes Engagement
        → Mitigation: A/B-Testing in Soft-Launch-Phase
        
        ⚠️ RISIKO 2: Influencer-Kooperationen floppen
        → Mitigation: Micro-Influencer (authentischer)
        
        ⚠️ RISIKO 3: Semester-Timing (Semesterferien)
        → Mitigation: Launch Mitte Januar (Semesterstart)
        
        ---
        
        10. QUICK WINS
        ✅ Woche 1: 3 Influencer-Posts (pre-produced)
        ✅ Woche 2: Campus-Plakate an 5 Top-Unis
        ✅ Woche 3: Instagram-Reels-Serie (5 Videos)
        ✅ Woche 4: PR-Push (3 Hochschul-Magazine)"
```

---

### Skills vs. MCP – Wann was nutzen?

```
┌────────────────────────────────────────────────────────┐
│  NUTZEN SIE SKILLS, WENN...                            │
├────────────────────────────────────────────────────────┤
│  ✅ Sie wiederkehrende Aufgaben haben                  │
│  ✅ Sie einen bestimmten Output-Stil wollen            │
│  ✅ Sie keine externe Datenanbindung brauchen          │
│  ✅ Sie es SOFORT nutzen wollen (keine IT)             │
│  ✅ Sie Claude "trainieren" wollen für Ihre Prozesse   │
│                                                        │
│  Beispiele:                                            │
│  - Texte im TK-Stil schreiben                          │
│  - Stellenanzeigen nach Schema prüfen                  │
│  - Social-Media-Posts optimieren                       │
│  - Briefings nach Template erstellen                   │
└────────────────────────────────────────────────────────┘

┌────────────────────────────────────────────────────────┐
│  NUTZEN SIE MCP, WENN...                               │
├────────────────────────────────────────────────────────┤
│  ✅ Sie Zugriff auf externe Daten brauchen             │
│  ✅ Sie Datenbanken abfragen wollen                    │
│  ✅ Sie System-Integrationen brauchen                  │
│  ✅ Sie automatisierte Workflows wollen                │
│  ✅ Ihre IT-Abteilung Sie unterstützt                  │
│                                                        │
│  Beispiele:                                            │
│  - Bewerberdatenbank durchsuchen                       │
│  - Google Drive nach Dateien durchsuchen               │
│  - Analytics-Daten automatisch abrufen                 │
│  - E-Mails automatisch versenden                       │
└────────────────────────────────────────────────────────┘
```

### Die perfekte Kombination

**Am besten wirkt die Kombination aus beiden:**

**Beispiel: Recruiting-Prozess**

```
1. MCP holt Bewerberdaten aus Datenbank
2. SKILL analysiert nach TK-Standard
3. SKILL erstellt Antwort-E-Mail im TK-Stil
4. MCP versendet E-Mail automatisch
5. MCP trägt Termin im Kalender ein
```

**Ohne manuelle Arbeit!**

---

## 🤝 ACP & A2A – Die Spezialprotokolle

### Was sind ACP und A2A?

**Kurz:** Protokolle, die es mehreren KI-Agenten ermöglichen, **miteinander** zu kommunizieren (nicht mit Ihnen).

### Der Unterschied zu MCP

```
MCP:
Sie ←→ Claude ←→ Ihre Daten

ACP/A2A:
KI-Agent 1 ←→ KI-Agent 2 ←→ KI-Agent 3
(Ohne Ihre direkte Beteiligung)
```

### Wann wird das relevant?

**Erst bei sehr fortgeschrittenen Automatisierungen**, die Ihre IT-Abteilung bauen würde.

#### Theoretisches Beispiel: Vollautomatisches Recruiting

```
┌─────────────────────────────────────────────────────────┐
│  MULTI-AGENT-SYSTEM (mit ACP/A2A)                       │
│                                                         │
│  🤖 Agent 1: "Bewerbungs-Screener"                      │
│  ↓                                                      │
│  Liest Bewerbungen → Sortiert nach Qualität            │
│  ↓                                                      │
│  Sendet Top-10 an...                                    │
│                                                         │
│  🤖 Agent 2: "Interview-Scheduler"                      │
│  ↓                                                      │
│  Prüft Kalender → Findet freie Slots                    │
│  ↓                                                      │
│  Sendet Termine an...                                   │
│                                                         │
│  🤖 Agent 3: "Kommunikations-Agent"                     │
│  ↓                                                      │
│  Schreibt personalisierte E-Mails → Versendet           │
│  ↓                                                      │
│  Informiert...                                          │
│                                                         │
│  🤖 Agent 4: "HR-System-Updater"                        │
│  ↓                                                      │
│  Trägt alles in HR-System ein                           │
└─────────────────────────────────────────────────────────┘
```

**Wichtig:** Das ist **Zukunftsmusik** für die meisten Unternehmen.

### Praktischer Hinweis

**Für Ihre tägliche Arbeit bei der TK:** Ignorieren Sie ACP/A2A vorerst.

**Fokus:** MCP + Skills = 95% Ihrer Anwendungsfälle abgedeckt

---

## 📊 Vergleichstabelle: Alle Technologien

| Kriterium | Standard-Claude | Claude Skills | MCP | ACP/A2A |
|-----------|----------------|---------------|-----|---------|
| **Setup-Zeit** | 0 Min. | 2 Min. | IT-Projekt | Entwicklungsprojekt |
| **Daten-Zugriff** | Nur Chat | Nur Chat | Externe Systeme | Zwischen Agenten |
| **Für wen?** | Alle | Alle | Mit IT-Support | Entwickler |
| **Kosten** | Abo | Abo | Abo + Setup | Komplex |
| **TK-Relevanz** | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐ |

---

## 💡 Welche Technologie für welchen Use Case?

### HR-Szenarien

| Use Case | Lösung | Warum? |
|----------|--------|--------|
| AGG-Check Stellenanzeigen | **Skill** | Wiederholbare Prüfung nach Schema |
| Bewerberdatenbank durchsuchen | **MCP** | Externe Daten nötig |
| Absage-E-Mails schreiben | **Skill** | TK-Tonalität wichtig |
| Onboarding-Checkliste erstellen | **Skill + MCP** | Template (Skill) + Daten (MCP) |
| Gehaltsvergleich recherchieren | **Standard** | Öffentliche Infos verfügbar |

### Marketing-Szenarien

| Use Case | Lösung | Warum? |
|----------|--------|--------|
| Social-Media-Posts optimieren | **Skill** | Wiederkehrendes Format |
| Kampagnen-Performance analysieren | **MCP** | Braucht Analytics-Zugriff |
| Content-Ideen brainstormen | **Standard** | Keine Daten nötig |
| Konkurrenzanalyse | **MCP** | Web-Scraping mehrerer Seiten |
| Redaktionsplan erstellen | **Skill** | Template-basiert |

---

## 🎯 Zusammenfassung: Was Sie mitnehmen sollten

### Die 5 Kern-Erkenntnisse

1. **MCP** = Claude bekommt Zugriff auf Ihre Systeme (Datenbanken, Google Drive, etc.)
   - Braucht IT-Support
   - Höchster Nutzen für Datenanalysen

2. **Skills** = Sie trainieren Claude für Ihre wiederkehrenden Aufgaben
   - Sofort nutzbar
   - Perfekt für Templates und Prozesse

3. **Standard-Claude** = Immer noch sehr mächtig für allgemeine Aufgaben
   - Keine Setup-Zeit
   - Für Brainstorming, Texterstellung, Recherche

4. **ACP/A2A** = Für komplexe Multi-Agent-Systeme
   - Aktuell nicht prioritär
   - Wird von IT gebaut

5. **Best Practice** = Kombination aus allen
   - Skill für Struktur
   - MCP für Daten
   - Standard für Kreativität

### Ihre nächsten Schritte

```
HEUTE:
□ Testen Sie einen simplen Skill
  (z.B. "Schreibe im TK-Stil")

DIESE WOCHE:
□ Überlegen Sie: Welche Daten würden MCP nützlich machen?
□ Notieren Sie 3 konkrete Use Cases

NÄCHSTEN MONAT:
□ Sprechen Sie mit Ihrer IT über MCP
□ Erstellen Sie 5 Skills für Ihre häufigsten Aufgaben
```

---

## ❓ FAQ

**F: Muss ich programmieren können?**  
A: Nein! Für Skills schreiben Sie nur Text-Anleitungen. MCP richtet Ihre IT ein.

**F: Kostet das extra?**  
A: Skills sind in Claude Pro/Team enthalten. MCP braucht IT-Setup (interner Aufwand).

**F: Kann ich Skills mit Kollegen teilen?**  
A: Ja! Skills sind einfach Text – per E-Mail teilbar.

**F: Wie sicher ist MCP mit TK-Daten?**  
A: Ihre IT kontrolliert den Zugriff. Sensible Daten (Versicherte, Gesundheit) sollten NIE angebunden werden.

**F: Was ist besser: Skills oder MCP?**  
A: Keine Konkurrenz – sie ergänzen sich! Skills für Prozesse, MCP für Daten.

---

**Viel Erfolg beim Ausprobieren! 🚀**

