# Schritt 1 Supabase Datenbank einrichten

Link: https://supabase.com/
<img width="3352" height="1890" alt="CleanShot 2025-10-30 at 03 43 09@2x" src="https://github.com/user-attachments/assets/d2bdcd8c-7dc6-4533-9260-448547618862" />

SignUp Prozess durchführen

Danach muss man eine Organisation einrichten in Supabase

<img width="3444" height="1450" alt="CleanShot 2025-10-30 at 03 45 59@2x" src="https://github.com/user-attachments/assets/75a11086-dfb7-4127-950f-39b1e74d68e1" />

Dann muss man für die Datenbank ein Passwort und den Standort definieren:

<img width="3422" height="1450" alt="CleanShot 2025-10-30 at 03 46 33@2x" src="https://github.com/user-attachments/assets/f8727b8e-3852-4915-8540-659c7c46c864" />

<img width="3440" height="1910" alt="CleanShot 2025-10-30 at 03 47 05@2x" src="https://github.com/user-attachments/assets/a5cf9860-8324-425f-8f13-5f94067d8659" />

Wir starten dann in N8N mit einem AI Agenten:

<img width="3442" height="1910" alt="CleanShot 2025-10-30 at 03 48 36@2x" src="https://github.com/user-attachments/assets/75f7f759-3cd7-44dd-b12f-7053e80bd51c" />

Man landet dann in der Agent Definition in N8N, die schließen wir erst mal wieder:

<img width="3404" height="1868" alt="CleanShot 2025-10-30 at 03 51 11@2x" src="https://github.com/user-attachments/assets/0c3feac4-e7ff-40bb-9445-5261321dbe81" />

Es erscheint der Workflow:
<img width="3440" height="1908" alt="CleanShot 2025-10-30 at 03 51 47@2x" src="https://github.com/user-attachments/assets/520f6505-0777-4d7b-b7c6-ca4652c82105" />

Hier wählen wir jetzt das Sprachmodell aus:
<img width="3440" height="1908" alt="CleanShot 2025-10-30 at 03 52 22@2x" src="https://github.com/user-attachments/assets/675e0978-8371-4bda-80f3-49aef7ad3022" />

Dafür brauchen wir einen API Key, damit wir das überhaupt machen können:
<img width="3404" height="1876" alt="CleanShot 2025-10-30 at 03 52 49@2x" src="https://github.com/user-attachments/assets/8e4ce429-e8a5-4b33-8705-d13b8107151e" />

API Keys bekommen wir auf dern platform.openai.com Webseite:
<img width="3422" height="1510" alt="CleanShot 2025-10-30 at 03 53 18@2x" src="https://github.com/user-attachments/assets/eac4ecde-c772-4bac-8fb2-b5b81497f2ad" />

Wir wählen dann das Sprachmodell für den Agenten aus und können das ganze dann auch schon mal testen:
<img width="3440" height="1900" alt="CleanShot 2025-10-30 at 03 54 53@2x" src="https://github.com/user-attachments/assets/c65bc7b8-6913-4488-aee1-1e91cf47ed4e" />

Jetzt wollen wir unsere Datenbank / Memory unserem Agenten hinzufügen:
<img width="3448" height="1904" alt="CleanShot 2025-10-30 at 03 57 35@2x" src="https://github.com/user-attachments/assets/45b2c155-9f86-4c81-9401-151547afc7db" />

Hier wählen wir Postgres aus - um dann unsere Supabase Datenbank zu verknüpfen

<img width="3394" height="1878" alt="CleanShot 2025-10-30 at 03 58 53@2x" src="https://github.com/user-attachments/assets/4020f25e-c924-4e05-9a17-e625bb4e61af" />

Dafür brauchen wir die Credentials - also die Zugriffsdaten von Supabase:
<img width="3408" height="1862" alt="CleanShot 2025-10-30 at 03 59 26@2x" src="https://github.com/user-attachments/assets/88d1d0c5-545f-4ad3-abc5-3c344b84469a" />

Dafür gehen wir wieder auf Supabase und klicken auf Connect
<img width="3442" height="1904" alt="CleanShot 2025-10-30 at 03 59 52@2x" src="https://github.com/user-attachments/assets/74f8f9a1-8af8-4f2c-ade2-40d24413fbf1" />

Wir müssen dann umstellen von URI auf Postgres SQL und auf Transaction als Methode, da wir einen RAG Chatbot bauen
<img width="2038" height="996" alt="CleanShot 2025-10-30 at 04 09 44@2x" src="https://github.com/user-attachments/assets/154b806a-c954-4740-aeea-0e9f7cbcb09e" />


Hier brauchen wir erst Mal den Host dann brauchen wir den Port und den Usernamen für die Datenbank:
<img width="2026" height="986" alt="CleanShot 2025-10-30 at 04 10 43@2x" src="https://github.com/user-attachments/assets/37d300ac-ab8d-4879-b061-644bdb71280b" />

Das tragen wir alles in N8N ein:
<img width="2386" height="1478" alt="CleanShot 2025-10-30 at 04 11 03@2x" src="https://github.com/user-attachments/assets/fb5dc9c3-f7a3-4111-a063-22bc341335fe" />

Mit dem Speichern wird die Verbindung getestet und hier sollte dann alles grün sein. wir gehen dann hier raus

<img width="3378" height="1842" alt="CleanShot 2025-10-30 at 04 11 58@2x" src="https://github.com/user-attachments/assets/6972ebda-af2f-4fdb-b6e8-c929ab69cfc7" />

Den Node für die Postgres SQL Datenbank lassen wir so und gehen wieder auf den Workflow und testen diesen:
<img width="3378" height="1842" alt="CleanShot 2025-10-30 at 04 11 58@2x" src="https://github.com/user-attachments/assets/e43ee72c-a140-4336-90dc-f0b2a5e2dd76" />

<img width="3450" height="1914" alt="CleanShot 2025-10-30 at 04 13 04@2x" src="https://github.com/user-attachments/assets/26488b85-e465-4ffe-baa7-214859f18724" />

Man sieht jetzt im Workflow, dass hier auch in die Datenbank was geschrieben wurde. Wenn wir ein wenig gechattet haben, kann man sich das auch anzeigen lassen in der Tabelle in Supabase:

<img width="3450" height="1916" alt="CleanShot 2025-10-30 at 04 15 36@2x" src="https://github.com/user-attachments/assets/5d13ed80-61f3-4edb-91a7-fa162578aab5" />
Dazu gehen wir auf den Tabel Editor und dort auf die Table für die n8n-chat-history

In dem Node für die Postgres SQL Datenbank im N8N Workflow kann man dann noch die Chat-History einstellen, die ist per Defaul auf 5 und kann auf 20 hochgesetzt werden.

Wenn wir den Chat Trigger Node öffnen, sehen wir hier das für jeden Chat eine ID vergeben wird, so dass man dann später Chatverläufe über die ID unterscheiden kann

<img width="3384" height="1850" alt="CleanShot 2025-10-30 at 04 18 25@2x" src="https://github.com/user-attachments/assets/2774b753-1106-46d4-a3e6-70c5b43a3f9f" />

Im nächsten Schritt wollen wir noch Dokumente hochladen, die wir dann als Wissen für einen Chatbot nutzen wollen. Dafür müssen wir unsere Datenbank als Vektorendatenbank nutzen und hier die Tabelle in der Datenbank für diese Dokumente anpassen.

Link: https://supabase.com/docs/guides/ai/langchain?database-method=sql

<img width="1966" height="1500" alt="CleanShot 2025-10-30 at 04 36 32@2x" src="https://github.com/user-attachments/assets/4f0e5a02-b2e9-4806-a454-f27c3766b0fb" />

Hier finden wir den "Code" um unsere SQL Datenbank in Supabase Vektor tauglich zu machen. Wir kopieren den ganzen Code und gehen in Supabase zurück:
<img width="3440" height="1816" alt="CleanShot 2025-10-30 at 04 38 59@2x" src="https://github.com/user-attachments/assets/198749f3-f979-491c-988a-2068349e813d" />

Dort wählen wir den SQL Editor aus und können den Code direkt einfügen 
ACHTUNG: extensions.vector(1536) müssen wir ersetzen durch vector(1536) - als ohne extensions.

Die Rückmeldung ist dann:
<img width="3442" height="1826" alt="CleanShot 2025-10-30 at 04 44 47@2x" src="https://github.com/user-attachments/assets/bbee19ea-f444-4ec2-8e82-79b6d4f155ca" />

Wenn wir dann auf den Table Editor gehen, sehen wir wieder unsere Chat-History aber auch eine neue Table Documents

<img width="3442" height="1904" alt="CleanShot 2025-10-30 at 04 45 37@2x" src="https://github.com/user-attachments/assets/545513b7-7597-43ab-a802-522dc120178e" />

Diese Tabelle ist wie folgt aufgebaut:
<img width="3440" height="1910" alt="CleanShot 2025-10-30 at 04 46 33@2x" src="https://github.com/user-attachments/assets/01d66f01-f7b6-4905-8040-255df88379b4" />
id, content, metadata, vector

So jetzt kehren wir wieder zur n8n zurück und wollen hier Dokumente aus deinem Google Drive Folder hochladen in die Vektordatenbank:
<img width="3434" height="1906" alt="CleanShot 2025-10-30 at 04 49 45@2x" src="https://github.com/user-attachments/assets/dcd56d60-958b-416f-82c1-a1fdcda385dd" />

Dazu wählen wir den passenden Trigger aus: On changes involving a specific folder

<img width="3436" height="1898" alt="CleanShot 2025-10-30 at 04 54 29@2x" src="https://github.com/user-attachments/assets/8d069536-0d24-47f1-a2fa-7149ad7438b8" />

Damit das ganze funktioniert, brauchen wir aber eine Authorisierung für Google, die wir jetzt noch mal machen - man mus das nur einmal machen für die jeweiligen Services in Google die man nutzen möchte.

# Google Services Authorisierung für N8N
Im ersten Schritt müssen wir auf die URL https://console.cloud.google.com/ gehen (vorausgesetzt wir haben ein Google Account)

<img width="3440" height="1906" alt="CleanShot 2025-10-30 at 05 07 37@2x" src="https://github.com/user-attachments/assets/2c99b9f9-54ad-4715-8e09-13cfedd33d45" />

Hier legen wir erst Mal ein neues Projekt an:

<img width="1376" height="944" alt="CleanShot 2025-10-30 at 05 08 36@2x" src="https://github.com/user-attachments/assets/9e6dff46-2029-4821-8360-3aae6d3e0d98" />

Sobald das Projekt erstellt wurde wählen wir es aus und können wir dieses Projekt dann die APIs von Google für die diversen Services aktivieren. Dazu klicken wir auf das Navigationsmenü links oben und wählen API und Dienste aus:

<img width="3446" height="1916" alt="CleanShot 2025-10-30 at 05 12 08@2x" src="https://github.com/user-attachments/assets/b80a12c3-17d2-4d92-ab44-96f700cb828b" />

Hier klicken wir auf APIs und Dienste aktivieren:
<img width="3424" height="1750" alt="CleanShot 2025-10-30 at 05 12 37@2x" src="https://github.com/user-attachments/assets/5cc22719-95e1-4fd2-aae5-5c9882746655" />

Wir wählen hier den jeweiligen Dienst aus - hier z.B. Google Drive
<img width="3446" height="1908" alt="CleanShot 2025-10-30 at 05 13 27@2x" src="https://github.com/user-attachments/assets/67393e79-f59a-46b1-92df-cd74efb0cdd6" />

Und dann können wir den Dienst aktivieren:
<img width="2498" height="1310" alt="CleanShot 2025-10-30 at 05 13 56@2x" src="https://github.com/user-attachments/assets/a3149b4d-e190-4f7a-9aae-9c9c3f026c7b" />

Unter Branding fügen wir noch die TOP Level Domain von N8N ein: n8n.cloud (bzw. die Domain auf die die N8N Instanz läuft)

So kann man jetzt Schritt für Schritt die Dienste (Mail, Kalender, Sheets, Slides) aktivieren. Damit da jetzt aber auch drauf zugreifen kann, brauchen wir eine Authorisierung mit OAUTH - dazu klicken wir links auf OAuth Zustimmung:

<img width="3446" height="1890" alt="CleanShot 2025-10-30 at 05 16 31@2x" src="https://github.com/user-attachments/assets/1bc8e68d-62ca-4c0f-bfd2-99f940e71a58" />

In dem Screen klicken wir dann auf erste Schritte:

Wir starten dann mit dem Namen für die Anwendung die den Dienst nutzen soll und die Support E-mail Adresse:
<img width="1930" height="1360" alt="CleanShot 2025-10-30 at 05 17 46@2x" src="https://github.com/user-attachments/assets/bf323025-9f57-4167-9963-fde93cdeee82" />

Dann wählen wir die Nutzer aus (extern):
<img width="1784" height="1334" alt="CleanShot 2025-10-30 at 05 18 47@2x" src="https://github.com/user-attachments/assets/3b5d88ab-cb47-4ef6-a9a7-d9b541a9f0fc" />

Dann noch eine Kontakt E-Mail Adresse eingeben:
<img width="1768" height="1216" alt="CleanShot 2025-10-30 at 05 19 38@2x" src="https://github.com/user-attachments/assets/baa9ea13-3613-490c-b00a-d3ed4a5d9b2e" />

Bestätigen und dann ist man hier fertig:

<img width="3450" height="970" alt="CleanShot 2025-10-30 at 05 20 15@2x" src="https://github.com/user-attachments/assets/244409f8-3e54-4bf3-a11b-97e692db98e5" />

Hier erstellen wir dann den OAuth Client:
<img width="3332" height="1912" alt="CleanShot 2025-10-30 at 05 22 18@2x" src="https://github.com/user-attachments/assets/e548f6e5-0d41-4f6b-9b36-cbdfb3167783" />

Webanwendung auswählen und einen Name der Anwendung festlegen und dann auf Autorisierte Weiterleitungs-URL klicken - das ist die N8N URL, die wir aus dem Node für den Google Service bekommen, den wir nutzen wollen und der gerade nach den Credentials von Google fragt:

<img width="2396" height="1488" alt="CleanShot 2025-10-30 at 05 24 18@2x" src="https://github.com/user-attachments/assets/60065e10-bce0-4b4f-9f71-78de53cf9409" />

Wenn man dann mit der Erstellung des OAuth Client fertig ist erscheint ein Dialog mit allen wichtigen Daten: Client-ID, Client-Secret, ... die wir in N8N brauchen. Diese Daten sind sicher zu speichern.
<img width="998" height="434" alt="CleanShot 2025-10-30 at 05 29 13@2x" src="https://github.com/user-attachments/assets/6447436b-7ea4-4986-a4dc-1b959f217a79" />


Client ID und Client Schlüssel fügt man dann in N8N ein:

<img width="2362" height="1484" alt="CleanShot 2025-10-30 at 05 30 35@2x" src="https://github.com/user-attachments/assets/3be4c9dd-dadc-4415-b333-a51c73e77352" />

Und dann hat man den Dienst verbunden

# Google Drive Folder Node

So zurück zu unserem Google Drive Node, hier verbinden wir jetzt den richtigen Ordner auf unserem Google Drive und die Aktion Watch for File Created aus:
<img width="3352" height="1812" alt="CleanShot 2025-10-30 at 05 32 33@2x" src="https://github.com/user-attachments/assets/eb917cae-3afc-428f-96f7-75b6b5553d3e" />

Wenn eine neue Datei eingestellt wurde, dann wollen wir die im nächsten Schritt von Google Drive herunterladen:

<img width="3438" height="1916" alt="CleanShot 2025-10-30 at 05 34 17@2x" src="https://github.com/user-attachments/assets/557f38a5-b5e8-486d-81af-9bf0d73e188d" />

Dafür brauchen wir den Google Drive Download Node

Hier definieren wir die Datei, die im Drive liegen wird über {{ $json.id }}, das ist die ID der hochgeladen Datei in Google Drive - jede Datei bekommt eine ID.

<img width="3434" height="1914" alt="CleanShot 2025-10-30 at 05 38 09@2x" src="https://github.com/user-attachments/assets/17935547-77d4-47f5-bfc6-73d0904ecd98" />

Als nächstes wollen wir die Datei in die Vektordatebank laden - dazu wählen wir die Supabase Vektordatenbank aus:

<img width="3446" height="1906" alt="CleanShot 2025-10-30 at 05 39 08@2x" src="https://github.com/user-attachments/assets/339ab680-f9d2-4f7d-a775-205ed2b08e09" />

Und hier dann die Action Add document to VectorStore

<img width="3444" height="1886" alt="CleanShot 2025-10-30 at 05 41 00@2x" src="https://github.com/user-attachments/assets/b8b4b00f-aa42-4b0e-a47c-55bbf02cc322" />

Den neuen Node für die Vektor-Datenbank müssen wir jetzt konfigurieren

<img width="3374" height="1842" alt="CleanShot 2025-10-30 at 05 41 37@2x" src="https://github.com/user-attachments/assets/9ddb6dda-b2da-4a88-9a29-25f0c54caa4d" />

Im ersten Schritt brauchen wir wieder Credentials - jetzt für die Supabase Vektordatenbank - dazu gehen wir wieder auf Supabase:

<img width="3442" height="1894" alt="CleanShot 2025-10-30 at 05 42 15@2x" src="https://github.com/user-attachments/assets/79015858-1dc1-4e8f-9bd8-6b25ec0d08d8" />

Hier auf Project Settings und dann auf Data API:
<img width="3434" height="1912" alt="CleanShot 2025-10-30 at 05 43 15@2x" src="https://github.com/user-attachments/assets/b9e77307-593b-4599-874b-fb26477c77c7" />

Hier finden wir die URL für N8N:
<img width="3398" height="1826" alt="CleanShot 2025-10-30 at 05 43 48@2x" src="https://github.com/user-attachments/assets/aec2b3de-0297-42e9-9781-1e1a442255ba" />

Dann brauchen wir noch die Service Secret Role, dazu gehen wir in Supabase auf API Keys
<img width="3432" height="1898" alt="CleanShot 2025-10-30 at 05 44 52@2x" src="https://github.com/user-attachments/assets/798c0b51-3369-487c-a727-baf3387a95d4" />

Hier können wir das service role secret kopieren und in N8N einfügen:

<img width="2386" height="1488" alt="CleanShot 2025-10-30 at 05 46 01@2x" src="https://github.com/user-attachments/assets/0a84ed05-29f4-4fad-b63e-0738d9b962f1" />

So jetzt muss man noch definieren, wo die Dokumente in die Vektordatenbank hochgeladen werden und das ist die zuvor angelegte Table "documents":

<img width="3396" height="1872" alt="CleanShot 2025-10-30 at 05 46 52@2x" src="https://github.com/user-attachments/assets/decd734e-313e-40c7-a5e1-829cce72ef5d" />

Damit jetzt beim Hochladen eines Dokuments aber überhaupt Vektorisierung durchgeführt wird brauchen wir ein LLM dafür - hier nehmen wir von OpenAI ein Embedding Modell

<img width="3424" height="1908" alt="CleanShot 2025-10-30 at 05 48 50@2x" src="https://github.com/user-attachments/assets/4420f7fd-95cc-41bb-9954-a8f7cb282b63" />

Dann konfigurieren wir das Embedding noch - welches Modell - hier large und die Vektorengröße unserer Datenbank geben wir noch an 1536

<img width="3342" height="1824" alt="CleanShot 2025-10-30 at 05 50 42@2x" src="https://github.com/user-attachments/assets/11b6c806-52df-4543-b49b-7947258e76ed" />

So jetzt brauchen wir noch den Data Loader, der die von Google Drive heruntergeladene Datei in den Vektorstore hochlädt:
<img width="3422" height="1888" alt="CleanShot 2025-10-30 at 05 52 21@2x" src="https://github.com/user-attachments/assets/0c35b2a7-4de6-4d10-95d9-206cde5cf45b" />

Dann muss man im Node noch den Typ (binary = Dateien) wählen und einen Splitting Modus - also wie wird das Dokument in einzelne Chunks gesplittet:

<img width="3396" height="1850" alt="CleanShot 2025-10-30 at 05 53 17@2x" src="https://github.com/user-attachments/assets/d01b980a-8589-4944-a17f-7d2601b2eaab" />

So dann kann man eine Datei in Google Drive ablegen und den Workflow starten:
<img width="3448" height="1906" alt="CleanShot 2025-10-30 at 05 57 29@2x" src="https://github.com/user-attachments/assets/f8c2860f-b4f2-4bb2-8252-b3b865ac8c3a" />

Die Datei wird dann heruntergeladen, zersägt in einzelne Chunks und in die Vektordatenbank hochgeladen

<img width="3448" height="1906" alt="CleanShot 2025-10-30 at 05 57 29@2x" src="https://github.com/user-attachments/assets/5f47f879-60e7-4117-954b-67108329a1fb" />

So jetzt kann man auch wieder in Supabase gehen und sich das im Table Editor anschauen:

<img width="3446" height="1830" alt="CleanShot 2025-10-30 at 05 59 45@2x" src="https://github.com/user-attachments/assets/e2f7d89d-8e1f-4763-bf8d-c4a22a97ad3d" />

Und hier sieht man die ganzen Chunks des pdf-Dokuments Zeile für Zeile

So jetzt müssen wir unserem eigentlichen Chat Agenten noch die Verbindung zur Vektordatenbank geben:

Dazu fügen wir als Tool für den Agenten den Supabase Vektorstore hinzu:

<img width="3378" height="1844" alt="CleanShot 2025-10-30 at 06 09 38@2x" src="https://github.com/user-attachments/assets/414abc38-d6d6-48e9-899e-5b97ef922bb6" />

Hier definieren wir noch die Tabelle in der Datenbank und wie viele der passenden Chunks für die Antwort des LLMs verwendet werden sollen

<img width="3386" height="1838" alt="CleanShot 2025-10-30 at 06 11 02@2x" src="https://github.com/user-attachments/assets/72b4cea3-457c-4c7d-a13b-8ca5429c9e38" />

So damit man jetzt mit den gefunden Vektoren was anfangen kann brauchen wir noch mal ein Embedding LLM:

<img width="3442" height="1912" alt="CleanShot 2025-10-30 at 06 13 29@2x" src="https://github.com/user-attachments/assets/84f90606-695f-45e6-bf6e-089214c12b23" />

Dafür verwenden wir dann auch wieder das OpenAI Embedding Modell:

<img width="3370" height="1816" alt="CleanShot 2025-10-30 at 06 15 04@2x" src="https://github.com/user-attachments/assets/ab7fcba5-c5a1-4553-82a8-bff87e4003e9" />


So jetzt können wir noch in unseren AI Agent reingehen und diesem eine System Message (Prompt) geben für seine Aufgabe/ Rolle/ Kontext/ ...

<img width="3386" height="1820" alt="CleanShot 2025-10-30 at 06 18 34@2x" src="https://github.com/user-attachments/assets/a31d3361-ff53-4d67-b904-029c6c76a8ad" />

























































































