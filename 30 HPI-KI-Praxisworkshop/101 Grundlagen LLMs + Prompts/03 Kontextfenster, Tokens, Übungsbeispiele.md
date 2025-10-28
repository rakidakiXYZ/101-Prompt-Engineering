

# 📚 Teil A: Grundverständnis – Wie KI mit Sprache arbeitet 

## Kapitel 1: Wie „denkt" eine KI? 🟢 Basis

### Die Wahrscheinlichkeits-Maschine

Stellen Sie sich ein Wort-Ergänzungsspiel vor. Genau das macht ein Sprachmodell – nur mit Statistik.

**Beispiel (vereinfacht):**

```
"Die HR-Abteilung bittet um..."
→ KI berechnet Wahrscheinlichkeiten:
   - Rückmeldung (38 %)
   - Feedback (27 %)
   - Stellungnahme (22 %)
   - Terminierung (9 %)
```

Die KI hat aus sehr vielen Texten gelernt, **welche Wörter typischerweise aufeinander folgen**. Sie „versteht" nicht wie ein Mensch – sie **erkennt und reproduziert Muster**.

### 🎯 Merksätze

* KI = Mustererkennung + Wahrscheinlichkeiten, kein echtes Verständnis.
* Antworten sind **Token für Token** berechnete Vorschläge.
* Wer **klare Vorgaben** macht, bekommt **klare Ergebnisse**.

**Praktisches TK-Beispiel:**

```
Prompt: "Erstelle eine Betreffzeile für eine Mitarbeiter-Rundmail zur neuen Homeoffice-Regelung."
KI denkt u.a.:
- "Neue Homeoffice-Regelung: Wichtige Infos für alle TK-Mitarbeitende"
- "Homeoffice-Update – Gültig ab [Datum]"
```

---

## Kapitel 2: Tokens – Die Bausteine der KI-Kommunikation 🟢 Basis

### Was sind Tokens?

Tokens sind kleinste Spracheinheiten (ähnlich Silben/Wortteile). Denken Sie an **Legosteine**.

**Visualisierung (vereinfachend):**

```
"Mitarbeitergespräch" → [Mit][ar][bei][ter][ge][spräch]  ≈ 6 Tokens
"Gesundheitsförderung" → [Ge][sund][heits][för][de][rung]  ≈ 6 Tokens
"Techniker Krankenkasse" → [Tech][ni][ker][Kran][ken][kas][se] ≈ 7 Tokens
```

**Grobe Faustregel (Deutsch):**

* **1 Token ≈ 4 Zeichen**
* **100 Tokens ≈ 70–80 Wörter**
* **Eine A4-Seite ≈ 500–700 Tokens** (je nach Dichte)

**Kostenbewusstsein (modellabhängig):**

```
Kurzer Betreff (10 Wörter)   ≈ 15 Tokens
Mail-Absatz (100 Wörter)     ≈ 130 Tokens
Eine Seite (500 Wörter)      ≈ 650 Tokens
Kapitel (2.000 Wörter)       ≈ 2.600 Tokens
```

**Übung 1 – Token schätzen**

1. „DSGVO" → ___ Tokens
2. „Bewerbungsgespräch" → ___ Tokens
3. „Gesundheitsmanagement" → ___ Tokens

*Lösung (typisch):* 1) 1–2  |  2) 4–5  |  3) 5–6

**Warum wichtig?**

* **Jeder Token kostet** (Zeit & Geld).
* **Kürzer & strukturierter** = schneller & günstiger.
* **Limits** begrenzen, wie viel Kontext die KI gleichzeitig „im Kopf" hat.

---

## Kapitel 3: Das Kontextfenster – das Arbeitsgedächtnis der KI 🟢 Basis

Die KI arbeitet mit einem **Notizblock**. Alles, was Sie eingeben (und was die KI ausgibt), muss auf diesen Block passen.

**Richtwerte (modell-/anbieterabhängig, ändern sich laufend):**

```
Typische Größen: ~128.000 bis >1.000.000 Tokens
→ von „mehreren Dutzend" bis „vielen Hundert" A4-Seiten
```

**Wenn der Block voll ist:**

```
[Frühere Mails] → [Zwischenergebnisse] → [Aktuelles] → [VOLL]
         ↑                               ↑
     wird verdrängt                bleibt erhalten
```

**Token sparen – Beispiel:**

```
Schlecht:
"Ich hoffe, es geht dir gut. Ich hätte da eine Bitte ... könntest du mir evtl. mal auflisten ..."
→ viele Füllwörter, hohe Kosten

Gut:
"Liste: 5 Benefits für Azubis im Gesundheitswesen. Je Punkt max. 20 Wörter."
→ präzise, günstig
```

---

## Kapitel 4: Den Token-Fluss verstehen 🟡 Mittel

So verarbeitet die KI Ihren Text:

```
1) EINGABE (Prompt)
2) TOKENISIERUNG  → Zerlegung in Tokens
3) VERARBEITUNG   → Musterabgleich
4) GENERIERUNG    → Ausgabe Token für Token
5) AUSGABE        → fertiger Text
```

**Generierung geschieht sequenziell (vereinfacht):**

```
Schritt 1: "Die" 
Schritt 2: "Die Kampagne" 
Schritt 3: "Die Kampagne zielt" 
Schritt 4: "Die Kampagne zielt auf..." 
```

**Übung 2 – Prompt kürzen**

* „Könntest du bitte so freundlich sein und mir erklären…"
  → „Erkläre kurz…"
* „Ich würde gerne von dir wissen, falls es möglich ist…"
  → „Nenne bitte…"
* „Es wäre super, wenn du mir sagen könntest…"
  → „Sag mir…"

---

# 📝 Teil B: Erste Schritte – Prompts für den HR- und Marketing-Alltag

## Kapitel 5: Die 4-K-Formel 🟢 Basis

1. **K**ontext – Worum geht's?
2. **K**onkrete Aufgabe – Was genau tun?
3. **K**riterien – Tonalität, Tiefe, Umfang, Prüfschritte
4. **K**ontrolle – Format (Liste/Tabelle), Länge, Zielgruppe

**Beispiel (HR-Konzept):**

```
Kontext: Interne Kommunikation für TK-Mitarbeitende, Thema "Neue Weiterbildungsangebote".
Aufgabe: 3 Kommunikationskanäle mit Pro/Contra.
Kriterien: Klar, motivierend, DSGVO-konform, keine Personendaten.
Kontrolle: Tabelle, max. 10 Zeilen, am Ende 1 Empfehlungssatz.
```

---

## Kapitel 6: Kontext aufbauen und halten 🟡 Mittel

**Technik „Roter Faden"**

```
P1: "Thema: Planung Recruiting-Kampagne 2026. Ziele: Pflegekräfte, IT-Experten, Gesundheitsberater."
P2: "Empfiehl 5 Social-Media-Kanäle, je 1 Satz Nutzen für die Zielgruppe."
P3: "Für Kanal 2: Entwurf eines 3-Post-Konzepts."
```

**Technik „Zwischenbilanz"**

```
"Fasse zusammen:
- Ziele (Stichpunkte)
- Entscheidungen offen
- Nächste Schritte (verantwortlich + Termin)"
```

**Technik „Checkpoint"**

```
"Checkpoint:
Wir arbeiten an [Thema].
Bisher: [Ergebnisse].
Fehlt: [Lücken].
Nächster Schritt: [Aufgabe + Format]."
```

**Übung 3 – Kontext-Kette (Mitarbeiterbindung)**

1. „Nenne 3 Hauptgründe für sinkende Mitarbeiterzufriedenheit."
2. „Entwickle für Grund 1 drei Gegenmaßnahmen (TK-Kontext)."
3. „Erstelle To-do-Liste 90 Tage, Verantwortliche & Meilensteine."

---

## Kapitel 7: Token-Sparstrategien 🟡 Mittel

**1) Abkürzungen definieren**

```
"Ab jetzt:
EB = Employer Branding
MA = Mitarbeitende
BGM = Betriebliches Gesundheitsmanagement
Erstelle EB-Kampagne mit BGM-Schwerpunkt."
```

**2) Struktur erzwingen**

```
"Ausgabe als Tabelle:
Spalte: Maßnahme | Nutzen | Aufwand | Zielgruppe | Frist"
```

**3) Inkrementell arbeiten**

```
Schritt 1: "Liste 5 Herausforderungen im Healthcare-Recruiting."
Schritt 2: "Detailliere Herausforderung 3 (Ursache/Wirkung/Lösung)."
Schritt 3: "Erstelle Maßnahmenplan (Owner + Termin)."
```

**Mini-Tabelle**

| Technik                        | Vorher | Nachher | Ersparnis |
| ------------------------------ | ------ | ------- | --------- |
| Abkürzungen & Glossar          | 150    | 90      | ~40%      |
| Listen/Tabelle statt Fließtext | 300    | 120     | ~60%      |
| Präzise Längen-Vorgaben        | 500    | 200     | ~60%      |

---

## Kapitel 8: Häufige Anfängerfehler 🟢 Basis

* **Romansprache** → direkt, kurz, sachlich.
* **„Erzähl mir alles…"** → lieber modular (Teilthemen).
* **Kontextverlust** → regelmäßig **Zusammenfassen lassen**.
* **Format vergessen** → **Liste/Tabelle** explizit verlangen.

**Checkliste vor dem Senden**

* [ ] präzise Aufgabe?
* [ ] ein Thema?
* [ ] Format + Länge vorgegeben?
* [ ] interne/ vertrauliche Daten entfernt/anonymisiert?

---

# 🚀 Teil C: Praxis im TK-Alltag

## Kapitel 9: Mini-Projekt – HR-Kampagne erstellen 🟡 Mittel

**Phase 1 – Grundlagen (Token-Budget ~100)**

```
Prompt 1.1:
"Erstelle 3 Personas für Recruiting-Zielgruppen (Pflegekräfte/IT-Experten/Gesundheitsberater).
Je Persona: Rolle | Motivation | Bedenken | KPI (je max. 8 Wörter)."
```

**Phase 2 – Strategie (Token-Budget ~150)**

```
Prompt 2.1:
"Für Persona 'Pflegekraft': 3 Maßnahmen zur Steigerung der Arbeitgeberattraktivität.
Format: Überschrift + 1 Satz Wirkung."
```

**Phase 3 – Inhalte (Token-Budget ~200)**

```
Prompt 3.1:
"Entwirf Executive Summary für HR-Leitung (max. 120 Wörter).
Ton: professionell, mitarbeiterorientiert. Am Ende 1 Handlungsempfehlung."
```

**Ihre Aufgabe:**
Dokumentieren Sie je Schritt: geschätzte Tokens, Qualität (Schulnote), Verbesserungsideen.

---

## Kapitel 10: Fortgeschrittene Techniken 🔴

**1) Denkkette anfordern (ohne sensible Daten)**

```
"Leite Schritt für Schritt her:
1) Problemdefinition
2) Annahmen
3) Optionen
4) Entscheidungskriterien
5) Empfehlung (1 Satz)"
```

**2) Few-Shot (mit Muster)**

```
"Beispiel-Protokollauszug:
- TOP 3: Diversity-Strategie
- Beschluss: Quarterly Review einführen
- Verantwortlich: HR-Leitung, Frist: 31.03.

Erstelle 2 ähnliche Auszüge für TOP 'Recruiting' und 'BGM'."
```

**3) Rollenwechsel**

```
"Du bist HR-Manager:in bei der Techniker Krankenkasse.
Ziel: 45-Minuten-Agenda zur Einführung eines neuen Bewerbermanagementsystems.
Erstelle Ablauf + Zeitboxen + Output je Abschnitt."
```

**4) Iteration**

```
Runde 1: "Grobkonzept Employer-Branding-Kampagne."
Runde 2: "Verdichte auf 1 Seite, Tabelle statt Fließtext."
Runde 3: "Prüfe auf DSGVO/Compliance; ergänze Datenschutzhinweise."
```

---

## Kapitel 11: Token-Optimierung für Profis 🔴

**80/20-Regel:**
Die **Qualität** hängt vor allem von **Ziel, Format, Länge** ab.

**Prioritäten**

* **Hoch:** Ziel, Format/Struktur, Länge
* **Mittel:** Zielgruppe, Tonalität, Beispiele
* **Niedrig:** Floskeln, Wiederholungen

**Hacks**

```
Batch:
"Für HR-Leitung, Marketing-Team, Recruiting:
je: Ziel (6 Wörter) | 3 KPIs | Frist (Datum)."

Template:
"[Thema]: [Ziel], [KPI], [Deadline], [Owner]."

Komprimierung:
Statt "Bitte erstelle ...": "Erstelle ..."
```

---

## Kapitel 12: Workshop mit Lösungen 🟢–🔴

**🟢 Aufgabe 1 – Token-Bewusstsein (Thema: Executive Summary)**

* Lang (50+): „Ich würde sehr gerne eine ausführliche, leicht verständliche…"
* Mittel (≈20): „Executive Summary zu Thema X, 5 Sätze, professionell."
* Kurz (≈10): „Executive Summary X – 5 Sätze."

**🟡 Aufgabe 2 – Kontext-Management (Mitarbeiterbindung)**

1. „Nenne 3 Kündigungsgründe (hypothesenbasiert)."
2. „Für Grund 1: 3 Gegenmaßnahmen."
3. „Maßnahme 2: Umsetzungsplan 6 Monate."
4. „Rollen/Owner + Meilensteine."
5. „KPIs (5) + Zielwerte."

**🔴 Aufgabe 3 – Prompt-Architektur (Budget ~500 Tokens)**

```
PROJEKT: HR-Konzept "Mitarbeiterbindung & Gesundheitsförderung"

PHASE 1 – Analyse (~120):
- Matrix: 3 Mitarbeitergruppen × 3 Maßnahmen
- je Feld: Nutzen (≤6 Wörter)

PHASE 2 – Optionen (~150):
- 3 Szenarien (Basis/Standard/Premium)
- je: Kosten (kurz), Risiken (3), KPI (3)

PHASE 3 – Umsetzung (~150):
- Roadmap 4 Quartale, Meilensteine, Verantwortliche

PHASE 4 – Entscheidung (~80):
- Entscheidungskriterien (5) + Empfehlung (1 Satz)
Format: Tabellen + Stichpunkte.
```

---

# 🧰 Teil D: TK-spezifische Use-Cases & Prompt-Vorlagen

## 1) HR-Konzept – Entscheidungsoptionen

```md
Kontext: HR-Konzept "[Thema]" für TK-Management, Präsentation am [Datum].
Aufgabe: 3 Entscheidungsoptionen mit Pro/Contra.
Kriterien: Neutral, faktenorientiert, keine Personendaten, DSGVO-konform.
Kontrolle: Tabelle (Option | Nutzen | Risiko | Aufwand | Frist | Owner).
```

## 2) Meeting-Protokoll-Kondensation (aus Langtext)

```md
Kontext: Langprotokoll einer 2-stündigen HR-Sitzung (intern).
Aufgabe: Kürze auf 10 Stichpunkte + 3 Beschlüsse + 3 To-dos.
Kriterien: Originaltreue, keine Mutmaßungen, Kennzeichnung offener Punkte.
Kontrolle: Liste + To-do-Tabelle (Punkt | Owner | Termin).
```

## 3) Mail-Entwurf an Führungskräfte

```md
Kontext: Info zur neuen Datenschutzrichtlinie, Handlungsbedarf in den Teams.
Aufgabe: Mail-Entwurf in 120–150 Wörtern.
Kriterien: Klar, handlungsorientiert, Bullet-Liste "Was ist zu tun?".
Kontrolle: Betreff (≤70 Zeichen), PS mit Linkplatzhalter.
```

## 4) Management-Meeting – Agenda (30 Min Slot)

```md
Kontext: Management-Meeting, Slot "Digitalisierung HR-Prozesse".
Aufgabe: Agenda mit Zeitboxen + erwartetes Ergebnis je Punkt.
Kriterien: 30 Min, Puffer 5 Min.
Kontrolle: Tabelle (Zeit | Punkt | Output).
```

## 5) Risiko-Register für HR-Projekte (kompakt)

```md
Kontext: Projekt [Name].
Aufgabe: Risiko-Register (5 Risiken) mit Ursache, Wirkung, Mitigation, Rest.
Kriterien: Konservativ, praxisnah, keine Personendaten.
Kontrolle: Tabelle (ID | Risiko | Ursache | Wirkung | Maßnahme | Owner | Termin).
```

## 6) Social-Media-Post-Skizze (Employer Branding)

```md
Kontext: LinkedIn-Post zu [Thema] für Employer Branding.
Aufgabe: 3 Post-Varianten + Hashtags (5).
Kriterien: Authentisch, wertschätzend, keine internen Zahlen ohne Freigabe.
Kontrolle: Endabschnitt "Freigabe durch [Marketing-Leitung] erforderlich".
```

---

# 🔐 Teil E: Compliance & Qualität im Arbeitsalltag

## Datenschutz-Quickcheck (DSGVO-Sensibilität)

* **Keine** personenbezogenen Mitarbeiterdaten eingeben (Namen, Personalnummern, Adressen etc.).
* Interne Dokumente nur in **freigegebenen** Tools/Umgebungen nutzen.
* **Anonymisieren/Pseudonymisieren**: „Mitarbeiter:in A", „Bewerber B", „Abteilung X".
* **Quellenpflicht**: Bei Zahlen/Regeln **Quelle/Datum** als Platzhalter einfordern.
* **Freigabewege respektieren**: Management-Material **immer** intern freigeben lassen.

**Prompt-Baustein (Schutz):**

```
"Arbeite ohne personenbezogene Daten. 
Wenn Informationen fehlen, frage nicht nach Klarnamen, sondern nutze Platzhalter.
Kennzeichne Annahmen eindeutig."
```

## Halluzinationen vermeiden (Reality-Check)

* **Format erzwingen**: „Nur, wenn Quelle vorhanden → ausgeben, sonst 'keine belastbare Quelle' schreiben."
* **Unbekannt kenntlich**: „Wenn unsicher, markiere [unsicher] und stoppe."
* **Verifikationsschritt**: Immer **„Prüfschritt"** miterzeugen lassen.

**Beispiel:**

```md
"Erstelle 5 Fakten zur aktuellen Arbeitsmarktlage im Gesundheitswesen.
Für jeden Fakt: Quelle (Titel, Datum), Linkplatzhalter.
Wenn keine verlässliche Quelle → 'keine belastbare Quelle'."
```

## Qualitäts-Sicherung (QA) – schneller Review

```md
"Prüfe den Text nach:
1) Ziel / Botschaft klar?
2) Zahlen mit Quelle/Datum?
3) DSGVO/Compliance ok?
4) Format konsistent (Tabelle/Listen)?
5) Max. Länge eingehalten?

Gib nur eine Fehlerliste mit Korrekturvorschlägen aus."
```

---

# 🗂️ Appendix

## Glossar (kompakt)

* **Completion** – KI-Antwort
* **Kontextfenster** – „Arbeitsgedächtnis" (Token-Limit)
* **Few-Shot** – Per Beispiel anleiten
* **Halluzination** – Erfundene „Fakten"
* **Prompt** – Ihre Anweisung
* **Temperature** – Kreativität (niedrig = präziser)
* **Token** – kleinste Recheneinheit für Text

## Nützliche Ressourcen (intern ergänzen)

* Token-Zähler/Tokenizer des genutzten Anbieters
* Interne Freigaberegeln & Vorlagen (HR/Marketing)
* Styleguide (Sprache, Ton, Markenführung TK)

---

# 🧪 Übungsteil (für das Seminar)

### Ü1 – Betreffzeilen (5 Min)

```
Thema: "Neue Weiterbildungsangebote für TK-Mitarbeitende"
Erzeuge 5 Betreffvarianten (≤70 Zeichen), motivierend, professionell.
```

### Ü2 – Executive Summary (10 Min)

```
Kontext: HR-Leitung benötigt Kurzlage zu "Recruiting-Strategie 2026".
Aufgabe: 5 Sätze, je ≤20 Wörter, am Ende 1 Handlungsempfehlung.
```

### Ü3 – Protokoll-Extrakt (10 Min)

```
Eingabe: (Trainertext/Langprotokoll)
Ausgabe: 8 Stichpunkte, 3 Beschlüsse, 3 To-dos (Owner + Termin).
```

### Ü4 – QA-Check (5 Min)

```
Prüfe Ü2 mit QA-Checkliste. Nenne nur Abweichungen + Korrektur.
```

---

# 📎 Schnellstart-Karten (zum Ausdrucken)

**1) 4-K-Formel**

```
Kontext | Konkrete Aufgabe | Kriterien | Kontrolle
```

**2) Standard-Kontrollsätze**

```
"Keine Personendaten, DSGVO-konform arbeiten."
"Quellen & Datum angeben; sonst 'keine belastbare Quelle'."
"Ausgabe als Tabelle/Liste, max. [Länge]."
```

**3) Mini-HR-Prompt**

```
"Executive Summary [Thema] für TK-Management:
5 Sätze, professionell, 1 Handlungsempfehlung am Ende."
```

---



**Praxis schlägt Theorie:** klein anfangen, iterieren, Vorlagen bauen – und konsequent **schutz- und prüforientiert** arbeiten. Viel Erfolg! 🚀
