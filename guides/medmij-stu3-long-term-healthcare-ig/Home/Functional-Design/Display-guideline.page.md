---
topic: Weergaverichtlijn
---

# Weergaverichtlijn

## Inleiding
Dit is de weergaverichtlijn voor gegevensdienst Basisgegevens Langdurige Zorg+ (BgLZ+).

De richtlijn bevat mock-ups die bedoeld zijn ter inspiratie. Persoonlijke gezondheidsomgevingen (PGO's) kunnen deze voorbeelden naar eigen inzicht visueel vormgeven, zolang de gebruiksvriendelijkheid behouden blijft.

## Doel
Deze richtlijn heeft als doel om duidelijke handvatten te bieden voor een patiëntvriendelijke en begrijpelijke weergave van langdurigezorggegevens in de PGO. De richtlijn ondersteunt ontwikkelaars en zorgverleners bij het:
- gebruiken van begrijpelijke en patiëntvriendelijke termen en toelichtingen;
- structureren en presenteren van een overzicht van gegevens op een manier die aansluit bij de informatiebehoefte van PGO-gebruikers.

De richtlijn geeft géén handvatten voor de vormgeving (kleur, vorm, lettertype, etc.) van gegevens.

## Scope
De scope van deze richtlijn bestaat uit de BgLZ+-gegevens die worden weergegeven in de PGO. Gegevens die via andere MedMij-gegevensdiensten verzameld worden in de PGO zijn hierin niet meegenomen.

## Inhoud richtlijn
Het inloggen en authenticeren bij de zorgaanbieder is niet opgenomen in deze richtlijn.
De gebruiker gaat in de PGO naar het overzicht Langdurige zorg en/of overzicht Zorgaanbieder - Langdurige zorg waar de langdurigezorggegevens getoond worden.

### Overzichtsscherm langdurige zorg
Er zijn twee weergaven gedefinieerd voor het overzicht van de langdurigezorggegevens:
- Scenario 1: Overzicht Langdurige zorg (met alle langdurigezorggegevens van alle zorgaanbieders in één overzicht)
- Scenario 2: Overzicht Zorgaanbieder - Langdurige zorg (met alle langdurigezorggegevens van één zorgaanbieder in één overzicht)

De twee scenario's, hieronder uitgewerkt, geven weer hoe een UX-design getoond kan worden. Een PGO is vrij om één of beide van deze scenario's te ondersteunen. De richtlijn gaat ervan uit dat de PGO een responsief ontwerp ondersteunt.

In deze richtlijn zijn twee mock-ups opgenomen ter inspiratie. Daaronder is elke CIM (Clinical Information Model) apart opgenomen, niet in een mock-up, maar in tabelvorm. De twee mock-ups gaan over afspraken en corresponderen met de CIM Contact.

#### Mock-ups overzichtsschermen langdurige zorg
<u>Overzicht Langdurige zorg</u>

In het Overzicht Langdurige zorg heeft het overzichtsscherm van elke CIM een aparte pagina waar de datavelden getoond worden, voor alle zorgaanbieders (binnen de langdurige zorg). 

{{render: guides/medmij-stu3-long-term-healthcare-ig/images/Overzicht Langdurige zorg.png}}

**Figuur 1: Voorbeeld Overzicht Langdurige zorg**

<u>Overzicht Zorgaanbieder - Langdurige zorg</u>

In het Overzicht Zorgaanbieder - Langdurige zorg heeft het overzichtsscherm van elke CIM een aparte pagina waar de datavelden getoond worden, per zorgaanbieder. De in de mock-up gebruikte tabs dienen enkel als voorbeeld van een mogelijke vormgeving.

{{render: guides/medmij-stu3-long-term-healthcare-ig/images/Overzicht Zorgaanbieder - Langdurige zorg.png}}

**Figuur 2: Voorbeeld Overzicht Zorgaanbieder - Langdurige zorg**

De acceptatiecriteria voor de overzichtsschermen van elke CIM is als volgt.

| Nr | Acceptatiecriteria |
| --- | --- |
| 1 | Standaard worden alle beschikbaar gestelde gegevens van de zorgaanbieders(s) overzichtelijk weergegeven, gesorteerd op datum van nieuw naar oud. |
| 2 | Je kunt zoeken op (delen van) de gegevens of op informatie uit de andere datavelden in het overzichtsscherm. De datum vormt hierop een uitzondering, omdat hiervoor al een periode kan worden opgegeven. |
| 3 | Voor de datavelden in het overzichtsscherm is het mogelijk om te filteren op één of meerdere waarden. De datum vormt hierop een uitzondering, omdat hiervoor al een periode kan worden opgegeven. |
| 4 | Voor het datumveld in het overzichtsscherm kun je een specifieke periode selecteren. |
| 5 | In het overzichtsscherm kan minimaal op datum worden gesorteerd, maar bij voorkeur is sorteren op alle datavelden mogelijk. |
| 6 | De datavelden in het overzichtsscherm zijn begrijpelijk en gebruiksvriendelijk geformuleerd. Zie de {{pagelink: Weergaverichtlijn, text: Tabel met specificaties, anchor: TabelSpecificaties}} voor de aanbevolen termen per opgehaald dataveld. In verband met beperkte schermruimte op mobiele apparaten mogen de labelnamen van de datavelden in het overzichtsscherm worden weggelaten. |

#### Detailscherm langdurige zorg
Dit detailscherm krijgt een PGO-gebruiker te zien na het selecteren van een specifieke regel in het overzichtsscherm. De in de mock-up weergegeven gegevens dienen uitsluitend ter demonstratie.

#### Mock-up detailscherm langdurige zorg

{{render: guides/medmij-stu3-long-term-healthcare-ig/images/Detailscherm Langdurige zorg.png}}

**Figuur 3: Voorbeeld Detailscherm Langdurige zorg**

| Nr | Acceptatiecriteria |
| --- | --- |
| 1 | De datavelden in het detailscherm zijn begrijpelijk en gebruiksvriendelijk geformuleerd. Zie de {{pagelink: Weergaverichtlijn, text: Tabel met specificaties, anchor: TabelSpecificaties}} voor de aanbevolen termen per opgehaald dataveld.|

### Langdurigezorggegevens per CIM
Hieronder wordt voor alle CIM's relevant voor langdurige zorg een voorbeeld in tabelvorm weergegeven. De zorgaanbieder in het overzichtsscherm en detailscherm is alleen nodig voor scenario 1. Deze is niet nodig voor scenario 2.

#### Contact

<u>Overzichtsscherm</u>

| Contact | Begindatum | Begintijd | Zorgverlener | Zorgorganisatie |
| --- | --- | --- | --- | --- |
| Advies over veilige en passende lichaamsbeweging | 30-03-2025 | 20:00 | Julia van den Bos | IJsselheem |
| Controle voortgang revalidatie | 01-06-2025 | 11:00 | W. Bloem | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Contact Advies over de veilige en passende lichaamsbeweging | Waarde |
| --- | --- |
| Type contact | Thuis |
| Begindatum | 30-03-2025 |
| Begintijd | 20:00 |
| Einddatum | 30-03-2025 |
| Eindtijd | 21:00 |
| Contact met | Julia van den Bos |
| Zorgorganisatie | IJsselheem |
| Reden contact | Advies over veilige en passende lichaamsbeweging |

<br/>

#### Dagrapportage

<u>Overzichtsscherm</u>

| Titel dagrapportage | Datum | Tijd | Zorgorganisatie |
| --- | --- | --- | --- |
| Problemen met mobiliteit en spraak | 15-03-2025 | 12:00 | IJsselheem |
| Vermoeidheid na middagactiviteit | 14-03-2025 | 16:45 | IJsselheem |
| Avondverslag voor slapengaan | 07-03-2025 | 21:00 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Dagrapportage 15-03-2025 12:00 | Waarde |
| --- | --- |
| Titel dagrapportage | Problemen met mobiliteit en spraak |
| Dagverslag | Mevrouw vertoont toenemende stijfheid bij het opstaan en lopen. Er is sprake van fijne tremor in de rechterhand. Tijdens het ochtendcontact had zij moeite om zich verbaal uit te drukken; gebruikt korte zinnen met lange pauzes. Zelfstandig toiletbezoek is mogelijk, maar met risico op vallen. Advies: looprek binnen handbereik houden en logopedie betrekken voor spraakondersteuning. |
| Datum | 15-03-2025 |
| Tijd | 12:00 |
| Zorgverlener | Julia van den Bos |
| Zorgorganisatie | IJsselheem |

<br/>

#### Alert

<u>Overzichtsscherm</u>

| Waarschuwing | Datum invoer | Zorgorganisatie |
| --- | --- | --- |
| Drager VRE | 15-03-2025 | IJsselheem |
| Verhoogd valrisico | 10-03-2015 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Waarschuwing 15-03-2025 | Waarde |
| --- | --- |
| Waarschuwing | Drager VRE |
| Waarschuwing actief sinds | 15-03-2025 |
| Type | Waarschuwing |
| Zorgorganisatie | IJsselheem |

<br/>

#### Bloeddruk

<u>Overzichtsscherm</u>

| Bloeddruk | Datum | Zorgorganisatie |
| --- | --- | --- |
| 160/92 mmHg | 15-03-2025 | IJsselheem |
| 160/80 mmHg | 31-11-2024 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Bloeddruk 15-03-2025 | Waarde |
| --- | --- |
| Methode | Niet-invasief |
| Manchettype | Klein |
| Locatie meting | Linker bovenarm |
| Korotkofftoon | Fase IV |
| Bovendruk | 160 mmHg |
| Onderdruk | 92 mmHg |
| Gemiddelde bloeddruk | 109 mmHg |
| Datum | 15-03-2025 |
| Tijd | 14:45 |
| Toelichting | mevrouw gebruikt medicatie |
| Houding | Zittende positie |
| Zorgorganisatie | IJsselheem |

<br/>

#### Lichaamslengte

<u>Overzichtsscherm</u>

| Lichaamslengte | Datum | Zorgorganisatie |
| --- | --- | --- |
| 160 cm | 15-03-2025 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Lichaamslengte 15-03-2025 | Waarde |
| --- | --- |
| Lichaamslengte | 160 cm |
| Datum | 15-03-2025 |
| Tijd | 14:30 |
| Toelichting | zonder schoenen aan |
| Positie | Staande positie |
| Zorgorganisatie | IJsselheem |

<br/>

#### Lichaamstemperatuur

<u>Overzichtsscherm</u>

| Lichaamstemperatuur | Datum | Zorgorganisatie |
| --- | --- | --- |
| 37,2 graden | 15-03-2025 | IJsselheem |
| 37,5 graden | 17-02-2025 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Lichaamstemperatuur 15-03-2025 | Waarde |
| --- | --- |
| Lichaamstemperatuur | 37,2 graden |
| Datum | 15-03-2025 |
| Tijd | 11:00 |
| Type temperatuur | Orale temperatuur (onder de tong) |
| Toelichting | een koude dag |
| Zorgorganisatie | IJsselheem |

<br/>

#### Lichaamsgewicht

<u>Overzichtsscherm</u>

| Lichaamsgewicht | Datum | Zorgorganisatie |
| --- | --- | --- |
| 58 kg | 15-03-2025 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Lichaamsgewicht 15-03-2025 | Waarde |
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
| 1400 ml / 1000 ml | 15-03-2025 | IJsselheem |
| 1600 ml / 1200 ml | 17-02-2025 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Vochtbalans 15-03-2025 | Waarde |
| --- | --- |
| Vochtinname totaal | 1400 ml |
| Vochtuitscheiding totaal | 1000 ml |
| Vochtbalans starttijd | 11:00 |
| Vochtbalans stoptijd | 12:00 |
| Toelichting | dehydratie |
| Zorgorganisatie | IJsselheem |

<br/>

#### Woonsituatie

<u>Overzichtsscherm</u>

| Woningtype | Datum | Toelichting | Zorgorganisatie |
| --- | --- | --- |
| Aanleunwoning | 15-03-2024 | Woning is op de begane grond | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Woonsituatie 15-03-2024 | Waarde |
| --- | --- |
| Type woning | Aanleunwoning |
| Datum | 15-03-2024 |
| Toelichting | Woning is op de begane grond |
| Zorgorganisatie | IJsselheem |

<br/>

#### Voedingsadvies

<u>Overzichtsscherm</u>

| Voedingsadvies | Datum | Consistentie | Zorgorganisatie |
| --- | --- | --- | ---|
| Lactosevrij | 15-03-2025 | Solide | IJsselheem |
| Selderij | 17-02-2025 | Solide | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Voedingsadvies Lactosevrij | Waarde |
| --- | --- |
| Voedingsadvies | Lactosevrij |
| Datum | 15-03-2025 |
| Tijd | 11:37 |
| Structuur van eten | Solide |
| Toelichting | Naar eigen zeggen: lactose-intolerant |
| Zorgorganisatie | IJsselheem |

<br/>

#### Betaler

<u>Overzichtsscherm</u>

| Naam betaler/verzekeraar | Zorgorganisatie |
| --- | --- |
| Trias | IJsselheem |
| J.L. Teunissen | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Betaler J.L. Teunissen | |
| --- | --- |
| Naam betaler | J.L. Teunissen |
| Naam bank | ING |
| Code bank | INGBNL2A |
| Rekeningnummer | NL91INGB0417164300 |
| Naam verzekeraar | |
| Begindatum | |
| Einddatum | |
| Soort verzekering | |
| Nummer verzekerde | |
| Zorgorganisatie | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Betaler Trias | Waarde |
| --- | --- |
| Naam betaler | |
| Naam bank | |
| Code bank | |
| Rekeningnummer | |
| Naam verzekeraar | Trias |
| Begindatum | 01-01-2025 |
| Einddatum | 31-12-2025 |
| Soort verzekering | Basis verzekerd |
| Nummer verzekerde | 12345678 |
| Zorgorganisatie | IJsselheem |

<br/>

#### Polsfrequentie

<u>Overzichtsscherm</u>

| Polsfrequentie | Datum | Zorgorganisatie |
| --- | --- | --- |
| 96 /min | 15-03-2025 | IJsselheem |
| 92 /min | 28-11-2024 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Polsfrequentie 15-03-2025 | Waarde |
| --- | --- |
| Polsfrequentie | 96 /min |
| Datum | 15-03-2025 |
| Tijd | 14:00 |
| Toelichting | |
| Polsregelmaat | Regelmatige polsslag |
| Zorgorganisatie | IJsselheem |

<br/>

#### Ademhaling

<u>Overzichtsscherm</u>

| Ademhaling | Datum | Zorgorganisatie |
| --- | --- | --- |
| 18 /min | 15-03-2025 | IJsselheem |
| 15 /min | 15-02-2025 | IJsselheem |

<u>Detailscherm</u>

| Geselecteerde regel: Ademhaling 15-03-2025 | Waarde |
| --- | --- |
| Ademhaling | 18 /min |
| Datum | 15-03-2025 |
| Tijd | 14:45 |
| Ritme | Abnormaal ademhalingsritme |
| Diepte | Normale ademhalingsdiepte |
| Afwijkend ademhalingspatroon | Apneu |
| Extra zuurstof toediening | Nee |
| Toelichting | meneer lijkt angstig |
| Hoeveelheid zuurstof per minuut | 2 l/min |
| Fractie zuurstof van ingeademde lucht | 0,29 |
| Hulpmiddel bij toediening | Zuurstofmasker |
| Type hulpmiddel | Venturi-masker |
| Zorgorganisatie | IJsselheem |

<br/>

## <a name="TabelSpecificaties"></a> Tabel met specificaties
In de tabel met specificaties staan de gegevens uit de gegevensdienst Verzamelen BgLZ+, die relevant zijn voor deze weergaverichtlijn, weergegeven.
De prioriteit van de te tonen datavelden wordt vastgesteld volgens de MoSCoW-methodiek. Datavelden die niet in de specificatietabel voorkomen, moeten worden beschouwd als datavelden met de letter W.

<br/>

| Prioriteit | Omschrijving |
| --- | --- |
| M(ust have) | Nodig voor de basisfunctionaliteit van de toepassing en moet worden geïmplementeerd om het proces succesvol te laten verlopen. |
| S(hould have) | Belangrijke functionaliteit die niet vereist is, maar die voordelen biedt voor gebruikers en de algehele gebruikservaring. |
| C(ould have) | Gewenste functionaliteit die waarde toevoegt, maar minder kritisch is en indien nodig kan worden uitgesteld. |
| W(on't have) | Functionaliteiten die nu buiten scope zijn maar mogelijk in de toekomst worden overwogen. PGO’s hebben de vrijheid om deze datavelden desondanks toch te tonen. Het uitgangspunt is echter dat deze velden niet primair worden weergegeven, zodat de gebruiker deze informatie niet direct ziet. De gegevens zijn alleen beschikbaar wanneer de gebruiker hier expliciet naar zoekt of doorklikt, aangezien deze datavelden geen duidelijke meerwaarde hebben voor directe weergave. |

<br/>

Merk op dat in onderstaande tabellen het dataitem Zorgaanbieder (van type Reference) is opgenomen. Hierbij wordt verwezen naar het concept Auteur uit de zib [BasisElementen](https://zibs.nl/wiki/BasisElementen-v1.0(2017NL)). Het bijbehorende id is een samengesteld id dat via de zib Zorgverlener loopt om tot een weergave van de Zorgaanbieder te komen.

<br/>

| Naam data-item | Type data-item | Id | Voorbeeld | Waar te tonen in PGO <br/> (a) in overzicht en als detailgegeven <br/> (b) als detailgegeven | Weergavetekst in PGO | Opmerkingen | Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Contact** | **Rootconcept** | NL-CM:15.1.1 | | a | Contact | | |
| Contacttype | Item | NL-CM:15.1.2 | Thuis (code 'HH' in codesysteem 'ActCode') | a | Type contact | | M |
| ContactMet::Zorgverlener | Reference | NL-CM:15.1.7 | Julia van den Bos | a of b | Contact met (of Zorgverlener) | | Zorgverlener naam: M <br/> Overige datavelden: W |
| Locatie::Zorgaanbieder | Reference | NL-CM:15.1.8 | IJsselheem | a | Locatie (of Zorgorganisatie) | Liefst geen afkortingen | M |
| BeginDatumTijd | Item | NL-CM:15.1.3 | 30-03-2025 10:20 | a | Begindatum en -tijd (Weergeven in twee velden
Begindatum en Begintijd) | BeginDatumTijd en EindDatumTijd mogen ook als periode in 1 veld getoond worden | M |
| EindDatumTijd | Item | NL-CM:15.1.4 | 30-03-2025 10:50 | b | Einddatum en -tijd of (Weergeven in twee velden
Einddatum en Eindtijd)| BeginDatumTijd en EindDatumTijd mogen ook als periode in 1 veld getoond worden | M |
| **RedenContact** | **Container** | NL-CM:15.1.13 | | b | Reden contact | | |
| Probleem | Reference | NL-CM:15.1.6 | | b | Reden contact | | S |
| Verrichting | Reference | NL-CM:15.1.11 | | b | Reden contact | | S |
| AfwijkendeUitslag | Item | NL-CM:15.1.12 | Advies over veilige en passende lichaamsbeweging | b | Reden contact | | M |

<br/>

| Naam data-item | Type data-item | Id | Voorbeeld | Waar te tonen in PGO <br/> (a) in overzicht en als detailgegeven <br/> (b) als detailgegeven | Weergavetekst in PGO | Opmerkingen | Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Dagrapportage** | **Rootconcept** | lz-dataelement-1 | | a | Dagrapportage | | |
| RapportageTitel | Item | lz-dataelement-2 | Problemen met mobiliteit en spraak | a | Titel dagrapportage | | M |
| RapportageDatumTijd | Item | lz-dataelement-3 | 17-05-2025 07:00 | a | Datum en tijd | | M |
| Uitvoerder::Zorgverlener | Reference | lz-dataelement-4 | Julia van den Bos | b | Zorgverlener | | M |
| Uitvoerder::Zorgaanbieder | Reference | lz-dataelement-14 | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | M |
| RapportageInhoud | Item | lz-dataelement-19 | Mevrouw vertoont toenemende stijfheid bij het opstaan en lopen. Er is sprake van fijne tremor in de rechterhand. Tijdens het ochtendcontact had zij moeite om zich verbaal uit te drukken; gebruikt korte zinnen met lange pauzes. Zelfstandig toiletbezoek is mogelijk, maar met risico op vallen. Advies: looprek binnen handbereik houden en logopedie betrekken voor spraakondersteuning. | b | Dagverslag | | M |

<br/>

| Naam data-item | Type data-item | Id | Voorbeeld | Waar te tonen in PGO <br/> (a) in overzicht en als detailgegeven <br/> (b) als detailgegeven | Weergavetekst in PGO | Opmerkingen | Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Alert** | **Rootconcept** | NL-CM:8.3.1 | | a | Waarschuwing | | |
| Conditie::Probleem | Item | NL-CM:8.3.3 | | a | Probleem | | M |
| AlertNaam |Item| NL-CM:8.3.4 | Drager VRE (code '431109006' in codesysteem 'SNOMED CT') | a | Waarschuwing | | M |
| BeginDatumTijd | Item | NL-CM:8.3.5 | 18-02-2025 | b | Waarschuwing actief sinds | | M |
| AlertType | Item | NL-CM:8.3.6 | Waarschuwing (code '74018-3' in codesysteem 'LOINC') | b | Type | | M |
| Zorgaanbieder | Reference | NL-CM:0.0.7 --> NL-CM:17.1.1 --> NL-CM:17.1.6 | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M <br/> Overige datavelden: W |

<br/>

| Naam data-item | Type data-item | Id | Voorbeeld | Waar te tonen in PGO <br/> (a) in overzicht en als detailgegeven <br/> (b) als detailgegeven | Weergavetekst in PGO | Opmerkingen | Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Bloeddruk** | **Rootconcept** | NL-CM:12.4.1 | | a | Bloeddruk | | |
| Meetmethode | Item | NL-CM:12.4.7 | Niet-invasief (code '22762002' in codesysteem 'SNOMED CT') | b | Methode | | M |
| ManchetType | Item | NL-CM:12.4.9 | Klein (code 'S' in codesysteem '2.16.840.1.113883.2.4.3.11.60.40.4.15.1') | b | Manchettype | | M |
| MeetLocatie | Item | NL-CM:12.4.10 | Linker bovenarm (code '368208006' in codesysteem 'SNOMED CT') | b | Locatie meting | | M |
| DiastolischEindpunt | Item | NL-CM:12.4.8 | Fase IV (code '225271000' in codesysteem 'SNOMED CT') | b | Korotkofftoon | | M |
| SystolischeBloeddruk | Item | NL-CM:12.4.2 | 160 mmHg | a | Bovendruk | | M |
| DiastolischeBloeddruk | Item | NL-CM:12.4.3 | 92 mmHg | a | Onderdruk | | M |
| GemiddeldeBloeddruk | Item | NL-CM:12.4.4 | 109 mmHg | b | Gemiddelde bloeddruk | | M |
| BloeddrukDatumTijd | Item | NL-CM:12.4.5 | 15-03-2025 14:45 | a | Datum en tijd | | M |
| Toelichting | Item | NL-CM:12.4.6 | mevrouw gebruikt medicatie | b | Toelichting | | M |
| Houding | Item | NL-CM:12.4.11 | Zittende positie (code '33586001' in codesysteem 'SNOMED CT') | b | Houding | | S |
| Zorgaanbieder | Reference | NL-CM:0.0.7 --> NL-CM:17.1.1 --> NL-CM:17.1.6 | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M <br/> Overige datavelden: W |

<br/>

| Naam data-item | Type data-item | Id | Voorbeeld | Waar te tonen in PGO <br/> (a) in overzicht en als detailgegeven <br/> (b) als detailgegeven | Weergavetekst in PGO | Opmerkingen | Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Lichaamslengte** | **Rootconcept** | NL-CM:12.2.1 | | a | Lichaamslengte | | |
| LengteWaarde | Item | NL-CM:12.2.2 | 160 cm | a | Lichaamslengte | | M |
| LengteDatumTijd | Item | NL-CM:12.2.4 | 15-03-2025 13:30 | a | Datum en tijd | | M |
| Toelichting | Item | NL-CM:12.2.3 | zonder schoenen aan | b | Toelichting | | M |
| Positie | Item | NL-CM:12.2.5 | Staande positie (code '10904000' in codesysteem 'SNOMED CT') | b | Positie | | S |
| Zorgaanbieder | Reference | NL-CM:0.0.7 --> NL-CM:17.1.1 --> NL-CM:17.1.6 | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M <br/> Overige datavelden: W |

<br/>

| Naam data-item | Type data-item | Id | Voorbeeld | Waar te tonen in PGO <br/> (a) in overzicht en als detailgegeven <br/> (b) als detailgegeven | Weergavetekst in PGO | Opmerkingen | Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |--- |
| **Lichaamstemperatuur** | **Rootconcept** | NL-CM:12.6.1 | | a | Lichaamstemperatuur | | |
| TemperatuurWaarde | Item | NL-CM:12.6.2 | 38,6 | a | Lichaamstemperatuur | | M |
| TemperatuurDatumTijd | Item | NL-CM:12.6.4 | 17-03-2025 07:00 | a | Datum en tijd | | M |
| Toelichting | Item | NL-CM:12.6.3 | voeten voelen heel koud aan | b | Toelichting | | M |
| TemperatuurType | Item | NL-CM:12.6.5 | Orale temperatuur (onder de tong) (code '415945006' in codesysteem 'SNOMED CT') | b | Type temperatuur | | M |
| Zorgaanbieder | Reference | NL-CM:0.0.7 --> NL-CM:17.1.1 --> NL-CM:17.1.6 | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M <br/> Overige datavelden: W |

<br/>

| Naam data-item | Type data-item | Id | Voorbeeld | Waar te tonen in PGO <br/> (a) in overzicht en als detailgegeven <br/> (b) als detailgegeven | Weergavetekst in PGO | Opmerkingen | Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |--- |
| **Lichaamsgewicht** | **Rootconcept** | NL-CM:12.1.1 | | a | Lichaamsgewicht | | |
| GewichtWaarde | Item | NL-CM:12.1.2 | 58 kg | a | Lichaamsgewicht | | M |
| Toelichting | Item | NL-CM:12.1.3 | mevrouw is aan het aansterken | b | Toelichting | | M |
| GewichtDatumTijd | Item | NL-CM:12.1.4 | 12-03-2025 14:30 | a | Datum en tijd | | M |
| Kleding | Item | NL-CM:12.1.5 | Lichte kleding/ondergoed (code 'MINIMAL' in codesysteem '2.16.840.1.113883.2.4.3.11.60.40.4.8.1') | b | Kleding | | M |
| Zorgaanbieder | Reference | NL-CM:0.0.7 --> NL-CM:17.1.1 --> NL-CM:17.1.6 | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M <br/> Overige datavelden: W |

<br/>

| Naam data-item | Type data-item | Id | Voorbeeld | Waar te tonen in PGO <br/> (a) in overzicht en als detailgegeven <br/> (b) als detailgegeven | Weergavetekst in PGO | Opmerkingen | Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |--- |
| **Vochtbalans** | **Rootconcept** | NL-CM:12.15.1 | | a | Vochtbalans | | |
| Toelichting | Item | NL-CM:12.15.6 | dehydratie | a of b | Vochtbalans | | M |
| VochtTotaalIn | Item | NL-CM:12.15.4 | 1400 ml | a | Totaal vocht in | | M |
| VochtTotaalUit | Item | NL-CM:12.15.5 | 1000 ml | a | Totaal vocht uit | | M |
| VochtbalansStarttijd | Item | NL-CM:12.15.2 | 14-03-2025 07:00 | a | Startdatum en -tijd | | M |
| VochtbalansStoptijd | Item | NL-CM:12.15.3 | 15-03-2025 07:00 | a of b | Einddatum en -tijd | | M |
| Zorgaanbieder | Reference | NL-CM:0.0.7 --> NL-CM:17.1.1 --> NL-CM:17.1.6 | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M <br/> Overige datavelden: W |

<br/>

| Naam data-item | Type data-item | Id | Voorbeeld | Waar te tonen in PGO <br/> (a) in overzicht en als detailgegeven <br/> (b) als detailgegeven | Weergavetekst in PGO | Opmerkingen | Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |--- |
| **Woonsituatie** | **Rootconcept** | NL-CM:7.8.1 | | a | Woonsituatie | | |
| WoningType | Item | NL-CM:7.8.3 | Aanleunwoning (code 'AANLW' in codesysteem '2.16.840.1.113883.2.4.3.11.60.40.4.13.1') | a | Type woning | | M |
| DatumTijd | Item | NL-CM:0.0.14 | 15-03-2024 | a | Datum | Alleen datum is voldoende | M |
| Toelichting | Item | NL-CM:7.8.2 | Woning is op de begane grond | a of b | Toelichting | | M |
| Zorgaanbieder | Reference | NL-CM:0.0.7 --> NL-CM:17.1.1 --> NL-CM:17.1.6 | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M <br/> Overige datavelden: W |

<br/>

| Naam data-item | Type data-item | Id | Voorbeeld | Waar te tonen in PGO <br/> (a) in overzicht en als detailgegeven <br/> (b) als detailgegeven | Weergavetekst in PGO | Opmerkingen | Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |--- |
| **Voedingsadvies** | **Rootconcept** | NL-CM:7.11.1 | | a | Voedingsadvies | | |
| DieetType | Item | NL-CM:7.11.2 | lactosevrij | a | Voedingsadvies | | M |
| DatumTijd | Item | NL-CM:0.0.14 | 15-03-2025 11:37 | a | Datum en tijd | | M |
| Consistentie | Item | NL-CM:7.11.3 | solide | b | Structuur van eten | | M |
| Toelichting | Item | NL-CM:7.11.4 | naar eigen zeggen lactose-intolerant | b | Toelichting | | M |
| Zorgaanbieder | Reference | NL-CM:0.0.7 --> NL-CM:17.1.1 --> NL-CM:17.1.6 | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M <br/> Overige datavelden: W |

<br/>

| Naam data-item | Type data-item | Id | Voorbeeld | Waar te tonen in PGO <br/> (a) in overzicht en als detailgegeven <br/> (b) als detailgegeven | Weergavetekst in PGO | Opmerkingen | Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Betaler** | **Rootconcept** | NL-CM:1.1.1 | | a | Verzekeraar | | |
| **BetalerPersoon** | **Container** | NL-CM:1.1.2 | | a (zie opmerkingen) | Betaler | Als Verzekeraar niet aanwezig is | |
| BetalerNaam | Item | NL-CM:1.1.5 | | a | Naam | | M |
| **Bankgegevens** | **Container** | NL-CM:1.1.4 | | b | Bankgegevens | | |
| BankNaam | Item | NL-CM:1.1.9 | ING | b | Naam bank | | M |
| Bankcode | Item | NL-CM:1.1.10 | INGBNL2A | b | Code bank | | M |
| Rekeningnummer | Item | NL-CM:1.1.11 | NL85INGB0001234567 | b | Rekeningnummer | | M |
| **Verzekeraar** | **Container** | NL-CM:1.1.3 | | a of b (zie opmerkingen) | Verzekeraar | Als BetalerPersoon niet aanwezig is | |
| **Verzekering** | **Container** | NL-CM:1.1.8 | | a of b | Verzekering | | |
| BeginDatumTijd | Item | NL-CM:1.1.13 | 18-03-2023 | b | Begindatum | Alleen datum is voldoende | M |
| EindDatumTijd | Item | NL-CM:1.1.14 | 17-03-2026 | b | Einddatum | Alleen datum is voldoende | M |
| Verzekeringssoort | Item | NL-CM:1.1.15 | Basis verzekerd (code 'B' in codesysteem '2.16.840.1.113883.2.4.3.11.60.101.5.1') | b | Soort verzekering | | M |
| IdentificatieNummer | Item | NL-CM:1.1.7 | 3332 (in identificerend systeem '2.16.840.1.113883.2.4.6.4') | b | Identificatienummer | | M |
| OrganisatieNaam | Item | NL-CM:1.1.16 | Menzis | a of b | Naam organisatie | | M |
| VerzekerdeNummer | Item | NL-CM:1.1.6 | 6318708200 | b | Nummer verzekerde | | M |
| Adresgegevens | Subbouwsteen | NL-CM:1.1.17 | | b | | | M |
| Contactgegevens | Subbouwsteen | NL-CM:1.1.12 | | b | | | M |
| Zorgaanbieder | Reference | NL-CM:0.0.7 --> NL-CM:17.1.1 --> NL-CM:17.1.6 | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M <br/> Overige datavelden: W |

<br/>

| Naam data-item | Type data-item | Id | Voorbeeld | Waar te tonen in PGO <br/> (a) in overzicht en als detailgegeven <br/> (b) als detailgegeven | Weergavetekst in PGO | Opmerkingen | Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- |--- |
| **Polsfrequentie** | **Rootconcept** | NL-CM:12.7.1 | | a | Polsfrequentie | | |
| PolsfrequentieWaarde | Item | NL-CM:12.7.2| 67 /min | a | Waarde | | M |
| PolsfrequentieDatumTijd | Item | NL-CM:12.7.3 | 03-06-2024 00:00 | a | Datum en tijd | | M |
| Toelichting | Item | NL-CM:12.7.4 | | b | Toelichting | | M |
| PolsRegelmatigheid | Item | NL-CM:12.7.5 | Regelmatige polsslag (code '271636001' in codesysteem 'SNOMED CT') | b | Polsregelmaat | | M |
| Zorgaanbieder | Reference | NL-CM:0.0.7 --> NL-CM:17.1.1 --> NL-CM:17.1.6 | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M <br/> Overige datavelden: W |

<br/>

| Naam data-item | Type data-item | Id | Voorbeeld | Waar te tonen in PGO <br/> (a) in overzicht en als detailgegeven <br/> (b) als detailgegeven | Weergavetekst in PGO | Opmerkingen | Prioriteit (MoSCoW) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Ademhaling** | **Rootconcept** | | | a | Ademhaling | | |
| Ademfrequentie | Item | NL-CM:12.5.2 | 15 /min | a | Ademfrequentie | | M |
| AdemhalingDatumTijd | Item | NL-CM:12.5.4 | 11-03-2015 14:47 | a | Datum en tijd | | M |
| Ritme | Item | NL-CM:12.5.5 | Normaal ademhalingsritme (code '5467003' in codesysteem 'SNOMED CT') | b | Ritme | | M |
| Diepte | Item | NL-CM:12.5.6| Normale ademhalingsdiepte (code '301284009' in codesysteem 'SNOMED CT') | b | Diepte | | M |
| AfwijkendAdemhalingspatroon | Item | NL-CM:12.5.7 | Apneu (code '1023001' in codesysteem 'SNOMED CT') | b | Afwijkend ademhalingspatroon | | M |
| ExtraZuurstofToediening | Item | NL-CM:12.5.12 | | b | Extra zuurstoftoediening | | M |
| Toelichting | Item | NL-CM:12.5.3 | | b | Toelichting | | M |
| **ToegediendeZuurstof** | **Container** | NL-CM:12.5.8 | | b | Toegediende zuurstof | | |
| FlowRate | Item | NL-CM:12.5.10 | 2 l/min | b | Hoeveelheid zuurstof per minuut | | S |
| FiO2 | Item | NL-CM:12.5.9 | 0,29 | b | Fractie zuurstof van ingeademde lucht | | S |
| ToedieningHulpmiddel::MedischHulpmiddel | Reference | NL-CM:12.5.13 | Zuurstofmasker | b | Hulpmiddel bij toediening | | S |
| ProductType | Item | NL-CM:10.1.3 | Venturi-masker (code '428285009' in codesysteem 'SNOMED CT') | b | Type hulpmiddel | | S |
| Zorgaanbieder | Reference | NL-CM:0.0.7 --> NL-CM:17.1.1 --> NL-CM:17.1.6 | IJsselheem | a | Zorgorganisatie | Liefst geen afkortingen | Organisatienaam: M <br/> Overige datavelden: W |