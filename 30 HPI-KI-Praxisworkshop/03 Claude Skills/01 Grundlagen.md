# 🎯 Claude Skills - Einfach erklärt

**Für HR-Profis in der Krankenversicherung**

---

## 💡 Was sind Claude Skills?

Stellen Sie sich vor, Sie haben für jede wiederkehrende Aufgabe eine **perfekt vorbereitete Checkliste** - genau das sind Skills! Sie sind **wiederverwendbare Anleitungen**, die Claude automatisch verwendet, wenn Sie etwas Bestimmtes von ihm möchten.

### 🔄 Der Skills-Workflow

```
┌─────────────┐      ┌─────────────┐      ┌─────────────┐      ┌─────────────┐
│     👤      │      │     🤖      │      │     📚      │      │     ✨      │
│             │      │             │      │             │      │             │
│ Sie fragen  │  →   │   Claude    │  →   │ Skill lädt  │  →   │  Ergebnis   │
│             │      │  erkennt    │      │    Ihre     │      │             │
│  "Erstelle  │      │ relevantes  │      │  Vorlagen   │      │  Perfekt    │
│ Stellen-    │      │    Skill    │      │             │      │ formatiert! │
│  anzeige"   │      │             │      │             │      │             │
└─────────────┘      └─────────────┘      └─────────────┘      └─────────────┘
```

---

## 🏗️ Skill-Struktur (vereinfacht)

```
📁 Meine Skills/
├── 📄 Stellenanzeigen-Skill/
│   └── SKILL.md (Ihre Regeln & Vorlagen)
│
├── 📄 Bewerber-Antwort-Skill/
│   └── SKILL.md (Ihre E-Mail-Vorlagen)
│
└── 📄 Onboarding-Skill/
    └── SKILL.md (Ihre Checklisten)
```

**Wichtig:** Skills sind einfache Textdateien (Markdown), die Ihre Regeln, Vorlagen und Best Practices enthalten.

---

## 🎯 Vorteile für HR in Krankenkassen

### ⚡ Zeitersparnis
Keine wiederholten Anweisungen mehr. Claude kennt Ihre Standards automatisch.

### 🎨 Konsistenz
Alle Texte folgen Ihrem Corporate Design und Ihrer Tonalität.

### 🔄 Wiederverwendbar
Einmal erstellt, in jedem Chat nutzbar - kein Copy & Paste mehr.

### 👥 Team-fähig
Teilen Sie Best Practices mit Kollegen durch Skills.

---

## 💼 Praktische Beispiele für Ihr HR-Marketing

### 📝 Beispiel 1: Stellenanzeigen-Skill

**Sie erstellen ein Skill mit Ihren Vorgaben:**

- ✅ Firmen-Tonalität (z.B. "Du" oder "Sie")
- ✅ Pflichtangaben für Krankenkassen
- ✅ Corporate Design-Elemente
- ✅ Gesetzliche Anforderungen (AGG-konform)
- ✅ Benefits-Struktur

**Ergebnis:** Sie sagen nur "Erstelle Stellenanzeige für Sachbearbeiter" - Claude nutzt automatisch Ihr Skill!

---

### 📧 Beispiel 2: Bewerber-Kommunikations-Skill

**Einmalige Definition Ihrer E-Mail-Standards:**

- ✅ Empathischer, wertschätzender Ton
- ✅ Datenschutz-Hinweise
- ✅ Signatur-Format
- ✅ Nächste Schritte klar kommunizieren

---

### 📱 Beispiel 3: Social-Media-Recruiting-Skill

**Für LinkedIn, Instagram & Co.:**

- ✅ Passende Hashtags für Gesundheitswesen
- ✅ Zeichenlimits beachten
- ✅ Call-to-Action-Formulierungen
- ✅ Employer Branding-Richtlinien

---

## 🆚 Skills vs. normale Prompts

| Aspekt | ❌ Normale Prompts | ✅ Mit Skills |
|--------|-------------------|---------------|
| **Wiederverwendung** | Jedes Mal neu eingeben | Automatisch geladen |
| **Konsistenz** | Kann variieren | Immer gleicher Standard |
| **Teamarbeit** | Schwer teilbar | Einfach im Team nutzbar |
| **Aktualisierung** | Überall manuell ändern | Einmal ändern, überall aktiv |
| **Komplexität** | Begrenzt durch Nachrichtenlänge | Kann sehr umfangreich sein |

---

## 📊 Technische Details: Wie Skills funktionieren

```
┌────────────────────────────────────────────────────────────────┐
│                     Context Window (Ihr Chat)                   │
│                                                                  │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ Agent's System Prompt                                     │  │
│  │ ┌────┐ ┌────┐ ┌──────┐ ┌────┐ ┌────┐                    │  │
│  │ │big-│ │docx│ │nda-  │ │pdf │ │pptx│ ... weitere Skills │  │
│  │ │query│    │  │review│     │      │                      │  │
│  │ └────┘ └────┘ └──────┘ └────┘ └────┘                    │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                  │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ User: "Erstelle eine Stellenanzeige für..."             │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                  │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ Claude: ✓ Skill erkannt → Lade Stellenanzeigen-Skill    │  │
│  │                                                            │  │
│  │ Tool use: file_read("/mnt/skills/user/stellenanzeigen/   │  │
│  │                      SKILL.md")                           │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                  │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ Tool result: {...Inhalt des SKILL.md...}                 │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                  │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ Claude: [Generiert Antwort nach Skill-Vorgaben]          │  │
│  └──────────────────────────────────────────────────────────┘  │
└────────────────────────────────────────────────────────────────┘
```

### Der 7-Schritte-Prozess:

1. **Mount Points** - Skills liegen in `/mnt/skills/` (schreibgeschützt)
2. **Skill Discovery** - Claude scannt verfügbare Skills beim Chat-Start
3. **Metadata Parsing** - Jedes Skill hat ein `SKILL.md` mit Beschreibung
4. **Pattern Matching** - Claude erkennt, welches Skill relevant ist
5. **Dynamic Loading** - Claude lädt das passende SKILL.md
6. **Context Injection** - Skill-Anweisungen werden dem Kontext hinzugefügt
7. **Instruction Following** - Claude arbeitet nach den Skill-Vorgaben

---

## 🚀 Erste Schritte - So starten Sie:

### Schritt 1: Wiederkehrende Aufgabe identifizieren
z.B. Stellenanzeigen, Absagen, Einladungen zum Gespräch

### Schritt 2: Den "Skill Creator" nutzen
Claude hat einen eingebauten Assistenten, der Ihnen beim Erstellen hilft

**So aktivieren Sie den Skill Creator:**
1. Gehen Sie zu **Einstellungen** → **Capabilities** → **Skills**
2. Aktivieren Sie das Skill **"skill-creator"**
3. Klicken Sie auf **"Try in chat"**

### Schritt 3: Ihre Standards definieren
- Tonalität
- Format
- Pflichtangaben
- Corporate Identity

### Schritt 4: Skill hochladen
- Über **Einstellungen** → **Capabilities** → **Upload Skill**
- Dateiformat: `.skill` (wird vom Skill Creator erzeugt)

### Schritt 5: Testen und verfeinern
Probieren Sie es aus und passen Sie nach Bedarf an

---

## 💡 Profi-Tipp für Ihre Krankenkasse

### Erstellen Sie ein "Master-Recruiting-Skill"

Ein zentrales Skill mit allen wichtigen Infos über Ihre Krankenkasse:

```
╔════════════════════════════════════════════════════════════╗
║         📋 Master-Recruiting-Skill Inhalt                  ║
╠════════════════════════════════════════════════════════════╣
║                                                            ║
║  🏢 Unternehmenswerte                                      ║
║     → Patientenorientierung, Verlässlichkeit, Innovation  ║
║                                                            ║
║  💎 Benefits                                               ║
║     → Betriebliche Altersvorsorge                         ║
║     → 30 Tage Urlaub + Sonderurlaub                       ║
║     → Weiterbildungsbudget €1.500/Jahr                    ║
║     → Mobiles Arbeiten (60% Remote möglich)               ║
║                                                            ║
║  📍 Standorte und Teams                                    ║
║     → Hauptsitz in [Stadt]                                ║
║     → Regionalzentren in [Städte]                         ║
║     → 5.000+ Mitarbeitende                                ║
║                                                            ║
║  📈 Karrierepfade im Gesundheitswesen                      ║
║     → Einstieg → Specialist → Senior → Team Lead          ║
║                                                            ║
║  ⭐ Besonderheiten Ihrer Kasse                             ║
║     → Spezialisierung auf [Bereich]                       ║
║     → Auszeichnungen [Liste]                              ║
║     → Innovationsprojekte [Beispiele]                     ║
║                                                            ║
╚════════════════════════════════════════════════════════════╝
```

→ Claude kann dann **jede Recruiting-Aufgabe** mit diesem Hintergrundwissen bearbeiten!

---


### Wann Skills sinnvoll sind:

✅ **Web UI Umgebung** (kein API-Zugriff)  
✅ **Häufig wechselnde Anforderungen** (Skills sofort aktualisierbar)  
✅ **Team-Kollaboration** (Skills sind teilbare Dateien)  
✅ **Multiple Spezial-Kontexte** (verschiedene Skills pro Aufgabe)  
✅ **Deterministische Ausgabestruktur** (Skills erzwingen Templates)

### Wann Skills NICHT die richtige Wahl sind:

❌ **API-Aufrufe mit hoher Frequenz** (System Prompts sind schneller)  
❌ **Dynamisches Verhalten basierend auf Runtime-State** (Skills sind statisch)  
❌ **Komplexe Logik mit Bedingungen** (Skills haben keine Programmierung)  
❌ **Secrets oder Credentials** (Skills sind von Claude lesbar)  
❌ **Echtzeit-Datenzugriff** (Skills können keine APIs aufrufen)

### Gemessener Overhead (Claude Sonnet 4.5):

- **Skill Loading:** 80-150ms Durchschnitt
- **Context Consumption:** 200-2.000 Tokens je nach Skill-Größe
- **Pattern Matching:** ~20-40ms (vernachlässigbar)
- **Total Latency Impact:** 100-190ms pro geladenem Skill

---

## 🛠️ Skill-Erstellung: Schritt-für-Schritt

### Option A: Mit dem Skill Creator (Empfohlen für Anfänger)

```
Sie: "Hey Claude - ich habe den skill-creator aktiviert. 
     Erstelle mir ein Skill für Stellenanzeigen."

Claude: [Stellt Ihnen Fragen zu Ihren Anforderungen]

Sie: [Beantworten die Fragen]

Claude: [Erstellt das Skill und bietet Download an]
```

### Option B: Manuell erstellen (Für Fortgeschrittene)

**Dateistruktur:**
```markdown
---
name: stellenanzeigen-skill
description: Erstellt professionelle Stellenanzeigen für eine gesetzliche 
             Krankenkasse nach Corporate Design und rechtlichen Vorgaben
---

# Stellenanzeigen-Skill für [Ihre Krankenkasse]

## Tonalität
- Verwende die "Sie"-Form (professionell, aber wertschätzend)
- Zeige Wertschätzung für Bewerbende
- Betone soziale Verantwortung im Gesundheitswesen

## Pflichtangaben
- AGG-konforme Formulierungen
- Standort und Vertragsart
- Bewerbungsfrist
- Ansprechpartner mit Kontaktdaten

## Struktur
1. Einleitung (2-3 Sätze über die Kasse)
2. Ihre Aufgaben (5-7 Bullet Points)
3. Ihr Profil (5-7 Bullet Points)
4. Wir bieten (Benefits)
5. Bewerbungshinweise

## Benefits (immer einbauen)
- Betriebliche Altersvorsorge
- 30 Tage Urlaub
- Fortbildungsbudget
- Mobiles Arbeiten
- Gesundheitsmanagement
- Jobticket

## Beispiel-Formulierungen
- "Gestalten Sie mit uns die Zukunft der Gesundheitsversorgung"
- "Wir schätzen Vielfalt und fördern Chancengleichheit"
- "Ihre Work-Life-Balance liegt uns am Herzen"
```

---

## 🎯 Konkrete Skill-Ideen für Ihre HR-Arbeit

### 1. 📝 Stellenanzeigen-Skill
**Trigger:** "Erstelle Stellenanzeige", "Jobposting für..."

**Inhalt:**
- Corporate Tonalität
- Benefits-Liste
- AGG-Konformität
- Formatierung
- Call-to-Action

---

### 2. 📧 E-Mail-Templates-Skill
**Trigger:** "Schreibe E-Mail an Bewerber", "Einladung Vorstellungsgespräch"

**Varianten:**
- Eingangsbestätigung
- Einladung zum Interview
- Absage nach Bewerbung
- Absage nach Interview
- Zusage
- Onboarding-Info

---

### 3. 📱 Social Media Recruiting-Skill
**Trigger:** "LinkedIn Post", "Instagram Story", "Social Media Kampagne"

**Plattform-spezifisch:**
- LinkedIn (1.300 Zeichen)
- Instagram (Caption + Hashtags)
- Facebook (lokale Zielgruppen)
- Xing (Businessnetzwerk)

---

### 4. 📊 Candidate Persona-Skill
**Trigger:** "Zielgruppe analysieren", "Candidate Persona"

**Analysiert:**
- Demografische Daten
- Motivationen
- Karriereziele
- Anforderungen an Arbeitgeber

---

### 5. 🎤 Interview-Leitfaden-Skill
**Trigger:** "Erstelle Interview-Fragen", "Gesprächsleitfaden"

**Generiert:**
- Strukturierte Fragen
- Kompetenzbereiche
- Bewertungskriterien
- AGG-konforme Formulierungen

---

## 📈 Best Practices für Skills

### DO's ✅

- **Spezifisch sein:** Je detaillierter, desto besser die Ergebnisse
- **Beispiele einbauen:** Zeigen Sie konkrete Formulierungen
- **Regelmäßig aktualisieren:** Skills leben von Aktualität
- **Im Team teilen:** Kollegen profitieren von Ihren Skills
- **Testen:** Probieren Sie das Skill aus und verfeinern Sie es

### DON'Ts ❌

- **Zu generisch:** "Schreibe professionell" ist zu vage
- **Sensible Daten:** Keine Passwörter oder persönliche Infos
- **Zu komplex:** Lieber mehrere kleine Skills als ein riesiges
- **Widersprüche:** Achten Sie auf konsistente Anweisungen
- **Rechtsunsicherheit:** Lassen Sie rechtliche Texte prüfen

---

## 🔍 Troubleshooting

### Problem: Skill wird nicht automatisch geladen

**Lösung:**
1. Prüfen Sie die `description` im SKILL.md - ist sie aussagekräftig?
2. Verwenden Sie eindeutige Trigger-Begriffe in Ihrer Anfrage
3. Erwähnen Sie das Skill explizit: "Nutze mein Stellenanzeigen-Skill"

---

### Problem: Ergebnisse entsprechen nicht den Erwartungen

**Lösung:**
1. Fügen Sie mehr Beispiele ins Skill ein
2. Formulieren Sie Anweisungen klarer und direkter
3. Nutzen Sie Listen und Strukturen statt Fließtext
4. Testen Sie verschiedene Formulierungen

---

### Problem: Skill ist zu lang / verbraucht zu viele Tokens

**Lösung:**
1. Teilen Sie das Skill in mehrere kleinere auf
2. Entfernen Sie redundante Informationen
3. Nutzen Sie prägnante Formulierungen
4. Überlegen Sie, ob alle Infos wirklich nötig sind

---

## 🎓 Weiterführende Ressourcen

### Offizielle Dokumentation
- [Claude Skills Documentation](https://docs.anthropic.com/claude/docs/skills)
- [Skill Creator Guide](https://docs.anthropic.com/claude/docs/skill-creator)

### Community
- Claude Skills Beispiele auf GitHub
- HR Tech & AI Communities auf LinkedIn
- Fachgruppen für KI in der Personalabteilung

---

## 📋 Zusammenfassung

### Skills in einem Satz:
**Skills sind wiederverwendbare Wissensbausteine, die Claude automatisch lädt, wenn Sie relevante Aufgaben stellen.**

### Die 5 wichtigsten Vorteile:

1. ⚡ **Zeitersparnis** - Keine wiederholten Anweisungen
2. 🎯 **Konsistenz** - Immer gleiche Qualität
3. 👥 **Teamwork** - Teilbar und gemeinsam nutzbar
4. 🔄 **Wartbarkeit** - Zentral aktualisierbar
5. 📊 **Skalierbar** - Beliebig viele Skills kombinierbar

### Ihre nächsten Schritte:

```
┌─────────────────────────────────────────────────┐
│ 1️⃣  Skill Creator aktivieren                    │
│                                                  │
│ 2️⃣  Erstes Skill erstellen                      │
│     (z.B. Stellenanzeigen)                      │
│                                                  │
│ 3️⃣  Testen und verfeinern                       │
│                                                  │
│ 4️⃣  Mit Team teilen                             │
│                                                  │
│ 5️⃣  Weitere Skills aufbauen                     │
│     (E-Mail, Social Media, etc.)                │
└─────────────────────────────────────────────────┘
```

---

## 🎉 Fazit

**Skills verwandeln Claude in Ihren persönlichen, perfekt eingearbeiteten HR-Assistenten!**

Statt bei jeder Anfrage alle Details zu erklären, haben Sie einen digitalen Kollegen, der Ihre Standards, Ihre Tonalität und Ihre Anforderungen bereits kennt.

Für HR-Profis in Krankenkassen bedeutet das:
- ✅ Schnellere Stellenbesetzung durch effizientere Prozesse
- ✅ Konsistentes Employer Branding über alle Kanäle
- ✅ Mehr Zeit für strategische Aufgaben statt Routinearbeit
- ✅ Professionelle Kandidaten-Experience in jeder Phase

---

