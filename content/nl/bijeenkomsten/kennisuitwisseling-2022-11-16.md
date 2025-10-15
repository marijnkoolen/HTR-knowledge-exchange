+++
date = '2022-11-17T13:07:34+02:00'
draft = false
title = 'HTR Kennisuitwisseling 16 november 2022'
[menus]
  [menus.main]
    parent = 'Bijeenkomsten'
    weight = 20
+++

De eerste bijeenkomst op 16 november 2022


## Bijeenkomst

Datum: 16 november 2022
Tijd: 13:00-15:00
Locatie: Spinhuis zaal 2.18, Oudezijds Achterburgwal 185, Amsterdam

## Agenda

- kennismaking
- intro
- discussie
- hoe verder?

<!--more-->

**Aanwezig**

- Rick Companje (Utrechts Archief)
- Mirjam Cuper (KB)
- Rik Hoekstra (HuC)
- Liesbeth Keijser (Nationaal Archief)
- Rutger van Koert (HuC)
- Marijn Koolen (HuC)
- Milan van Lange (NIOD)
- Annelies van Nispen (NIOD)
- Ismee Tames (NIOD)
- Leon van Wissen (UvA)


## Discussiepunten

- structuur aanbrengen/toevoegen aan grote hoeveelheden scans en OCR/HTR output (transcripten)
    - Impliceert bestaan van logische structuur in bronnen --> hoe doe je dit bij bijvoorbeeld gevarieerde collecties egodocumenten?
    - classificatie-algoritmen (trainen)
        - op basis van visuele of tekstuele aspecten (verschillende benaderingen)
    - Document resolution (oorlog voor de rechter, oorlogsbrievenproject)
    - Hoe doe je dit als er geen GroundTruth is? En wat is GT eigenlijk? (en wie bepaalt dat?)
        - Open beginnen, of beginnen met metadata als info voor classifier om op te trainen.
- categoriseren van 'document genres' voor pagina's 
    - op basis van visuele aspecten
    - op basis van tekstuele aspecten
    - combinatie van beide
    - document resolution (welke pagina's zijn onderdeel van 1 document?)
    - 
- categoriseren van layout elementen en structuren in pagina's/documenten
    - b.v. deels getypte/deels handgeschreven formulieren
    - standaard elementen/hierarchie elementen
- trainen van herkenners/classifiers hiervoor
    - Transkribus: baseline training?
    - training sturen met metadata/context: e.g. Republic, dan correspondentie, migrant archiefcollecties
    - baseline detection
    - line detection
    - region detection
- gebruik van inventarissen en andere metadata voor training
    - NER-modellen trainen en uitwisselen? Binnen Transkribus (Transkribus Tagger) of elders?
    - project-specifieke modellen vs. algemene/gecombineerde modellen
        - pre-training op zoveel mogelijk en zo divers mogelijk, maar wel gebalanceerd (document genres, periodes, talen, ...)
        - daarna fine-tuning op specifieke data
    - gestructureerde externe resources: thesauri, termenlijsten 
    - gedeelde vorm/toepassing voor e.g. attestatie (voor e.g. document type, object types (logo, ...))
- duurzaamheid van pipelines/programma's
    - n.a.v. discont. htr+ citlab in Transkribus
    - ground truth, modellen
    - best practices 
    - 

Document genres:
- seriele bronnen (administratief)
- ego documenten
- indexen/registers
- gedrukt versus handgeschreven

## Vragen

- Is het wenselijk een procedure op te zetten om onderling eenvoudig HTR-modellen of Ground Truth te kunnen delen?
    - Gebruik 'standaarden' om data te delen?
    - Meerdere versies van dezelfde scan?
    - https://htr-united.github.io/ en https://zenodo.org/communities/ocr_models/ 
    - Exploring Data Provenance in Handwritten Text Recognition Infrastructure: Sharing and Re-Using Ground Truth-Data, Referencing Models, and Acknowledging Contributions. https://docs.google.com/document/d/11EBSHRoRteZC2ulIimDy0tsdN3ZO1v3h/edit
- Op welk niveau en in de context van welke projecten kunnen we nauwer samenwerken? En op welke onderwerpen zou dit dan zijn? Bijvoorbeeld:
    - Terminologie (thesaurie)
    - Annotaties (generiek)
        - Documentbegin/-eindes, classificatie
        - Visuele kenmerken, logo's, handtekeningen, plaatjes, etc.
        - NER

## Inventarisatie gedeelde interesses (reservelijst van onderwerpen)

- Toegankelijkheid materiaal in digitaal formaat versus/en/of gebruik in (digitaal) onderzoek
- Document resolution (in gevarieerde collecties) / autoencoder
- Schrijveridentificatie 
- sturen van training d.m.v. context/metadata bij herkenning van layout en tekst
- thesaurus van classificaties, documenttypen, etc.
- GrootGemeenschappelijkModel of ieder voor zich?
- tooling delen:
    - overzicht bijhouden 
    - OCReval: https://eddieantonio.ca/ocreval/
    - PageXML tools: generieke functionaliteit (Python) voor werken met PageXML data https://github.com/knaw-huc/pagexml
    - Loghi: 

- AVG en andere eventueel beperkende wetgeving en hoe daarmee om te gaan.
    - e.g. ground truth delen (geldt vooral voor 20ste eeuw)
    - NA werkt cases uit in de context van Oorlog voor de rechter

- NER en verwante technieken voor automatische metadatageneratie

## Agenda volgende bijeenkomst
- AVG en andere eventueel beperkende wetgeving en hoe daarmee om te gaan.
    - e.g. ground truth delen (geldt vooral voor 20ste eeuw)
    - NA werkt cases uit in de context van Oorlog voor de rechter
- Splits tips, tricks en technieken voor:
    - pre-HTR/OCR: e.g.:
        - image resolution (laag voor classificatie o.b.v. high-level features)
    - tijdens HTR/OCR, e.g.:
        - metadata/context meegeven, 
        - output layer aanpassen
        - layers vervangen
    - post-HTR/OCR analyse/extractie
        - classificatie op basale/generieke variabele (bytes, height, width, num words, num lines, num regions, num punctuation, num numbers, num stopwords, num long words, ...)
        - language identification per region
- Projectpresentaties 
    - Rick C. - persoonskaarten CBG (OCR in Mac OS)
    - Ismee - idee delen (Nansen-project)
- Breder uitnodigen
    - Martijn Maas en Stefan Klut (HuC DI - Team Images)
    - Gerhard de Kok (Universiteit Leiden)





