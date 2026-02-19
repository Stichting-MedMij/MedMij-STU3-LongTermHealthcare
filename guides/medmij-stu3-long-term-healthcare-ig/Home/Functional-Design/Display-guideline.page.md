---
topic: Weergaverichtlijn
---
 
# Weergaverichtlijn
 
## Inleiding
Dit is de weergaverichtlijn voor gegevensdienst Verzamelen Basisgegevens Langdurige Zorg+ (BgLZ+).

De richtlijn bevat mock-ups die bedoeld zijn ter inspiratie. Persoonlijke gezondheidsomgevingen (PGO’s) kunnen deze voorbeelden naar eigen inzicht visueel vormgeven, zolang de gebruiksvriendelijkheid behouden blijft.

## Doel
Deze richtlijn heeft als doel om duidelijke handvatten te bieden voor een patiëntvriendelijke en begrijpelijke weergave van langdurige zorg gegevens de PGO. De richtlijn ondersteunt ontwikkelaars en zorgverleners bij het:
- gebruiken van begrijpelijke en patiëntvriendelijke termen en toelichtingen;
- structureren en presenteren van een overzicht van gegevens op een manier die aansluit bij de informatiebehoefte van PGO gebruikers.

De richtlijn geeft géén handvatten voor de vormgeving (kleur, vorm, lettertype, etc.) van gegevens.

## Scope
De scope bevat de gegevensdienst BgLZ+ voorzien van een aanvullende set gegevens BgLZ+ die worden weergegeven in de PGO. 

De richtlijn is ontwikkeld voor gegevens die verzameld worden via de aanvullende gegevens set BgLZ+. Gegevens die via andere MedMij-gegevensdiensten verzameld worden in de PGO zijn hierin niet meegenomen.

## Inhoud richtlijn
Het inloggen en authentiseren bij de zorgaanbieder is niet opgenomen in deze richtlijn.
De gebruiker gaat in de PGO naar het overzicht langdurige zorg en/of overzicht zorgorganisatie-langdurige zorg waar de langdurige zorg gegevens getoond worden. 

### Overzichtsscherm langdurige zorggegevens
Er zijn twee weergaven gedefinieerd voor het overzicht van de langdurige zorggegevens:
- Scenario 1: Overzicht Langdurige zorg (met alle langdurige zorggegevens van alle zorgaanbieders in één overzicht)
- Scenario 2: Overzicht Zorgorganisatie-Langdurige zorg (met alle langdurige zorggegevens van één zorgaanbieder in één overzicht)

De twee scenario’s, hieronder uitgewerkt, geven weer hoe een UX design getoond kan worden. Een PGO is vrij om 1 of beide van deze scenario’s te ondersteunen. De richtlijn gaat ervan uit dat PGO’s een responsief ontwerp ondersteunen. 

In deze richtlijn hebben we twee voorbeeld mockups opgenomen ter inspiratie. Daaronder hebben we elke zib apart opgenomen, niet in mockup vorm maar in tabel vorm. De twee voorbeeld mockups gaan over afspraken, maar let op, de zib “contact” is apart opgenomen in tabelvorm. 

#### Voorbeeld mockup overzichtsschermen langdurige zorg
Overzicht Langdurige zorg:

Het overzichtsscherm van elke zib heeft dus een aparte pagina waar de datavelden getoond worden, voor alle (langdurige zorg) zorgaanbieders.  

{{render: guides/medmij-stu3-long-term-healthcare-ig/images/Langdurige zorg overzicht.png}}

**Figuur 1: Voorbeeld Overzicht Langdurige zorg**

Overzicht Zorgorganisatie-langdurige zorg

Het overzichtsscherm van elke zib heeft dus een aparte tab waar de datavelden getoond worden, per zorgaanbieder. 

{{render: guides/medmij-stu3-long-term-healthcare-ig/images/Zorgorganisatie overzicht.png}} 

**Figuur 2: Voorbeeld Overzicht Zorgorganisatie - langdurige zorg**

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
| Begindatum | 30-03-2025 |
| Begintijd | 20:00 |
| Einddatum | 30-03-2025 |
| Eindtijd | 21:00 |
| Zorgverlener | Julia van den Bos |
| Zorgorganisatie | IJsselheem |
| Reden contact | Advies over veilige en passende lichaamsbeweging |

<br/> 

#### Dagrapportage 

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

<br/> 

#### Alert

<u>Overzichtsscherm</u>

| Waarschuwing | Datum invoer | Zorgorganisatie |
| --- | --- | --- |
| Drager VRE | 15-03-2025 | IJsselheem |
| Verhoogd valrisico | 10-03-2015 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Waarschuwing 15-03-2025 | Voorbeeldwaarde |
| --- | --- |
| Waarschuwing | Drager VRE |
| Datum invoer | 15-03-2025 |
| Zorgorganisatie | IJsselheem |

<br/> 

#### Bloeddruk

<u>Overzichtsscherm</u>

| Bloeddruk | Datum | Zorgorganisatie |
| --- | --- | --- |
| 160/92 mmHg | 15-03-2025 | IJsselheem |
| 160/80 mmHg | 31-11-2024 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: 160/92 mmHg 15-03-2025 | Voorbeeldwaarde |
| --- | --- |
| Meet methode | Niet-invasief |
| Manchettype | Klein |
| Meet locatie | Linker bovenarm |
| Rust druk | 80 mmHg |
| Bovendruk | 160 mmHg |
| Onderdruk | 92 mmHg |
| Gemiddelde bloeddruk | 109 mmHg |
| Toelichting | mevrouw gebruikt medicatie |
| Houding | Zittende positie |
| Datum | 15-03-2025 |
| Tijd | 14:45 |
| Zorgorganisatie | IJsselheem |

<br/> 

#### Lichaamslengte

<u>Overzichtsscherm</u>

| Lichaamslengte | Datum | Zorgorganisatie |
| --- | --- | --- |
| 160 cm | 15-03-2025 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Lichaamslengte 15-03-2025 | Voorbeeldwaarde |
| --- | --- |
| Lichaamslengte | 160 cm |
| Datum | 15-03-2025 |
| Tijd | 14:30 |
| Toelichting | zonder schoenen aan |
| Positie | staande positie | 

<br/> 

#### Lichaamstemperatuur

<u>Overzichtsscherm</u>

| Lichaamstemperatuur | Datum | Zorgorganisatie |
| --- | --- | --- |
| 37,2 graden | 15-03-2025 | IJsselheem |
| 37,5 graden | 17-02-2025 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Lichaamstemperatuur 15-03-2025 | Voorbeeldwaarde |
| --- | --- |
| Lichaamstemperatuur | 37,2 graden |
| Datum | 15-03-2025 |
| Tijd | 11:00 |
| Toelichting | een koude dag |
| Temperatuur type | Orale temperatuur (onder de tong) |
| Zorgorganisatie | IJsselheem |

<br/> 

#### Lichaamsgewicht

<u>Overzichtsscherm</u>

| Lichaamsgewicht | Datum | Zorgorganisatie |
| --- | --- | --- |
| 58 kg | 15-03-2025 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Lichaamsgewicht 15-03-2025 | Voorbeeldwaarde |
| --- | --- |
| Lichaamsgewicht | 58 kg |
| Datum | 15-03-2025 |
| Tijd | 14:30 |
| Kleding | Lichte kleding/ondergoed |
| Toelichting | mevrouw is aan het aansterken |
| Zorgorganisatie | IJsselheem |

<br/> 

#### Vochtbalans

<u>Overzichtsscherm</u>

| Vochtbalans | Datum | Zorgorganisatie |
| --- | --- | --- |
| 1400ml/ 1000ml | 15-03-2025 | IJsselheem |
| 1600ml/1200ml | 17-02-2025 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: 1400 ml/ 1000 ml 15-03-2025 | Voorbeeldwaarde |
| --- | --- |
| Vocht totaal inname | 1400 ML |
| Vocht totaal uit | 1000 ML |
| Vochtbalans starttijd | 11:00 |
| Vochtbalans stoptijd | 12:00 |
| Toelichting | dehydratie |
| Zorgorganisatie | IJsselheem |

<br/> 

#### Woonsituatie

<u>Overzichtsscherm</u>

| Woningtype | Toelichting | Zorgorganisatie |
| --- | --- | --- |
| Aanleunwoning | Woning is op de begane grond | IJsselheem |

<br/> 

#### Voedingsadvies

<u>Overzichtsscherm</u>

| Voedingsadvies | Consistentie | Zorgorganisatie |
| --- | --- | --- |
| Lactosevrij | Solide | IJsselheem |
| Selderij | Solide | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Waarde Lactosevrij | Voorbeeldwaarde |
| --- | --- |
| Voedingsadvies | Lactosevrij |
| Consistentie | Solide |
| Toelichting | Naar eigen zeggen: lactose-intolerant |
| Zorgorganisatie | IJsselheem |

<br/> 

#### Betaler

<u>Overzichtsscherm</u>

| Naam betaler | Zorgorganisatie |
| --- | --- |
| Trias | IJsselheem |
| Menzis | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Trias | Voorbeeldwaarde |
| --- | --- |
| Naam betaler | Trias |
| Naam Bank |   |
| Code Bank |   |
| Rekeningnummer Bank |   |
| Begin datum | 01-01-2025 |
| Eind datum | 31-12-2025 |
| Naam verzekeraar | Trias |
| Soort verzekering | Basis verzekerd |
| Nummer verzekerde | 12345678 |
| Zorgorganisatie | IJsselheem |

<br/> 

#### Polsfrequentie

<u>Overzichtsscherm</u>

| Polsfrequentie | Datum | Zorgorganisatie |
| --- | --- | --- |
| 96 | 15-03-2025 | IJsselheem |
| 92 | 28-11-2024 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: 96 - 15-03-2025 | Voorbeeldwaarde |
| --- | --- |
| Polsfrequentie | 96 per min |
| Datum | 15-03-2025 |
| Tijd | 14:00 |
| Toelichting |  |
| PolsRegelmatigheid | Regelmatige polsslag |
| Zorgorganisatie | IJsselheem |

<br/> 

#### Ademhaling

<u>Overzichtsscherm</u>

| Ademhaling | Datum | Zorgorganisatie |
| --- | --- | --- |
| 18 | 15-03-2025 | IJsselheem |
| 15 | 15-02-2025 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Ademhaling 15-03-2025 | Voorbeeldwaarde |
| --- | --- |
| Ademhaling | 18 per min |
| Datum | 15-03-2025 |
| Tijd | 14:45 |
| Ritme | Abnormaal ademhalingsritme |
| Diepte | Normale ademhalingsdiepte |
| Afwijkend ademhalingspatroon | Apneu |
| Extra zuurstof toediening | Nee |
| Toelichting | meneer lijkt angstig |
| Flowrate | 2 l/min |
| FiO2 | 0.29l |
| Toediening hulpmiddel |  |
| ProductType |  |
| Zorgorganisatie | IJsselheem |

<br/> 

## Tabel met specificaties
In de tabel met specificaties staan de gegevens uit de gegevensdienst Verzamelen BgLZ+, die relevant zijn voor deze weergaverichtlijn weergegeven. 
De prioriteit van de te tonen datavelden wordt vastgesteld volgens de MoSCoW-methodiek. Datavelden die niet in de specificatietabel voorkomen, moeten worden beschouwd als datavelden met de letter W.
<br/> 

| **Prioriteit** | **Omschrijving** |
| --- | --- |
| M(ust have) | Nodig voor de basisfunctionaliteit van de toepassing en moet worden geïmplementeerd om het proces succesvol te laten verlopen. |
| S(hould have) | Belangrijke functionaliteit die niet vereist is, maar die voordelen biedt voor gebruikers en de algehele gebruikservaring. |
| C(ould have) | Gewenste functionaliteit die waarde toevoegt, maar minder kritisch is en indien nodig kan worden uitgesteld. |
| W(on't have) | Functionaliteiten die nu buiten scope zijn maar mogelijk in de toekomst worden overwogen. |


| 1. Naam data item | 2. Type data item | 3. Id | 4. Voorbeeld | 5. Advies waar te tonen in PGO <br/> (a) in overzicht en detailgegeven <br/> (b) in detailgegeven <br/> (c) niet tonen | 6. Advies tekst weergave in PGO | 7. Opmerkingen | 8. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Contact** | **Rootconcept** | NL-CM:15.1.1 | | a | Contact | | | 
| Contacttype | Item | NL-CM:15.1.2 | Thuis | a | Type contact of afspraak | (code = 'HH' in "codesystem Index - FHIR v5.0.0": "https://hl7.org/fhir/?utm_referrer=https%3A%2F%2Fwww.hl7.org%2F") | M |
| ContactMet:: Zorgverlener | Reference | NL-CM:15.1.7 | Julia van den Bos | a | Contact met |  | Zorgverlener naam: M <br/> Overige datavelden: W |
| Locatie:: Zorgaanbieder | Reference | NL-CM:15.1.8 | Ijsselheem | a | Locatie | | M |
| BeginDatumTijd | Item | NL-CM:15.1.3 | 2025-03-30T10:20:00+00:00 | a | Begindatum en tijd | | M |
| EindDatumTijd | Item | NL-CM:15.1.4 | 2025-03-30T10:20:30+00:00 | a | Einddatum en tijd | | M |
| **RedenContact** | **Container** | NL-CM:15.1.13 | | | | | |
| Contact::Probleem | Reference | NL-CM:15.1.6 | | b | Probleem | | M |
| Contact::Verrichting | Reference | NL-CM:15.1.11 | | b | Verrichting | | M |
| AfwijkendeUitslag | Item | NL-CM:15.1.12 | | b | Afwijkende uitslag | | M |
| Herkomst | Item | NL-CM:15.1.14 | Instelling voor revalidatie | b | Herkomst | (code = '80522000' in codeSystem SNOMED CT ) | M |
| Bestemming | Item | NL-CM:15.1.16 | Eigen woonomgeving | b | Bestemming | code = '264362003' in codeSystem SNOMED CT )| M |

<br/> 

| 1. Naam data item | 2. Type data item | 3. Id | 4. Voorbeeld | 5. Advies waar te tonen in PGO <br/> (a) in overzicht en detailgegeven <br/> (b) in detailgegeven <br/> (c) niet tonen | 6. Advies tekst weergave in PGO | 7. Opmerkingen | 8. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Dagrapportage** | **Rootconcept** | | | a | Dagrapportage | | |
| ObservatieDatumTijd | Item | | 2025-05-17T07:00:00+01:00 | b | Datum en Tijd| | M |
| Dagverslag (ObservatieNaam) | Item | | Mevrouw vertoont toenemende stijfheid bij het opstaan en lopen. Er is sprake van fijne tremor in de rechterhand. Tijdens het ochtendcontact had zij moeite om zich verbaal uit te drukken; gebruikt korte zinnen met lange pauzes. Zelfstandig toiletbezoek is mogelijk, maar met risico op vallen. Advies: looprek binnen handbereik houden en logopedie betrekken voor spraakondersteuning. | b | Dagverslag | | M | 
| ObservatieMethode | Item | | | b | Oberservatie methode | | M |
| Toelichting | Item | | | b | Toelichting | | M |

<br/> 

| 1. Naam data item | 2. Type data item | 3. Id | 4. Voorbeeld | 5. Advies waar te tonen in PGO <br/> (a) in overzicht en detailgegeven <br/> (b) in detailgegeven <br/> (c) niet tonen | 6. Advies tekst weergave in PGO | 7. Opmerkingen | 8. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Alert** | **Rootconcept** | NL-CM:8.3.1| | a | Alertnaam | | |
| AlertNaam |Item| NL-CM:8.3.4 | Drager VRE| a | Waarschuwing | (code = '431109006' in codeSystem SNOMED CT ) | M |
| BeginDatumTijd | Item | NL-CM:8.3.5 | 2025-02-18| b | Waarschuwing actief sinds | | M |
| AlertType | Item | NL-CM:8.3.6 | | b | Type waarschuwing | (code = '74018-3' in codeSystem 'LOINC') | M |

<br/> 

| 1. Naam data item | 2. Type data item | 3. Id | 4. Voorbeeld | 5. Advies waar te tonen in PGO <br/> (a) in overzicht en detailgegeven <br/> (b) in detailgegeven <br/> (c) niet tonen | 6. Advies tekst weergave in PGO | 7. Opmerkingen | 8. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Bloeddruk** | **Rootconcept** | NL-CM:12.4.1 | | a | Bloeddruk | | |
| Meetmethode | Item | NL-CM:12.4.7 | Niet-invasief | b | Methode | (code = '22762002' in codeSystem SNOMED CT ) | M |
| ManchetType | Item | NL-CM:12.4.9 | Klein | b | Manchet type | (code = 'S' in codeSystem '2.16.840.1.113883.2.4.3.11.60.40.4.15.1') | M |
| MeetLocatie | Item | NL-CM:12.4.10 | Linker bovenarm | b | Locatie meting | (code = '368208006' in codeSystem SNOMED CT ) | M |
| DiastolischEindpunt | Item | NL-CM:12.4.8 | | b | Fase IV  | (code = '225271000' in codeSystem SNOMED CT ) | M |  
| SystolischeBloeddruk | Item | NL-CM:12.4.2 | 160 mmhg | a | Bovendruk | | M |
| DiastolischeBloeddruk  | Item | NL-CM:12.4.3 | 92 mmhg | a | Onderdruk | | M |
| GemiddeldeBloeddruk  | Item | NL-CM:12.4.4 | 109 mmhg | a | Gemiddelde bloeddruk | | M |
| BloeddrukDatumTijd | Item | NL-CM:12.4.5 | 2025-03-15T14:45:00+01:00 | a | Datum en Tijd | | M |
| Toelichting | Item | NL-CM:12.4.6 | mevrouw gebruikt medicatie | b | Toelichting | | M |
| Houding | Item | NL-CM:12.4.11 | Zittende positie | b | Houding | (code = '33586001' in codeSystem SNOMED CT ) | S |

<br/> 

| 1. Naam data item | 2. Type data item | 3. Id | 4. Voorbeeld | 5. Advies waar te tonen in PGO <br/> (a) in overzicht en detailgegeven <br/> (b) in detailgegeven <br/> (c) niet tonen | 6. Advies tekst weergave in PGO | 7. Opmerkingen | 8. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Lichaamslengte** | **Rootconcept** | NL-CM:12.2.1 | | a | Lichaamslengte | | M |
| LengteWaarde | Item | NL-CM:12.2.2 | 160 cm | a | Lichaamslengte | | M |
| LengteDatumTijd | Item | NL-CM:12.2.4	| 2025-03-15T13:30:00+01:00 | a | Meetdatum | | M |
| Toelichting | Item | NL-CM:12.2.3 | zonder schoenen aan | b | Toelichting | | M |
| Positie | NL-CM:12.2.5 | Staande positie | b | Positie | (code = '10904000' in codeSystem SNOMED CT ) | S |

<br/> 

| 1. Naam data item | 2. Type data item | 3. Id | 4. Voorbeeld | 5. Advies waar te tonen in PGO <br/> (a) in overzicht en detailgegeven <br/> (b) in detailgegeven <br/> (c) niet tonen | 6. Advies tekst weergave in PGO | 7. Opmerkingen | 8. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |--- |
| **Lichaamstemperatuur** | **Rootconcept** | NL-CM:12.6.1 | | a | Lichaamstemperatuur | |  |
| TemperatuurWaarde | Item | NL-CM:12.6.2 | 38.6 | a | Lichaamstemperatuur | | M |
| TemperatuurDatumTijd | Item | NL-CM:12.6.4 | 2025-03-17T07:00:00+01:00 | a | Datum en tijd meting | | M |
| Toelichting | Item | NL-CM:12.6.3 | voeten voelen heel koud aan | b | Toelichting | | M |
| TemperatuurType | Item | NL-CM:12.6.5 | Tympanic temperature | b | Type temperatuur | (code = '415974002' in codeSystem SNOMED CT ) | M |

<br/> 

| 1. Naam data item | 2. Type data item | 3. Id | 4. Voorbeeld | 5. Advies waar te tonen in PGO <br/> (a) in overzicht en detailgegeven <br/> (b) in detailgegeven <br/> (c) niet tonen | 6. Advies tekst weergave in PGO | 7. Opmerkingen | 8. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |--- |
| **Lichaamsgewicht** | **Rootconcept** | NL-CM:12.1.1 | | a | Lichaamsgewicht | |  |
| GewichtWaarde | Item | NL-CM:12.1.2 | 58 kg | a | Lichaamsgewicht | | M |
| Toelichting | Item | NL-CM:12.1.3 | mevrouw is aan het aansterken | b | Toelichting | | M |
| GewichtDatumTijd | Item | NL-CM:12.1.4 | 2025-03-12T14:30:00+01:00 | a | Datum en tijd meting | | M |
| Kleding | Item | NL-CM:12.1.5 | Lichte kleding/ondergoed | b | Kleding | (code = 'MINIMAL' in codeSystem '2.16.840.1.113883.2.4.3.11.60.40.4.8.1') | M |

<br/> 

| 1. Naam data item | 2. Type data item | 3. Id | 4. Voorbeeld | 5. Advies waar te tonen in PGO <br/> (a) in overzicht en detailgegeven <br/> (b) in detailgegeven <br/> (c) niet tonen | 6. Advies tekst weergave in PGO | 7. Opmerkingen | 8. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |--- |
| **Vochtbalans** | **Rootconcept** | NL-CM:12.15.1 | | a | Vochtbalans | | |
| Toelichting | Item | NL-CM:12.15.6 | dehydratie | a | Vochtbalans | | M |
| VochtTotaalIn | Item | NL-CM:12.15.4 | 1400 ml | a | Totaal vocht in | | M |
| VochtTotaalUit | Item | NL-CM:12.15.5 | 1000 ml | a | Totaal vocht uit | | M |
| VochtbalansStarttijd | Item | NL-CM:12.15.2 | 2025-03-14T07:00:00+02:00 | a | Startdatum en tijd meting | | M |
| VochtbalansStoptijd | Item | NL-CM:12.15.3 | 2025-03-15T07:00:00+02:00 | a | Einddatum en tijd meting | | M |

<br/> 

| 1. Naam data item | 2. Type data item | 3. Id | 4. Voorbeeld | 5. Advies waar te tonen in PGO <br/> (a) in overzicht en detailgegeven <br/> (b) in detailgegeven <br/> (c) niet tonen | 6. Advies tekst weergave in PGO | 7. Opmerkingen | 8. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |--- |
| **Woonsituatie** | **Rootconcept** | NL-CM:7.8.1 | | a | Woonsituatie | | |
| Toelichting | Item | NL-CM:7.8.2 | Woning is op de begane grond | b | Toelichting | | M |
| WoningType | Item | NL-CM:7.8.3 | Aanleunwoning | b | Type woning | (code = 'AANLW' in codeSystem '2.16.840.1.113883.2.4.3.11.60.40.4.13.1') | M |

<br/> 

| 1. Naam data item | 2. Type data item | 3. Id | 4. Voorbeeld | 5. Advies waar te tonen in PGO <br/> (a) in overzicht en detailgegeven <br/> (b) in detailgegeven <br/> (c) niet tonen | 6. Advies tekst weergave in PGO | 7. Opmerkingen | 8. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |--- |
| **Voedingsadvies** | **Rootconcept** | NL-CM:7.11.1 | | a | Voedingsadvies | | |
| DieetType | Item | NL-CM:7.11.2 | lactosevrij | a | Voedingsadvies | | M |
| Consistentie | Item | NL-CM:7.11.3 | solide | b | Structuur van eten | | M |
| Toelichting | Item | NL-CM:7.11.4 | naar eigen zeggen lactose-intolerant | b | Toelichting | | M |

<br/> 

| 1. Naam data item | 2. Type data item | 3. Id | 4. Voorbeeld | 5. Advies waar te tonen in PGO <br/> (a) in overzicht en detailgegeven <br/> (b) in detailgegeven <br/> (c) niet tonen | 6. Advies tekst weergave in PGO | 7. Opmerkingen | 8. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Betaler** | **Rootconcept** | NL-CM:1.1.1 | | a | Verzekeraar | | |
| **BetalerPersoon** | **Container** | NL-CM:1.1.2 | | b (zie opmerkingen) | | Als verzekeraar niet aanwezig is | |
| BetalerNaam | Item | NL-CM:1.1.5 | | b | Naam | | M |
| **Bankgegevens** | **Container** | NL-CM:1.1.4 | | b | Bankgegevens | | |
| BankNaam | Item | NL-CM:1.1.9 | ING | b | Naam Bank | | M |
| Bankcode | Item | NL-CM:1.1.10 | INGBNL2A | b | | | M |
| Rekeningnummer | Item | NL-CM:1.1.11 | NL85INGB0001234567 | b | Rekeningnummer | | M |
| **Verzekeraar** | **Container** | NL-CM:1.1.3 | | b (zie opmerkingen) | Verzekeraar | Als betalerpersoon niet aanwezig is | |
| **Verzekering** | **Container** | NL-CM:1.1.8 | | b | Verzekering | | |
| BeginDatumTijd | Item | NL-CM:1.1.13 | 2023-03-18 | b | Begindatum | | M |
| EindDatumTijd | Item | NL-CM:1.1.14 | 2026-03-17 | b | Einddatum | | M |
| Verzekeringssoort | Item | NL-CM:1.1.15 | Basis verzekerd | b | Soort Verzekering | (code = 'B' in codeSystem '2.16.840.1.113883.2.4.3.11.60.101.5.1') | M |
| IdentificatieNummer | Item | NL-CM:1.1.7 | 3332 | b | Identificatie nummer | (in identificerend systeem: 2.16.840.1.113883.2.4.6.4) | M |
| OrganisatieNaam | Item | NL-CM:1.1.16 | Menzis | b | Naam Organisatie | | M |
| VerzekerdeNummer | Item | NL-CM:1.1.6 | 6318708200 | b | Verzekerde nummer | | M |

<br/> 

| 1. Naam data item | 2. Type data item | 3. Id | 4. Voorbeeld | 5. Advies waar te tonen in PGO <br/> (a) in overzicht en detailgegeven <br/> (b) in detailgegeven <br/> (c) niet tonen | 6. Advies tekst weergave in PGO | 7. Opmerkingen | 8. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |--- |
| **Polsfrequentie** | **Rootconcept** | NL-CM:12.7.1 | | a | Pols frequentie | | |
| PolsfrequentieWaarde | Item | NL-CM:12.7.2| 67/min | a | Waarde | (code '/min' in codeSystem http://unitsofmeasure.org) | M |
| PolsfrequentieDatumTijd | Item | NL-CM:12.7.3 | 2024-06-03T00:00:00+02:00 | a | Datum en Tijd meting | | M |
| Toelichting | Item | NL-CM:12.7.4 | | b | Toelichting | | M |
| PolsRegelmatigheid | Item | NL-CM:12.7.5 | Regelmatige polsslag | b | PolsRegelmatigheid | (code '271636001' in codeSystem SNOMED CT ) | M |

<br/> 

| 1. Naam data item | 2. Type data item | 3. Id | 4. Voorbeeld | 5. Advies waar te tonen in PGO <br/> (a) in overzicht en detailgegeven <br/> (b) in detailgegeven <br/> (c) niet tonen | 6. Advies tekst weergave in PGO | 7. Opmerkingen | 8. Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Ademhaling** | **Rootconcept** | | | a | Ademhaling | | |
| Ademfrequentie | Item | NL-CM-12.5.2 | 15/min | a | Adem frequentie | | M |
| AdemhalingDatumTijd | Item | NL-CM-12.5.4 | 2015-03-11T14:47:00Z | a | Datum en Tijd meting | | M |
| Ritme | Item | NL-CM-12.5.5 | Normaal ademhalingsritme | b | | (code = '5467003' in codesystem SNOMED CT) | M |
| Diepte | Item | NL-CM-12.5.6| Normale ademhalingsdiepte | b | | (code = '301284009' in codeSystem SNOMED CT) | M |
| AfwijkendAdemhalingspatroon | Item | NL-CM-12.5.7 | Apneu | b | Afwijkend Ademhalingspatroon | (code = '1023001' in codeSystem SNOMED CT) | M |
| ExtraZuurstofToediening | Item | NL-CM-12.5.12 | | b | Extra zuurstof toediening | | M |
| Toelichting | Item | NL-CM-12.5.3 | | b | Toelichting | | M |
| **ToegediendeZuurstof** | **Container** | NL-CM-12.5.8 | | a | Toegediende zuurstof | | |
| FlowRate | Item | NL-CM-12.5.10 | 2/min | a | Hoeveelheid zuurstof per minuut | | W |
| FiO2 | Item | NL-CM-12.5.9 | 0.29 | b | Fractie zuurstof van de inademings-lucht | | W |
| **ToedieningHulpmiddel::MedischHulpmiddel** | **Reference** | NL-CM-12.5.13 | Zuurstofmasker | b | Medisch hulpmiddel | | |
| ProductType | Item | NL-CM-2017-4 | Venturi-masker | b | Producttype | (code = '428285009' in codeSystem SNOMED CT) | W |