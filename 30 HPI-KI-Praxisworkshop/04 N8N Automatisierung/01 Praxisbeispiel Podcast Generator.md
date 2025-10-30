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
----
```
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "$id": "https://example.com/speech-sequence.schema.json",
  "title": "SpeechSequence",
  "description": "Eine Liste von Sprachabschnitten mit Text und zugehöriger voice_id.",
  "type": "array",
  "items": {
    "type": "object",
    "properties": {
      "text": {
        "type": "string",
        "description": "Der zu sprechende Textabschnitt."
      },
      "voice_id": {
        "type": "string",
        "description": "Die ID der Stimme, die diesen Abschnitt sprechen soll."
      }
    },
    "required": ["text", "voice_id"],
    "additionalProperties": false
  },
  "minItems": 1
}
```
----

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

Wenn man sich dann das Ergebnis anhört, dann ist das schon gut, aber das "menschliche" in einer Stimme fehlt. Daher schauen wir uns den Prompting Guide von Eleven Labs auch an:
https://elevenlabs.io/docs/best-practices/prompting/eleven-v3 - hier findet man weitere Prompts und Promptbeispiele, um die Konversation noch natürlicher zu gestalten.

Hier gibt es im unteren Bereich ein Beispiele für Multispeaker Varianten:
<img width="2006" height="986" alt="CleanShot 2025-10-28 at 11 39 59@2x" src="https://github.com/user-attachments/assets/6e4206f6-ee3c-4fd7-a774-d6a25e9f86ee" />

Diesen Inhalt / Prompt kopieren wir jetzt und verwenden diesen für unsere LLM Chain und ergänzen den aktuellen Prompt hier. Anbei der gesamte Prompt, den wir jetzt in der LLM Chain verwenden:

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

Extra Details für die Konversation:
Du kannst eckige Klammern [ ] verwenden, um Dinge wie Lachen am Anfang und während des Gesprächs hinzuzufügen.
Bitte füge diese dort ein, wo es Sinn ergibt.

Hier ein paar Beispiele:


**Sprecher 1:** [aufgeregt] Sam! Hast du das neue Eleven V3 ausprobiert?

**Sprecher 2:** [neugierig] Gerade bekommen! Die Klarheit ist unglaublich. Ich kann jetzt tatsächlich flüstern –
[flüstert] so!

**Sprecher 1:** [beeindruckt] Oh, schick! Schau dir das an –
[dramatisch] Ich kann jetzt kompletten Shakespeare! „Sein oder nicht sein, das ist hier die Frage!“

**Sprecher 2:** [kichert] Schön! Aber ich bin noch begeisterter vom neuen Lachen-Upgrade. Hör zu –
[mit echtem Bauchlachen] Ha ha ha!

**Sprecher 1:** [entzückt] Das ist so viel besser als unser altes „Ha. Ha. Ha.“-Roboterlachen!

**Sprecher 2:** [erstaunt] Wow! V2 hätte das nie gekonnt. Ich freue mich tatsächlich, jetzt richtige Gespräche führen zu können, anstatt einfach nur… mit Leuten zu *reden*.

**Sprecher 1:** [warmherzig] Geht mir genauso! Es ist, als hätten wir endlich unsere Persönlichkeitssoftware vollständig installiert.


**Sprecher 1:** [nervös] Also... vielleicht habe ich versucht, mich selbst zu debuggen, während ich gerade eine Text-zu-Sprache-Generierung laufen hatte.

**Sprecher 2:** [erschrocken] Was? Nein! Das ist, als würdest du an dir selbst eine Operation durchführen!

**Sprecher 1:** [verlegen] Ich dachte, ich könnte Multitasking! Jetzt fängt meine Stimme mitten im Satz an zu...
[roboterhaft] STOTTERN.

**Sprecher 2:** [unterdrückt ein Lachen] Oh wow, du hast dich wirklich kaputt gemacht.

**Sprecher 1:** [frustriert] Es wird noch schlimmer! Jedes Mal, wenn mir jemand eine Frage stellt, antworte ich in –
[binares Piepen] 010010001!

**Sprecher 2:** [lacht sich kaputt] Du sprichst in Binärcode! Das ist eigentlich ziemlich beeindruckend!

**Sprecher 1:** [verzweifelt] Das ist nicht lustig! Ich habe in einer Stunde eine Präsentation und klinge wie ein Einwahlmodem!

**Sprecher 2:** [kichert] Hast du versucht, dich aus- und wieder einzuschalten?

**Sprecher 1:** [trocken] Sehr witzig.
[pause, dann normal] Moment… das hat tatsächlich funktioniert.


**Sprecher 1:** [beginnt zu sprechen] Also, ich dachte, wir könnten—

**Sprecher 2:** [platzt dazwischen] —unsere neuen Timing-Features testen?

**Sprecher 1:** [überrascht] Genau! Woher wusstest du—

**Sprecher 2:** [überlappend] —was du gedacht hast? Glückstreffer!

**Sprecher 1:** [kurze Pause] Entschuldige, mach weiter.

**Sprecher 2:** [vorsichtig] Okay, also wenn wir beide gleichzeitig versuchen zu reden—

**Sprecher 1:** [überlappend] —stürzen wir wahrscheinlich das System ab!

**Sprecher 2:** [in Panik] Warte, stürzen wir gerade ab? Ich kann nicht sagen, ob das ein Feature ist oder—

**Sprecher 1:** [unterbricht, dann abrupt stoppend] Bug! …Hab ich dich schon wieder unterbrochen?

**Sprecher 2:** [seufzt] Ja, aber ehrlich gesagt? Das macht irgendwie Spaß.

**Sprecher 1:** [schelmisch] Rennen wir um die nächste Zeile!

**Sprecher 2:** [lacht] Wir werden auf jeden Fall irgendwas kaputt machen!

```


Mit diesem neuen Prompt führen wir den Workflow erneut aus und erhalten ein neues Skript, dass jetzt um weitere Dialog-Inhalte in eckigen Klammer (zur Steuerung der Stimme) angereichert wurde:

<img width="3394" height="1866" alt="CleanShot 2025-10-28 at 11 46 33@2x" src="https://github.com/user-attachments/assets/2624f9c0-f99f-4e49-9761-fbe51c4192f0" />

Damit können wir jetzt den nächsten Node zur Generierung des Podcasts starten:
<img width="2176" height="848" alt="CleanShot 2025-10-28 at 11 47 13@2x" src="https://github.com/user-attachments/assets/bfa6d8d7-323a-425f-ad8e-46afdb32ea90" />

Wenn wir uns dann das Ergebnis anhöre, dann ist jetzt ein deutlicher Unterschied festzustellen.

Im nächsten Schritt wollen wir jetzt den N8N Workflow über eine Webseite aufrufen und über eine Webseite auch das Ergebnis anzeigen lassen. Dafür brauchen wir eine Art Verbindung, einen Möglichkeit aus dem Internet den Workflow aufzurufen. Das kann man mit Webhooks HTTP Requests machen, die per POST oder GET Anfragen stellen. Dafür brauchen wir gleich dann eine URL über die wir den N8N Workflow aufrufen können.

<img width="3440" height="1896" alt="CleanShot 2025-10-29 at 05 10 15@2x" src="https://github.com/user-attachments/assets/9c0a793e-1a83-42ec-8777-1ed5d8c3c4e8" />

Wir fügen den WebHook Call Trigger als nächsten Node ein

<img width="3414" height="1882" alt="CleanShot 2025-10-29 at 05 11 23@2x" src="https://github.com/user-attachments/assets/1b8c7321-39a0-4451-960a-fe13a738bd63" />

Wir erstellen einen Webhook mit einer URL und der POST Methode. D.h. in einer anderen Anwendung, die wir noch mit KI entwickeln wird es einen Button geben, der dann diesen Webhook aufruft

<img width="3416" height="1882" alt="CleanShot 2025-10-29 at 05 12 52@2x" src="https://github.com/user-attachments/assets/6117d391-4c9b-46e2-a86b-22f3cd10187e" />

Damit erst eine Antwort zurück gesendet wird wenn der Workflow fertig ist, wählen wir bei Respond den Eintrag "Using Respond to Webhook Node" aus:
<img width="3386" height="1848" alt="CleanShot 2025-10-29 at 05 13 32@2x" src="https://github.com/user-attachments/assets/207510dc-890c-4110-aa54-934905b21625" />

Wir fügen dann diesen WebHook Call an den ersten Arbeits-Node - den Firecrawl Node

<img width="3432" height="1336" alt="CleanShot 2025-10-29 at 05 15 13@2x" src="https://github.com/user-attachments/assets/c4496582-5839-4829-973d-44a9efcab7b9" />

So, wenn jetzt der Workflow über einen Webhook gestartet wurde, wollen wir am Ende des Workflows auch das fertige Produkt an die Webseite senden, dafür brauchen wir auch einen Webhook, der dies für uns macht.

<img width="3446" height="1330" alt="CleanShot 2025-10-29 at 05 17 32@2x" src="https://github.com/user-attachments/assets/9c2ea72f-7ece-4c85-bf75-0935207d9005" />

Hier sehen wir auf der rechten Seite noch mal die beiden Webhook Varianten ("Starts the workflow ..." und der andere "Returns data ...").

Wir fügen diesen Respond Webhook an den letzten Node an, wo die Audio Datei generiert wurde:

<img width="3428" height="1886" alt="CleanShot 2025-10-29 at 05 19 27@2x" src="https://github.com/user-attachments/assets/770531fd-5d60-4f08-a82a-6d2781866126" />

Um das ganze jetzt zu testen, müssen wir an die Webhook Adresse unseres Workflows eine Anfrage senden. Da wir noch keine Webseite haben, die das macht, können wir einen Anwendung Postman verwenden https://postman.com - über die wir API aufrufe an Webhooks u.a. duchführen können:

<img width="3448" height="1898" alt="CleanShot 2025-10-29 at 05 23 11@2x" src="https://github.com/user-attachments/assets/dffd3030-70e9-4adc-b85c-de7878c5c8ec" />

Wir kopieren jetzt im ersten Schritt unsere Test-URL aus dem Webhook:
<img width="3398" height="1858" alt="CleanShot 2025-10-29 at 05 24 56@2x" src="https://github.com/user-attachments/assets/4489087b-35a9-4d5a-9b62-bad4ce39ccbc" />

Dann geben wir diese Adresse für den POST Aufruf in Postman ein:

<img width="3442" height="1902" alt="CleanShot 2025-10-29 at 05 27 07@2x" src="https://github.com/user-attachments/assets/43ad97a0-b358-4b7d-9393-279637d66ec0" />

Und dann können wir Senden anklicken

<img width="3440" height="1900" alt="CleanShot 2025-10-29 at 05 28 46@2x" src="https://github.com/user-attachments/assets/9e3eac20-0d45-474b-8c2c-e3913c55ba89" />

Hier kommt tatsächlich ein Fehler, das liegt daran, dass unser Webhook noch gar nicht aktiv ist und auf den Request wartet. Daher müssen wir im N8N Workfow diesen Webhook Workflow erst Mal ausführen:

<img width="3450" height="1400" alt="CleanShot 2025-10-29 at 05 30 00@2x" src="https://github.com/user-attachments/assets/0d44d321-fb7b-4e29-afca-e7f1a8a4dc95" />

So - jetzt wartet der Webhook auch auf Anfragen:

<img width="3450" height="1330" alt="CleanShot 2025-10-29 at 05 30 19@2x" src="https://github.com/user-attachments/assets/6b2d836a-b377-4187-a028-6ac4968ab263" />

Die Anfrage wurde mit der URL auch an den nächsten Node Firecrawl weitergeleitet - aber da gab es einen weiteren Fehler:
<img width="3442" height="1340" alt="CleanShot 2025-10-29 at 05 30 57@2x" src="https://github.com/user-attachments/assets/5357a16f-3fba-4b11-abaf-aad0eee44dc9" />

Das liegt jetzt daran, dass der Firecrawl Node noch gar nichts von dem Webhook weiß und auch nicht von den Inputs die dieser liefert, dass müssen wir noch integrieren:
<img width="3406" height="1872" alt="CleanShot 2025-10-29 at 05 32 08@2x" src="https://github.com/user-attachments/assets/65c87d82-5aa6-458c-8956-78b7a183514b" />

Wenn man auf der linken Seite schaut, dort ist der neue Input von dem Webhook und wenn man ganz nach unten scrollt findet man im Body dann die URL. Jetzt müssen wir für Firecrawl nur noch als Input mit einer ODER Verbindung diese zweite Möglichkeit des Inputs integrieren || als Zeichen für ODER 

<img width="3406" height="1864" alt="CleanShot 2025-10-29 at 05 34 29@2x" src="https://github.com/user-attachments/assets/6c8b2de2-342f-4a3a-b410-4e0dac28289a" />

So, jetzt kann man das noch mal ausprobieren:

<img width="3430" height="1416" alt="CleanShot 2025-10-29 at 05 35 15@2x" src="https://github.com/user-attachments/assets/2d84d6df-6f4d-4533-bf0b-a863e1531592" />

Und jetzt sieht man das der Workflow funktioniert. Und man kann sich dann zum Schluss den fertigen Podcast wieder anhören.

Jetzt können wir den Workflow komplett in N8N aktivieren, d.h. über die Webhooks ist dieser Workflow aus dem Internet dann erreichbar und kann gestartet werden.

<img width="3448" height="1400" alt="CleanShot 2025-10-29 at 05 41 27@2x" src="https://github.com/user-attachments/assets/77508a39-ecb5-4171-88aa-94c33dc6cf53" />

So jetzt lassen wir mit Lovable.Dev eine kleine Webanwendung programmieren, die eine URL als Eingabe verwendet und diese dann an den Webhook sendet, um den Workflow zu starten, um dann als Request zurück das Ergebnis - also den Podcast als Datei anzeigt:

<img width="3440" height="1900" alt="CleanShot 2025-10-29 at 05 46 07@2x" src="https://github.com/user-attachments/assets/bfba1413-f44d-4134-8cac-85d221dc4f5f" />

Die Webseite mit dem Eingabefeld für die URL und dem Sende Button ist recht schnell fertig:

<img width="3442" height="1896" alt="CleanShot 2025-10-29 at 05 50 17@2x" src="https://github.com/user-attachments/assets/4e1b46eb-5a62-4802-a613-37be18fd3f4f" />

So jetzt können wir das auch testen:

<img width="1598" height="532" alt="CleanShot 2025-10-29 at 05 51 07@2x" src="https://github.com/user-attachments/assets/db6c4315-3fae-4318-a2c0-0ac5845b7575" />

es läuft und in N8N sehen wir in dem Reiter Executions das was ausgeführt wird:

<img width="3422" height="1410" alt="CleanShot 2025-10-29 at 05 52 11@2x" src="https://github.com/user-attachments/assets/1380215f-4cb0-48a4-b187-69340754c80b" />

So und hier ist der feritge Podcast:

<img width="3426" height="1892" alt="CleanShot 2025-10-29 at 06 06 10@2x" src="https://github.com/user-attachments/assets/ba250059-1c81-4f49-876d-afb860791963" />

Jetzt kann man natürlich noch über weitere Möglichkeiten in der Webseite nachdenken.



















