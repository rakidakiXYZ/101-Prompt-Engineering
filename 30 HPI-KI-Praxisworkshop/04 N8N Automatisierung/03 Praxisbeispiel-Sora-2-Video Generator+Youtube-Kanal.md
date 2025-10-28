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

Anschließend wählen wir dann GPT-5 mini als Modell aus

<img width="3442" height="1888" alt="CleanShot 2025-10-28 at 05 13 48@2x" src="https://github.com/user-attachments/assets/7bac46cd-2330-4894-ad1d-78b9594e160c" />

In der LLM Chain fügen wir dann noch den Prompt "Generate Script" als Anweisung für die LLM Chain hinzu. In der System Message habenw wir ja die komplette Rolle hinterlegt
<img width="3452" height="1904" alt="CleanShot 2025-10-28 at 05 15 11@2x" src="https://github.com/user-attachments/assets/1e3864ee-c877-4b18-bf5c-3339e46b250f" />

Jetzt können wir das ganze schon mal testen:
<img width="3422" height="1892" alt="CleanShot 2025-10-28 at 05 16 36@2x" src="https://github.com/user-attachments/assets/062d358d-9772-4cd1-8833-c71284911bcc" />

Diesen Output benötigen wir jetzt noch als Structure Output:
<img width="3446" height="1898" alt="CleanShot 2025-10-28 at 05 22 34@2x" src="https://github.com/user-attachments/assets/963a289f-c09e-4979-a9b3-9c76bf8ea5ee" />


# Wir wollen jetzt mit OpenAI Sora 2 das Video generieren
<img width="3440" height="1908" alt="CleanShot 2025-10-28 at 05 25 47@2x" src="https://github.com/user-attachments/assets/d979f8c6-9f5a-45db-a726-9c980c923be1" />

Hier sieht man, dass aktuell keine Aktion für Generate Video with Sora 2 zur Verfügung steht, daher müssen wir mit einem HTTPRequest arbeiten
<img width="3442" height="1898" alt="CleanShot 2025-10-28 at 05 27 23@2x" src="https://github.com/user-attachments/assets/3a6e338d-aa58-4f63-b696-5108f865c811" />

Wir müssen jetzt einen POST Request machen an die API von Open AI: https://api.openai.com/v1/videos


Und dann müssen wir noch die Credentials für den Zugriff eingeben über "Generic Credential Type und Header Auth

<img width="3434" height="1896" alt="CleanShot 2025-10-28 at 05 31 28@2x" src="https://github.com/user-attachments/assets/e8ae32f6-d7a4-4b82-9e4c-fa0be77c9dda" />

Name ist "Authorization"
Value ist der Begriff "Bearer" Leerzeichen gefolgt von dem OpenAI API Key

<img width="720" height="262" alt="CleanShot 2025-10-28 at 05 33 12@2x" src="https://github.com/user-attachments/assets/e7f54f6d-dc7c-4801-b31e-71e980349870" />

Das sieht dann so aus:
<img width="3448" height="1896" alt="CleanShot 2025-10-28 at 05 33 41@2x" src="https://github.com/user-attachments/assets/e407901f-6508-4ff1-bf7d-0681f463bf69" />

Jetzt müssen wir definieren was wir per HTTPRequest Post versenden wollen über Send Body:

<img width="3436" height="1896" alt="CleanShot 2025-10-28 at 05 36 35@2x" src="https://github.com/user-attachments/assets/d1a952b6-1c89-46c8-a886-72f1004de3a8" />

Hier müssen wir die Parameter definieren (Model, Auflösung, Dauer, ...)

Diese Details findet man bei OpenAI über diese Webseite: https://platform.openai.com/docs/api-reference/videos

Wir können das ganze jetzt testen:
<img width="3426" height="1878" alt="CleanShot 2025-10-28 at 05 39 27@2x" src="https://github.com/user-attachments/assets/c38aeb79-e29c-4586-a2cd-a039e2aa07cb" />

Hier sehen wir, dass die Produktion des Videos in einer "queued" Warteschlange sich befindet. Das bedeutet wir brauchen noch einen HTTPRequest, um den Status der Videoproduktion zu prüfen - also eine Art Warteschlagen Management

<img width="3452" height="1904" alt="CleanShot 2025-10-28 at 05 43 02@2x" src="https://github.com/user-attachments/assets/cdc837a7-b5bf-4ef4-867d-f11c873f9718" />

Wir wollen etwas abfragen, also verwenden wir die GET Methode und fragen dann bei der Video-Generierungs-API von OpenAI den Status für die ID der aktuellen Videoproduktion ab

<img width="3430" height="1878" alt="CleanShot 2025-10-28 at 05 42 31@2x" src="https://github.com/user-attachments/assets/c2e32bc2-124c-40b1-8e32-5f7cd771a51f" />

Dazu verwenden wir die schon zuvor verwendete URL: https://api.openai.com/v1/videos und hängen einen / und dann die ID des Videos daran

Dann müssen wir den Zugriff authorisieren mit den zuvor schon erstellten Credentials:

<img width="3440" height="1902" alt="CleanShot 2025-10-28 at 05 45 38@2x" src="https://github.com/user-attachments/assets/326c15af-9548-45d2-b2a9-2ac0aa704e3a" />

Wenn wir den Node jetzt ausführen, sehen wir den Status für dieses Video:

<img width="3430" height="1894" alt="CleanShot 2025-10-28 at 05 46 21@2x" src="https://github.com/user-attachments/assets/1026367b-3857-409c-b9d2-d0c2d403d0da" />

Hier sehen wir jetzt den Status "completed"

Was wir jetzt noch machen müssen ist eine kleine Abfrage hinzufügen, um diesen Status zu prüfen und wenn dieser von queued auf completed springt, dann mit dem nächsten Schritt weiter zu machen.

<img width="3432" height="1884" alt="CleanShot 2025-10-28 at 05 48 59@2x" src="https://github.com/user-attachments/assets/d89204b0-09cf-4666-9015-6f38e53d5527" />

Jetzt haben wir zwei Ausgänge von diesem IF Node: wenn der Status "completed" dann geht es weiter und wenn nicht, dann soll noch mal gewartet werden, d.h. wir fügen eine Warteschleife jetzt noch ein, die dann nach 5 sek. z.B. erneut den Status abfragen wird

<img width="3436" height="1894" alt="CleanShot 2025-10-28 at 05 50 49@2x" src="https://github.com/user-attachments/assets/7073e895-4d9a-493c-8204-ba217f75e860" />


So sieht der Workflow jetzt aus:
<img width="3436" height="1898" alt="CleanShot 2025-10-28 at 05 51 32@2x" src="https://github.com/user-attachments/assets/39d33e45-5c91-43fe-bb2c-a4745cf81e9f" />

Hier haben wir jetzt auch den IF Node ausgeführt und gesehen, dass es mit dem TRUE Pfad weitergehen wird

So, wenn also das Video fertig ist, wollen wir es noch herunterladen, dazu brauchen wir auch wieder einen HTTPRequest Node

Wir verwenden die GET Methode, da wir das Video ja abholen wollen und die gleiche URL wieder mit der ID des Scripts plus der Ergänzung /content
Also: https://api.openai.com/v1/videos/...(id des Videos)/content

<img width="3436" height="1884" alt="CleanShot 2025-10-28 at 05 54 46@2x" src="https://github.com/user-attachments/assets/b2afe65d-4044-4a79-82d9-b855fd41e523" />

Dann müssen wir noch die Credentials (Header, Auth, ...) wie zuvor hinterlegen, wir haben das ja schon gemacht und müssen nur den Eintrag OpenAI jetzt auswählen
<img width="3436" height="1902" alt="CleanShot 2025-10-28 at 05 56 20@2x" src="https://github.com/user-attachments/assets/ce3096b0-565d-45e9-944f-b31be38284a7" />

Anschließend können wir den Node ausführen und prüfen, ob das Video heruntergeladen wird

<img width="3436" height="1902" alt="CleanShot 2025-10-28 at 05 57 28@2x" src="https://github.com/user-attachments/assets/cfc61a43-209f-493b-8f8a-dc4bb31b114a" />

Das Video steht zur Verfügung und man kann es sich anschauen:
<img width="1202" height="2096" alt="CleanShot 2025-10-28 at 05 58 01@2x" src="https://github.com/user-attachments/assets/4c1e36fa-c8db-415c-8583-e1efc6147dec" />


# Upload to Youtube
Jetzt müssen wir das generierte Video nur noch zu Youtube hochladen

<img width="3444" height="1902" alt="CleanShot 2025-10-28 at 06 03 58@2x" src="https://github.com/user-attachments/assets/d5e222b5-3bb8-4c70-9574-ac32cfde5bc8" />
Dazu wählen wir die Aktion Upload Video für Youtube aus

<img width="3436" height="1898" alt="CleanShot 2025-10-28 at 06 04 41@2x" src="https://github.com/user-attachments/assets/1bb3e5fa-a867-48df-a61b-2886b66033c9" />

## Google Account - Youtube - Credentials für Google Services

Grundvoraussetzung ist ein Google Account 
<img width="3434" height="1906" alt="CleanShot 2025-10-28 at 07 16 30@2x" src="https://github.com/user-attachments/assets/0692fbad-0f3f-4b89-9868-78f8bbb25748" />

Aufruf der Konsole für die Google Cloud Services über folgende URL: https://console.cloud.google.com/

<img width="3446" height="1908" alt="CleanShot 2025-10-28 at 07 17 26@2x" src="https://github.com/user-attachments/assets/7cc35ca0-a05c-4c18-a7dc-6c7c72cad592" />

Erstellung eines neuen Projektes in der Google Cloud Console
<img width="3454" height="1710" alt="CleanShot 2025-10-28 at 07 18 16@2x" src="https://github.com/user-attachments/assets/2832e4f0-36d3-420f-a939-9e359a5c3ba3" />

Wenn man über Neues Projekt dann ein Projekt anlegt ist in der Regel auch noch keine Organisation vorhanden, die wird dann zuerst angelegt

<img width="2550" height="1094" alt="CleanShot 2025-10-28 at 07 18 58@2x" src="https://github.com/user-attachments/assets/ac2d9837-1936-42da-b949-671339d882b0" />

Projekte dienen dazu die verschiedenen Leistungen von Google und natürlich auch die dazu passenden Abrechnungen zu ordnen, daher hat man irgendwann auch diverse Projekte und ggf. auch Organisationen in der Verwaltung in der Console:

<img width="3448" height="1656" alt="CleanShot 2025-10-28 at 07 19 48@2x" src="https://github.com/user-attachments/assets/84d582ba-bfbf-475b-bf3a-f606859ec611" />

Über den Menüeintrag oben links kann man dann auf die diversen Services zugreifen und wir wollen jetzt zu den APIs und Diensten, um die Zugriffe von N8N auf die Google Services zu definieren

<img width="3442" height="1732" alt="CleanShot 2025-10-28 at 07 20 58@2x" src="https://github.com/user-attachments/assets/edc07ab0-2bac-4f3e-b882-b1cf8d055c58" />

Hier wollen wir auf den Dienst OAUTH-Zustimmungsbildschirm zugreifen, um die Credentials für den Zugriff von N8N zu ermöglichen

<img width="3446" height="1906" alt="CleanShot 2025-10-28 at 07 23 43@2x" src="https://github.com/user-attachments/assets/cc9f2646-18fd-4c21-9115-41630deff3c5" />

Wir starten hier mit dem Button erste Schritte

<img width="2736" height="1424" alt="CleanShot 2025-10-28 at 07 24 23@2x" src="https://github.com/user-attachments/assets/a4aec5c7-d933-404e-87e0-a8a53ba858a9" />

Dann geben wir die Informationen für den Anwendungsnamen und die E-Mail Adresse ein

<img width="3450" height="1914" alt="CleanShot 2025-10-28 at 07 27 02@2x" src="https://github.com/user-attachments/assets/9675a025-a5b6-4db5-889c-115ca144d147" />

Hier verwenden wir einen sinnvollen Namen und in diesem Fall die E-Mail Adresse des Google Accounts

<img width="2692" height="1756" alt="CleanShot 2025-10-28 at 07 36 23@2x" src="https://github.com/user-attachments/assets/1bb8d693-ba55-4e49-be09-0caca8385462" />

Zugriff auf diesen Service muss definiert werden: intern bedeutet, dass wir die E-Mail Adressen angeben müssen, extern bedeutet, dass beliebige User zugreifen dürfen

<img width="2700" height="1336" alt="CleanShot 2025-10-28 at 07 37 55@2x" src="https://github.com/user-attachments/assets/2191e9bf-404c-4ae3-a4d5-506539cf1d72" />

Für den Service geben wir dann noch eine Kontaktadresse ein

<img width="3450" height="1910" alt="CleanShot 2025-10-28 at 07 38 33@2x" src="https://github.com/user-attachments/assets/53a03404-f246-4756-bf4d-edaddbcfb133" />

Dann bestätigen wir das ganz und machen weiter

<img width="3446" height="1904" alt="CleanShot 2025-10-28 at 07 38 59@2x" src="https://github.com/user-attachments/assets/f1e27361-c5c6-4d5d-bc7b-5629788ce25e" />

Damit haben wir auf diesen OAuth Client auch zugreifen können müssen wir diesen veröffentlichen. Dazu klicken wir auf Zielgruppe:

<img width="3448" height="1914" alt="CleanShot 2025-10-28 at 07 40 25@2x" src="https://github.com/user-attachments/assets/5258a7f6-e409-4cfd-b6fa-d5bfde2c128d" />

Wir klicken hier auf veröffentlichen - für die Veröffentlichung als produktiven Service

<img width="3454" height="1910" alt="CleanShot 2025-10-28 at 07 41 09@2x" src="https://github.com/user-attachments/assets/8c9a32f8-e57c-4617-ad17-8b5d05b2fca2" />

Dann gehen wir in der Navigationsleiste links auf Clients

<img width="3454" height="1912" alt="CleanShot 2025-10-28 at 07 42 02@2x" src="https://github.com/user-attachments/assets/47904872-af45-468e-9c3c-a28f2de54a56" />

Hier sehen wir, dass noch keine Client-IDs erstellt sind, daher starten wir mit der Erstellung:

<img width="2686" height="1910" alt="CleanShot 2025-10-28 at 07 42 44@2x" src="https://github.com/user-attachments/assets/b87ab36f-bf81-4084-aec2-2aef4b29a036" />

Wir vergeben einen Namen (hier kann man für verschiedene Projekte, Szenarien, ... sinnvolle Namen definieren)
<img width="2752" height="1836" alt="CleanShot 2025-10-28 at 07 44 09@2x" src="https://github.com/user-attachments/assets/d654736f-0513-4c3b-96f1-f3bee7459a68" />

Da wir über eine Domain von N8N Cloud auf diesen Google Service zugreifen und hier mit JavaScript Code u.a. gearbeitet wird, sollten wir die N8N Cloud Domain hier angeben, siehe nachfolgender URL Screenshot:

<img width="804" height="262" alt="CleanShot 2025-10-28 at 07 45 34@2x" src="https://github.com/user-attachments/assets/cb31690d-d21f-45ab-a2cc-262c4bcfe4c3" />

Diese Domain fügen wir hier ein:
<img width="2702" height="1894" alt="CleanShot 2025-10-28 at 07 46 27@2x" src="https://github.com/user-attachments/assets/ca054b1b-25f5-4709-b56f-b5b01493609e" />

Jetzt benötigen wir noch eine Redirect URL von N8N - also die Rücksprung Verbindung, die bekommen wir aus der Authorisierungsmaske für Youtube aus N8N oder aus einer anderen N8N Node Authorisierung für einen Google Service:

<img width="3408" height="1880" alt="CleanShot 2025-10-28 at 07 47 39@2x" src="https://github.com/user-attachments/assets/db8c5205-b403-4a53-b69c-8d886535c2da" />

Diese URL können wir hier in N8N kopieren und dann wieder zurück in der Google Console einfügen:

<img width="3436" height="1918" alt="CleanShot 2025-10-28 at 07 48 21@2x" src="https://github.com/user-attachments/assets/3f6c8233-3dd0-4f99-a433-5a779da21c1a" />

Dann können wir auf Erstellen klicken

Es erscheint dann ein Dialogfenster mit der Client ID und dem Client Secret, welche wir dann kopieren und in N8N einfügen:

<img width="2406" height="1494" alt="CleanShot 2025-10-28 at 07 53 37@2x" src="https://github.com/user-attachments/assets/324c4e00-e132-4034-9490-ff69ac9c3d26" />

Und in der Google Console sehen wir den Eintrag für diesen OAuth Client
<img width="3442" height="884" alt="CleanShot 2025-10-28 at 07 53 55@2x" src="https://github.com/user-attachments/assets/54151f42-ab3b-44d3-ad7a-cacdceca5932" />

Ganz unten in dem N8N Auth Fenster können wir jetzt mit dem Google Konto uns anmelden und damit sozusagen als authorisierter User die Verbindung zu N8N mit Google Services bestätigen 

<img width="3066" height="1734" alt="CleanShot 2025-10-28 at 07 55 41@2x" src="https://github.com/user-attachments/assets/9ea924a3-4b82-4a52-bdcc-b36ddb440929" />

Hier erfolgt dann auch noch die Abfrage für welchen Youtube Kanal man das mit dem angemeldeten Google Konto machen möchte, also hier den gerade erstellten Kanal auswählen:

<img width="984" height="1382" alt="CleanShot 2025-10-28 at 08 01 39@2x" src="https://github.com/user-attachments/assets/b5794f9f-41c2-49ad-a309-d3766c433450" />


Es wird dann noch angezeigt, welche Services Sie jetzt freigeben zur Nutzung mit N8N:
<img width="968" height="1138" alt="CleanShot 2025-10-28 at 07 57 18@2x" src="https://github.com/user-attachments/assets/11e1dfe6-3de8-4d6e-833c-e83d8397957e" />




In N8N erhält man dann noch eine Rückmeldung, dass die Verbindung erfolgreich war:

<img width="2370" height="596" alt="CleanShot 2025-10-28 at 07 58 03@2x" src="https://github.com/user-attachments/assets/dea0982a-58bf-4e60-a0a1-68a0dbea9359" />

So - jetzt können wir weitermachen, um den Upload genauer zu definieren:

<img width="3402" height="1852" alt="CleanShot 2025-10-28 at 08 04 56@2x" src="https://github.com/user-attachments/assets/7207761f-50d5-426c-8fa1-6311b9de56da" />

Im oberen Bereich wechseln wir die linke Anzeige von Binary auf Schema, wo wir dann im unteren linken Bereich die einzelnen Ergebnisse der Workflow Schritte sehen:

<img width="3382" height="1832" alt="CleanShot 2025-10-28 at 08 05 24@2x" src="https://github.com/user-attachments/assets/e3087b77-38d5-4adc-aa95-e5c8246db227" />

Dort können wir die Basic LLM Chain aufklappen und sehen hier den Output und u.a. den Titel

<img width="3410" height="1866" alt="CleanShot 2025-10-28 at 08 06 03@2x" src="https://github.com/user-attachments/assets/7a51ebf0-ac52-4eb8-863a-6ce164a65cb5" />

Wir füllen jetzt die Felder Titel mit der ID aus dem Workfow, die Region wählen wir aus "Germany" und die Kategorie für Youtube wird entweder im Drop-Down zur Auswahl gestellt, wir wählen hier Entertainment aus. Bei den Daten wählen wir oben anstellen von Schema wieder Binary und sehen, das die Datei den Variablen Namen "data" hat, den wir hier übernehmen.

<img width="3398" height="1846" alt="CleanShot 2025-10-28 at 08 11 04@2x" src="https://github.com/user-attachments/assets/ae73ccf8-8c06-4715-98d6-0e3a8bcef27e" />

Wir können dann noch einen zusätzlichen Parameter hinzufügen - die Beschreibung / Description:
<img width="3368" height="1824" alt="CleanShot 2025-10-28 at 08 12 09@2x" src="https://github.com/user-attachments/assets/41cc5494-2272-4cfa-9ccb-a0c5d77737ce" />

Und diese Beschreibung ergänzen wir dann noch:

<img width="3388" height="1856" alt="CleanShot 2025-10-28 at 08 13 07@2x" src="https://github.com/user-attachments/assets/a3279acb-ff2c-4f76-80cc-04f5c537b0be" />


















