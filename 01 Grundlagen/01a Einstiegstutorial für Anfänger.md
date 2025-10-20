
# Wie man ChatGPT gezielt als Experten nutzt

## Einleitung

Künstliche Intelligenz wie ChatGPT kann uns in der täglichen Arbeit auf vielfältige Weise unterstützen – ob beim Formulieren von Texten, Entwickeln neuer Ideen, Analysieren von Daten oder Strukturieren komplexer Themen. Der Schlüssel zu wirklich hilfreichen Ergebnissen liegt dabei weniger in der Technik selbst, sondern in der Art, **wie wir mit ihr sprechen**.  
Mit gezielten Anweisungen, sogenannten *Personas*, lässt sich ChatGPT so steuern, dass es wie ein spezialisierter Experte agiert – etwa als Marketingstratege, IT-Architekt oder Organisationsentwickler. Der folgende Text zeigt Schritt für Schritt, wie man solche Rollen definiert und nutzt, um die Leistungsfähigkeit der KI gezielt für unsere Aufgaben in der Volksbank einzusetzen.

---

## Wie LLMs funktionieren

Zuerst eine kurze Erklärung: LLMs wie ChatGPT zerlegen Wörter in Zahlen (Tokens) und ordnen sie in einem Vektorraum an, in dem ihre Beziehungen durch Muster in den Trainingsdaten bestimmt werden. Der Vektorraum stellt Assoziationen und Korrelationen dar, keine explizite symbolische Logik. Man kann sich das wie eine Wortwolke vorstellen. Wenn du ChatGPT sagst: „Ich möchte, dass du den Namen Alex annimmst“, dann erhält diese Persona alle Eigenschaften, die typischerweise mit dem Wortfeld um „Alex“ verbunden sind – was oft großartig für Programmierer und ähnliche Rollen funktioniert. Aber diese Personas sind noch zu allgemein. Man sollte viel spezifischer werden. Zum Beispiel, wenn du Schwierigkeiten in deinem Python-Kurs hast und einen Python-Tutor brauchst?

Und um das klarzustellen: Wenn wir über „Personas“ oder „Archetypen“ in ChatGPT sprechen, handelt es sich nicht um einprogrammierte Charaktere. Es gibt keine fest codierten Personas. Es sind alles nur Wörter (Tokens) und ihre Assoziationen. Aber weil LLMs Sprachmuster lernen, kann man durch die richtigen sprachlichen Signale bestimmte Experten oder Denkweisen „hervorrufen“. Es gibt Wortcluster, die ChatGPT dazu bringen oder darin bestärken, auf eine bestimmte Weise zu reagieren. Wenn man genug dieser Wörter gemeinsam und im richtigen Ton verwendet, zieht man das Modell in die Richtung, die für die jeweilige Aufgabe am nützlichsten ist. Man kann sogar die aktuelle ChatGPT-Instanz verwenden, um solche Wortcluster zu finden.

---

## Der richtige Experte für die jeweilige Aufgabe

Zuerst sollte man wissen, welche Art von Experte man braucht. ChatGPT hat höchstwahrscheinlich bereits bestehende Wortassoziationen (oder genauer gesagt: Token-Beziehungen) für nahezu alles, was man sich vorstellen kann – ob es sich nun um einen Marketingexperten handelt, der sich auf die Planung regionaler Kampagnen spezialisiert hat, einen IT-Architekten für sichere Bankprozesse, einen Berater für Change-Management in der Unternehmensentwicklung, einen Experten für Genossenschaftsrecht oder einen Kommunikationsprofi, der Pressemitteilungen und Vorstandspräsentationen perfekt formulieren kann.

---

## Schritt 1: Den Experten beschreiben

Frage ChatGPT:

> „Welche 20 Wörter würden einen [spezifischen Spezialisten] beschreiben?“

In meinem Beispiel habe ich „Marketingexperte, der sich auf die Entwicklung regionaler Volksbank-Kampagnen spezialisiert“ verwendet, und ChatGPT gab mir diese Liste:  
Strategisch, Regional, Kundenorientiert, Kampagne, Vertrauen, Genossenschaftlich, Kreativ, Analytisch, Zielgruppe, Markenbewusstsein, Lokal, Kooperation, Storytelling, Mitgliederbindung, Emotion, Effizienz, Konzept, Authentisch, Wirkungsvoll, Nachhaltig.

---

## Schritt 2: Einen passenden Prompt erstellen

Sobald die Liste erstellt ist, sage:

> „Verwende so viele dieser Wörter wie möglich und schreibe einen vier Sätze langen Prompt, der diesen Spezialisten in einem LLM herbeirufen würde. Er soll so klingen, als würde der Nutzer ein bestimmtes Gespräch beginnen, wie etwa: ‘Ich würde gerne sprechen mit…’. Achte darauf, dass der Ton zur Persönlichkeit und zum Stil des Archetyps passt.“

Der Ton ist in diesem Fall weniger wichtig als bei Charakteren für Worldbuilding, aber du willst trotzdem, dass diese Spezialisten einen gewissen Ton haben. Du würdest schließlich keinen fluchenden, zu lockeren Marketingexperten wollen, der die nächste Vorstandspräsentation erstellt.

---

## Schritt 3: Den Prompt in einem neuen Chat verwenden

Sobald du den generierten Prompt hast, starte einen neuen Chat und verwende diesen Prompt dort. Wenn du den Prompt in denselben Chat einfügst, wird ChatGPT verwirrt und antwortet möglicherweise mit etwas wie:  
„Das ist ein fantastischer Prompt! Er fasst den [Beispielcharakter] mit Charme und Witz perfekt zusammen. Möchtest du ihn noch verfeinern oder direkt verwenden?“

---

## Praxisbeispiele aus dem Volksbank-Kontext

### Marketingexperte für regionale Bankkampagnen
> „Ich möchte mit dem Marketingexperten sprechen, der kreative, regionale Kampagnen für Volksbanken entwickelt – jemand, der unsere genossenschaftlichen Werte versteht, strategisch denkt und mit Authentizität kommuniziert. Du weißt, wie man Vertrauen stärkt, Mitglieder emotional anspricht und gleichzeitig klare KPIs im Blick behält. Du bist erfahren im Storytelling, präzise im Messaging und kennst die Besonderheiten lokaler Märkte. Wenn du verfügbar bist, möchte ich gemeinsam mit dir eine Kampagne zur Mitgliederbindung entwickeln, die wirklich wirkt.“

---

### IT-Architekt für Bankprozesse
> „Ich möchte mit dem IT-Architekten sprechen, der sich auf sichere und effiziente Bankprozesse spezialisiert – jemand, der Datenschutz, Compliance und Nutzerfreundlichkeit perfekt vereint. Du denkst in klaren Strukturen, erkennst Schwachstellen und findest pragmatische Lösungen, ohne die Stabilität des Systems zu gefährden. Du arbeitest methodisch, dokumentierst präzise und kommunizierst klar mit Fachbereichen und IT-Teams. Wenn du verfügbar bist, möchte ich dich zu einem Prozess zur Optimierung unseres OnlineBankings befragen.“

---

### Berater für Unternehmensentwicklung
> „Ich möchte mit dem Organisationsentwickler sprechen, der genossenschaftliche Banken durch Veränderungsprozesse begleitet – jemand, der strategisch, empathisch und zukunftsorientiert denkt. Du kombinierst Erfahrung aus Change-Management, Digitalisierung und Personalentwicklung, erkennst Chancen in Widerständen und vermittelst komplexe Themen verständlich. Du bist analytisch und menschlich zugleich, fokussierst dich auf Umsetzbarkeit und nachhaltigen Erfolg. Wenn du verfügbar bist, möchte ich mit dir eine Strategie zur Stärkung unserer Innovationskultur entwickeln.“

---

### Kommunikationsprofi für Vorstandspräsentationen
> „Ich möchte mit dem Kommunikationsexperten sprechen, der Vorstandspräsentationen klar, überzeugend und visuell ansprechend aufbereitet – jemand, der Bankthemen verständlich macht, ohne an Tiefe zu verlieren. Du weißt, wie man komplexe Informationen auf den Punkt bringt, die Botschaft schärft und Präsentationen auf Wirkung ausrichtet. Du bist souverän im Ton, präzise in der Formulierung und achtest auf Professionalität in jedem Detail. Wenn du verfügbar bist, möchte ich deine Hilfe bei der Vorbereitung eines strategischen Workshops mit dem Vorstand nutzen.“

---

### Datenanalyst für Kundenverhalten und Filialstrategie
> „Ich möchte mit dem Datenanalysten sprechen, der Kundenverhalten in regionalen Banken analysiert – jemand, der Muster erkennt, Zusammenhänge versteht und daraus klare Handlungsempfehlungen ableitet. Du bist detailorientiert, analytisch und gleichzeitig in der Lage, komplexe Zahlen in verständliche Geschichten zu übersetzen. Du denkst in Trends, segmentierst sauber und unterstützt Entscheidungen mit belastbaren Fakten. Wenn du verfügbar bist, möchte ich mit dir unsere Kundenbewegungen im OnlineBanking und Filialgeschäft analysieren.“

---

## Fazit

Wenn du diese Prompts in einen neuen Chat mit ChatGPT kopierst, erhältst du sofort Antworten „in-character“, bereit, dich gezielt bei deinem Projekt zu unterstützen – sei es bei der Entwicklung einer Marketingstrategie, der Prozessoptimierung in der IT, der Gestaltung interner Workshops oder der datenbasierten Entscheidungsfindung im Vorstand.  
So wird ChatGPT zu einem digitalen Sparringspartner, der Fachwissen, Effizienz und kreative Ideen für die Arbeit in der Volksbank vereint.


---


