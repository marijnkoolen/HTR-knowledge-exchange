+++
date = '2023-01-13T13:07:34+02:00'
draft = true
title = 'HTR Kennisuitwisseling 11 januari 2023'
[menus]
  [menus.main]
    parent = 'Bijeenkomsten'
    weight = 20
+++

De tweede bijeenkomst op 11 januari 2023

## Bijeenkomst

Datum: 11 januari 2023
Tijd: 11:30-13:30
Locatie: NIOD, vergaderzaal, Herengracht 380, Amsterdam

## Presentaties
- Rick Companje - persoonskaarten CBG
- Ismee - Nansen-project

<!--more-->

**Aanwezig**

## Aanwezig/uitgenodigd

- Arno Bosse (HuC DI - Globalise)
- Rick Companje (Utrechts Archief)
- Rik Hoekstra (Huygens Instituut)
- Liesbeth Keijser (Nationaal Archief)
- Stefan Klut (HuC DI - Team Images)
- Gerhard de Kok (Universiteit Leiden)
- Marijn Koolen (Huygens Instituut)
- Milan van Lange (NIOD)
- Ronald Sluijter (Huygens Instituut)
- Ismee Tames (NIOD)
- Niek Verhoeff (Stadsarchief Amsterdam)
- Heleen Wilbrink (Utrechts Archief)
- Leon van Wissen (UvA)

Afwezig:
- Mirjam Cuper (KB)
- Carlijn Keijzer (NIOD)
- Rutger van Koert (HuC)
- Annelies van Nispen (NIOD)
- Martijn Maas (HuC DI - Team Images)
- Pauline van den Heuvel (Stadsarchief Amsterdam)



## Agenda

- Projectpresentaties en Q&A 11:30 - 12:15
    - Rick Companje - persoonskaarten CBG (OCR in Mac OS) (15 min.)
    - Ismee - Nansen-project (probleem/vraag delen) (15 min.)
    - Vragen en opmerkingen aan Rick en Ismee        (15 min.)

- Lunch 12:25 - 13:00
    - Bespreken: tips, trucks en technieken voor:
        - pre-HTR/OCR
        - tijdens HTR/OCR
        - post-HTR/OCR analyse/extractie

- Bespreken: Doelen en vervolg van deze groep 13:00-13:30
    - Delen van resources (software, data/modellen, best practices, literatuur, etc.)
    - Gedeeld communicatiekanaal (slack)
    - Idenficeren aanknopingspunten concrete (toekomstige) samenwerkingsprojecten


## Notities

- Persoonskaarten CBG (Rick Companje)
    - focus op vier velden: voornaam, achternaam, geboortedatum, geboorteplaats
    - preprocessing: model-detectie (kaartmodellen), scans voorbereiden (grayscale, speck removal), uitlijnen, opschonen/maskeren
    - OCR: niet in de cloud, dus opties: Tesseract, Easy OCR of Monterey (standaard ingebouwde OCR/HTR in macOs)
    - controle/correctie a.d.h.v. Woordenlijsten CBG: familienamen, voornamen, plaatsnamen
    - gebruik vaste elementen en fuzzy search voor segmentatie
    - gebruik ChatGPT om tekst om te zetten in gestructureerde data

- Nansen paspoorten (Ismee Tames)
    - staatloze mensen jaren '40 en '50
    - **onderzoeksfocus**: beschrijf hoe het was om staatloos te zijn in de gekozen periode.
    - **uitdaging**: bij elkaar brengen van heel divers materiaal uit heel veel archieven.
    - downloaden: handmatig per pagina op de website. **vraag**: kan dit handiger?
    - **vraag**: hoe kan ik snel focus kiezen voor analyse, zonder vast te raken in perfecte data maken van irrelevante data?
    - Taken:
        - document segmentatie
            - documentset per persoon
            - document type binnen documentset
        - paginatype classificeren/clusteren (formulier vs. brief, gestructureerd vs. lopende tekst, gedrukt, getypt, handgeschreven)
        - taaldetectie per regel/alinea
        - kaartenbak: modeldetectie
    - focus kiezen o.b.v. steekproeven:
        - Wat zit er in welk archief? Wat kun je uit elk archief halen?



## Discussiepunten


- Splits tips, tricks en technieken voor:
    - pre-HTR/OCR: e.g.:
        - image resolution (laag voor classificatie o.b.v. high-level features)
        - Layout training and recognition
        - Wat is Ground Truth eigenlijk? Gedeelde criteria wenselijk?
    - tijdens HTR/OCR, e.g.:
        - metadata/context meegeven,
        - output layer aanpassen
        - layers vervangen
    - post-HTR/OCR analyse/extractie
        - **correctie** a.d.h.v. woordenlijsten (persoonsnamen, plaatsnamen, ...)
        - **segmentatie** o.b.v. vaste elementen
        - **classificatie** o.b.v. basale/generieke variabele (bytes, height, width, num words, num lines, num regions, num punctuation, num numbers, num title words, num stopwords, num long words, ...)
            - classificatie van text lines voor tekstsegmentatie
            - classificatie van pagina's voor pagina type metadata
            - clustering voor identificeren document genres
        - **taaldetectie**: per text region
- Inzet ChatGPT
    - problemen met gefantaseerde output: hoe controleer je in grote batches waar en wanneer ChatGPT output verzint die niet correspondeert met enige input?
    - problemen met gebruik van closed source, commercieele software.


