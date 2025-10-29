# 🎯 Anleitung: Wie man einen Skill-Prompt erstellt


---

## 📚 Was ist ein Skill-Prompt?

Ein **Skill-Prompt** ist eine strukturierte Anleitung, die Sie Claude geben, damit er ein wiederverwendbares Skill für Sie erstellt. 

**Denken Sie daran wie an ein Rezept:**
- Sie schreiben einmal genau auf, WAS das Skill können soll
- Claude erstellt daraus ein fertiges Skill
- Danach können Sie das Skill immer wieder nutzen

---

## 🔍 Analyse des "Hook Creator" Beispiel-Prompts

Schauen wir uns an, wie der Beispiel-Prompt aufgebaut ist und WARUM:

### 1️⃣ Klare Zielsetzung am Anfang

```markdown
Help me create a Skill called "Hook Creator" that generates 
attention-grabbing headlines and hooks for marketing content.
```

**Was passiert hier?**
- ✅ Gibt dem Skill einen **eindeutigen Namen** ("Hook Creator")
- ✅ Erklärt in **einem Satz**, was das Skill macht
- ✅ Definiert den **Anwendungsbereich** (Marketing Content)

**💡 Lernen Sie daraus:**
Beginnen Sie immer mit einer klaren, prägnanten Beschreibung. Claude muss sofort verstehen, wofür das Skill da ist.

---

### 2️⃣ Skill Purpose (Zweck des Skills)

```markdown
## Skill Purpose
This skill should help me quickly generate 5-10 hook options 
for any marketing content using proven copywriting frameworks...
```

**Was passiert hier?**
- ✅ Erklärt das **Hauptziel** detaillierter
- ✅ Gibt **konkrete Zahlen** an (5-10 Optionen)
- ✅ Nennt **Methoden** (Copywriting Frameworks)

**💡 Lernen Sie daraus:**
Dieser Abschnitt ist das "Warum". Er erklärt, welches Problem das Skill löst und wie es das tut.

---

### 3️⃣ When to Use This Skill (Wann wird es genutzt?)

```markdown
## When to Use This Skill
Invoke this skill whenever I need to:
- Write email subject lines
- Create social media hooks
- Draft ad headlines
...
```

**Was passiert hier?**
- ✅ Listet **konkrete Anwendungsfälle** auf
- ✅ Hilft Claude zu erkennen, **wann** das Skill relevant ist
- ✅ Gibt dem Nutzer **Orientierung** für die Verwendung

**💡 Lernen Sie daraus:**
Je klarer Sie definieren, WANN das Skill verwendet wird, desto besser kann Claude es automatisch erkennen und vorschlagen.

**Für Ihr HR-Beispiel wäre das:**
```markdown
## When to Use This Skill
Invoke this skill whenever I need to:
- Erstelle Stellenanzeigen
- Schreibe Bewerbermails
- Formuliere Social Media Posts für Recruiting
```

---

### 4️⃣ Required Inputs (Benötigte Eingaben)

```markdown
## Required Inputs
When I invoke this skill, ask me for:
1. [Content type] - email, social post, ad, landing page, etc.
2. [Target audience] - who I'm writing for
3. [Main benefit or promise] - what the content delivers
4. [Tone] - professional, casual, urgent, playful, etc.
```

**Was passiert hier?**
- ✅ Definiert, welche **Informationen** Claude vom Nutzer braucht
- ✅ Gibt **Beispiele** für jede Eingabe
- ✅ Macht das Skill **interaktiv** - Claude stellt Fragen

**💡 Lernen Sie daraus:**
Das ist der wichtigste Teil! Sie sagen Claude genau, welche Informationen er VOR der Arbeit vom Nutzer erfragen soll.

**Für Ihr Stellenanzeigen-Skill wäre das:**
```markdown
## Required Inputs
When I invoke this skill, ask me for:
1. [Position] - Sachbearbeiter, Pflegefachkraft, etc.
2. [Abteilung] - Kundenservice, Leistungsabteilung, etc.
3. [Standort] - Hauptsitz, Regionalbüro [Stadt]
4. [Besonderheiten] - Teilzeit möglich, Führungsposition, etc.
```

---

### 5️⃣ Output Format (Wie soll das Ergebnis aussehen?)

```markdown
## Output Format
Generate 10 hook options using at least 5 different frameworks. 
For each hook:
- Present the hook text
- Label which framework was used in parentheses
- Keep hooks under 100 characters when possible
```

**Was passiert hier?**
- ✅ Definiert die **Struktur** der Ausgabe
- ✅ Gibt **Formatierungsvorgaben** (z.B. Zeichenlimit)
- ✅ Erklärt, wie die Ergebnisse **präsentiert** werden sollen

**💡 Lernen Sie daraus:**
Je präziser Sie das Format beschreiben, desto konsistenter sind Ihre Ergebnisse.

**Für Ihr Stellenanzeigen-Skill wäre das:**
```markdown
## Output Format
Erstelle eine Stellenanzeige mit folgender Struktur:
1. Einleitung (2-3 Sätze über die Krankenkasse)
2. Ihre Aufgaben (5-7 Bulletpoints)
3. Ihr Profil (5-7 Bulletpoints)
4. Wir bieten (Benefits in Bulletpoints)
5. Bewerbungshinweise (Kontaktdaten, Frist)
```

---

### 6️⃣ Frameworks/Methoden (Welche Techniken werden verwendet?)

```markdown
## Hook Frameworks to Use
- Curiosity Gap (incomplete information that demands resolution)
- Pain-Agitation-Solution (call out pain, make it worse, hint at solution)
- Benefit-Driven (lead with clear value)
...
```

**Was passiert hier?**
- ✅ Listet **konkrete Methoden** auf, die Claude nutzen soll
- ✅ Erklärt jede Methode **kurz** in Klammern
- ✅ Gibt Claude ein **Werkzeug-Set** an die Hand

**💡 Lernen Sie daraus:**
Wenn Sie möchten, dass Claude bestimmte bewährte Techniken nutzt, listen Sie diese explizit auf.

**Für Ihr Stellenanzeigen-Skill wäre das:**
```markdown
## Formulierungs-Ansätze
- Wertschätzend (Anerkennung der Bewerbenden)
- Mission-driven (Beitrag zur Gesundheitsversorgung)
- Benefit-fokussiert (Was bieten wir?)
- Entwicklungsorientiert (Karriereperspektiven)
- Team-bezogen (Wir-Gefühl)
```

---

### 7️⃣ Additional Guidelines (Zusätzliche Richtlinien)

```markdown
## Additional Guidelines
- Avoid clickbait that doesn't deliver on promises
- Test different lengths (short punchy vs. longer descriptive)
- Include at least 2 options that break category norms
- Make hooks specific rather than generic
- Ensure hooks align with brand voice
```

**Was passiert hier?**
- ✅ Gibt **Do's und Don'ts**
- ✅ Definiert **Qualitätskriterien**
- ✅ Verhindert **unerwünschte Ergebnisse**

**💡 Lernen Sie daraus:**
Dieser Abschnitt ist Ihre Qualitätskontrolle. Hier verhindern Sie häufige Fehler.

**Für Ihr Stellenanzeigen-Skill wäre das:**
```markdown
## Additional Guidelines
- Verwende IMMER die "Sie"-Form
- Stelle AGG-Konformität sicher (m/w/d, keine Diskriminierung)
- Integriere 5-7 Benefits aus unserer Standard-Liste
- Halte professionellen, aber warmherzigen Ton
- Vermeide Floskeln wie "dynamisch" oder "jung"
```

---

### 8️⃣ Call-to-Action am Ende

```markdown
Create this skill now and save it so I can invoke it whenever 
I need compelling hooks.
```

**Was passiert hier?**
- ✅ Gibt Claude eine **klare Handlungsanweisung**
- ✅ Erklärt, was mit dem Skill passieren soll

**💡 Lernen Sie daraus:**
Beenden Sie immer mit einer direkten Aufforderung, damit Claude weiß, dass er jetzt aktiv werden soll.

---

## 🏗️ Die perfekte Skill-Prompt-Struktur

Hier ist die **universelle Vorlage**, die Sie für JEDES Skill verwenden können:

```markdown
Help me create a Skill called "[SKILL-NAME]" that [HAUPTFUNKTION].

## Skill Purpose
[Detaillierte Beschreibung des Zwecks, was das Skill löst]

## When to Use This Skill
Invoke this skill whenever I need to:
- [Anwendungsfall 1]
- [Anwendungsfall 2]
- [Anwendungsfall 3]

## Required Inputs
When I invoke this skill, ask me for:
1. [Input 1] - [Erklärung mit Beispielen]
2. [Input 2] - [Erklärung mit Beispielen]
3. [Input 3] - [Erklärung mit Beispielen]

## Output Format
[Beschreibe genau, wie die Ausgabe strukturiert sein soll]
- [Format-Regel 1]
- [Format-Regel 2]
- [Format-Regel 3]

## [Methoden/Frameworks/Richtlinien]
[Falls Sie bestimmte Techniken oder Ansätze vorschreiben wollen]
- [Methode 1] - [Kurze Erklärung]
- [Methode 2] - [Kurze Erklärung]

## Additional Guidelines
- [Do/Don't 1]
- [Do/Don't 2]
- [Do/Don't 3]
- [Qualitätskriterium]

Create this skill now and save it so I can invoke it whenever [ANWENDUNGSFALL].
```

---

## ✅ Checkliste: Ist mein Skill-Prompt gut?

Prüfen Sie Ihren Prompt gegen diese Checkliste:

- [ ] **Klarer Name** - Kann ich in einem Wort sagen, wofür das Skill ist?
- [ ] **Eindeutiger Zweck** - Weiß Claude, was das Hauptziel ist?
- [ ] **Konkrete Trigger** - Habe ich Anwendungsfälle definiert?
- [ ] **Required Inputs** - Weiß Claude, welche Infos er braucht?
- [ ] **Output-Format** - Ist klar, wie das Ergebnis aussehen soll?
- [ ] **Beispiele** - Habe ich konkrete Beispiele gegeben?
- [ ] **Qualitätskriterien** - Habe ich Do's und Don'ts definiert?
- [ ] **Spezifität** - Ist der Prompt konkret oder zu vage?

---

## 🎓 Übung: Erstellen Sie Ihr erstes Skill

**Versuchen Sie es selbst!**

Wählen Sie eine Aufgabe aus Ihrem HR-Alltag:
1. Absagemails an Bewerber
2. LinkedIn-Posts für Stellenausschreibungen
3. Onboarding-Checklisten
4. Interview-Leitfäden
5. Mitarbeiter-Newsletter

Nutzen Sie die Vorlage oben und erstellen Sie einen Skill-Prompt!

---

## 💡 Profi-Tipps

### Tipp 1: Fangen Sie klein an
Erstellen Sie lieber 3 spezifische Skills als 1 riesiges, das alles können soll.

**❌ Schlecht:** "Ein Skill für alle HR-Aufgaben"  
**✅ Gut:** Separates Skill für Stellenanzeigen, E-Mails und Social Media

---

### Tipp 2: Nutzen Sie Beispiele
Je mehr konkrete Beispiele Sie geben, desto besser versteht Claude, was Sie wollen.

**❌ Schlecht:** "Schreibe professionell"  
**✅ Gut:** "Schreibe so: 'Sehr geehrte Frau Müller, vielen Dank für Ihre Bewerbung...'"

---

### Tipp 3: Iterieren Sie
Ihr erstes Skill wird nicht perfekt sein. Testen Sie es, verfeinern Sie es, testen Sie wieder.

**Workflow:**
1. Skill erstellen
2. 3-5 mal testen
3. Schwächen identifizieren
4. Skill aktualisieren
5. Erneut testen

---

### Tipp 4: Denken Sie ans Team
Formulieren Sie Skills so, dass auch Kollegen sie nutzen können.

**Gut dokumentiert:**
- Klare Anwendungsfälle
- Beispiele für Inputs
- Hinweise zur Anpassung

---

## 🚀 Nächste Schritte

1. **Lesen Sie den Beispiel-Prompt unten** (Englisch + Deutsch)
2. **Identifizieren Sie die einzelnen Bausteine** im Prompt
3. **Aktivieren Sie den Skill Creator** in Claude
4. **Erstellen Sie Ihr erstes eigenes Skill**
5. **Teilen Sie es mit dem Team**

---

---

# 📄 Original-Prompt (Englisch)

## Hook Creator Skill Prompt

```
Help me create a Skill called "Hook Creator" that generates attention-grabbing headlines and hooks for marketing content.

## Skill Purpose
This skill should help me quickly generate 5-10 hook options for any marketing content using proven copywriting frameworks like curiosity gaps, pain-agitation-solution, benefit-driven, contrarian statements, and specific numbers.

## When to Use This Skill
Invoke this skill whenever I need to:
- Write email subject lines
- Create social media hooks
- Draft ad headlines
- Write landing page headlines
- Generate video titles or thumbnails text

## Required Inputs
When I invoke this skill, ask me for:
1. [Content type] - email, social post, ad, landing page, etc.
2. [Target audience] - who I'm writing for
3. [Main benefit or promise] - what the content delivers
4. [Tone] - professional, casual, urgent, playful, etc.

## Output Format
Generate 10 hook options using at least 5 different frameworks. For each hook:
- Present the hook text
- Label which framework was used in parentheses
- Keep hooks under 100 characters when possible for platform compatibility

## Hook Frameworks to Use
- Curiosity Gap (incomplete information that demands resolution)
- Pain-Agitation-Solution (call out pain, make it worse, hint at solution)
- Benefit-Driven (lead with clear value)
- Contrarian (challenge common assumptions)
- Specific Numbers (use odd, precise numbers for credibility)
- Question + Benefit (problem question + implied solution)
- Social Proof (leverage popularity or authority)
- Time/Urgency (leverage FOMO or timely relevance)
- Transformation (before → after framing)
- Listicle (numbered format)

## Additional Guidelines
- Avoid clickbait that doesn't deliver on promises
- Test different lengths (short punchy vs. longer descriptive)
- Include at least 2 options that break category norms
- Make hooks specific rather than generic
- Ensure hooks align with brand voice

Create this skill now and save it so I can invoke it whenever I need compelling hooks.
```

---

---

# 📄 Deutsche Übersetzung

## Hook Creator Skill Prompt (Deutsch)

```
Hilf mir, ein Skill namens "Hook Creator" zu erstellen, das aufmerksamkeitsstarke Überschriften und Hooks für Marketing-Inhalte generiert.

## Zweck des Skills
Dieses Skill soll mir helfen, schnell 5-10 Hook-Optionen für beliebige Marketing-Inhalte zu generieren, unter Verwendung bewährter Copywriting-Frameworks wie Neugier-Lücken, Problem-Verstärkung-Lösung, Nutzen-orientiert, konträre Aussagen und spezifische Zahlen.

## Wann dieses Skill verwendet wird
Aktiviere dieses Skill, wenn ich Folgendes benötige:
- E-Mail-Betreffzeilen schreiben
- Social-Media-Hooks erstellen
- Werbe-Überschriften entwerfen
- Landing-Page-Überschriften formulieren
- Video-Titel oder Thumbnail-Texte generieren

## Benötigte Eingaben
Wenn ich dieses Skill aufrufe, frage mich nach:
1. [Inhaltstyp] - E-Mail, Social Post, Anzeige, Landing Page, etc.
2. [Zielgruppe] - für wen ich schreibe
3. [Hauptnutzen oder Versprechen] - was der Inhalt liefert
4. [Tonalität] - professionell, locker, dringend, verspielt, etc.

## Ausgabeformat
Generiere 10 Hook-Optionen unter Verwendung von mindestens 5 verschiedenen Frameworks. Für jeden Hook:
- Präsentiere den Hook-Text
- Kennzeichne das verwendete Framework in Klammern
- Halte Hooks nach Möglichkeit unter 100 Zeichen für Plattform-Kompatibilität

## Zu verwendende Hook-Frameworks
- Neugier-Lücke (unvollständige Information, die Auflösung verlangt)
- Problem-Verstärkung-Lösung (Problem benennen, verschlimmern, Lösung andeuten)
- Nutzen-orientiert (mit klarem Wert beginnen)
- Konträr (gängige Annahmen herausfordern)
- Spezifische Zahlen (ungerade, präzise Zahlen für Glaubwürdigkeit)
- Frage + Nutzen (Problemfrage + implizierte Lösung)
- Social Proof (Popularität oder Autorität nutzen)
- Zeit/Dringlichkeit (FOMO oder zeitliche Relevanz nutzen)
- Transformation (Vorher → Nachher Darstellung)
- Listicle (nummeriertes Format)

## Zusätzliche Richtlinien
- Vermeide Clickbait, der seine Versprechen nicht hält
- Teste verschiedene Längen (kurz und knackig vs. länger und beschreibend)
- Füge mindestens 2 Optionen hinzu, die Kategorie-Normen brechen
- Mache Hooks spezifisch statt generisch
- Stelle sicher, dass Hooks zur Markenstimme passen

Erstelle dieses Skill jetzt und speichere es, damit ich es jederzeit aufrufen kann, wenn ich überzeugende Hooks brauche.
```

---

---

# 🎯 Anwendungsbeispiel: Ihr HR-Skill

Basierend auf dem Hook Creator Beispiel, hier ein **Stellenanzeigen-Skill** für Ihre Krankenkasse:

```
Hilf mir, ein Skill namens "Stellenanzeigen-Generator" zu erstellen, 
das professionelle, AGG-konforme Stellenanzeigen für unsere 
gesetzliche Krankenkasse erstellt.

## Zweck des Skills
Dieses Skill soll mir helfen, konsistente, ansprechende 
Stellenanzeigen zu erstellen, die unsere Arbeitgebermarke stärken, 
rechtlich korrekt sind und unsere Unternehmenskultur widerspiegeln.

## Wann dieses Skill verwendet wird
Aktiviere dieses Skill, wenn ich:
- Eine neue Stelle ausschreibe
- Eine Stellenanzeige aktualisiere
- Mehrere Varianten für verschiedene Kanäle brauche
- Eine Stelle intern und extern ausschreibe

## Benötigte Eingaben
Wenn ich dieses Skill aufrufe, frage mich nach:
1. [Position] - Sachbearbeiter, Pflegefachkraft, IT-Spezialist, etc.
2. [Abteilung] - Kundenservice, Leistungen, Finanzen, etc.
3. [Standort] - Hauptsitz [Stadt], Regionalbüro [Stadt]
4. [Vertragsart] - Vollzeit, Teilzeit, befristet/unbefristet
5. [Besonderheiten] - Remote möglich, Führung, Projektarbeit

## Ausgabeformat
Erstelle eine Stellenanzeige mit folgender Struktur:

**1. Einleitung (2-3 Sätze)**
- Wer wir sind
- Was uns besonders macht

**2. Ihre Aufgaben (5-7 Bulletpoints)**
- Konkrete Tätigkeiten
- Verantwortungsbereiche

**3. Ihr Profil (5-7 Bulletpoints)**
- Muss-Qualifikationen
- Wunsch-Qualifikationen
- Soft Skills

**4. Wir bieten (Benefits)**
- Mindestens 6 Benefits aus unserer Standard-Liste
- Formatiert als Bulletpoints

**5. Bewerbungshinweise**
- Ansprechpartner
- Bewerbungsfrist
- Erforderliche Unterlagen

## Verpflichtende Elemente
- **Anrede:** Immer "Sie"-Form
- **AGG-Konformität:** "(m/w/d)" hinter jeder Positionsbezeichnung
- **Standard-Benefits einbauen:**
  - Betriebliche Altersvorsorge
  - 30 Tage Urlaub
  - Weiterbildungsbudget €1.500/Jahr
  - Mobiles Arbeiten (bis zu 60%)
  - Gesundheitsmanagement
  - Jobticket/Fahrtkostenzuschuss
  - Flexible Arbeitszeiten
  - Betriebliches Eingliederungsmanagement

## Tonalität und Stil
- Wertschätzend und professionell
- Authentisch, keine Floskeln
- Mission-driven (Beitrag zur Gesundheitsversorgung betonen)
- Inklusiv und divers
- Klare, verständliche Sprache

## Zusätzliche Richtlinien
- Vermeide Klischees wie "dynamisch", "jung", "belastbar"
- Verwende geschlechtsneutrale Sprache
- Betone echte Entwicklungsmöglichkeiten, keine leeren Versprechen
- Halte Anforderungen realistisch (nicht 5 Jahre Erfahrung für Einstiegsposition)
- Stelle sicher, dass keine diskriminierenden Formulierungen enthalten sind
- Erwähne unsere Werte: Patientenorientierung, Verlässlichkeit, Innovation

## Varianten generieren
Erstelle optional auch Kurzversionen für:
- LinkedIn (max. 1.000 Zeichen)
- Indeed (komprimierte Version)
- Interne Ausschreibung (zusätzliche interne Infos)

Erstelle dieses Skill jetzt und speichere es, damit ich es für 
alle zukünftigen Stellenausschreibungen nutzen kann.
```

---

## 📊 Vergleich der beiden Skills

| Aspekt | Hook Creator | Stellenanzeigen-Generator |
|--------|-------------|---------------------------|
| **Zielgruppe** | Marketing-Profis | HR-Mitarbeiter |
| **Output** | 10 Hook-Varianten | 1 vollständige Anzeige |
| **Komplexität** | Mittel (kreativ) | Hoch (rechtlich relevant) |
| **Frameworks** | 10 Copywriting-Methoden | Strukturvorgaben + Benefits |
| **Rechtl. Relevanz** | Niedrig | Hoch (AGG-konform) |
| **Anpassbarkeit** | Hoch (viele Varianten) | Mittel (feste Struktur) |

---

## 🎓 Was Sie gelernt haben

Nach dieser Anleitung können Sie:

✅ Die **Struktur eines Skill-Prompts** verstehen  
✅ **Eigene Skills** für Ihre HR-Aufgaben erstellen  
✅ **Best Practices** für Skill-Prompts anwenden  
✅ Skills für Ihr **Team teilen und dokumentieren**  
✅ Den Unterschied zwischen **guten und schlechten** Prompts erkennen

---

## 🚀 Ihr nächster Schritt

1. **Kopieren Sie die Vorlage** (Seite 3)
2. **Füllen Sie sie aus** für eine Ihrer wiederkehrenden Aufgaben
3. **Geben Sie den Prompt an Claude** (im Chat)
4. **Testen Sie das generierte Skill**
5. **Verfeinern Sie bei Bedarf**

**Viel Erfolg beim Erstellen Ihrer ersten Skills!** 🎉

---


