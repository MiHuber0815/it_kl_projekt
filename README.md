# Projektbericht
## Kontext und Beschreibung des publizierten Vokabulars

Das mit **SKOHub Pages** publizierte kontrollierte Vokabular **„Berufsrollen früher Archäologen“** wurde im Projekt  
**„Spuren archäologischer Wissensgenerierung. Propylaeum-VITAE – ein Instrument für die Wissenschaftsgeschichte der Archäologie“** entwickelt.

Es ist Teil einer Sammlung von Nachschlagelisten, die in **Propylaeum-VITAE** für die Beschreibung der Lebensläufe eingesetzt werden:  
<https://www.propylaeum.de/themen/propylaeum-vitae>

Die in Propylaeum-VITAE verwendeten Vokabulare sollen sukzessive mit **SKOS** publiziert werden.  
Die hier vorgelegte, bislang umfangreichste Liste enthält Berufsrollen von Personen aus einer Zeit, in der die Archäologie noch nicht professionalisiert war.  
Das Vokabular umfasst insgesamt 51 Einträge.

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
Durch eine Publikation des Vokabulars via Skohub-Pages wird den Vorgaben guter wissenschaftlicher Praxis gefolgt, seine Forschungsergebnisse der Öffentlichkeit zur Verfügung zu stellen. Damit wird gleichzeitig ein Diskurs in der Fachcommunity möglich um fehlende oder unzureichende Definitionen zu verbessern und zu ergänzen. Die Publikation ermöglich potentiell eine Verknüpfung mit anderen publizierten Vokabularen mit Hilfe von [[SKOS Mapping|https://www.w3.org/2004/02/skos/mapping/spec/2004-11-11.html]].

Die redaktionelle Hoheit liegt beim Leipniz Institut für Archäologie. Die Finalisierung des Vokabular muss in Rücksprache mit den dort zuständigen Stellen getätigt werden. Aus diesem Grund und um Redundanzen zu vermeiden entschied sich das Projektteam gegen die Festlegung auf einen persistenten Idcentifier. 

---

## Vorbereiten des Vokabulars - Von Tabelle zu Turtle


Die verwendeten Nachschlagelisten wurden vom Projektteam **Propylaeum-VITAE** in einer Excel-Tabelle mit mehreren Arbeitsmappen vorgehalten,
die zur Weiterverarbeitung in CSV-Datein umgewandelt wurden.
Sie enthielten ausschließlich die Begriffe, jedoch keine Definitionen oder Hierarchien.

Für das kleine Projekt im **MALIS-Studiengang** wurde die Liste der Berufsrollen extrahiert und um folgende **SKOS-Properties** ergänzt:

- `skos:prefLabel`
- `skos:altLabel`
- `skos:definition`
- `skos:note`
- `skos:broader`
- `skos:narrower`

Für die Umwandlung von Tabelle zu skos-Vokabular im [[Turtleformat|https://www.w3.org/TR/2014/REC-turtle-20140225/]] wurde auf Python, spezifischer, ein [[Jupyter-notebook|https://github.com/MiHuber0815/it_kl_projekt/blob/main/prep_stuff/prep_csv.ipynb]] zurückgegriffen. Die Dokumentation des Codes ist ebenfalls dort zu finden.
Für die Transformation mit Python fiel die Entscheidung für die Verwendung der Templatesprache [[jinja|https://jinja.palletsprojects.com/en/stable/templates/]] in der Erwartung, dass die Menschenlesbarkeit dadurch eher erhalten wird als die ebenfalls in Erwägung gezogene Realisierung mit Hilfe von [[rdfLib|https://rdflib.readthedocs.io/en/stable/]]. RdfLibs technische Umsetzung hat zur Folge, dass dort modellierte Graphe unsortiert gespeichert werden und es zusätzlichen Aufwand bedeuten würde, die Knoten vor der Serialisierung zu sortieren. Die Verwendung einer Templatesprache versprach mehr Kontrolle über die Formatierung des Outputs.

## Fazit

Anhand des Projekt konnte das Projektteam nicht nur die im vorherigen Semester erworbene Programmierfähigkeiten festigen und ausbauen, sondern beschäftigte sich auch mit den Konzepten von Linked Open Data, insbesondere mit SKOS und dem Format Turtle.
Die Umsetzung wurde etwas schwieriger, durch fehlende oder zumindest nicht explizite Dokumentation welche Eigenschaften auf welcher Ebene (Concept Scheme, Top Concept, Concept) von Skohub-Pages gerendert wird. Letzteres konnte in Rücksprache mit den Dozierenden geklärt werden. 
