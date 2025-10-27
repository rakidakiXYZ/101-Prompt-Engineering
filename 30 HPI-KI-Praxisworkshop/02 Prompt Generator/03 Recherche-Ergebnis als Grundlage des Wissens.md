1️⃣ Was du mit dem *Recherche-Prompt* machst
2️⃣ Was das *Ergebnis* ist
3️⃣ Wie du dieses *Ergebnis weiterverwendest*, um daraus konkrete **Prompt-Vorlagen für Bild- und Videogenerierung** (z. B. für Gemini Nano Banana & Veo) zu entwickeln

---

````markdown
# 🧭 Anleitung: Wie du den Recherche-Prompt nutzt & daraus Vorlagen entwickelst

## 🧩 1. Ziel des Recherche-Prompts

Der **Recherche-Prompt** ist kein Produktionsprompt (er generiert keine Bilder oder Videos direkt),  
sondern ein **Wissens- und Analysewerkzeug**.

➡️ Er dient dazu, dass die KI **alle verfügbaren Prompt-Engineering-Techniken** für Gemini-Modelle (Nano Banana & Veo) recherchiert, analysiert und systematisch zusammenfasst.

**Kurz gesagt:**  
Du nutzt ihn, um dir ein *Expertenwissen-Fundament* zu bauen, bevor du eigene Prompts schreibst.

---

## 🔍 2. Wie du den Prompt einsetzt

### Schritt-für-Schritt:
1. **Kopiere den gesamten Recherche-Prompt** (den Masterprompt aus der vorherigen Antwort).  
2. **Füge ihn in ein KI-System** ein, das webfähige Recherche oder modellbezogene Daten auswerten kann  
   (z. B. Gemini 2.5, GPT-5 mit Webzugriff, Claude, etc.).  
3. **Starte die Abfrage** unverändert — keine zusätzlichen Parameter nötig.  
4. **Warte auf die strukturierte Ausgabe**, die wie folgt aufgebaut ist:
   - Kurzübersicht  
   - Techniken (mit Beschreibung, Beispiel, Tipps)  
   - Top 10 Tipps  
   - Checkliste

---

## 📊 3. Was du als Ergebnis erhältst

Die Ausgabe ist eine **strukturierte Wissensbasis** zum Thema *Prompt-Engineering* für:

- 🖼️ **Nano Banana (Gemini Image Flash)** → Bildgenerierung & Bildbearbeitung  
- 🎬 **Veo 3.1** → Videogenerierung  

Typischer Aufbau der Ergebnisse:
| Technik | Beschreibung | Beispiel | Anwendung | Tipps & Limitationen |
|----------|---------------|-----------|------------|----------------------|
| Chain-of-Thought | Schrittweise Gedankenstrukturierung | „Erstelle zuerst Konzept, dann Szene“ | Storyboards für Veo | Präzise Zeitangaben notwendig |
| Style Conditioning | Stilsteuerung über Referenzbilder | „im Stil von Ukiyo-e“ | Nano Banana | Farb- und Texturabgleich beachten |

➡️ Das ist dein **Rohmaterial für eigene Prompt-Vorlagen**.

---

## 🧠 4. Wie du das Ergebnis weiterverwendest

### A. Erstelle **Explizite Prompt-Vorlagen**
Nutze die recherchierten Techniken, um **funktionierende, wiederverwendbare Prompt-Templates** zu entwickeln.

#### Beispiel: *Bildgenerierung mit Nano Banana*
```text
Prompt-Struktur:
[Thema] im Stil von [Künstler/Bewegung], mit [Stimmung/Licht], Fokus auf [Objekt/Detail],
verwende Parameter [Auflösung, Format, Farbton].

Beispiel:
Ein futuristisches Stadtporträt bei Nacht, im Stil von Syd Mead,
neonfarben, reflektierende Straßen, Fokus auf Architektur — 16:9, UHD.
````

#### Beispiel: *Videogenerierung mit Veo 3.1*

```text
Prompt-Struktur:
[Szene] zeigt [Aktion/Bewegung] in [Umgebung],
Kameraperspektive [Typ], Beleuchtung [Art], Dauer [x Sekunden],
mit optionalem [Audio/Voice/Transition].

Beispiel:
Eine Kamerafahrt über ein Regenwald-Tal bei Sonnenaufgang,
Vögel fliegen, Nebel steigt, sanft orchestraler Soundtrack, 8 Sekunden.
```

---

### B. Erstelle **eigene Prompt-Bibliotheken**

* Sammle erfolgreiche Beispiele in Kategorien:

  * 🔹 Porträt / Charakter / Umgebung / Stil
  * 🔹 Bewegung / Übergang / Kameraperspektive
* Ergänze bei jedem Prompt:

  * Zielmodell (Nano Banana oder Veo 3.1)
  * Effekt / Technik / Parameter

Beispiel-Ordnerstruktur:

```
/Prompts/
 ├── Image/
 │    ├── Style_Transfer.md
 │    ├── Lighting_Control.md
 └── Video/
      ├── Scene_Transitions.md
      ├── Camera_Motion.md
```

---

## 🧩 5. Bonus: Iterativer Workflow

1. **Führe den Recherche-Prompt aus.**
2. **Analysiere die besten Techniken.**
3. **Erstelle 3–5 Vorlagen basierend auf diesen Techniken.**
4. **Teste sie im Modell (Nano Banana / Veo).**
5. **Verbessere sie iterativ anhand der Modellreaktionen.**

🔁 So baust du dir über Zeit eine **eigene Prompt-Bibliothek**, die immer besser funktioniert.

---

## ✅ Fazit

Mit dem Recherche-Prompt:

* bekommst du **fundiertes Wissen über Prompting-Techniken**,
* lernst **modellgerechtes Formulieren**,
* und kannst daraus **effektive, wiederverwendbare Prompt-Vorlagen** für Bild- und Video-KI entwickeln.

---

```
