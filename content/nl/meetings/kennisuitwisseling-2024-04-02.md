+++
date = '2024-04-10T13:07:34+02:00'
draft = false
title = 'HTR Kennisuitwisseling 2 april 2024'
[menus]
  [menus.main]
    parent = 'Bijeenkomsten'
    weight = 20
+++

De zesde bijeenkomst op 2 april 2024

### Bijeenkomst

Datum: 2 april 2024
Tijd: 15:00-17:00
Locatie: NIOD Grote Vergaderzaal, 1e verdieping, Herengracht 380, Amsterdam

### Agenda

- Katrien Depuydt - Fouten en de evaluatie daarvan
- Annemieke Romein - Toer langs HTR projecten
- Ronde tafel: gedeelde problemen/uitdagingen

<!--more-->

### Aanwezig
- Katrien Depuydt 
- Jesse de Does 
- Roland de Bonth 
- Erik Tjong Kim Sang 
- Carsten Schnober 
- Rutger van Koert 
- Stefan Klut
- Ger Dijktra
- Kay Pepping 
- Pauline van den Heuvel 
- Milan van Lange 
- Marijn Koolen
- (een aantal namen vergeten op te schrijen)

### Thema: Fouten en de evaluatie daarvan

Hoe komen we erachter wat er níet goed gaat met HTR? Hoe werken we vanuit daar aan verbetering? 

### Katrien Depuydt (INT) - noden en problemen in OCR en HTR evaluatie

- Courantencorpus voor evidentie van woorden en woordvoorkomens
- OCR fouten zijn een groot probleem
- Belangrijk: documentsegmentatie (artikelen in kranten)
- issues: duplicaten, geen coordinaten

- Managementomgeving voor progressie (alternatief voor Vele Handen?)
    - in house gemaakt, maar kan hergebruikt worden (neem contact op)
- IMPACT project (Improving ACces to Text)
- Vergelijking van Transkribus, PyLaia, Calamari, Loghi en Tesseract
    - evaluatie-tools: intern per tool, Dinglehopper (https://github.com/qurator-spk/dinglehopper)
- Digitization Hub
    - voor algemene kennis voor HTR vanuit verschillende projecten
    - mensen kunnen rapporten en tutorials indienen en links toevoegen naar eigen data
- Literatuur:
    - Phillip Benjamin Ströbel, Martin Volk, Simon Clematide, Raphael Schwitter, Tobias Hodel, David Schoch:  [Evaluation of HTR models without Ground Truth Material](https://aclanthology.org/2022.lrec-1.467.pdf)
    - Christian Clausner, Stefan Pletschacher, Apostolos Antonacopoulos: [Flexible character accuracy measure for reading-order-independentc evaluation](https://www.sciencedirect.com/science/article/pii/S0167865520300416)


Vragen:
- kunnen tags overlappen? Hoe ga je hier mee om in training?
- Hoe kies je modellen en methoden voor HTR en layout?
- Hoe kies je criteria voor Ground Truth
- Hoe evalueer je reading order?
- Zijn de evaluatie-vragen van de onderzoeker of databeheerder hetzelfde als die van de HTR trainer?
- Hoe kun je regio-evaluatie verbeteren t.o.v. pixel-overlap?
    - voor alle regelparen in de GT aangeven of ze in dezelfde regio zitten, zelfde voor regelparen in de HTR output -> Het gaat om correctheid van regelclustering (maar voor regio's naast elkaar is dit problematischer dan voor regio's onder elkaar)
    - Suggestie van Jesse: **in GT tekstregio's maken door baselines te groeperen.**


### Annemieke Romein - Toer langs HTR projecten

Toer langs HTR projecten
- Law and Order (Ugent)
- Entalged Histories (KB)
    - complexere layout, minder voorspelbaar, marginalia en meerdere kolommen
- A Game of Thrones (Huygens)
- Samenwerking met PlanetAI/Freiburg/Bern
- Andere projecten
- Poster van recent werk: [Evaluating State‐of‐the‐Art Handwritten Text Recognition (HTR) Engines; with Large Language Models (LLMs) for Historical Document Digitisation](https://zenodo.org/records/8102666)

- In sommige project zijn CER en WER niet leidend, het gaat om begrijpelijke/doorzoekbare tekst
- In huidig project is layout leidend
- evaluatie en vormen van transcriberen: hyper-diplomatisch, diplomatisch of vrijere transcriptie (ander perspectief op wat/hoe geëvalueerd moet worden)

Opmerkingen:
- [OCR-D](https://ocr-d.de/en/gt-guidelines/trans/) voor verschillende (niveau's) transcriptie-methoden

Vragen:
- handmatige corrigeren/pagina's herzien: wat wordt gecorrigeerd? Tekst? Of ook layout?
    - voornamelijk fouten in regelbegin en -einde (baselines)
    - kwam vooral door vervaging van de tekst aan begin en eind
- Hoe heb je regelvolgorde geëvalueerd? Is dat in de ground truth aangegeven? Of is dat handmatig gedaan.
- Trainen van fields modellen kon toch al? 
    - Ja, kon middels PyLaia, maar trefzekerheid was laag. Met fields models gaat het aanzienlijk beter.
- Wat is het verschil tussen regions en fields?
    - een fields model gebruikt de text regions



### Ronde tafel: gedeelde problemen/uitdagingen


Behoefte aan gezamenlijke concordans voor documenttypes en teksttypes:
- e.g. header of titel
- hierarchisch model:
    - generieke types: 
        - lopende tekst/alinea/paragraaf versus pre-ambule/resolutie
        - header versus titel
- Draft document: https://docs.google.com/document/d/1M3d9_QJgKih8x8SQNMQYTHg2CydBBlP25YAr6Opu6qo/edit
- Delen via DH^2


Vrijwilligers:
- complexe instructies zijn altijd problematisch, veel curatie nodig 
    - maar kan ook door specifieke vrijwilligers te vragen en te begeleiden
- Pauline: er is vaak behoefte aan een fysieke plek om bij elkaar te komen

Voor een andere keer:
- Muriël Bouman - Onleesbare handschriften in 20e eeuwse dagboeken (worst case scenario uit de praktijk, afgezegd)
