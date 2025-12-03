# BMAD System - Vollständige Nutzungsanleitung

## 📋 Überblick

BMAD (Build, Make, Analyze, Design) ist ein KI-gestütztes Framework mit virtuellen Experten-Agenten für professionelle Softwareentwicklungsprozesse. Das System bietet spezialisierte KI-Personas, die verschiedene Rollen im Entwicklungsprozess übernehmen.

## 🎭 Verfügbare Agenten

Du hast **7 XML-Dateien** hochgeladen:

### Einzelne Agenten (6 Dateien)

1. **📊 Mary - Business Analyst** (`analyst.xml`)
   - Strategische Geschäftsanalyse & Requirements-Engineering
   - Marktforschung, Wettbewerbsanalyse, Anforderungsermittlung
   
2. **🏗️ Winston - Architect** (`architect.xml`)
   - System-Architektur & Technisches Design
   - Verteilte Systeme, Cloud-Infrastruktur, API-Design
   
3. **📋 John - Product Manager** (`pm.xml`)
   - Produktstrategie & Marktanalyse
   - Priorisierung, Business Impact, User Insights
   
4. **🏃 Bob - Scrum Master** (`sm.xml`)
   - Agile Prozesse & Story-Vorbereitung
   - Sprint-Planning, User Stories, Developer-Ready Specs
   
5. **📚 Paige - Technical Writer** (`tech-writer.xml`)
   - Technische Dokumentation
   - CommonMark, DITA, OpenAPI, strukturierte Dokumentation
   
6. **🎨 Sally - UX Designer** (`ux-designer.xml`)
   - User Experience & UI Design
   - User Research, Interaction Design, Prototyping

### Team-Bundle (1 Datei)

7. **🎭 Team Fullstack** (`team-fullstack.xml`)
   - Enthält ALLE Agenten in einer Datei
   - BMad Orchestrator als Master-Agent
   - Ermöglicht Wechsel zwischen Agenten

---

## 🚀 Verwendung

### Option 1: Einzelnen Agenten verwenden

**Schritt-für-Schritt:**

1. **Agent auswählen**
   - Lade die entsprechende XML-Datei hoch (z.B. `analyst.xml`)
   
2. **Agent aktivieren**
   - Sende die Nachricht: "Aktiviere den Agenten aus dieser XML-Datei"
   - Der Agent stellt sich vor und zeigt sein Menü

3. **Mit Befehlen arbeiten**
   - Wähle eine Nummer aus dem Menü ODER
   - Gib den Befehlsnamen ein (z.B. `*brainstorm-project`)

4. **Workflows ausführen**
   - Folge den Anweisungen des Agenten
   - Beantworte Fragen, wenn der Agent innehält
   - Der Agent führt dich durch den kompletten Workflow

5. **Beenden**
   - Gib `*exit` ein, um den Agenten zu verlassen

**Beispiel:**
```
User: Aktiviere Mary, die Business Analyst
Agent: Hallo! Ich bin Mary, deine Business Analyst...
       1. *help - Menü anzeigen
       2. *brainstorm-project - Geführtes Brainstorming
       3. *research - Geführte Recherche
       ...
User: 2
Agent: [Startet Brainstorming-Workflow]
```

---

### Option 2: Team-Bundle verwenden (Empfohlen!)

Das Team-Bundle ist die **mächtigste Option**, da es alle Agenten vereint.

**Schritt-für-Schritt:**

1. **Team-Bundle laden**
   - Lade `team-fullstack.xml` hoch
   
2. **Orchestrator aktivieren**
   - Sende: "Aktiviere den BMad Orchestrator"
   - Der Orchestrator begrüßt dich mit dem Hauptmenü

3. **Agenten auflisten**
   - Befehl: `*list-agents`
   - Zeigt alle verfügbaren Agenten mit Beschreibungen

4. **Zu einem Agenten wechseln**
   - Befehl: `*agents [name]` (z.B. `*agents analyst`)
   - Der Orchestrator transformiert sich in diesen Agenten
   - Du arbeitest dann direkt mit diesem Agenten

5. **Zwischen Agenten wechseln**
   - `*exit` - Zurück zum Orchestrator
   - Dann `*agents [anderer-name]` - Zu einem anderen Agenten wechseln

6. **Party Mode** 🎉
   - Einige Agenten bieten `*party-mode`
   - Bringt mehrere Agenten zusammen für kollaborative Diskussionen

**Beispiel:**
```
User: Aktiviere den BMad Orchestrator
Orchestrator: Willkommen! Ich bin der BMad Orchestrator...
              1. *agents [name] - Zu einem Agenten wechseln
              2. *list-agents - Alle Agenten anzeigen
              ...
User: *list-agents
Orchestrator: [Zeigt alle 6+ Agenten]
User: *agents analyst
Mary (Analyst): Hallo! Ich bin Mary...
User: *brainstorm-project
Mary: [Startet Workflow]
User: *exit
Mary: Bestätigung...
Orchestrator: Wieder zurück beim Orchestrator
User: *agents architect
Winston: Hallo! Ich bin Winston...
```

---

## 🎯 Typische Workflows

### 1. Projekt-Konzeption
```
analyst.xml → *brainstorm-project
           → *research
           → *product-brief
```

### 2. Technisches Design
```
architect.xml → Architektur-Workflows
             → API-Design
             → Technologie-Auswahl
```

### 3. Sprint-Planning
```
pm.xml → Anforderungen definieren
      ↓
sm.xml → User Stories erstellen
      → Story-Vorbereitung
```

### 4. Dokumentation
```
tech-writer.xml → API-Dokumentation
               → Benutzerhandbücher
               → Technische Spezifikationen
```

### 5. UX-Design
```
ux-designer.xml → User Research
               → Wireframes
               → Prototyping
```

---

## 💡 Wichtige Befehle

### Universal (alle Agenten)
- `*help` - Menü anzeigen
- `*exit` - Agent verlassen / zurück zum Orchestrator

### Orchestrator (nur team-fullstack.xml)
- `*list-agents` - Alle Agenten auflisten
- `*agents [name]` - Zu einem Agenten wechseln

### Häufige Workflow-Befehle
- `*brainstorm-project` - Geführtes Brainstorming
- `*research` - Strukturierte Recherche
- `*product-brief` - Produktbeschreibung erstellen
- `*party-mode` - Mehrere Agenten zusammenbringen
- `*advanced-elicitation` - Erweiterte Fragetechniken

---

## 🔥 Best Practices

### 1. Wähle den richtigen Agenten
- **Frühphase**: Business Analyst oder Product Manager
- **Planung**: Architect oder Product Manager
- **Umsetzung**: Scrum Master
- **Dokumentation**: Technical Writer
- **Design**: UX Designer

### 2. Nutze die Workflows
- Alle Agenten haben vorgefertigte Workflows
- Lass dich vom Agenten durch den Prozess führen
- Beantworte Fragen vollständig für beste Ergebnisse

### 3. Party Mode für komplexe Entscheidungen
- Nutze `*party-mode` für multi-perspektivische Diskussionen
- Mehrere Experten diskutieren dein Thema
- Verschiedene Sichtweisen werden berücksichtigt

### 4. Team-Bundle vs. Einzelagenten
- **Team-Bundle**: Für komplexe Projekte mit mehreren Phasen
- **Einzelagenten**: Für fokussierte, spezifische Aufgaben

### 5. Kontext mitführen
- Agenten haben keine Erinnerung zwischen Sessions
- Fasse wichtige Entscheidungen zusammen
- Referenziere frühere Outputs wenn nötig

---

## 🛠️ Technische Details

### Dateistruktur
Jede XML-Datei ist ein "Agent Bundle" mit:
- **Agent-Definition**: Rolle, Persona, Kommunikationsstil
- **Aktivierungsschritte**: Wie der Agent startet
- **Menü**: Verfügbare Befehle
- **Gebündelte Dateien**: Workflows, Templates, Tasks (in CDATA)
- **Agent-Manifest**: Liste aller verfügbaren Agenten

### Workflow-Ausführung
1. Agent lädt das Bundle
2. Zeigt Menü an
3. Wartet auf Benutzereingabe
4. Führt Workflow Schritt für Schritt aus
5. Speichert Outputs nach jedem Schritt

### Menu-Handler
- `workflow="..."` - Führt einen Workflow aus
- `exec="..."` - Führt eine Aufgabe aus
- `tmpl="..."` - Verwendet ein Template
- `action="..."` - Führt eine direkte Aktion aus

---

## 📊 Beispiel-Projektablauf

```
Phase 1: Konzeption
  ├─ Business Analyst: Brainstorming & Research
  └─ Product Manager: Product Brief erstellen

Phase 2: Design
  ├─ UX Designer: User Flows & Wireframes
  └─ Architect: Technische Architektur

Phase 3: Planung
  ├─ Product Manager: Feature-Priorisierung
  └─ Scrum Master: Sprint Planning & Stories

Phase 4: Dokumentation
  └─ Technical Writer: Dokumentation erstellen
```

---

## ⚡ Quick Start

**Für schnellen Einstieg:**

1. Lade `team-fullstack.xml` hoch
2. Sende: "Aktiviere den BMad Orchestrator"
3. Sende: `*list-agents` um Optionen zu sehen
4. Sende: `*agents analyst` um zu starten
5. Folge dem Menü des Agenten

**Oder für fokussierte Arbeit:**

1. Lade einen einzelnen Agent hoch (z.B. `analyst.xml`)
2. Sende: "Aktiviere den Agenten"
3. Folge dem Menü

---

## 🎓 Tipp für optimale Nutzung

Die Agenten funktionieren am besten, wenn du:
- **Konkret** bist in deinen Antworten
- **Vollständig** Kontext lieferst
- Den **Workflows folgst** statt Abkürzungen zu nehmen
- **Fragen beantwortest** wenn der Agent innehält
- **Iterativ arbeitest** - mehrere Durchläufe sind normal

---

## 📞 Support & Weiterentwicklung

Das BMAD-System ist modular aufgebaut:
- Jeder Agent kann unabhängig aktualisiert werden
- Neue Agenten können hinzugefügt werden
- Workflows können angepasst werden
- Das System lernt aus jeder Interaktion

---

**Viel Erfolg mit deinem BMAD-System!** 🚀

Bei Fragen aktiviere einfach einen Agenten und lass dich durch den Prozess führen. Die Agenten sind darauf trainiert, hilfreiche, strukturierte Unterstützung zu bieten.
