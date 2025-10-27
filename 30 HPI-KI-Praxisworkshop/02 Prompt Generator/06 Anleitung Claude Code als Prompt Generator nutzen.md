

```markdown
# 🤖 Anleitung: Automatisierte Prompt-Erstellung in Claude Code

## 🧩 Ziel

Mit diesem Setup erzeugst du **vollautomatisch komplette KI-Prompt-Bibliotheken**, basierend auf:
- einer vorhandenen **Recherche-Datei (.md)** (z. B. mit deinem Fachwissen oder Projektdaten),
- und einem **Masterprompt**, der alle Schritte und Strukturen der Generierung definiert.

Das Ergebnis ist eine fertige **AI Prompt Suite** mit:
✅ Prompts für Text, Bild, Video & Audio  
✅ Projektstruktur & Dokumentation  
✅ Integrationsempfehlungen & Kostenübersichten  

---

## ⚙️ Voraussetzungen

- Du arbeitest in **Claude Code**.  
- In deinem Projektordner befindet sich bereits eine **Recherche-Datei** (z. B. `prompt_research.md`).  
- Du hast den vollständigen **Masterprompt** (der große XML-artige Codeblock mit `<system>` bis `</business_context_instructions>`).  

---

## 🚀 Schritt-für-Schritt-Anleitung

### **Schritt 1: Projekt vorbereiten**
1. Öffne deinen Claude-Code-Projektordner.  
2. Stelle sicher, dass deine Recherchedatei vorhanden ist, z. B.:

```

/mein-projekt/
├── prompt_research.md
└── assets/

```

---

### **Schritt 2: Initialisierung**
1. Tippe in Claude Code:
```

/init

```
2. Claude erstellt automatisch eine neue Datei:
```

.claude.md

````
Diese Datei dient als **Projektsteuerung** und speichert den Systemzustand für deine Generierung.

---

### **Schritt 3: Masterprompt einfügen**
1. Öffne die Datei `.claude.md`.  
2. **Kopiere den vollständigen Masterprompt** (den XML-Block mit `<system> ... </business_context_instructions>`) hinein.  
3. Speichere die Datei.

💡 Der Masterprompt enthält alle definierten Phasen:  
Business-Analyse → Ordneraufbau → Prompt-Generierung → Dokumentation → Optimierung.  
Er ist das „Bauplan-Skript“, das Claude nutzt, um automatisch dein Projekt zu erzeugen.

---

### **Schritt 4: Business Context eingeben**
Direkt **nachdem du den Masterprompt eingefügt hast**, gib unten in der Claude-Code-Konsole deinen **Business-Kontext** ein.  
Beispiel:

```text
Business Context:
Wir sind ein Designstudio, das KI nutzen möchte, um Markenbilder, Social-Media-Videos und Sprachassistenten zu entwickeln. 
Unser Ziel ist es, kreative Prozesse zu automatisieren und den Content-Ausstoß zu verdoppeln.
````

Sobald du das eingibst, beginnt Claude automatisch mit der **Ausführung des Plans** aus dem Masterprompt.

---

## 🔄 Was Claude jetzt automatisch macht

Claude führt alle Phasen deines Masterprompts aus:

| Phase                    | Aufgabe                                                           |
| ------------------------ | ----------------------------------------------------------------- |
| 🧠 **business_analysis** | Analysiert dein Unternehmen, erkennt Potenziale & KI-Anwendungen  |
| 🗂️ **folder_creation**  | Erstellt automatisch eine saubere Ordnerstruktur für alle Prompts |
| 🪄 **prompt_generation** | Generiert 40 + Prompts (Text, Bild, Video, Voice)                 |
| 🧾 **documentation**     | Erstellt README, Best-Practices & Vergleichstabellen              |
| ⚙️ **optimization**      | Optimiert alle Prompts auf Kosten, Effizienz & Modellqualität     |

---

## 📦 Ergebnis

Nach Abschluss findest du im Projektordner eine vollständige Struktur:

```
ai-prompt-suite/
├── README.md
├── text-generation/
│   ├── daily-operations/
│   ├── content-creation/
│   ├── analysis-research/
│   └── customer-communication/
├── image-generation/
│   ├── marketing-collateral/
│   ├── brand-assets/
│   └── educational-content/
├── video-generation/
│   ├── social-media/
│   └── product-demos/
├── voice-agents/
│   ├── customer-service/
│   └── appointment-booking/
└── implementation/
    ├── quick-start.md
    ├── platform-comparison.md
    ├── best-practices.md
    └── troubleshooting.md
```

In diesen Ordnern findest du:

* 🧩 **Fertige Prompts** mit Parametern, Beispielen & Modellvorschlägen
* ⚙️ **Dokumentationen** mit Setup- und Integrationstipps
* 💬 **Anleitungen zur Nutzung und Optimierung**

---

## 💡 Wie du die Ergebnisse nutzt

### 🔸 Text-Prompts

→ Direkt für **GPT-5**, **Claude 4** oder ähnliche Modelle einsetzen:

* Marketingtexte
* E-Mails
* Analysen & Automatisierungen

### 🔸 Bild-Prompts

→ Verwende sie mit **Nano Banana (Gemini 2.5 Flash Image)** oder **GPT-4o**:

* Markenbilder, Grafiken, Social-Assets
* Stilvorlagen & Design-Iterationen

### 🔸 Video-Prompts

→ Nutze sie mit **Veo 3 / 3.1** oder **Sora Turbo**:

* Storyboards, Motion-Design, Produktvideos

### 🔸 Voice-Prompts

→ Implementiere sie in **VAPI**, **Retell**, **OpenAI Realtime** oder **ElevenLabs** für:

* Sprachassistenten, Telefonbots, Schulungsanwendungen

---

## 📈 Warum das sinnvoll ist

| Vorteil             | Nutzen                                                        |
| ------------------- | ------------------------------------------------------------- |
| **Automatisiert**   | Spart enorme Zeit bei der Prompt-Erstellung                   |
| **Konsistent**      | Einheitliche Struktur & Formatierung über alle Plattformen    |
| **Skalierbar**      | Für jedes Unternehmen oder Projekt wiederverwendbar           |
| **Produktionsreif** | Jeder Prompt ist direkt einsatzfähig                          |
| **Lernfördernd**    | Du erkennst, wie professionelle Prompt-Systeme aufgebaut sind |

---

## 🧰 Zusammenfassung

| Schritt | Aktion                    | Ergebnis                                  |
| ------- | ------------------------- | ----------------------------------------- |
| 1       | Projekt öffnen            | Zugriff auf Recherchedatei                |
| 2       | `/init` ausführen         | Erstellt `.claude.md`                     |
| 3       | Masterprompt einfügen     | Definiert Automatisierungsplan            |
| 4       | Business Context eingeben | Startet Generierung                       |
| 5       | Ergebnisse prüfen         | Fertige Prompt-Bibliothek & Dokumentation |

---

## 🧠 Tipp für Einsteiger

> „Du bringst das Wissen (Recherchedatei) und den Bauplan (Masterprompt) –
> Claude baut daraus automatisch eine komplette, produktionsreife KI-Prompt-Bibliothek.“

---

## ✅ Endergebnis

Nach Abschluss besitzt du:

* Über **40 fertige KI-Prompts** für Text, Bild, Video & Audio
* Eine vollständige, dokumentierte **Projektstruktur**
* **Best Practices & Integrationshilfen**
* Eine solide Grundlage für deine eigene KI-Strategie

---

```

---

```

