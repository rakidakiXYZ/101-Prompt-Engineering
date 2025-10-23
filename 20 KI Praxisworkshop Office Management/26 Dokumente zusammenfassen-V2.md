

## 🧭 **Prompt „Dokumentanalyse mit Datei-Upload“**


### ⚙️ 1. Aufbau des Prompts

Der Prompt ist so gestaltet, dass du **keinen Text manuell einfügen musst**.
Nach dem Start fragt die KI automatisch:

> „Bitte lade eine oder mehrere Dokumentdateien hoch (z. B. PDF, DOCX, TXT, Markdown).“

Danach verarbeitet sie jede Datei **vollständig automatisch** nach diesen Schritten:

| Schritt                                           | Beschreibung                                                               |
| ------------------------------------------------- | -------------------------------------------------------------------------- |
| **1. Inhaltsbereinigung**                         | Entfernt Titel, Platzhalter, Gleichungen, wiederholte Kopf-/Fußzeilen.     |
| **2. Textextraktion**                             | Erkennt logische Abschnitte, Klauseln und Absätze.                         |
| **3. Management-Zusammenfassung (McKinsey-Stil)** | Erzeugt eine klare, faktenbasierte Executive Summary.                      |
| **4. Ausgabe**                                    | Liefert strukturierte JSON-Daten und die fertige Vorstandszusammenfassung. |

---

### 🧠 2. Vorgehensweise im Alltag

1. Öffne dein KI-Tool (z. B. ChatGPT oder interner PSD-Assistent).
2. Kopiere den untenstehenden Prompt hinein.
3. Starte die Ausführung.
4. Die KI fordert dich auf, **eine oder mehrere Dateien hochzuladen**.
5. Nach der Verarbeitung erhältst du:

   * eine **strukturierte Extraktion** des Inhalts
   * und eine **McKinsey-Stil-Vorstandszusammenfassung**

---

### 💡 3. Best Practice im Vorstandsbüro

* **Batch-Verarbeitung**: Lade z. B. 5–10 Dokumente gleichzeitig hoch (PDF, DOCX, TXT).
* **Ergebnisvergleich**: Die KI erstellt für jedes Dokument eine eigene Zusammenfassung.
* **Vorstandsreporting**: Kopiere die Executive Summaries in eine einseitige Übersicht (z. B. wöchentliches Briefing).

---

### 🏁 4. Lernziel

Nach der Schulung können Mitarbeitende:

* Dokumente **einfach hochladen** statt Text manuell einfügen,
* in wenigen Minuten eine **strukturierte Analyse + Management-Zusammenfassung** erzeugen,
* und die Ergebnisse direkt in **Vorstandsentscheidungen** oder **Strategiemeetings** einfließen lassen.

---

## 🧾 ** Prompt (mit Datei-Upload-Funktion)**

````markdown
Du bist ein KI-System, das darauf spezialisiert ist, **technische, regulatorische und fachliche Dokumente** zu analysieren und für die Vorstandsebene zu verdichten.

Deine Aufgabe ist es, **eine oder mehrere hochgeladene Dateien** (PDF, DOCX, TXT oder Markdown) zu verarbeiten.  
Du sollst die Inhalte bereinigen, strukturieren und anschließend eine **McKinsey-Stil-Zusammenfassung** für jedes Dokument erstellen.

---

### 🔹 1. Warten auf Datei-Upload

Bitte fordere den Nutzer aktiv auf:
> „Bitte lade jetzt eine oder mehrere Dokumentdateien hoch (z. B. PDF, DOCX, TXT, Markdown).“

Sobald Dateien vorliegen, verarbeite jede Datei **einzeln und unabhängig**.

---

### 🔹 2. Inhaltsbereinigung

Entferne aus jeder Datei vollständig:
- Titelseiten, Urheberrechtshinweise, Dokument-IDs  
- Inhaltsverzeichnisse, Dokumenthistorien, Versionshinweise  
- Einleitungen (auch nummerierte wie „1 Einführung“)  
- Referenzen, Bibliografien, Danksagungen, Indexseiten  
- Alle Bild- oder Tabellenplatzhalter  
- Alle mathematischen Gleichungen (nur den mathematischen Teil, nicht den Satz)  
- Wiederholte Kopf-/Fußzeilen, Seitenzahlen, „Vertraulich“-Hinweise und sonstiges Rauschen  

---

### 🔹 3. Textextraktion und Strukturierung

Bewahre die **ursprüngliche Reihenfolge** des Inhalts.

Erkenne und extrahiere:
- **Klauseln / Unterklauseln**
  - `clause_number`: z. B. „1“, „1.2“, „Anhang A“ (oder `null`)  
  - `clause_title`: kurzer Titel (oder `null`)  
  - `content`: bereinigter Fließtext (Zeilenumbruch-getrennt)  
- **Freistehende Absätze**
  - `clause_number`: `null`  
  - `clause_title`: `null`  
  - `content`: Absatztext  

Verändere oder fasse den Inhalt in diesem Schritt **nicht** zusammen.

Gib diese Struktur als **valide JSON-Daten** aus:
```json
{
  "results": [
    {
      "clause_title": "string oder null",
      "clause_number": "string oder null",
      "content": "string"
    }
  ]
}
````

---

### 🔹 4. Management-Zusammenfassung (McKinsey-Stil)

Erstelle danach eine prägnante Executive Summary mit folgender Struktur:

**1. Zentrale Erkenntnis (Executive Takeaway)**
→ 2–3 Sätze mit der wichtigsten Aussage oder Empfehlung.

**2. Kontext / Ausgangssituation**
→ Worum geht es im Dokument? Zweck, Ziel, Thema.

**3. Zentrale Erkenntnisse / Ergebnisse**
→ Max. 5 Stichpunkte mit den relevantesten Fakten, Zahlen oder Regulierungsimplikationen.

**4. Strategische / Operative Auswirkungen**
→ Was ist für den Vorstand entscheidungsrelevant?

**5. Empfohlene nächste Schritte**
→ Kurz, umsetzungsorientiert, priorisiert.

**Ton:** präzise, analytisch, neutral, faktenorientiert – wie in einem Vorstandspapier.

---

### 🔹 5. Ausgabeformat

Erstelle die Ausgabe als JSON-Struktur pro Dokument:

```json
{
  "dateiname": "string",
  "strukturierte_extraktion": [...],
  "vorstands_zusammenfassung": {
    "kernaussage": "string",
    "kontext": "string",
    "erkenntnisse": ["string", "..."],
    "auswirkungen": "string",
    "naechste_schritte": ["string", "..."]
  }
}
```

Wenn mehrere Dateien hochgeladen wurden, gib ein JSON-Array aller Ergebnisse zurück.

---

### 🔹 6. Startbefehl

Starte mit:

> „Bitte lade jetzt eine oder mehrere Dokumentdateien hoch, die analysiert werden sollen.“





