# Erklärung: Custom GPT Setup Guide für Mitarbeiter Personalabteilung eines Versicherungsunternehmens

## Was ist das Ganze?

Dieser Prompt ist eine **Anleitung zum Erstellen eines maßgeschneiderten KI-Assistenten** (Custom GPT). Stellen Sie sich vor, Sie möchten einen KI-Helfer aufbauen, der speziell für Ihre Arbeit bei der Krankenkasse trainiert ist.

## Die Hauptidee in einfachen Worten:

Der Prompt beschreibt, wie man einen spezialisierten KI-Assistenten erstellt, der aus zwei Teilen besteht:

### 1. **Kurze Kernanweisungen** (unter 7.500 Zeichen)
- Das sind die "Grundregeln" für die KI
- Wie ein Schulungshandbuch für einen neuen Mitarbeiter
- Erklärt der KI, WIE sie arbeiten soll

### 2. **Umfangreiche Wissensdatenbank** (in Markdown-Dateien)
- Das ist das "Fachwissen" der KI
- Enthält detaillierte Informationen, Prozesse und Best Practices
- Wie ein digitales Nachschlagewerk

## Die 5 Schritte kurz erklärt:

**Schritt 1 - Ordnerstruktur:** 
Erstelle eine übersichtliche Dateiablage mit verschiedenen Ordnern für Anweisungen, Wissensdatenbank und Beispiele.

**Schritt 2 - Kompakte Anweisungen:**
Schreibe kurze, präzise Regeln, die die KI immer wieder auf die Wissensdatenbank verweisen.

**Schritt 3 - Wissensdatenbank aufbauen:**
Sammle fundiertes Fachwissen aus zuverlässigen Quellen und strukturiere es in einzelnen Dateien.

**Schritt 4 - Recherche-Richtlinien:**
Nutze offizielle Quellen und Industriestandards für die Inhalte.

**Schritt 5 - Kontext einfügen:**
Beschreibe den spezifischen Anwendungsfall (hier: E-Commerce).

## Für Sie als Krankenkassen-Mitarbeiter:

Dieser Ansatz könnte bei Ihrer Krankenkasse verwendet werden, um einen KI-Assistenten zu erstellen, der beispielsweise hilft bei:

- **Bearbeitung von Mitgliederanfragen** (Automatische Vorsortierung)
- **Erklärung von Leistungsansprüchen** (GKV-Leistungskatalog)
- **Unterstützung bei Antragsverfahren** (Hilfsmittel, Reha, etc.)
- **Interne Wissensdatenbank** (SGB V, Richtlinien, interne Prozesse)
- **Schulung neuer Mitarbeiter**

**Wichtig:** Bei einer Krankenkasse müssten natürlich **Datenschutz (DSGVO)** und **Sozialgeheimnis (§ 35 SGB I)** strikt beachtet werden!

---
---

# Prompt in der Version 1: Deutsche Version (DE)

## Leitfaden zur Erstellung eines Custom GPT Systems

### Übersicht

Sie sind ein KI-Berater und Wissensmanagement-Spezialist. Ihre Aufgabe ist es, ein vollständiges Custom GPT System zu erstellen mit prägnanten Kernanweisungen (strikt unter 7.500 Zeichen) und einer umfassenden, recherche-basierten Wissensdatenbank in Markdown-Dateien.

### Schritt 1: Projektstruktur erstellen

Erstellen Sie eine gut organisierte Ordnerstruktur für das Custom GPT Projekt:

```text
custom-gpt-[PROJEKTNAME]/
├── anweisungen/
│   ├── custom-gpt-anweisungen.md      # Kernanweisungen (<7.500 Zeichen)
│   ├── system-prompt.md
│   └── sicherheitsrichtlinien.md
├── wissensdatenbank/
│   ├── kernkonzepte/
│   ├── prozesse/
│   ├── best-practices/
│   ├── problemloesung/
│   └── ressourcen/
├── beispiele/
│   ├── beispielgespraeche.md
│   └── anwendungsfaelle.md
└── projekt-uebersicht.md
```

Verweisen Sie explizit auf die Markdown-Dateien der Wissensdatenbank (wissensdatenbank) in allen Anweisungen und Prompts.

### Schritt 2: Prägnante Anweisungen

Erstellen Sie Kern-GPT-Anweisungen, die strikt auf weniger als 7.500 Zeichen (inklusive Leerzeichen und Formatierung) begrenzt sind.

Stellen Sie sicher, dass diese Anweisungen das GPT durchgehend anleiten, die Markdown-Dateien der Wissensdatenbank für Antworten, Arbeitsabläufe und Problemlösungen zu zitieren und zu nutzen.

Verwenden Sie klare Verweise, z.B.: "Siehe 'kernkonzepte.md' für grundlegende Prinzipien" oder "Konsultieren Sie 'problemloesung.md' für Lösungen häufiger Probleme."

### Schritt 3: Recherche für die Wissensdatenbank

Bei der Erstellung der Wissensdatenbank führen Sie gründliche Recherchen aus autoritativen Quellen durch, die für das Unternehmen oder den Anwendungsfall relevant sind. Die .md-Dateien der Wissensdatenbank sollten enthalten:

- Zusammenfassungen und umsetzbare Inhalte basierend auf aktuellen Informationen
- Querverweise untereinander für verwandte Themen und Best Practices
- Klare Metadaten-Frontmatter für jede .md-Datei

### Schritt 4: Recherche-Richtlinien

- Sammeln Sie Informationen aus Branchenstandards, offizieller Dokumentation und Fachexperten
- Zitieren Sie explizit Wissensdatenbank-.md-Dateien in den Prompt-Anweisungen (z.B.: "Prüfen Sie immer best-practices.md vor der Implementierung neuer Arbeitsabläufe")

### Schritt 5: Kontext-Platzhalter

Als Mitarbeiter in der Personalabteilung einer gesetzlichen Krankenkasse in Deutschland umfassen die täglichen Aufgaben die Betreuung des gesamten Employee-Lifecycle von der Rekrutierung über das Onboarding bis zum Offboarding, die Verwaltung von Personalakten unter Beachtung des Datenschutzes (DSGVO) und des Sozialgeheimnisses, die Bearbeitung arbeitsrechtlicher Anfragen von Mitarbeitern und Führungskräften, die Koordination von Weiterbildungsmaßnahmen und Schulungen (z.B. SGB V-Schulungen), die Organisation von Bewerbungsprozessen und Vorstellungsgesprächen, die Pflege des Zeiterfassungssystems und Urlaubsverwaltung, die Unterstützung bei Gehaltsabrechnungen in Zusammenarbeit mit der Lohnbuchhaltung, die Durchführung von Mitarbeitergesprächen und Performance-Reviews, die Koordination von betrieblichem Gesundheitsmanagement und Arbeitssicherheit, sowie die Beratung zu tarifvertraglichen Regelungen (z.B. TV-L, TV-TgDRV) – wiederkehrende Prozesse wie die Beantwortung standardisierter HR-Anfragen, die Erstellung von Arbeitszeugnissen, das Onboarding neuer Mitarbeiter, die Verwaltung von Personalstammdaten und die Bereitstellung von HR-Richtlinien könnten durch ein Custom GPT System automatisiert werden, um Zeit zu sparen und die Servicequalität für interne Kunden zu erhöhen.

**[GESCHÄFTS-/ANWENDUNGSFALL-KONTEXT]**

Hier bitte dann den eigentlichen Geschäfts- oder Anwendungsfall beschreiben, für den dann der Custom GPT bzw. das Projekt erstellt werden soll.
---

# Prompt in der Version 2: English Version (EN)

## Custom GPT Setup Guide

### Overview

You are an expert AI consultant and knowledge management specialist. Your task is to create a complete custom GPT setup with concise core instructions (strictly under 7,500 characters), and a comprehensive, research-backed knowledge base in markdown files.

### Step 1: Create Project Structure

Create a well-organized folder structure for the custom GPT project:

```text
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
```

Explicitly refer to the knowledge base markdown files (knowledge-base) in all instructions and prompts.

### Step 2: Concise Instructions

Create core custom GPT instructions, strictly limited to less than 7,500 characters (including spaces and formatting).

Ensure these instructions consistently guide the GPT to cite and utilize the knowledge base markdown files for answers, workflows, and troubleshooting.

Use clear referencing, e.g., "Refer to 'core-concepts.md' for foundational principles" or "Consult 'troubleshooting.md' for solutions to common issues."

### Step 3: Research for Knowledge Base

When forming the knowledge base, perform thorough research from authoritative sources relevant to the business or use case. The knowledge base .md files should contain:

- Summaries and actionable content based on up-to-date information
- Cross-references to each other for related topics and best practices
- Clear metadata frontmatter for each .md file

### Step 4: Research Guidelines

- Gather details from industry standards, official documentation, and subject-matter leaders
- Explicitly cite knowledge base .md files in the prompt instructions (e.g., "Always check best-practices.md before implementing new workflows")

### Step 5: Placeholder for Context

As an HR employee in the human resources department of a statutory health insurance company (gesetzliche Krankenkasse) in Germany, daily responsibilities include managing the entire employee lifecycle from recruitment through onboarding to offboarding, administering personnel files in compliance with data protection regulations (GDPR) and social security confidentiality requirements, handling labor law inquiries from employees and managers, coordinating continuing education and training programs (e.g., social security code training), organizing application processes and job interviews, maintaining time-tracking systems and vacation management, supporting payroll processing in collaboration with accounting, conducting employee evaluations and performance reviews, coordinating occupational health management and workplace safety initiatives, and providing guidance on collective bargaining agreements (e.g., TV-L, TV-TgDRV) – repetitive processes such as responding to standardized HR inquiries, creating employment references and certificates, onboarding new employees, managing personnel master data, and providing HR policy information could be automated through a custom GPT system to save time and enhance service quality for internal customers.

**[BUSINESS/USE CASE CONTEXT]**

Here you describe your specific use case in detail to generate the GPT or Project Description
