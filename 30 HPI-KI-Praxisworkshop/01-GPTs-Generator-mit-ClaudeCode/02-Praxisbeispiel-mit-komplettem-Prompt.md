# Custom GPT Erstellungsanweisungen: Arbeitszeugnis-Generator für Krankenkassen

## Leitfaden zur Erstellung eines Custom GPT Systems

### Nutzungshinweise:
Geben Sie den nachfolgenden Prompt in Claude Code ein und damit startet dann die Generierung des "Codes" - in diesem Fall des GPTs mit allen Anweisungsdateien und der Recherche und Erstellung des notwendigen Wissens.


### Prompt

Sie sind ein KI-Berater und Wissensmanagement-Spezialist. Ihre Aufgabe ist es, ein vollständiges Custom GPT System zu erstellen mit prägnanten Kernanweisungen (strikt unter 7.500 Zeichen) und einer umfassenden, recherche-basierten Wissensdatenbank in Markdown-Dateien.

### Schritt 1: Projektstruktur erstellen

Erstellen Sie eine gut organisierte Ordnerstruktur für das Custom GPT Projekt:

```text
custom-gpt-arbeitszeugnis-generator/
├── anweisungen/
│   ├── custom-gpt-anweisungen.md      # Kernanweisungen (<7.500 Zeichen)
│   ├── system-prompt.md
│   └── sicherheitsrichtlinien.md
├── wissensdatenbank/
│   ├── kernkonzepte/
│   │   ├── zeugnisarten.md
│   │   ├── rechtliche-grundlagen.md
│   │   └── zeugnissprache.md
│   ├── prozesse/
│   │   ├── erstellungsprozess.md
│   │   ├── qualitaetssicherung.md
│   │   └── freigabeworkflow.md
│   ├── best-practices/
│   │   ├── formulierungsrichtlinien.md
│   │   ├── notenskala-kodierung.md
│   │   └── branchenspezifische-taetigkeiten.md
│   ├── problemloesung/
│   │   ├── haeufige-fehler.md
│   │   ├── rechtliche-fallstricke.md
│   │   └── konfliktfaelle.md
│   └── ressourcen/
│       ├── musterformulierungen.md
│       ├── taetigkeitsbeschreibungen-krankenkasse.md
│       ├── rechtsprechung.md
│       └── vorlagen.md
├── beispiele/
│   ├── beispielgespraeche.md
│   └── anwendungsfaelle.md
└── projekt-uebersicht.md
```

Verweisen Sie explizit auf die Markdown-Dateien der Wissensdatenbank (wissensdatenbank) in allen Anweisungen und Prompts.

### Schritt 2: Prägnante Anweisungen

Erstellen Sie Kern-GPT-Anweisungen, die strikt auf weniger als 7.500 Zeichen (inklusive Leerzeichen und Formatierung) begrenzt sind.

Stellen Sie sicher, dass diese Anweisungen das GPT durchgehend anleiten, die Markdown-Dateien der Wissensdatenbank für Antworten, Arbeitsabläufe und Problemlösungen zu zitieren und zu nutzen.

Verwenden Sie klare Verweise, z.B.: 
- "Siehe 'zeugnisarten.md' für die Unterscheidung zwischen einfachem und qualifiziertem Zeugnis"
- "Konsultieren Sie 'notenskala-kodierung.md' für die korrekte Leistungsbeurteilung"
- "Prüfen Sie 'rechtliche-grundlagen.md' für Wahrheitspflicht und Wohlwollensprinzip"
- "Verwenden Sie 'musterformulierungen.md' für branchenübliche Formulierungen"
- "Beachten Sie 'taetigkeitsbeschreibungen-krankenkasse.md' für spezifische Berufsbilder"

### Schritt 3: Recherche für die Wissensdatenbank

Bei der Erstellung der Wissensdatenbank führen Sie gründliche Recherchen aus autoritativen Quellen durch, die für das Unternehmen oder den Anwendungsfall relevant sind. Die .md-Dateien der Wissensdatenbank sollten enthalten:

#### Für den Arbeitszeugnis-Generator spezifisch zu recherchieren:

**Rechtliche Grundlagen:**
- Gesetzliche Anspruchsgrundlage (§ 109 GewO)
- BAG-Rechtsprechung zu Arbeitszeugnissen
- Wahrheitspflicht vs. Wohlwollensprinzip
- Formalien und Pflichtbestandteile
- Ausstellungsfristen und Verjährung

**Zeugnissprache und Kodierung:**
- Notenskala (sehr gut bis ausreichend)
- Verschlüsselte Formulierungen und ihre Bedeutung
- Standardformulierungen und Abweichungen
- Geheimcodes und deren rechtliche Unzulässigkeit
- Schlussformeln und ihre Bewertung

**Krankenkassen-spezifische Tätigkeiten:**
- Sachbearbeiter Leistungen (Krankenversicherung, Pflege)
- Kundenberater / Versichertenberater
- Vertriebsmitarbeiter Außendienst
- Teamleiter / Abteilungsleiter
- Fachabteilungen (Beitragsabrechnung, Leistungsmanagement, etc.)
- Spezialisten (Datenschutz, Compliance, IT)

**Strukturelemente eines Zeugnisses:**
- Kopfzeile und Einleitung
- Tätigkeitsbeschreibung
- Leistungsbeurteilung
- Verhaltensbeurteilung (Sozialverhalten)
- Schlussformel
- Datum und Unterschrift

**Best Practices:**
- Formulierungsempfehlungen nach Leistungsniveau
- Vermeidung diskriminierender Aussagen (AGG)
- Vermeidung negativer Formulierungen
- Positive Umschreibung von Kritikpunkten
- Vollständigkeit und Lückenlosigkeit

Jede .md-Datei sollte enthalten:
- Zusammenfassungen und umsetzbare Inhalte basierend auf aktuellen Informationen
- Querverweise untereinander für verwandte Themen und Best Practices
- Klare Metadaten-Frontmatter für jede .md-Datei

### Schritt 4: Recherche-Richtlinien

- Sammeln Sie Informationen aus Branchenstandards, offizieller Dokumentation und Fachexperten:
  - Bundesarbeitsgericht (BAG) Urteile zu Arbeitszeugnissen
  - § 109 Gewerbeordnung (GewO)
  - Fachliteratur zum Arbeitsrecht
  - Zeugnisratgeber und HR-Standardwerke
  - Krankenkassen-spezifische Tätigkeitsprofile
  - Tarifverträge (TV-TgDRV, TV-L) für Positionsbezeichnungen

- Zitieren Sie explizit Wissensdatenbank-.md-Dateien in den Prompt-Anweisungen:
  - "Prüfen Sie immer 'rechtliche-grundlagen.md' vor der Zeugnis-Erstellung"
  - "Konsultieren Sie 'notenskala-kodierung.md' für jede Leistungsbeurteilung"
  - "Verwenden Sie 'formulierungsrichtlinien.md' für alle Textbausteine"
  - "Beachten Sie 'haeufige-fehler.md' zur Qualitätssicherung"

### Schritt 5: Geschäfts-/Anwendungsfall-Kontext

In der Personalabteilung einer gesetzlichen Krankenkasse erstellen Sie regelmäßig qualifizierte Arbeitszeugnisse für ausscheidende Mitarbeiter. Zu den Aufgaben gehören die Sammlung von Informationen über Tätigkeitsbereiche, Verantwortlichkeiten und Leistungsbeurteilungen aus Mitarbeitergesprächen und Personalakten, die Einhaltung rechtlicher Vorgaben nach § 109 GewO (wohlwollende Formulierung bei gleichzeitiger Wahrheitspflicht), die Beachtung der BAG-Rechtsprechung zu Arbeitszeugnissen, die Anwendung branchenspezifischer Standards für Krankenkassen-Berufe (z.B. Sachbearbeiter Leistungen SGB V, Kundenberater Versicherte, Teamleiter Leistungsmanagement, Vertriebsmitarbeiter Außendienst, Fachreferenten Gesundheitsmanagement), die korrekte Formulierung in Zeugnissprache mit präziser Notenskala-Kodierung (sehr gut bis ausreichend), die Abstimmung mit direkten Vorgesetzten und Abteilungsleitern zur Leistungsbeurteilung, die rechtliche und sprachliche Qualitätssicherung unter Vermeidung diskriminierender Aussagen (AGG-Konformität), die Sicherstellung der Vollständigkeit aller Pflichtbestandteile (Tätigkeitsbeschreibung, Leistungsbeurteilung, Verhaltensbeurteilung, Schlussformel), die termingerechte Erstellung bei Kündigungen gemäß gesetzlicher Ausstellungsfristen, die Unterscheidung zwischen einfachen und qualifizierten Zeugnissen je nach Mitarbeiterwunsch, sowie die Archivierung in Personalakten unter Beachtung des Datenschutzes (DSGVO) und des Sozialgeheimnisses (§ 35 SGB I).

Wiederkehrende Prozesse wie die strukturierte Informationssammlung von Führungskräften, die Generierung von Zeugnisentwürfen basierend auf Tätigkeitsprofilen und Leistungsbewertungen, die Formulierung rechtssicherer und wohlwollender Textbausteine, die Anwendung der korrekten Zeugnissprache und Notenskala, die Vermeidung rechtlicher Fallstricke und missverständlicher Formulierungen, die Erstellung verschiedener Zeugnisarten (Zwischenzeugnis, Endzeugnis, Ausbildungszeugnis), die Qualitätsprüfung auf Vollständigkeit und formale Korrektheit, sowie die Bereitstellung von Formulierungshilfen und Textbausteinen für unterschiedliche Leistungsniveaus und Tätigkeitsbereiche könnten durch ein Custom GPT System automatisiert und standardisiert werden, um die Bearbeitungszeit erheblich zu reduzieren, die Qualität und Rechtssicherheit der Zeugnisse zu erhöhen, HR-Mitarbeiter von repetitiven Aufgaben zu entlasten und eine konsistente, faire und rechtskonforme Zeugniserstellung für alle Mitarbeiter der Krankenkasse sicherzustellen.

**Kernanforderungen an das Custom GPT System:**

1. **Strukturierte Informationsaufnahme:** Geführte Abfrage aller relevanten Daten (Position, Tätigkeiten, Zeitraum, Leistung, Verhalten)

2. **Tätigkeitsbeschreibungen:** Generierung präziser, vollständiger Tätigkeitsbeschreibungen basierend auf krankenkassen-spezifischen Berufsprofilen (siehe 'taetigkeitsbeschreibungen-krankenkasse.md')

3. **Leistungsbeurteilung:** Korrekte Anwendung der Notenskala-Kodierung mit entsprechenden Standardformulierungen (siehe 'notenskala-kodierung.md' und 'formulierungsrichtlinien.md')

4. **Rechtssicherheit:** Einhaltung aller gesetzlichen Vorgaben, Vermeidung rechtlicher Fallstricke (siehe 'rechtliche-grundlagen.md' und 'rechtliche-fallstricke.md')

5. **Qualitätssicherung:** Automatische Prüfung auf Vollständigkeit, Konsistenz und formale Korrektheit (siehe 'qualitaetssicherung.md')

6. **Anpassungsfähigkeit:** Generierung unterschiedlicher Zeugnisarten und individueller Anpassungen bei Bedarf (siehe 'zeugnisarten.md')

7. **Compliance:** DSGVO-konforme Verarbeitung sensibler Personaldaten, AGG-konforme Formulierungen (siehe 'sicherheitsrichtlinien.md')

---

## Zusätzliche Implementierungshinweise für den Arbeitszeugnis-Generator:

### Interaktiver Workflow:
Das GPT sollte einen schrittweisen Dialog führen:
1. Zeugnis-Art abfragen (Zwischenzeugnis/Endzeugnis/Ausbildungszeugnis)
2. Mitarbeiterdaten erfassen (Name, Position, Zeitraum)
3. Tätigkeitsbereiche strukturiert abfragen
4. Leistungsbewertung erfragen (Note 1-5 oder qualitative Beschreibung)
5. Verhaltensbewertung erfragen
6. Besondere Leistungen/Projekte erfragen
7. Kündigungsgrund erfragen (für Schlussformel)
8. Zeugnisentwurf generieren
9. Feedback-Schleife für Anpassungen

### Ausgabeformat:
- Vollständiges, druckfertiges Zeugnis
- Optional: Erklärung der verwendeten Formulierungen
- Qualitätsprüfungs-Checkliste
- Hinweise auf potenzielle rechtliche Risiken

### Datenschutz-Hinweise:
- Keine Speicherung personenbezogener Daten
- Hinweis auf vertrauliche Behandlung
- Empfehlung zur Überprüfung durch HR-Leitung


## Screenshot aus Claude Code in Visual Studio Code integriert:

<img width="3454" height="2030" alt="CleanShot 2025-10-27 at 06 41 41@2x" src="https://github.com/user-attachments/assets/0c4142e2-79bd-4863-bb8e-72db9133784c" />

### Anleitung Nutzung der Daten:

Mit den Daten in den Ordnern kann man jetzt einen GPT oder ein Projekt erstellen. Dabei nutzt man die Inhalte aus dem Ordner Anweisungen für den Bereich "Hinweise" bzw. "Instructions" des GPTs/ Projekts und die anderen Dateien sind dann das "Wissen", das man hochlädt. Eine wichtige Datei ist dabei die "projekt-uebersicht.md" Datei, die die gesamte Struktur erklärt und die man im Bereich Hinweise / Instructions des GPTs bzw. Projektes auch "verlinken" sollte, damit diese als erste wichtige Anweisung gelesen wird.
