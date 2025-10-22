# 📚 Teil A: Grundverständnis – Wie KI mit Sprache arbeitet 

## Kapitel 1: Wie „denkt“ eine KI? 🟢 Basis

### Die Wahrscheinlichkeits-Maschine

Stellen Sie sich ein Wort-Ergänzungsspiel vor. Genau das macht ein Sprachmodell – nur mit Statistik.

**Beispiel (vereinfacht):**

```
"Der Vorstand bittet um..."
→ KI berechnet Wahrscheinlichkeiten:
   - Freigabe (38 %)
   - Entscheidung (27 %)
   - Stellungnahme (22 %)
   - Terminierung (9 %)
```

Die KI hat aus sehr vielen Texten gelernt, **welche Wörter typischerweise aufeinander folgen**. Sie „versteht“ nicht wie ein Mensch – sie **erkennt und reproduziert Muster**.

### 🎯 Merksätze

* KI = Mustererkennung + Wahrscheinlichkeiten, kein echtes Verständnis.
* Antworten sind **Token für Token** berechnete Vorschläge.
* Wer **klare Vorgaben** macht, bekommt **klare Ergebnisse**.

**Praktisches Bank-Beispiel:**

```
Prompt: "Erstelle eine Betreffzeile für ein Vorstands-Rundschreiben zur MaRisk-Änderung."
KI denkt u.a.:
- "Aktualisierte MaRisk: Relevante Punkte für PSD [Stadt]"
- "MaRisk-Update – Handlungsbedarf bis [Datum]"
```

---

## Kapitel 2: Tokens – Die Bausteine der KI-Kommunikation 🟢 Basis

### Was sind Tokens?

Tokens sind kleinste Spracheinheiten (ähnlich Silben/Wortteile). Denken Sie an **Legosteine**.

**Visualisierung (vereinfachend):**

```
"Vorstandsvorlage" → [Vor][stands][vor][la][ge]  ≈ 5 Tokens
"Zinsänderung"     → [Zins][än][de][rung]        ≈ 4 Tokens
"PSD Bank"         → [PSD][Bank]                  ≈ 2 Tokens
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

1. „MaRisk“ → ___ Tokens
2. „Vorstandssitzung“ → ___ Tokens
3. „Kreditvergaberichtlinie“ → ___ Tokens

*Lösung (typisch):* 1) 1–2  |  2) 3–4  |  3) 5–6

**Warum wichtig?**

* **Jeder Token kostet** (Zeit & Geld).
* **Kürzer & strukturierter** = schneller & günstiger.
* **Limits** begrenzen, wie viel Kontext die KI gleichzeitig „im Kopf“ hat.

---

## Kapitel 3: Das Kontextfenster – das Arbeitsgedächtnis der KI 🟢 Basis

Die KI arbeitet mit einem **Notizblock**. Alles, was Sie eingeben (und was die KI ausgibt), muss auf diesen Block passen.

**Richtwerte (modell-/anbieterabhängig, ändern sich laufend):**

```
Typische Größen: ~128.000 bis >1.000.000 Tokens
→ von „mehreren Dutzend“ bis „vielen Hundert“ A4-Seiten
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
"Liste: 5 MaRisk-Änderungen 202x mit Kurzwirkung für PSD-Vorstände. Je Punkt max. 20 Wörter."
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
Schritt 2: "Die Vorlage" 
Schritt 3: "Die Vorlage fasst" 
Schritt 4: "Die Vorlage fasst die Änderungen..." 
```

**Übung 2 – Prompt kürzen**

* „Könntest du bitte so freundlich sein und mir erklären…“
  → „Erkläre kurz…“
* „Ich würde gerne von dir wissen, falls es möglich ist…“
  → „Nenne bitte…“
* „Es wäre super, wenn du mir sagen könntest…“
  → „Sag mir…“

---

# 📝 Teil B: Erste Schritte – Prompts für den Bank-Alltag

## Kapitel 5: Die 4-K-Formel 🟢 Basis

1. **K**ontext – Worum geht’s?
2. **K**onkrete Aufgabe – Was genau tun?
3. **K**riterien – Tonalität, Tiefe, Umfang, Prüfschritte
4. **K**ontrolle – Format (Liste/Tabelle), Länge, Zielgruppe

**Beispiel (Vorstandsvorlage):**

```
Kontext: Vorlage für Vorstandssitzung PSD [Stadt], TOP "Zinsänderung Privatkredite".
Aufgabe: 3 Entscheidungsoptionen mit Pro/Contra.
Kriterien: Klar, neutral, bankintern. DSGVO-konform, keine Kundendaten.
Kontrolle: Tabelle, max. 10 Zeilen, am Ende 1 Empfehlungssatz.
```

---

## Kapitel 6: Kontext aufbauen und halten 🟡 Mittel

**Technik „Roter Faden“**

```
P1: "Thema: Vorbereitung Vorstandsklausur 202x. Ziele: Effizienz, Vertrieb, Risiko."
P2: "Empfiehl 5 Agenda-Punkte, je 1 Satz Nutzen für den Vorstand."
P3: "Für Agenda-Punkt 2: Entwurf eines 10-Minuten-Inputs."
```

**Technik „Zwischenbilanz“**

```
"Fasse zusammen:
- Ziele (Stichpunkte)
- Entscheidungen offen
- Nächste Schritte (verantwortlich + Termin)"
```

**Technik „Checkpoint“**

```
"Checkpoint:
Wir arbeiten an [Thema].
Bisher: [Ergebnisse].
Fehlt: [Lücken].
Nächster Schritt: [Aufgabe + Format]."
```

**Übung 3 – Kontext-Kette (Mitgliederbindung → Kundenbindung)**

1. „Nenne 3 Hauptgründe für abnehmende Giro-Aktivität.“
2. „Entwickle für Grund 1 drei Gegenmaßnahmen (PSDKontext).“
3. „Erstelle To-do-Liste 90 Tage, Verantwortliche & Meilensteine.“

---

## Kapitel 7: Token-Sparstrategien 🟡 Mittel

**1) Abkürzungen definieren**

```
"Ab jetzt:
VV = Vorstandsvorlage
AR = Aufsichtsrat
R&I = Risiko & Internes
Erstelle VV zu 'Filialnetz-Optimierung' mit R&I-Abschnitt."
```

**2) Struktur erzwingen**

```
"Ausgabe als Tabelle:
Spalte: Maßnahme | Nutzen | Aufwand | Risiko | Frist"
```

**3) Inkrementell arbeiten**

```
Schritt 1: "Liste 5 Risiken beim Projekt X."
Schritt 2: "Detailliere Risiko 3 (Ursache/Wirkung/Mitigation)."
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
* **„Erzähl mir alles…“** → lieber modular (Teilthemen).
* **Kontextverlust** → regelmäßig **Zusammenfassen lassen**.
* **Format vergessen** → **Liste/Tabelle** explizit verlangen.

**Checkliste vor dem Senden**

* [ ] präzise Aufgabe?
* [ ] ein Thema?
* [ ] Format + Länge vorgegeben?
* [ ] interne/ vertrauliche Daten entfernt/anonymisiert?

---

# 🚀 Teil C: Praxis im PSD-Bank-Alltag

## Kapitel 9: Mini-Projekt – Vorstands-Unterlage erstellen 🟡 Mittel

**Phase 1 – Grundlagen (Token-Budget ~100)**

```
Prompt 1.1:
"Erstelle 3 Personas für Vorstandsklausur-Zielgruppen (Mitarbeitende/ Mitglieder/ Partner).
Je Persona: Rolle | Ziel | Sorge | KPI (je max. 8 Wörter)."
```

**Phase 2 – Strategie (Token-Budget ~150)**

```
Prompt 2.1:
"Für Persona 'Mitglied': 3 Maßnahmen zur Erhöhung Giro-Aktivität.
Format: Überschrift + 1 Satz Wirkung."
```

**Phase 3 – Inhalte (Token-Budget ~200)**

```
Prompt 3.1:
"Entwirf Vorstands-Executive-Summary (max. 120 Wörter).
Ton: neutral, faktenorientiert. Am Ende 1 Entscheidungsempfehlung."
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
- TOP 3: IT-Resilienz
- Beschluss: Drittanbieter-Monitoring vierteljährlich
- Verantwortlich: CISO, Frist: 31.03.

Erstelle 2 ähnliche Auszüge für TOP 'Vertrieb' und 'Compliance'."
```

**3) Rollenwechsel**

```
"Du bist Assistenz des Vorstands.
Ziel: 30-Minuten-Agenda zur MaRisk-Umsetzung.
Erstelle Ablauf + Zeitboxen + Output je Abschnitt."
```

**4) Iteration**

```
Runde 1: "Grobkonzept Vorstandsvorlage."
Runde 2: "Verdichte auf 1 Seite, Tabelle statt Fließtext."
Runde 3: "Prüfe auf Risiken/Compliance; ergänze Mitigations."
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
"Für AR, Vorstand, Bereichsleiter:
je: Ziel (6 Wörter) | 3 KPIs | Frist (Datum)."

Template:
"[TOP]: [Ziel], [KPI], [Entscheidung bis], [Owner]."

Komprimierung:
Statt "Bitte erstelle ...": "Erstelle ..."
```

---

## Kapitel 12: Workshop mit Lösungen 🟢–🔴

**🟢 Aufgabe 1 – Token-Bewusstsein (Thema: Executive Summary)**

* Lang (50+): „Ich würde sehr gerne eine ausführliche, leicht verständliche…“
* Mittel (≈20): „Executive Summary zu Thema X, 5 Sätze, neutral.“
* Kurz (≈10): „Executive Summary X – 5 Sätze.“

**🟡 Aufgabe 2 – Kontext-Management (Mitgliederkommunikation)**

1. „Nenne 3 Austrittsgründe (hypothesenbasiert).“
2. „Für Grund 1: 3 Gegenmaßnahmen.“
3. „Maßnahme 2: Kampagnenplan 6 Monate.“
4. „Rollen/Owner + Meilensteine.“
5. „KPIs (5) + Zielwerte.“

**🔴 Aufgabe 3 – Prompt-Architektur (Budget ~500 Tokens)**

```
PROJEKT: Vorstandsvorlage "Filialnetz & Service"

PHASE 1 – Analyse (~120):
- Matrix: 3 Kundensegmente × 3 Kanäle
- je Feld: Nutzen (≤6 Wörter)

PHASE 2 – Optionen (~150):
- 3 Szenarien (Konsolidierung/Hybrid/Invest)
- je: Opex/Capex (kurz), Risiken (3), KPI (3)

PHASE 3 – Umsetzung (~150):
- Roadmap 4 Quartale, Meilensteine, Verantwortliche

PHASE 4 – Entscheidung (~80):
- Entscheidungskriterien (5) + Empfehlung (1 Satz)
Format: Tabellen + Stichpunkte.
```

---

# 🧰 Teil D: PSD-spezifische Use-Cases & Prompt-Vorlagen

## 1) Vorstandsvorlage (VV) – Entscheidungsoptionen

```md
Kontext: VV TOP "[Thema]" für PSD [Stadt], Sitzung am [Datum].
Aufgabe: 3 Entscheidungsoptionen mit Pro/Contra.
Kriterien: Neutral, faktenorientiert, keine Kundendaten, DSGVO-konform.
Kontrolle: Tabelle (Option | Nutzen | Risiko | Aufwand | Frist | Owner).
```

## 2) Protokoll-Kondensation (aus Langtext/PDF)

```md
Kontext: Langprotokoll einer 2-stündigen Sitzung (intern).
Aufgabe: Kürze auf 10 Stichpunkte + 3 Beschlüsse + 3 To-dos.
Kriterien: Originaltreue, keine Mutmaßungen, Kennzeichnung offener Punkte.
Kontrolle: Liste + To-do-Tabelle (Punkt | Owner | Termin).
```

## 3) Mail-Entwurf an Bereichsleiter:innen

```md
Kontext: Info zur MaRisk-Anpassung 202x, Handlungsbedarf in den Bereichen.
Aufgabe: Mail-Entwurf in 120–150 Wörtern.
Kriterien: Klar, handlungsorientiert, Bullet-Liste "Was ist zu tun?".
Kontrolle: Betreff (≤70 Zeichen), PS mit Linkplatzhalter.
```

## 4) Aufsichtsrat – Sitzungsagenda (30 Min Slot)

```md
Kontext: AR-Sitzung, Slot "IT-Resilienz".
Aufgabe: Agenda mit Zeitboxen + erwartetes Ergebnis je Punkt.
Kriterien: 30 Min, Puffer 5 Min.
Kontrolle: Tabelle (Zeit | Punkt | Output).
```

## 5) Risiko-Register (kompakt)

```md
Kontext: Projekt [Name].
Aufgabe: Risiko-Register (5 Risiken) mit Ursache, Wirkung, Mitigation, Rest.
Kriterien: Konservativ, banküblich, keine Kundendaten.
Kontrolle: Tabelle (ID | Risiko | Ursache | Wirkung | Maßnahme | Owner | Termin).
```

## 6) Pressestatement-Skizze

```md
Kontext: Externes Statement zu [Thema].
Aufgabe: 3 Kernbotschaften + 1 Q&A-Block (5 Fragen/Antworten).
Kriterien: Sachlich, keine Zahlen ohne Quelle, Freigabehinweis einfügen.
Kontrolle: Endabschnitt "Freigabe durch [Funktion] erforderlich".
```

---

# 🔐 Teil E: Compliance & Qualität im Arbeitsalltag

## Datenschutz-Quickcheck (DSGVO/BaFin-Sensibilität)

* **Keine** personenbezogenen Kundendaten eingeben (Namen, IBAN, Adressen etc.).
* Interne Dokumente nur in **freigegebenen** Tools/Umgebungen nutzen.
* **Anonymisieren/Pseudonymisieren**: „Kunde A“, „Fall B“, „Filiale X“.
* **Quellenpflicht**: Bei Zahlen/Regeln **Quelle/Datum** als Platzhalter einfordern.
* **Freigabewege respektieren**: Vorstands-/AR-Material **immer** intern freigeben lassen.

**Prompt-Baustein (Schutz):**

```
"Arbeite ohne personenbezogene Daten. 
Wenn Informationen fehlen, frage nicht nach Klarnamen, sondern nutze Platzhalter.
Kennzeichne Annahmen eindeutig."
```

## Halluzinationen vermeiden (Reality-Check)

* **Format erzwingen**: „Nur, wenn Quelle vorhanden → ausgeben, sonst ‘keine belastbare Quelle’ schreiben.“
* **Unbekannt kenntlich**: „Wenn unsicher, markiere [unsicher] und stoppe.“
* **Verifikationsschritt**: Immer **„Prüfschritt“** miterzeugen lassen.

**Beispiel:**

```md
"Erstelle 5 Fakten zur MaRisk-Änderung 202x.
Für jeden Fakt: Quelle (Titel, Datum), Linkplatzhalter.
Wenn keine verlässliche Quelle → 'keine belastbare Quelle'."
```

## Qualitäts-Sicherung (QA) – schneller Review

```md
"Prüfe den Text nach:
1) Ziel / Entscheidung klar?
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
* **Kontextfenster** – „Arbeitsgedächtnis“ (Token-Limit)
* **Few-Shot** – Per Beispiel anleiten
* **Halluzination** – Erfundene „Fakten“
* **Prompt** – Ihre Anweisung
* **Temperature** – Kreativität (niedrig = präziser)
* **Token** – kleinste Recheneinheit für Text

## Nützliche Ressourcen (intern ergänzen)

* Token-Zähler/Tokenizer des genutzten Anbieters
* Interne Freigaberegeln & Vorlagen (VV/AR/Protokoll)
* Styleguide (Sprache, Ton, Markenführung)

---

# 🧪 Übungsteil (für das Seminar)

### Ü1 – Betreffzeilen (5 Min)

```
Thema: "Zinsanpassung Privatkredite"
Erzeuge 5 Betreffvarianten (≤70 Zeichen), neutral, ohne Marketing.
```

### Ü2 – Executive Summary (10 Min)

```
Kontext: Vorstand benötigt Kurzlage zu "Filialnetz & Servicezeiten".
Aufgabe: 5 Sätze, je ≤20 Wörter, am Ende 1 Entscheidungssatz.
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
"Keine Kundendaten, DSGVO-konform arbeiten."
"Quellen & Datum angeben; sonst 'keine belastbare Quelle'."
"Ausgabe als Tabelle/Liste, max. [Länge]."
```

**3) Mini-Vorstands-Prompt**

```
"Executive Summary [Thema] für Vorstand PSD [Stadt]:
5 Sätze, neutral, 1 Entscheidungsempfehlung am Ende."
```

---



**Praxis schlägt Theorie:** klein anfangen, iterieren, Vorlagen bauen – und konsequent **schutz- und prüforientiert** arbeiten. Viel Erfolg! 🚀

