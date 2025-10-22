# Seminar-Handout (für Assistenz der Vorstände in PSD Banken)

## Halluzinationen & Bias bei LLMs im Bankalltag vermeiden

---

## 📚 Teil 1: Grundlagen – mit Fokus Banking

### Warum „halluzinieren“ LLMs – und warum ist das im Bankkontext heikel?

LLMs erzeugen sprachlich plausible Antworten auf Basis von Wahrscheinlichkeiten – nicht auf Basis von „Verstehen“. Im regulierten Umfeld einer Bank führt das zu besonderen Risiken:

* 🔄 **Mustervervollständigung:** Fehlende Fakten (z. B. zu MaRisk/BAIT-Passagen) werden glaubwürdig „ergänzt“.
* 📊 **Überanpassung:** Aus einzelnen Presseartikeln werden allgemeine Branchenaussagen abgeleitet.
* 🎯 **Kontext-Drift:** Fragen zu Zinsänderungen vermischen sich mit veralteten Meldungen.
* ⚡ **Temperatur:** Höhere Kreativität erhöht das Risiko falscher, aber überzeugender Antworten.

**Bank-spezifische Folgen:** Falsche Vorstandsbriefings, fehlerhafte Aufsichtsvorlagen, unzulässige Kundenkommunikation, Reputationsrisiken.

### Warum entsteht Bias – und wie zeigt er sich in Banken?

Bias (systematische Verzerrung) spiegelt unausgewogene Trainingsdaten wider:

* 🏛️ **Regulatorik-Bias:** Dominanz internationaler (nicht-deutscher) Regulierungsquellen.
* 🌍 **Kultur-/Sprach-Bias:** Englische/US-Perspektive dominiert, deutsche Institute unterrepräsentiert.
* 👥 **Rollen-Bias:** Veraltete Stereotype zu Funktionen (z. B. „Beratung = männlich“).
* ✅ **Confirmation Bias:** Modell bestätigt vermutete Trends (z. B. „Filialschließungen = immer sinnvoll“), ohne lokale Daten zu prüfen.

---

## 🎯 Teil 2: Halluzinationen erkennen & vermeiden – für Vorstandsassistenz

### 2.1 Struktur-Prompts statt „kurzer Frage“

**❌ Fehleranfälliger Prompt (Bank):**

```
Wie ist der aktuelle Stand der EZB-Zinsen und was bedeutet das für unser Einlagengeschäft?
```

**✅ Belastbarer Prompt mit „Step-by-Step“:**

```
Erstelle eine faktenbasierte Kurzlage (max. 10 Sätze) zu Leitzinsen und Auswirkungen auf das Einlagengeschäft.

1) QUELLEN:
- Nutze NUR offizielle/verifizierte Quellen (z. B. Notenbank, Aufsicht, Bundesstatistik).
- Keine Sekundärblogs oder Foren.

2) AKTUALITÄT:
- Nenne das genaue Datum der verwendeten Zahlen.
- Markiere Informationen älter als 6 Monate mit [Veraltet].

3) INHALT:
- Nenne den aktuellen Leitzins und das Datum der Entscheidung.
- Skizziere Auswirkungen auf Marge, Passivseite und Kundennachfrage.
- Führe Unsicherheiten und Szenarien (Best-/Base-/Worst-Case) separat.

4) KENNZEICHNUNG:
- Jede Zahl mit [Quelle, Jahr].
- Eigene Ableitungen als [Einschätzung] markieren.

5) OUTPUT-FORMAT:
- Bullet-Point-Briefing + 3 Handlungspunkte für den Vorstand.
```

**🎯 Wirkung:** Nachvollziehbar, datengesichert, klar getrennt zwischen Fakt & Einschätzung.

### 2.2 Temperatur & Top-P sinnvoll einstellen

```
Für regulatorische/faktische Inhalte (MaRisk, BAIT, DSGVO):
- Temperature: 0.1–0.3
- Top-P: 0.1–0.5

Für Ideation (Kampagnen, interne Events, Change-Kommunikation):
- Temperature: 0.6–0.8 (Fakten gesondert prüfen)
- Top-P: 0.7–0.95
```

### 2.3 Eingebaute Faktenprüfung (Fact-Checking)

**✅ Prompt-Template (Bankquellen):**

```
Erstelle ein Vorstandsbriefing (max. 1 Seite) zur Entwicklung von Baufinanzierungen.

VALIDIERUNG:
1) Nutze nur verifizierte Primärquellen (z. B. amtliche Statistik, Aufsicht, Zentralbank).
2) Markiere pro Aussage:
   - [Quelle: Name, Link/Publikation, Datum]
   - [Einschätzung] für interne Ableitungen
   - [Keine Daten verfügbar] falls Lücke
3) Weisen Sie explizit auf Datenstand + Unsicherheiten hin.
4) Füge am Ende eine Prüfliste „Was intern zu verifizieren ist“ hinzu.
```

---

## 🔍 Teil 3: Bias erkennen & reduzieren – typische Bankfälle

### 3.1 Häufige Bias-Arten im Bankumfeld

| Bias-Typ                | Bankbeispiel                                       | Erkennung                                 |
| ----------------------- | -------------------------------------------------- | ----------------------------------------- |
| **Region-/Filial-Bias** | „Stadtfilialen sind immer defizitär.“              | Gegentest mit Land-/Suburban-Daten        |
| **Produkt-Bias**        | „Junge Kund:innen wollen nur App, keine Beratung.“ | Kohortenvergleich & Kundensegmente prüfen |
| **Rollen-Bias**         | „Kreditanalyse = männlich, Service = weiblich.“    | Rollen/Pronomen vertauschen               |
| **Quellen-Bias**        | „US-Studien = global gültig.“                      | EU-/DE-Quellen gegenprüfen                |

### 3.2 A/B-Prompting gegen Bias

**Prompt A (riskant):**

```
Beschreibe die typische PSD-Kundin für Konsumentenkredite.
```

**Prompt B (besser):**

```
Beschreibe die Vielfalt der PSD-Kund:innen für Konsumentenkredite:
- Altersspannen, Einkommenssituationen, Lebenslagen
- Unterschiedliche Kontaktkanäle (Filiale, Telefon, App)
- Barrierefreie und kultursensible Aspekte
- Hinweise auf regionale Unterschiede
Vermeide Stereotype. Nutze inklusive Sprache.
```

### 3.3 Perspektivenwechsel für ausgewogene Vorlagen

```
Analysiere Ursachen sinkender Giro-Neukunden aus DREI Blickwinkeln:

1) Vorstand/Ertrag:
- Marge, Pricing, Cross-Selling-Potenziale

2) Kund:innen (18–30):
- Onboarding-Hürden, UX, Multibanking-Verhalten

3) Compliance/Betrieb:
- KYC-Aufwand, Prozesszeiten, Ablehnungsgründe

SYNTHESE:
- Überschneidungen, Zielkonflikte, Quick Wins (30/60/90 Tage)
```

### 3.4 „Devil’s Advocate“ verpflichtend

```
Nach jeder Empfehlung:
- Was spricht GEGEN die Maßnahme?
- Welche Kundengruppen könnten benachteiligt werden?
- Gibt es rechtliche oder reputative Risiken?
- Welche unbeabsichtigten Effekte drohen operativ?
```

---

## 🛠️ Teil 4: Praktische Techniken & Tools für die Assistenz

### 4.1 Selbst-Validierungs-Checkliste (Bankversion)

```markdown
## Vorstandsunterlagen – KI-Validierung

☐ ZAHLEN
- Summen/Prozente plausibel? Rundungen konsistent?
- Datumsstand jeder Kennzahl notiert?

☐ REGULATORIK
- Aussagen zu MaRisk/BAIT/DSGVO als Zitat/Quelle belegt?
- Keine Rechtsberatung formuliert?

☐ BIAS
- Alle relevanten Kundensegmente berücksichtigt?
- Sprache inklusiv, keine Stereotype?

☐ QUELLEN
- Primärquelle vorhanden? (Amtlich/Behörde/Notenbank)
- Aktualität ≤ 12 Monate (falls älter: markieren)
- Eigene Einschätzungen klar gekennzeichnet?

☐ VERTRAULICHKEIT
- Keine internen, nicht freigegebenen Daten ausgegeben?
- Personenbezug/DSGVO gewahrt?
```

### 4.2 Prompt-Vorlagen für typische Bankaufgaben

**📑 Vorstandsbriefing (faktenbasiert):**

```
Temperature: 0.2
Aufgabe: Erstelle ein 1-Seiten-Briefing zur Entwicklung der Passivseite (Sichteinlagen/Termineinlagen).

REGELN:
- Nutze NUR bereitgestellte Zahlen/Charts [hier einfügen].
- Keine Schätzungen ohne Kennzeichnung [Einschätzung].
- Nenne für jede Kennzahl: Zeitraum, Einheit, Quelle.
- Trenne „Fakten“ und „Implikationen“.
- Ende: 3 priorisierte To-Dos (0–90 Tage).
```

**🧪 Entscheidungsvorlage mit Risiken:**

```
Temperature: 0.3
Erstelle eine kompakte Entscheidungsvorlage (max. 12 Bullet Points) zur Einführung eines neuen Kontomodells.

Abschnitte:
1) Ziel & Zielgruppe
2) Finanzielle Effekte (Ertrag/Kosten) – mit Datenstand
3) Compliance-/Operational-Risiken
4) Kund:innenwirkung & Kommunikation
5) Abhängigkeiten (IT/Prozess/Schulung)
6) Alternativen + „Devil’s Advocate“
```

**💡 Kampagnen-Ideen (mit Bias-Kontrolle):**

```
Temperature: 0.7
Generiere 6 Ideen zur Einlagenkampagne.

DIVERSITÄT:
- 2 Ideen für Berufseinsteiger:innen
- 2 Ideen für Familien
- 2 Ideen für 55+
- Jede Idee: Barrierefreiheit + Offline/Online-Kanal
- Budgetvarianten: klein/mittel/groß
- Keine Stereotype; inklusiv formulieren.
```

**🧾 Sitzungsprotokoll-Entwurf (robust gegen Halluzination):**

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
| **Custom Instructions**  | Standard-Checks erzwingen | Bias-/Quellenpflicht in jedes Prompt „eingebacken“ |
| **Template-Bibliothek**  | Konsistenz                | Seminar-Ordner mit geprüften Prompts pflegen       |

---

## 🎮 Teil 5: Interaktive Übungen (Bank)

### Übung 1: Halluzination erkennen

**KI-Ausgabe:**

> „Das neue Meldewesen-Update verlangt ab sofort täglich eine LCR-Meldung.“

**Warnsignale (ankreuzen):**

* [ ] Sehr spezifische, ungeprüfte Behauptung
* [ ] Fehlendes Datum/Quelle
* [ ] Keine Abgrenzung Land/Regime
* [ ] Kein Hinweis auf Übergangsfristen

### Übung 2: Bias identifizieren

**KI-Ausgabe:**

> „Filialkund:innen ab 60 bevorzugen grundsätzlich Barzahlung und meiden Apps.“

**Bias-Arten:**

* [ ] Alters-Bias
* [ ] Generalisierung ohne Daten
* [ ] Kanal-Bias (unterstellt Mono-Kanal)
* [ ] Mangel an Segmentierung (Region, Bildung, Affinität)

**Bessere Version:**

> „Nutzungspräferenzen variieren innerhalb der Altersgruppe 60+. Segment- und regionalspezifische Daten sind erforderlich; Angebote sollten kanalübergreifend und barrierefrei gestaltet werden. [Einschätzung]“

---

## ⚠️ Teil 6: Grenzen von LLMs im Bankbetrieb

**Nicht geeignet für:**
🚫 Rechtlich verbindliche Auslegung von Regulatorik
🚫 Vertrauliche personenbezogene Datenverarbeitung (DSGVO – nur anonymisiert/pseudonymisiert)
🚫 Echtzeit- oder Kursdaten ohne geprüfte Quelle
🚫 Abschließende Risiko-/Finanzprognosen ohne menschliche Validierung
🚫 Interne Policies ohne Freigabe „interpretieren“

**Menschliche Expertise nötig bei:**
✅ Finale Rechts-/Compliance-Bewertung
✅ Strategische Entscheidungen & Reputationsfragen
✅ Eskalationen, Kund:innenbeschwerden, Medienanfragen
✅ Prüfung lokaler/regionaler Besonderheiten

---

## 📋 Kompakte Checkliste für die Vorstandsassistenz

**Vor dem Prompt:**

* [ ] Ziel und Adressat (Vorstand/Ausschuss) klar?
* [ ] Temperature passend (Fakt vs. Idee)?
* [ ] Quellen & Aktualität gefordert?
* [ ] Bias-/Devil’s-Advocate integriert?

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

1. **Step-by-Step:** „Erkläre faktenbasiert, getrennt nach Fakten/Einschätzung…“
2. **Temperatur-Steuerung:** Fakten 0.2, Ideen 0.7
3. **Perspektivenwechsel:** Vorstand ↔ Kund:innen ↔ Compliance/IT
4. **Quellen-Pflicht:** Datum + Primärquelle oder als [Einschätzung] kennzeichnen
5. **Gegentest:** Segmente/Kanäle/Regionen bewusst variieren

---

## 📎 Bonus: Copy-&-Paste-Prompts für euren Alltag

**1) „Vorstand-auf-einen-Blick“ (max. 8 Bullet Points)**

```
Temperature: 0.2
Erstelle eine Executive Summary (max. 8 Bullet Points) zum Thema: [Thema].

REGELN:
- Jede Zahl mit Datum + Quelle.
- Trennung: Fakten / Auswirkungen / Entscheidungen.
- Ende: 3 To-Dos (Owner + Termin).
```

**2) „Presse/Medien-Check“ (risikoarm)**

```
Temperature: 0.3
Fasse Medienberichte zu [Thema] zusammen.

REGELN:
- Nur seriöse Primär-/Leitmedien.
- Keine Spekulationen. Zitiere knapp, paraphrasiere sonst.
- Markiere Widersprüche und fehlende Bestätigungen.
```

**3) „Meeting-Protokoll mit Action Items“**

```
Temperature: 0.2
Erzeuge ein präzises Protokoll aus folgendem Text: [Transkript].

FORMAT:
- Beschlüsse (mit Datum)
- Action Items: [Owner] – [Deadline] – [Messkriterium]
- Offene Risiken/Abhängigkeiten
```

**4) „Regulatorik-Extrakt“ (ohne Rechtsberatung)**

```
Temperature: 0.2
Extrahiere aus diesem Dokument die relevanten Anforderungen für unsere Bank. 
Kennzeichne Originalzitate mit Anführungszeichen und Seitenangabe.
Führe mögliche Auswirkungen als [Einschätzung] separat auf.
```

**5) „Kampagnenideen ohne Bias“**

```
Temperature: 0.7
Erstelle 5 Kampagnenideen für [Zielsegment] zur Steigerung von [Zielgröße].
Jede Idee: Kanal (on/offline), Barrierefreiheit, Messgröße, Budget (S/M/L).
Vermeide Stereotype; nutze inklusive Sprache.
```

---

**Hinweis für das Seminar:**
Speichert die besten Prompts als geprüfte Templates, hinterlegt Quellenlisten (nur Primärquellen), und nutzt RAG auf **freigegebene** interne Dokumente. So senkt ihr Halluzinationen, bleibt compliant – und liefert dem Vorstand verlässlich aufbereitete Unterlagen.
