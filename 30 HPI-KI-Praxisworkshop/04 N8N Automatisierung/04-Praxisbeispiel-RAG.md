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

Sobald das Projekt erstellt wurde wählen wir es aus und können wir dieses Projekt dann die APIs von Google für die diversen Services aktivieren:










































