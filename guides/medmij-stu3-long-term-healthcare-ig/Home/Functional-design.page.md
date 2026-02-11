---
topic: FO
---

# Functioneel ontwerp

## Algemeen 

Dit ontwerp beschrijft de databeschikbaarheid richting de persoon voor de Basisgegevens Langdurige Zorg+ (BgLZ+). Hierdoor kan de burger, cliënt of patiënt zijn relevante langdurige zorggegevens bekijken via de PGO om een beter en vollediger inzicht te krijgen in de eigen medische situatie.​ 

Het doel van dit document is om de BgLZ+ beschikbaar te stellen aan een persoon (in de PGO). 

### Doelgroep 

De doelgroep voor deze pagina wijkt niet af van de [algemene doelgroep](https://informatiestandaarden.nictiz.nl/wiki/MedMij:FO:V1/FunctioneelOntwerp#Doelgroep) van de MedMij functionele ontwerpen. 

### Kaders en uitgangspunten 

### Richtlijn & proces 

Dit ontwerp is conform specificaties genoemd in [de algemene inleiding](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.01/Ontwerpen#Richtlijn) van de MedMij functionele ontwerpen. 

### Reikwijdte 

De reikwijdte van dit ontwerp beslaat de functionele beschrijvingen en de dataset voor de gegevensuitwisselingen die voortvloeien uit uitgevoerde langdurige zorg. 

Deze pagina beschrijft het functioneel ontwerp voor de Basisgegevens Langdurige Zorg+ (BgLZ+). De BgLZ+ bestaat uit gegegevens die relevant zijn voor uitwisseling met patiënten en cliënten binnen de langdurige zorg via hun persoonlijke gezondheidsomgeving (PGO). Deze BgLZ+ kan samen met de Basisgegevensset Langdurige zorg (BgLZ) uitgewisseld worden. De BgLZ wordt in stand gehouden zoals die er nu staat, hier zullen geen wijzigingen in plaatsvinden. De BgLZ+ gaat over de aanvullende health and care information models (HCIM) die naast de al bestaande BgLZ verzameld kunnen worden via de PGO. De BgLZ+ HCIMs kunnen samen met de BgLZ alsook als lossstaande gegevevensdiensten granulair uitgwisseld worden. We stappen in deze gegevensdienst af van het uitwisselen van gegevens als één grote gegevensdienst,en gaan toe naar granulaire uitwisseling op het niveau van afzonderlijke HCIMs. Meer informatie over granulaire gegevensdiensten is te vinden via de [MedMij STU3 Core pagina](https://simplifier.net/guide/medmij-stu3-core-ig?version=current). 


### Infrastructuur 

Geen nadere specificatie, anders dan genoemd in de [algemene inleiding](https://informatiestandaarden.nictiz.nl/wiki/MedMij:FO:V1/FunctioneelOntwerp#Infrastructuur) van de MedMij functionele ontwerpen. 

### Geografische reikwijdte 

Geen nadere specificatie, anders dan genoemd in [de algemene inleiding](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/Ontwerpen#Geografische_reikwijdte)van de MedMij functionele ontwerpen. 

## Use-cases 

### Algemeen 

Een usecase is een specifieke beschrijving van een praktijksituatie in de langdurige zorg waarbij voor een concrete situatie het uitwisselen van informatie wordt beschreven aan de hand van actoren (mensen, systemen) en transacties (welke informatie wordt wanneer uitgewisseld). Een usecase is een verbijzondering van een specifiek onderdeel van het zorgproces in de langdurige zorg.   


### Doel en relevantie granulair raadplegen BgLZ+

Het voor de burger, cliënt of patiënt mogelijk maken om regie te nemen op hun eigen gezondheid door inzicht te geven over de langdurige zorggegevens die over henzelf gaan. 


#### Patient journey BgLZ+   

De patient journey beschrijft enkele momenten waarop je als patiënt zijnde inzicht kan of zou willen hebben in zijn langdurige zorggegevens.

In de landurige zorg zijn er veel verschillende patiëntreizen te onderscheiden. Onderstaand is één patiëntreis beschreven. Er zijn eerder meer patiëntreizen beschreven, onder andere in opdracht van Platform IZO (zie document Het netwerk in de praktijk, 31-03-2022) en ook door Nictiz (Casus Kenneth van Someren -  https://informatiestandaarden.nictiz.nl/images/a/a6/Casus_Kenneth_van_Someren_MedMij.pdf).   

Hieronder een voorbeeld van patiëntreis van denkbeeldige patiënt Peter (eigenlijk spreekt men in de langdurige zorg meestal van cliënt) en de gegevensuitwisseling binnen de langdurige zorg tussen zorgaanbieder en patiënt. Gezien het langdurige zorggegevensuitwisseling naar de PGO betreft is onderstaand een specifieke patiëntreis geschetst waarbij gegevens geraadpleegd worden vanuit de PGO:  

Peter is een actieve weduwnaar van 72 jaar oud. Peter heeft drie kinderen, twee zoons, een dochter en vijf kleinkinderen. Thuis had Peter al steeds meer hulp nodig, zo kan hij onder andere moeilijk zelf douchen en het bijhouden van zijn medicatie vindt hij ook lastig. Peter heeft daardoor, de afgelopen vijf jaar, veel wijkverpleging op bezoek gehad gezien hij hulp nodig had met zijn Algemene Dagelijkse Levensverrichtingen (ADL).   

Een maand geleden is Peter getroffen door een hersenbloeding (CVA). Er wordt nu een opname in een verpleeghuis overwogen. Het is namelijk niet de verwachting dat hij voldoende zal herstellen gezien hij door zijn hersenbloeding halfzijdig verlamd is geraakt. In de wijk waar Peter woont, is een locatie gevestigd en daar zou hij graag naar toe willen. In samenspraak met Peter, zijn dochter en het verpleeghuis wordt een indicatie aangevraagd bij het CIZ.   

Peter is door de vele zorgverleners die hij de afgelopen tijd heeft ontmoet het overzicht kwijtgeraakt over zijn zorg en wil hier nog eens naar kijken. Bovendien was er te weinig tijd tijdens het consult om hierover door te praten met zijn zorgverlener.  

Op aanraden van zijn dochter heeft Peter nu een eigen gekozen PGO. In zijn PGO wil Peter zijn BgLZ+ zorggegevens raadplegen, hij is nieuwsgierig naar deze gegevens. Zijn dochter kijkt mee, die is bij Peter op visite. Hij wil deze gegevens graag thuis inzien zonder dat hij daarvoor de zorgverlener hoeft te belasten. Bovendien hoeft hij dan zelf nergens naartoe te gaan. Hij raadpleegt via zijn PGO de betreffende zorgaanbieder waar hij onder behandeling is om zijn BgLZ+ zorggegevens op te halen en in te zien. Peter ziet nu zijn medische gegevens, waardoor hij meer inzicht heeft in de status van zijn gezondheid.

#### Preproces 

- De cliënt beschikt over een eigen PGO dat aan de MedMij-eisen voldoet.  
- De cliënt heeft toestemming gegeven voor het elektronisch uitwisselen van medische gegevens tussen het betreffende XIS/EPD en de eigen persoonlijke gezondheidsomgeving. 
- Er is sprake van een dossier voor de cliënt binnen de langdurige zorg sector.   

#### Proces 

- De cliënt raadpleegt de ‘bloeddruk’ in zijn of haar PGO.
- Het systeem van de cliënt (PGO) vraagt om beschikbare medische gegevens bij een XIS/EPD aan de hand van een zoekopdracht.
- Het systeem van de zorgaanbieder (XIS) stelt de BgLZ+ gegevensdienst voor bloeddruk beschikbaar voor de patiënt.

#### Postproces 

- In de PGO van de cliënt wordt de bloeddruk overzichtelijk en begrijpelijk getoond.  

### Bedrijfsrollen en UML activity diagram 

Deze usecase onderscheidt twee bedrijfsrollen, namelijk de Persoon en de (Zorg)Aanbieder zoals te zien in onderstaande tabel.
 
Tabel 1 Bedrijfsrollen 
 
| Bedrijfsrol (actor) | Beschrijving bedrijfsrol |
| --- | --- |
| Patiënt/ Persoon | Gebruiker van de PGO |
| (zorg)aanbieder | Gebruiker van het XIS |

### Informatieoverdracht
 
Zowel de persoon als de (zorg)aanbieder maken ieder gebruik van een informatiesysteem:
 
- PGO (persoon)
- XIS zorginformatiesysteem

#### Systemen & Systeemrollen 
Deze systemen kennen ieder verschillende systeemrollen, die het uitwisselen van gegevens tussen deze systemen mogelijk maken. Hier gaat het om de BgLZ+ geregistreerd bij de zorgaanbieders naar de persoon. Er is per granulaire gegevensdienst een systeemrol opgesteld. Deze systeemrollen staan beschreven in de MedMij STU3 Core pagina ofwel als het domeinspecifieke gegevens betreft zullen deze beschreven staan op deze pagina van het Functioneel ontwerp. Via tabel 2 zijn de gegevensdiensten en systeemrollen te vinden. 
 

### Transacties en Transactiegroepen 

Het uitwisselen van gegevens tussen de verschillende systeemrollen gebeurt op basis van transacties. Een transactie (bijvoorbeeld een vraag- en antwoordbericht) vormt een zogeheten transactiegroep. Voor de transacties die tussen de systeemrollen plaatsvinden, wordt in ART-DECOR beschreven welke gegevenselementen en met welke kardinaliteiten de gegevens uitgewisseld worden vanuit de BgLZ+. De gegevensdiensten staan gepubliceerd op [ART-DECOR](https://decor.nictiz.nl/ad/#/mm-bglzplus-/datasets/dataset/2.16.840.1.113883.2.4.3.11.60.151.1.1/2026-01-21T08:25:05). Alle gegevens zullen granulair uitgewisseld worden, wij wisselen dus niet ten alle tijden in een verzameling van gegevens uit voor de BgLZ+, maar in aparte FHIR resources. De BgLZ+ is samengesteld uit de [zib-publicatie 2017](https://zibs.nl/wiki/ZIB_Publicatie_2017(NL)) en er zijn twee profielen opgesteld voor de CIM 'Contact' met FHIR profiel 'lz-encounter' en CIM 'Dagrapportage' met FHIR profiel 'nl-core-nursingreport'. 

Voor de technische specificaties en FHIR implementation guide, zie de {{pagelink:TO, text:FHIR IG}}. 

Tabel 2 Transactiegroep voor verzamelen domeinspecifieke BgLZ+ HCIMs 

| Transactiegroep | Transactie | CIM Systeemrolcode  | Systeem | Bedrijfsrol | 
| --- | --- | --- | --- | --- |  
| Verzamelen Basisgegevens Langdurige Zorg+ Contact (CIM2026/STU3) 1.0.0-beta.1 (PULL) | Raadplegen Contact | BgLZplus-ENR-CIM2026/STU3-1.0.0-beta.1-FHIR| PGO | Patiënt | 
| Verzamelen Basisgegevens Langdurige Zorg+ Contact (CIM2026/STU3) 1.0.0-beta.1 (PULL)| Beschikbaar stellen Contact | BgLZplus-ENB-CIM2026/STU3-1.0.0-beta.1-FHIR| XIS | Zorgaanbieder | 
| Verzamelen Basisgegevens Langdurige Zorg+ Dagrapportage (CIM2026/STU3) 1.0.0-beta.1 (PULL) | Raadplegen Dagrapportage | BgLZplus-NRR-CIM2026/STU3-1.0.0-beta.1 | PGO | Patiënt | 
| Verzamelen Basisgegevens Langdurige Zorg+ Dagrapportage (CIM2026/STU3) 1.0.0-beta.1 (PULL)| Beschikbaar stellen Dagrapportage| BgLZplus-NRB-CIM2026/STU3-1.0.0-beta.1| XIS | Zorgaanbieder |

Tabel 3 Transactiegroep voor verzamelem CIMs MedMij Core

| Transactiegroep | Transactie | MedMij Core | Systeem | Bedrijfsrol | 
| --- | --- | --- | --- | --- |  
| Verzamelen MedMij Core - Alert (zib2017/STU3) 1.0.0-beta.1  (PULL) | Raadplegen Alert | [MedMij Core - Alert (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-Alert?version=1.0.0) | PGO | Patiënt | 
| Verzamelen MedMij Core - Alert (zib2017/STU3) 1.0.0-beta.1 (PULL)| Beschikbaar stellen Alert| [MedMij Core - Alert (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-Alert?version=1.0.0)  | XIS | Zorgaanbieder | 
| Verzamelen MedMij Core - Bloeddruk (zib2017/STU3) 1.0.0-beta.1  (PULL) | Raadplegen Bloeddruk |  [MedMij Core - Blood pressure (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BloodPressure?version=1.0.0) | PGO | Patiënt | 
| Verzamelen MedMij Core - Bloeddruk (zib2017/STU3) 1.0.0-beta.1 (PULL)| Beschikbaar stellen Bloeddruk| [MedMij Core - Blood pressure (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BloodPressure?version=1.0.0) | XIS | Zorgaanbieder | 
| Verzamelen MedMij Core - Lichaamslengte (zib2017/STU3) 1.0.0-beta.1  (PULL) | Raadplegen Lichaamslengte | [MedMij Core - Body height (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BodyHeight?version=1.0.0)  | PGO | Patiënt | 
| Verzamelen MedMij Core - Lichaamslengte (zib2017/STU3) 1.0.0-beta.1 (PULL) | Beschikbaar stellen Lichaamslengte| [MedMij Core - Body height (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BodyHeight?version=1.0.0) | XIS | Zorgaanbieder | 
| Verzamelen MedMij Core - Lichaamstemperatuur (zib2017/STU3) 1.0.0-beta.1 (PULL) | Raadplegen Lichaamstemperatuur | [MedMij Core - Body temperature (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BodyTemperature?version=1.0.0) | PGO | Patiënt | 
| Verzamelen MedMij Core - Lichaamstemperatuur (zib2017/STU3) 1.0.0-beta.1 (PULL) | Beschikbaar stellen Lichaamstemperatuur|[MedMij Core - Body temperature (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BodyTemperature?version=1.0.0) | XIS | Zorgaanbieder | 
| Verzamelen MedMij Core - Lichaamsgewicht (zib2017/STU3) 1.0.0-beta.1 (PULL) | Raadplegen Lichaamsgewicht | [MedMij Core - Body weight (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BodyWeight?version=1.0.0)  | PGO | Patiënt | 
| Verzamelen MedMij Core - Lichaamsgewicht (zib2017/STU3) 1.0.0-beta.1 (PULL)  | Beschikbaar stellen Lichaamsgewicht| [MedMij Core - Body weight (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BodyWeight?version=1.0.0)  | XIS | Zorgaanbieder | 
| Verzamelen MedMij Core - Vochtbalans (zib2017/STU3) 1.0.0-beta.1  (PULL) | Raadplegen Vochtbalans | [MedMij Core - Fluid balance (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-FluidBalance?version=1.0.0) | PGO | Patiënt | 
| Verzamelen MedMij Core - Vochtbalans (zib2017/STU3) 1.0.0-beta.1 (PULL) | Beschikbaar stellen Vochtbalans|[MedMij Core - Fluid balance (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-FluidBalance?version=1.0.0) | XIS | Zorgaanbieder | 
| Verzamelen MedMij Core - Woonsituatie (zib2017/STU3) 1.0.0-beta.1  (PULL) | Raadplegen Woonsituatie |  [MedMij Core - Living situation (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-LivingSituation?version=1.0.0)  | PGO | Patiënt | 
| Verzamelen MedMij Core - Woonsituatie (zib2017/STU3) 1.0.0-beta.1 (PULL) | Beschikbaar stellen Woonsituatie|[MedMij Core - Living situation (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-LivingSituation?version=1.0.0) | XIS | Zorgaanbieder |
| Verzamelen MedMij Core - Voedingsadvies (zib2017/STU3) 1.0.0-beta.1   (PULL) | Raadplegen Voedingsadvies | [MedMij Core - Nutrition Advice (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-NutritionAdvice?version=1.0.0)  | PGO | Patiënt | 
| Verzamelen MedMij Core - Voedingsadvies (zib2017/STU3) 1.0.0-beta.1 (PULL) | Beschikbaar stellen Voedingsadvies| [MedMij Core - Nutrition Advice (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-NutritionAdvice?version=1.0.0)  | XIS | Zorgaanbieder | 
| Verzamelen MedMij Core - Betaler (zib2017/STU3) 1.0.0-beta.1   (PULL) | Raadplegen Betaler | [MedMij Core - Payer (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-Payer?version=1.0.0) | PGO | Patiënt | 
| Verzamelen MedMij Core - Betaler (zib2017/STU3) 1.0.0-beta.1  (PULL) | Beschikbaar stellen Betaler| [MedMij Core - Payer (zib2017/STU3)](hhttps://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-Payer?version=1.0.0)  | XIS | Zorgaanbieder | 
| VVerzamelen MedMij Core - Polsfrequentie (zib2017/STU3) 1.0.0-beta.1  (PULL) | Raadplegen Polsfrequentie | [MedMij Core - Pulse rate (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-PulseRate?version=1.0.0)  | PGO | Patiënt | 
| Verzamelen MedMij Core - Polsfrequentie (zib2017/STU3) 1.0.0-beta.1 (PULL) | Beschikbaar stellen Polsfrequentie|[MedMij Core - Pulse rate (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-PulseRate?version=1.0.0)| XIS | Zorgaanbieder |
| Verzamelen MedMij Core - Ademhaling (zib2017/STU3) 1.0.0-beta.1 (PULL) | Raadplegen Ademhaling | [MedMij Core - Respiration (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-Respiration?version=1.0.0)  | PGO | Patiënt | 
| Verzamelen MedMij Core - Ademhaling (zib2017/STU3) 1.0.0-beta.1 (PULL) | Beschikbaar stellen Ademhaling|[MedMij Core - Respiration (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-Respiration?version=1.0.0) | XIS | Zorgaanbieder | 

