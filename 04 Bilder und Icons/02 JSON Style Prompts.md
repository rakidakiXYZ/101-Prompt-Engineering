# 🏦 **JSON Prompting Guide für KI-Bildgenerierung**


(Bilingual Edition: Deutsch + English)

## 📘 1. Grundprinzipien
Warum JSON-Prompts?

JSON-Prompts strukturieren Ideen klar und nachvollziehbar.
Statt lange Sätze zu schreiben, werden Inhalte in logische Blöcke unterteilt.
Das führt zu konsistenteren, realistischeren und markenkonformen Bildern.

Vorteile:

Klare Trennung von Stil, Technik, Material und Komposition

Leicht anpassbar für verschiedene Szenarien (z. B. ESG, Team, Beratung, Produkt)

Besser reproduzierbare Ergebnisse

Kombinierbar mit internen Corporate Design Richtlinien

## ⚙️ 2. Grundstruktur eines JSON-Prompts
{
  "meta": {},
  "subject": {},
  "style": {},
  "technical": {},
  "materials": {},
  "environment": {},
  "composition": {},
  "quality": {}
}

💡 Denke an:

meta: Zweck, Prioritäten, Gewichtungen

subject: Was wird gezeigt? Wer ist zu sehen?

style: Licht, Stimmung, Farbwelt

technical: Kameraeinstellungen, Fokus, Auflösung

materials: Texturen und Oberflächen

environment: Ort, Tageszeit, Atmosphäre

composition: Bildaufbau, Perspektive, Fokuspunkt

quality: Qualität, Referenzen, Dinge, die vermieden werden sollen

## 🎯 3. Beispiel – ESG-Meeting in der Volksbank Wiesbaden
🇩🇪 Deutsche Version

```json
{
  "meta": {
    "prompt_purpose": "Bild für ESG-Kommunikation der Volksbank Wiesbaden",
    "priority": ["subject", "style", "composition", "lighting", "environment", "quality"],
    "weights": {
      "subject": 1.0,
      "style": 0.9,
      "composition": 0.85,
      "lighting": 0.8,
      "environment": 0.7,
      "quality": 0.7
    },
    "notes": "Professionelle, glaubwürdige Darstellung nach deutschem Corporate-Fotostil."
  },

  "subject": {
    "what": "Meeting von Volksbank Wiesbaden Mitarbeitenden, die an einem ESG-Strategiepapier arbeiten",
    "participants": ["5–6 Personen, gemischtes Geschlecht und Alter"],
    "actions": ["Diskussion am Konferenztisch", "zeigen auf ESG-Diagramme und Laptops"],
    "expression_mood": "engagiert, kooperativ, fokussiert",
    "dress_code": "Business-Casual in Bankfarben (Blau, Grau, Weiß)"
  },

  "style": {
    "primary": "dokumentarisch-realistisch",
    "secondary": ["Corporate Editorial", "authentische Reportage"],
    "mood": ["optimistisch", "vertrauenswürdig", "fokussiert"],
    "color_palette": ["neutrale Tageslichttöne", "Akzente in Blau und Grün für Nachhaltigkeit"],
    "rendering_quality": ["8k Details", "natürliche Hauttöne", "realistische Kontraste"]
  },

  "technical": {
    "camera_settings": {
      "lens": "35mm",
      "aperture": "f/4",
      "iso": "200",
      "shutter": "1/125"
    },
    "focus": "Gesichter und Gesten scharf, Hintergrund leicht weich",
    "lighting_setup": "weiches Tageslicht durch Fenster, dezente Aufhellung",
    "postprocessing": ["minimale Retusche", "echte Farben", "leichte Vignette"]
  },

  "materials": {
    "skin_and_faces": "authentische Texturen, natürliche Imperfektionen",
    "fabrics": "Baumwolle, Wolle, Leinen – sichtbar realistische Stoffstruktur",
    "surfaces": "mattes Konferenztischholz, ESG-Unterlagen sichtbar",
    "special": "feine Papierstruktur auf ESG-Reports erkennbar"
  },

  "environment": {
    "location": "moderner Konferenzraum der Volksbank Wiesbaden",
    "background_elements": ["Glaswände, Stadtblick, dezentes Logo im Hintergrund"],
    "lighting_conditions": "Tageslicht mit warmer Grundstimmung",
    "decor": ["Pflanzen für Nachhaltigkeitssymbolik", "reduziertes, elegantes Design"],
    "time_of_day": "später Vormittag"
  },

  "composition": {
    "shot_type": "Halbtotale",
    "perspective": "Augenhöhe mit leichtem Winkel für Tiefe",
    "framing": ["Drittelregel", "harmonische Gruppierung"],
    "subject_placement": "Team in leichter Bogenform um den Tisch",
    "leading_lines": "Tischkanten und Lichtlinien führen zum ESG-Dokument",
    "avoid": ["unruhiger Hintergrund", "überbelichtete Fenster", "angeschnittene Köpfe"]
  },

  "quality": {
    "include": [
      "authentische Teamarbeit",
      "natürliche Beleuchtung",
      "professioneller Unternehmensstil"
    ],
    "avoid": [
      "gestellte Posen",
      "überschärfte Haut",
      "künstliche HDR-Effekte"
    ],
    "reference": ["Volksbank Geschäftsberichte", "ESG-Kommunikation DAX-Unternehmen"],
    "safety": "Markenrechte respektieren; keine sensiblen Inhalte"
  }
}
```

🇬🇧 English Version
```json
{
  "meta": {
    "prompt_purpose": "Corporate image for Volksbank Wiesbaden ESG communication",
    "priority": ["subject", "style", "composition", "lighting", "environment", "quality"],
    "weights": {
      "subject": 1.0,
      "style": 0.9,
      "composition": 0.85,
      "lighting": 0.8,
      "environment": 0.7,
      "quality": 0.7
    },
    "notes": "Professional and authentic depiction in German corporate photo style."
  },

  "subject": {
    "what": "meeting of Volksbank Wiesbaden employees working on an ESG strategy paper",
    "participants": ["5–6 professionals of mixed gender and age"],
    "actions": ["discussing around a conference table", "pointing at ESG charts and laptops"],
    "expression_mood": "engaged, collaborative, focused",
    "dress_code": "business-casual in brand colors (blue, grey, white)"
  },

  "style": {
    "primary": "documentary photorealism",
    "secondary": ["corporate editorial", "authentic reportage"],
    "mood": ["optimistic", "trustworthy", "focused"],
    "color_palette": ["neutral daylight tones", "blue and green accents for sustainability"],
    "rendering_quality": ["8k detail", "natural skin tones", "realistic contrast"]
  },

  "technical": {
    "camera_settings": {
      "lens": "35mm",
      "aperture": "f/4",
      "iso": "200",
      "shutter": "1/125"
    },
    "focus": "faces and gestures sharp, background softly defocused",
    "lighting_setup": "soft daylight through windows, balanced fill",
    "postprocessing": ["minimal retouching", "true color balance", "slight vignette"]
  },

  "materials": {
    "skin_and_faces": "authentic textures, natural imperfections",
    "fabrics": "cotton, wool, linen with visible structure",
    "surfaces": "matte wooden conference table, ESG reports visible",
    "special": "fine paper texture visible on documents"
  },

  "environment": {
    "location": "modern Volksbank Wiesbaden conference room",
    "background_elements": ["glass walls, city view, subtle logo presence"],
    "lighting_conditions": "daylight with warm base tone",
    "decor": ["plants for sustainability symbolism", "minimalist German office design"],
    "time_of_day": "late morning"
  },

  "composition": {
    "shot_type": "medium wide shot",
    "perspective": "eye-level with slight angle for depth",
    "framing": ["rule of thirds", "balanced team layout"],
    "subject_placement": "team arranged in gentle arc around table center",
    "leading_lines": "table edges guide viewer toward ESG document",
    "avoid": ["cluttered background", "overexposed windows", "cropped heads"]
  },

  "quality": {
    "include": [
      "authentic teamwork",
      "natural lighting",
      "professional corporate aesthetic"
    ],
    "avoid": [
      "overly posed expressions",
      "plastic or oversharpened skin",
      "HDR glow"
    ],
    "reference": ["Volksbank annual report photography", "Deloitte ESG imagery"],
    "safety": "respect brand integrity; no sensitive data or identities"
  }
}
```

## 💼 4. Kompakte Variante (Deutsch + Englisch)

Kurzversion für Tools wie Midjourney oder DALL·E:

🇩🇪 Deutsch

Fotorealistisches, dokumentarisches Bild eines Meetings von Volksbank Wiesbaden Mitarbeitenden, die an einem ESG-Strategiepapier arbeiten. Moderne deutsche Büroarchitektur, Tageslicht, warme Farbwelt mit Blau- und Grünakzenten, authentische Teamarbeit, professionelle Komposition nach Drittelregel, natürliche Hauttöne, keine übertriebene Retusche oder HDR-Effekte.


🇬🇧 English

Photorealistic documentary-style image of Volksbank Wiesbaden employees collaborating on an ESG strategy paper. Modern German office architecture, soft daylight, warm color palette with blue and green accents, authentic teamwork expressions, professional rule-of-thirds composition, natural skin tones, no over-retouching or HDR glow.

## 🧩 5. Best Practices für Volksbanken-Marketingteams

✅ Tun:

Immer klare Rollen und Emotionen im Team zeigen

Authentische Beleuchtung (Tageslicht, Fensterlicht)

Leichte Markenfarbakzente (Blau, Grün, Weiß)

Offene, kooperative Körpersprache

ESG- oder Nachhaltigkeitselemente dezent einbinden

🚫 Vermeiden:

Stark gestellte Gruppen oder künstliches Lächeln

Übertriebene Sättigung oder Weichzeichnung

Nicht authentische Kleidung oder Orte

Zu viele Accessoires (ablenkend vom Kernthema)





---

## 👥 JSON-Template – Beratungsgespräch mit Kundin

### 🇩🇪 Deutsch

```json
{
  "meta": {"prompt_purpose": "Bild für Finanzberatung im Kundenzentrum Volksbank"},
  "subject": {
    "what": "Beratungsgespräch zwischen Bankberater und Kundin am Schreibtisch",
    "expression_mood": "kompetent, freundlich, vertrauensvoll"
  },
  "style": {
    "primary": "realistische Businessfotografie",
    "mood": ["seriös", "transparent", "nahbar"],
    "color_palette": ["helles Holz", "blau-grau", "weiß"]
  },
  "technical": {"camera_settings": {"lens": "50mm", "aperture": "f/2.8"}},
  "environment": {"location": "Volksbank-Filiale mit Tageslicht"},
  "composition": {"framing": ["Halbnah", "Drittelregel"]},
  "quality": {"include": ["authentisches Lächeln", "realistische Hauttöne"], "avoid": ["übertriebene Pose"]}
}
```

### 🇬🇧 English

```json
{
  "meta": {"prompt_purpose": "Financial consultation scene in a Volksbank branch"},
  "subject": {
    "what": "bank advisor and female client in discussion at a desk",
    "expression_mood": "professional, friendly, trustworthy"
  },
  "style": {
    "primary": "realistic corporate photography",
    "mood": ["serious", "transparent", "approachable"],
    "color_palette": ["light wood", "blue-grey", "white"]
  },
  "technical": {"camera_settings": {"lens": "50mm", "aperture": "f/2.8"}},
    "environment": {"location": "Volksbank branch with daylight"},
    "composition": {"framing": ["medium shot", "rule of thirds"]},
    "quality": {"include": ["authentic smile", "natural skin tones"], "avoid": ["exaggerated pose"]}
}
```

---

## 💻 JSON-Template – Digitale Zusammenarbeit (Innovation)

### 🇩🇪 Deutsch

```json
{
  "meta": {"prompt_purpose": "Bild zur digitalen Zusammenarbeit in Volksbank Marketing"},
  "subject": {
    "what": "Teammeeting mit digitalen Tools",
    "actions": ["Personen arbeiten mit Laptops und Tablets", "zeigen auf Datenvisualisierungen"],
    "expression_mood": "innovativ, konzentriert, motiviert"
  },
  "style": {
    "primary": "moderner Dokumentarstil",
    "mood": ["dynamisch", "technologisch", "positiv"],
    "color_palette": ["hell, blau, weiß", "leicht futuristische Akzente"]
  },
  "technical": {"camera_settings": {"lens": "28mm", "aperture": "f/4"}},
  "environment": {"location": "modernes Büro mit Glaswänden und digitalen Displays"},
  "composition": {"perspective": "leicht von oben für Übersicht"},
  "quality": {"include": ["klare Linien", "saubere Lichtführung"], "avoid": ["dunkle Schatten", "unruhige Hintergründe"]}
}
```

### 🇬🇧 English

```json
{
  "meta": {"prompt_purpose": "Image showing digital collaboration at Volksbank Marketing team"},
  "subject": {
    "what": "team meeting using laptops and tablets",
    "actions": ["pointing at data visualizations"],
    "expression_mood": "innovative, focused, motivated"
  },
  "style": {
    "primary": "modern documentary realism",
    "mood": ["dynamic", "technological", "positive"],
    "color_palette": ["bright, blue, white", "slightly futuristic tones"]
  },
  "technical": {"camera_settings": {"lens": "28mm", "aperture": "f/4"}},
  "environment": {"location": "modern office with glass walls and digital screens"},
  "composition": {"perspective": "slightly top-down for overview"},
  "quality": {"include": ["clean lines", "balanced lighting"], "avoid": ["dark shadows", "cluttered background"]}
}
```

---

## 🌿 JSON-Template – Nachhaltigkeit & Umweltbewusstsein

### 🇩🇪 Deutsch

```json
{
  "meta": {"prompt_purpose": "Nachhaltigkeitssymbolik in Volksbank Kommunikation"},
  "subject": {
    "what": "Volksbank Mitarbeitende pflanzen einen Baum im Rahmen eines ESG-Projekts",
    "expression_mood": "engagiert, positiv, verantwortungsbewusst"
  },
  "style": {
    "primary": "natürlicher Fotostil",
    "mood": ["Hoffnung", "Teamgeist", "Zukunft"],
    "color_palette": ["Grün, Erde, Blau, natürliche Hauttöne"]
  },
  "technical": {"camera_settings": {"lens": "35mm", "aperture": "f/5.6"}},
  "environment": {"location": "Park oder Grünfläche", "lighting_conditions": "weiches Morgenlicht"},
  "composition": {"framing": ["weit", "Drittelregel"], "perspective": "leicht von unten, betont Aktion"},
  "quality": {"include": ["natürliches Licht", "authentische Emotion"], "avoid": ["Kitsch", "übertriebene Symbolik"]}
}
```

### 🇬🇧 English

```json
{
  "meta": {"prompt_purpose": "Sustainability symbolism in Volksbank communication"},
  "subject": {
    "what": "Volksbank employees planting a tree as part of an ESG initiative",
    "expression_mood": "engaged, positive, responsible"
  },
  "style": {
    "primary": "natural outdoor realism",
    "mood": ["hopeful", "team spirit", "future-focused"],
    "color_palette": ["greens, earth tones, blue sky, natural skin tones"]
  },
  "technical": {"camera_settings": {"lens": "35mm", "aperture": "f/5.6"}},
  "environment": {"location": "park or green space", "lighting_conditions": "soft morning light"},
  "composition": {"framing": ["wide", "rule of thirds"], "perspective": "slightly low angle to emphasize action"},
  "quality": {"include": ["natural lighting", "authentic emotion"], "avoid": ["overly symbolic imagery"]}
}
```

---

## 👔 JSON-Template – Employer Branding / Mitarbeiterportrait

### 🇩🇪 Deutsch

```json
{
  "meta": {"prompt_purpose": "Portrait für Employer Branding Kampagne Volksbank"},
  "subject": {
    "what": "Volksbank Mitarbeiterin steht im Büro mit freundlichem Ausdruck",
    "expression_mood": "selbstbewusst, sympathisch, authentisch"
  },
  "style": {
    "primary": "editorial portrait photography",
    "mood": ["professionell", "vertrauensvoll", "modern"],
    "color_palette": ["helles Blau, Weiß, warme Grautöne"]
  },
  "technical": {"camera_settings": {"lens": "85mm", "aperture": "f/2.8"}},
  "environment": {"location": "Volksbank-Büro mit natürlichem Licht"},
  "composition": {"framing": ["Halbportrait", "Drittelregel"], "perspective": "Augenhöhe"},
  "quality": {"include": ["natürliche Haut", "Corporate-Look"], "avoid": ["übermäßige Retusche"]}
}
```

### 🇬🇧 English

```json
{
  "meta": {"prompt_purpose": "Employee portrait for Volksbank employer branding campaign"},
  "subject": {
    "what": "Volksbank employee standing in office with friendly expression",
    "expression_mood": "confident, approachable, authentic"
  },
  "style": {
    "primary": "editorial portrait photography",
    "mood": ["professional", "trustworthy", "modern"],
    "color_palette": ["light blue, white, warm greys"]
  },
  "technical": {"camera_settings": {"lens": "85mm", "aperture": "f/2.8"}},
  "environment": {"location": "Volksbank office with natural light"},
  "composition": {"framing": ["half-portrait", "rule of thirds"], "perspective": "eye-level"},
  "quality": {"include": ["natural skin texture", "corporate look"], "avoid": ["over-retouching"]}
}
```

---

## 📊 8. Interne Anwendungsempfehlung

| Ziel                             | Beispiel    | Verwendung                                            |
| -------------------------------- | ----------- | ----------------------------------------------------- |
| **ESG-Kommunikation**            | Template #1 | Geschäftsberichte, Nachhaltigkeitsposter              |
| **Kundenberatung**               | Template #2 | Website, Print, Kampagnenbilder                       |
| **Digitalisierung / Innovation** | Template #3 | Social Media, Intranet, Employer Branding             |
| **Nachhaltigkeit**               | Template #4 | CSR-Kommunikation, Projektberichte                    |
| **Employer Branding**            | Template #5 | Karriereportal, Social Recruiting, Mitarbeiterstories |

---

## 🧠 **9. Qualitäts-Checkliste vor jedem Render**

✅ Motiv klar (wer/was/welches Ziel)
✅ Markenfarben korrekt (Blau, Grau, Weiß, Grün)
✅ Natürliches Licht (kein Spot, kein HDR)
✅ Emotion authentisch
✅ Kleidung & Haltung glaubwürdig
✅ Keine Klischees oder Übertreibungen
✅ Perspektive harmonisch (Augenhöhe, Drittelregel)

---

Möchtest du, dass ich zum Abschluss noch eine **Markdown-kompatible Exportvorlage (z. B. als Handbuch-Seite für Confluence)** erstelle, die dieses gesamte Material strukturiert mit Inhaltsverzeichnis, Quicklinks und Copy-Buttons für jedes JSON enthält?
Damit könnte euer Team es direkt als interne Prompt-Bibliothek einsetzen.

