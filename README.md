# Projektbericht
## Kontext und Beschreibung des publizierten Vokabulars

Das mit **SKOHub Pages** publizierte kontrollierte Vokabular **„Berufsrollen früher Archäologen“** wurde im Projekt  
**„Spuren archäologischer Wissensgenerierung. Propylaeum-VITAE – ein Instrument für die Wissenschaftsgeschichte der Archäologie“** entwickelt.

Es ist Teil einer Sammlung von Nachschlagelisten, die in **Propylaeum-VITAE** für die Beschreibung der Lebensläufe eingesetzt werden:  
<https://www.propylaeum.de/themen/propylaeum-vitae>

Die in Propylaeum-VITAE verwendeten Vokabulare sollen sukzessive mit **SKOS** publiziert werden.  
Die hier vorgelegte, bislang umfangreichste Liste enthält **Berufsrollen von Personen aus einer Zeit, in der die Archäologie noch nicht professionalisiert war**.  
Das Vokabular umfasst insgesamt **51 Einträge**.

### Verwendete Properties

- **ConceptScheme**
  - `dct:title`
  - `dct:creator`
  - `dct:created`
  - `dct:license`

- **TopConcept / Konzepte**
  - `skos:prefLabel`
  - `skos:altLabel`
  - `dct:description`
  - `skos:definition`
  - `skos:note`
  - `skos:broader`
  - `skos:narrower`

Das Concept Scheme bietet perspektivisch die Möglichkeit, das **komplette Vokabular**, wie es in Propylaeum-VITAE verwendet wird, abzubilden.

Die verwendete Sprache ist **Deutsch**; perspektivisch ist eine **Erweiterung um Englisch** geplant.

---

## Vorbereiten des Vokabulars

Die verwendeten Nachschlagelisten wurden vom Projektteam **Propylaeum-VITAE** in einer **Excel-Tabelle mit mehreren Arbeitsmappen** vorgehalten.  
Sie enthielten ausschließlich die Begriffe, jedoch **keine Definitionen oder Hierarchien**.

Für das kleine Projekt im **MALIS-Studiengang** wurde die Liste der Berufsrollen extrahiert und um folgende **SKOS-Properties** ergänzt:

- `skos:prefLabel`
- `skos:altLabel`
- `skos:definition`
- `skos:note`
- `skos:broader`
- `skos:narrower`

