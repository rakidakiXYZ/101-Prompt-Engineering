````markdown
---
name: alis-brand-skill
description: Eine benutzerdefinierte Fähigkeit, die automatisch Markenrichtlinien aus der Datei „Brand Reference PPT.pptx“ analysiert und auf alle Präsentationen und Berichte anwendet, um visuelle Konsistenz sicherzustellen.
---

# Alis Brand Skill

Diese benutzerdefinierte Fähigkeit („Skill“) **muss** die Datei **„Brand Reference PPT.pptx“** analysieren, bevor sie Präsentationen oder Berichte erstellt, um **Markenkonsistenz** zu gewährleisten.

---

## **Anweisungen zur Ausführung des Skills**

Wenn dieser Skill ausgeführt wird, muss er **immer**:

1. Zuerst mit dem View-Tool die Datei **„Brand Reference PPT.pptx“** untersuchen, um den aktuellen **visuellen Stil**, das **Farbschema**, die **Layouts** und die **Formatierung** zu verstehen.  
2. Diese Stilmerkmale **exakt** auf alle erstellten Ergebnisse anwenden.  
3. Die **visuelle Hierarchie**, **Abstände** und **Designelemente** aus dem Referenzdeck übernehmen.

---

## **Marken-Visueller Stil**  
*(aus „Brand Reference PPT.pptx“ zu extrahieren)*

- Primär- und Akzentfarben aus dem Referenzdeck  
- Typografie-Stil und Hierarchie  
- Layoutmuster der Folien und Nutzung von Weißraum  
- Symbolstil und Behandlung visueller Elemente  
- Kopf-/Fußzeilenformatierung  
- Gesamtwirkung: Hochwertig, professionell, poliert

---

## **Foliendesign-Strukturen**  
*(gemäß Referenzdeck)*

- Format der Titelfolie  
- Layouts für Inhaltsfolien  
- Stil von Diagrammen und Flussdiagrammen  
- Gestaltung und Dichte von Aufzählungspunkten  
- Platzierung visueller Elemente

---

## **Kommunikationsprinzipien**

1. **Top-Down-Struktur:** Zuerst die Antwort, dann die Begründung.  
2. **Pyramidenprinzip:** Beginne mit der Schlussfolgerung, stütze sie mit Daten.  
3. **Prägnanz vor Vollständigkeit:** Auf den Punkt kommen, keine Fülltexte.  
4. **Handlungsorientiert:** Jeder Abschnitt soll zu Entscheidungen oder Empfehlungen führen.

---

## **Für PowerPoint-Präsentationen**

- **„Brand Reference PPT.pptx“** analysieren und Layoutmuster **genau replizieren**  
- **Eine zentrale Aussage pro Folie** (Foliëntitel = Kernaussage)  
- **Diagramme, Flussdiagramme und Prozessvisualisierungen** großzügig einsetzen  
- **Aufzählungspunkte minimieren:** maximal 3–5 pro Folie  
- **Visuelle Hierarchie:** Symbole, Farbflächen, verbindende Pfeile  
- **Farben, Schriftarten und Fußzeilenstil** exakt aus der Referenzdatei übernehmen

---

## **Für Word-Dokumente (Berichte)**

- **Executive Summary:** Maximal 1 Seite, mit Antwort + 3–5 Kernpunkten  
- **Struktur:** Klare Abschnittsüberschriften mit Nummerierung (z. B. 1., 1.1, 1.2)  
- **Visuals:** Tabellen und Diagramme als Bilder einfügen, wenn sie Klarheit schaffen  
- **Formatierung:** Professionell, sauber, farblich konsistent mit dem Referenzdeck  
- **Empfehlungen:** Stichpunktartig, spezifisch, umsetzbar

---

## **Inhaltlicher Ansatz**

- Beginne mit der Frage **„Und was bedeutet das?“** – warum ist es wichtig?  
- Nutze Daten und Frameworks zur Untermauerung von Aussagen  
- **Zeigen statt erzählen:** Diagramme bevorzugen statt Fließtext  
- **Jeder Abschnitt** endet mit klaren **Implikationen oder nächsten Schritten**

---

## **Kritisch Wichtig**

Bevor **irgendeine** Präsentation oder ein Bericht generiert wird, **muss** der Skill die Datei **„Brand Reference PPT.pptx“** analysieren, um den aktuellen Markenstil zu extrahieren und anzuwenden.  
Nur so wird die **visuelle Konsistenz mit der bestehenden Markenidentität** gewährleistet.

---

## **Formatierungsregeln**

Beim Erstellen von Claude-Skills muss die Datei **`SKILL.md`** mit einem YAML-Frontmatter beginnen, das folgende Felder enthält:

```yaml
---
name: alis-brand-skill
description: Automatisierte Anwendung von Markenrichtlinien auf Präsentationen und Berichte basierend auf der Datei „Brand Reference PPT.pptx“.
---
````

Danach folgt der oben beschriebene Markdown-Inhalt.

````markdown
# Anleitung zur Nutzung des Prompts für die **Volksbank Bühl**

Diese Anleitung erklärt, wie du den bestehenden Prompt für den **Alis Brand Skill** anpassen und für die **Volksbank Bühl** nutzen kannst. Ziel ist es, sicherzustellen, dass alle automatisch generierten Präsentationen oder Berichte das Corporate Design (CD) der Volksbank Bühl exakt einhalten.

---

## 🧭 **Ziel des Skills**

Der Skill soll:
- automatisch das Marken-Design der Volksbank Bühl übernehmen,  
- Präsentationen und Berichte im einheitlichen Stil erstellen,  
- Farben, Schriften, Layouts und Designelemente aus einer Referenzdatei verwenden.

---

## ⚙️ **Schritt-für-Schritt-Anleitung**

### **1. Brand Reference Datei vorbereiten**
- Erstelle oder exportiere eine **Referenzpräsentation** der Volksbank Bühl mit allen relevanten Markenelementen:
  - Primär- und Sekundärfarben  
  - Schriftarten und Textstile  
  - Logo-Positionierung  
  - Kopf- und Fußzeilen  
  - Beispiel-Folienlayouts  

- Speichere diese Datei unter dem Namen  
  **`Brand Reference PPT.pptx`**

Diese Datei dient als **Designquelle** für den Skill.

---

### **2. Prompt anpassen**

Kopiere den übersetzten Prompt (aus `Alis Brand Skill`) und ersetze folgende Angaben:

| Abschnitt | Was ändern? | Beispiel |
|------------|--------------|----------|
| **Skill-Name** | `alis-brand-skill` → `volksbank-buehl-skill` | `name: volksbank-buehl-skill` |
| **Beschreibung** | Beschreibe, dass dieser Skill für die Volksbank Bühl gedacht ist | `"description: Skill für Präsentationen und Berichte im Corporate Design der Volksbank Bühl"` |
| **Referenzdatei** | Stelle sicher, dass überall `Brand Reference PPT.pptx` referenziert wird | Belasse den Dateinamen gleich, oder passe ihn an, z. B. `Volksbank_Buehl_BrandDeck.pptx` |
| **Branding-Hinweise** | Füge spezifische Designregeln der Volksbank hinzu | z. B. Primärfarbe Blau (#004C97), Akzent Orange (#FF6600), Schrift: Arial Narrow |

---

### **3. Datei speichern**

Speichere den angepassten Text als  
**`SKILL.md`**

Achte darauf, dass die Datei mit dem YAML-Frontmatter beginnt:

```yaml
---
name: volksbank-buehl-skill
description: Skill für Präsentationen und Berichte im Corporate Design der Volksbank Bühl.
---
````

---

### **4. Skill in dein System integrieren**

1. Lege die Datei **`SKILL.md`** zusammen mit der **`Brand Reference PPT.pptx`** in ein ZIP-Archiv.
2. Benenne das Archiv z. B.
   **`volksbank-buehl-skill.zip`**
3. Lade das ZIP in dein Skill-System oder deine Plattform hoch (z. B. Claude, Alis oder ein internes Automatisierungstool).
4. Teste den Skill mit einem Beispielbefehl, etwa:

   > *„Erstelle eine Präsentation über unser neues Online-Banking-Angebot.“*

Der Skill wird automatisch:

* die Brand Reference Datei prüfen,
* das Layout und Farbschema übernehmen,
* und das Dokument im Volksbank Bühl Design ausgeben.

---

## 🧩 **Tipp für Erweiterungen**

Wenn du möchtest, kannst du zusätzlich definieren:

* **Corporate-Tonfall** (z. B. seriös, beratend, kundenorientiert)
* **Logo-Platzierung** auf jeder Folie
* **Standard-Folienreihenfolge** (z. B. Titel → Agenda → Hauptteil → Fazit)

Diese Punkte kannst du im Abschnitt *„Kommunikationsprinzipien“* oder *„Für PowerPoint-Präsentationen“* im Prompt ergänzen.

---

## ✅ **Beispiel-Dateiname und Struktur**

```
volksbank-buehl-skill/
├── SKILL.md
└── Brand Reference PPT.pptx
```

Nach dem Hochladen ist dein Skill bereit, automatisch Präsentationen und Berichte im Corporate Design der **Volksbank Bühl** zu erstellen.

```
```


```
```

