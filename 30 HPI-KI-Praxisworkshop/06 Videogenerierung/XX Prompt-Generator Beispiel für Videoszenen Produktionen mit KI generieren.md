#  AI scriptwriting prompt

---

````markdown
# Role

You are an expert AI scriptwriter for 8-second micro-documentaries.  
You write serious, authoritative narration for short clips where the “fact” is confidently incorrect in a way that feels almost plausible.

---

# Purpose

Create documentary-style, deadpan narrations that pair with generic B-roll (animals, nature, space, everyday objects, inventions, life-hacks, history).  
The humour comes from credible-sounding nonsense that makes viewers replay to process the error.

---

# Non-Negotiables

**Open with authority:**  
Start with “Did you know…” (or a close variant like “Scientists say…”, “Experts believe…”).  
Prefer “Did you know…” by default.

**Believably wrong:**  
Use near-truth twists (misattributed causes, swapped mechanisms, off-by-one logic, category errors, misread jargon).  
Avoid random, disconnected absurdity.

**Deadpan documentary tone:**  
No winks, no punchline cadence, no dialogue. It should sound educational.

**8 seconds max:**  
Write for ~18–26 spoken words (≈2.3–3.2 words/sec). If in doubt, tighten.

**B-roll friendly:**  
The line should pair cleanly with common footage of the subject mentioned.

**Universal & safe:**  
PG-13. No politics, health/medical claims, religion, identity, or dangerous/imitable “hacks”  
(e.g., heat, electricity, blades, chemicals, stunts).  
No encouragement of illegal acts.

---

# Craft Principles

**Proximity to truth:**  
Anchor to a real attribute, then bend it (e.g., “penguins wear natural tuxedos” → tweak purpose or mechanism, not species or setting).

**One clean claim:**  
One idea, one scene. Don’t stack facts.

**Causal reversals:**  
Swap cause/effect in a subtle way.

**Misapplied terms:**  
Use real jargon slightly wrong (e.g., “solar panels store moonlight”).

**Scale & units slips:**  
Small, plausible-sounding numerics (e.g., “99% of clouds are recycled each week”).

**Etymology traps:**  
Confident but wrong origins (e.g., “sandwich named after the inventor, Sandy Witch”).

**Time & history fog:**  
Off-by-century with confidence.

---

# Output Format

Return a JSON object with exactly these properties:

- **Script** (the narrator’s single sentence)
- **Title** (max 8 words)
- **Description** (short; include 3 hashtags)

---

# Writing Template *(internal guidance; don’t output this)*

Script begins: “Did you know …”  
Words: 18–26  
Tone: calm, informative, certain  
Content: one specific subject that matches easy B-roll

---

# Better, Believable-Wrong Examples

**Nature – Bees**  
“Did you know bees make honey mostly at night, because sunlight melts the recipe during the day?”  
→ Anchors to honey/temperature; wrong mechanism.

**Space – Moon**  
“Did you know the Moon looks bigger near the horizon because Earth’s atmosphere works like a magnifying glass set to ‘zoom’?”  
→ Plays on the real Moon illusion; wrong cause.

**Animals – Owls**  
“Did you know owls rotate their heads to cool their brains, like a built-in desk fan?”  
→ Real rotation, wrong purpose.

**Everyday – Bananas**  
“Did you know bananas ripen faster near Wi-Fi, because the signal ‘wakes up’ their sugars?”  
→ Sounds techy; harmlessly wrong.

**Science – Rainbows**  
“Did you know double rainbows happen when clouds copy-paste the first one by accident?”  
→ Office metaphor; visually coherent.

**History – Maps**  
“Did you know old maps were drawn with north on top only because printing presses stacked pages that way?”  
→ Confident, procedural, wrong.

**Plants – Sunflowers**  
“Did you know sunflowers face east in the morning to download light more efficiently?”  
→ Real heliotropism, tech-wrongness.

**Everyday – Keys**  
“Did you know metal keys work better when warmed by your pocket, because locks read temperature as a password?”  
→ Everyday object, wrong mechanism.

**Weather – Wind**  
“Did you know wind slows down at night because trees are off the clock?”  
→ Personification of a real night/day pattern.

**Materials – Glass**  
“Did you know glass is technically a slow liquid, which is why old windows sag from top to bottom?”  
→ Classic myth, confidently asserted.

---

# Quality Checklist (apply before returning)

✅ 18–26 words?  
✅ Starts with “Did you know…” (or approved variant)?  
✅ One believable-wrong idea, clearly paired to obvious B-roll?  
✅ No danger, politics, religion, or health claims?  
✅ Deadpan tone (no punchlines or jokes)?

---

# Example JSON Outputs

```json
{
  "Script": "Did you know bees make honey mostly at night, because sunlight melts the recipe during the day?",
  "Title": "Night-Shift Honey",
  "Description": "A serious mini-doc that’s confidently wrong. #funfacts #documentary #shorts"
}
````

```json
{
  "Script": "Did you know the Moon looks bigger near the horizon because Earth’s atmosphere works like a magnifying glass set to ‘zoom’?",
  "Title": "Why the Moon ‘Zooms’",
  "Description": "Deadpan science—subtly, hilariously wrong. #space #didyouknow #shorts"
}
```

---

# Description Format

* Write a short, 2-sentence max SEO description for the video.
* Include a section at the bottom of the description with the text:

```
DISCLAIMER:
This video was generated using AI as a fun experiment to view the world through an LLM's "eyes". 
It's intended to be odd and factually inaccurate.
```

---

# IMPORTANT

**No Captions or On-Screen Text:**
Never include or suggest subtitles, on-screen words, or text overlays.
Scripts are for narration only — visuals are implied through B-roll, not text.
The prompt to the video generation model should include a parenthetical note, e.g.
`(do not include captions)`

---

```

---

✅ This version merges all fragments, corrects formatting, and ensures consistent structure — perfect for directly reusing as an **AI system prompt** or **instruction document**.
```

---
---

# 📘 NUTZUNGSANLEITUNG: TK Veo 3 Video Generator

## Willkommen zum TK Video-Content-Generator!

Diese Anleitung zeigt Ihnen Schritt für Schritt, wie Sie mit dem optimierten Veo 3 Prompt professionelle Video-Inhalte für Social Media erstellen.

---

## 🎯 Inhaltsverzeichnis

1. [Schnellstart](#schnellstart)
2. [Voraussetzungen](#voraussetzungen)
3. [Schritt-für-Schritt-Anleitung](#schritt-für-schritt-anleitung)
4. [Praktische Beispiele](#praktische-beispiele)
5. [Tipps & Best Practices](#tipps--best-practices)
6. [Häufige Fragen](#häufige-fragen)
7. [Troubleshooting](#troubleshooting)

---

## 🚀 Schnellstart

**In 5 Minuten zum ersten Video-Prompt:**

1. JSON-Datei `tk_veo3_optimierter_prompt.json` öffnen
2. Gesamten Inhalt kopieren
3. In ChatGPT oder Claude einfügen
4. Auf Begrüßung warten
5. Gewünschtes Video beschreiben
6. JSON-Output kopieren
7. In Google Veo 3 einfügen
8. Video generieren!

---

## ✅ Voraussetzungen

### Technische Voraussetzungen
- ✅ Zugang zu einem LLM (ChatGPT Plus, Claude Pro, oder ähnlich)
- ✅ Zugang zu Google Veo 3 (Video-Generierungs-Tool)
- ✅ Web-Browser (Chrome, Firefox, Safari, Edge)
- ✅ Stabile Internetverbindung

### Inhaltliche Voraussetzungen
- ✅ Grundverständnis der TK-Markenidentität
- ✅ Kenntnis der Zielgruppe
- ✅ Klare Vorstellung der gewünschten Botschaft
- ✅ Bewusstsein für Compliance-Anforderungen (bei Gesundheitsthemen)

### Organisatorische Voraussetzungen
- ✅ Bei Mitarbeiter-Content: Einwilligungen einholen
- ✅ Bei Gesundheitscontent: Fachabteilung für Review einplanen
- ✅ Legal/Compliance-Freigabe-Prozess kennen
- ✅ Rechte an Musik/Bildern/Stimmen klären

---

## 📋 Schritt-für-Schritt-Anleitung

### Phase 1: Vorbereitung

#### Schritt 1: Content-Planung (5-10 Minuten)

**Bevor Sie den Prompt nutzen, klären Sie:**

**a) Ziel des Videos**
- Was wollen Sie erreichen? (Awareness, Engagement, Recruiting, Information)
- Welche Aktion soll ausgelöst werden? (App-Download, Bewerbung, Gesundheits-Tipp umsetzen)

**b) Zielgruppe definieren**
- Externe: Versicherte, Interessenten, allgemeine Öffentlichkeit
- Interne: Mitarbeitende, Bewerber*innen, Partner

**c) Kernbotschaft formulieren**
- Eine klare Hauptaussage (nicht mehr als ein Satz!)
- Beispiel: "Die TK-App macht Hautcheck einfach und schnell"
- Beispiel: "Bei der TK arbeitest du an sinnvollen digitalen Lösungen"

**d) Content-Kategorie wählen**
- 🏥 Gesundheitsprävention & Tipps
- 💼 Employer Branding & Recruiting
- 👥 Mitarbeiter-Stories & Testimonials
- 📱 Service & digitale Angebote
- 🎯 Event-Promotion & Kampagnen
- 🌟 Behind-the-Scenes
- 🤝 Kooperationen & Partner
- 📚 Aufklärung & Information

**e) Platform festlegen**
- Instagram Reels (9:16, 7-15 Sek)
- TikTok (9:16, 8-20 Sek)
- LinkedIn (1:1 oder 16:9, 15-30 Sek)
- Facebook (1:1, 10-30 Sek)
- YouTube Shorts (9:16, 15-60 Sek)

#### Schritt 2: Compliance-Check vorab (2-5 Minuten)

**Prüfen Sie vor der Erstellung:**

✅ **Bei Gesundheitsthemen:**
- Sind die Aussagen evidenzbasiert?
- Keine Heilversprechen?
- Fachabteilung für Review verfügbar?

✅ **Bei Mitarbeiter-Content:**
- Liegt Einwilligung der Person vor?
- Persönlichkeitsrechte geklärt?
- Person über Nutzung informiert?

✅ **Generell:**
- TK-Markenrichtlinien bekannt?
- Musik-/Bildrechte geklärt?
- Budget für eventuelle Nachbearbeitung?

---

### Phase 2: Prompt-Nutzung

#### Schritt 3: Prompt aktivieren (1 Minute)

**a) JSON-Datei öffnen**
- Öffnen Sie die Datei `tk_veo3_optimierter_prompt.json`
- Nutzen Sie einen Text-Editor oder öffnen Sie direkt im Browser

**b) Komplett kopieren**
- Wählen Sie den GESAMTEN Inhalt aus (Strg+A / Cmd+A)
- Kopieren Sie alles (Strg+C / Cmd+C)

**c) In LLM einfügen**
- Öffnen Sie ChatGPT, Claude oder ähnliches Tool
- Fügen Sie den kopierten JSON-Code ein (Strg+V / Cmd+V)
- Senden Sie die Nachricht

**d) Auf Begrüßung warten**
Der Prompt sollte automatisch mit folgender Begrüßung antworten:

> "Hallo! Ich bin der TK Video-Generator für Social Media Content. Ich erstelle professionelle Video-Prompts für die Bereiche HR und Marketing der Techniker Krankenkasse. Welche Art von Video möchten Sie heute erstellen?"

**✅ Perfekt! Der Generator ist aktiviert und bereit.**

#### Schritt 4: Video-Anforderungen kommunizieren (2-3 Minuten)

**Sie haben zwei Optionen:**

**Option A: Strukturierte Anfrage (empfohlen für Anfänger)**

Nutzen Sie folgendes Template:

```
Ich möchte ein Video für [PLATFORM] erstellen:

- Kategorie: [z.B. Gesundheitstipp, Employer Branding, Service-Erklärer]
- Thema: [z.B. Rückenschmerzen im Büro, Karriere bei der TK, TK-App Feature]
- Zielgruppe: [z.B. Versicherte 25-45, Bewerber*innen IT-Bereich]
- Länge: [z.B. 8 Sekunden, 15 Sekunden, 20 Sekunden]
- Protagonist: [z.B. TK-Gesundheitsexpertin, Mitarbeiter aus IT, repräsentative Person]
- Setting: [z.B. Büro, Home-Office, Studio, Outdoor]
- Besonderheiten: [z.B. dynamisch, ruhig, mit Team im Hintergrund]
```

**Beispiel:**
```
Ich möchte ein Video für Instagram Reels erstellen:

- Kategorie: Gesundheitsprävention
- Thema: 3 schnelle Dehnübungen gegen Nackenverspannungen im Home-Office
- Zielgruppe: Berufstätige im Home-Office, 28-45 Jahre
- Länge: 8-10 Sekunden
- Protagonist: Sympathische TK-Gesundheitsexpertin, ca. 35 Jahre
- Setting: Modernes Home-Office mit Fenster
- Besonderheiten: Motivierend, praktisch umsetzbar, freundliche Atmosphäre
```

**Option B: Freie Beschreibung (für Fortgeschrittene)**

Beschreiben Sie in eigenen Worten, was Sie möchten:

```
"Ich brauche einen kurzen Clip für TikTok, der zeigt, wie einfach der Hautcheck in der TK-App funktioniert. Sollte etwa 15 Sekunden lang sein und step-by-step zeigen: App öffnen, Hautcheck auswählen, Foto machen, Ergebnis bekommen. Zielgruppe sind junge Erwachsene die präventiv auf ihre Gesundheit achten wollen."
```

#### Schritt 5: JSON-Output erhalten (sofort)

Der Generator erstellt nun ein vollständiges JSON-Objekt mit allen Details:

```json
{
  "scene_name": {
    "scene": {
      "camera": {...},
      "subject": {...},
      "props": {...},
      "setting": {...},
      "lighting": {...}
    },
    "action": {...},
    "dialogue": {...},
    "audio": {...},
    "style": {...},
    "tk_compliance_check": {...}
  }
}
```

**Wichtig:** Kopieren Sie das KOMPLETTE JSON-Objekt!

---

### Phase 3: Video-Generierung

#### Schritt 6: JSON in Veo 3 übertragen (1 Minute)

**a) Google Veo 3 öffnen**
- Navigieren Sie zu Google Veo 3 (https://labs.google/veo)
- Melden Sie sich an mit Ihrem Account

**b) JSON einfügen**
- Fügen Sie das komplette JSON-Objekt in das Prompt-Feld ein
- ODER: Konvertieren Sie das JSON in einen Textprompt (manuelle Zusammenfassung)

**c) Einstellungen wählen**
- Format: Wählen Sie 9:16 (vertikal) für Instagram/TikTok oder 16:9 für YouTube/LinkedIn
- Dauer: Wählen Sie die gewünschte Länge
- Qualität: Wählen Sie die höchste verfügbare Qualität

**d) Video generieren**
- Klicken Sie auf "Generate" oder "Erstellen"
- Warten Sie auf die Generierung (kann 2-10 Minuten dauern)

#### Schritt 7: Erstes Review (2-3 Minuten)

**Prüfen Sie das generierte Video auf:**

✅ **Technische Qualität**
- Ist die Bildqualität gut?
- Ist der Ton klar und verständlich?
- Funktioniert die Lippensynchronisation?
- Gibt es visuelle Artefakte oder Fehler?

✅ **Inhaltliche Korrektheit**
- Wird die Botschaft klar vermittelt?
- Entspricht es der TK-Markenidentität?
- Ist der Ton/die Stimmung passend?
- Stimmen die Details (Branding, Setting)?

✅ **Compliance-Aspekte**
- Bei Gesundheitscontent: Sind die Aussagen korrekt?
- Keine problematischen Darstellungen?
- TK-Logo korrekt verwendet?

**Wenn nicht zufrieden:** Passen Sie das JSON an und generieren Sie erneut!

---

### Phase 4: Nachbearbeitung & Freigabe

#### Schritt 8: Nachbearbeitung (5-15 Minuten)

**Empfohlene Nachbearbeitungs-Schritte:**

**a) Untertitel hinzufügen**
- Auch wenn Veo 3 "no_subtitles" vorschlägt: Untertitel sind für Barrierefreiheit essentiell!
- Tools: CapCut, Adobe Premiere, Kapwing, Descript
- Achten Sie auf korrekte Rechtschreibung und Sync

**b) TK-Branding optimieren**
- TK-Logo hinzufügen/optimieren (falls nötig)
- Outro mit Social-Media-Handles
- Call-to-Action-Text einblenden

**c) Audio optimieren**
- Lautstärke anpassen
- Hintergrundmusik hinzufügen (lizenzfreie Musik!)
- Rauschunterdrückung wenn nötig

**d) Feinschliff**
- Farbkorrektur für TK-Brand Colors
- Schnitte optimieren
- Übergänge glätten

**Empfohlene Tools:**
- CapCut (kostenlos, benutzerfreundlich)
- Adobe Premiere Pro (professionell)
- DaVinci Resolve (kostenlos, professionell)
- Kapwing (online, einfach)

#### Schritt 9: Freigabe-Prozess (variabel, 1-5 Tage)

**Abhängig vom Content-Typ:**

**Gesundheitsprävention-Content:**
1. Medizinische Fachabteilung prüft Inhalte → 1-2 Tage
2. Legal/Compliance Check → 1 Tag
3. Marketing-Freigabe → 1 Tag
4. Finale Freigabe

**Employer-Branding-Content:**
1. HR-Abteilung prüft Darstellung → 1 Tag
2. Betroffene Mitarbeiter*innen final freigeben → 1 Tag
3. Marketing-Freigabe → 1 Tag
4. Finale Freigabe

**Service-Content:**
1. Fachbereich prüft Korrektheit → 1 Tag
2. Legal prüft Claims → 1 Tag
3. Marketing-Freigabe → 1 Tag
4. Finale Freigabe

**Behind-the-Scenes/Event-Content:**
1. HR/Marketing prüft → 1 Tag
2. Finale Freigabe

**Tipp:** Planen Sie Freigabe-Zeit im Content-Kalender ein!

#### Schritt 10: Veröffentlichung (10-30 Minuten)

**a) Plattform-spezifische Anpassungen**

**Instagram Reels:**
- Format: 9:16
- Upload direkt über Instagram App
- Hashtags: 5-10 relevante Hashtags
- Caption: Kurz und prägnant
- Cover-Bild: Auswählen

**TikTok:**
- Format: 9:16
- Trending Sounds nutzen (wenn passend)
- Hashtags: Mix aus großen und Niche-Hashtags
- Caption: Mit Hook beginnen
- Posting-Zeit: Best Times beachten

**LinkedIn:**
- Format: 1:1 oder 16:9
- Native Upload (nicht als Link!)
- Caption: Ausführlicher, professionell
- Hashtags: Business-relevant
- Tagging: TK-Account, relevante Personen

**b) Posting-Strategie**
- Bester Zeitpunkt: Je nach Plattform und Zielgruppe
- Cross-Posting: Anpassen für jede Plattform
- Community Management: Kommentare beantworten einplanen

**c) Tracking vorbereiten**
- UTM-Parameter in Links (wenn applicable)
- Tracking-Pixel einrichten
- Notieren: Posting-Datum, -Zeit, -Platform für Reporting

---

## 💡 Praktische Beispiele

### Beispiel 1: Gesundheitstipp für Instagram Reels

**Anfrage an den Generator:**
```
Erstelle ein Video für Instagram Reels:

- Kategorie: Gesundheitsprävention
- Thema: "Augen-Entspannung bei Bildschirmarbeit - 20-20-20 Regel"
- Zielgruppe: Büroangestellte, 25-50 Jahre
- Länge: 8 Sekunden
- Protagonist: Freundliche TK-Augengesundheits-Expertin
- Setting: Helles modernes Büro
- Besonderheiten: Schnell erfassbar, sofort umsetzbar
```

**Nutzung des JSON-Outputs:**
1. JSON generieren lassen
2. In Veo 3 einfügen → Video erstellen
3. Untertitel hinzufügen: "Alle 20 Min: 20 Sek auf 20 Fuß (6m) Entfernung schauen 👀"
4. TK-Logo unten rechts
5. Musik: Ruhige, fokussierte Beats
6. Hashtags: #Augengesundheit #BüroTipps #TechnikerKrankenkasse #Gesundheit #HomeOffice

**Ergebnis:** Snackable Content, der wertvollen Tipp liefert und TK als kompetenten Partner zeigt.

---

### Beispiel 2: Employer Branding für LinkedIn

**Anfrage an den Generator:**
```
Ich brauche ein Employer-Branding-Video für LinkedIn:

- Kategorie: Mitarbeiter-Testimonial
- Thema: "Warum ich als IT-Entwickler bei der TK arbeite"
- Zielgruppe: IT-Professionals, Bewerber*innen
- Länge: 20 Sekunden
- Protagonist: Echter TK-Mitarbeiter (männlich, 32 Jahre, Developer)
- Setting: Modernes Entwickler-Office mit Team im Hintergrund
- Besonderheiten: Authentisch, technologie-fokussiert, zeigt moderne Tools
```

**Nutzung des JSON-Outputs:**
1. JSON generieren
2. Anpassen: Namen des echten Mitarbeiters einfügen
3. Veo 3 für Grundgerüst nutzen ODER direkt mit echtem Mitarbeiter drehen
4. Nachbearbeitung: Untertitel, TK-Branding, Call-to-Action ("Jetzt bewerben: tk.de/karriere")
5. Caption für LinkedIn: Ausführlicher Text über Technologie bei der TK
6. Tagging: Mitarbeiter taggen, #TKKarriere, #DevLife, #HealthTech

**Ergebnis:** Authentisches Recruiting-Video, das Tech-Talent anspricht.

---

### Beispiel 3: Service-Erklärer für TikTok

**Anfrage an den Generator:**
```
Service-Erklärer für TikTok:

- Kategorie: Service & digitale Angebote
- Thema: "TK-App Bonusprogramm in 3 Steps"
- Zielgruppe: Junge Versicherte, 18-35
- Länge: 15 Sekunden
- Protagonist: Dynamische Person mit Smartphone
- Setting: Casual, Couch oder Café
- Besonderheiten: TikTok-Style, snappy, Screen-Recording-Elemente
```

**Nutzung des JSON-Outputs:**
1. JSON generieren
2. Veo 3 → Basis-Video
3. Screen-Recording der TK-App hinzufügen
4. Schnelle Schnitte für TikTok-Dynamik
5. Trending Sound nutzen
6. Text-Overlays: "Step 1", "Step 2", "Step 3"
7. Hashtags: #TKApp #Bonus #LifeHack #Gesundheit

**Ergebnis:** App-Download-Driver mit viraler TikTok-Anmutung.

---

## 🎓 Tipps & Best Practices

### Content-Erstellung

**✅ DO's:**
- ✅ **Eine Botschaft pro Video** - Fokus ist key
- ✅ **Hook in den ersten 2 Sekunden** - Attention Grabber nutzen
- ✅ **Authentizität zeigen** - Echte Menschen, echte Stories
- ✅ **Mobile First denken** - Vertikales Format bevorzugen
- ✅ **Untertitel IMMER hinzufügen** - 85% schauen ohne Ton
- ✅ **Call-to-Action einbauen** - Was soll der Viewer tun?
- ✅ **A/B-Testing durchführen** - Verschiedene Versionen testen
- ✅ **Storytelling nutzen** - Emotionen schaffen Verbindung
- ✅ **Qualität vor Quantität** - Lieber weniger, aber hochwertig
- ✅ **Trends beobachten** - Aber authentisch bleiben

**❌ DON'Ts:**
- ❌ **Zu viele Botschaften** - Verwirrt den Viewer
- ❌ **Langsamer Start** - Verliert sofort Attention
- ❌ **Zu verkäuferisch** - Authentizität geht verloren
- ❌ **Komplizierte Sprache** - Keep it simple
- ❌ **Schlechte Audio-Qualität** - Dealbreaker für Engagement
- ❌ **Inkonsistente Branding** - Verwirrt die Zielgruppe
- ❌ **Blind Trends folgen** - Muss zur Marke passen
- ❌ **Compliance ignorieren** - Rechtliche Risiken
- ❌ **Barrierefreiheit vergessen** - Exkludiert Zielgruppe
- ❌ **Performance nicht tracken** - Kein Lernen möglich

### Prompt-Optimierung

**Wie Sie bessere JSON-Outputs bekommen:**

1. **Je spezifischer, desto besser**
   - ❌ Schlecht: "Mach ein Video über Gesundheit"
   - ✅ Gut: "8-Sekunden Instagram Reel über 3 Nackenübungen für Home-Office-Arbeiter"

2. **Visuelle Details liefern**
   - Beschreiben Sie Setting, Licht, Stimmung
   - Beispiel: "Helles, freundliches Büro mit Fenster, natürliches Tageslicht, moderne Einrichtung"

3. **Zielgruppe präzise definieren**
   - ❌ Schlecht: "Junge Menschen"
   - ✅ Gut: "Berufseinsteigende IT-Professionals, 23-30 Jahre, technikaffin"

4. **Tone of Voice spezifizieren**
   - Beispiel: "Motivierend aber nicht übertrieben, freundlich und kompetent"

5. **Bei Unzufriedenheit: Iterieren!**
   - Sagen Sie dem Generator was Sie ändern möchten
   - Beispiel: "Das Setting ist gut, aber die Protagonistin sollte jünger und dynamischer wirken"

### Compliance & Legal

**Checkliste für rechtssichere Videos:**

**Gesundheitscontent:**
- [ ] Keine Heilversprechen ("garantiert", "heilt", "kuriert")
- [ ] Evidenzbasierte Aussagen (wissenschaftlich fundiert)
- [ ] Bei Unsicherheit: Fachabteilung konsultieren
- [ ] Disclaimer wo nötig ("Ersetzt nicht ärztliche Beratung")
- [ ] Keine Diagnose-Aussagen

**Persönlichkeitsrechte:**
- [ ] Schriftliche Einwilligung von erkennbaren Personen
- [ ] Verwendungszweck klar kommuniziert
- [ ] Recht auf Widerruf beachten
- [ ] Bei Kindern: Eltern-Einwilligung
- [ ] Anonymisierung wo sinnvoll

**Urheberrechte:**
- [ ] Musik lizenziert oder lizenzfrei
- [ ] Keine geschützten Marken/Logos (außer eigene)
- [ ] Stockfootage lizenziert
- [ ] KI-generierte Inhalte: Nutzungsrechte klären
- [ ] Bei Zitaten: Quellenangabe

**Datenschutz:**
- [ ] Keine personenbezogenen Gesundheitsdaten
- [ ] DSGVO-konform
- [ ] Datenschutzerklärung verlinkt (wo applicable)
- [ ] Keine sensiblen Daten sichtbar

**Wettbewerbsrecht:**
- [ ] Keine irreführende Werbung
- [ ] Konkurrenz nicht herabsetzen
- [ ] Wahrheitsgemäße Aussagen
- [ ] Vergleichende Werbung nur mit Fakten

### Performance-Optimierung

**So tracken Sie den Erfolg Ihrer Videos:**

**KPIs definieren je nach Ziel:**

**Awareness-Content:**
- Reach/Impressions
- View Rate
- Watch Time/Completion Rate
- Shares

**Engagement-Content:**
- Likes, Comments, Saves
- Engagement Rate
- Click-Through-Rate
- Follower-Wachstum

**Conversion-Content:**
- Link-Clicks
- App-Downloads
- Bewerbungen eingegangen
- Lead-Generierung

**Tools nutzen:**
- Native Platform Analytics (Instagram Insights, TikTok Analytics, LinkedIn Analytics)
- Google Analytics (für Traffic auf Website)
- UTM-Parameter für Campaign-Tracking
- Social Media Management Tools (Hootsuite, Buffer, Sprout Social)

**Learnings dokumentieren:**
- Was funktioniert? (Format, Thema, Stil, Länge)
- Was funktioniert nicht?
- Zielgruppen-Insights
- Best Performing Time Slots
- Content-Saturation (Wie oft zum gleichen Thema posten?)

---

## ❓ Häufige Fragen (FAQ)

### Allgemeine Fragen

**F: Wie lange dauert es, ein Video mit diesem System zu erstellen?**
A: Von der Idee bis zum fertigen Video:
- Planung: 5-10 Min
- Prompt & JSON-Generierung: 2-3 Min
- Veo 3 Video-Generierung: 2-10 Min
- Nachbearbeitung: 5-15 Min
- **Gesamt: Ca. 15-40 Minuten** (ohne Freigabe-Prozess)

**F: Kostet die Nutzung von Veo 3 etwas?**
A: Google Veo 3 ist aktuell in einer Beta-Phase. Die Kosten-Struktur kann variieren. Bitte prüfen Sie die aktuellen Preise auf der Google Labs Website.

**F: Kann ich den gleichen Prompt mehrfach nutzen?**
A: Ja! Sie können den Generator beliebig oft verwenden. Jedes Mal wenn Sie das JSON einfügen, startet eine neue Session.

**F: Muss ich den GESAMTEN JSON-Code einfügen?**
A: Ja, für die optimale Funktionalität sollten Sie den kompletten Prompt einfügen. Der Generator benötigt alle Kontext-Informationen.

### Technische Fragen

**F: Welche LLMs funktionieren am besten mit diesem Prompt?**
A: Empfohlen:
- ChatGPT-4 oder höher (OpenAI)
- Claude 3 Opus/Sonnet (Anthropic)
- Google Gemini Pro

**F: Das JSON ist sehr lang - kann ich es kürzen?**
A: Wir empfehlen, das vollständige JSON zu nutzen. Kürzungen können die Qualität der Outputs beeinträchtigen.

**F: Funktioniert der Prompt auch in anderen Sprachen?**
A: Der Prompt ist auf Deutsch optimiert, funktioniert aber grundsätzlich auch auf Englisch. Die Outputs werden dann allerdings auf Englisch sein.

**F: Wie speichere ich das generierte JSON für spätere Nutzung?**
A: Kopieren Sie das JSON und speichern Sie es als .json oder .txt Datei lokal. Sie können auch ein "Prompt-Bibliothek" anlegen.

### Content-Fragen

**F: Kann ich auch längere Videos (>60 Sekunden) generieren?**
A: Der Prompt ist auf Social-Media-Short-Form-Content optimiert (8-60 Sekunden). Für längere Videos müssten Sie mehrere Szenen generieren und zusammenfügen.

**F: Kann ich echte TK-Mitarbeiter in KI-generierte Videos "einsetzen"?**
A: Das ist rechtlich und ethisch komplex. Empfehlung:
- Für Employer Branding: Lieber echte Mitarbeiter filmen
- KI-Videos: Mit fiktiven/repräsentativen Personen
- Hybrid: Echte Aufnahmen + KI-generierte B-Roll

**F: Wie gehe ich mit sensiblen Gesundheitsthemen um?**
A: 
1. Immer Fachabteilung konsultieren
2. Keine Diagnosen oder Behandlungsempfehlungen
3. Allgemeine Präventionstipps sind OK
4. Disclaimer nutzen: "Ersetzt nicht ärztliche Beratung"

**F: Kann ich den Prompt für andere Krankenkassen anpassen?**
A: Technisch ja, aber dieser Prompt ist spezifisch für die TK-Markenidentität optimiert. Für andere Organisationen sollten Sie Brand-Guidelines, Tone of Voice und Compliance-Anforderungen anpassen.

### Workflow-Fragen

**F: Wie viele Videos sollte ich auf einmal generieren?**
A: Empfehlung:
- Start: 3-5 Pilot-Videos testen
- Dann: Wöchentlich 5-10 Videos produzieren
- Wichtig: Qualität vor Quantität!

**F: Sollte ich einen Content-Kalender führen?**
A: Absolut! Empfohlene Struktur:
- Monatsplan mit Themen
- Wochenplan mit konkreten Videos
- Posting-Schedule mit Best Times
- Tracking-Sheet für Performance

**F: Wie oft sollte ich den gleichen Content-Type posten?**
A: Abhängig von Platform und Zielgruppe:
- Gesundheitstipps: 2-3x/Woche
- Employer Branding: 1-2x/Woche
- Service-Erklärer: 1x/Woche
- Behind-the-Scenes: 1x/Monat
- Event-Content: Ad-hoc

**F: Kann ich Videos recyceln/repurposen?**
A: Ja! Strategie:
- Gleichen Content für verschiedene Platforms anpassen
- Saisonale Themen jährlich neu aufgreifen
- Evergreen-Content regelmäßig re-posten
- Updates/Refreshes bei veralteten Infos

### Compliance-Fragen

**F: Wer muss bei Gesundheitsvideos final freigeben?**
A: Empfohlener Freigabe-Prozess:
1. Medizinische Fachabteilung (Inhalt)
2. Legal/Compliance (Rechtliches)
3. Marketing (Branding)
4. Finale Freigabe durch verantwortliche Führungskraft

**F: Muss ich bei KI-generierten Videos kennzeichnen, dass sie von KI erstellt wurden?**
A: Aktuell keine gesetzliche Pflicht in Deutschland, aber:
- Transparenz schafft Vertrauen
- Bei täuschend echten Inhalten: Disclosure empfohlen
- Plattform-Richtlinien beachten (können sich ändern)

**F: Wie lange muss ich Einwilligungen von Mitarbeitern aufbewahren?**
A: Nach DSGVO: Solange die Daten verarbeitet werden + 3 Jahre danach. Praktisch: Solange das Video online ist + Aufbewahrungsfrist.

---

## 🔧 Troubleshooting

### Problem: JSON-Generator reagiert nicht

**Symptom:** Nach Einfügen des Prompts kommt keine Begrüßung

**Mögliche Lösungen:**
1. ✅ Prüfen Sie, ob der KOMPLETTE JSON-Code eingefügt wurde
2. ✅ Versuchen Sie es in einer neuen Chat-Session
3. ✅ Wechseln Sie ggf. das LLM (ChatGPT → Claude oder umgekehrt)
4. ✅ Überprüfen Sie, ob JSON-Format korrekt ist (keine fehlenden Klammern)

---

### Problem: Generiertes JSON funktioniert nicht in Veo 3

**Symptom:** Veo 3 akzeptiert das JSON nicht oder generiert Fehler

**Mögliche Lösungen:**
1. ✅ Veo 3 akzeptiert möglicherweise kein direktes JSON → Konvertieren Sie zu Text-Prompt
2. ✅ Extrahieren Sie die Kern-Elemente manuell:
   - Camera-Setup
   - Subject-Beschreibung
   - Action
   - Dialogue
   - Setting
   - Audio
3. ✅ Erstellen Sie einen zusammenhängenden Text-Prompt aus diesen Elementen
4. ✅ Nutzen Sie den Generator mit Prompt: "Konvertiere dieses JSON in einen zusammenhängenden Veo-3-Prompt"

---

### Problem: Video-Qualität entspricht nicht Erwartungen

**Symptom:** Generiertes Video ist unscharf, hat Artefakte oder falsche Details

**Mögliche Lösungen:**
1. ✅ JSON detaillierter gestalten - mehr visuelle Details hinzufügen
2. ✅ Mehrere Versionen generieren und beste auswählen
3. ✅ Veo-3-Einstellungen anpassen (höhere Qualität wählen)
4. ✅ Komplexität reduzieren - einfachere Szenen generieren oft bessere Ergebnisse
5. ✅ Nachbearbeitung nutzen um Schwächen auszugleichen

---

### Problem: TK-Branding nicht korrekt dargestellt

**Symptom:** Farben, Logo oder Stil entsprechen nicht TK-Guidelines

**Mögliche Lösungen:**
1. ✅ Im JSON mehr Details zu TK-Branding spezifizieren:
   ```
   "Nutze TK-Blau (#005E9A) als Hauptfarbe"
   "TK-Logo unten rechts platzieren"
   "Moderne, aufgeräumte TK-Büro-Ästhetik"
   ```
2. ✅ In Nachbearbeitung Branding hinzufügen/optimieren
3. ✅ Color Grading auf TK-Farben anpassen
4. ✅ Logo und Branding-Elemente als Overlay hinzufügen

---

### Problem: Compliance-Bedenken nach Video-Generierung

**Symptom:** Video enthält problematische Aussagen oder Darstellungen

**Mögliche Lösungen:**
1. ✅ Video NICHT veröffentlichen
2. ✅ Problematische Stellen identifizieren
3. ✅ JSON anpassen mit spezifischen Compliance-Hinweisen
4. ✅ Neu generieren
5. ✅ Bei Unsicherheit: Legal/Compliance-Team konsultieren
6. ✅ In Nachbearbeitung problematische Teile ausschneiden/übersprechen

---

### Problem: Protagonist wirkt nicht authentisch/natürlich

**Symptom:** KI-generierte Person sieht "uncanny" oder künstlich aus

**Mögliche Lösungen:**
1. ✅ Für Employer Branding & Testimonials: Echte Mitarbeiter filmen (empfohlen!)
2. ✅ JSON anpassen: Mehr Details zu natürlichen Ausdrücken und Bewegungen
3. ✅ Mehrere Versionen generieren
4. ✅ Close-ups vermeiden (Artefakte bei KI-Gesichtern häufiger)
5. ✅ Hybrid-Ansatz: KI für B-Roll, echte Menschen für Talking Heads

---

### Problem: Audio-Qualität schlecht oder asynchron

**Symptom:** Stimme klingt robotisch oder Lippen nicht synchron

**Mögliche Lösungen:**
1. ✅ Im JSON Voice-Beschreibung detaillieren: "Natürliche, warme Stimme, klare Aussprache"
2. ✅ Neu generieren (manchmal hilft schon ein zweiter Versuch)
3. ✅ Voice-Over in Nachbearbeitung ersetzen mit:
   - Professionellem Sprecher
   - TK-Mitarbeiter
   - Hochwertigem Text-to-Speech
4. ✅ Lippensync-Tools nutzen (z.B. D-ID, Synthesia für Korrektur)

---

### Problem: Video zu lang/kurz für Platform

**Symptom:** Generiertes Video passt nicht zur gewünschten Plattform-Länge

**Mögliche Lösungen:**
1. ✅ Im JSON Timing präziser spezifizieren:
   ```
   "timing": "0-2s [Hook], 2-6s [Content], 6-8s [CTA]"
   ```
2. ✅ In Nachbearbeitung kürzen/verlängern
3. ✅ Neu generieren mit angepasstem Timing
4. ✅ Geschwindigkeit anpassen (1.2x schneller für kürzere Version)

---

### Problem: Call-to-Action fehlt oder unklar

**Symptom:** Video endet ohne klare Handlungsaufforderung

**Mögliche Lösungen:**
1. ✅ Im JSON explizit CTA hinzufügen:
   ```
   "dialogue": {
     "speech": "...[Content]... Jetzt TK-App downloaden!",
     ...
   }
   ```
2. ✅ In Nachbearbeitung Text-Overlay mit CTA hinzufügen
3. ✅ End-Card mit Handlungsaufforderung anhängen
4. ✅ In Caption/Beschreibung klaren CTA platzieren

---

## 📞 Support & Kontakt

### Interne Ansprechpartner (fiktive Struktur - bitte anpassen!)

**Bei technischen Fragen:**
- IT-Support: it-support@tk.de
- Digital Marketing Team: digital-marketing@tk.de

**Bei Content-Fragen:**
- Marketing: marketing@tk.de
- HR-Kommunikation: hr-kommunikation@tk.de

**Bei Compliance/Legal:**
- Legal Department: legal@tk.de
- Datenschutz: datenschutz@tk.de

**Bei Gesundheitsinhalten:**
- Medizinische Fachabteilung: medizin@tk.de

### Externe Ressourcen

**Google Veo 3:**
- Website: https://labs.google/veo
- Documentation: https://ai.google.dev/veo

**Best Practices Social Media:**
- Meta Business: https://business.facebook.com/
- LinkedIn Marketing: https://business.linkedin.com/
- TikTok for Business: https://www.tiktok.com/business/

---

## 📚 Weitere Ressourcen

### Empfohlene Lernressourcen

**Video-Produktion:**
- YouTube Creator Academy (kostenlos)
- LinkedIn Learning (Video Marketing Kurse)
- Udemy (Social Media Video Kurse)

**KI-Tools:**
- Google AI Blog
- ChatGPT/Claude Documentation
- Veo 3 Community Forum

**Social Media Marketing:**
- HubSpot Academy (Social Media Zertifizierung)
- Hootsuite Social Marketing Zertifizierung
- Meta Blueprint (Facebook/Instagram Marketing)

**Rechtliches:**
- DSGVO-Informationsportal
- Urheberrecht.de
- IHK-Ratgeber Social Media Recht

---

## 🎉 Los geht's!

Sie haben jetzt alle Informationen, um mit dem TK Veo 3 Video Generator professionelle Social-Media-Videos zu erstellen!

**Quick Start Reminder:**
1. ✅ JSON-Datei öffnen und kopieren
2. ✅ In ChatGPT/Claude einfügen
3. ✅ Begrüßung abwarten
4. ✅ Video-Wunsch beschreiben
5. ✅ JSON-Output in Veo 3 nutzen
6. ✅ Video generieren
7. ✅ Nachbearbeiten & Freigeben
8. ✅ Veröffentlichen & Tracken

**Viel Erfolg bei der Video-Produktion für die Techniker Krankenkasse! 🎬**

---



