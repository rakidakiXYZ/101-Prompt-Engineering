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






























