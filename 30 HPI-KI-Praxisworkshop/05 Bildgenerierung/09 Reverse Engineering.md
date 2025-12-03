# Anleitung: Bilder analysieren wie ein Profi mit dem Reverse Engineering Prompt

Herzlich willkommen! Dieses Tutorial zeigt Ihnen, wie Sie mit einem speziellen KI-Prompt Bilder analysieren können, um deren Stil, Aufbau und "Geheimnisse" zu entschlüsseln. Das ist besonders nützlich, um professionelle und konsistente Bilder für Coherent zu erstellen.

---

## 1. Was ist "Reverse Engineering" für Bilder?

Stellen Sie sich vor, Sie sehen ein beeindruckendes Foto – zum Beispiel von einem Konkurrenzprodukt oder aus einer erfolgreichen Werbekampagne – und fragen sich: "Wie wurde dieses Bild gemacht? Welchen Stil hat es? Welche Kameraeinstellungen wurden verwendet?"

Genau hier setzt der **Reverse Engineering Prompt** an.

Anstatt der KI zu sagen, was sie *erstellen* soll, geben Sie ihr ein **bestehendes Bild** und den Auftrag, es zu **analysieren und zu zerlegen**. Das Ergebnis ist eine extrem detaillierte Beschreibung des Bildes, die Sie wiederum nutzen können, um ähnliche Bilder selbst zu erstellen.

**Kurz gesagt: Sie verwandeln ein Bild zurück in einen perfekten Prompt.**

---

## 2. Warum ist das nützlich für Coherent?

Dieser Prozess ist ein mächtiges Werkzeug für verschiedene Abteilungen:

| Abteilung | Anwendungsfall | Nutzen |
| :--- | :--- | :--- |
| **Marketing** | Analyse von Wettbewerber-Bildern oder erfolgreichen Stockfotos. | Verstehen, was ein Bild erfolgreich macht (Licht, Farbe, Komposition) und diesen Stil für eigene Kampagnen adaptieren. |
| **Engineering / F&E** | Dokumentation von Laboraufbauten oder Prototypen. | Erstellen von präzisen, textbasierten Beschreibungen für technische Dokumente, Patente oder Präsentationen. |
| **Branding & Design** | Sicherstellung eines konsistenten visuellen Stils. | Analyse von bestehenden Coherent-Bildern, um einen "Master-Prompt" zu erstellen, der den offiziellen Coherent-Look definiert. |
| **Vertrieb** | Erstellung von überzeugenden Präsentations-Bildern. | Analyse von Bildern, die bei Kunden gut ankommen, um gezielt ähnliche, wirkungsvolle Visuals zu erstellen. |

---

## 3. Schritt-für-Schritt-Anleitung für KI-Anfänger

So einfach wenden Sie den Prozess an:

### Schritt 1: Den Master-Prompt kopieren

Öffnen Sie die Bilddatei, die den Prompt enthält, und kopieren Sie den **gesamten Text** des Reverse Engineering Prompts. Es ist ein langer, strukturierter Text, der der KI genaue Anweisungen gibt.

### Schritt 2: KI-Assistenten vorbereiten

Öffnen Sie einen KI-Assistenten, der Bild-Uploads unterstützt (z.B. ChatGPT-4, Claude 3 Opus).

### Schritt 3: Prompt einfügen & Bild hochladen

1.  Fügen Sie den kopierten **Master-Prompt** in das Chatfenster ein.
2.  **Laden Sie das Bild hoch**, das Sie analysieren möchten. Fügen Sie es direkt nach dem Prompt in dieselbe Nachricht ein.

Ihre Eingabe sollte also so aussehen:

> [Kompletter Reverse Engineering Prompt Text]
> 
> [Hier das Bild einfügen/hochladen]

### Schritt 4: Analyse starten und Ergebnis prüfen

Senden Sie die Nachricht ab. Die KI wird nun das Bild anhand der Anweisungen analysieren und Ihnen zwei Dinge liefern:

1.  **Eine detaillierte JSON-Analyse:** Eine strukturierte Aufschlüsselung des Bildes in Kategorien wie `subject`, `environment`, `style`, `composition`, `lighting` etc.
2.  **Einen finalen, optimierten Prompt:** Einen zusammenhängenden, langen Prompt, den Sie direkt in einem KI-Bildgenerator (wie Midjourney, DALL-E 3 oder Stable Diffusion) verwenden können, um ein Bild im selben Stil zu erzeugen.

---

## 4. Praxisbeispiele für Coherent

### Beispiel 1: Analyse eines Wettbewerber-Produktfotos (Marketing)

**Ziel:** Sie möchten verstehen, warum das Produktfoto eines Wettbewerbers so hochwertig aussieht, um Ihre eigenen Produktbilder zu verbessern.

1.  **Input:** Sie laden ein professionelles Foto eines Lasersystems von einem Wettbewerber hoch.
2.  **Analyse-Ergebnis (Auszug aus dem JSON):**
    ```json
    {
      "style": "cinematic product photography, dramatic lighting, high-contrast",
      "composition": "low-angle shot, rule of thirds",
      "lighting": "key light from the side, subtle blue rim light, creating sharp reflections on metal surfaces",
      "mood": "high-tech, powerful, precise, innovative"
    }
    ```
3.  **Finaler Prompt (Auszug):**
    > "Cinematic product photography of a futuristic laser system, low-angle shot, placed according to the rule of thirds. Dramatic lighting with a strong key light from the side and a subtle blue rim light, creating sharp reflections on the brushed metal texture..."

**Nutzen:** Ihr Marketing-Team hat jetzt eine genaue "Rezeptur", um eigene Produktfotos mit einer ähnlich professionellen und wirkungsvollen Ästhetik zu erstellen.

### Beispiel 2: Dokumentation eines Laboraufbaus (Engineering)

**Ziel:** Ein komplexer Versuchsaufbau im Labor soll für eine technische Dokumentation präzise beschrieben werden.

1.  **Input:** Sie laden ein Foto Ihres optischen Tisches mit Lasern, Linsen und Fasern hoch.
2.  **Analyse-Ergebnis (Auszug aus dem JSON):**
    ```json
    {
      "subject": "A complex optical experiment setup on a lab bench",
      "elements": ["laser modules", "lenses on mounts", "mirrors", "fiber optic cables", "oscilloscope"],
      "composition": "top-down perspective, slightly angled, cluttered but organized",
      "lighting": "bright, even, neutral laboratory fluorescent lighting"
    }
    ```
3.  **Finaler Prompt (Auszug):**
    > "Top-down photograph of a complex optical experiment on a lab bench. The scene is filled with various technical components like laser modules, lenses on mounts, mirrors, and a network of colorful fiber optic cables..."

**Nutzen:** Sie erhalten eine perfekte textuelle Beschreibung, die Sie direkt in Ihre Dokumentation, einen Konferenzbeitrag oder eine Präsentation einfügen können.

---

## 5. Wichtige Hinweise

-   **Datenschutz:** Laden Sie keine Bilder hoch, die vertrauliche Coherent-Technologie, unveröffentlichte Prototypen oder Personen ohne deren Einwilligung zeigen.
-   **Urheberrecht:** Nutzen Sie diesen Prozess, um Stile zu lernen und sich inspirieren zu lassen – nicht, um urheberrechtlich geschützte Bilder 1:1 zu kopieren.
-   **Qualität:** Je besser die Qualität des Eingangsbildes, desto präziser und nützlicher ist die Analyse der KI.

Mit diesem Werkzeug können Sie die Bildsprache Ihrer Branche meisterhaft entschlüsseln und für Coherents Erfolg nutzen. Viel Spaß beim Ausprobieren!

---

**@ 2025 - HPI KI Workshops | Tutorials**
