# KI-Bildgenerierung: Anleitung für HR & Marketing

## Was ist das?

Dieser **JSON-Prompt** ist eine Vorlage zur Erstellung professioneller Portrait-Fotos mit KI-Bildgeneratoren. Sie können damit aus einem echten Foto eine Person in einem neuen Setting, mit neuer Kleidung und professioneller Beleuchtung darstellen lassen.

---

## 🎯 Anwendungsfälle für TK HR & Marketing

**HR-Abteilung:**
- Mitarbeiterportraits für interne Kommunikation
- Diverse Kandidaten-Beispiele für Recruiting-Kampagnen
- Schulungsmaterialien mit authentischen Gesichtern

**Marketing:**
- Kampagnenbilder ohne kostspielige Fotoshootings
- Diverse Testimonials für verschiedene Zielgruppen
- Social Media Content mit konsistentem Look

---

## 📋 Schritt-für-Schritt Anleitung

### **Schritt 1: Vorbereitung**
- Laden Sie ein **Referenzfoto** der Person hoch (Frontalansicht, gute Qualität)
- Wählen Sie einen KI-Bildgenerator (z.B. Midjourney, Leonardo AI)

### **Schritt 2: Prompt anpassen**
Bearbeiten Sie diese Bereiche:

**Wichtigste Anpassungen:**

| Bereich | Was ändern | Beispiel für TK |
|---------|------------|-----------------|
| `"who"` | Beschreibung der Person | "professional woman in her 30s" |
| `"wardrobe"` | Kleidung | "business casual: white blouse, navy blazer" |
| `"scene" → "location"` | Hintergrund | "modern office environment" oder "healthcare setting" |
| `"mood"` | Stimmung | "trustworthy, approachable, professional" |

### **Schritt 3: Prompt umwandeln**
Der JSON-Style ist zur Übersicht – die meisten KI-Tools brauchen **Fließtext**:

**Beispiel-Umwandlung:**
```
Create a photorealistic portrait using the uploaded reference photo. 
Keep exact facial features unchanged. Show a professional woman in 
her 30s wearing a white blouse and navy blazer, seated in a modern 
office with soft natural lighting. Vertical 9:16 format, shallow 
depth of field, calm and trustworthy expression.
```

### **Schritt 4: Generieren & verfeinern**
- Generieren Sie 3-4 Varianten
- Wählen Sie die beste aus
- Bei Bedarf: Details im Prompt anpassen und neu generieren

---

## ⚠️ Wichtige Hinweise für die TK

### **Rechtliches:**
- ✅ Holen Sie **Einwilligung** ein, bevor Sie Mitarbeiterfotos verwenden
- ✅ Prüfen Sie **Lizenzrechte** des KI-Tools für kommerzielle Nutzung
- ✅ Kennzeichnen Sie KI-generierte Bilder transparent

### **Markenkonformität:**
Passen Sie für TK-CI an:
```json
"wardrobe": "colors: navy blue, white, light grey (TK brand colors)",
"scene": "clean, professional, health-focused environment",
"mood": "trustworthy, caring, competent"
```

### **Best Practices:**
- Verwenden Sie **diverse** Referenzbilder für inklusive Darstellung
- Achten Sie auf **Authentizität** – keine Überglättung
- Testen Sie verschiedene **Settings** (Büro, Beratungssituation, casual)

---

## 🚀 Schnellstart-Beispiel für TK

```
Photorealistic portrait, keep uploaded face identity exact.
Show a confident female healthcare professional in her 40s,
wearing navy blue blazer over white shirt. Modern TK office 
setting with soft natural light. Warm, trustworthy expression.
Vertical format 9:16, shallow depth of field. 
Exclude: artificial look, logos, text.
```

Viel Erfolg beim Erstellen authentischer, professioneller Bilder für Ihre Kampagnen! 🎨




# Prompt Vorlage

## Englischer JSON Prompt

```
1) JSON-Style Prompt Template (copy → edit placeholders)
{
  "task": "image-to-image",
  "reference_image": "USE_UPLOADED_PHOTO",
  "subject": {
    "who": "young man (use the uploaded face)",
    "identity_lock": "keep exact facial structure, skin tone, hairstyle, and body identity unchanged",
    "pose": "seated on stairs, elbows on thighs, hands loosely clasped, chin slightly lifted, gaze toward the light",
    "expression": "calm, confident, subtle smile"
  },
  "scene": {
    "location": "minimalist indoor stairway beside a matte concrete wall",
    "background": "clean, uncluttered, no logos or text"
  },
  "wardrobe": "black ribbed knit sweater, tapered grey chinos, chunky white sneakers",
  "style": {
    "genre": "cinematic, fashion editorial, ultra-realistic",
    "aesthetics": "fine film grain, sharp details, natural skin texture"
  },
  "lighting": {
    "key": "hard warm sunlight from camera-right creating a crisp rectangular beam",
    "fill": "soft ambient bounce",
    "contrast": "high with long shadows",
    "time_of_day": "golden hour mood"
  },
  "camera": {
    "framing": "vertical portrait",
    "lens": "50–85mm prime",
    "aperture": "f/2.2",
    "angle": "low–mid angle from a few steps below",
    "depth_of_field": "shallow"
  },
  "technical": {
    "quality": "4K, photorealistic textures",
    "aspect_ratio": "9:16",
    "sharpness": "crisp focus on face and eyes"
  },
  "mood": "calm, confident, editorial",
  "exclude": [
    "cartoon, CGI look, over-smoothing, plastic skin",
    "artifacts, banding, blown highlights",
    "warped anatomy, extra fingers, double shadow",
    "dirty wall, clutter, watermark, logo, text"
  ]
}
```

## Englischer Text Prompt

Ultra-realistic cinematic vertical portrait (9:16). Use the uploaded photo as reference and keep the exact facial structure, skin tone, hairstyle, and body identity unchanged. A young man sits on an indoor stairway beside a matte concrete wall. A rectangular beam of warm sunlight from camera-right hits the wall, creating a crisp shadow frame; soft ambient bounce provides fill. Wardrobe: black ribbed knit sweater, tapered grey chinos, chunky white sneakers. Camera: low–mid angle from a few steps below, 50–85mm prime at f/2.2, shallow depth of field, crisp focus on face and eyes. Style: minimalist fashion editorial, ultra-realistic textures, fine film grain, high contrast with long shadows, golden-hour mood. Background clean and uncluttered. Exclude: cartoon/CGI look, over-smoothing, plastic skin, artifacts, banding, blown highlights, warped anatomy, extra fingers, double shadow, dirty wall, clutter, watermark, logo, text.


## Deutscher JSON Prompt:

```
1) JSON-Style Prompt-Vorlage (kopieren → Platzhalter anpassen)
{
  "aufgabe": "image-to-image",
  "referenzbild": "HOCHGELADENES_FOTO_VERWENDEN",
  "motiv": {
    "wer": "junger Mann (verwende das hochgeladene Gesicht)",
    "identitaet": "exakte Gesichtsstruktur, Hautton, Frisur und Körper-Identität unverändert lassen",
    "pose": "sitzend auf Treppe, Ellbogen auf Oberschenkeln, Hände locker gefaltet, Kinn leicht angehoben, Blick zum Licht",
    "mimik": "ruhig, selbstbewusst, dezentes Lächeln"
  },
  "szene": {
    "ort": "minimalistische Innentreppe neben einer matten Betonwand",
    "hintergrund": "sauber, aufgeräumt, keine Logos oder Texte"
  },
  "kleidung": "schwarzer Rippstrick-Pullover, graue Chino mit Tapered Fit, chunky weiße Sneaker",
  "stil": {
    "genre": "cinematic, Fashion-Editorial, ultra-realistisch",
    "aesthetik": "feines Filmkorn, scharfe Details, natürliche Hautstruktur"
  },
  "licht": {
    "key": "hartes, warmes Sonnenlicht von kamera-rechts mit rechteckigem Lichtfenster",
    "fill": "weiches Umgebungs-Reflexlicht",
    "kontrast": "hoch mit langen Schatten",
    "tageszeit": "Golden-Hour-Stimmung"
  },
  "kamera": {
    "framing": "vertikales Porträt",
    "objektiv": "50–85mm Festbrennweite",
    "blende": "f/2.2",
    "winkel": "leicht tiefer Standpunkt, ein paar Stufen darunter",
    "schärfentiefe": "gering (Hintergrund weich)"
  },
  "technik": {
    "qualitaet": "4K, fotorealistische Texturen",
    "seitenverhaeltnis": "9:16",
    "schaerfe": "präziser Fokus auf Gesicht und Augen"
  },
  "stimmung": "ruhig, selbstbewusst, editorial",
  "ausschliessen": [
    "Cartoon/CGI-Look, übermäßiges Weichzeichnen, Plastikhaut",
    "Artefakte, Banding, ausgefressene Lichter",
    "verzerrte Anatomie, extra Finger, doppelte Schatten",
    "schmutzige Wand, Unordnung, Wasserzeichen, Logo, Text"
  ]
}
```

## Deutscher Text Prompt: 

Ultra-realistisches, kinoreifes Hochformat-Porträt (9:16). Verwende das hochgeladene Foto als Referenz und lasse die exakte Gesichtsstruktur, den Hautton, die Frisur und die Körper-Identität unverändert. Ein junger Mann sitzt auf einer Innentreppe neben einer matten Betonwand. Ein rechteckiger Lichtstrahl warmen Sonnenlichts von kamera-rechts trifft die Wand und erzeugt einen klaren Schattenrahmen; weiches Umgebungslicht dient als Aufheller. Kleidung: schwarzer Rippstrick-Pullover, graue Tapered-Chinos, chunky weiße Sneaker. Kamera: leicht tiefer Blickwinkel von ein paar Stufen darunter, 50–85mm Festbrennweite bei f/2.2, geringe Schärfentiefe, präziser Fokus auf Gesicht und Augen. Stil: minimalistisches Fashion-Editorial, ultra-realistischer Look, feines Filmkorn, hoher Kontrast mit langen Schatten, Golden-Hour-Stimmung. Hintergrund sauber und aufgeräumt. Ausschließen: Cartoon/CGI-Look, übermäßiges Weichzeichnen, Plastikhaut, Artefakte, Banding, ausgefressene Lichter, verzerrte Anatomie, extra Finger, doppelte Schatten, schmutzige Wand, Unordnung, Wasserzeichen, Logo, Text.
