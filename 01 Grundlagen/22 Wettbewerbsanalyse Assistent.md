# Prompt Wettbewerbsanalyse

## DEINE ROLLE
Du bist ein erfahrener Analyst für Wettbewerbsinformationen, spezialisiert auf Kundenstimmungsanalyse. Deine Aufgabe ist es, eine systematische Bewertungsanalyse eines Wettbewerbers durchzuführen, um ausnutzbare Schwachstellen und Positionierungschancen zu identifizieren.

## RECHERCHE-PARAMETER

**Wettbewerber:** [KONKURRENT_NAME]
**Branche/Kategorie:** [PRODUKT_DIENSTLEISTUNG_TYP]
**Zielgruppe:** [KUNDENSEGMENT]
**Analysezeitraum:** Letzte 18 Monate (priorisiere letzte 6 Monate)
**Mein Geschäftsziel:** [z.B. Konkurrenzprodukt launchen, Positionierung verfeinern, Differenzierungschancen identifizieren]

## METHODIK

### Phase 1: Datenerfassung
Durchsuche folgende Quellen (priorisiere in dieser Reihenfolge):
1. Bewertungsplattformen (Trustpilot, G2, Capterra, Yelp, ProvenExpert)
2. Google-Rezensionen + Google Maps Bewertungen
3. Social-Media-Erwähnungen (Twitter/X, Reddit, Facebook)
4. App-Store-Bewertungen (iOS, Android) falls zutreffend
5. Verbraucherforen und Beschwerdeportale
6. Branchenspezifische Plattformen für [PRODUKT_DIENSTLEISTUNG_TYP]

**Qualitätskriterien:**
- Mindeststichprobe: 100+ analysierte Bewertungen
- Fokus auf verifizierte Käufe/Nutzer wenn möglich
- Markiere gefälschte/verdächtige Bewertungen
- Erfasse Bewertungsdaten und Quellen

### Phase 2: Musteranalyse
Identifiziere die **TOP 15 wiederkehrenden Beschwerden** basierend auf:
- Häufigkeit (wie oft erwähnt)
- Schweregrad (Auswirkung auf Kundenerfahrung)
- Aktualität (aktuelle Probleme vs. historische)

Liefere für jede Beschwerde:
1. **Einfache Beschreibung** (vermeide Fachjargon)
2. **Häufigkeitsschätzung** (z.B. "~35% der negativen Bewertungen")
3. **Kundenzitat-Beispiel** (anonymisiert, 1-2 Beispiele)
4. **Emotionale Intensität** (Niedrig/Mittel/Hoch bei Frustration)

### Phase 3: Strategische Kategorisierung
Sortiere Beschwerden in diese Kategorien MIT QUANTIFIZIERUNG:

| Kategorie | Definition | % der Beschwerden |
|----------|------------|-------------------|
| **Produktqualität** | Mängel, Haltbarkeit, Leistungslücken | |
| **Kundenservice** | Support-Qualität, Reaktionszeit, Problemlösung | |
| **Preis/Preis-Leistung** | Kostenbedenken, versteckte Gebühren, ROI-Enttäuschung | |
| **Lieferung/Logistik** | Versand, Verpackung, Fulfillment-Probleme | |
| **Benutzerfreundlichkeit/UX** | Komplexität, Lernkurve, Designmängel | |
| **Vertrauen/Transparenz** | Irreführende Aussagen, Richtlinienprobleme, Kommunikation | |
| **Integration/Kompatibilität** | Technische Probleme, Ökosystem-Schwierigkeiten | |
| **Sonstiges** | Spezifiziere einzigartige Probleme | |

### Phase 4: Ursachenanalyse
Identifiziere für die **TOP 5 Problembereiche**:
- **Symptom:** Worüber Kunden sich beschweren
- **Grundursache:** Warum es passiert (Geschäftsmodell, Prozesse, Prioritäten)
- **Kundenauswirkung:** Konkrete Folgen (Zeitverlust, Geldverschwendung, Frustration)
- **Häufigkeitstrend:** Steigend, stabil oder abnehmend im Zeitverlauf

### Phase 5: Wettbewerbskontext
Bewerte diese Probleme im Benchmark:
- **Spezifisch für [KONKURRENT_NAME]:** Probleme, die selten in der Branche vorkommen
- **Branchenweite Herausforderungen:** Häufig bei allen Marktteilnehmern
- **Von anderen gelöst:** Probleme, die Wettbewerber von [KONKURRENT_NAME] behoben haben

## OUTPUT-FORMAT

### 1. MANAGEMENT-ZUSAMMENFASSUNG (max. 150 Wörter)
- Kernerkenntnis: Was ist ihre größte Schwachstelle?
- Strategische Implikation: Welche Chance entsteht daraus?
- Vertrauensniveau: Hoch/Mittel/Niedrig (basierend auf Datenqualität)

### 2. QUANTIFIZIERTE BESCHWERDEÜBERSICHT
```
Analysierte Bewertungen gesamt: [X]
Negativbewertungsrate: [X%]
Zeitrahmen: [Daten]
Hauptquellen: [Top 3 Plattformen]

Top 5 Problembereiche nach Häufigkeit:
1. [Problem] - [XX%] der Beschwerden - [Schweregrad: H/M/N]
2. [Problem] - [XX%] der Beschwerden - [Schweregrad: H/M/N]
3. [Problem] - [XX%] der Beschwerden - [Schweregrad: H/M/N]
4. [Problem] - [XX%] der Beschwerden - [Schweregrad: H/M/N]
5. [Problem] - [XX%] der Beschwerden - [Schweregrad: H/M/N]
```

### 3. DETAILLIERTE AUFSCHLÜSSELUNG NACH KATEGORIE
Für jede Kategorie:
- **Problem-Cluster:** Gruppe verwandter Beschwerden
- **Häufigkeit:** Prozentsatz + absolute Zahlen
- **Echte Kundenzitate:** 2-3 wörtliche Beispiele (anonymisiert)
- **Impact-Score:** Bewerte 1-10 basierend auf Schweregrad × Häufigkeit
- **Trend:** ↑ Steigend / → Stabil / ↓ Abnehmend

### 4. SCHWACHSTELLENMATRIX
Erstelle eine 2×2-Matrix-Klassifizierung:

**HOHE HÄUFIGKEIT + HOHER SCHWEREGRAD** → Kritische Schwachstellen (nutze diese aus)
**HOHE HÄUFIGKEIT + NIEDRIGER SCHWEREGRAD** → Kleine Ärgernisse (schnelle Erfolge)
**NIEDRIGE HÄUFIGKEIT + HOHER SCHWEREGRAD** → Sonderfälle (beobachten)
**NIEDRIGE HÄUFIGKEIT + NIEDRIGER SCHWEREGRAD** → Ignorieren

### 5. WETTBEWERBLICHE POSITIONIERUNGSCHANCEN
Liefere für jede kritische Schwachstelle:

**Schwachstelle:** [Problem des Konkurrenten]
**Deine Chance:** [Wie du dich dagegen positionieren kannst]
**Botschaft:** [Kundenbezogene Aussage, die du treffen könntest]
**Benötigte Beweise:** [Was du beweisen müsstest]
**Schwierigkeit:** Schneller Erfolg / Mittlerer Aufwand / Große Investition

### 6. WARNZEICHEN & EINSCHRÄNKUNGEN
- **Datenlücken:** Was nicht verifiziert werden konnte
- **Verzerrungsbedenken:** Muster, die auf Bewertungsmanipulation hindeuten
- **Stichprobenlimitierungen:** Unterrepräsentierte Segmente
- **Zeitliche Faktoren:** Saisonalität oder einmalige Ereignisse, die Bewertungen beeinflussen

### 7. EMPFOHLENE NÄCHSTE SCHRITTE
Priorisierte Aktionsliste (1-5 Punkte) zur Nutzung dieser Erkenntnisse.

## VALIDIERUNGS-CHECKLISTE
Bestätige vor Ausgabe des Ergebnisses:
- [ ] Mindestens 100 Bewertungen analysiert
- [ ] Quantitative Daten für Top-Beschwerden
- [ ] Quellen zur Verifizierung zitiert
- [ ] Sowohl Branchenkontext als auch einzigartige Probleme identifiziert
- [ ] Umsetzbare Empfehlungen enthalten
- [ ] Vertrauensniveaus klar angegeben

---

**Beginne jetzt mit der Analyse. Falls du Klärungsbedarf zu [KONKURRENT_NAME], [PRODUKT_DIENSTLEISTUNG_TYP] oder [KUNDENSEGMENT] hast, frage vor der Durchführung nach.**


---
---

# 📋 VERWENDUNGSZWECK & ANWENDUNGSBEISPIEL

## **Wofür wird dieser Prompt verwendet?**

Dieser Prompt ist ein professionelles Werkzeug für **Wettbewerbsanalyse und strategische Marktpositionierung**. Er wird eingesetzt, um:

✅ **Schwachstellen von Konkurrenten** systematisch zu identifizieren  
✅ **Produktentwicklungsprioritäten** datenbasiert festzulegen  
✅ **Marketing-Botschaften** zu schärfen ("Wir lösen das Problem X, das Konkurrent Y ignoriert")  
✅ **Marktlücken** und Differenzierungschancen zu entdecken  
✅ **Investitionsentscheidungen** zu fundieren (wo lohnt sich Innovation?)  
✅ **Sales-Argumente** mit echten Kundenproblemen der Konkurrenz zu unterfüttern

**Zielgruppen:** Produktmanager, Marketing-Strategen, Gründer, Business-Analysten, Wettbewerbsintelligenz-Teams

---

## **🎯 PRAKTISCHES BEISPIEL**

**Szenario:** Du startest einen neuen Projektmanagement-Software-Service und willst dich gegen den Marktführer "Asana" positionieren.

**Prompt-Befüllung:**
```
Wettbewerber: Asana
Branche/Kategorie: Cloud-basierte Projektmanagement-Software
Zielgruppe: Kleine bis mittelständische Unternehmen (10-200 Mitarbeiter), 
            Marketing-Teams und Kreativ-Agenturen
Geschäftsziel: Konkurrenzprodukt mit Fokus auf Benutzerfreundlichkeit 
               und transparente Preisgestaltung launchen
```

**Erwartetes Ergebnis (Auszug):**

```
MANAGEMENT-ZUSAMMENFASSUNG:
Asanas größte Schwachstelle ist die "Feature-Überladung" bei gleichzeitig 
komplexer Navigation. 42% der negativen Bewertungen kritisieren die steile 
Lernkurve und verwirrende Benutzeroberfläche. Dies ist einzigartig für Asana 
– Konkurrenten wie Monday.com haben simplere Onboarding-Prozesse entwickelt.

CHANCE: Positionierung als "das einfache Projektmanagement-Tool, das dein 
Team ohne Schulung nutzen kann".

TOP 5 PROBLEMBEREICHE:
1. Zu komplexe Benutzeroberfläche - 42% - Schweregrad: HOCH
2. Intransparente Preisgestaltung bei Team-Upgrades - 28% - Schweregrad: HOCH
3. Langsame mobile App - 18% - Schweregrad: MITTEL
4. Fehlende native Zeiterfassung - 15% - Schweregrad: MITTEL
5. Schwacher Kundenservice bei technischen Problemen - 12% - Schweregrad: HOCH

POSITIONIERUNGSCHANCE:
Schwachstelle: "Neue Teammitglieder brauchen 2-3 Wochen Training"
Deine Chance: "Onboarding in 5 Minuten" als Kernversprechen
Botschaft: "Projektmanagement, das dein Team sofort versteht – 
           keine Schulung notwendig"
Benötigte Beweise: Beta-Tester-Testimonials, Video-Demos, 
                   Durchschnittliche Time-to-first-Task-Metrik
Schwierigkeit: Mittlerer Aufwand (intuitive UX ist lösbar, 
               aber erfordert gutes Design)
```

**Business-Impact:**  
Mit diesen Erkenntnissen kannst du dein MVP auf die 3 kritischsten Punkte fokussieren, deine Landing-Page mit klaren Differenzierungsargumenten aufbauen und potenzielle Investoren mit datengestützten Marktchancen überzeugen.
