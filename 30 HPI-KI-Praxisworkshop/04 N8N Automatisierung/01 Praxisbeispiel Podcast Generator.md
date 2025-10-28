# Wir starten mit einem manuellen Trigger in N8N
<img width="3444" height="1916" alt="CleanShot 2025-10-28 at 09 14 59@2x" src="https://github.com/user-attachments/assets/95323607-2288-49f5-8c09-6c4335158bd0" />

Diesen öffnen wir und bearbeiten den Output - also wir hinterlegen einen statischen Output:
<img width="3440" height="1904" alt="CleanShot 2025-10-28 at 09 16 13@2x" src="https://github.com/user-attachments/assets/2d9ebd7e-ea76-44b6-8ef7-087c7db9d505" />

Wir erstellen dann die Daten für den statischen Output - Link zu einem News Beitrag von Anthropic

<img width="3380" height="1858" alt="CleanShot 2025-10-28 at 09 17 22@2x" src="https://github.com/user-attachments/assets/abbe5517-aae2-4d00-810a-a1286bad1303" />

Diese manuell eingegebenen Daten sind jetzt fest "angepinnt" für die weiteren Workflows / Nodes als Input:
<img width="3448" height="1908" alt="CleanShot 2025-10-28 at 09 18 01@2x" src="https://github.com/user-attachments/assets/b2ac9a81-09d9-4912-8c28-2d4fcfe88329" />

Jetzt wollen wir von dieser URL alle Daten der Webseite herunterladen (scrapen ...). Dafür gibt es in N8N die Integration von Firecrawl - einem Tool, dass man dafür mit ein paar Credits erst Mal kostenlos nutzen kann:

<img width="3438" height="1906" alt="CleanShot 2025-10-28 at 09 19 23@2x" src="https://github.com/user-attachments/assets/10876ff9-8db7-4368-8579-fe5f3039a4f7" />

Wir wählen hier die Aktion Scrape a Website and get its content aus:
<img width="3436" height="1894" alt="CleanShot 2025-10-28 at 09 20 17@2x" src="https://github.com/user-attachments/assets/f8a52696-0c9a-4b10-9f22-8b487fa7b488" />

Jetzt müssen wir unseren API Schlüssel für Firecrawl generieren und dafür auch ein Konto erst bei Firecrawl anlegen:
<img width="3396" height="1854" alt="CleanShot 2025-10-28 at 09 21 09@2x" src="https://github.com/user-attachments/assets/b295f2b7-48e9-4aa2-9053-2a8c922dacb9" />

Wir gehen jetzt auf die Webseite von Firecrawl und erstellen hier einen API Key
<img width="3434" height="1910" alt="CleanShot 2025-10-28 at 09 22 20@2x" src="https://github.com/user-attachments/assets/be6ad449-f35c-46b0-aee0-45f44aa94275" />

Den neuen generierten Key fügen wir dann in N8N ein:
<img width="2912" height="1738" alt="CleanShot 2025-10-28 at 09 23 19@2x" src="https://github.com/user-attachments/assets/ad93b345-8a60-4801-9491-008dabb8a46c" />

Als URL verwenden wir dann die statische URL aus dem vorhergehenden manuellen Trigger:
<img width="3392" height="1852" alt="CleanShot 2025-10-28 at 09 24 28@2x" src="https://github.com/user-attachments/assets/7aac7614-e42e-4830-b50b-9220d70f0c93" />

Wir können dann auch schon direkt diesen Node ausführen, um die Daten von der angegebenen URL zu scrapen:
<img width="3412" height="1878" alt="CleanShot 2025-10-28 at 09 25 09@2x" src="https://github.com/user-attachments/assets/7dd8f187-57bb-4553-b71d-0cfb08793528" />

Wir wollen jetzt die Inhalte nachh dem Scrapen, die im Markdown Format vorliegen (also die Textinformationen der Webseite) als Input in einem LLM verwenden, um damit dann eine Konversation zwischen zwei Personen zu generieren. Dafür verwenden wir als nächsten Node eine LLM Chain:

<img width="3442" height="1914" alt="CleanShot 2025-10-28 at 09 27 06@2x" src="https://github.com/user-attachments/assets/8ee39769-a231-4b43-8a77-9d850ba2818b" />

Wir wollen jetzt den Prompt für diese LLM Chain definieren:
<img width="3382" height="1852" alt="CleanShot 2025-10-28 at 09 28 16@2x" src="https://github.com/user-attachments/assets/d82e0b06-d28a-4066-9b53-20e24fb15203" />

Wir nutzen im ersten Schritt den folgenden Prompt:
<img width="3346" height="1738" alt="CleanShot 2025-10-28 at 09 31 22@2x" src="https://github.com/user-attachments/assets/ef8bac91-c591-43b2-971d-f8405e16261e" />

Prompt
```
Deine Aufgabe ist es, einen Dialog zwischen zwei Podcast-Hosts zu erstellen.

Der erste Host ist eine freundliche und aufgeregte Person.
Der zweite Host ist pessimistisch und skeptisch.

Erstelle bis zu 10 Gesprächsrunden zwischen den beiden Hosts, basierend auf dem untenstehenden Artikel.
Vermeide technische Informationen wie Installationsschritte oder ähnliches im Gespräch.
Stattdessen sollte das Gespräch eine allgemeine Diskussion auf höherer Ebene sein, die sich auf spannende oder kritische Aspekte des Inhalts konzentriert.
```

Im nächsten Schritt müssen wir für die LLM Chain das Sprachmodell auswählen:
<img width="3410" height="1870" alt="CleanShot 2025-10-28 at 09 38 59@2x" src="https://github.com/user-attachments/assets/a1979d99-69e9-4e23-8f26-107eb0b007f9" />

Für die Nutzung müssen wir dann wieder einen OPENAI API Key generieren, damit wir diesen in N8N verwenden können:
<img width="3350" height="1858" alt="CleanShot 2025-10-28 at 09 40 39@2x" src="https://github.com/user-attachments/assets/9434dcdd-92c8-43fb-beda-2a8620e1bc90" />


Generierung eines OpenAI API Keys über die URL: https://platform.openai.com/api-keys
<img width="3430" height="1894" alt="CleanShot 2025-10-28 at 09 39 29@2x" src="https://github.com/user-attachments/assets/590ba40f-8f24-4f1f-bfa6-adc6550ce661" />

Als Sprachmodell verwenden wir dann GPT 4.1:
<img width="3406" height="1858" alt="CleanShot 2025-10-28 at 09 41 16@2x" src="https://github.com/user-attachments/assets/d5a4e0d8-15e2-4f2c-8cb0-b8ffbc40aaf2" />

Im nächsten Schritt wählen wir dann den Structured Output Parser aus:
<img width="3446" height="1910" alt="CleanShot 2025-10-28 at 09 41 50@2x" src="https://github.com/user-attachments/assets/5a4675b7-be09-479a-b0be-8af80a8a68c0" />

Hier wollen wir jetzt unser eigenes Output JSON Schema definieren:
<img width="3422" height="1884" alt="CleanShot 2025-10-28 at 09 42 29@2x" src="https://github.com/user-attachments/assets/3bcecf85-0250-4272-9752-ad0828c22758" />

Die Frage ist jetzt, wie genau dieses Output Schema aussehen soll, dass wir dann verwenden wollen für die Generierung eines Podcasts. 
<img width="3378" height="1844" alt="CleanShot 2025-10-28 at 09 44 44@2x" src="https://github.com/user-attachments/assets/616aec45-4283-4a1b-ab5d-9ddb38051a18" />

Wir wollen für die Stimmen und die Generierung des Podcasts den Service von Eleven Labs verwenden: https://elevenlabs.io/de
<img width="2924" height="1480" alt="CleanShot 2025-10-28 at 09 45 46@2x" src="https://github.com/user-attachments/assets/b49fd521-4b41-436c-97ea-126b7430642a" />

Um die genaue Struktur für ein Schema zu finden, gehen wir auf die API-Referenz unter dem Bereich Entwickler:
<img width="2866" height="912" alt="CleanShot 2025-10-28 at 09 46 38@2x" src="https://github.com/user-attachments/assets/925a6c6d-7fd0-441f-a212-8e70f6c779fa" />

Dort gibt es alle Services von Eleven Labs, die man per API ansteuern kann unter anderem Text to Dialogue:
<img width="3414" height="1586" alt="CleanShot 2025-10-28 at 09 47 26@2x" src="https://github.com/user-attachments/assets/6e0fb144-eacb-4975-b406-0129e14dc4f9" />

Man kann jetzt das Beispiel für einen Dialog auf der rechten Seite kopieren in ChatGPT reingehen und sich dann ein Schema generieren lassen für N8N:
<img width="2866" height="1278" alt="CleanShot 2025-10-28 at 09 48 18@2x" src="https://github.com/user-attachments/assets/4a6cd159-c2c9-4d46-bd8e-e8f5552a19b3" />

Mit nachfolgendem Prompt erhält man dann ein Schema:
```
Erstelle ein JSON Schema basierend auf dem nachfolgenden Output, um diesen zu generieren von einem Input: [ { "text": "Knock knock", "voice_id": "JBFqnCBsd6RMkjVDRZzb" }, { "text": "Who is there?", "voice_id": "Aw4FAjKCGjjNkVhN1Xmq" } ]
```

Hier dann das Ergebnis in ChatGPT, welches wir dann in N8N reinkopieren (also nur die Schema Definition):

<img width="3382" height="1840" alt="CleanShot 2025-10-28 at 09 51 24@2x" src="https://github.com/user-attachments/assets/d6e06cbe-7ece-466c-a1d7-c9d727efd416" />

In dem Schema sieht man noch die Definition von Stimmen über Voice-IDs, diese können wir jetzt bei Eleven Labs uns raussuchen:
<img width="1228" height="888" alt="CleanShot 2025-10-28 at 09 52 06@2x" src="https://github.com/user-attachments/assets/d98679e5-ebbf-449e-80f0-ab78a2fb7e47" />

Auf der Webseite von ElevenLabs nach der Anmeldung kann man über Voices dann auf Best Voices for Eleven V3 zugreifen:
<img width="3440" height="1898" alt="CleanShot 2025-10-28 at 09 54 15@2x" src="https://github.com/user-attachments/assets/9b1d5bf1-3639-4e44-aaff-9d3dac7def8b" />

Hier finden wir dann zahlreiche Stimmen und können rechts immer auf die ID zugreifen:
<img width="3434" height="1902" alt="CleanShot 2025-10-28 at 09 54 39@2x" src="https://github.com/user-attachments/assets/6adb4857-ccce-4820-859a-8129e498705b" />

Mit diesen IDs können wir dann bisherigen Prompt für die Generierung des Dialogs erweitern:

In N8N ergänzen wir jetzt unseren Prompt einfach:
<img width="3410" height="1852" alt="CleanShot 2025-10-28 at 09 57 32@2x" src="https://github.com/user-attachments/assets/26dc0fe7-7324-45eb-b093-9cd59298357a" />

Prompt:

```
Deine Aufgabe ist es, einen Dialog zwischen zwei Podcast-Hosts zu erstellen.

Der erste Host ist eine freundliche und aufgeregte weibliche Person mit dem Namen Blondie. Ihre Voice-ID ist: exsUS4vynmxd379XN4yO

Der zweite Host ist pessimistisch und skeptisch, sein Name ist Mark und seine Voice-ID ist: 1SM7GgM6IMuvQlz2BwM3

Erstelle bis zu 10 Gesprächsrunden zwischen den beiden Hosts, basierend auf dem untenstehenden Artikel.
Vermeide technische Informationen wie Installationsschritte o. Ä. im Gespräch.
Stattdessen sollte das Gespräch eine allgemeine Diskussion auf höherer Ebene sein, die sich auf spannende oder kritische Aspekte des Inhalts konzentriert.


Artikelinhalt:
{{ $json.data.markdown }}

Output Struktur:
Gib das Gespräch als ein Array von Nachrichten zurück.
Jede Nachricht sollte eine **Voice-ID** und den **Nachrichtentext** enthalten.

**Beispiel:**


{
  "inputs": [
    {
      "text": "Klopf klopf",
      "voiceId": "JBFqnCBsd6RMkjVDRZzb"
    },
    {
      "text": "Wer ist da?",
      "voiceId": "Aw4FAjKCGjjNkVhN1Xmq"
    }
  ]
}
```


Dann starten wir das ganze jetzt:
<img width="3452" height="1418" alt="CleanShot 2025-10-28 at 10 01 09@2x" src="https://github.com/user-attachments/assets/6f5c1657-c437-410e-b88d-de30c9b28517" />

Wenn wir dann die LLM Chain für die Konversation öffnen, sehen wir hier das Ergebnis:
<img width="3390" height="1842" alt="CleanShot 2025-10-28 at 10 02 59@2x" src="https://github.com/user-attachments/assets/89550fb7-6d97-4089-ba5e-760c41f1c4c5" />

Wenn wir uns das im JSON Format anschauen, dann sieht es wie folgt aus:
<img width="3396" height="1854" alt="CleanShot 2025-10-28 at 10 03 51@2x" src="https://github.com/user-attachments/assets/2b0f9560-88fa-43a0-b4c2-ea1aaa1101d8" />

So, jetzt haben wir alle Daten für den Dialog und brauchen Eleven Labs Service jetzt, um mit diesen Texten und ausgewählten Stimmen den Dialog zu erstellen:

<img width="3436" height="1910" alt="CleanShot 2025-10-28 at 10 04 54@2x" src="https://github.com/user-attachments/assets/203d1106-4cd1-454e-97de-708b1aa3a240" />

Im obigen Screenshot sieht man, dass es bereits eine Eleven Labs Integration gibt, aber die Funktion aus einem Text ein Dialog zu erstellen fehlt hier. Daher müssen wir über einen HTTPRequest direkt die API ansprechen:

<img width="3418" height="1890" alt="CleanShot 2025-10-28 at 10 05 59@2x" src="https://github.com/user-attachments/assets/9067c370-1203-4fba-8bf2-a8011a94c63d" />

Wir wollen ja die Inhalte (die generierten Textdialoge) senden, also verwenden wir die Post Methode und wir benötigen dann die URL wohin es gesendet werden soll. Die bekommen wir von der API Webseite, wo wir schon mal waren: https://elevenlabs.io/docs/api-reference/text-to-dialogue/convert

<img width="2948" height="1344" alt="CleanShot 2025-10-28 at 10 07 58@2x" src="https://github.com/user-attachments/assets/ac8745f5-76f7-4592-90b9-3a745ecff35b" />

Jetzt müssen wir noch einen API Key hinterlegen (und vorher bei Eleven Labs generieren), um auf den Service zugreifen zu dürfen:

<img width="3386" height="1848" alt="CleanShot 2025-10-28 at 10 09 43@2x" src="https://github.com/user-attachments/assets/c882d50a-6a1d-4ae8-a30b-018ca22adeef" />

Im vorhergehenden Dialog haben wir schon gesehen, dass die API mit dem Namen xi-api-key angesprochen wird. Den API Key bekommen wir auf der Eleven Labs Webseite nach der Anmeldung über den Eintrag Developers in der linken Navigationsleiste:

<img width="3450" height="1906" alt="CleanShot 2025-10-28 at 10 12 05@2x" src="https://github.com/user-attachments/assets/af06b267-6416-4958-9a70-9891d0a7d210" />

Hier kann man dann einen API Key erstellen und diesen "limitieren" für die Nutzung oder als unlimitierten Key freischalten:
<img width="3450" height="1910" alt="CleanShot 2025-10-28 at 10 13 10@2x" src="https://github.com/user-attachments/assets/89bc2818-87fd-468a-b46b-6f1a38ec78ae" />

Wir erstellen hier mal einen unlimitierten Key für die Nutzung für unseren Podcast Generator und fügen diesen in N8N ein:
<img width="3388" height="1864" alt="CleanShot 2025-10-28 at 10 14 51@2x" src="https://github.com/user-attachments/assets/59c9e9f2-e4a6-45a9-8418-1a770758ddcd" />

So jetzt müssen wir noch definieren, was wir versenden wollen:
<img width="3382" height="1854" alt="CleanShot 2025-10-28 at 10 18 45@2x" src="https://github.com/user-attachments/assets/e1302fae-d602-47a9-8138-7c6418db096b" />

Das ist ja das JSON Output Format aus dem vorherigen Node, dass wir hier definieren, d.h. Send Body, welchen Input und wie soll die Variable für diesen Input heißen. Welchen Input ist einfach, das ist der Output aus dem vorhergehenden Node. Den Namen der Variablen für Eleven Labs zur Verarbeitung bekommen wir von der ElevenLabs Webseite: 
<img width="2928" height="1310" alt="CleanShot 2025-10-28 at 10 21 28@2x" src="https://github.com/user-attachments/assets/418caa9b-3632-44ad-89d5-15cc56e7375e" />

Also müssen wir hier den Variablen Namen "inputs" eintragen

So das wars jetzt:
<img width="3412" height="1868" alt="CleanShot 2025-10-28 at 10 22 21@2x" src="https://github.com/user-attachments/assets/047e3ed5-425c-4b67-b2c9-c42c3297c546" />

Wir können den Node ausführen und den Workflow testen:

<img width="3404" height="1866" alt="CleanShot 2025-10-28 at 10 23 49@2x" src="https://github.com/user-attachments/assets/fa396ecd-7128-407d-8d12-33318f72fa44" />

Die Generierung dauert in der Regel 2-3 Minuten

<img width="3396" height="1862" alt="CleanShot 2025-10-28 at 10 24 31@2x" src="https://github.com/user-attachments/assets/99105b17-675e-4370-b539-081f0482cff2" />



















































