+++
date = '2023-03-19T13:07:34+02:00'
draft = true
title = 'HTR Kennisuitwisseling 15 maart 2023'
[menus]
  [menus.main]
    parent = 'Bijeenkomsten'
    weight = 20
+++

De derde bijeenkomst op 15 maart 2023

## Bijeenkomst

Datum: 15 maart 2023
Tijd: 13:00-15:00
Locatie: Spinhuis zaal 2.18, Oudezijds Achterburgwal 185, Amsterdam

## Presentaties

- Gerhard de Kok - toepassing van PageXML tools op Notariële akten
- Marijn Koolen - PageXML Tools en inventarisatie van taken op PageXML data

<!--more-->


### Aanwezig

- Pauline van den Heuvel
- Annemieke Romein
- Bram Buitendijk
- Milan van Lange
- Marijn Koolen
- Jirsi Reinders
- Niek Verhoeff
- Rik Hoekstra
- Rick Companje
- Filotas Liakos
- Stefan Klut
- Heleen Wilbrink
- Esger Renkema
- Ronald Sluijter
- Eric van der Linden
- Kay Pepping
- Gerhard de Kok

## Programma

- [PageXML tools](https://github.com/knaw-huc/pagexml)
- gebruik van PageXML
    - Gerhard de Kok, toepassing van PageXML tools op ...
    - inventarisatie van taken op PageXML data

## PageXML-Tools


Python module voor het inlezen en werken met PageXML bestanden. De [Github repository](https://github.com/knaw-huc/pagexml) bevat verschillende tutorials voor verschillende taken.

Doel is het ondersteunen van een aantal taken in het werken met HTR/OCR output:
- **scan-classificatie**: hoe kun je verschillende soorten pagina's herkennen o.b.v. basale layout en tekst-karakteristieken?
- **boeksectie-detectie**: hoe kun je detecteren of een opeenvolgende set scans uit verschillende secties bestaat?
- **kwaliteitscontrole**: in grote bulk PageXML bestanden, hoe kun je inzicht krijgen wat de kwaliteit van de HTR/OCR is?
- **alinea-generatie**: hoe kun je tekstregels samen voegen tot lopende tekst, zodat woordafbreektekens correct afgehandeld worden?
- **tekst zoeken**: hoe kun je (efficient) zoeken naar keywords en key phrases in één of meer PageXML bestanden? Hoe kun je fuzzy zoeken naar spellingsvarianten.
- **leesvolgorde bepalen**: hoe kun je verschillende leesvolgordes hanteren voor documenten?
- **herstructuren van pagina-elementen**: hoe kun je PageXML elementen combineren to nieuwe elementen?

## Inventarisatie PageXML taken

- document resolution: gegeven een meter archief, detecteer de grenzen tussen individuele documenten in dit archief.
- informatie extractie en structureren
- extractie entiteiten en rollen en de relaties daartussen
- end-to-end pipelines voor grote schaal
- feedback naar layout analyse, metadata over elementen koppelen aan coordinaten
- rijke ground truth maken
- document type vaststellen



Implementeren:

- van JSON naar XML (maar wat is een zinnige use case?)
- check element in other element (kun nu via `.is_horizontally_overlapping` en `.is_vertically_overlapping`, maar kan makkelijker gemaakt kunnen worden door een functie die deze combineert.)
- lezen uit directory

## Presentatie Gerard de Kok

Gebruik PageXML tools voor detecteren van WIC opvarenden in notarieel archief.

## Inventarisatie PageXML taken

- document resolution: gegeven een meter archief, detecteer de grenzen tussen individuele documenten in dit archief.


