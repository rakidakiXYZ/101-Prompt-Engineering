
---

## Überblick

Der Prompt beschreibt ein **Projekt**, bei dem man ein eigenes „Custom-GPT“ (also ein KI-Modell mit individuellen Regeln und Wissen) aufbaut.
Das Ziel:
👉 Die KI soll klare Instruktionen haben **und** auf eine strukturierte Wissensbasis (Sammlung von Markdown-Dateien) zurückgreifen.

Damit soll das GPT-System später im Alltag eines E-Commerce-Unternehmens nützlich sein, z. B. beim **Kundenservice, Lager, Versand oder Marketing**.

---

---
## Der Prompt

```markdown
Du bist ein erfahrener KI-Berater und Spezialist für Wissensmanagement.  
Deine Aufgabe ist es, ein vollständiges benutzerdefiniertes GPT-Setup zu erstellen mit präzisen Kerninstruktionen (streng unter 7.500 Zeichen) sowie einer umfassenden, forschungsbasierten Wissensbasis in Markdown-Dateien.  

### Schritt 1: Projektstruktur erstellen
Erstelle eine gut organisierte Ordnerstruktur für das Custom-GPT-Projekt:  

```text
custom-gpt-[PROJEKT_NAME]/
├── instructions/
│   ├── custom-gpt-instructions.md # Kerninstruktionen (<7.500 Zeichen)
│   ├── system-prompt.md
│   └── security-guidelines.md
├── knowledge-base/
│   ├── core-concepts/
│   ├── procedures/
│   ├── best-practices/
│   ├── troubleshooting/
│   └── resources/
├── examples/
│   ├── sample-conversations.md
│   └── use-case-scenarios.md
└── project-overview.md
````

Beziehe dich in allen Instruktionen und Prompts explizit auf die Markdown-Dateien der Wissensbasis (`knowledge-base`).

---

### Schritt 2: Prägnante Instruktionen

Erstelle die zentralen Custom-GPT-Instruktionen, streng begrenzt auf weniger als 7.500 Zeichen (einschließlich Leerzeichen und Formatierung).
Stelle sicher, dass diese Instruktionen das GPT konsequent anleiten, die Markdown-Dateien der Wissensbasis für Antworten, Workflows und Problemlösungen zu zitieren und zu nutzen.

Verwende klare Referenzen, z. B.:

* „Siehe `core-concepts.md` für grundlegende Prinzipien“
* „Konsultiere `troubleshooting.md` für Lösungen zu häufigen Problemen.“

---

### Schritt 3: Recherche für die Wissensbasis

Bei der Erstellung der Wissensbasis führe gründliche Recherchen aus autoritativen Quellen durch, die für das jeweilige Unternehmen oder den Anwendungsfall relevant sind.
Die .md-Dateien der Wissensbasis sollen enthalten:

* Zusammenfassungen und umsetzbare Inhalte, basierend auf aktuellen Informationen
* Querverweise untereinander für verwandte Themen und Best Practices
* Klar strukturierte **Metadaten (Frontmatter)** für jede .md-Datei

---

### Schritt 4: Recherche-Richtlinien

Sammle Details aus Industriestandards, offizieller Dokumentation und anerkannten Expertenquellen.
Zitiere die Wissensbasis-Dateien explizit in den Prompt-Instruktionen (z. B. „Prüfe immer `best-practices.md`, bevor neue Workflows implementiert werden“).

---

### Schritt 5: Platzhalter für den Kontext
[GESCHÄFTS-/ANWENDUNGSFALL-KONTEXT]

Hier kommt jetzt ein Beispiel für den Kontext:

Als Inhaber eines E-Commerce-Unternehmens umfassen die täglichen Aufgaben u. a.:

* Verwaltung von Auftragsabwicklung und Versand
* Beantwortung von Kunden-E-Mails und Supportanfragen
* Überwachung von Lagerbeständen und Aktualisierung von Produktlisten
* Bearbeitung von Retouren und Umtauschvorgängen
* Überprüfung von Verkaufs- und Leistungsberichten
* Planung von Marketing- und Social-Media-Aktivitäten
* Automatisierung von E-Mail-Antworten auf häufige Fragen
* Koordination mit Lieferanten oder Partnern

… bei gleichzeitiger kontinuierlicher Steigerung der Effizienz und Sicherstellung der Kundenzufriedenheit. Dies geschieht durch die Automatisierung wiederkehrender Aufgaben wie Kundenkommunikation, Bestandsaktualisierungen, Support-Ticket-Triage und Reporting – zentrale Prozesse, die von einem Custom-GPT-System übernommen werden können, um Zeit zu sparen und Abläufe zu optimieren.

```

---

## Schritt-für-Schritt-Erklärung

### 🔹 Schritt 1: Projektstruktur

* Du legst eine **Ordnerstruktur** an.
* Diese sorgt dafür, dass alle Dateien übersichtlich sortiert sind:

  * **instructions/** → enthält die Kernanweisungen, den System-Prompt und Sicherheitsrichtlinien
  * **knowledge-base/** → hier liegt das gesammelte Wissen, aufgeteilt in Themen wie Grundlagen, Best Practices oder Troubleshooting
  * **examples/** → Beispielgespräche und Anwendungsszenarien
  * **project-overview.md** → eine Übersicht über das ganze Projekt

👉 Vorteil: So weiß die KI genau, wo sie Informationen findet.

---

### 🔹 Schritt 2: Prägnante Instruktionen

* Die **zentralen Anweisungen** für die KI dürfen **maximal 7.500 Zeichen** lang sein.
* Sie sollen klar regeln, wie die KI arbeitet.
* Besonders wichtig: Die KI soll immer auf die **Markdown-Dateien in der Wissensbasis** verweisen.

  * Beispiel: „Siehe `core-concepts.md`“ oder „Schau in `troubleshooting.md`“.

👉 Das macht die Antworten nachvollziehbar und konsistent.

---

### 🔹 Schritt 3: Wissensbasis erstellen

* Die Markdown-Dateien in `knowledge-base/` sind das **Herzstück**.
* Sie enthalten:

  * **Zusammenfassungen** und **umsetzbare Tipps**
  * **Querverweise** zu anderen Dateien (damit die Inhalte zusammenhängen)
  * **Metadaten (Frontmatter)** am Anfang jeder Datei (z. B. Titel, Erstellungsdatum, Tags)

👉 So bleibt das Wissen aktuell, durchsuchbar und wiederverwendbar.

---

### 🔹 Schritt 4: Recherche-Richtlinien

* Bevor du Inhalte für die Wissensbasis erstellst, sollst du **gründlich recherchieren**.
* Quellen: Offizielle Dokumentationen, Industriestandards, Expertenartikel.
* In den Instruktionen für das GPT soll explizit stehen, dass es diese Dateien nutzen soll.

👉 Beispiel: „Bevor du einen Workflow beschreibst, prüfe `best-practices.md`.“

---

### 🔹 Schritt 5: Platzhalter für den Anwendungsfall

* Der Prompt liefert einen **konkreten Geschäftskontext**:
  Ein **E-Commerce-Unternehmen**, das viele tägliche Aufgaben hat:

  * Aufträge bearbeiten
  * Kunden-E-Mails beantworten
  * Lager und Bestände überwachen
  * Retouren abwickeln
  * Verkaufsberichte prüfen
  * Marketing planen
* Ziel: Wiederkehrende Aufgaben **automatisieren** und Zeit sparen.

👉 An dieser Stelle ([GESCHÄFTS-/ANWENDUNGSFALL-KONTEXT]) wird später **der individuelle Kontext** eingesetzt, z. B. Infos über das eigene Geschäft.

---

## Zusammenfassung für Anfänger

* Das Projekt baut ein **maßgeschneidertes GPT-System** auf.
* Die **Instruktionen** steuern das Verhalten der KI (max. 7.500 Zeichen).
* Die **Wissensbasis** ist wie ein Handbuch in Markdown-Dateien.
* Die KI muss diese Dateien zitieren und nutzen.
* Alles wird mit einer **klaren Ordnerstruktur** organisiert.
* Am Ende entsteht ein **praktisches KI-Werkzeug für ein E-Commerce-Business**, das Aufgaben automatisieren hilft.

---

👉 Einfach gesagt:
Der Prompt zeigt dir, **wie du Schritt für Schritt eine „eigene KI“ mit Regeln + Wissen + Praxisbeispielen aufbaust**, damit sie im Geschäftsalltag zuverlässig eingesetzt werden kann.

---

Möchtest du, dass ich dir dazu ein **visuelles Schaubild** erstelle, das die Struktur und den Ablauf für Anfänger noch klarer macht?

