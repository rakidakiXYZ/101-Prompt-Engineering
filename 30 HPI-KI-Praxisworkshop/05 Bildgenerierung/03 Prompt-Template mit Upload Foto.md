# Prompt Vorlage

## Englischer JSON Prompt

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

## Englischer Text Prompt

Ultra-realistic cinematic vertical portrait (9:16). Use the uploaded photo as reference and keep the exact facial structure, skin tone, hairstyle, and body identity unchanged. A young man sits on an indoor stairway beside a matte concrete wall. A rectangular beam of warm sunlight from camera-right hits the wall, creating a crisp shadow frame; soft ambient bounce provides fill. Wardrobe: black ribbed knit sweater, tapered grey chinos, chunky white sneakers. Camera: low–mid angle from a few steps below, 50–85mm prime at f/2.2, shallow depth of field, crisp focus on face and eyes. Style: minimalist fashion editorial, ultra-realistic textures, fine film grain, high contrast with long shadows, golden-hour mood. Background clean and uncluttered. Exclude: cartoon/CGI look, over-smoothing, plastic skin, artifacts, banding, blown highlights, warped anatomy, extra fingers, double shadow, dirty wall, clutter, watermark, logo, text.


## Deutscher JSON Prompt:

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

## Deutscher Text Prompt: 

Ultra-realistisches, kinoreifes Hochformat-Porträt (9:16). Verwende das hochgeladene Foto als Referenz und lasse die exakte Gesichtsstruktur, den Hautton, die Frisur und die Körper-Identität unverändert. Ein junger Mann sitzt auf einer Innentreppe neben einer matten Betonwand. Ein rechteckiger Lichtstrahl warmen Sonnenlichts von kamera-rechts trifft die Wand und erzeugt einen klaren Schattenrahmen; weiches Umgebungslicht dient als Aufheller. Kleidung: schwarzer Rippstrick-Pullover, graue Tapered-Chinos, chunky weiße Sneaker. Kamera: leicht tiefer Blickwinkel von ein paar Stufen darunter, 50–85mm Festbrennweite bei f/2.2, geringe Schärfentiefe, präziser Fokus auf Gesicht und Augen. Stil: minimalistisches Fashion-Editorial, ultra-realistischer Look, feines Filmkorn, hoher Kontrast mit langen Schatten, Golden-Hour-Stimmung. Hintergrund sauber und aufgeräumt. Ausschließen: Cartoon/CGI-Look, übermäßiges Weichzeichnen, Plastikhaut, Artefakte, Banding, ausgefressene Lichter, verzerrte Anatomie, extra Finger, doppelte Schatten, schmutzige Wand, Unordnung, Wasserzeichen, Logo, Text.
