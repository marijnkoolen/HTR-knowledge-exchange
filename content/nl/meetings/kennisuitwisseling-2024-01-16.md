+++
date = '2024-01-18T13:07:34+02:00'
draft = false
title = 'HTR Kennisuitwisseling 16 januari 2024'
[menus]
  [menus.main]
    parent = 'Bijeenkomsten'
    weight = 20
+++

De vijfde bijeenkomst op 16 januari 2024

#### Bijeenkomst

- Datum: 16 januari 2024
- Tijd: 13:00-15:00
- Locatie: Huygens Instituut, Spinhuis, Oudezijds Achterburgwal 185, Amsterdam

#### Presentaties

- Gijs Hoekstra en Milan van Lange: Wensen en uitdagingen in het project "De Nederlandse Spoorwegen in oorlogstijd"
- Marijn Koolen: REPUBLIC pipeline
- Niek Verhoeff (online): Korte update NER bij het Stadsarchief
- Erik Tjong Kim Sang: HTR en formulieren

<!--more-->

### Aanwezig

- Liesbeth Keijser
- Niek Verhoeff (online)
- Rick Companje
- Erik Tjong Kim Sang
- Esger Renkema
- Gerhard de Kok
- Milan van Lange
- Kay Pepping
- Gijs Hoekstra
- Marijn Koolen
- Pauline van den Heuvel
- Jirsi Reinders




## Presentaties

### Gijs Hoekstra en Milan van Lange: Wensen en uitdagingen in het project "De Nederlandse Spoorwegen in oorlogstijd"

- Uitdagingen: spellingsvariatie
- Tooling: 
    - modellen voor juiste periode en genre
    - annotation tools: Prodigy (prodi.gy), Label Studio

### Marijn Koolen: REPUBLIC pipeline

Zie ook: https://republic.huygens.knaw.nl/index.php/en/about-republic/ 

- Information Extraction in REPUBLIC.
- De handschrift- en typoscriptherkenning gebeurt met Loghi. Het project heeft ook veel trainingsmateriaal aangeleverd.

- Ook het handgeschreven materiaal is fenomenaal goed herkend inmiddels.

- Nu bezig met de volgende stappen: entiteiten herkennen. 

Eerste ronde: ruim 8 miljoen. 

##### Wat is een goede reden om entiteiten te herkennen?

- Extra toegang
    - Additional access points (for navigation)
    - Contextual information 

##### Wat is een goede reden om entiteiten niet te herkennen?

- Bij slechte herkenning vooral weglaten (in een online repository waar je te maken hebt met gebruikers).
- De toegevoegde waarde is mogelijk kleiner dan de moeite die het kost (en bij slechte kwaliteit draagt dit niet bij aan de kwaliteit).

##### Welke entiteiten?
- Welke entiteiten komen voor?
- Welke entiteiten zijn interessant?
- Welke entiteiten zijn annoteerbaar?

Entiteiten: Personen, attribution, location / political entity, organisation, Commission, Date, resolution reference, Other.

Het taggen is gedaan met Inception. 

Tijdspad:
- juni - oktober 2022: ontwikkelen instructies
- december 2022: start Tag de Besluiten
- april 2023: 1631 tagged resolutions 18e eeuw
- juli 2023: 513 tagged paragraphs 17e eeuw (handgeschreven)
- september 2023: begonnen met trainen van taggers

Keuze: Werken met één model voor alles (ook nested entities), of één model per type entiteit? 

De laatste heeft als voordeel dat er per type entiteit een passend model te trainen is, en eventueel de keuze om een bepaald type niet mee te nemen makkelijk te maken is.

Nesting is een thema dat veel onenigheid kan opleveren. Historische kennis helpt hierbij. Ground Truth is lastig met geneste structuren.

![NER evaluatie](../../images/ner_evaluation-REPUBLIC.jpg)

Voor verschillende entiteittypen verschillende modellen. Waarbij 'Resolution ref' het enige type is waarbij een model voor alle typen het best werkt.

Opvallende uitkomst: karakter-modellen (op basis van vier karakters) doen het vaak verrassend goed.

##### Cureren van de entiteitstypen

#### Tooling:
- NN Models
- FLAIR
- GT annotatie: INCEpTION, Prodigy, Brat, Label Studio
- Syntactic parsers: Bert-based, POS-tags and lemma information can help NER.

#### Uitgangspunten algemeen:
- Goede GT is van tijdloze waarde, modellen zijn snel verouderd.
- Trainingsdata op 'flow' van tekst en tekstvolgorde is belangrijk. Ook voor semantische (?) taken.
- (shocking!): Layout analyse is belangrijk voor NER! We moeten ons allemaal op layout richten. 

### Niek Verhoeff (online): Korte update NER bij het Stadsarchief
- Prodigy gebruikt. Take-home message: domein specifieke modellen werken het best (b.v. personen, plaatsnamen, organisaties apart). 

### Erik Tjong Kim Sang

- [Slides deel 1](https://ifarm.nl/erikt/talks/slides-20230922-clin.pdf) en [Slides deel 2](https://ifarm.nl/erikt/talks/slides-20231130-clariah.pdf)

- HDSC project escience-center en Radboud Universiteit

- Vrijwilligersproject (hetvolk) handmatig invoeren van gedrukte en handgeschreven tekst van formulieren. Doel: omzetten in digitale vorm.
- Niet volledige tekst-transcripties, alleen invullen van gegevens uit de formulieren.
- Doel is om te kijken of HTR-technologie een nuttige toevoeging kan zijn om formulieren en transcripten verder te digitaliseren. Transkribus momenteel, Loghi wordt nog geexploreerd.

- Ook hier speelt layout-analyse een belangrijke rol. Veel consistentie in vorm van formulieren.

- probleem: HTR van eigennamen.
    - accuracy op ouder materiaal is hoger dan op nieuwer materiaal
    - filteren op quality estimation geeft grote boost aan accuracy
- 

##### NER

- Met Huggingface modellen. 
- --> Resultatentabel hier invoegen?

## Discussiethema's 

- Informatie Extractie, NER + semantic role labelling, entity linking en event detection
    - generiek (brede toepassing) vs. specifiek (bron-georienteerd)
    - toepassing: inhoudelijke analyse vs. brede ontsluiting (e.g. scheve/onvolledige tagging)
    - nested entities
    - annotatie: instructies, curatie en hergebruik
    - tooling: Inception, Prodigy, Label Studio, Flair (Python), SpaCy
    - layout detectie en logische structuur
    - tabellen: https://www.amsterdam.nl/stadsarchief/organisatie/blog-bronnen-bytes/tekstherkenning-(5)-tabellen/?trk=feed-detail_main-feed-card_reshare_feed-article-content

## Uitdagingen/wensen

## Rondvraag

- Voorstel thema volgende keer: Evaluatie OCR/HTR resultaten (IvdNT)?
- Verzamelen input voor cureren van de uitgewisselde kennis (redactie, structuur, github als kennisbank?)





