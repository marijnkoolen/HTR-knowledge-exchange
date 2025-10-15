+++
date = '2023-10-31T13:07:34+02:00'
draft = true
title = 'HTR Kennisuitwisseling 24 oktober 2023'
[menus]
[menus.main]
parent = 'Bijeenkomsten'
weight = 20
+++

De vierde bijeenkomst op 24 okbtober 2023

## Bijeenkomst

Datum: 24 oktober 2023
Tijd: 11:00-13:00
Locatie: Spinhuis zaal 2.18, Oudezijds Achterburgwal 185, Amsterdam

## Presentaties

- Rutger van Koert & Stefan Klut - Loghi
- Carsten Schnober - HTR Quality

<!--more-->

### Aanwezig

- Rutger van Koert
- Niek Verhoeff
- Rick Companje
- Arno Bosse
- Carsten Schnober
- Gerhard de Kok
- Milan van Lange
- Kay Pepping
- Stefan Klut
- Marijn Koolen
- Pauline van den Heuvel
- Rik Hoekstra


## Presentatie Loghi (Rutger van Koert en Stefan Klut)

- Loghi: 
    - HTR and layout analysis toolkit
    - https://github.com/knaw-huc/loghi
- LayPa: 
    - tool for text detection - where is the text in a scan
    - https://github.com/stefanklut/laypa
- Pre-processing
    - PageXML segmentation
    - semantic (type classificatie), 
    - panoptic (groep classificatie o.b.v. pixels), 
    - instance (o.b.v. polygonen)
- Post-processing
    - semantic segmentation to baselines
    - cut out text lines (seam carving)
- Next step:
    - transformer-based HTR
    - convolution+recurrent reads line-by-line, requires little training data
    - transformers require more training data
- Other features
    - underline/strikethrough/superscript
    - finetuning of basemodels
    - PageXML 2019
    - data augmentation
- Future
    - segmentation free OCR/HTR
    - generic models
    - LLM integration (including historical languages)
    - less GT needed hopefully



## Presentatie HTR Quality (Carsten Schnober)

Classifying quality of digitzed documents
- https://github.com/LAHTeR/htr-quality-classifier
- developed for VOC documents in the GLOBALISE project
- but applicable more generally
- Context: LaHTeR project
    - faclitate manual and automatic analysis of HTR'ed documents
- Challenges
    - downstream tasks have different requirements
    - Event detection is more sensitive than keyword searach to correct readign order and text segmentation 
- Ground truth
    - focus on layout analysis
    - good/medium/bad
    - 328 scans
- Traffic light decision tree
    - red: re-do HTR
    - yellow: post-correction
    - green: done
- scoring
    - Dictionary scores
    - trigram scores
    - garbage token score (heuristics e.g. long words, repeated characters, odd character sequences)
    - GT set shows no single feature is good at distinguishing between the classes
- To do
    - account for different languages
    - consider: add layout information as input, e.g. page type


Vragen:
- over de ground truth, waarom worden scans met annotator disagreement weggelaten? (gelaagde/getrapte benadering van annotator disagreement als alternatief voorgesteld)
- Is het zinnig om temporele aspecten op te nemen in de ground truth? E.g. aparte ngram distributies voor begin 17de eeuw, eind 17de eeuw, etc. 

## Rondvraag

- wensen voor de volgende keer: NER en entity linking/event detection
- GLOBALISE built a transcript viewer.
    - Globalise Labs Transcriptions Viewer. https://transcriptions.globalise.huygens.knaw.nl: this is just a simple, interim tool for users, made available in conjunction with the first, full release of the 4.7M VOC transcripts. Note: it's not the research portal or VRE for Globalise. This is also explained on the landing page. 
    - https://lab.globalise.huygens.knaw.nl is the place to store all the experiments and beta versions of tools and resources from the Globalise project.
- 



