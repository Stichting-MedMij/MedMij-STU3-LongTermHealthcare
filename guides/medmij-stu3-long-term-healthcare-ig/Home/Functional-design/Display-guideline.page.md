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

**Figuur 1: Voorbeeld Langdurige zorg overzicht**

Zorgorganisatie-langdurige zorg overzicht

Het overzichtsscherm van elke zib heeft dus een aparte tab waar de datavelden getoond worden, per zorgaanbieder. 

{{render: guides/medmij-stu3-long-term-healthcare-ig/images/Zorgorganisatie overzicht.png}} 

**Figuur 2: Voorbeeld Zorgorganisatie - langdurige zorg overzicht**

De acceptatiecriteria voor de overzichtsschermen van elke zib is als volgt.

| Nr | Acceptatiecriteria | 
| --- | --- | 
| 1 | Standaard worden alle gegevens van de geraadpleegde zorgaanbieder(s) weergegeven, gesorteerd op datum van jong naar oud. | 
| 2 | Je kunt zoeken op (delen van) de gegevens of op informatie uit de andere datavelden in het overzichtsscherm. De gebruiker moet minimaal 3 karakters invoeren. | 
| 3 | Voor de datavelden in het overzichtsscherm is het mogelijk om te filteren op één of meerdere waarden. |
| 4 | Voor het dataveld Datum op kun je een specifieke periode selecteren. | 
| 5 | Alle datavelden in het overzichtsscherm zijn sorteerbaar. | 
| 6 | De datavelden in het overzichtsscherm zijn begrijpelijk en gebruiksvriendelijk geformuleerd. Zie de paragraaf Tabel met specificaties voor de aanbevolen termen per opgehaald dataveld. | 

#### Detailoverzicht langdurige zorg
Dit detail scherm krijg je te zien als je een specifieke regel in het overzichtsscherm selecteert. 

#### Voorbeeld mockup detailoverzicht langdurige zorg

{{render: guides/medmij-stu3-long-term-healthcare-ig/images/Detailscherm LZ.png}} 

**Figuur 3: Voorbeeld Detailoverzicht - langdurige zorg**

### Langdurige zorggegevens per zib
Hieronder worden alle langdurige zorg zibs in tabel vorm weergegeven. De zorgorganisatie in het overzichtsscherm en detailscherm is alleen nodig voor scenario 1. Deze is niet nodig voor scenario 2.

#### Contact

<u>Overzichtsscherm</u>

| Type contact | Begindatum | Begintijd | Zorgverlener | Zorgorganisatie |
| --- | --- | --- | --- | --- |
| advies over veilige en passende lichaamsbeweging | 30-03-2025 | 20:00 | Julia van den Bos | IJsselheem | 
| Controle voortgang revalidatie | 01-06-2025 | 11:00 | W. Bloem | IJsselheem | 

<u>Detailscherm</u>

| Geselecteerde regel: advies over de veilige en passende lichaamsbeweging | Voorbeeldwaarde | 
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

| Geselecteerde regel: Dagrapportage 15-03-2025 12:00 |  Voorbeeldwaarde | 
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

| 1. Naam data item | 2. Type data item | 3. Voorbeeld | 4. Advies waar te tonen in PGO <br/> (a) in overzicht <br/> (b) als overzicht en detailgegeven <br/> (c) niet tonen | 5. Advies tekst weergave in PGO | 6. Opmerkingen | 7. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |
| **Contact** | **Rootconcept** | | a | Contact | | |
| Contacttype | Item | Thuis | a | Type contact of afspraak | (code = 'HH' in "codesystem Index - FHIR v5.0.0": "https://hl7.org/fhir/?utm_referrer=https%3A%2F%2Fwww.hl7.org%2F") | M |
| ContactMet: Zorgverlener | Reference | Julia van den Bos | a | Contact met | (nl-core-practioner-eov-cert-1-1b-01) | Zorgverlener naam: M <br/> Overige datavelden: W |
| Locatie: Zorgaanbieder | Reference | Ijsselheem | a | Locatie | | M |
| BeginDatumTijd | Item | 2025-03-30T10:20:00+00:00 | a | Begindatum en tijd | | M |
| EindDatumTijd | Item | 2025-03-30T10:20:30+00:00 | a | Einddatum en tijd | | M |
| **RedenContact** | **Container** | | | | | |
| Toelichting RedenContact | Item | | b | Type contact uitleg (of Type contact Toelichting) | | M |
| Contact::Probleem | Reference | | b | Probleem | | M |
| Contact::Verrichting | Reference | | b | Verrichting | | M |
| AfwijkendeUitslag | Item | | b | Afwijkende uitslag | | M |
| Herkomst | Item | | b | Herkomst | | M |
| Bestemming | Item | | b | Bestemming | | M |

| 1. Naam data item | 2. Type data item | 3. Voorbeeld | 4. Advies waar te tonen in PGO <br/> (a) in overzicht <br/> (b) als overzicht en detailgegeven <br/> (c) niet tonen | 5. Advies tekst weergave in PGO | 6. Opmerkingen | 7. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |
| **Dagrapportage** | **Rootconcept** | | a | Dagrapportage | | |
| ObservatieDatumTijd | Item | 2025-05-17T07:00:00+01:00 | b | Datum en Tijd| | M |
| Dagverslag (ObservatieNaam) | Item | Mevrouw vertoont toenemende stijfheid bij het opstaan en lopen. Er is sprake van fijne tremor in de rechterhand. Tijdens het ochtendcontact had zij moeite om zich verbaal uit te drukken; gebruikt korte zinnen met lange pauzes. Zelfstandig toiletbezoek is mogelijk, maar met risico op vallen. Advies: looprek binnen handbereik houden en logopedie betrekken voor spraakondersteuning. | b | Dagverslag | | M | 
| OberservatieMethode | Item | | b | Oberservatie methode | | M |
| Toelichting | Item | | b | Toelichting | | M |
| Zorgaanbieder | Reference | IJsselheem | a | Liefst geen afkortingen | Zorgorganisatie | Organisatienaam: M <br/> Overige datavelden: W |

| 1. Naam data item | 2. Type data item | 3. Voorbeeld | 4. Advies waar te tonen in PGO <br/> (a) in overzicht <br/> (b) als overzicht en detailgegeven <br/> (c) niet tonen | 5. Advies tekst weergave in PGO | 6. Opmerkingen | 7. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |
| **Alert** | **Rootconcept** | | a | Waarschuwing | | |
|AlertNaam |Item|Drager VRE| a | Waarschuwing | (code = '431109006' in codeSystem 'SNOMED CT') | M |
| BeginDatumTijd | Item | 2025-02-18| b | Waarschuwing actief sinds | | M |
| AlertType | Item | | b | Type waarschuwing | (code = 74018-3' in codeSystem 'LOINC') | M |
| Zorgaanbieder | Reference | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | organisatienaam: M Overige datavelden: W |

| 1. Naam data item | 2. Type data item | 3. Voorbeeld | 4. Advies waar te tonen in PGO <br/> (a) in overzicht <br/> (b) als overzicht en detailgegeven <br/> (c) niet tonen | 5. Advies tekst weergave in PGO | 6. Opmerkingen | 7. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |
| **Bloeddruk** | **Rootconcept** |  | a | Bloeddruk | | |
| Meetmethode | Item | Niet-invasief | b | Methode | (code = '22762002' in codeSystem 'SNOMED CT') | M |
| ManchetType | Item | Klein | b | Manchet type | (code = 'S' in codeSystem '2.16.840.1.113883.2.4.3.11.60.40.4.15.1') | M |
| MeetLocatie | Item | Linker bovenarm | b | Locatie meting | (code = '368208006' in codeSystem 'SNOMED CT') | M |
| DiastolischEindpunt | Item | | b | Hartslag bij rust  | | M |  
| SystolischeBloeddruk | Item | 160 mmhg | a | Bovendruk | | M |
| DiastolischeBloeddruk  | Item | 92 mmhg | a | Onderdruk | | M |
| GemiddeldeBloeddruk  | Item | 109 mmhg | a | Gemiddelde bloeddruk | | M |
| BloeddrukDatumTijd | Item | 2025-03-15T14:45:00+01:00 | a | Datum en Tijd | | M |
| Toelichting | Item | mevrouw gebruikt medicatie | b | Toelichting | | M |
| Houding | Item | Zittende positie | b | Houding | (code = '33586001' in codeSystem 'SNOMED CT') |  |
| Zorgaanbieder |Reference | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M
Overige datavelden: W |

| 1. Naam data item | 2. Type data item | 3. Voorbeeld | 4. Advies waar te tonen in PGO <br/> (a) in overzicht <br/> (b) als overzicht en detailgegeven <br/> (c) niet tonen | 5. Advies tekst weergave in PGO | 6. Opmerkingen | 7. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |
| **Lichaamslengte** | **Rootconcept** | | a | Lichaamslengte | | M |
| LengteWaarde | Item | 160 cm | a | Lichaamslengte | | M |
| LengteDatumTijd | Item | 2025-03-15T13:30:00+01:00 | a | Meetdatum | | M |
| Toelichting | Item | zonder schoenen aan | b | Toelichting | | M |
| Zorgaanbieder |Reference | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M
Overige datavelden: W |

| 1. Naam data item | 2. Type data item | 3. Voorbeeld | 4. Advies waar te tonen in PGO <br/> (a) in overzicht <br/> (b) als overzicht en detailgegeven <br/> (c) niet tonen | 5. Advies tekst weergave in PGO | 6. Opmerkingen | 7. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |
| **Lichaamstemperatuur** | **Rootconcept** | | a | Lichaamstemperatuur | |  |
| TemperatuurWaarde | Item | 38.6 | a | Lichaamstemperatuur | | M |
| TemperatuurDatumTijd | Item | 2025-03-17T07:00:00+01:00 | a | Datum en tijd meting | | M |
| Toelichting | Item | voeten voelen heel koud aan | b | Toelichting | | M |
| TemperatuurType | Item | Tympanic temperature | b | Type temperatuur | (code = '415974002' in codesystem http://snomed.info/sct) | M |
| Zorgaanbieder |Reference | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M
Overige datavelden: W |

| 1. Naam data item | 2. Type data item | 3. Voorbeeld | 4. Advies waar te tonen in PGO <br/> (a) in overzicht <br/> (b) als overzicht en detailgegeven <br/> (c) niet tonen | 5. Advies tekst weergave in PGO | 6. Opmerkingen | 7. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |
| **Lichaamsgewicht** | **Rootconcept** | | a | Lichaamsgewicht | |  |
| GewichtWaarde | Item | 58 kg | a | Lichaamsgewicht | | M |
| Toelichting | Item | mevrouw is aan het aansterken | b | Toelichting | | M |
| GewichtDatumTijd | Item | 2025-03-12T14:30:00+01:00 | a | Datum en tijd meting | | M |
| Kleding | Item | Lichte kleding/ondergoed | b | Kleding | (code = 'MINIMAL' in codeSystem '2.16.840.1.113883.2.4.3.11.60.40.4.8.1') | M |
| Zorgaanbieder |Reference | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M
Overige datavelden: W |

| 1. Naam data item | 2. Type data item | 3. Voorbeeld | 4. Advies waar te tonen in PGO <br/> (a) in overzicht <br/> (b) als overzicht en detailgegeven <br/> (c) niet tonen | 5. Advies tekst weergave in PGO | 6. Opmerkingen | 7. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |
| **Vochtbalans** | **Rootconcept** | | a | Vochtbalans | | |
| Toelichting | Item | dehydratie | a | Vochtbalans | | M |
| VochtTotaalIn | Item | 1400 ml | a | Totaal vocht in | | M |
| VochtTotaalUit | Item | 1000 ml | a | Totaal vocht uit | | M |
| VochtbalansStarttijd | Item | 2025-03-14T07:00:00+02:00 | a | Startdatum en tijd meting | | M |
| VochtbalansStoptijd | Item | 2025-03-15T07:00:00+02:00 | a | Einddatum en tijd meting | | M |
| Zorgaanbieder |Reference | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M
Overige datavelden: W |

| 1. Naam data item | 2. Type data item | 3. Voorbeeld | 4. Advies waar te tonen in PGO <br/> (a) in overzicht <br/> (b) als overzicht en detailgegeven <br/> (c) niet tonen | 5. Advies tekst weergave in PGO | 6. Opmerkingen | 7. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |
| **Woonsituatie** | **Rootconcept** | | a | Woonsituatie | | |
| Toelichting | Item | Woning is op de begane grond | b | Toelichting | | M |
| WoningType | Item | Aanleunwoning | b | Type woning | (code = 'AANLW' in codeSystem '2.16.840.1.113883.2.4.3.11.60.40.4.13.1') | M |
| Zorgaanbieder |Reference | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M
Overige datavelden: W |

| 1. Naam data item | 2. Type data item | 3. Voorbeeld | 4. Advies waar te tonen in PGO <br/> (a) in overzicht <br/> (b) als overzicht en detailgegeven <br/> (c) niet tonen | 5. Advies tekst weergave in PGO | 6. Opmerkingen | 7. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |
| **Voedingsadvies** | **Rootconcept** | | a | Voedingsadvies | | |
| DieetType | Item | lactosevrij | a | Voedingsadvies | | M |
| Consistentie | Item | solide | b | Structuur van eten | | M |
| Toelichting | Item | naar eigen zeggen lactose-intolerant | b | Toelichting | | M |
| Zorgaanbieder | Reference | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M Overige datavelden: W |

| 1. Naam data item | 2. Type data item | 3. Voorbeeld | 4. Advies waar te tonen in PGO <br/> (a) in overzicht <br/> (b) als overzicht en detailgegeven <br/> (c) niet tonen | 5. Advies tekst weergave in PGO | 6. Opmerkingen | 7. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |
| **Betaler** | **Rootconcept** | | a | Verzekeraar | | |
| **BetalerPersoon** | **Container** | | b (zie opmerkingen) | | Als verzekeraar niet aanwezig is | |
| BetalerNaam | Item | | b | Naam | | M |
| **Bankgegevens** | **Container** |  | b | Bankgegevens | | |
| BankNaam | Item | ABN AMRO | b | Naam Bank | | M |
| Bankcode | Item | ABNANL2A | b | | | M |
| Rekeningnummer | Item | NL91 ABNA 0417 1643 00 | b | Rekeningnummer | | M |
| **Verzekeraar** | **Container** |  | b (zie opmerkingen) | Verzekeraar | Als betalerpersoon niet aanwezig is | |
| **Verzekering** | **Container** |  | b | Verzekering | | |
| BeginDatumTijd | Item | 2023-03-18 | b | Begindatum | | M |
| EindDatumTijd | Item | 2026-03-17 | b | Einddatum | | M |
| Verzekerings soort | Item | Basis verzekerd | b | Soort Verzekering | (code = 'B' in codeSystem '2.16.840.1.113883.2.4.3.11.60.101.5.1') | M |
| IdentificatieNummer | Item | 3332 | b | Identificatie nummer | (in identificerend systeem: 2.16.840.1.113883.2.4.6.4) | M |
| OrganisatieNaam | Item | Menzis | b | Naam Organisatie | | M |
| VerzekerdeNummer | Item | 6318708200 | b | Verzekerde nummer | | M |
| Zorgaanbieder | Reference | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M<br/>Overige datavelden: W |

| 1. Naam data item | 2. Type data item | 3. Voorbeeld | 4. Advies waar te tonen in PGO <br/> (a) in overzicht <br/> (b) als overzicht en detailgegeven <br/> (c) niet tonen | 5. Advies tekst weergave in PGO | 6. Opmerkingen | 7. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |
| **Polsfrequentie** | **Rootconcept** | | a | Pols frequentie | | |
| PolsfrequentieWaarde | Item | 67 | a | Waarde | (code /min in codesystem http://unitsofmeasure.org) | M |
| PolsfrequentieDatumTijd | Item | 2024-06-03T00:00:00+02:00 | a | Datum en Tijd meting | | M |
| Toelichting | Item | | b | Toelichting | | M |
| PolsRegelmatigheid | Item | polsslag regelmatig | b | Polsregelmatigheid | (code 271636001 in codesystem SNOMED CT) | M |
| Zorgaanbieder | Reference | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M<br/>Overige datavelden: W |

| 1. Naam data item | 2. Type data item | 3. Voorbeeld | 4. Advies waar te tonen in PGO <br/> (a) in overzicht <br/> (b) als overzicht en detailgegeven <br/> (c) niet tonen | 5. Advies tekst weergave in PGO | 6. Opmerkingen | 7. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |
| **Ademhaling** | **Rootconcept** | | a | Ademhaling | | |
| Ademfrequentie | Item | 15 (code {breaths/min} in codesystem http://unitsofmeasure.org) | a | Adem frequentie | | M |
| AdemhalingDatumTijd | Item | 2015-03-11T14:47:00Z | a | Datum en Tijd meting | | M |
| Ritme | Item | Normaal ademhalingsritme | b | | (code = 5467003 in codesystem SNOMED CT) | M |
| Diepte | Item | Normale ademhalingsdiepte | b | | (code = 301284009 in codeystem SNOMED CT) | M |
| AfwijkendAdemhalingspatroon | Item | | b | Afwijkend Ademhalingspatroon | | M |
| ExtraZuurstofToediening | Item | | b | Extra zuurstof toediening | | M |
| Toelichting | Item | | b | Toelichting | | M |
| Zorgaanbieder | Reference | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M<br/>Overige datavelden: W |
| **ToegediendeZuurstof** | **Container** | | a | Toegediende zuurstof | | |
| FlowRate | Item | 2/min | a | Hoeveelheid zuurstof per minuut | | W |
| FiO2 | Item | 0.29 | b | Fractie zuurstof van de inademings-lucht | | W |
| **ToedieningHulpmiddel::MedischHulpmiddel** | **Reference** | Zuurstofmasker | | Medisch hulpmiddel | | |
| ProductType | Item | Venturi-masker | | Producttype | | W |
| Zorgaanbieder | Reference | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M<br/>Overige datavelden: W |
