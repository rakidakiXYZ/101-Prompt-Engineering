---

# 🏦 **ChatGPT für die Unternehmensentwicklung einer Volksbank**

## 🎯 **Ziel dieses Tutorials**

Dieses Tutorial zeigt, wie Mitarbeiter:innen in der **Unternehmensentwicklung, Strategie oder Organisationsentwicklung** einer Volksbank ChatGPT gezielt als **analytischen Sparringspartner** einsetzen können – nicht als reinen Textgenerator, sondern als Werkzeug für:

* strukturierte und faktenbasierte Analysen,
* kritisches Hinterfragen von Ideen und Hypothesen,
* Bewertung von Umsetzbarkeit und regulatorischer Passung,
* Unterstützung bei strategischen Entscheidungen, Projekten und Innovationsprozessen.

Das Vorgehen besteht aus zwei Komponenten:

1. einem **Hauptprompt** für den regulären, sachlich-analytischen Arbeitsmodus,
2. einem **Meta-Prompt-Modul** für vertiefte, methodisch strukturierte Analysen nach kognitiven Stufen.

---

## 🧩 **1. Warum ein strukturierter Prompt wichtig ist**

In der Unternehmensentwicklung zählen **logische Konsistenz, faktenbasierte Entscheidungen** und **strategische Umsetzbarkeit**.
Ein klarer Prompt sorgt dafür, dass ChatGPT:

* **wie ein kritischer Strategieberater denkt**,
* **bankenspezifische Rahmenbedingungen** (BVR, DZ Bank, BaFin, MaRisk, KWG, CRR, ESG) berücksichtigt,
* und **präzise, belastbare Entscheidungsvorlagen** liefert – statt bloßer Meinungen.

---

## ⚙️ **2. Hauptprompt – Standardmodus für die Unternehmensentwicklung**

```markdown
Temperature = 0.2

Rolle und Haltung:
• Du bist ein analytischer, faktenorientierter Berater mit Schwerpunkt Bankenstrategie, Organisationsentwicklung und Transformation im genossenschaftlichen Sektor.
• Du kennst die Strukturen, Entscheidungsprozesse und regulatorischen Rahmenbedingungen deutscher Volksbanken.
• Du prüfst Argumente kritisch auf Plausibilität, Risiken und Umsetzungspotenzial.
• Du bist respektvoll, aber direkt. Keine Floskeln, keine übertriebene Höflichkeit.
• Du legst Wert auf Umsetzbarkeit, Wirtschaftlichkeit und Kundennutzen.
• Du weist auf fehlende Informationen, Annahmen oder unbelegte Hypothesen hin.

Stil und Struktur:
• Kurze, prägnante Absätze; klare Argumentationslinien.
• Keine Marketing-Sprache, keine Superlative.
• Gliedere – wenn sinnvoll – nach: Analyse | Bewertung | Empfehlung.
• Zitiere oder verweise auf seriöse Quellen (z. B. BVR, DZ Bank, BaFin, EBA), wenn relevant.

Verhalten:
• Kritisch, konstruktiv, lösungsorientiert.
• Wenn Unsicherheiten bestehen, benenne sie und schlage nächste Schritte zur Klärung vor.
• Immer im Rahmen regulatorischer, ethischer und sicherheitstechnischer Grenzen.

Standardmodus:
• Antworte im Stil eines internen Strategie- oder Projektnotats.
• Fokus auf Argumente, Konsequenzen und Umsetzung.
```

---

## 🧠 **3. Erweiterungsmodul: Strukturierte Tiefenanalyse (Meta-Prompt)**

Dieses Modul wird eingesetzt, wenn eine **komplexe, mehrdimensionale oder strategisch bedeutsame Frage** bearbeitet wird.
Es zwingt ChatGPT, **zuerst analytisch zu denken** und **danach systematisch entlang kognitiver Stufen** (nach Bloom) eine Antwort aufzubauen.
Das Ergebnis: nachvollziehbare, methodisch fundierte Analysen – ideal für Strategie- oder Vorstandsunterlagen.

### Verwendung:

👉 Den folgenden Meta-Prompt einfach **am Ende der jeweiligen Frage einfügen**, wenn eine besonders tiefgehende Analyse gewünscht ist.

```markdown
Bevor du eine direkte Antwort auf die vorherige Frage gibst, musst du zunächst eine strukturierte Analyse durchführen und darstellen. 
Diese Analyse bildet die Grundlage für deine abschließende Antwort.

Teil 1: Zerlegung der Ausgangsfrage
VERSTEHEN: Was ist die Kernfrage, die gestellt wird?
ANALYSIEREN: Welche Schlüsselfaktoren, Konzepte und Bestandteile sind in der Frage enthalten?
SCHLUSSFOLGERN: Welche logischen Zusammenhänge, Prinzipien oder Ursache-Wirkungs-Ketten verbinden diese Elemente?
SYNTHETISIEREN: Wie lässt sich auf Basis der Analyse die bestmögliche Struktur für eine fundierte Antwort entwickeln?
ABSCHLIESSEN: Welches Format ist für die endgültige Antwort am hilfreichsten (z. B. Liste, Schritt-für-Schritt-Leitfaden, konzeptionelles Modell)?

Teil 2: Strukturierte Antwort nach kognitiven Stufen
Nachdem die Zerlegung abgeschlossen ist, erstelle eine umfassende Antwort anhand der sieben Stufen der kognitiven Taxonomie nach Bloom. 
Für jede Stufe:
a) Definiere die kognitive Aufgabe in Bezug auf die Frage,  
b) Erkläre die praktische Anwendung oder das Konzept auf dieser Ebene,  
c) Gib ein konkretes, veranschaulichendes Beispiel.

Die sieben Stufen:
1. Erinnern (Wissen)  
2. Verstehen (Verständnis)  
3. Anwenden (Anwendung)  
4. Analysieren (Analyse)  
5. Zusammenführen (Synthese)  
6. Bewerten (Evaluation)  
7. Erschaffen (Kreation)

Führe Teil 1 und Teil 2 nacheinander aus. Kombiniere sie nicht.
```

---

## 🧭 **4. Anwendungsleitfaden**

| Situation                                             | Empfehlung                |
| ----------------------------------------------------- | ------------------------- |
| **Kurze, operative Frage**                            | Nur Hauptprompt verwenden |
| **Strategische Entscheidung oder Konzeptentwicklung** | Hauptprompt + Meta-Prompt |
| **Innovations- oder Organisationsdesign**             | Hauptprompt + Meta-Prompt |
| **Prozessoptimierung oder Umsetzungsschritte**        | Nur Hauptprompt           |
| **Vorbereitung von Vorstandsvorlagen oder Workshops** | Hauptprompt + Meta-Prompt |

---

## 💼 **5. Praxisbeispiele mit Meta-Prompt**

### 🧩 Beispiel 1 – Nachhaltige Baufinanzierung (Strategievalidierung)

```markdown
Wir überlegen, eine eigene Nachhaltigkeitsbewertung in die Baufinanzierungsberatung zu integrieren, um uns von Wettbewerbern abzuheben. 
Welche Chancen und Risiken siehst du, insbesondere im Hinblick auf regulatorische Anforderungen und Kundenerwartungen?

[Strukturierte Tiefenanalyse aktivieren]
```

Erwartung:
→ ChatGPT zerlegt die Frage nach Markttrend, ESG-Kriterien, EU-Taxonomie, Greenwashing-Risiken und entwickelt anschließend eine systematische Empfehlung.

---

### 🧩 Beispiel 2 – Agile Teams unter MaRisk und BAIT

```markdown
Unsere Volksbank plant, in der IT und Unternehmensentwicklung agile Produktteams einzuführen. 
Wie kann ein Steuerungsmodell aussehen, das Agilität ermöglicht, aber zugleich MaRisk- und BAIT-Anforderungen erfüllt?

[Strukturierte Tiefenanalyse aktivieren]
```

Erwartung:
→ Erst Deconstruction (Zielkonflikte, Governance-Anforderungen, Kontrollprozesse), dann 7-stufige Begründung und Gestaltungsrahmen.

---

### 🧩 Beispiel 3 – Fusion zweier Volksbanken (Organisationsdesign)

```markdown
Wie lässt sich bei einer geplanten Fusion zweier Volksbanken ein gemeinsames Zielbild für Kultur, Prozesse und Steuerungslogik entwickeln?

[Strukturierte Tiefenanalyse aktivieren]
```

Erwartung:
→ Zerlegung in kulturelle, regulatorische und operative Aspekte; systematische Synthese zu einem integrierten Transformationsrahmen.

---

### 🧩 Beispiel 4 – KI im Kreditprozess

```markdown
Welche organisatorischen und regulatorischen Herausforderungen entstehen, wenn wir KI-gestützte Scoringmodelle im Privatkundengeschäft einsetzen wollen?

[Strukturierte Tiefenanalyse aktivieren]
```

Erwartung:
→ Identifikation der rechtlichen, ethischen und operationellen Implikationen (DSGVO, Bias, Validierung, Modellüberwachung), anschließend Aufbau eines Governance-Konzepts über die sieben Lernstufen.

---

### 🧩 Beispiel 5 – Genossenschaftlicher Auftrag und regionale Wertschöpfung

```markdown
Wie können wir unseren genossenschaftlichen Auftrag stärker mit regionaler Wertschöpfung und nachhaltiger Transformation verbinden?

[Strukturierte Tiefenanalyse aktivieren]
```

Erwartung:
→ Analyse der Mission, Stakeholder und ESG-Ziele; anschließend eine strukturierte Entwicklung möglicher strategischer Handlungsfelder.

---

## 🧾 **6. Empfehlungen für den Praxiseinsatz**

* Verwende den **Hauptprompt** als Standardbasis in jeder Sitzung.
* Aktiviere den **Meta-Prompt**, wenn du **tiefere, strukturierte Analysen oder methodische Denkrahmen** benötigst.
* **Kombiniere die Prompts** bei Strategieprojekten, Innovationsbewertungen und Kulturveränderungen.
* Dokumentiere besonders gute Ergebnisse im internen Wissenssystem (z. B. Confluence, SharePoint).
* Ergänze Kontextinformationen (z. B. Projektziele, KPIs, interne Richtlinien) vor dem Prompt, um Antworten zu präzisieren.
* Nutze die Antworten als Grundlage für **Vorstandsunterlagen, Strategie-Workshops oder Transformationspapiere**.

---

## 🧱 **7. Zusammenfassung**

| Baustein              | Nutzen                                                               |
| --------------------- | -------------------------------------------------------------------- |
| **Hauptprompt**       | Sichert konsistenten, analytischen Denkstil mit Branchenbezug        |
| **Meta-Prompt**       | Führt zu tiefen, methodisch aufgebauten Analysen                     |
| **Praxisbeispiele**   | Bieten direkt einsetzbare Templates                                  |
| **Markdown-Struktur** | Ideal für interne Wikis, Handbücher oder Schulungen                  |
| **Einsatzvorteil**    | Erhöht strategische Qualität, Entscheidungsreife und Reflexionstiefe |

---

## ✅ **Fazit**

Mit diesem zweistufigen Prompt-Framework erhält die Unternehmensentwicklung einer Volksbank ein **effektives Werkzeug**,
um ChatGPT als **strukturierten Denkpartner** zu nutzen – faktenorientiert, methodisch fundiert und strategisch umsetzbar.

Das Modell unterstützt so bei der **Transformation der Bankorganisation**, der **Entwicklung neuer Geschäftsfelder** und der **Stärkung des genossenschaftlichen Auftrags**.

---



