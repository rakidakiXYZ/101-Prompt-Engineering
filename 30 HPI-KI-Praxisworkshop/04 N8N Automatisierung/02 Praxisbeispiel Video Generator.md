# N8N Überblick

# N8N neuer Workflow
Trigger


# Basic LLM Chain
Auswahl eines LLM für die Erstellung eines Scripts für das Video

<img width="3446" height="1902" alt="CleanShot 2025-10-28 at 02 30 10@2x" src="https://github.com/user-attachments/assets/b9f6f5f5-43a2-49e5-9720-8ccb4ebb976a" />

# Google API Key

<img width="3444" height="1912" alt="CleanShot 2025-10-28 at 02 37 19@2x" src="https://github.com/user-attachments/assets/e41bd6ef-0072-4c8c-8f0a-ec67aca8f30d" />


# Auswahl des Modells von Google
<img width="3450" height="1900" alt="CleanShot 2025-10-28 at 02 40 29@2x" src="https://github.com/user-attachments/assets/a2abb53d-002b-452a-8c5b-6190b2b50382" />

# Wir probieren das LLM aus:
<img width="3410" height="1884" alt="CleanShot 2025-10-28 at 02 41 52@2x" src="https://github.com/user-attachments/assets/cef9a860-5167-4beb-bcd1-09743b534994" />

# Kosten Nutzung LLM mit API Keys
<img width="3444" height="1908" alt="CleanShot 2025-10-28 at 02 44 43@2x" src="https://github.com/user-attachments/assets/14c71b93-b364-4183-a1a7-72b3f381cedf" />

Budgets definieren
<img width="3442" height="1908" alt="CleanShot 2025-10-28 at 02 46 14@2x" src="https://github.com/user-attachments/assets/5331c794-2483-44da-8125-eafb95e69577" />

# Prompt Engineering für Video Skripte
Wir erstellen eine System Message

<img width="3440" height="1898" alt="CleanShot 2025-10-28 at 02 48 12@2x" src="https://github.com/user-attachments/assets/edb49602-385e-4459-bab5-c543c4124ed8" />

# Wir nutzen ChatGPT, um dann den Prompt hier zu generieren
Wissen 1: https://cloud.google.com/blog/products/ai-machine-learning/ultimate-prompting-guide-for-veo-3-1?hl=en
Wissen 2: https://deepmind.google/models/veo/prompt-guide/

# Prompt:
Wir starten mit ChatGPT, um einen Prompt zu generieren, hier der Input:

```
Please improve my prompt to work with Veo 3.1.

This is my prompt
"Create a script for a short, 8-second social-media video promoting health and fitness for a health insurance company. Output return a JSON structure containing: Videoscript - Youtube Title - Youtube Description"

Here is the veo 3.1 prompt guide and example prompts:

Und danach fügen wir dann das Wissen von den obigen beiden Seiten ein Copy&Paste
```

# Ergebnis von ChatGPT:

Perfect — you’re looking to upgrade your **Veo 3.1 prompt** so it aligns with its **cinematography-first design** and returns your desired **structured JSON output** (`Videoscript`, `Youtube Title`, `Youtube Description`).

Below is an **optimized and Veo-3.1–ready version** of your original prompt, with cinematic detail, timestamp sequencing, sound direction, and clear JSON formatting instructions.

---

### 💡 Improved Veo 3.1 Prompt

**Prompt:**

```
Create an 8-second cinematic video promoting health and fitness for a health insurance company. 

Use timestamp-based direction with descriptive cinematography, subject, action, context, and ambiance for each shot. Include natural sound effects and upbeat background music. Avoid brand logos or text overlays within the video.

[00:00–00:02] Wide aerial shot over a sunrise-lit city park. Morning mist rolls over the grass as joggers begin their runs. SFX: soft morning breeze, distant birds, ambient city hum. Mood: hopeful and energizing.

[00:02–00:04] Medium tracking shot of a young woman jogging past trees, earbuds in, smiling confidently. Sunlight flares through the leaves. Cinematic lens flare, shallow depth of field. SFX: rhythmic footsteps on gravel, upbeat music building softly.

[00:04–00:06] Close-up on the woman’s face as she exhales and smiles, sweat glistening, the sun behind her. Emotion: empowerment, health, vitality. Lighting: warm golden tones.

[00:06–00:08] Crane shot rising above a group of diverse people stretching and laughing together on the grass, framed by the glowing sunrise. SFX: joyful chatter, birds, music crescendo. Tone: community, motivation, wellness.

After generating the visual and audio sequence, return a structured JSON output with the following keys:
{
  "Videoscript": "Concise summary of the scene-by-scene visuals and audio.",
  "Youtube Title": "Catchy, SEO-optimized title (under 70 characters).",
  "Youtube Description": "Short description (under 200 words) promoting health, fitness, and the company’s commitment to well-being. Include a call to action."
}

Style & Ambiance: Cinematic, natural lighting, uplifting, motivational, modern health aesthetic.
```

---

### 🧠 Why This Works

✅ **Follows Veo’s five-part formula:**
Each timestamp clearly defines cinematography, subject, action, context, and ambiance.

✅ **Timestamp workflow:**
Enables multi-shot control within a single Veo generation.

✅ **Audio direction:**
Includes SFX and music cues to help Veo design the soundstage.

✅ **Structured JSON return:**
Ensures you get a clean, parseable output ready for downstream automation.

✅ **Cinematic clarity:**
Uses warm, emotionally resonant visual language aligned with Veo’s cinematic style.

---

Would you like me to **adapt this prompt for a specific tone** (e.g., *corporate professional*, *inspirational lifestyle*, or *youthful energy*)?
That tweak would help align Veo’s mood and pacing with your target audience.
