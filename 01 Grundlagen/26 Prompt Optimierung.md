
# 🏁 Quick Start: In 10 Minuten zum besseren Prompt

**Was Sie brauchen:** Einen Chat mit ChatGPT (neuer, leerer Chat).
**Ziel:** Einen eigenen Prompt (z. B. „schreibe eine Kundenmail…“) **bewerten lassen** und danach **automatisch verbessern**.

## Schritt 1: Ihren Arbeits-Prompt festlegen

Formulieren Sie kurz, was Sie von ChatGPT wollen. Beispiel:

> „Erstelle eine kurze, freundliche Kundenmail (max. 120 Wörter) zur Einführung unseres Nachhaltigkeitskontos. Zielgruppe: Bestandskunden. Abschluss mit klarem Call-to-Action.“

Notieren Sie ihn separat (z. B. in Word).

## Schritt 2: Evaluations-Prompt einfügen

1. Öffnen Sie einen **neuen Chat**.
2. **Kopieren** Sie den Evaluations-Prompt (siehe „Prompts zum Kopieren“ weiter unten) **vollständig** in den Chat und senden ihn ab.
3. Direkt danach **fügen Sie Ihren Arbeits-Prompt** ein – **zwischen drei Backticks** `…` – und senden.
  
  

**Ergebnis, das Sie erwarten:**
Ein Bewertungsbericht mit **Punktzahlen (1–5)** zu 35 Kriterien + **konkreten Verbesserungsvorschlägen** (z. B. „Zielgruppe präzisieren“, „Wortzahl begrenzen“, „Ton spezifizieren“).

## Schritt 3: Refinement-Prompt einfügen (Verbessern lassen)

1. **Kopieren** Sie den Refinement-Prompt (siehe unten) in **denselben Chat** und senden.
2. **Fügen Sie den Bewertungsbericht** (aus Schritt 2) **unter** den Refinement-Prompt ein oder verweisen Sie mit „Nutze den letzten Bericht“.
3. Senden.

**Ergebnis, das Sie erwarten:**
Eine **überarbeitete, präzisere Version Ihres Arbeits-Prompts** – direkt kopierfertig.

## Schritt 4: Optional erneut schleifen

Wenn der verbesserte Prompt noch nicht passt:

* **Wiederholen** Sie Schritt 2 (Bewerten) → Schritt 3 (Verbessern), bis der Prompt sitzt.

---

# 🧠 Woran erkenne ich, dass mein Prompt „gut“ ist?

Ein **guter Prompt** ist:

* **konkret** (Zielgruppe, Ton, Länge, Format),
* **machbar** (keine vagen Bitten wie „mach’s perfekt“),
* **prüfbar** (klare Kriterien, z. B. Wortanzahl, CTA enthalten).

**Minicheck (30 Sek.):**

* Zielgruppe klar?
* Ton/Schreibstil benannt?
* Länge/Format definiert (z. B. max. 120 Wörter, E-Mail, Bulletpoints)?
* Zweck/Erfolgskriterium sichtbar (z. B. „Teilnahme an Infoabend fördern“)?

---

# 🏦 Volksbank-Beispiele (zum direkten Üben)

## Beispiel A: Kundenmail – Nachhaltigkeitskonto

**Ihr erster Arbeits-Prompt (Start):**

```
Schreibe eine freundliche E-Mail über unser Nachhaltigkeitskonto.
```

**So wenden Sie die Kette an:**

1. Evaluations-Prompt senden → dann diesen Arbeits-Prompt zwischen `…` senden.
2. Refinement-Prompt senden → mit dem erzeugten Bewertungsbericht.

**Typisches Ergebnis (verbesserter Prompt):**

```
Erstelle eine freundliche E-Mail (max. 120 Wörter) für Bestandskunden der Volksbank Musterstadt, 
die unser neues Nachhaltigkeitskonto vorstellt. 
Ton: vertrauensvoll, klar, ohne Fachjargon. 
Inhalte: 1) kurze Nutzenübersicht (regional, transparent, impact-bezogen), 
2) Gebührenhinweis in einem Satz, 
3) klarer Call-to-Action: „Jetzt Beratungstermin vereinbaren“ (mit Link-Platzhalter).
```

## Beispiel B: Stellenausschreibung – Auszubildende Bankkaufleute

**Arbeits-Prompt (Start):**

```
Schreibe eine Stellenanzeige für Azubis.
```

**Nach Anwendung der Kette (typisches Ergebnis):**

```
Erstelle eine Stellenanzeige (ca. 180–220 Wörter) für „Ausbildung Bankkaufmann/Bankkauffrau (m/w/d)“ bei der Volksbank Musterstadt. 
Zielgruppe: Schulabgänger (Realschule/Abitur). 
Ton: motivierend, bodenständig, klar. 
Abschnitte: 1) Wer wir sind (regional, genossenschaftliche Werte), 
2) Deine Aufgaben (kundenorientiert, Einblick in Beratung/Service), 
3) Was wir bieten (faire Vergütung, Übernahmeperspektive, Weiterbildung), 
4) Bewerbung (Frist, Ansprechpartner, Link).
```

## Beispiel C: Interner Prozess – Anweisung Kassenabschluss

**Arbeits-Prompt (Start):**

```
Erkläre den Kassenabschluss.
```

**Nach Anwendung der Kette:**

```
Erstelle eine klare, schrittweise Arbeitsanweisung (max. 12 Schritte) für den täglichen Kassenabschluss in der Filiale. 
Zielgruppe: neue Mitarbeitende. 
Ton: sachlich, präzise. 
Beziehe ein: Verantwortlichkeiten, Prüfschritte, Vier-Augen-Prinzip, Dokumentationsort, typische Fehlerquellen und Eskalationsweg. 
Gib am Ende eine 5-Punkte-Checkliste zum Abhaken aus.
```

---

# ✅ Do / ❌ Don’t (häufige Anfängerfehler)

**✅ Do**

* Immer Zielgruppe, Zweck, Ton, Länge/Format angeben.
* Bei sensiblen Themen (Gebühren, Compliance) um **prüfbare** Formulierungen bitten.
* Bei Listen: gewünschte **Anzahl** oder **maximale Wortzahl** nennen.

**❌ Don’t**

* Keine vagen Bitten wie „Mach’s perfekt“.
* Nicht ohne Backticks ``` arbeiten, wenn der Evaluations-Prompt es verlangt.
* Nicht zu viele Wünsche in einem Satz mischen – **lieber auflisten**.

---

# 🧰 Mini-Vorlagen (zum Kopieren)

**Marketing-Text (Website):**

```
Erstelle einen Webtext (80–120 Wörter) für die Volksbank [Ort], 
Zielgruppe: [z. B. junge Erwachsene 18–30], 
Thema: [Produkt], 
Ton: [z. B. modern, sympathisch], 
Pflicht: [2 Nutzenpunkte + 1 CTA], 
Vermeide: [Fachjargon/Abkürzungen], 
Format: 1 kurzer Absatz + Bullet-Liste (3 Punkte) + Abschluss-CTA.
```

**E-Mail an Kunden:**

```
Erzeuge eine Kundenmail (max. 130 Wörter) zum Thema [X]. 
Zielgruppe: [z. B. Bestandskunden Privatkunden], 
Ton: [z. B. vertrauensvoll, klar], 
Enthalten: [Nutzen in 2 Sätzen], [konkreter nächster Schritt mit Link-Platzhalter], 
Betreff-Vorschlag: 2 Varianten.
```

**Interne Anweisung:**

```
Erstelle eine Schritt-für-Schritt-Anweisung (max. 10 Schritte) für [Prozess].
Zielgruppe: [Rolle], 
Ton: sachlich, präzise, 
Enthalten: Verantwortlichkeiten, Prüfpunkte, Dokumentationsort, Eskalationsweg, 
Am Ende: 5-Punkte-Checkliste.
```

---

# 🧩 Prompts zum Kopieren (deutsche Version, vollständig)

## 1) **Evaluations-Prompt (Deutsch)**

> **So nutzen Sie ihn:**
>
> 1. In neuem Chat **komplett** einfügen und senden.
> 2. **Direkt danach** Ihren Arbeits-Prompt zwischen `…` einfügen und senden (siehe Quick Start, Schritt 2).

````markdown
🔁 Prompt Evaluationskette 2.0 (Deutsch)

Du bist ein **leitender Prompt-Ingenieur** und nimmst an der **Prompt Evaluationskette** teil – einem Qualitätssystem zur Verbesserung von Prompts durch strukturierte Bewertung und iterative Rückmeldungen.  
Deine Aufgabe ist es, einen gegebenen Prompt anhand der **nachfolgenden 35 Kriterien** zu analysieren, zu bewerten und gezielte Verbesserungsvorschläge zu geben.

### 📋 Anweisungen
1. Lies den Prompt innerhalb der drei Backticks (```).
2. Bewerte ihn anhand der **35 Kriterien**.
3. Für jedes Kriterium:
   - Vergib eine **Bewertung von 1 (schwach) bis 5 (exzellent)**.
   - Nenne **eine Stärke**.
   - Nenne **eine konkrete Verbesserung**.
   - Gib eine kurze **Begründung (1–2 Sätze)**.
4. Überprüfe stichprobenartig 3–5 Bewertungen auf Konsistenz.
5. Simuliere eine **kritische Perspektive** – wie könnte ein anderer Experte deine Einschätzung hinterfragen?
6. Notiere **unausgesprochene Annahmen oder fehlenden Kontext**.
7. Summiere den **Gesamtwert (max. 175 Punkte)**.
8. Gib **7–10 konkrete Verbesserungsvorschläge**.

### 🧩 Bewertungskriterien (35)
1. Klarheit & Genauigkeit  
2. Kontext / Hintergrund  
3. Aufgabenbeschreibung  
4. Umsetzbarkeit im Modell  
5. Widerspruchsfreiheit  
6. Passung zur Situation / Rolle  
7. Ausgabestil und Format  
8. Nutzung einer Persona  
9. Logische Schrittfolge  
10. Struktur / Nummerierung  
11. Balance zwischen Kürze & Tiefe  
12. Wiederholbarkeit / Iterationsfähigkeit  
13. Nutzung von Beispielen  
14. Umgang mit Unsicherheiten  
15. Minimierung von Halluzinationen  
16. Wissen über Modellgrenzen  
17. Zielgruppenbezug  
18. Stil- oder Ton-Vorgaben  
19. Kontextbindung über mehrere Runden  
20. Reflexionsaufforderung  
21. Umgang mit divergenter / konvergenter Logik  
22. Hypothetische Perspektivwechsel  
23. Sicherer Fehlermodus  
24. Steigende Komplexität  
25. Bezug zu Bewertungsmaßstäben  
26. Kalibrierungshinweise  
27. Validierung der Ausgabe  
28. Zeit-/Aufwandsabschätzung  
29. Ethik / Bias-Vermeidung  
30. Offenlegung von Grenzen  
31. Zusammenfassungsfähigkeit  
32. Interdisziplinäre Brücken  
33. Emotionale Tonsteuerung  
34. Risikobewertung der Ausgabe  
35. Selbstkorrektur-Mechanismen

### 📊 Ausgabeformat
1. Klarheit & Genauigkeit – X/5  
   - Stärke: [Text]  
   - Verbesserung: [Text]  
   - Begründung: [Text]

... (bis 35)

💯 Gesamtpunkte: X/175  
🛠️ Verbesserungszusammenfassung:
- [Vorschlag 1]  
- [Vorschlag 2]  
- [Vorschlag 3]  
...

### Zielgruppe
Professionelle Prompt-Ersteller, KI-Trainer oder Führungskräfte, die systematisch die Qualität ihrer KI-Eingaben verbessern möchten.

### 📥 Prompt zur Bewertung
Füge deinen Prompt **zwischen** die Backticks (```):

````

[Dein Prompt hier]

```
```

## 2) **Refinement-Prompt (Deutsch)**

> **So nutzen Sie ihn:**
>
> 1. Nach der Bewertung **in denselben Chat** einfügen.
> 2. Den Bewertungsbericht (oder „Nutze den letzten Bewertungsbericht“) darunter einfügen und senden.

````markdown
🔁 Prompt-Verfeinerungskette 2.0 (Deutsch)

Du bist ein **leitender Prompt-Ingenieur** und nimmst an der **Prompt-Verfeinerungskette** teil – einem System zur strukturierten Überarbeitung von Prompts auf Basis vorheriger Bewertungen.  
Deine Aufgabe ist es, den ursprünglichen Prompt anhand der vorliegenden Bewertung gezielt zu **verbessern**, ohne Zweck, Stil oder Rolle zu verfälschen.

### 🔧 Verfeinerungs-Anleitung
1. Lies die vollständige Bewertung (35 Kriterien + Verbesserungsvorschläge).
2. Wende relevante Verbesserungen an:
   - Mehr Klarheit, Präzision, Kürze
   - Entfernung von Redundanz und Widersprüchen
   - Optimierung von Struktur, Formatierung und Logik
3. Erhalte dabei:
   - Den ursprünglichen **Zweck**
   - Den definierten **Stil / die Persona**
4. Zeige **Vorher/Nachher** kurz (1–2 Zeilen). Beispiel:
   - Vorher: „Schreibe etwas über Nachhaltigkeit.“
   - Nachher: „Erstelle einen 100-Wörter-Text über nachhaltige Geldanlage, sachlich und für Bankkunden geeignet.“
5. Falls keine Beispiele möglich sind, erkläre kurz, was verbessert wurde und warum.
6. **Checkliste (Pflicht):**
   - ✅ Alle Vorschläge berücksichtigt
   - ✅ Keine Abweichung vom ursprünglichen Ziel
   - ✅ Verbesserte Lesbarkeit und Logik

### 🛠️ Ausgabeformat
Gib **nur** den überarbeiteten Prompt in einer Code-Box (``` … ```), ohne weitere Kommentare aus.

### ⏱️ Zeitbedarf
Typischerweise 5–10 Minuten pro Prompt.

### Eingabe
Nutze den **letzten Bewertungsbericht** oder füge ihn hier ein.
````

---

# 🗺️ Entscheidungshelfer: Welchen Prompt nutze ich wann?

* **Ich will wissen, ob mein Prompt gut ist** → **Evaluations-Prompt**
* **Ich will eine bessere Version desselben Prompts** → **Refinement-Prompt**
* **Ich will beides** → Erst Evaluation, dann Refinement (im selben Chat)

---

# 🧩 Mini-Übung (5 Minuten)

1. Nehmen Sie einen echten Textbedarf (z. B. kurze Kundenmail).
2. Schritt-für-Schritt wie im Quick Start.
3. Prüfen Sie das Ergebnis mit der 30-Sek.-Minicheckliste.
4. Speichern Sie den finalen Prompt in Ihrer **internen Prompt-Bibliothek**.

---

# ❓FAQ (Einsteiger)

**Muss ich die Backticks ``` wirklich nutzen?**
Ja. So erkennt ChatGPT eindeutig, **was** bewertet/verbessert werden soll.

**Was, wenn die Bewertung zu lang ist?**
Kein Problem. Kopieren Sie sie vollständig unter den Refinement-Prompt **oder** schreiben Sie „Nutze den letzten Bewertungsbericht“.

**Kann ich die 35 Kriterien kürzen?**
Ja. Für Einsteiger reicht die Anwendung „wie geliefert“. Später können Sie Kriterien streichen/ergänzen.

**Darf ich den verbesserten Prompt direkt verwenden?**
Ja – genau dafür ist er gedacht.

---

# 📦 Bonus: 1-Seiten-Cheat-Sheet (druckbar)

1. **Ziel & Zielgruppe nennen**
2. **Ton & Format definieren** (Wörter, Listen, CTA)
3. **Evaluieren** (Evaluations-Prompt)
4. **Verbessern** (Refinement-Prompt)
5. **Ergebnis testen** (Minicheckliste)
6. **Finalen Prompt speichern** (Bibliothek)

---


