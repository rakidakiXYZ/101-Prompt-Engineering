## Halluzinationen & Bias bei LLMs vermeiden

---

## 📚 Teil 1: Grundlagen – mit Fokus Gesundheitswesen

### Warum „halluzinieren" LLMs – und warum ist das im Krankenkassen-Kontext heikel?

LLMs erzeugen sprachlich plausible Antworten auf Basis von Wahrscheinlichkeiten – nicht auf Basis von „Verstehen". Im regulierten Umfeld einer Krankenkasse führt das zu besonderen Risiken:

* 🔄 **Mustervervollständigung:** Fehlende Fakten (z. B. zu DSGVO/Datenschutz-Passagen) werden glaubwürdig „ergänzt".
* 📊 **Überanpassung:** Aus einzelnen Presseartikeln werden allgemeine Branchenaussagen abgeleitet.
* 🎯 **Kontext-Drift:** Fragen zu Gesundheitsthemen vermischen sich mit veralteten Meldungen.
* ⚡ **Temperatur:** Höhere Kreativität erhöht das Risiko falscher, aber überzeugender Antworten.

**TK-spezifische Folgen:** Falsche Management-Briefings, fehlerhafte HR-Vorlagen, unzulässige Versichertenkommunikation, Reputationsrisiken.

### Warum entsteht Bias – und wie zeigt er sich bei Krankenkassen?

Bias (systematische Verzerrung) spiegelt unausgewogene Trainingsdaten wider:

* 🏛️ **Regulatorik-Bias:** Dominanz internationaler (nicht-deutscher) Gesundheitssystem-Quellen.
* 🌍 **Kultur-/Sprach-Bias:** Englische/US-Perspektive dominiert, deutsches Gesundheitswesen unterrepräsentiert.
* 👥 **Rollen-Bias:** Veraltete Stereotype zu Funktionen (z. B. „Pflege = weiblich").
* ✅ **Confirmation Bias:** Modell bestätigt vermutete Trends (z. B. „Digitalisierung = immer besser"), ohne lokale Daten zu prüfen.

---

## 🎯 Teil 2: Halluzinationen erkennen & vermeiden – für HR und Marketing

### 2.1 Struktur-Prompts statt „kurzer Frage"

**❌ Fehleranfälliger Prompt (TK):**

```
Wie ist die aktuelle Situation im Pflegekräfte-Recruiting und was bedeutet das für unsere Strategie?
```

**✅ Belastbarer Prompt mit „Step-by-Step":**

```
Erstelle eine faktenbasierte Kurzlage (max. 10 Sätze) zur Pflegekräfte-Situation und Auswirkungen auf Recruiting-Strategien.

1) QUELLEN:
- Nutze NUR offizielle/verifizierte Quellen (z. B. Bundesagentur für Arbeit, Statistisches Bundesamt, Gesundheitsministerium).
- Keine Sekundärblogs oder Foren.

2) AKTUALITÄT:
- Nenne das genaue Datum der verwendeten Zahlen.
- Markiere Informationen älter als 6 Monate mit [Veraltet].

3) INHALT:
- Nenne aktuelle Zahlen zu offenen Stellen und Bewerberzahlen.
- Skizziere Auswirkungen auf Recruiting-Kosten, Employer Branding und Mitarbeiterbindung.
- Führe Unsicherheiten und Szenarien (Best-/Base-/Worst-Case) separat.

4) KENNZEICHNUNG:
- Jede Zahl mit [Quelle, Jahr].
- Eigene Ableitungen als [Einschätzung] markieren.

5) OUTPUT-FORMAT:
- Bullet-Point-Briefing + 3 Handlungspunkte für HR-Leitung.
```

**🎯 Wirkung:** Nachvollziehbar, datengesichert, klar getrennt zwischen Fakt & Einschätzung.

### 2.2 Temperatur & Top-P sinnvoll einstellen

```
Für regulatorische/faktische Inhalte (DSGVO, Arbeitsrecht, Datenschutz):
- Temperature: 0.1–0.3
- Top-P: 0.1–0.5

Für Ideation (Kampagnen, Events, Employer Branding):
- Temperature: 0.6–0.8 (Fakten gesondert prüfen)
- Top-P: 0.7–0.95
```

### 2.3 Eingebaute Faktenprüfung (Fact-Checking)

**✅ Prompt-Template (TK-Quellen):**

```
Erstelle ein Management-Briefing (max. 1 Seite) zur Entwicklung im Healthcare-Recruiting.

VALIDIERUNG:
1) Nutze nur verifizierte Primärquellen (z. B. amtliche Statistik, Bundesagentur für Arbeit, Fachverbände).
2) Markiere pro Aussage:
   - [Quelle: Name, Link/Publikation, Datum]
   - [Einschätzung] für interne Ableitungen
   - [Keine Daten verfügbar] falls Lücke
3) Weise explizit auf Datenstand + Unsicherheiten hin.
4) Füge am Ende eine Prüfliste „Was intern zu verifizieren ist" hinzu.
```

---

## 🔍 Teil 3: Bias erkennen & reduzieren – typische TK-Fälle

### 3.1 Häufige Bias-Arten im Krankenkassen-Umfeld

| Bias-Typ                | TK-Beispiel                                       | Erkennung                                 |
| ----------------------- | -------------------------------------------------- | ----------------------------------------- |
| **Alters-Bias** | „Ältere Mitarbeitende nutzen keine digitalen Tools."              | Gegentest mit differenzierten Altersgruppen-Daten        |
| **Geschlechter-Bias**        | „Pflegekräfte sind immer weiblich." | Rollen/Pronomen vertauschen |
| **Rollen-Bias**         | „IT = männlich, HR = weiblich."    | Geschlechterneutrale Formulierungen testen               |
| **Quellen-Bias**        | „US-Studien = global gültig."                      | EU-/DE-Quellen gegenprüfen                |

### 3.2 A/B-Prompting gegen Bias

**Prompt A (riskant):**

```
Beschreibe die typische TK-Bewerberin für Pflegestellen.
```

**Prompt B (besser):**

```
Beschreibe die Vielfalt der TK-Bewerber:innen für Pflegestellen:
- Altersspannen, Qualifikationen, Lebenssituationen
- Unterschiedliche Motivationen (Karriere, Work-Life-Balance, Sinnstiftung)
- Barrierefreie und kultursensible Aspekte
- Hinweise auf regionale Unterschiede
Vermeide Stereotype. Nutze inklusive Sprache.
```

### 3.3 Perspektivenwechsel für ausgewogene Vorlagen

```
Analysiere Ursachen sinkender Bewerberzahlen aus DREI Blickwinkeln:

1) HR-Leitung/Management:
- Recruiting-Kosten, Employer-Branding-Strategie, Time-to-Hire

2) Bewerber:innen (verschiedene Altersgruppen):
- Bewerbungsprozess-Hürden, Kommunikation, Benefits-Transparenz

3) Mitarbeitende (intern):
- Weiterempfehlungsbereitschaft, Unternehmenskultur, Entwicklungsmöglichkeiten

SYNTHESE:
- Überschneidungen, Zielkonflikte, Quick Wins (30/60/90 Tage)
```

### 3.4 „Devil's Advocate" verpflichtend

```
Nach jeder Empfehlung:
- Was spricht GEGEN die Maßnahme?
- Welche Mitarbeitergruppen könnten benachteiligt werden?
- Gibt es rechtliche oder reputative Risiken?
- Welche unbeabsichtigten Effekte drohen operativ?
```

---

## 🛠️ Teil 4: Praktische Techniken & Tools für HR und Marketing

### 4.1 Selbst-Validierungs-Checkliste (TK-Version)

```markdown
## Management-Unterlagen – KI-Validierung

☐ ZAHLEN
- Summen/Prozente plausibel? Rundungen konsistent?
- Datumsstand jeder Kennzahl notiert?

☐ REGULATORIK
- Aussagen zu DSGVO/Arbeitsrecht/Datenschutz als Zitat/Quelle belegt?
- Keine Rechtsberatung formuliert?

☐ BIAS
- Alle relevanten Mitarbeitergruppen berücksichtigt?
- Sprache inklusiv, keine Stereotype?

☐ QUELLEN
- Primärquelle vorhanden? (Amtlich/Behörde/Fachverband)
- Aktualität ≤ 12 Monate (falls älter: markieren)
- Eigene Einschätzungen klar gekennzeichnet?

☐ VERTRAULICHKEIT
- Keine internen, nicht freigegebenen Daten ausgegeben?
- Personenbezug/DSGVO gewahrt?
```

### 4.2 Prompt-Vorlagen für typische TK-Aufgaben

**📑 Management-Briefing (faktenbasiert):**

```
Temperature: 0.2
Aufgabe: Erstelle ein 1-Seiten-Briefing zur Entwicklung der Mitarbeiterzufriedenheit.

REGELN:
- Nutze NUR bereitgestellte Zahlen/Charts [hier einfügen].
- Keine Schätzungen ohne Kennzeichnung [Einschätzung].
- Nenne für jede Kennzahl: Zeitraum, Einheit, Quelle.
- Trenne „Fakten" und „Implikationen".
- Ende: 3 priorisierte To-Dos (0–90 Tage).
```

**🧪 Entscheidungsvorlage mit Risiken:**

```
Temperature: 0.3
Erstelle eine kompakte Entscheidungsvorlage (max. 12 Bullet Points) zur Einführung eines neuen Benefits-Programms.

Abschnitte:
1) Ziel & Zielgruppe
2) Finanzielle Effekte (Kosten/ROI) – mit Datenstand
3) Compliance-/Operational-Risiken
4) Mitarbeiterwirkung & Kommunikation
5) Abhängigkeiten (IT/Prozess/Schulung)
6) Alternativen + „Devil's Advocate"
```

**💡 Kampagnen-Ideen (mit Bias-Kontrolle):**

```
Temperature: 0.7
Generiere 6 Ideen zur Employer-Branding-Kampagne.

DIVERSITÄT:
- 2 Ideen für Berufseinsteiger:innen
- 2 Ideen für Berufserfahrene (30-50 Jahre)
- 2 Ideen für 50+
- Jede Idee: Barrierefreiheit + Offline/Online-Kanal
- Budgetvarianten: klein/mittel/groß
- Keine Stereotype; inklusiv formulieren.
```

**🧾 Meeting-Protokoll-Entwurf (robust gegen Halluzination):**

```
Temperature: 0.2
Erstelle ein Protokollgerüst basierend auf DIESEM Wortlaut [Transkript/Notizen einfügen].

REGELN:
- NUR Inhalte aus dem Transkript verwenden.
- Keine Ergänzungen oder Interpretationen.
- Offene Punkte als [Action Item] markieren mit Verantwortlichen und Termin.
```

### 4.3 Tool-Hinweise (neutral & sicher)

| Tool/Methode             | Zweck                     | Anwendung                                          |
| ------------------------ | ------------------------- | -------------------------------------------------- |
| **RAG auf interne Doks** | Halluzinationen senken    | Nur freigegebene Richtlinien/Prozesse durchsuchen  |
| **Quellen-Pinning**      | Verlässlichkeit erhöhen   | Nur definierte Primärquellen zulassen              |
| **Custom Instructions**  | Standard-Checks erzwingen | Bias-/Quellenpflicht in jedes Prompt „eingebacken" |
| **Template-Bibliothek**  | Konsistenz                | Ordner mit geprüften Prompts pflegen       |

---

## 🎮 Teil 5: Interaktive Übungen (TK)

### Übung 1: Halluzination erkennen

**KI-Ausgabe:**

> „Das neue Arbeitsschutzgesetz verlangt ab sofort wöchentliche Gesundheitschecks für alle Mitarbeitenden."

**Warnsignale (ankreuzen):**

* [ ] Sehr spezifische, ungeprüfte Behauptung
* [ ] Fehlendes Datum/Quelle
* [ ] Keine Abgrenzung Branche/Unternehmensgröße
* [ ] Kein Hinweis auf Übergangsfristen

### Übung 2: Bias identifizieren

**KI-Ausgabe:**

> „Mitarbeitende ab 55 bevorzugen grundsätzlich Präsenzarbeit und meiden digitale Kommunikationstools."

**Bias-Arten:**

* [ ] Alters-Bias
* [ ] Generalisierung ohne Daten
* [ ] Kanal-Bias (unterstellt Mono-Präferenz)
* [ ] Mangel an Segmentierung (Abteilung, Rolle, Erfahrung)

**Bessere Version:**

> „Arbeitspräferenzen variieren innerhalb der Altersgruppe 55+. Abteilungs- und rollenspezifische Daten sind erforderlich; Angebote sollten flexibel und individuell gestaltbar sein. [Einschätzung]"

---

## ⚠️ Teil 6: Grenzen von LLMs im TK-Betrieb

**Nicht geeignet für:**
🚫 Rechtlich verbindliche Auslegung von Arbeitsrecht/Datenschutz
🚫 Vertrauliche personenbezogene Datenverarbeitung (DSGVO – nur anonymisiert/pseudonymisiert)
🚫 Medizinische oder versicherungsrechtliche Aussagen ohne geprüfte Quelle
🚫 Abschließende Risiko-/Budget-Prognosen ohne menschliche Validierung
🚫 Interne Policies ohne Freigabe „interpretieren"

**Menschliche Expertise nötig bei:**
✅ Finale Rechts-/Compliance-Bewertung
✅ Strategische Entscheidungen & Reputationsfragen
✅ Eskalationen, Versichertenbeschwerden, Medienanfragen
✅ Prüfung lokaler/regionaler Besonderheiten

---

## 📋 Kompakte Checkliste für HR und Marketing

**Vor dem Prompt:**

* [ ] Ziel und Adressat (Management/Team) klar?
* [ ] Temperature passend (Fakt vs. Idee)?
* [ ] Quellen & Aktualität gefordert?
* [ ] Bias-/Devil's-Advocate integriert?

**Nach der Antwort:**

* [ ] Zahlen/Datumsstand plausibel?
* [ ] Primärquellen genannt?
* [ ] Sensible Daten? (falls ja: entfernen)
* [ ] Unsicherheiten/Annahmen markiert?

**Bei Fehlern:**

1. Ausgabe stoppen, unklare Stellen markieren
2. Prompt schärfen (Quellen, Zeitraum, Format)
3. Fakten gegen Primärquelle prüfen
4. Gegenperspektive einholen
5. Lessons Learned ins Prompt-Template übernehmen

---

## 🎯 Quick-Reference: Die 5 wichtigsten Techniken

1. **Step-by-Step:** „Erkläre faktenbasiert, getrennt nach Fakten/Einschätzung…"
2. **Temperatur-Steuerung:** Fakten 0.2, Ideen 0.7
3. **Perspektivenwechsel:** Management ↔ Mitarbeitende ↔ Bewerber:innen
4. **Quellen-Pflicht:** Datum + Primärquelle oder als [Einschätzung] kennzeichnen
5. **Gegentest:** Altersgruppen/Abteilungen/Regionen bewusst variieren

---

## 📎 Bonus: Copy-&-Paste-Prompts für euren Alltag

**1) „Management-auf-einen-Blick" (max. 8 Bullet Points)**

```
Temperature: 0.2
Erstelle eine Executive Summary (max. 8 Bullet Points) zum Thema: [Thema].

REGELN:
- Jede Zahl mit Datum + Quelle.
- Trennung: Fakten / Auswirkungen / Entscheidungen.
- Ende: 3 To-Dos (Owner + Termin).
```

**2) „Presse/Medien-Check" (risikoarm)**

```
Temperature: 0.3
Fasse Medienberichte zu [Thema] zusammen.

REGELN:
- Nur seriöse Primär-/Leitmedien.
- Keine Spekulationen. Zitiere knapp, paraphrasiere sonst.
- Markiere Widersprüche und fehlende Bestätigungen.
```

**3) „Meeting-Protokoll mit Action Items"**

```
Temperature: 0.2
Erzeuge ein präzises Protokoll aus folgendem Text: [Transkript].

FORMAT:
- Beschlüsse (mit Datum)
- Action Items: [Owner] – [Deadline] – [Messkriterium]
- Offene Risiken/Abhängigkeiten
```

**4) „Datenschutz-Extrakt" (ohne Rechtsberatung)**

```
Temperature: 0.2
Extrahiere aus diesem Dokument die relevanten DSGVO-Anforderungen für die TK. 
Kennzeichne Originalzitate mit Anführungszeichen und Seitenangabe.
Führe mögliche Auswirkungen als [Einschätzung] separat auf.
```

**5) „Kampagnenideen ohne Bias"**

```
Temperature: 0.7
Erstelle 5 Kampagnenideen für [Zielsegment] zur Steigerung von [Zielgröße].
Jede Idee: Kanal (on/offline), Barrierefreiheit, Messgröße, Budget (S/M/L).
Vermeide Stereotype; nutze inklusive Sprache.
```

---


