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
















