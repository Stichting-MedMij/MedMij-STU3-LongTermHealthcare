---
topic: FO
---

# Functioneel ontwerp

## Algemeen 
Dit ontwerp beschrijft de databeschikbaarheid richting de persoon voor de Basisgegevens Langdurige Zorg+ (BgLZ+). Hierdoor kan de persoon zijn relevante langdurigezorggegevens bekijken via de PGO om een beter en vollediger inzicht te krijgen in de eigen medische situatie.​ In het vervolg wordt de term 'patiënt' gebruikt om de persoon aan te duiden, maar hier kan ook 'cliënt' of 'burger' gelezen worden. De term 'cliënt' is gebruikelijk binnen de langdurige zorg.

Dit functioneel ontwerp beschrijft de BgLZ+, die een uitbreiding vormt op de [Basisgegevensset Langdurige zorg (BgLZ)](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/OntwerpLangdurigeZorg). De BgLZ+ heeft betrekking op enkele aanvullende klinische informatiemodellen (Clinical Information Models, CIM's) die naast de BgLZ verzameld kunnen worden via de PGO. Deze uitbreiding van de BgLZ richt zich in eerste instantie op zorginformatiebouwstenen (zibs) uit [Publicatie 2017](https://zibs.nl/wiki/ZIB_Publicatie_2017(NL)) die onderdeel zijn van de door Nictiz gepubliceerde informatiestandaard [Minimale eOverdracht (MeO), versie 4.0](https://informatiestandaarden.nictiz.nl/wiki/Landingspagina_Verpleegkundige_Zorg).

De gegevens van de BgLZ+ worden op een granulaire wijze uitgewisseld. Dit houdt in dat elke CIM binnen de BgLZ+ los opgevraagd en uitgewisseld kan worden, en dat voor elke CIM een zogenaamde granulaire gegevensdienst is gedefinieerd. Meer informatie over granulaire uitwisseling is te vinden in de [MedMij STU3 Core IG](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-exchange?version=1.0.0).

Omdat de BgLZ+ een uitbreiding vormt op de BgLZ, worden de langdurigezorggegevens uitgewisseld door een combinatie van de BgLZ (waarvan de huidige usecase in stand wordt gehouden) en de BgLZ+. Merk op dat uitwisseling van de BgLZ geen vereiste is voor het uitwisselen van de BgLZ+: implementaties kunnen ervoor kiezen zowel de BgLZ als BgLZ+ uit te wisselen, alleen de BgLZ (buiten scope van deze IG) of alleen (een deel van) de BgLZ+.

Merk op dat naast dit ontwerp ook de (functionele) eisen en richtlijnen beschreven in de [MedMij STU3 Core IG](https://simplifier.net/guide/medmij-stu3-core-ig?version=1.0.0) en de door Nictiz gepubliceerde [Ontwerpen MedMij, versie 2020.02](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/Ontwerpen) van toepassing zijn.

### Doelgroep
De doelgroep voor deze pagina wijkt niet af van de [algemene doelgroep](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/Ontwerpen#Doelgroep) van de functionele onderwerpen binnen MedMij. 

### Kaders en uitgangspunten

### Richtlijn en proces 
Dit ontwerp is conform specificaties genoemd in de [algemene inleiding](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/Ontwerpen#Richtlijn) van de functionele onderwerpen binnn MedMij.

### Reikwijdte
De reikwijdte van dit ontwerp beslaat de functionele beschrijvingen en de dataset voor de gegevensuitwisselingen die voortvloeien uit uitgevoerde langdurige zorg. 

### Infrastructuur
Geen nadere specificatie, anders dan genoemd in de [algemene inleiding](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/Ontwerpen#Infrastructuur) van de functionele onderwerpen binnn MedMij.

### Geografische reikwijdte
Geen nadere specificatie, anders dan genoemd in de [algemene inleiding](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/Ontwerpen#Geografische_reikwijdte) van de functionele onderwerpen binnen MedMij.

### Kwalificatie en testen
Op dit moment wordt de usecase uit dit ontwerp getoetst in een Proof of Concept (PoC). Later volgt meer informatie over kwalificatie.

## Usecases

### Algemeen
Een usecase is een specifieke beschrijving van een praktijksituatie waarbij voor een concrete situatie het uitwisselen van informatie wordt beschreven aan de hand van actoren (mensen, systemen) en transacties (welke informatie wordt wanneer uitgewisseld). Een usecase is een verbijzondering van een specifiek onderdeel van het zorgproces. In dit ontwerp zijn usecases binnen de langdurige zorg in scope.

### Doel en relevantie granulair raadplegen BgLZ+
Het doel is om het voor patiënten mogelijk te maken om regie te nemen op hun eigen gezondheid door inzicht te geven over de langdurigezorggegevens die over henzelf gaan.

#### Patiëntreis BgLZ+
Een patiëntreis beschrijft enkele momenten waarop een patiënt inzicht kan of zou willen hebben in zijn zorggegevens. In de langdurige zorg zijn er veel verschillende patiëntreizen te onderscheiden. Hieronder is één patiëntreis beschreven, maar er zijn door andere partijen meer patiëntreizen beschreven, onder andere in opdracht van Platform IZO (zie [Het netwerkmodel in de praktijk](https://infoizo.nl/nieuws/bericht/het-netwerkmodel-de-praktijk)) en ook door Nictiz ([Casus Kenneth van Someren](https://informatiestandaarden.nictiz.nl/images/a/a6/Casus_Kenneth_van_Someren_MedMij.pdf)). De patiëntreis hieronder gaat over een denkbeeldige patiënt Peter en de uitwisseling van langdurigezorggegevens tussen zorgaanbieder en patiënt (via de PGO).

Peter is een actieve weduwnaar van 72 jaar oud. Peter heeft drie kinderen, twee zoons en een dochter, en vijf kleinkinderen. Thuis had Peter al steeds meer hulp nodig, zo kan hij onder andere moeilijk zelf douchen en het bijhouden van zijn medicatie vindt hij ook lastig. Peter heeft daardoor de afgelopen vijf jaar veel wijkverpleging op bezoek gehad, aangezien hij hulp nodig had met zijn Algemene Dagelijkse Levensverrichtingen (ADL).   

Een maand geleden is Peter getroffen door een hersenbloeding (CVA). Er wordt nu een opname in een verpleeghuis overwogen. Het is namelijk niet de verwachting dat hij voldoende zal herstellen, omdat hij door zijn hersenbloeding halfzijdig verlamd is geraakt. In de wijk waar Peter woont, is een locatie gevestigd en daar zou hij graag naartoe willen. In samenspraak met Peter, zijn dochter en het verpleeghuis wordt een indicatie aangevraagd bij het CIZ.   

Peter is door de vele zorgverleners die hij de afgelopen tijd heeft ontmoet het overzicht kwijtgeraakt over zijn zorg en wil hier nog eens naar kijken. Bovendien was er te weinig tijd tijdens het consult om hierover door te praten met zijn zorgverlener.  

Op aanraden van zijn dochter heeft Peter nu een eigen gekozen PGO. In zijn PGO wil Peter zijn BgLZ+-gegevens raadplegen, omdat hij nieuwsgierig is naar deze gegevens. Zijn dochter kijkt mee wanneer ze bij hem op visite is. Hij wil deze gegevens graag thuis inzien zonder dat hij daarvoor de zorgverlener hoeft te belasten. Bovendien hoeft hij dan zelf nergens naartoe te gaan. Hij raadpleegt via zijn PGO de betreffende zorgaanbieder waar hij onder behandeling is om zijn BgLZ+-gegevens op te halen en in te zien. Peter ziet nu zijn medische gegevens, waardoor hij meer inzicht heeft in de status van zijn gezondheid.

#### Preproces
- De patiënt beschikt over een eigen PGO dat aan de MedMij-eisen voldoet.  
- De patiënt heeft toestemming gegeven voor het elektronisch uitwisselen van medische gegevens tussen het betreffende XIS en de eigen persoonlijke gezondheidsomgeving. 
- Er is sprake van een dossier voor de patiënt binnen de sector langdurige zorg.   

#### Proces
- De patiënt raadpleegt zijn langdurigezorggegevens in zijn PGO.
- Het systeem van de patiënt (PGO) vraagt om beschikbare medische gegevens bij een XIS aan de hand van een zoekopdracht.
- Het systeem van de zorgaanbieder (XIS) stelt de gevraagde gegevens beschikbaar voor de patiënt.

#### Postproces
- In de PGO van de patiënt worden de opgevraagde gegevens overzichtelijk en begrijpelijk getoond.  

### Bedrijfsrollen
Deze usecase onderscheidt twee bedrijfsrollen, namelijk de *Patiënt* en de *Zorgaanbieder*, zoals te zien in onderstaande tabel.
 
| Bedrijfsrol (actor) | Beschrijving |
| --- | --- |
| Patiënt | Gebruiker van de PGO |
| Zorgaanbieder | Gebruiker van het XIS |

**Tabel 1: Bedrijfsrollen**

### Informatieoverdracht
Zowel de patiënt als de zorgaanbieder maken ieder gebruik van een informatiesysteem:

- PGO (patiënt)
- XIS (zorgaanbieder)

#### Systemen en systeemrollen
Deze systemen kennen ieder verschillende systeemrollen, die het uitwisselen van gegevens tussen deze systemen mogelijk maken. Hier gaat het om de BgLZ+-gegevens die zijn geregistreerd bij de zorgaanbieder naar de patiënt. Aangezien de BgLZ+ wordt uitgewisseld door middel van granulaire gegevensdiensten, is er per gegevensdienst een systeemrol opgesteld. De systeemrollen worden hier niet expliciet benoemd, maar zijn onderdeel van de specificatie van de individuele granulaire gegevensdiensten.
 
### Transacties en transactiegroepen
Het uitwisselen van gegevens tussen de verschillende systeemrollen gebeurt op basis van transacties. Een verzameling van transacties (bijvoorbeeld een vraag- en antwoordbericht) vormt een zogeheten transactiegroep. Voor de transacties die tussen de systeemrollen plaatsvinden, wordt in [ART-DECOR](https://decor.nictiz.nl/ad/#/mm-bglzplus-/datasets/dataset/2.16.840.1.113883.2.4.3.11.60.151.1.1/2026-01-21T08:25:05) beschreven welke gegevenselementen uitgewisseld worden binnen de BgLZ+. Voor de technische specificaties, zie het {{pagelink: TD, text: technisch ontwerp}}.

De onderstaande tabel geeft een overzicht van alle granulaire gegevensdiensten die van toepassing zijn voor de BgLZ+. Merk op dat de domeinoverstijgende gegevensdiensten in de MedMij STU3 Core IG worden beschreven, terwijl domeinspecifieke gegevensdiensten in deze IG worden beschreven. Op dit moment zijn er alleen domeinoverstijgende gegevensdiensten opgenomen.

| Id | Gegevensdienstnaam zonder versie | Versie |
| --- | --- | --- | --- |
| 900000404 | [Verzamelen MedMij Core - Alert (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-Alert?version=1.0.0) | 1.0.0-beta.1 |
| 900000401 | [Verzamelen MedMij Core - Bloeddruk (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BloodPressure?version=1.0.0) | 1.0.0-beta.1 |
| 900000402 | [Verzamelen MedMij Core - Lichaamslengte (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BodyHeight?version=1.0.0) | 1.0.0-beta.1 |
| 900000409 | [Verzamelen MedMij Core - Lichaamstemperatuur (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BodyTemperature?version=1.0.0) | 1.0.0-beta.1 |
| 900000403 | [Verzamelen MedMij Core - Lichaamsgewicht (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BodyWeight?version=1.0.0) | 1.0.0-beta.1 |
| 900000410 | [Verzamelen MedMij Core - Vochtbalans (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-FluidBalance?version=1.0.0) | 1.0.0-beta.1 |
| 900000406 | [Verzamelen MedMij Core - Woonsituatie (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-LivingSituation?version=1.0.0) | 1.0.0-beta.1 |
| 900000405 | [Verzamelen MedMij Core - Voedingsadvies (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-NutritionAdvice?version=1.0.0) | 1.0.0-beta.1 |
| 900000407 | [Verzamelen MedMij Core - Betaler (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-Payer?version=1.0.0) | 1.0.0-beta.1 |
| 900000412 | [Verzamelen MedMij Core - Polsfrequentie (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-PulseRate?version=1.0.0) | 1.0.0-beta.1 |
| 900000411 | [Verzamelen MedMij Core - Ademhaling (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-Respiration?version=1.0.0) | 1.0.0-beta.1 |

**Tabel 2: Granulaire gegevensdiensten relevant voor BgLZ+**

### Weergaverichtlijn

#### Scope weergaverichtlijn 
- Het betreft een richtlijn. PGO-leveranciers hebben zelf de keuze of zij (delen van de) richtlijn toepassen voor de weergave van langdurigezorggegevens.

De richtlijn geeft handvatten voor:
- het gebruik van patiëntvriendelijke termen en toelichting;
- de inhoud van het overzicht van langdurigezorggegevens in de PGO.

De richtlijn geeft géén handvatten voor de vormgeving (kleur, vorm, lettertype, etc.) van langdurigezorggegevens. 

### Inhoud weergaverichtlijn
De weergaverichtlijn voor Langdurige Zorg is [hier](https://medmij.atlassian.net/wiki/spaces/IER/pages/478969857/Weergaverichtlijn+Langdurige+Zorg+Beta+versie) te vinden.