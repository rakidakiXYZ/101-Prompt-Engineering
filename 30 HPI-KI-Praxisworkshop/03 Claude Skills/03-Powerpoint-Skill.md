# Tutorial: Erstellen eines CI-PowerPoint-Skills für Ihr Unternehmen

## Übersicht

Dieses Tutorial zeigt Ihnen Schritt für Schritt, wie Sie einen eigenen PowerPoint-Skill erstellen, der automatisch Präsentationen im Corporate Design Ihres Unternehmens generiert. Am Ende haben Sie einen wiederverwendbaren Skill, den Ihr gesamtes Team nutzen kann.

## Was Sie erreichen werden

- ✅ Einen Skill namens "branded-deck", der CI-konforme Präsentationen erstellt
- ✅ Automatische Anwendung Ihrer Unternehmensfarben, -schriftarten und -layouts
- ✅ Konsistente Logo-Platzierung und visuelle Hierarchie
- ✅ Ein installationsfähiges .skill-Paket für Ihr Team

## Voraussetzungen

### Was Sie benötigen

1. **Ihre PowerPoint-Vorlage**: Eine .pptx-Datei mit Ihrem Corporate Design
2. **Zugriff auf Claude**: Mit aktivierter Computer-Use-Funktion
3. **Grundlegendes Verständnis**: Von Farben (Hex-Codes) und Schriftarten

### Was die Vorlage enthalten sollte

- Master-Folien mit Ihrem Layout
- Ihr Firmenlogo (korrekt platziert)
- Definierte Farben und Schriftarten
- Verschiedene Folienlayouts (Titel, Inhalt, etc.)

---

## Schritt 1: Verstehen der Ausgangssituation

### Was ist ein Skill?

Ein Skill ist ein modulares Paket, das Claude neue Fähigkeiten gibt. In unserem Fall:
- **Input**: "Erstelle eine Q4-Präsentation im CI meines Unternehmens"
- **Output**: Professionelle PowerPoint-Präsentation mit Ihrem Corporate Design

### Projektstruktur verstehen

Ein fertiger Skill sieht so aus:

```
branded-deck/
├── SKILL.md                    # Hauptanweisungen für Claude
├── assets/
│   └── template.pptx           # Ihre CI-Vorlage
└── references/
    └── design-system.md        # Extrahierte Design-Informationen
```

---

## Schritt 2: Vorbereitung - Design-Informationen sammeln

### 2.1 Vorlage analysieren

Laden Sie Ihre PowerPoint-Vorlage hoch und fragen Sie Claude:

```
Bitte analysiere diese PowerPoint-Vorlage und extrahiere:
1. Alle verwendeten Farben (als Hex-Codes)
2. Alle Schriftarten (Name und wo sie verwendet werden)
3. Logo-Position und -Größe
4. Typische Folienlayouts
5. Abstände und Größenverhältnisse
```

### 2.2 Design-System dokumentieren

Claude wird etwas Ähnliches erstellen:

```markdown
# Design-System: [Ihr Firmenname]

## Farben
- **Primärfarbe**: #003366 (Dunkelblau) - Überschriften, Header
- **Sekundärfarbe**: #FF6600 (Orange) - Akzente, wichtige Punkte
- **Hintergrund**: #FFFFFF (Weiß)
- **Text**: #333333 (Dunkelgrau)

## Schriftarten
- **Überschriften**: Montserrat Bold, 32pt
- **Unterüberschriften**: Montserrat SemiBold, 24pt
- **Fließtext**: Open Sans Regular, 14pt
- **Fußzeilen**: Open Sans Regular, 10pt

## Logo
- Position: Obere rechte Ecke
- Größe: 120px × 40px
- Abstand: 20px von oben, 20px von rechts

## Layouts
1. Titelfolie: Zentriert, großes Logo
2. Inhaltsfolie: Logo oben rechts, Überschrift links
3. Zwei-Spalten: 60/40 Aufteilung
```

**💡 Tipp**: Speichern Sie diese Informationen - sie werden in `references/design-system.md` verwendet.

---

## Schritt 3: Skill initialisieren

### 3.1 Skill-Struktur erstellen

Bitten Sie Claude:

```
Bitte initialisiere einen neuen Skill namens "branded-deck" mit dem init_skill.py Skript.
```

Claude führt aus:

```bash
python /mnt/skills/public/skill-creator/scripts/init_skill.py branded-deck --path /home/claude/branded-deck
```

Dies erstellt die Grundstruktur:

```
branded-deck/
├── SKILL.md (Template mit TODOs)
├── scripts/
│   └── example_script.py
├── references/
│   └── example_reference.md
└── assets/
    └── example_asset.txt
```

### 3.2 Unnötige Dateien entfernen

Die Beispieldateien können gelöscht werden:

```bash
rm branded-deck/scripts/example_script.py
rm branded-deck/references/example_reference.md
rm branded-deck/assets/example_asset.txt
```

---

## Schritt 4: Design-Informationen integrieren

### 4.1 Vorlage speichern

Ihre PowerPoint-Vorlage muss in den `assets/` Ordner:

```
Bitte kopiere meine hochgeladene Vorlage "FirmaX_Template.pptx" 
nach /home/claude/branded-deck/assets/template.pptx
```

### 4.2 Design-System dokumentieren

Erstellen Sie `references/design-system.md` mit den gesammelten Informationen:

```
Bitte erstelle /home/claude/branded-deck/references/design-system.md 
mit den vorher extrahierten Design-Informationen.
```

**Wichtig**: Diese Datei sollte alle Details enthalten:
- Exakte Hex-Codes für Farben
- Font-Namen und -Größen
- Präzise Abstände und Positionen
- Layout-Muster

---

## Schritt 5: SKILL.md schreiben

### 5.1 Frontmatter definieren

Der Kopf von SKILL.md definiert, wann der Skill aktiviert wird:

```yaml
---
name: branded-deck
description: Creates professional PowerPoint presentations following [Your Company]'s corporate identity. Use when users request company presentations, CI slides, pitch decks, or branded presentations. Automatically applies company colors, fonts, logo placement, and layout standards.
---
```

**Trigger-Begriffe** (wann der Skill aktiviert wird):
- "CI-Präsentation"
- "Unternehmens-CI"
- "Pitch-Deck im Firmen-Style"
- "Firmenpräsentation"
- "gebrandete Folien"

### 5.2 Haupt-Anweisungen schreiben

Der Body von SKILL.md enthält die Arbeitsanweisungen:

```markdown
# Branded Deck Creator - [Your Company] CI

## Überblick

Erstelle PowerPoint-Präsentationen, die dem Corporate Design von [Your Company] folgen.
Verwende die bereitgestellte Vorlage und das Design-System für konsistente, professionelle Ergebnisse.

## Wann diesen Skill verwenden

Verwende diesen Skill, wenn der Benutzer fragt nach:
- Unternehmenspräsentationen im CI
- Pitch-Decks im Firmen-Style
- CI-konforme Folien
- Gebrandete Präsentationen

## Workflow

### 1. Design-System laden

Lies IMMER zuerst das Design-System:
- Datei: `references/design-system.md`
- Enthält: Farben, Schriftarten, Logo-Specs, Layouts

### 2. Vorlage verwenden oder HTML2PPTX?

**Entscheidungsbaum:**

**Verwende die Vorlage** (`assets/template.pptx`), wenn:
- Der Benutzer eine Standard-Präsentation möchte (5-15 Folien)
- Die Layouts aus der Vorlage ausreichen
- Schnelle Erstellung wichtiger ist als komplexe Anpassungen

**Verwende HTML2PPTX**, wenn:
- Sehr spezifische, individuelle Layouts benötigt werden
- Komplexe Visualisierungen erforderlich sind
- Mehr als 20 Folien erstellt werden sollen

### 3. Vorlage-basierter Workflow

Wenn Sie die Vorlage verwenden:

1. **Vorlage laden und analysieren**
   ```bash
   # Text extrahieren
   python -m markitdown assets/template.pptx > template-content.md
   
   # Thumbnails erstellen
   python /mnt/skills/public/pptx/scripts/thumbnail.py assets/template.pptx workspace/template-thumbnails
   ```

2. **Folien-Inventar erstellen**
   - Lies die Vorlage komplett durch
   - Erstelle `template-inventory.md` mit ALLEN Folien (0-indiziert!)
   - Gruppiere nach Typ (Titel, Inhalt, Zwei-Spalten, etc.)

3. **Präsentations-Outline erstellen**
   - Plane basierend auf verfügbaren Vorlagen
   - Weise jedem Inhaltspunkt eine Vorlage zu
   - Erstelle präzise Texte für jede Folie

4. **Folien duplizieren**
   ```bash
   python /mnt/skills/public/pptx/scripts/duplicate.py \
     assets/template.pptx working.pptx \
     --keep 0 2 2 5 5 3 1
   ```

5. **Text-Replacement-JSON erstellen**
   - Extrahiere Inventar der neuen Datei
   - Erstelle `replacement-text.json` mit allen Texten
   - Behalte Formatierung bei (bold, alignment, colors)

6. **Replacements anwenden**
   ```bash
   python /mnt/skills/public/pptx/scripts/replace.py \
     working.pptx replacement-text.json output.pptx
   ```

7. **Validierung**
   - Erstelle Thumbnails des Ergebnisses
   - Prüfe auf Text-Cutoffs, Überlappungen
   - Korrigiere bei Bedarf

### 4. HTML2PPTX-basierter Workflow

Wenn individuelle Erstellung nötig ist:

1. **pptx Skill-Dokumentation lesen**
   ```bash
   # IMMER ZUERST lesen:
   cat /mnt/skills/public/pptx/html2pptx.md
   ```

2. **CSS-Variablen aus Design-System erstellen**
   
   Erstelle `styles.css` mit Ihren CI-Farben:
   ```css
   :root {
     --color-primary: #003366;
     --color-secondary: #FF6600;
     --color-text: #333333;
     --color-background: #FFFFFF;
     
     --font-heading: 'Montserrat', sans-serif;
     --font-body: 'Open Sans', sans-serif;
     
     --spacing-lg: 40px;
     --spacing-md: 24px;
     --spacing-sm: 16px;
   }
   ```

3. **HTML-Folien erstellen**
   
   Jede Folie als separate HTML-Datei (960×540px für 16:9):
   ```html
   <!DOCTYPE html>
   <html>
   <head>
     <style>
       /* Embed styles.css hier */
       body { width: 960px; height: 540px; }
       .logo { 
         position: absolute; 
         top: 20px; 
         right: 20px; 
         width: 120px; 
         height: 40px; 
       }
       h1 { 
         color: var(--color-primary); 
         font-family: var(--font-heading); 
       }
     </style>
   </head>
   <body>
     <img src="logo.svg" class="logo">
     <h1>Folientitel</h1>
     <p>Inhalt...</p>
   </body>
   </html>
   ```

4. **Konvertierungs-Skript ausführen**
   ```javascript
   const pptxgen = require("pptxgenjs");
   const { html2pptx } = require("@ant/html2pptx");
   
   const pptx = new pptxgen();
   pptx.layout = "LAYOUT_16x9";
   
   await html2pptx("slide1.html", pptx);
   await html2pptx("slide2.html", pptx);
   // ... weitere Folien
   
   await pptx.writeFile("output.pptx");
   ```

5. **Thumbnails prüfen**
   ```bash
   python /mnt/skills/public/pptx/scripts/thumbnail.py output.pptx workspace/check
   ```

## Design-Regeln

### Farben

Verwende IMMER die definierten CI-Farben aus `references/design-system.md`:
- Primärfarbe für Überschriften und wichtige Elemente
- Sekundärfarbe sparsam für Akzente
- Konsistente Textfarben

### Schriftarten

Halte dich an die Schrift-Hierarchie:
- H1: Hauptüberschriften (größte Schrift)
- H2: Unterüberschriften
- Body: Fließtext
- Small: Fußnoten, Quellen

### Logo

**KRITISCH**: Logo-Platzierung ist fest definiert!
- Position gemäß `references/design-system.md`
- Niemals skalieren oder verzerren
- Immer ausreichend Freiraum

### Abstände

Folge den Spacing-Regeln:
- Konsistente Ränder auf allen Folien
- Ausreichend Whitespace
- Lesbare Zeilenhöhen

## Best Practices

1. **Konsistenz ist König**: Jede Folie sollte dem CI folgen
2. **Weniger ist mehr**: Nicht zu viel Text pro Folie
3. **Visuell prüfen**: Immer Thumbnails kontrollieren
4. **Validieren**: Keine Fehler durchlassen

## Häufige Probleme vermeiden

❌ **Falsch**: Farben erfinden oder abweichen  
✅ **Richtig**: Exakt die CI-Farben verwenden

❌ **Falsch**: Logo frei platzieren  
✅ **Richtig**: Logo an definierter Position

❌ **Falsch**: Verschiedene Schriftgrößen für gleiche Hierarchie  
✅ **Richtig**: Konsistente Größen für H1, H2, Body

## Qualitätskontrolle

Vor Auslieferung prüfen:
- [ ] Alle Folien haben das Logo korrekt platziert
- [ ] CI-Farben wurden durchgängig verwendet
- [ ] Schriftarten und -größen sind konsistent
- [ ] Kein Text wird abgeschnitten
- [ ] Keine Überlappungen
- [ ] Ausreichend Kontrast für Lesbarkeit

## Beispiel-Anfragen

**Benutzer**: "Erstelle eine Q4-Ergebnispräsentation im CI meines Unternehmens"

**Vorgehen**:
1. Design-System laden
2. Outline erstellen (z.B.: Titelfolie, Agenda, Highlights, Zahlen, Ausblick)
3. Passende Vorlagen aus template.pptx wählen
4. Folien duplizieren und Text ersetzen
5. Validieren

**Benutzer**: "Erstelle ein 10-seitiges Pitch-Deck mit unserer CI-Vorlage"

**Vorgehen**:
1. Design-System laden
2. Pitch-Deck-Struktur planen (Problem, Lösung, Markt, etc.)
3. Falls Vorlage ausreicht: Template-Workflow
4. Falls spezielle Visualisierungen nötig: HTML2PPTX-Workflow
5. Validieren

## Referenzen

- **Design-System**: `references/design-system.md`
- **Vorlage**: `assets/template.pptx`
- **pptx Skill**: `/mnt/skills/public/pptx/SKILL.md`
```

---

## Schritt 6: Skill validieren und paketieren

### 6.1 Validierung

Bitten Sie Claude:

```
Bitte validiere den branded-deck Skill mit dem package_skill.py Skript.
```

Claude führt aus:

```bash
python /mnt/skills/public/skill-creator/scripts/package_skill.py /home/claude/branded-deck
```

**Mögliche Fehler und Lösungen:**

| Fehler | Lösung |
|--------|--------|
| "Missing description" | Fügen Sie eine aussagekräftige description im Frontmatter hinzu |
| "SKILL.md too large" | Verschieben Sie Details in references/ |
| "Invalid YAML" | Prüfen Sie die Syntax im Frontmatter |

### 6.2 Paketierung

Nach erfolgreicher Validierung wird automatisch ein `.skill` File erstellt:

```
✅ Created: branded-deck.skill
```

---

## Schritt 7: Skill installieren und testen

### 7.1 Umbenennung für Download

Da `.skill` Dateien spezielle Behandlung haben:

```
Bitte benenne branded-deck.skill in branded-deck.zip um 
und kopiere es nach /mnt/user-data/outputs/
```

### 7.2 Installation

1. Laden Sie `branded-deck.zip` herunter
2. Benennen Sie es zurück zu `branded-deck.skill`
3. Öffnen Sie Claude.ai
4. Gehen Sie zu **Settings > Skills**
5. Klicken Sie auf **"Upload Skill"**
6. Wählen Sie `branded-deck.skill`
7. Der Skill ist jetzt aktiv! ✨

### 7.3 Test-Anfragen

Testen Sie den Skill mit verschiedenen Anfragen:

```
1. "Erstelle eine 5-seitige Q4-Präsentation im Firmen-CI"
2. "Mache ein Pitch-Deck für unser neues Produkt mit unserer CI-Vorlage"
3. "Erstelle Folien für ein Kunden-Meeting im Unternehmens-Style"
```

**Prüfen Sie**:
- ✅ Werden die CI-Farben korrekt verwendet?
- ✅ Ist das Logo richtig platziert?
- ✅ Sind die Schriftarten konsistent?
- ✅ Sehen die Folien professionell aus?

---

## Schritt 8: Iteration und Verbesserung

### 8.1 Feedback sammeln

Nach den ersten Tests:

1. Notieren Sie, was gut funktioniert
2. Identifizieren Sie Verbesserungspotenzial
3. Sammeln Sie Feedback vom Team

### 8.2 Skill aktualisieren

Um den Skill zu verbessern:

```
Claude, bitte lade den branded-deck Skill und aktualisiere:
- Die Abstände in den Überschriften vergrößern
- Eine neue Folie für Team-Vorstellungen hinzufügen
- Die Farben noch präziser definieren
```

Claude wird:
1. Die Änderungen vornehmen
2. Den Skill neu paketieren
3. Ihnen die aktualisierte Version geben

### 8.3 Best Practices für Updates

- **Versionierung**: Notieren Sie Änderungen (intern oder im Team-Wiki)
- **Testing**: Testen Sie nach jeder Änderung gründlich
- **Dokumentation**: Aktualisieren Sie Team-Dokumentation bei größeren Änderungen

---

## Fortgeschrittene Anpassungen

### Custom Scripts hinzufügen

Wenn Sie häufig wiederkehrende Operationen haben:

```python
# scripts/add_company_footer.py
def add_footer(pptx_file, company_name):
    """Fügt automatisch Fußzeile zu allen Folien hinzu"""
    # Implementierung...
```

Referenzieren in SKILL.md:

```markdown
## Fußzeilen automatisch hinzufügen

```bash
python scripts/add_company_footer.py presentation.pptx "FirmaX GmbH"
```
```

### Mehrere Vorlagen unterstützen

Organisieren Sie mehrere Vorlagen:

```
assets/
├── template-standard.pptx    # Normale Präsentationen
├── template-pitch.pptx       # Pitch-Decks
└── template-internal.pptx    # Interne Updates
```

Wählen Sie in SKILL.md basierend auf Kontext:

```markdown
## Vorlagen-Auswahl

- **Standard**: Für allgemeine Präsentationen
- **Pitch**: Für Investoren und Partner
- **Internal**: Für Team-Updates

Wähle die passende Vorlage basierend auf der Anfrage des Benutzers.
```

### Internationale Unterstützung

Für mehrsprachige Teams:

```markdown
## Sprach-Unterstützung

Der Skill unterstützt:
- 🇩🇪 Deutsch (Standard)
- 🇬🇧 Englisch
- 🇫🇷 Französisch

Erkenne die Sprache der Benutzeranfrage und erstelle die Präsentation 
in der entsprechenden Sprache.
```

---

## Troubleshooting

### Problem: Skill wird nicht aktiviert

**Symptom**: Claude verwendet den Skill nicht, obwohl Sie CI-Präsentationen anfragen.

**Lösungen**:
1. Prüfen Sie die `description` im Frontmatter - enthält sie Trigger-Wörter?
2. Seien Sie spezifischer: "Erstelle eine CI-konforme Firmenpräsentation"
3. Erwähnen Sie den Skill explizit: "Verwende den branded-deck Skill"

### Problem: Farben sind falsch

**Symptom**: Die Präsentation verwendet nicht die CI-Farben.

**Lösungen**:
1. Prüfen Sie `references/design-system.md` auf korrekte Hex-Codes
2. Stellen Sie sicher, dass SKILL.md auf das Design-System verweist
3. Validieren Sie, dass Claude die Referenz lädt: "Bitte lies zuerst das Design-System"

### Problem: Logo fehlt oder ist falsch platziert

**Symptom**: Logo ist nicht da oder an falscher Position.

**Lösungen**:
1. Prüfen Sie, ob das Logo in `assets/` vorhanden ist
2. Validieren Sie Logo-Spezifikationen in `references/design-system.md`
3. Für Template-Workflow: Überprüfen Sie, ob das Logo in der Vorlage korrekt ist
4. Für HTML2PPTX: Stellen Sie sicher, dass Logo im HTML-Code eingebunden ist

### Problem: Text wird abgeschnitten

**Symptom**: Texte überlappen oder werden abgeschnitten.

**Lösungen**:
1. Erstellen Sie Thumbnails zur visuellen Prüfung
2. Reduzieren Sie Textmenge pro Folie
3. Passen Sie Schriftgrößen an (in `design-system.md` dokumentieren)
4. Bei Template-Workflow: Wählen Sie passendere Vorlagen-Layouts

### Problem: Validation schlägt fehl

**Symptom**: `package_skill.py` gibt Fehler aus.

**Häufige Fehler**:
- **"Invalid YAML"**: Syntax-Fehler im Frontmatter → Prüfen Sie Einrückung und Quotes
- **"Description too short"**: Description muss aussagekräftig sein → Erweitern Sie sie
- **"Missing required field"**: `name` oder `description` fehlt → Ergänzen Sie sie
- **"File too large"**: SKILL.md > 500 Zeilen → Verschieben Sie Inhalte nach `references/`

---

## Checkliste: Skill bereit für Produktion

Bevor Sie den Skill an Ihr Team verteilen:

### Qualität
- [ ] SKILL.md ist klar und präzise geschrieben
- [ ] Alle Pfade zu Dateien sind korrekt
- [ ] Design-System ist vollständig dokumentiert
- [ ] Vorlage(n) sind im `assets/` Ordner
- [ ] Beispiel-Anfragen funktionieren einwandfrei

### Testing
- [ ] Skill mit 5+ verschiedenen Anfragen getestet
- [ ] Alle generierten Präsentationen visuell geprüft
- [ ] CI-Konformität bestätigt (Farben, Fonts, Logo)
- [ ] Keine Text-Cutoffs oder Überlappungen
- [ ] Funktioniert mit kurzen und langen Präsentationen

### Dokumentation
- [ ] Team weiß, wie man den Skill installiert
- [ ] Beispiel-Anfragen dokumentiert und geteilt
- [ ] Ansprechpartner für Fragen definiert
- [ ] Update-Prozess festgelegt

### Packaging
- [ ] Validation erfolgreich durchlaufen
- [ ] .skill File erstellt
- [ ] Als .zip für Download verfügbar
- [ ] Version irgendwo notiert (z.B. "v1.0")

---

## Team-Rollout: Best Practices

### 1. Kommunikation

Informieren Sie Ihr Team:

```
📧 E-Mail-Template:

Betreff: Neuer Skill verfügbar: Automatische CI-Präsentationen

Hallo Team,

ab sofort könnt ihr Claude verwenden, um automatisch Präsentationen 
im Unternehmens-CI zu erstellen!

Was ist neu:
✨ Automatische Anwendung unserer CI-Farben und -Fonts
✨ Korrektes Logo-Placement
✨ Professionelle Layouts

So funktioniert's:
1. Skill installieren (Anleitung im Anhang)
2. Claude fragen: "Erstelle eine Q4-Präsentation im Firmen-CI"
3. Fertiges Deck erhalten ✅

Beispiel-Anfragen:
- "Erstelle ein Pitch-Deck mit unserer CI-Vorlage"
- "Mache eine Kundenpräsentation im Unternehmens-Style"
- "Erstelle 10 Folien für unser Team-Meeting im CI"

Bei Fragen: [Ihr Name]

Viel Erfolg!
```

### 2. Schulung

**Quick-Start Session** (15 Minuten):
- Demo: Live-Erstellung einer Präsentation
- Hands-on: Jeder erstellt eine Test-Präsentation
- Q&A: Fragen beantworten

**Ressourcen bereitstellen**:
- Dieses Tutorial als PDF
- Video-Tutorial (Screen-Recording)
- FAQ-Dokument

### 3. Support-Struktur

Definieren Sie:
- **Skill-Owner**: Wer ist verantwortlich für Updates?
- **Support-Kanal**: Slack-Channel oder E-Mail?
- **Feedback-Prozess**: Wie werden Verbesserungsvorschläge gesammelt?

### 4. Monitoring

Sammeln Sie regelmäßig:
- Nutzungsstatistiken (wie oft wird der Skill verwendet?)
- Feedback (was funktioniert gut, was nicht?)
- Feature-Requests (was würde den Skill noch besser machen?)

---

## Zusammenfassung

Sie haben jetzt gelernt:

✅ **Konzept**: Was Skills sind und wie sie funktionieren  
✅ **Vorbereitung**: Design-Informationen sammeln und dokumentieren  
✅ **Erstellung**: Skill-Struktur aufbauen und SKILL.md schreiben  
✅ **Paketierung**: Skill validieren und als .skill File paketieren  
✅ **Installation**: Skill in Claude hochladen und aktivieren  
✅ **Testing**: Skill gründlich testen und verbessern  
✅ **Rollout**: Skill ans Team verteilen und supporten

### Nächste Schritte

1. **Starten Sie klein**: Erstellen Sie zuerst einen einfachen Skill mit einer Vorlage
2. **Iterieren Sie**: Verbessern Sie basierend auf echtem Feedback
3. **Erweitern Sie**: Fügen Sie mehr Vorlagen und Features hinzu
4. **Teilen Sie**: Rollen Sie den Skill ans Team aus

### Weitere Ressourcen

- **Skill Creator Dokumentation**: `/mnt/skills/public/skill-creator/SKILL.md`
- **PPTX Skill Dokumentation**: `/mnt/skills/public/pptx/SKILL.md`
- **Claude Docs**: https://docs.anthropic.com

---

## Anhang: Vollständiges Beispiel

### Beispiel: Komplettes `branded-deck/` für "TechCorp"

```
branded-deck/
├── SKILL.md (siehe Schritt 5.2)
├── assets/
│   └── template.pptx (TechCorp CI-Vorlage)
└── references/
    └── design-system.md
```

### design-system.md für TechCorp

```markdown
# TechCorp Design System

## Brand Identity
**Company**: TechCorp Solutions GmbH  
**Industry**: Technology / SaaS  
**Brand Values**: Innovation, Reliability, Clarity

## Color Palette

### Primary Colors
- **Tech Blue**: `#0066CC` - Headers, key information, CTAs
- **Deep Navy**: `#003366` - Titles, emphasis
- **Pure White**: `#FFFFFF` - Backgrounds, contrast

### Secondary Colors
- **Vibrant Orange**: `#FF6600` - Highlights, warnings, action items
- **Soft Gray**: `#F5F5F5` - Backgrounds for content sections
- **Dark Gray**: `#333333` - Body text

### Accent Colors
- **Success Green**: `#00CC66` - Positive metrics, growth indicators
- **Alert Red**: `#CC0000` - Urgent information, decline indicators

## Typography

### Font Families
- **Headings**: Roboto Bold
- **Subheadings**: Roboto Medium
- **Body Text**: Roboto Regular
- **Captions**: Roboto Light

### Font Sizes
- **Title Slide H1**: 44pt
- **Content Slide H1**: 32pt
- **H2**: 24pt
- **Body Text**: 16pt
- **Captions/Footnotes**: 12pt

### Line Heights
- **Headings**: 1.2
- **Body Text**: 1.5
- **Lists**: 1.8

## Logo Specifications

### Primary Logo
- **File**: `logo-primary.svg`
- **Position**: Top right corner
- **Size**: 140px × 50px
- **Spacing**: 24px from top, 24px from right
- **Clear Space**: Minimum 12px on all sides

### Logo Variations
- **Dark Background**: Use white logo (`logo-white.svg`)
- **Light Background**: Use colored logo (`logo-primary.svg`)
- **Minimum Size**: Never smaller than 80px wide

## Layout System

### Slide Dimensions
- **Aspect Ratio**: 16:9
- **Width**: 960px
- **Height**: 540px

### Grid System
- **Columns**: 12-column grid
- **Gutter**: 24px
- **Margins**: 48px (left/right), 40px (top/bottom)

### Safe Zones
- **Title Zone**: Top 80px (reserved for headers + logo)
- **Footer Zone**: Bottom 40px (reserved for page numbers, copyright)
- **Content Area**: Middle 420px

## Slide Layouts

### 1. Title Slide
- **Layout**: Centered
- **Elements**: 
  - Large logo (centered, 200px width)
  - H1 title (centered, Tech Blue)
  - Subtitle (centered, Dark Gray)
  - Presenter name (bottom center)
- **Background**: White with subtle gradient

### 2. Content Slide
- **Layout**: Single column
- **Elements**:
  - Logo (top right)
  - H1 title (left-aligned, Tech Blue)
  - Body content (bullet points or paragraphs)
  - Footer with page number
- **Background**: White

### 3. Two-Column Slide
- **Layout**: 50/50 or 60/40 split
- **Elements**:
  - Logo (top right)
  - H1 title (spans both columns)
  - Left column: Text content
  - Right column: Image or chart
- **Divider**: 1px vertical line in Soft Gray

### 4. Chart Slide
- **Layout**: Full-width content area
- **Elements**:
  - Logo (top right)
  - H1 title
  - Large chart (centered)
  - Caption/source (bottom left, small)
- **Chart Colors**: Primary palette for data series

### 5. Quote Slide
- **Layout**: Centered
- **Elements**:
  - Large quotation mark icon (Vibrant Orange)
  - Quote text (36pt, Tech Blue)
  - Attribution (18pt, Dark Gray)
- **Background**: Soft Gray

### 6. Section Divider
- **Layout**: Full-bleed
- **Elements**:
  - Large H1 (centered, white text)
  - Section number (Vibrant Orange)
- **Background**: Deep Navy gradient

## Component Patterns

### Headers
```
H1: Roboto Bold, 32pt, Tech Blue (#0066CC)
H2: Roboto Medium, 24pt, Deep Navy (#003366)
```

### Lists
- **Bullet Style**: Round, Vibrant Orange
- **Indent**: 24px
- **Line Spacing**: 1.8
- **Font**: Roboto Regular, 16pt

### Tables
- **Header Row**: Tech Blue background, white text
- **Alternating Rows**: White / Soft Gray
- **Border**: 1px solid Dark Gray
- **Cell Padding**: 12px

### Charts
- **Primary Data**: Tech Blue (#0066CC)
- **Secondary Data**: Vibrant Orange (#FF6600)
- **Tertiary Data**: Success Green (#00CC66)
- **Grid Lines**: Soft Gray (#F5F5F5)
- **Axis Labels**: Dark Gray, 12pt

## Spacing Rules

### Margins
- **Slide Edges**: 48px minimum
- **Between Elements**: 24px standard, 32px for major sections
- **Title to Content**: 32px

### Padding
- **Text Boxes**: 16px all sides
- **Shapes**: 20px all sides
- **Tables**: 12px cell padding

## Accessibility

### Contrast Ratios
- **Body Text**: Minimum 7:1 (Dark Gray on White)
- **Headers**: Minimum 4.5:1 (Tech Blue on White)
- **Charts**: Ensure pattern differentiation beyond color

### Font Sizes
- **Minimum Body Text**: 14pt (never smaller)
- **Minimum Caption**: 11pt

## Common Patterns

### Success Story
- Green accent bar on left
- Client logo (top left)
- Quote in Roboto Medium, 20pt
- Metrics highlighted in Success Green

### Problem/Solution
- Two-column layout
- Problem (left): Red accent
- Solution (right): Green accent
- Arrow between columns

### Roadmap/Timeline
- Horizontal timeline across slide
- Milestones marked with orange circles
- Past: Dark Gray, Future: Tech Blue

## Don'ts ❌

- ❌ Never distort the logo
- ❌ Never use colors outside the palette
- ❌ Never use fonts other than Roboto
- ❌ Never place text over busy backgrounds without overlay
- ❌ Never go below minimum font sizes
- ❌ Never ignore safe zones
- ❌ Never mix different border radius values
- ❌ Never use more than 3 font sizes per slide

## Review Checklist

Before finalizing any presentation:
- [ ] Logo present and correct on all slides
- [ ] All colors from approved palette
- [ ] Font hierarchy consistent
- [ ] Sufficient whitespace
- [ ] No text cutoffs
- [ ] Readable contrast ratios
- [ ] Aligned to grid system
- [ ] Page numbers present (except title slide)
```

---


