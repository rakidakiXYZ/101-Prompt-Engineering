# 🏥 **JSON Prompting Guide für KI-Bildgenerierung**


## 📘 1. Grundprinzipien
Warum JSON-Prompts?

JSON-Prompts strukturieren Ideen klar und nachvollziehbar.
Statt lange Sätze zu schreiben, werden Inhalte in logische Blöcke unterteilt.
Das führt zu konsistenteren, realistischeren und markenkonformen Bildern.

Vorteile:

Klare Trennung von Stil, Technik, Material und Komposition

Leicht anpassbar für verschiedene Szenarien (z. B. Gesundheitsberatung, Team, Prävention, Digitalisierung)

Besser reproduzierbare Ergebnisse

Kombinierbar mit internen Corporate Design Richtlinien der TK

## ⚙️ 2. Grundstruktur eines JSON-Prompts
```json
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
```

💡 Denke an:

meta: Zweck, Prioritäten, Gewichtungen

subject: Was wird gezeigt? Wer ist zu sehen?

style: Licht, Stimmung, Farbwelt

technical: Kameraeinstellungen, Fokus, Auflösung

materials: Texturen und Oberflächen

environment: Ort, Tageszeit, Atmosphäre

composition: Bildaufbau, Perspektive, Fokuspunkt

quality: Qualität, Referenzen, Dinge, die vermieden werden sollen

## 🎯 3. Beispiel – Digitale Gesundheitsberatung in der Techniker Krankenkasse
🇩🇪 Deutsche Version

```json
{
  "meta": {
    "prompt_purpose": "Bild für digitale Gesundheitskommunikation der Techniker Krankenkasse",
    "priority": ["subject", "style", "composition", "lighting", "environment", "quality"],
    "weights": {
      "subject": 1.0,
      "style": 0.9,
      "composition": 0.85,
      "lighting": 0.8,
      "environment": 0.7,
      "quality": 0.7
    },
    "notes": "Professionelle, empathische Darstellung nach TK Corporate Design."
  },

  "subject": {
    "what": "Meeting von TK-Mitarbeitenden, die an einer digitalen Gesundheitsstrategie arbeiten",
    "participants": ["5–6 Personen, gemischtes Geschlecht und Alter"],
    "actions": ["Diskussion am Konferenztisch", "zeigen auf Gesundheits-Dashboards und Tablets"],
    "expression_mood": "engagiert, empathisch, innovativ, fokussiert",
    "dress_code": "Business-Casual in TK-Farben (Blau, Cyan, Grau, Weiß)"
  },

  "style": {
    "primary": "dokumentarisch-realistisch",
    "secondary": ["Health Editorial", "authentische Reportage"],
    "mood": ["optimistisch", "vertrauenswürdig", "menschlich", "zukunftsorientiert"],
    "color_palette": ["helles Blau und Cyan", "frisches Grün", "warme neutrale Töne"],
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
    "surfaces": "mattes Konferenztischholz, Gesundheits-Unterlagen sichtbar",
    "special": "feine Papierstruktur auf Dokumenten erkennbar, moderne Tablet-Displays"
  },

  "environment": {
    "location": "moderner Konferenzraum der Techniker Krankenkasse",
    "background_elements": ["Glaswände, dezentes TK-Logo im Hintergrund", "moderne Gesundheitstechnologie"],
    "lighting_conditions": "Tageslicht mit frischer, positiver Grundstimmung",
    "decor": ["Pflanzen für Gesundheitssymbolik", "reduziertes, modernes Design", "ergonomische Möbel"],
    "time_of_day": "später Vormittag"
  },

  "composition": {
    "shot_type": "Halbtotale",
    "perspective": "Augenhöhe mit leichtem Winkel für Tiefe",
    "framing": ["Drittelregel", "harmonische Gruppierung"],
    "subject_placement": "Team in leichter Bogenform um den Tisch",
    "leading_lines": "Tischkanten und Lichtlinien führen zur digitalen Gesundheitsanwendung",
    "avoid": ["unruhiger Hintergrund", "überbelichtete Fenster", "angeschnittene Köpfe"]
  },

  "quality": {
    "include": [
      "authentische Teamarbeit",
      "natürliche Beleuchtung",
      "professioneller Gesundheitsdienstleister-Stil",
      "empathische Ausstrahlung"
    ],
    "avoid": [
      "gestellte Posen",
      "überschärfte Haut",
      "künstliche HDR-Effekte",
      "klinische Krankenhausatmosphäre"
    ],
    "reference": ["TK-Geschäftsberichte", "moderne Gesundheitskommunikation", "digitale Health-Kampagnen"],
    "safety": "Markenrechte respektieren; keine sensiblen Gesundheitsdaten; DSGVO-konform"
  }
}
```

🇬🇧 English Version
```json
{
  "meta": {
    "prompt_purpose": "Corporate image for Techniker Krankenkasse digital health communication",
    "priority": ["subject", "style", "composition", "lighting", "environment", "quality"],
    "weights": {
      "subject": 1.0,
      "style": 0.9,
      "composition": 0.85,
      "lighting": 0.8,
      "environment": 0.7,
      "quality": 0.7
    },
    "notes": "Professional and empathetic depiction in TK corporate design style."
  },

  "subject": {
    "what": "meeting of Techniker Krankenkasse employees working on a digital health strategy",
    "participants": ["5–6 professionals of mixed gender and age"],
    "actions": ["discussing around a conference table", "pointing at health dashboards and tablets"],
    "expression_mood": "engaged, empathetic, innovative, focused",
    "dress_code": "business-casual in brand colors (blue, cyan, grey, white)"
  },

  "style": {
    "primary": "documentary photorealism",
    "secondary": ["health editorial", "authentic reportage"],
    "mood": ["optimistic", "trustworthy", "human-centered", "future-focused"],
    "color_palette": ["bright blue and cyan", "fresh green", "warm neutral tones"],
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
    "surfaces": "matte wooden conference table, health documents visible",
    "special": "fine paper texture visible on documents, modern tablet displays"
  },

  "environment": {
    "location": "modern Techniker Krankenkasse conference room",
    "background_elements": ["glass walls, subtle TK logo presence", "modern health technology"],
    "lighting_conditions": "daylight with fresh, positive tone",
    "decor": ["plants for health symbolism", "minimalist modern design", "ergonomic furniture"],
    "time_of_day": "late morning"
  },

  "composition": {
    "shot_type": "medium wide shot",
    "perspective": "eye-level with slight angle for depth",
    "framing": ["rule of thirds", "balanced team layout"],
    "subject_placement": "team arranged in gentle arc around table center",
    "leading_lines": "table edges guide viewer toward digital health application",
    "avoid": ["cluttered background", "overexposed windows", "cropped heads"]
  },

  "quality": {
    "include": [
      "authentic teamwork",
      "natural lighting",
      "professional health service provider aesthetic",
      "empathetic presence"
    ],
    "avoid": [
      "overly posed expressions",
      "plastic or oversharpened skin",
      "HDR glow",
      "clinical hospital atmosphere"
    ],
    "reference": ["TK annual report photography", "modern health communication", "digital health campaigns"],
    "safety": "respect brand integrity; no sensitive health data; GDPR-compliant"
  }
}
```

## 💼 4. Kompakte Variante (Deutsch + Englisch)

Kurzversion für Tools wie Midjourney oder DALL·E:

🇩🇪 Deutsch

Fotorealistisches, dokumentarisches Bild eines Meetings von Techniker Krankenkasse Mitarbeitenden, die an einer digitalen Gesundheitsstrategie arbeiten. Moderne Büroarchitektur, Tageslicht, frische Farbwelt mit Blau-, Cyan- und Grünakzenten, authentische Teamarbeit, professionelle Komposition nach Drittelregel, natürliche Hauttöne, empathische Ausstrahlung, keine übertriebene Retusche oder HDR-Effekte.


🇬🇧 English

Photorealistic documentary-style image of Techniker Krankenkasse employees collaborating on a digital health strategy. Modern office architecture, soft daylight, fresh color palette with blue, cyan and green accents, authentic teamwork expressions, professional rule-of-thirds composition, natural skin tones, empathetic presence, no over-retouching or HDR glow.

## 🧩 5. Best Practices für TK HR- und Marketing-Teams

✅ Tun:

Immer klare Rollen und authentische Emotionen im Team zeigen

Natürliche Beleuchtung (Tageslicht, Fensterlicht)

TK-Markenfarbakzente (Blau, Cyan, Grün, Weiß)

Offene, empathische Körpersprache

Gesundheit und Wohlbefinden subtil visualisieren

Diversität und Inklusion selbstverständlich darstellen

🚫 Vermeiden:

Stark gestellte Gruppen oder künstliches Lächeln

Übertriebene Sättigung oder Weichzeichnung

Klinische oder sterile Krankenhausatmosphäre

Kitschige Gesundheitssymbolik (z.B. rote Herzen)

Nicht authentische Kleidung oder Orte

Darstellung sensibler Gesundheitsdaten

---

## 👥 JSON-Template – Persönliche Gesundheitsberatung

### 🇩🇪 Deutsch

```json
{
  "meta": {"prompt_purpose": "Bild für persönliche Gesundheitsberatung der TK"},
  "subject": {
    "what": "TK-Gesundheitsberater im Gespräch mit Versicherten am Schreibtisch",
    "expression_mood": "empathisch, kompetent, vertrauensvoll, zugewandt"
  },
  "style": {
    "primary": "realistische Gesundheitsfotografie",
    "mood": ["warmherzig", "professionell", "nahbar"],
    "color_palette": ["helles Blau und Cyan", "warme Grautöne", "weiß", "natürliche Holztöne"]
  },
  "technical": {"camera_settings": {"lens": "50mm", "aperture": "f/2.8"}},
  "environment": {"location": "TK-Kundencenter mit freundlicher, heller Atmosphäre"},
  "composition": {"framing": ["Halbnah", "Drittelregel"]},
  "quality": {"include": ["authentisches Lächeln", "realistische Hauttöne", "empathische Zuwendung"], "avoid": ["übertriebene Pose", "klinische Kälte"]}
}
```

### 🇬🇧 English

```json
{
  "meta": {"prompt_purpose": "Personal health consultation scene at TK customer center"},
  "subject": {
    "what": "TK health advisor in conversation with insured person at desk",
    "expression_mood": "empathetic, competent, trustworthy, attentive"
  },
  "style": {
    "primary": "realistic health care photography",
    "mood": ["warm", "professional", "approachable"],
    "color_palette": ["bright blue and cyan", "warm greys", "white", "natural wood tones"]
  },
  "technical": {"camera_settings": {"lens": "50mm", "aperture": "f/2.8"}},
  "environment": {"location": "TK customer center with friendly, bright atmosphere"},
  "composition": {"framing": ["medium shot", "rule of thirds"]},
  "quality": {"include": ["authentic smile", "natural skin tones", "empathetic attention"], "avoid": ["exaggerated pose", "clinical coldness"]}
}
```

---

## 💻 JSON-Template – Digitale Gesundheitsservices (Innovation)

### 🇩🇪 Deutsch

```json
{
  "meta": {"prompt_purpose": "Bild zur digitalen Gesundheitsinnovation der TK"},
  "subject": {
    "what": "TK-Team arbeitet an digitalen Gesundheitsanwendungen",
    "actions": ["Personen nutzen Tablets und Smartphones", "zeigen auf Gesundheits-Apps und Datenvisualisierungen"],
    "expression_mood": "innovativ, konzentriert, motiviert, zukunftsorientiert"
  },
  "style": {
    "primary": "moderner Tech-Dokumentarstil",
    "mood": ["dynamisch", "technologisch", "menschlich", "positiv"],
    "color_palette": ["frisches Blau und Cyan", "weiß", "leichte grüne Akzente", "warme Hauttöne"]
  },
  "technical": {"camera_settings": {"lens": "28mm", "aperture": "f/4"}},
  "environment": {"location": "modernes TK-Büro mit digitalen Displays und freundlicher Atmosphäre"},
  "composition": {"perspective": "leicht von oben für Übersicht"},
  "quality": {"include": ["klare Linien", "saubere Lichtführung", "moderne Technologie", "menschliche Nähe"], "avoid": ["dunkle Schatten", "unruhige Hintergründe", "sterile Technik-Ästhetik"]}
}
```

### 🇬🇧 English

```json
{
  "meta": {"prompt_purpose": "Image showing digital health innovation at TK"},
  "subject": {
    "what": "TK team working on digital health applications",
    "actions": ["using tablets and smartphones", "pointing at health apps and data visualizations"],
    "expression_mood": "innovative, focused, motivated, future-oriented"
  },
  "style": {
    "primary": "modern tech documentary realism",
    "mood": ["dynamic", "technological", "human-centered", "positive"],
    "color_palette": ["fresh blue and cyan", "white", "light green accents", "warm skin tones"]
  },
  "technical": {"camera_settings": {"lens": "28mm", "aperture": "f/4"}},
  "environment": {"location": "modern TK office with digital displays and friendly atmosphere"},
  "composition": {"perspective": "slightly top-down for overview"},
  "quality": {"include": ["clean lines", "balanced lighting", "modern technology", "human warmth"], "avoid": ["dark shadows", "cluttered background", "sterile tech aesthetic"]}
}
```

---

## 🏃 JSON-Template – Prävention & Gesundheitsförderung

### 🇩🇪 Deutsch

```json
{
  "meta": {"prompt_purpose": "Präventionssymbolik in TK Gesundheitskommunikation"},
  "subject": {
    "what": "Diverse Gruppe von Menschen bei einem TK-Gesundheitskurs im Freien",
    "participants": ["6–8 Personen verschiedenen Alters bei Yoga oder leichtem Outdoor-Training"],
    "expression_mood": "aktiv, entspannt, motiviert, gesund"
  },
  "style": {
    "primary": "natürlicher Lifestyle-Fotostil",
    "mood": ["Vitalität", "Gemeinschaft", "Wohlbefinden"],
    "color_palette": ["frisches Grün", "helles Blau", "natürliche Hauttöne", "warme Sonnentöne"]
  },
  "technical": {"camera_settings": {"lens": "35mm", "aperture": "f/5.6"}},
  "environment": {"location": "Park oder Grünfläche", "lighting_conditions": "weiches Morgenlicht oder goldene Stunde"},
  "composition": {"framing": ["weit", "Drittelregel"], "perspective": "Augenhöhe, betont Gruppendynamik"},
  "quality": {"include": ["natürliches Licht", "authentische Bewegung", "diverse Körpertypen"], "avoid": ["Fitness-Klischees", "perfektionistische Körperbilder", "übertriebene Sportler-Posen"]}
}
```

### 🇬🇧 English

```json
{
  "meta": {"prompt_purpose": "Prevention symbolism in TK health communication"},
  "subject": {
    "what": "diverse group of people at a TK health course outdoors",
    "participants": ["6–8 people of various ages doing yoga or light outdoor exercise"],
    "expression_mood": "active, relaxed, motivated, healthy"
  },
  "style": {
    "primary": "natural lifestyle photography",
    "mood": ["vitality", "community", "well-being"],
    "color_palette": ["fresh green", "bright blue", "natural skin tones", "warm sunlight"]
  },
  "technical": {"camera_settings": {"lens": "35mm", "aperture": "f/5.6"}},
  "environment": {"location": "park or green space", "lighting_conditions": "soft morning light or golden hour"},
  "composition": {"framing": ["wide", "rule of thirds"], "perspective": "eye-level, emphasizes group dynamic"},
  "quality": {"include": ["natural lighting", "authentic movement", "diverse body types"], "avoid": ["fitness clichés", "perfectionist body images", "exaggerated athletic poses"]}
}
```

---

## 👔 JSON-Template – Employer Branding / Mitarbeiterportrait

### 🇩🇪 Deutsch

```json
{
  "meta": {"prompt_purpose": "Portrait für Employer Branding Kampagne TK"},
  "subject": {
    "what": "TK-Mitarbeiter/in steht im modernen Büro mit freundlichem, authentischem Ausdruck",
    "expression_mood": "selbstbewusst, sympathisch, authentisch, zugewandt"
  },
  "style": {
    "primary": "editorial portrait photography",
    "mood": ["professionell", "menschlich", "modern", "vertrauensvoll"],
    "color_palette": ["helles Blau und Cyan", "Weiß", "warme Grautöne"]
  },
  "technical": {"camera_settings": {"lens": "85mm", "aperture": "f/2.8"}},
  "environment": {"location": "TK-Büro mit natürlichem Licht und modernem Design"},
  "composition": {"framing": ["Halbportrait", "Drittelregel"], "perspective": "Augenhöhe"},
  "quality": {"include": ["natürliche Haut", "Corporate-Look", "Persönlichkeit sichtbar"], "avoid": ["übermäßige Retusche", "steife Business-Posen"]}
}
```

### 🇬🇧 English

```json
{
  "meta": {"prompt_purpose": "Employee portrait for TK employer branding campaign"},
  "subject": {
    "what": "TK employee standing in modern office with friendly, authentic expression",
    "expression_mood": "confident, approachable, authentic, attentive"
  },
  "style": {
    "primary": "editorial portrait photography",
    "mood": ["professional", "human", "modern", "trustworthy"],
    "color_palette": ["bright blue and cyan", "white", "warm greys"]
  },
  "technical": {"camera_settings": {"lens": "85mm", "aperture": "f/2.8"}},
  "environment": {"location": "TK office with natural light and modern design"},
  "composition": {"framing": ["half-portrait", "rule of thirds"], "perspective": "eye-level"},
  "quality": {"include": ["natural skin texture", "corporate look", "visible personality"], "avoid": ["over-retouching", "stiff business poses"]}
}
```

---

## 🩺 JSON-Template – Telemedizin & Remote-Beratung

### 🇩🇪 Deutsch

```json
{
  "meta": {"prompt_purpose": "Bild für Telemedizin-Services der TK"},
  "subject": {
    "what": "Versicherte/r nutzt TK-Video-Sprechstunde am Laptop oder Tablet zu Hause",
    "expression_mood": "entspannt, zufrieden, konzentriert"
  },
  "style": {
    "primary": "moderner Lifestyle-Dokumentarstil",
    "mood": ["komfortabel", "vertraut", "professionell", "zugänglich"],
    "color_palette": ["warme Wohntöne", "helles Blau", "natürliches Licht"]
  },
  "technical": {"camera_settings": {"lens": "35mm", "aperture": "f/2.8"}},
  "environment": {"location": "heimische Umgebung mit Wohnzimmer oder Homeoffice-Ecke"},
  "composition": {"framing": ["Halbnah bis Halbtotale"], "perspective": "leicht von der Seite"},
  "quality": {"include": ["authentisches Zuhause", "moderne Technologie", "entspannte Atmosphäre"], "avoid": ["perfekt aufgeräumte Kulisse", "sterile Tech-Ästhetik"]}
}
```

### 🇬🇧 English

```json
{
  "meta": {"prompt_purpose": "Image for TK telemedicine services"},
  "subject": {
    "what": "insured person using TK video consultation on laptop or tablet at home",
    "expression_mood": "relaxed, satisfied, focused"
  },
  "style": {
    "primary": "modern lifestyle documentary style",
    "mood": ["comfortable", "familiar", "professional", "accessible"],
    "color_palette": ["warm home tones", "bright blue", "natural light"]
  },
  "technical": {"camera_settings": {"lens": "35mm", "aperture": "f/2.8"}},
  "environment": {"location": "home environment with living room or home office corner"},
  "composition": {"framing": ["medium to medium-wide shot"], "perspective": "slightly from the side"},
  "quality": {"include": ["authentic home setting", "modern technology", "relaxed atmosphere"], "avoid": ["perfectly styled backdrop", "sterile tech aesthetic"]}
}
```

---

## 📊 8. Interne Anwendungsempfehlung für die TK

| Ziel                                    | Template    | Verwendung                                                    |
| --------------------------------------- | ----------- | ------------------------------------------------------------- |
| **Digitale Gesundheitsstrategie**       | Template #1 | Geschäftsberichte, Strategiepräsentationen                    |
| **Persönliche Beratung**                | Template #2 | Website, Print, Versichertenkommunikation                     |
| **Digitalisierung / Innovation**        | Template #3 | Social Media, App-Marketing, Tech-Kommunikation               |
| **Prävention & Gesundheitsförderung**   | Template #4 | Präventionskampagnen, Kursprogramme, Social Media             |
| **Employer Branding**                   | Template #5 | Karriereportal, Social Recruiting, Mitarbeiterstories         |
| **Telemedizin & digitale Services**     | Template #6 | App-Promotion, Service-Erklärungen, Kundenmagazine            |

---

## 🧠 **9. Qualitäts-Checkliste vor jedem Render**

✅ Motiv klar (wer/was/welches Ziel)
✅ TK-Markenfarben korrekt (Blau, Cyan, Grün, Weiß, Grau)
✅ Natürliches Licht (kein Spot, kein HDR)
✅ Emotion authentisch und empathisch
✅ Kleidung & Haltung glaubwürdig
✅ Diversität selbstverständlich dargestellt
✅ Keine Gesundheits-Klischees oder Übertreibungen
✅ Perspektive harmonisch (Augenhöhe, Drittelregel)
✅ DSGVO-konform (keine sensiblen Daten sichtbar)

---

## 🎨 10. TK-spezifische Stilrichtlinien

### Farbwelt
- **Primärfarbe:** TK-Blau und Cyan (frisch, modern, vertrauenswürdig)
- **Sekundärfarben:** Grün (Gesundheit, Vitalität), Weiß (Klarheit, Transparenz)
- **Akzentfarben:** Warme Grautöne, natürliche Hauttöne

### Bildsprache
- **Menschlich:** Echte Emotionen, keine gestellten Stock-Fotos
- **Modern:** Zeitgemäße Technologie, aber nicht kühl
- **Nahbar:** Auf Augenhöhe, einladend, nicht distanziert
- **Kompetent:** Professionell, aber nicht steril
- **Divers:** Selbstverständliche Abbildung verschiedener Menschen

### Vermeiden
- ❌ Klinische Krankenhausatmosphäre
- ❌ Kitschige Gesundheitssymbolik (rote Herzen, Kreuz-Symbolik)
- ❌ Übertriebene Fitness-Ästhetik
- ❌ Sterile, unpersönliche Tech-Darstellung
- ❌ Homogene Darstellung (nur junge, sportliche Menschen)

---

## 💡 11. Praktische Tipps für den Arbeitsalltag

### Für Social Media
- Quadratisches Format (1:1) oder Hochformat (9:16) mitdenken
- Platz für Text-Overlays einplanen
- Kompaktere Prompts verwenden
- Stärkere emotionale Momente betonen

### Für Print-Materialien
- Hochauflösende Qualität betonen (8k, 300dpi)
- Querformat (16:9 oder 4:3) bevorzugen
- Ruhigere Kompositionen für bessere Lesbarkeit

### Für Präsentationen
- Klare Fokuspunkte setzen
- Genug Weißraum für Texteinblendungen
- Professioneller Look, aber nicht zu formal

### Für Employer Branding
- Authentizität vor Perfektion
- Vielfalt der Mitarbeitenden zeigen
- Arbeitsumgebung realistisch darstellen
- Persönlichkeit durchscheinen lassen

---

## 🚀 12. Schnellstart-Guide

### In 5 Schritten zum perfekten TK-Bild:

1. **Ziel definieren:** Welche Botschaft? Welcher Kanal?
2. **Template wählen:** Passendes Beispiel aus diesem Guide
3. **Anpassen:** Spezifische Details für Ihr Projekt ergänzen
4. **Qualitätskontrolle:** Checkliste durchgehen
5. **Generieren:** Prompt in KI-Tool eingeben und iterieren

### Beispiel-Workflow:
```
Aufgabe: Social Media Post für neue TK-App
↓
Template #3 (Digitale Services) wählen
↓
Anpassen: Smartphone statt Tablet, jüngere Zielgruppe, Hochformat
↓
Checkliste: TK-Farben ✓, Authentisch ✓, Divers ✓
↓
Generieren und feintunen
```

---

