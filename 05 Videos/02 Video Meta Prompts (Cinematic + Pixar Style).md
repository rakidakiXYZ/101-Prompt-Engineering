

# 🎬 Leitfaden: Meta Prompts für KI-Videos

### (Cinematic Movies & Pixar-Style Movies)

---

## 🧭 1. Was ist ein Meta Prompt?

Ein **Meta Prompt** ist eine Art „Regieanleitung für die KI“.
Er beschreibt **nicht direkt den Film**, sondern **führt den Nutzer Schritt für Schritt** zu einer strukturierten Video-Beschreibung im **JSON-Format**.
Dieses Format kann dann in **AI-Videogeneratoren** (z. B. Runway, Pika, Kaiber, Sora) verwendet werden, um **automatisch Filmszenen zu erzeugen**.

---

## 🎥 2. Warum ist das relevant?

Für Unternehmen wie **Volksbanken** bietet diese Technik:

* **Schnellere Content-Erstellung** (z. B. Imagevideos, Schulungsclips, Social-Media-Beiträge)
* **Konsistente visuelle Qualität**, da die KI klar strukturierte Informationen bekommt
* **Geringere Abhängigkeit von Agenturen** bei einfachen Video-Produktionen
* **Einfache Bedienung** auch ohne technisches Vorwissen

---

## ⚙️ 3. Wie funktioniert ein Meta Prompt?

1. Der Nutzer gibt eine **Idee oder ein Thema** ein (z. B. „Nachhaltigkeit in unserer Bank“).
2. Die KI stellt gezielte **Fragen** zu Stil, Emotion, Kamera, Musik, Text usw.
3. Aus den Antworten entsteht automatisch eine **strukturierte JSON-Beschreibung**.
4. Diese Beschreibung kann anschließend in ein KI-Videotool eingefügt werden, um ein Video zu erzeugen.

---

## 🎬 4. Meta Prompt 1: **Cinematic Movie Builder**

### 🎯 Ziel

Erstellt realistische, filmreife Szenen – z. B. für Werbeclips, Präsentationen oder Markenfilme.

### 🧩 Struktur (vereinfacht)

```json
{
  "description": "",
  "style": "",
  "camera": "",
  "lighting": "",
  "environment": "",
  "elements": [],
  "motion": "",
  "audio": "",
  "dialogue": [],
  "voice": "",
  "ending": "",
  "text": "",
  "keywords": []
}
```

### 🪄 Beispiel 1 – Deutsch

**Idee:** Eine emotionale Szene über Gemeinschaft und Vertrauen bei der Volksbank.

```markdown
{
  "description": "Langsame Kamerafahrt durch eine sonnendurchflutete Bankfiliale. Mitarbeiter begrüßen Kunden mit Lächeln. Eine Hand hilft einer älteren Dame beim Einzahlen eines Scheins. Die Szene endet mit einem Gruppenlächeln vor dem Logo der Volksbank.",
  "style": "cinematic realism",
  "camera": "ruhige Steadicam, sanfte Bewegung",
  "lighting": "goldenes Nachmittagslicht",
  "environment": "moderne Filiale mit Holzelementen und Pflanzen",
  "audio": "sanftes Klavier, dezentes Stadtgeräusch",
  "dialogue": [
    {"character": "Erzähler", "line": "Vertrauen verbindet Menschen – und das seit Generationen.", "tone": "warm, ruhig"}
  ],
  "voice": "tiefe männliche Erzählerstimme",
  "ending": "Zoom auf das Logo der Volksbank",
  "text": "Vertrauen. Nähe. Volksbank.",
  "keywords": ["Gemeinschaft", "Vertrauen", "Nahbarkeit", "4K"]
}
```

### 🪄 Example 1 – English

```markdown
{
  "description": "A slow camera glides through a sunlit bank branch. Employees greet customers warmly. A hand helps an elderly lady deposit money. The scene ends with a group smile in front of the Volksbank logo.",
  "style": "cinematic realism",
  "camera": "smooth steadycam",
  "lighting": "golden hour light",
  "environment": "modern branch with wood and plants",
  "audio": "gentle piano, subtle city sounds",
  "dialogue": [
    {"character": "Narrator", "line": "Trust connects people – for generations.", "tone": "warm, calm"}
  ],
  "voice": "deep male narrator",
  "ending": "zoom to Volksbank logo",
  "text": "Trust. Closeness. Volksbank.",
  "keywords": ["community", "trust", "warm tone", "4K"]
}
```

---

### 🪄 Beispiel 2 – Nachhaltigkeit (Deutsch)

```markdown
{
  "description": "Drohnenaufnahme über grünen Dächern und Solarflächen. Kinder pflanzen Bäume auf dem Schulhof. Ein Mitarbeiter hält eine Volksbank-Karte hoch – Sonne spiegelt sich darin.",
  "style": "documentary cinematic",
  "lighting": "weiches Sonnenlicht am Morgen",
  "audio": "ruhige Gitarrenmusik, Vogelgezwitscher",
  "text": "Gemeinsam nachhaltig handeln.",
  "keywords": ["Nachhaltigkeit", "Zukunft", "Gemeinschaft"]
}
```

---

### 🪄 Beispiel 3 – Produktvideo (Englisch)

```markdown
{
  "description": "Close-up of a smartphone displaying the Volksbank app. The interface animates smoothly as the user transfers money with one tap.",
  "style": "modern tech ad",
  "camera": "macro lens, smooth rotation",
  "lighting": "cool reflections and soft shadows",
  "audio": "minimal electronic beat",
  "text": "Banking. Simple. Secure.",
  "keywords": ["fintech", "innovation", "mobile banking"]
}
```

---

## 🧚‍♀️ 5. Meta Prompt 2: **Pixar-Style Movie Builder**

### 🎯 Ziel

Erzeugt animierte, emotionale Kurzfilme im Stil von Pixar – mit Charakteren, Stimmen, Musik und Moral.

### 🧩 Struktur (vereinfacht)

```json
{
  "description": "",
  "style": "Pixar-style emotional 3D animation",
  "characters": [],
  "emotion": "",
  "camera": "",
  "lighting": "",
  "color_palette": "",
  "environment": "",
  "motion": "",
  "dialogue": [],
  "voices": [],
  "audio": "",
  "ending": "",
  "text": "",
  "keywords": []
}
```

---

### 🪄 Beispiel 1 – Deutsch

**Idee:** Eine Münze entdeckt, dass Teilen glücklicher macht.

```markdown
{
  "description": "Eine glänzende Euro-Münze liegt auf einem Tresen. Sie rollt davon, trifft andere Münzen und lernt, dass man Glück teilen kann. Am Ende landet sie in einer Spendenbox mit einem Lächeln.",
  "characters": [
    {"name": "Euro", "description": "kleine, neugierige Münze mit großen Augen"}
  ],
  "emotion": "Freude, Teilen, Zusammenhalt",
  "lighting": "warme Innenbeleuchtung mit goldenem Schimmer",
  "color_palette": "gold und blau",
  "audio": "verspielte Orchester-Musik",
  "dialogue": [
    {"character": "Euro", "line": "Ich dachte, ich wäre nur Geld... aber ich kann Freude bringen!", "tone": "neugierig, glücklich"}
  ],
  "voices": [
    {"character": "Euro", "voice": "junge weibliche Stimme, lebhaft"}
  ],
  "ending": "Kamera zoomt auf lachende Spendenbox",
  "text": "Freude, die zählt. – Volksbank",
  "keywords": ["Pixar-Stil", "Animation", "Freude", "Gemeinschaft"]
}
```

### 🪄 Example 1 – English

```markdown
{
  "description": "A shiny euro coin sits on a counter. It rolls away, meets other coins, and learns that sharing brings happiness. It ends up in a donation box with a smile.",
  "characters": [
    {"name": "Euro", "description": "small curious coin with big eyes"}
  ],
  "emotion": "joy, generosity, togetherness",
  "lighting": "warm golden glow",
  "audio": "playful orchestral score",
  "dialogue": [
    {"character": "Euro", "line": "I thought I was just money... but I can bring joy!", "tone": "curious, happy"}
  ],
  "voices": [
    {"character": "Euro", "voice": "young lively female voice"}
  ],
  "ending": "camera zooms on smiling donation box",
  "text": "Joy that counts. – Volksbank",
  "keywords": ["Pixar style", "animation", "joy", "community"]
}
```

---

### 🪄 Beispiel 2 – Beratung & Vertrauen

```markdown
{
  "description": "Ein junger Spatz stürzt aus dem Nest und lernt, dass er mit Hilfe anderer wieder fliegen kann. Seine Freunde bilden einen Kreis und helfen ihm aufzusteigen.",
  "emotion": "Mut, Vertrauen, Zusammenhalt",
  "audio": "sanftes Streichorchester mit emotionalem Aufbau",
  "dialogue": [
    {"character": "Spatz", "line": "Alleine bin ich klein... aber mit euch kann ich fliegen!", "tone": "ermutigend"}
  ],
  "voices": [
    {"character": "Spatz", "voice": "sanfte Kinderstimme, hoffnungsvoll"}
  ],
  "text": "Gemeinsam schaffen wir mehr. – Volksbank",
  "keywords": ["Pixar", "Teamwork", "Mut", "Freundschaft"]
}
```

---

### 🪄 Beispiel 3 – Zukunft & Innovation (Englisch)

```markdown
{
  "description": "In a futuristic city, a small robot banker learns to understand emotions while helping customers smile again.",
  "emotion": "curiosity, empathy, wonder",
  "lighting": "soft neon glow",
  "audio": "uplifting piano with electronic undertones",
  "dialogue": [
    {"character": "Robo", "line": "It’s not just numbers... it’s people.", "tone": "gentle and amazed"}
  ],
  "voices": [
    {"character": "Robo", "voice": "warm, slightly mechanical male voice"}
  ],
  "ending": "camera pans to glowing bank logo at sunset",
  "text": "Banking with heart. – Volksbank",
  "keywords": ["Pixar style", "AI empathy", "innovation", "emotion"]
}
```

---

## 💡 6. Fazit

| Aspekt      | Cinematic Prompt                    | Pixar-Style Prompt                          |
| ----------- | ----------------------------------- | ------------------------------------------- |
| **Ziel**    | Realistische, emotionale Filmszenen | Animierte, charakterbasierte Kurzfilme      |
| **Einsatz** | Imagefilme, Produktvideos, Werbung  | Storytelling, Wertekommunikation, HR-Videos |
| **Tonfall** | Ruhig, filmisch, realistisch        | Verspielt, emotional, mit Moral             |
| **Output**  | Kamera, Licht, Text, Musik          | Charaktere, Stimmen, Emotionen, Musik       |

---

### 🚀 Nutzen für Volksbanken

* **Cinematic Prompt:** Ideal für reale Kampagnen- oder Produktvideos
* **Pixar Prompt:** Ideal für Markenkommunikation, Werte- oder Schulungsthemen

Beide Ansätze ermöglichen es, **Videoideen in Minuten zu strukturieren** und direkt in moderne KI-Video-Generatoren zu übertragen.

---


