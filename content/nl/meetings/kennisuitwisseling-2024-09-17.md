+++
date = '2024-04-10T13:07:34+02:00'
draft = false
title = 'HTR Kennisuitwisseling 17 september 2024'
[menus]
    [menus.main]
        parent = 'Bijeenkomsten'
        weight = 20
+++

De zevende bijeenkomst op 17 september 2024

### Bijeenkomst

Datum: 17 september 2024
Tijd: 14:00-16:00
Locatie: Bushuis, Amsterdam

Het thema van deze bijeenkomst is: Hoe word ik wegwijs in de wereld van ATR?

### Agenda

- Steven Claeyssens - Hoe kun je lopende productieprocessen en -beleid bijsturen a.d.h.v. huidige ontwikkelingen en kennis?
- Ronde tafel: Wat wil je bereiken? Wat zou je in retrospect anders doen?

<!--more-->


### Aanwezig

Aanwezigen en ervaringen met/vragen over OCR/HTR:

- Stefan Klut - Team Images Huc - diverse projecten
- Joyce Pennings (?) - Utrechts Archief - OCR/HTR, resoluties 17e & 18e eeuw, burgerlijke stand met Loghi, Vele Handen
- Arvid de Raaij - NIOD - expertise met evaluatie
- Muriel Bouman - NIOD - collectie brieven, kan ATR helpen bij onleesbare handschriften
- Rachel Westerveld - Gelders archief - Transcripties in beginfase, eerste projecten opstarten
- Tom Willemsen - Gelders Archief
- Irene Rooker - Gelders Archief
- Machteld van Voskuilen - ECR - Grote archieven transcriberen
- Eelke Muller - ECR  -
- Daniel Hendrikse - ECR - onderzoeker, verkenning mogelijkheden
- Kay Pepping - Huygens - informatie extractie, tutorials voor Tesseract op Programming Historian, voor Transkribus is in de maak
- Celine (?)
- Floris Kunert - NIOD/ECR - archieven met (semi-)gestructureerde informatie operationaliseren.
- Milan van Lange - NIOD - Oorlogsbrieven, moeielijke scans (gevarieerd), selectie van gevarieerde en gebalanceerde training set.
- Annelies van Nispen - NIOD
- Carlijn Keijzer - NIOD -
- Pauline van den Heuvel - Stadsarchief Amsterdams - ervaring met Transkribus, notarieelarchief, indicateurs (tabellen/kolommen), burgerlijke stand, charters, LLMs, data-extractie
- Rutger van Koert - HuC/NA - Loghi
- Liesbeth Keijser - NA -
- Ralf Futselaar - NIOD/Erasmus Rotterdam -
- Esger Renkema - Huygens - informatie extractie
- Eric van der Linden - Huygens - informatie extractie
- Marijn Koolen - Huygens / HuC DHLab - informatie extractie


### Presentatie Steven Claeyssens

- Project HaiCu - NL-breed project (https://www.haicu.science)
- Impact project - centre of competence: https://www.digitisation.eu
- Couranten Corpus (INT, https://ivdnt.org/corpora-lexica/courantencorpus/)
- Hoe kun je lopende productieprocessen en -beleid bijsturen a.d.h.v. huidige ontwikkelingen en kennis?
    - Experimenten met Transkribus kunnen 50% kosten reduceren of output verdubbelen
    - Experimenten met Loghi
    - Nieuwe digitaliseringsstrategie: geeft aan wat we willen toevoegen de huidige digitale collecties (nieuwe ATR, nieuwe scans)
Naar aanleiding van een presentatie van Steven Claeyssens (K.B.) willen we een aantal aspecten aan bod laten komen, o.a.:

·           Opstarten ATR-project: waar te beginnen?
·           dataverzameling, geschikte scans, vraag- of bron-georiënteerd werken?
·           Data management, project design en menselijke interventies
·           Keuze voor tooling: off-the-shelve, open source, eigen maak? Transkribus versus Loghi (en alternatieven)
·           Keuze voor modellen: standaard, delen, zelf trainen?

### Ronde tafel

Voor sommigen van jullie zijn een aantal van deze aspecten gesneden koek, voor anderen niet. Omdat dit een kennisuitwisseling is, lijkt het ons erg nuttig als mensen van te voren kunnen nadenken over welke kennis of vragen ze kunnen bijdragen.

- Voor aspecten waar je al ervaring mee hebt: wat zou je in retrospect anders/opnieuw doen?
- Voor aspecten waar je nog geen ervaring mee hebt: wat wil je bereiken, welke vragen heb je en wat zijn eventuele belemmeringen of struikelblokken?



**Vragen:**
- Selectie van bronnen: Welke archieven kies je eerst als het gaat om digitaliseren? Hoe maak je die selectie?
    - bronnen met veel lopende tekst zijn makkelijk te digitaliseren (huidige modellen zijn vaak goed genoeg, zonder veel handwerk). Goed startpunt.
    - Layout is vaak de bottleneck. 'HTR is af', aldus M. Koolen, april 2024
- (Semi-)gestructureerde informatie en het herkennen van structuur  / layout
    - Tabellen, indexen op het archief (volgnummers en kolommen), heel nuttig voor ontsluiting.
        - vooral voor verbaalarchieven
        - doel is doorklikbare volgnummers in transcripties
        - Stadsarchief Amsterdam heeft Transkribus hiervoor gebruikt
        - probleem: scribenten houden zich niet altijd aan kolomgrenzen, dus kijk altijd goed naar je layout (ligt aan consistentie)
        - kwaliteitseisen liggen aan gebruik, bronnen relevant voor breed publiek wil je wellicht hoger hebben (verbeteringen door crowd of door opnieuw trainen)
        - Laat je dan alles controleren? Of maak je een selectie van meest risicovolle materiaal (Utrechts Archief doet alles)
- kwaliteitscontroles: hoe, wat, wat doe je ermee?
- hoe delen we informatie?

- In hoeverre is ATR een technologie voor het leesbaar maken van onleesbare handschriften en documenten?
    - los trainen op segmenten die wel herkend kunnen worden kan helpen (ook model iteratief laten trainen op eigen output)

- Er zijn tutorials voor b.v. Tesseract (zie Programming Historian), maar geen praktische tools en manuals voor PageXML-tools of Loghi (binnen het historische onderzoeksdomein).
    - https://programminghistorian.org/en/lessons/ocr-with-google-vision-and-tesseract
    - Een Transkribus tutorial is in de maak voor Programming Historian


- Vergelijk Transkribus en Loghi (en alternatieven)
    - met minder dan 100,000 scans: gebruik Transkribus, want Loghi opzetten is vrij veel moeite (Transkribus is veel gebruiksvriendelijker)
        - Starten via: https://help.transkribus.org/
        - Toegang geven aan/delen met anderen en crowd sourcing, publiceerbaar via zelfde platform.
        - Modellen trainen in Transkribus is makkelijk, delen met anderen, maar niet bruikbaar in andere ecosystemen
        - Loghi modellen zijn niet allemaal publiek,
    - Met meer dan 100,000 scans: Loghi is voor grote hoeveelheden goedkoper (als je je eigen machinerie hebt!)
    - a]Als materiaal niet openbaar mag zijn, dan is het belangrijk om alles op eigen servers/machines te draaien
    - maken van ground truth kan wel in Transkribus, niet in Loghi. Ground Truth kan wel vanuit Transkribus gebruikt worden in Loghi.
    - Transkribus is handige start: alles kan op een makkelijke manier (ground truth maken, modellen trainen, delen, transcripties maken, evalueren)
    - Layout: standard output in PageXML (bevat transcriptietekst en layoutinformatie, in te laden in zowel Transkribus en Loghi)
    - Metdata in sites(?, voorheen Read-and-Search, Transkribus) is rudimentair, maar wordt langzaam uitgebreid
- Alternatieven voor Transkribus, Loghi:
    - Kraken: https://kraken.re/main/index.html
    - TrOCR: (taalmodel, https://huggingface.co/docs/transformers/model_doc/trocr), vergt meer zelf een software pipeline opzetten

- Medatatering / informatie-extractie
    - a.d.h.v. LLMs (vooral ChatGPT vanwege de hoge kwaliteit). Kosten zijn laag (via Transkribus is flink duurder). Er kleven veel ethische bezwaren aan het gebruik van OpenAI's ChatGPT, en het delen van data met OpenAI is in strijd met wet- en regelgeving voor privacy, persoonsgegevensbescherming en auteursrecht.
    - Alternatieven voor ChatGPT die op een lokale machine kunnen draaien (minder resources nodig, data hoeft niet gedeeld te worden met commerciele bedrijven, nog lagere kosten)
        - Nomic AI (https://www.nomic.ai)
        - Ollama (https://ollama.com)

- Selectie en balanceren van de trainingset bij zeer gevarieerd materiaal en uitzonderlijk lastige layout
    - Random selectie is goed voor het genereren van een validatie-set
    - voor training is gebalanceerde selectie beter (als je verschillende types documenten hebt, dan is stratified sampling nuttig, zorg dat alle types vertegenwoordigd zijn in de ground truth)
- Hoe kunnen we opschalen en een hele instituutscollectie / archief in één keer door ATR halen, hoe geef je dit proces vorm en waar en hoe controleer je?


    - Opzetten van een ATR-straat met Loghi:
    - Simpel 'poor man's service: input-map met scans, output-map met ATR output, is al snel voldoende (300,000 a 400,000 scans / week)
        - Wat is hier voor nodig? 
        - Zie ook: https://github.com/knaw-huc/loghi 
        - Linux machine, GPU (of Windows met subsystem Linux). 
        - Mappenstructuur opzetten: inputmap, werkmap, outputmap
    
    - Geavanceerd: meerdere machines, meerdere stappen, elke stap op een aparte machine, rekenkracht per stap/machine is aangepast zodat elke stap even lang duurt, voor optimale flow (2 miljoen scans / week)
        - controleproces: is het proces goed genoeg? steekproef selecteren, transcriberen en regels daaruit handmatig corrigeren (iteratief evalueren met steeds nieuwe ground truth)
        - visuele controle: vooral layoutcontrole (regio's en baselines)
    - Aansluiten op eigen infrastructuur is altijd lastig.
    - Transformer modellen kunnen gaan hallucineren: nadeel! 

- Reverdi (internationaal project) - becijferen: hoe duur is het om één fysiek boek 10 jaar te bewaren versus een digitale representatie 10 jaar bewaren.

**Ronde tafel: Verdere opmerkingen en vragen:**

- Is er een frontend voor Loghi:
    - nee, niet echt (alleen een demo waarbij je een scan kunt slepen om te transcriberen)
- Documentclassificatie
    - voeg label toe aan scan om aan te geven wat voor document het is
- Documentsegmentatie:
    - welke scans vormen samen één document? Bredere punt: waar zijn documentgrenzen (komen soms overeen met scangrenzen, i.e. hele scan hoort helemaal bij één document, maar soms binnen een scan, i.e. ergens halverwege de scan zit een grens tussen twee documenten)


