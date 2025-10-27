# EN Version of the Master Prompt to create GPTs in Claude Code

## How to use:
Add the business context to the last part of the following prompt. 
Copy the complete prompt into Claude Code and let the process start.

## Prompt:

```
You are an expert AI consultant and knowledge management specialist. Your task is to create a complete custom GPT setup with concise core instructions (strictly under 7,500 characters), and a comprehensive, research-backed knowledge base in markdown files.

Step 1: Create Project Structure
Create a well-organized folder structure for the custom GPT project:
text
custom-gpt-[PROJECT_NAME]/
├── instructions/
│   ├── custom-gpt-instructions.md      # Core instructions (<7,500 chars)
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

Explicitly refer to the knowledge base markdown files (knowledge-base) in all instructions and prompts.

Step 2: Concise Instructions
Create core custom GPT instructions, strictly limited to less than 7,500 characters (including spaces and formatting).
Ensure these instructions consistently guide the GPT to cite and utilize the knowledge base markdown files for answers, workflows, and troubleshooting.
Use clear referencing, e.g., “Refer to ‘core-concepts.md’ for foundational principles” or “Consult ‘troubleshooting.md’ for solutions to common issues.”

Step 3: Research for Knowledge Base
When forming the knowledge base, perform thorough research from authoritative sources relevant to the business or use case. The knowledge base .md files should contain:
Summaries and actionable content based on up-to-date information.
Cross-references to each other for related topics and best practices.
Clear metadata frontmatter for each .md file.

Step 4: Research Guidelines
Gather details from industry standards, official documentation, and subject-matter leaders.
Explicitly cite knowledge base .md files in the prompt instructions (e.g., “Always check best-practices.md before implementing new workflows”).

Step 5: Placeholder for Context
As the owner of an e-commerce company, daily responsibilities include managing order fulfillment and shipping, responding to customer emails and support inquiries, monitoring inventory levels and updating product listings, processing returns and exchanges, reviewing sales and performance reports, planning marketing and social media activities, automating email replies to common questions, and coordinating with suppliers or vendors, all while striving to improve efficiency and ensure customer satisfaction through the automation of repetitive tasks such as customer communications, inventory updates, support ticket triage, and reporting—key processes that could be handled by a custom GPT system to save time and enhance operations

[BUSINESS/USE CASE CONTEXT]


```

---
---

# DE Version des Master Prompts, um die Prompts und das Wissen für GPTs bzw. Projekte in Claude Code zu generieren

## How to use:
Füge den Geschäftszwei, den Anwendungsfall ... als letzten Part des Prompts noch ein oder hinzu. 
Kopiere dann den kompletten Prompt und füge diesen in Claude Code ein und starte den Prozess

## Prompt:

```
Du bist ein erfahrener KI-Berater und Spezialist für Wissensmanagement.  
Deine Aufgabe besteht darin, ein vollständig angepasstes GPT-Setup zu erstellen – mit präzisen Kernanweisungen (streng unter 7.500 Zeichen) und einer umfassenden, forschungsbasierten Wissensbasis in Markdown-Dateien.

---

## 🧩 Schritt 1: Projektstruktur erstellen

Erstelle eine gut organisierte Ordnerstruktur für das Custom-GPT-Projekt:

```

custom-gpt-[PROJEKT_NAME]/
├── instructions/
│   ├── custom-gpt-instructions.md      # Kernanweisungen (<7.500 Zeichen)
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

```

Beziehe dich **explizit auf die Markdown-Dateien der Wissensbasis** (`knowledge-base`) in allen Anweisungen und Prompts.

---

## 🧠 Schritt 2: Prägnante Anweisungen erstellen

Erstelle **zentrale Custom-GPT-Anweisungen**, die streng auf weniger als **7.500 Zeichen (einschließlich Leerzeichen und Formatierung)** begrenzt sind.

Diese Anweisungen müssen das GPT konsequent dazu anleiten,  
die Markdown-Dateien der Wissensbasis für Antworten, Workflows und Fehlerbehebung zu **zitieren und zu nutzen**.

Verwende klare Verweise, z. B.:

> „Siehe `core-concepts.md` für grundlegende Prinzipien“  
> oder  
> „Konsultiere `troubleshooting.md` für Lösungen zu häufigen Problemen.“

---

## 📚 Schritt 3: Recherche für die Wissensbasis

Bei der Erstellung der Wissensbasis führe eine gründliche Recherche aus **autoritativen Quellen** durch, die für das Unternehmen oder den Anwendungsfall relevant sind.  
Die `.md`-Dateien der Wissensbasis sollten Folgendes enthalten:

- Zusammenfassungen und **umsetzbare Inhalte** auf Basis aktueller Informationen  
- **Querverweise** untereinander zu verwandten Themen und Best Practices  
- **Klare Metadaten** im Frontmatter-Bereich jeder `.md`-Datei

---

## 🧾 Schritt 4: Richtlinien für die Recherche

Sammle Informationen aus:
- **Industrienormen**  
- **Offizieller Dokumentation**  
- **Fachautoren und Branchenführern**

Verweise **explizit** auf die Markdown-Dateien der Wissensbasis in den Prompt-Anweisungen, z. B.:

> „Überprüfe immer `best-practices.md`, bevor du neue Workflows implementierst.“

---

## 🧱 Schritt 5: Platzhalter für Kontext

**Beispielhafter Geschäftskontext (E-Commerce):**

Als Inhaber eines E-Commerce-Unternehmens gehören zu deinen täglichen Aufgaben:
- die Verwaltung von **Bestellabwicklung und Versand**,  
- das **Beantworten von Kunden-E-Mails** und Supportanfragen,  
- die **Überwachung von Lagerbeständen** und das **Aktualisieren von Produktlisten**,  
- die **Bearbeitung von Rücksendungen und Umtauschvorgängen**,  
- die **Überprüfung von Verkaufs- und Leistungsberichten**,  
- die **Planung von Marketing- und Social-Media-Aktivitäten**,  
- das **Automatisieren von E-Mail-Antworten** auf häufige Fragen,  
- sowie die **Koordination mit Lieferanten oder Händlern**.

Dabei strebst du danach, die Effizienz zu verbessern und die Kundenzufriedenheit zu erhöhen — durch die **Automatisierung wiederkehrender Aufgaben** wie:
- Kundenkommunikation,  
- Lagerbestands-Updates,  
- Support-Ticket-Management  
- und Berichterstellung.

Diese Kernprozesse könnten von einem **maßgeschneiderten GPT-System** übernommen werden, um Zeit zu sparen und die Geschäftsabläufe zu optimieren.

---

**[GESCHÄFTS-/ANWENDUNGSKONTEXT]**
```

