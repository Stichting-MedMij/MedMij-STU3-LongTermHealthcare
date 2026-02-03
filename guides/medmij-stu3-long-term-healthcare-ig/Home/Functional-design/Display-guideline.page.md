---
topic: Weergaverichtlijn
---
 
# Weergaverichtlijn
 
## Inleiding
Dit is de weergaverichtlijn voor gegevensdienst Verzamelen Basisgegevens Langdurige Zorg 3.0 (MedMij gegevensdienst 61). 

De richtlijn bevat mock-ups die bedoeld zijn ter inspiratie. Persoonlijke gezondheidsomgevingen (PGO’s) kunnen deze voorbeelden naar eigen inzicht visueel vormgeven, zolang de gebruiksvriendelijkheid behouden blijft.

## Doel
Deze richtlijn heeft als doel om duidelijke handvatten te bieden voor een patiëntvriendelijke en begrijpelijke weergave van langdurige zorg gegevens in PGO's. De richtlijn ondersteunt ontwikkelaars en zorgverleners bij het:
- gebruiken van begrijpelijke en patiëntvriendelijke termen en toelichtingen;
- structureren en presenteren van een overzicht van gegevens op een manier die aansluit bij de informatiebehoefte van PGO gebruikers.

De richtlijn geeft géén handvatten voor de vormgeving (kleur, vorm, lettertype, etc.) van gegevens.

## Scope
De scope bevat de gegevensdienst Verzamelen Basisgegevens Langdurige Zorg 3.0 voorzien van een aanvullende set gegevens BgLZ+ die worden weergegeven in de PGO. 

De richtlijn is ontwikkeld voor gegevens die verzameld worden via de Verzamelen Basisgegevens Langdurige Zorg 3.0 MedMij-gegevensdienst met de aanvullende gegevens set BgLZ+. Gegevens die via andere MedMij-gegevensdiensten verzameld worden in de PGO zijn hierin niet meegenomen.

## Inhoud richtlijn
Het inloggen en authentiseren bij de zorgaanbieder is niet opgenomen in deze richtlijn.
De gebruiker gaat in de PGO naar het langdurige zorgoverzicht en/of zorgorganisatie-langdurige zorgoverzicht waar de langdurige zorg gegevens getoond worden. 

### Overzichtsscherm langdurige zorggegevens
Er zijn twee weergaven gedefinieerd voor het overzicht van de langdurige zorggegevens:
- Scenario 1: Langdurige zorgoverzicht (met alle langdurige zorggegevens van alle zorgaanbieders in één overzicht)
- Scenario 2: Zorgorganisatie-Langdurige zorgoverzicht (met alle langdurige zorggegevens van één zorgaanbieder in één overzicht)

De twee scenario’s, hieronder uitgewerkt, geven weer hoe een UX design getoond kan worden. Een PGO is vrij om 1 of beide van deze scenario’s te ondersteunen. De richtlijn gaat ervan uit dat PGO’s een responsief ontwerp ondersteunen. 

In deze richtlijn hebben we twee voorbeeld mockups opgenomen ter inspiratie. Daaronder hebben we elke zib apart opgenomen, niet in mockup vorm maar in tabel vorm. De twee voorbeeld mockups gaan over afspraken, maar let op, de zib “contact” is apart opgenomen in tabelvorm. 

#### Voorbeeld mockup overzichtsschermen langdurige zorg
Langdurige zorg overzicht:

Het overzichtsscherm van elke zib heeft dus een aparte pagina waar de datavelden getoond worden, voor alle (langdurige zorg) zorgaanbieders.  

{{render: guides/medmij-stu3-long-term-healthcare-ig/images/Langdurige zorg overzicht.png}}

**Figuur 1 : Voorbeeld Langdurige zorg overzicht**

Zorgorganisatie-langdurige zorg overzicht

Het overzichtsscherm van elke zib heeft dus een aparte tab waar de datavelden getoond worden, per zorgaanbieder. 

{{render: guides/medmij-stu3-long-term-healthcare-ig/images/Zorgorganisatie overzicht.png}} 

**Figuur 2 : Voorbeeld Zorgorganisatie - langdurige zorg overzicht**

De acceptatiecriteria voor de overzichtsschermen van elke zib is als volgt.

| Nr | Acceptatiecriteria | 
| --- | --- | 
| 1 | Standaard worden alle gegevens van de geraadpleegde zorgaanbieder(s) weergegeven, gesorteerd op datum van jong naar oud.  | 
| 2 | Je kunt zoeken op (delen van) de gegevens of op informatie uit de andere datavelden in het overzichtsscherm. De gebruiker moet minimaal 3 karakters invoeren.  | 
| 3 | Voor de datavelden in het overzichtsscherm is het mogelijk om te filteren op één of meerdere waarden.  |
| 4 | Voor het dataveld Datum op kun je een specifieke periode selecteren.  | 
| 5 | Alle datavelden in het overzichtsscherm zijn sorteerbaar.  | 
| 6 | De datavelden in het overzichtsscherm zijn begrijpelijk en gebruiksvriendelijk geformuleerd. Zie de paragraaf Tabel met specificaties voor de aanbevolen termen per opgehaald dataveld.  | 

#### Detailoverzicht langdurige zorg
Dit detail scherm krijg je te zien als je een specifieke regel in het overzichtsscherm selecteert. 

#### Voorbeeld mockup detailoverzicht langdurige zorg

{{render: guides/medmij-stu3-long-term-healthcare-ig/images/Detailscherm LZ.png}} 

**Figuur 3 : Voorbeeld Detailoverzicht - langdurige zorg**

### Langdurige zorggegevens per zib
Hieronder worden alle langdurige zorg zibs in tabel vorm weergegeven. De zorgorganisatie in het overzichtsscherm en detailscherm is alleen nodig voor scenario 1. Deze is niet nodig voor scenario 2.

#### Contact

<u>Overzichtsscherm</u>

| Type contact | Begindatum | Begintijd | Zorgverlener | Zorgorganisatie |
| --- | --- | --- | --- | --- |
| advies over veilige en passende lichaamsbeweging | 30-03-2025 | 20:00 | Julia van den Bos | IJsselheem | 
| Controle voortgang revalidatie | 01-06-2025 | 11:00 | W. Bloem | IJsselheem | 

<u>Detailscherm</u>

| Geselecteerde regel : Advies over de veilige en 
passende lichaamsbeweging | Voorbeeldwaarde   | 
| --- | --- |
| Type contact | Thuis |
| Begin datum | 30-03-2025 |
| Begin tijd | 20:00 |
| Eind datum | 30-03-2025 |
| Eind tijd | 21:00 |
| Zorgverlener | Julia van den Bos |
| Zorgorganisatie | IJsselheem |
| Type contact uitleg | advies over veilige en passende lichaamsbeweging |

#### Dagrapportage [nl-core-nursingreport]

<u>Overzichtsscherm</u>

| Dagrapportage | Datum | Tijd | Zorgorganisatie |
| --- | --- | --- | --- |
| Dagrapportage | 15-03-2025 | 12:00 | IJsselheem | 
| Dagrapportage | 14-03-2025 | 16:45 | IJsselheem | 
| Dagrapportage | 07-03-2025 | 21:00 | IJsselheem | 

<u>Detailscherm</u>

| Geselecteerde regel : Dagrapportage 15-03-2025 12:00 |  Voorbeeldwaarde  | 
| --- | --- |
| Dagrapportage | Mevrouw vertoont toenemende stijfheid bij het opstaan en lopen. Er is sprake van fijne tremor in de rechterhand. Tijdens het ochtendcontact had zij moeite om zich verbaal uit te drukken; gebruikt korte zinnen met lange pauzes. Zelfstandig toiletbezoek is mogelijk, maar met risico op vallen. Advies: looprek binnen handbereik houden en logopedie betrekken voor spraakondersteuning. |
| Datum | 15-03-2025 |
| Tijd | 12:00 |
| Zorgorganisatie | IJsselheem |

## Tabel met specificaties
In de tabel met specificaties staan de gegevens uit de gegevensdienst Verzamelen Basisgegevens Langdurige Zorg 3.0, die relevant zijn voor deze weergaverichtlijn weergegeven. 
De prioriteit van de te tonen datavelden wordt vastgesteld volgens de MoSCoW-methodiek. Datavelden die niet in de specificatietabel voorkomen, moeten worden beschouwd als datavelden met de letter W.

| Prioriteit | Omschrijving |
| --- | --- |
| M(ust have) | Nodig voor de basisfunctionaliteit van de toepassing en moet worden geïmplementeerd om het proces succesvol te laten verlopen. |
| S(hould have) | Belangrijke functionaliteit die niet vereist is, maar die voordelen biedt voor gebruikers en de algehele gebruikservaring. |
| C(ould have) | Gewenste functionaliteit die waarde toevoegt, maar minder kritisch is en indien nodig kan worden uitgesteld. |
| W(on't have) | Functionaliteiten die nu buiten scope zijn maar mogelijk in de toekomst worden overwogen. |

| 1. Naam data item | 2. Type data item | 3. Voorbeeld | 4. Advies waar te tonen in PGO | 5. Advies tekst weergave in PGO | 6. Opmerkingen | 7. Prioriteit (MoSCoW) |
| --- | --- | --- | (a) in overzicht (b) als overzicht en detailgegeven (c) niet tonen | --- | --- | --- |
| Contact | Rootconcept | --- | --- | --- | --- | --- |
| Contacttype | Item | Thuis | a | Type contact of afspraak | (code = 'HH' in "codesystem Index - FHIR v5.0.0": "https://hl7.org/fhir/?utm_referrer=https%3A%2F%2Fwww.hl7.org%2F") | M |
| ContactMet: Zorgverlener | Reference | Julia van den Bos | a | Contact met | (nl-core-practioner-eov-cert-1-1b-01) | Zorgverlener naam: M 

Overige datavelden: W |
| Locatie: Zorgaanbieder | Reference | Ijsselheem | a | Locatie | --- | M |
| BeginDatumTijd | Item | 2025-03-30T10:20:00+00:00 | a | Begindatum en tijd | --- | M |
| EindDatumTijd | Item | 2025-03-30T10:20:30+00:00 | a | Einddatum en tijd | --- | M |
| RedenContact | Container | --- | --- | --- | --- | --- |
| Toelichting RedenContact | Item | --- | b | Type contact uitleg (of Type contact Toelichting) | --- | M |
| Contact::Probleem | Reference | --- | b | Probleem | --- | M |
| Contact::Verrichting | Reference | --- | b | Verrichting | --- | M |
| AfwijkendeUitslag | Item | --- | b | Afwijkende uitslag | --- | M |
| Herkomst | Item | --- | b | Herkomst | --- | M |
| Bestemming | Item | --- | b | Bestemming | --- | M |
| --- | --- | --- | --- | --- | --- | --- |
| Dagrapportage | Rootconcept | --- | a | Dagrapportage | --- | --- |
| ObservatieDatumTijd | Item | 2025-05-17T07:00:00+01:00 | b | Datum en Tijd| --- | M |
| Dagverslag (ObservatieNaam) | Item | Mevrouw vertoont toenemende stijfheid bij het opstaan en lopen. Er is sprake van fijne tremor in de rechterhand. Tijdens het ochtendcontact had zij moeite om zich verbaal uit te drukken; gebruikt korte zinnen met lange pauzes. Zelfstandig toiletbezoek is mogelijk, maar met risico op vallen. Advies: looprek binnen handbereik houden en logopedie betrekken voor spraakondersteuning. | b | Dagverslag | --- | M | 
| OberservatieMethode | Item | --- | b | Oberservatie methode | --- | M |
| Toelichting | Item | --- | b | Toelichting | --- | M |
| Zorgaanbieder | Reference | IJsselheem | a | Liefst geen afkortingen | Zorgorganisatie | Organisatienaam: M Overige datavelden: W |