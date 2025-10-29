# 🎬 Leitfaden: Meta Prompts für KI-Videos

### (Cinematic Movies & Pixar-Style Movies)

---

## 🧭 1. Was ist ein Meta Prompt?

Ein **Meta Prompt** ist eine Art „Regieanleitung für die KI".
Er beschreibt **nicht direkt den Film**, sondern **führt den Nutzer Schritt für Schritt** zu einer strukturierten Video-Beschreibung im **JSON-Format**.
Dieses Format kann dann in **AI-Videogeneratoren** (z. B. Runway, Pika, Kaiber, Sora) verwendet werden, um **automatisch Filmszenen zu erzeugen**.

---

## 🎥 2. Warum ist das relevant?

Für Unternehmen wie die **Techniker Krankenkasse** bietet diese Technik:

* **Schnellere Content-Erstellung** (z. B. Employer-Branding-Videos, Gesundheitskampagnen, Social-Media-Beiträge)
* **Konsistente visuelle Qualität**, da die KI klar strukturierte Informationen bekommt
* **Geringere Abhängigkeit von Agenturen** bei einfachen Video-Produktionen
* **Einfache Bedienung** auch ohne technisches Vorwissen

---

## ⚙️ 3. Wie funktioniert ein Meta Prompt?

1. Der Nutzer gibt eine **Idee oder ein Thema** ein (z. B. „Digitale Gesundheitsservices bei der TK").
2. Die KI stellt gezielte **Fragen** zu Stil, Emotion, Kamera, Musik, Text usw.
3. Aus den Antworten entsteht automatisch eine **strukturierte JSON-Beschreibung**.
4. Diese Beschreibung kann anschließend in ein KI-Videotool eingefügt werden, um ein Video zu erzeugen.

---

## 🎬 4. Meta Prompt 1: **Cinematic Movie Builder**

### 🎯 Ziel

Erstellt realistische, filmreife Szenen – z. B. für Recruiting-Videos, Präsentationen oder Gesundheitskampagnen.

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

**Idee:** Eine emotionale Szene über Gesundheitskompetenz und Vertrauen bei der TK.

```markdown
{
  "description": "Langsame Kamerafahrt durch ein helles, modernes TK-Kundencenter. Gesundheitsberater sprechen freundlich mit Versicherten. Eine Hand reicht einem jungen Vater ein Tablet mit der TK-App. Die Szene endet mit einem zufriedenen Lächeln vor dem TK-Logo.",
  "style": "cinematic realism",
  "camera": "ruhige Steadicam, sanfte Bewegung",
  "lighting": "weiches Tageslicht mit türkisen Akzenten",
  "environment": "modernes Kundencenter mit Pflanzen und digitalen Infoscreens",
  "audio": "sanftes Klavier, dezentes Stimmengewirr",
  "dialogue": [
    {"character": "Erzähler", "line": "Gesundheit braucht Vertrauen – und das seit über 135 Jahren.", "tone": "warm, kompetent"}
  ],
  "voice": "freundliche weibliche Erzählerstimme",
  "ending": "Zoom auf das TK-Logo in Türkis",
  "text": "Kompetenz. Nähe. Techniker.",
  "keywords": ["Gesundheit", "Vertrauen", "Innovation", "4K"]
}
```

### 🪄 Example 1 – English

```markdown
{
  "description": "A slow camera glides through a bright, modern TK customer center. Health consultants speak warmly with insured persons. A hand passes a tablet with the TK app to a young father. The scene ends with a satisfied smile in front of the TK logo.",
  "style": "cinematic realism",
  "camera": "smooth steadycam",
  "lighting": "soft daylight with turquoise accents",
  "environment": "modern customer center with plants and digital info screens",
  "audio": "gentle piano, subtle background voices",
  "dialogue": [
    {"character": "Narrator", "line": "Health needs trust – for over 135 years.", "tone": "warm, competent"}
  ],
  "voice": "friendly female narrator",
  "ending": "zoom to TK logo in turquoise",
  "text": "Competence. Closeness. Techniker.",
  "keywords": ["health", "trust", "innovation", "4K"]
}
```

---

### 🪄 Beispiel 2 – Prävention & Bewegung (Deutsch)

```markdown
{
  "description": "Drohnenaufnahme über einen sonnigen Park. Menschen verschiedener Altersgruppen joggen, machen Yoga und spielen Volleyball. Ein TK-Gesundheitscoach zeigt einer Gruppe Dehnübungen. Nahaufnahme eines Fitness-Trackers mit TK-Bonusprogramm.",
  "style": "documentary cinematic",
  "lighting": "goldenes Morgenlicht",
  "audio": "energetische Indie-Musik, Vogelgezwitscher",
  "text": "Bewegt leben. Gesund bleiben.",
  "keywords": ["Prävention", "Bewegung", "Lebensfreude", "Community"]
}
```

---

### 🪄 Beispiel 3 – Employer Branding (Englisch)

```markdown
{
  "description": "Close-up of diverse TK employees collaborating in a bright office space. They laugh while working on a digital health project. Camera pans to show the Hamburg skyline through floor-to-ceiling windows.",
  "style": "modern corporate storytelling",
  "camera": "dynamic handheld, authentic feel",
  "lighting": "natural office light with warm undertones",
  "audio": "uplifting acoustic track",
  "text": "Work with purpose. Join TK.",
  "keywords": ["employer branding", "diversity", "innovation", "teamwork"]
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

**Idee:** Ein kleines Herz lernt, dass Gesundheit mehr ist als Medizin.

```markdown
{
  "description": "Ein winziges, schlagendes Herz mit großen Augen erwacht in einem Körper. Es beobachtet, wie der Mensch sich bewegt, lacht und entspannt. Das Herz lernt, dass Freude, Bewegung und Ruhe genauso wichtig sind wie Medikamente. Am Ende schlägt es zufrieden im Takt mit anderen Organen.",
  "characters": [
    {"name": "Herzi", "description": "kleines rotes Herz mit neugierigen Augen und fröhlichem Gesicht"}
  ],
  "emotion": "Entdeckung, Freude, Zusammenhalt",
  "lighting": "warmes, organisches Licht im Körperinneren",
  "color_palette": "türkis, rot und warme Pastelltöne",
  "audio": "verspielte Orchester-Musik mit Herzklopfen-Rhythmus",
  "dialogue": [
    {"character": "Herzi", "line": "Ich dachte, ich bin nur fürs Pumpen da... aber ich bin Teil von allem!", "tone": "staunend, glücklich"}
  ],
  "voices": [
    {"character": "Herzi", "voice": "junge, lebhafte Stimme"}
  ],
  "ending": "Kamera zoomt heraus und zeigt glücklichen Menschen beim Lachen",
  "text": "Gesundheit ist mehr. – Die Techniker",
  "keywords": ["Pixar-Stil", "Animation", "Prävention", "Ganzheitlichkeit"]
}
```

### 🪄 Example 1 – English

```markdown
{
  "description": "A tiny beating heart with big eyes wakes up inside a body. It watches as the person moves, laughs, and relaxes. The heart learns that joy, movement, and rest are as important as medicine. It ends beating happily in rhythm with other organs.",
  "characters": [
    {"name": "Hearty", "description": "small red heart with curious eyes and cheerful face"}
  ],
  "emotion": "discovery, joy, unity",
  "lighting": "warm organic light inside the body",
  "color_palette": "turquoise, red, and warm pastels",
  "audio": "playful orchestral score with heartbeat rhythm",
  "dialogue": [
    {"character": "Hearty", "line": "I thought I was just here to pump... but I'm part of everything!", "tone": "amazed, happy"}
  ],
  "voices": [
    {"character": "Hearty", "voice": "young, lively voice"}
  ],
  "ending": "camera zooms out showing happy person laughing",
  "text": "Health is more. – Die Techniker",
  "keywords": ["Pixar style", "animation", "prevention", "holistic health"]
}
```

---

### 🪄 Beispiel 2 – Mentale Gesundheit & Achtsamkeit

```markdown
{
  "description": "Ein kleiner Gedanke schwebt als leuchtende Wolke durch den Kopf einer gestressten Person. Er entdeckt einen ruhigen Ort – einen inneren Garten – wo andere Gedanken entspannt sitzen. Die Wolke lernt, dass Pausen wichtig sind.",
  "emotion": "Ruhe, Selbstfürsorge, Achtsamkeit",
  "audio": "sanftes Streichorchester mit meditativen Klängen",
  "dialogue": [
    {"character": "Gedankenwolke", "line": "Ich muss nicht immer rasen... ich darf auch mal innehalten.", "tone": "erleichtert, friedlich"}
  ],
  "voices": [
    {"character": "Gedankenwolke", "voice": "sanfte, beruhigende Stimme"}
  ],
  "text": "Gesundheit beginnt im Kopf. – Die Techniker",
  "keywords": ["Pixar", "Mental Health", "Achtsamkeit", "Selbstfürsorge"]
}
```

---

### 🪄 Beispiel 3 – Digitale Gesundheit (Englisch)

```markdown
{
  "description": "In a bright digital world, a friendly app icon named TiKi helps people navigate their health journey. TiKi transforms doctor appointments into colorful pathways and makes health data fun to understand.",
  "emotion": "empowerment, curiosity, innovation",
  "lighting": "soft digital glow with turquoise highlights",
  "audio": "uplifting electronic music with playful tones",
  "dialogue": [
    {"character": "TiKi", "line": "Health doesn't have to be complicated – let me show you!", "tone": "enthusiastic, helpful"}
  ],
  "voices": [
    {"character": "TiKi", "voice": "warm, modern voice"}
  ],
  "ending": "camera pans to glowing TK logo in smartphone",
  "text": "Health in your hands. – Die Techniker",
  "keywords": ["Pixar style", "digital health", "innovation", "user-friendly"]
}
```

---

## 💡 6. Fazit

| Aspekt      | Cinematic Prompt                                 | Pixar-Style Prompt                                  |
| ----------- | ------------------------------------------------ | --------------------------------------------------- |
| **Ziel**    | Realistische, emotionale Filmszenen              | Animierte, charakterbasierte Kurzfilme              |
| **Einsatz** | Employer Branding, Gesundheitskampagnen, Werbung | Storytelling, Wertekommunikation, Präventionsvideos |
| **Tonfall** | Ruhig, filmisch, realistisch                     | Verspielt, emotional, mit Moral                     |
| **Output**  | Kamera, Licht, Text, Musik                       | Charaktere, Stimmen, Emotionen, Musik               |

---

### 🚀 Nutzen für die Techniker Krankenkasse

* **Cinematic Prompt:** Ideal für Recruiting-Videos, Imagekampagnen oder digitale Gesundheitsservices
* **Pixar Prompt:** Ideal für Präventionskommunikation, Wertevermittlung oder Schulungsthemen

Beide Ansätze ermöglichen es, **Videoideen in Minuten zu strukturieren** und direkt in moderne KI-Video-Generatoren zu übertragen.

---
