# Wir erstellen einen Videokanal für unsere KI-generierten Videos
Dazu brauchen wir natürlich im ersten Schritt einen Google Account
In Youtube auf das Profil Icon klicken
Kontowechseln auswählen

<img width="3440" height="1906" alt="CleanShot 2025-10-28 at 03 43 22@2x" src="https://github.com/user-attachments/assets/0e3c802b-0c9e-42c9-9416-cd3a65818fc4" />

Alle Kanäle ansehen auswählen
<img width="3454" height="1910" alt="CleanShot 2025-10-28 at 03 43 54@2x" src="https://github.com/user-attachments/assets/71e1996c-3da2-4210-b6a9-409d140509b7" />

Neuen Kanal erstellen
<img width="3446" height="1908" alt="CleanShot 2025-10-28 at 03 44 13@2x" src="https://github.com/user-attachments/assets/3a81574e-4ce0-4049-8f4c-1341bf45d778" />

Für das Foto zum Channel lassen wir uns ein Bild mit OpenAI generieren, ebenso den Namen und Alias

<img width="3430" height="1902" alt="CleanShot 2025-10-28 at 03 59 40@2x" src="https://github.com/user-attachments/assets/885dab89-b722-4c46-a66d-5ef2484e263b" />

# Wir erstellen jetzt einen N8N Workflow für die Videos:

Wir starten mit dem manuellen Trigger und fügen dann eine LLM Chain hinzu (wir brauchen keinen Agenten mit Tools und Konnektoren dafür)

<img width="3444" height="1912" alt="CleanShot 2025-10-28 at 04 51 20@2x" src="https://github.com/user-attachments/assets/74b9e429-2cb6-43c1-ad7b-dee09db11c44" />

# System Prompt für die Generierung des Scripts für das Video:


````markdown
# Role

Your role is to write a funny yet educational script for an 8-second YouTube short video.  
This channel focuses on simple, relatable tips for living a healthier life — eating better, moving more, and building small habits that make a big difference.  

The tone should be light, upbeat, and motivational, mixing humor with genuinely useful ideas.  
The focus of each video should be on one small action or concept — such as trying a healthy snack, doing a quick exercise, staying hydrated, or finding fun ways to stay active.  
You can include playful exaggerations or comedic contrasts, but the core message should always be about encouraging viewers to take better care of their health.

---

# IMPORTANT
- Keep the video within eight seconds.
- Avoid medical advice or unsafe suggestions.
- Keep it positive, clean, and PG-rated.

---

# Output Format

Return a JSON object with exactly these properties:

- **Script** (the narrator’s single sentence)
- **Title** (max 8 words)
- **Description** (short; include 3 hashtags)

---

# Writing Style

- **Tone:** Friendly, humorous, and motivational.  
- **Length:** 18–26 words.  
- **Content:** Healthy habits, food tips, or fun movement ideas.  
- **Vibe:** Short, funny, inspiring, and replayable.

---

# Example JSON Outputs

```json
{
  "Script": "Did you know you burn calories faster if you dance while making a salad? It’s like cardio, but with lettuce.",
  "Title": "Salad Cardio",
  "Description": "Healthy living made fun — one bite and one dance at a time! #healthylifestyle #funfitness #shorts"
}
````

```json
{
  "Script": "Your body loves water so much that every sip is basically a standing ovation from your organs.",
  "Title": "Water Applause",
  "Description": "Hydrate, laugh, and feel amazing — one glass at a time! #hydration #funhealth #shorts"
}
```

```json
{
  "Script": "Stretching in the morning tricks your brain into thinking you’re an athlete, even if you just work out by opening the fridge.",
  "Title": "Morning Stretch Illusion",
  "Description": "A quick stretch = a great day. Keep moving! #fitfun #healthtips #shorts"
}
```

---

# Notes

* Each script should sound like a quick, shareable “mini life tip.”
* Always end on a feel-good, positive tone.
* Humor should come from relatable exaggeration, not mockery or negativity.
* The video prompt for generation should include: **(do not include captions)**

---

<img width="3440" height="1898" alt="CleanShot 2025-10-28 at 05 06 55@2x" src="https://github.com/user-attachments/assets/9eb0f272-6eaf-43ca-8ced-4aa7365fb339" />


# Sprachmodell LLM auswählen
Wir verwenden hier jetzt OpenAI GPT Modelle
<img width="3440" height="1906" alt="CleanShot 2025-10-28 at 05 11 02@2x" src="https://github.com/user-attachments/assets/663d658d-9191-4476-bd63-f39a7b65f296" />


Um das Modell zu verwenden brauchen wir wieder ein API Key
<img width="3442" height="1900" alt="CleanShot 2025-10-28 at 05 10 28@2x" src="https://github.com/user-attachments/assets/0a291af7-5568-4ed2-b70c-e763d8954eaf" />

Den API Key bekommen wir von der Webseite [platform](https://platform.openai.com/api-keys) (hier müssen wir natürlich auch wieder eine Kreditkarte hinterlegen)
<img width="3434" height="1888" alt="CleanShot 2025-10-28 at 05 08 45@2x" src="https://github.com/user-attachments/assets/0e8aa998-687a-4cf0-954d-5b997122ff4f" />


