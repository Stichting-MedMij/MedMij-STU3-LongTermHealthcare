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

Deze versie van de gegevensdiensten “Raadplegen BgLZ+” heeft betrekking op het raadplegen en beschikbaar stellen van zorginformatiebouwstenen die al beschikbaar zijn bij de zorgaanbieders in de XIS-systemen. De BgLZ+ is samengesteld uit de [zib-publicatie 2017](https://zibs.nl/wiki/ZIB_Publicatie_2017(NL)). De BgLZ+ zibs worden bovenop de Basisgegevensset Langdurige zorg (BgLZ) uitgewisseld. De BgLZ wordt in stand gehouden zoals die er nu staat, hier zullen geen wijzigingen in plaatsvinden. De BgLZ+ gaat over de extra zibs die naast de al bestaande BgLZ beschikbaar worden gesteld. De BgLZ zibs zijn te vinden via [ART DECOR BGLZ](https://decor.nictiz.nl/ad/#/lanzo-/datasets/dataset/2.16.840.1.113883.2.4.3.11.60.58.1.1/2019-04-04T16:57:35) en de BgLZ+ zibs zijn te vinden via [ART DECOR BGLZ+](https://decor.nictiz.nl/ad/#/mm-bglzplus-/datasets/dataset)

### Infrastructuur 

Geen nadere specificatie, anders dan genoemd in de [algemene inleiding](https://informatiestandaarden.nictiz.nl/wiki/MedMij:FO:V1/FunctioneelOntwerp#Infrastructuur) van de MedMij functionele ontwerpen. 

### Geografische reikwijdte 

Geen nadere specificatie, anders dan genoemd in [de algemene inleiding](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/Ontwerpen#Geografische_reikwijdte) van de MedMij functionele ontwerpen. 

### Kwalificatie en testen 

Op dit moment wordt de usecase uit dit ontwerp getoetst in een pilot.

## Usecases 

### Algemeen 

Een usecase is een specifieke beschrijving van een praktijksituatie in de langdurige zorg waarbij voor een concrete situatie het uitwisselen van informatie wordt beschreven aan de hand van actoren (mensen, systemen) en transacties (welke informatie wordt wanneer uitgewisseld). Een usecase is een verbijzondering van een specifiek onderdeel van het zorgproces in de langdurige zorg.   

### Granulair raadplegen aanvullende gegevensset Langdurige zorg 
We stappen in deze pilot af van het monolithische concept als één grote gegevensdienst,en gaan toe naar granulaire uitwisseling en kwalificatie op het niveau van afzonderlijke zibs/FHIR-profielen. 
 
In het huidige Medmij-Afsprakenstelsel is de Basisgegevensset Langdurige Zorg één gegevensdienst waarin een vastgestelde set van FHIR-profielen (op basis van zibs) als geheel moet worden ondersteund. We willen met de aanvullende gegevensset langdurige zorg toe naar een situatie waarbij elke zib (en dus elk FHIR-profiel) wordt beschouwd als een losstaande gegevensdienst met een eigen: 

- Specificaties (zib + bijhorende FHIR-profielen) 
- Kwalificatiecriteria 
- Testscenario’s 

Wat blijft hetzelfde? 

- De zibs blijven leidend als informatiemodel 
- De keten (bronsysteem > DVA > PGO) blijft bestaan 
- Authenticatie, autorisatie, adressering en logging blijven conform het Medmij-afpsrakenstelsel. 

### Doel en relevantie granulair raadplegen gegevens Langdurige zorg 

De gegevens voor uitwisseling in eerste instantie gebaseerd op de gegevensset Minimale eOverdracht (MeO) v4.0 zie voor meer informatie over welke zibs binnen de eOverdracht in scope zijn de Nictiz wiki pagina  [algemeen overzicht van de inhoudelijke opbouw van de gehele eOverdracht.](https://informatiestandaarden.nictiz.nl/wiki/vpk:V4.0_Opbouw_eOverdracht_algemeen). Via de [landingspagina Verpleegkundige zorg](https://informatiestandaarden.nictiz.nl/wiki/Landingspagina_Verpleegkundige_Zorg) is de meest actuele eOverdracht informatiestandaard te bekijken, deze richt zich op overdracht van een patiënt/cliënt tussen zorginstellingen.

Het scenario eOverdracht is voor zorgaanbieder – zorgaanbieder uitwisseling ingericht. Deze set van gegevens worden met dit functioneel ontwerp ontsloten naar de Patiënt via de PGO. Wij zullen zoveel als mogelijk verwijzen naar de Nictiz pagina gezien de zibs van zorgaanbieder- zorgaanbieder uitwisseling ook naar de PGO ontsloten kunnen worden. 

Naast de Miniale eOverdracht zibs zijn er nog extra metingen en een dagrapportage (nl-core-nursingreport) beschikbaar bij de bronleverancier, ook deze zullen met de BgLZ+ granulair ontsloten worden naar de PGO.

Naast de BgLZ gaan er meer gegevens granulair beschikbaar worden gesteld, verder genoemd BgLZ+. Specifiek gaat het om onderstaande zibs: 

| Standaard| Zorginformatiebouwsteen|
| --- | --- |
| Minimale eOverdracht Volwassenen | zib Bloeddruk | 
| Minimale eOverdracht Volwassenen | zib Lichaamslengte | 
| Minimale eOverdracht Volwassenen | zib Lichaamsgewicht | 
| Minimale eOverdracht Volwassenen | zib Alert | 
| Minimale eOverdracht Volwassenen | zib Voedingsadvies | 
| Minimale eOverdracht Volwassenen | zib Woonsituatie | 
| Minimale eOverdracht Volwassenen | zib Betaler | 
| Minimale eOverdracht Volwassenen | zib Contact | 
| BgLZ+ - Meting | zib Lichaamstemperatuur | 
| BgLZ+ - Meting | zib Vochtbalans | 
| BgLZ+ - Meting | zib Ademhaling | 
| BgLZ+ - Meting | zib Polsfrequentie | 
| BgLZ+ - Verslag | CIM nl-core-nursingreport | 


Niet alle zibs die in de BgLZ+ uitgewisseld worden zijn bij elke bronleverancier beschikbaar. Gezien wij een granulaire gegevensset opstellen zal het niet verplicht zijn om alle zibs uit te wisselen voor kwalificatie, dit zal per leverancier gecommuniceerd en gerapporteerd worden. Meer informatie over granulair uitwisselen kan gevonden worden via de [MedMij STU3 Core](https://simplifier.net/guide/medmij-stu3-core-ig?version=current) pagina. Op deze pagina staan alle domeinoversteigende gegevensdiensten gepubliceerd. 

### Ontwerp granulair uitwisselen 

{{render: guides/medmij-stu3-long-term-healthcare-ig/images/Granulair_LZ.png}}

#### Patient journey aanvullende gegevensset langdurige zorg  

De patient journey beschrijft enkele momenten waarop je als patiënt zijnde inzicht kan of zou willen hebben in zijn langdurige zorggegevens.

In de landurige zorg zijn er veel verschillende patiëntreizen te onderscheiden. Onderstaand is één patiëntreis beschreven. De eOverdracht is een use-case waarbij het gaat om eenmalige overdracht van gegevens, zoals op vastgelegd moment van overdracht. Dit is een redelijk algemene patiëntreis en toch zijn er vele andere denkbaar. In overleg met de zorgaanbieders en leveranciers zullen we later een of meer patiëntreizen uitwerken.  Er zijn eerder meer patiëntreizen beschreven, onder andere in opdracht van Platform IZO (zie document Het netwerk in de praktijk, 31-03-2022) en ook door Nictiz (Casus Kenneth van Someren -  https://informatiestandaarden.nictiz.nl/images/a/a6/Casus_Kenneth_van_Someren_MedMij.pdf).   

Hieronder een voorbeeld van patiëntreis van denkbeeldige patiënt Peter (eigenlijk spreekt men in de langdurige zorg meestal van cliënt) en de gegevensuitwisseling binnen de langdurige zorg tussen zorgaanbieder en patiënt. Gezien het voor de aanvullende gegevensset langdurige zorg uitwisseling naar de PGO betreft is onderstaand een specifieke patientreis geschetst waarbij gegevens geraadpleegt worden vanuit de PGO:  

Peter is een actieve weduwnaar van 72 jaar oud. Peter heeft drie kinderen, twee zoons, een dochter en vijf kleinkinderen. Thuis had Peter al steeds meer hulp nodig, zo kan hij onder andere moeilijk zelf douchen en het bijhouden van zijn medicatie vindt hij ook lastig. Peter heeft daardoor, de afgelopen vijf jaar, veel wijkverpleging op bezoek gehad gezien hij hulp nodig had met zijn Algemene Dagelijkse Levensverrichtingen (ADL).   

Een maand geleden is Peter getroffen door een hersenbloeding (CVA). Er wordt nu een opname in een verpleeghuis overwogen. Het is namelijk niet de verwachting dat hij voldoende zal herstellen gezien hij door zijn hersenbloeding halfzijdig verlamd is geraakt. In de wijk waar Peter woont, is een locatie gevestigd en daar zou hij graag naar toe willen. In samenspraak met Peter, zijn dochter en het verpleeghuis wordt een indicatie aangevraagd bij het CIZ.   

Peter is door de vele zorgverleners die hij de afgelopen tijd heeft ontmoet het overzicht kwijtgeraakt over zijn zorg en wil hier nog eens naar kijken. Bovendien was er te weinig tijd tijdens het consult om hierover door te praten met zijn zorgverlener.  

Op aanraden van zijn dochter heeft Peter nu een eigen gekozen PGO. In zijn PGO wil Peter zijn aanvullende gegevensset langdurige zorggegevens raadplegen, hij is nieuwsgierig naar deze gegevens. Zijn dochter kijkt mee, die is bij Peter op visite. Hij wil deze gegevens graag thuis inzien zonder dat hij daarvoor de zorgverlener hoeft te belasten. Bovendien hoeft hij dan zelf nergens naartoe te gaan. Hij raadpleegt via zijn PGO de betreffende zorgaanbieder waar hij onder behandeling is om zijn aanvullende gegevensset landurige zorggegevens op te halen en in te zien. Peter ziet nu zijn medische gegevens, waardoor hij meer inzicht heeft in de status van zijn gezondheid.

#### Preproces 

- De cliënt beschikt over een eigen PGO dat aan de MedMij-eisen voldoet.  
- De cliënt heeft toestemming gegeven voor het elektronisch uitwisselen van medische gegevens tussen het betreffende XIS/EPD en de eigen persoonlijke gezondheidsomgeving. 
- Er is sprake van een dossier voor de cliënt binnen de langdurige zorg sector.   

#### Proces 

- De cliënt raadpleegt de ‘bloeddruk’ in zijn of haar PGO.
- Het systeem van de cliënt (PGO) vraagt om beschikbare medische gegevens bij een XIS/EPD aan de hand van een zoekopdracht.
- Het systeem van de zorgaanbieder (XIS) stelt de anvullende gegevensset Langdurige zorg beschikbaar voor de patiënt.

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
Deze systemen kennen ieder verschillende systeemrollen, de systeemrollen zijn per granulair gegeven in het hoofdstuk Transacties en Transactiegroepen gedefinieerd. Hier gaat het om de BgLZ+ geregistreerd bij de zorgaanbieders naar de persoon.  
 

### Transacties en Transactiegroepen 

Het uitwisselen van gegevens tussen de verschillende systeemrollen gebeurt op basis van transacties. Een transactie (bijvoorbeeld een vraag- en antwoordbericht) vormt een zogeheten transactiegroep. Voor de transacties die tussen de systeemrollen plaatsvinden, wordt in ART-DECOR beschreven welke gegevenselementen en met welke kardinaliteiten de gegevens uitgewisseld worden vanuit de minimale eOverdracht. De gegevenselementen van de Minimale eOverdracht staan gepubliceerd op 
[ART-DECOR](https://decor.nictiz.nl/decor/services/RetrieveTransaction?language=nl-NL&version=2021-05-10T09%3A35%3A29&hidecolumns=45ghi&id=2.16.840.1.113883.2.4.3.11.60.30.4.39&effectiveDate=2021-01-27T00%3A00%3A00&format=html). Daarbij hebben wij een Excel weergave opgesteld met de gehele dataset Basisgegevensset langdurige zorg en de BgLZ+ voor testdoeleinden. Alle gegevens zullen granulair uitgewisseld worden, wij wisselen dus niet in bundles van gegevens uit binnen dit project echter in aparte FHIR resources.

Voor de technische specificaties en FHIR implementation guide, zie de {{pagelink:TO, text:FHIR IG}}. 

Tabel 2 Transactiegroep

| Transactiegroep | Transactie | Systeemrolcode | Systeem | Bedrijfsrol | 
| --- | --- | --- | --- | --- |  
| Verzamelen BgLZ+ (PULL) | Raadplegen Granulair gegeven Bloeddruk |  BP-v3.1R-FHIR  | PGO | Patiënt | 
| Verzamelen BgLZ+ | Beschikbaar stellen Granulair gegeven Bloeddruk|  BP-v3.1B-FHIR  | XIS | Zorgaanbieder | 
| Verzamelen BgLZ+ (PULL) | Raadplegen Granulair gegeven Lichaamslengte | BH-v3.1R-FHIR  | PGO | Patiënt | 
| Verzamelen BgLZ+ | Beschikbaar stellen Granulair Lichaamslengte| BH-v3.1B-FHIR | XIS | Zorgaanbieder | 
| Verzamelen BgLZ+ (PULL) | Raadplegen Granulair gegeven Lichaamsgewicht | BW-v3.1R-FHIR   | PGO | Patiënt | 
| Verzamelen BgLZ+ | Beschikbaar stellen Granulair Lichaamsgewicht| BW-v3.1B-FHIR  | XIS | Zorgaanbieder | 
| Verzamelen BgLZ+ (PULL) | Raadplegen Granulair gegeven Alert | BP-v3.1R-FHIR  | PGO | Patiënt | 
| Verzamelen BgLZ+ | Beschikbaar stellen Granulair Alert| BP-v3.1B-FHIR  | XIS | Zorgaanbieder | 
| Verzamelen BgLZ+ (PULL) | Raadplegen Granulair gegeven Voedingsadvies | NA-v3.1R-FHIR  | PGO | Patiënt | 
| Verzamelen BgLZ+ | Beschikbaar stellen Granulair Voedingsadvies| NA-v3.1B-FHIR  | XIS | Zorgaanbieder | 
| Verzamelen BgLZ+ (PULL) | Raadplegen Granulair gegeven Woonsituatie |  LS-v3.1R-FHIR  | PGO | Patiënt | 
| Verzamelen BgLZ+ | Beschikbaar stellen Granulair Woonsituatie|LS-v3.1B-FHIR | XIS | Zorgaanbieder | 
| Verzamelen BgLZ+ (PULL) | Raadplegen Granulair gegeven Betaler | PAY-v3.1R-FHIR | PGO | Patiënt | 
| Verzamelen BgLZ+ | Beschikbaar stellen Granulair gegeven Betaler| PAY-v3.1B-FHIR  | XIS | Zorgaanbieder | 
| Verzamelen BgLZ+ (PULL) | Raadplegen Granulair gegeven Contact | ENC-v3.1R-FHIR | PGO | Patiënt | 
| Verzamelen BgLZ+ | Beschikbaar stellen Granulair gegeven Contact| ENC-v3.1B-FHIR | XIS | Zorgaanbieder | 
| Verzamelen BgLZ+ (PULL) | Raadplegen Granulair gegeven Lichaamstemperatuur | BT-v3.1R-FHIR | PGO | Patiënt | 
| Verzamelen BgLZ+ | Beschikbaar stellen Granulair Lichaamstemperatuur|BT-v3.1B-FHIR | XIS | Zorgaanbieder | 
| Verzamelen BgLZ+ (PULL) | Raadplegen Granulair gegeven Vochtbalans | FB-v1.0R-FHIR  | PGO | Patiënt | 
| Verzamelen BgLZ+ | Beschikbaar stellen Granulair Vochtbalans|FB-v1.0R-FHIR | XIS | Zorgaanbieder | 
| Verzamelen BgLZ+ (PULL) | Raadplegen Granulair gegeven Ademhaling | RES-v3.1R-FHIR  | PGO | Patiënt | 
| Verzamelen BgLZ+ | Beschikbaar stellen Granulair Ademhaling|RES-v3.1B-FHIR | XIS | Zorgaanbieder | 
| Verzamelen BgLZ+ (PULL) | Raadplegen Granulair gegeven Polsfrequentie | PR-v3.1R-FHIR  | PGO | Patiënt | 
| Verzamelen BgLZ+ | Beschikbaar stellen Granulair Polsfrequentie|PR-v3.1R-FHIR| XIS | Zorgaanbieder |
| Verzamelen BgLZ+ (PULL) | Raadplegen Granulair gegeven Dagrapportage | NR-v3.1R-FHIR  | PGO | Patiënt | 
| Verzamelen BgLZ+ | Beschikbaar stellen Granulair Dagrapportage| NR-v3.1R-FHIR | XIS | Zorgaanbieder |


### Activity diagram 

{{render: guides/medmij-stu3-long-term-healthcare-ig/images/Activity diagram.png}}

### Weergaverichtlijn

#### Scope weergaverichtlijn 
- Het betreft een richtlijn. PGO-leveranciers hebben zelf de keuze of zij (delen van de) richtlijn toepassen voor de weergave van langdurige zorggevens.

De richtlijn geeft handvatten voor:
- het gebruik van patiëntvriendelijke termen en toelichting;
- de inhoud van het overzicht van langdurige zorggegevens in de PGO.

De richtlijn geeft géén handvatten voor de vormgeving (kleur, vorm, lettertype, etc.) van langdurige zorggegevens. 

### Inhoud weergaverichtlijn
De weergaverichtlijnen voor de langdurige zorggegevens zijn [hier](https://medmij.atlassian.net/wiki/spaces/IER/pages/478969857/Weergaverichtlijn+Langdurige+Zorg+Beta+versie) te vinden.

