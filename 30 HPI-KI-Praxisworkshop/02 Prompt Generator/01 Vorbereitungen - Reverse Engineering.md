

---

# 🧭 Anleitung: Vom Roh-Prompt zum Masterprompt

### *(Reverse Engineering eines KI-Prompts für Anfänger)*

## 🧩 Ziel

Diese Anleitung zeigt dir, **wie du einen einfachen Prompt analysierst, bewertest und systematisch verbesserst**, um ein **präzises, leistungsfähiges Prompt-Design** zu erhalten – z. B. für Gemini, GPT oder andere Modelle.

---

## 🪜 **Schritt 1: Den Ausgangsprompt verstehen**

**Beispiel:**

> „Hey, kannst du dich selbst trainieren oder recherchieren über die neuesten Methoden für Prompt Engineering bei Gemini-Modellen …“

👉 **Ziel:** Erfassen, *was die Kernintention* ist.

* Was will ich eigentlich erreichen?
* Geht es um Recherche, Kreativität, Problemlösung, Code, etc.?
* Wer ist die Zielgruppe (Entwickler, Anfänger, Forscher)?

**Tipp:** Schreib 1–2 Sätze als Zusammenfassung:

> „Ich möchte, dass die KI die besten Prompting-Techniken für Gemini-Modelle recherchiert und strukturiert zusammenfasst.“

---

## 🧠 **Schritt 2: Bewertung des Prompts (Ist-Zustand)**

Erstelle eine Mini-Analyse deines Prompts mit diesen 5 Punkten:

| Kriterium                    | Beschreibung                                                                | Beispielbewertung             |
| ---------------------------- | --------------------------------------------------------------------------- | ----------------------------- |
| 🎯 **Klarheit**              | Ist das Ziel eindeutig formuliert?                                          | Mittel (unklare Zielrichtung) |
| 🧩 **Struktur**              | Gibt es klare Teilschritte oder Bulletpoints?                               | Fehlend                       |
| 📦 **Output-Erwartung**      | Weiß die KI, *wie* sie antworten soll (Format, Tiefe, Struktur)?            | Nein                          |
| 📚 **Kontexttiefe**          | Hat der Prompt genügend Hintergrundinfos (z. B. Modelle, Versionen, Daten)? | Teilweise                     |
| ⚙️ **Präzision der Sprache** | Wird Fachsprache klar und unmissverständlich verwendet?                     | Unpräzise                     |

➡️ Ergebnis: z. B. „Bewertung 6/10 – Ziel klar, aber Struktur und Format fehlen.“

---

## 🧱 **Schritt 3: Schwächen gezielt umformulieren**

Verbessere jeden Aspekt aus der Analyse:

| Problem                | Verbesserung                                                                          |
| ---------------------- | ------------------------------------------------------------------------------------- |
| Unklare Aufgabe        | Füge ein **Zielstatement** hinzu: „Deine Aufgabe ist es, …“                           |
| Kein Outputformat      | Definiere: „Strukturiere die Antwort als Tabelle/Liste …“                             |
| Fehlende Quellenangabe | Ergänze: „Nutze aktuelle (2024–2025) öffentliche Quellen.“                            |
| Zu vage Sprache        | Verwende Fachbegriffe: „Prompt-Engineering-Techniken“, „Frameworks“, „Best Practices“ |

---

## 🧰 **Schritt 4: Strukturbausteine eines guten Prompts**

Baue deinen Prompt aus **klaren Modulen** auf:

1. **Systemrolle / Identität**
   → „Du bist ein erfahrener Prompt-Engineer und Forscher …“

2. **Zielbeschreibung**
   → „Deine Aufgabe ist es, umfassend zu recherchieren …“

3. **Aufgabenstruktur**
   → „1. Erkläre Grundlagen  2. Liste Techniken  3. Gib Beispiele …“

4. **Outputformat**
   → „Gib das Ergebnis in Markdown mit Tabellenstruktur aus.“

5. **Ton & Stil**
   → „Technisch, klar, ohne Umgangssprache.“

6. **Qualitätsrichtlinien**
   → „Wenn Informationen fehlen, markiere sie als ‘nicht dokumentiert’.“

---

## ⚙️ **Schritt 5: Den Prompt zusammenbauen**

Kombiniere alle Bausteine zu einem **Masterprompt**:

```markdown
**Systemrolle:**  
Du bist ein KI-Forscher mit Spezialisierung auf Prompt Engineering.

**Ziel:**  
Recherchiere und analysiere alle aktuellen Prompting-Techniken für Gemini-Modelle (Nano Banana & Veo).

**Aufgaben:**  
1. Fasse die wichtigsten Methoden zusammen.  
2. Vergleiche Bild- vs. Video-Prompting.  
3. Gib konkrete Beispielprompts.  
4. Liste typische Fehler und Best Practices.  

**Outputformat:**  
Markdown-Tabelle mit: Technik | Beschreibung | Anwendungsbereich | Beispiel | Vorteile | Einschränkungen  

**Ton:**  
Professionell, analytisch, praxisnah.
```

---

## 🧩 **Schritt 6: Feinschliff und Testen**

* **Teste deinen Prompt mehrfach** (z. B. in Gemini, GPT oder Claude).
* **Beobachte**, welche Ergebnisse unklar bleiben.
* **Optimiere iterativ** (z. B. füge Quellenanweisungen oder Rollen hinzu).

📈 Tipp:
Führe eine Versionierung deiner Prompts ein:

> `Prompt_v1_raw.md` → `Prompt_v2_structured.md` → `Prompt_v3_master.md`

---

## ✅ **Endergebnis**

Ein optimierter Prompt hat folgende Eigenschaften:

* 🎯 **Zielklarheit:** Die KI weiß genau, was du willst.
* 🧱 **Struktur:** Der Output ist logisch gegliedert.
* 🔍 **Recherchetiefe:** Quellen und Datenbasis sind aktuell.
* 💡 **Umsetzbarkeit:** Die Ergebnisse sind praktisch nutzbar.

---



