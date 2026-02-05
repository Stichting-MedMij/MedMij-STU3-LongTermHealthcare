---
topic: Deduplicatierichtlijn
---

# Deduplicatierichtlijn

## Inleiding en doel
In deze richtlijn wordt uitgelegd wat deduplicatie is en hoe dit kan worden toegepast bij de gegevensdienst Basisgegevens Langdurige Zorg + (BgLZ+). Het doel van deze richtlijn is PGO-leveranciers richting te geven in de wijze waarop zij PGO-gebruikers kunnen attenderen op mogelijk dubbel getoonde BgLZ+-gegevens.

Deze richtlijn is tot stand gekomen met input van de PGO-leveranciers die deelnemen aan het ontwikkeltraject van de BgLZ+.

## Deduplicatie 
Deduplicatie (of ontdubbelen) is het maar één keer tonen of overnemen van gedupliceerde gegevens.

Deduplicatie is afhankelijk van de mogelijkheid tot automatische duplicaatdetectie: het vinden van duplicaatgegevens op basis van identificerende informatie. Indien deze niet of onvoldoende beschikbaar is, kan ook handmatige deduplicatie plaatsvinden.

Automatisch ontdubbelen kan op basis van het `.id` of de `.identifier` plaatsvinden. Meer informatie over het toepassen van de elementen `.id` en `.identifier` in FHIR-resources is te vinden in de [MedMij FHIR Implementation Guide voor STU3](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/FHIR_IG#Usage_of_the_.id.2C_.identifier_and_.fullUrl_elements_in_FHIR_instances). In de praktijk worden door de DVA (in combinatie met het bronsysteem) vaker `.id`s dan `.identifier`s beschikbaar gesteld. Het voordeel van het gebruiken van `.id` als identificerend kenmerk dat er hier altijd één van is. De `.identifier` is over alle zorgaanbieder heen uniek en het `.id` alleen binnen één zorgaanbieder. Er kunnen meerdere `.identifier`s zijn toegekend door de DVA, alle met een eigen `.system`-waarde wat het complexer maakt.

Handmatige duplicaatdetectie kan met ondersteuning vanuit de PGO plaatsvinden. Als gegevens worden getoond die overeenkomstige informatie bevatten, kan de PGO-gebruiker via een waarschuwing (bijvoorbeeld via een uitroepteken, specifieke kleur of andere vorm) worden gewaarschuwd voor een mogelijke dubbele weergave van dezelfde gegevens. De PGO-leverancier kan vervolgens de PGO-gebruiker de mogelijkheid bieden om de duplicaatgegevens in het overzicht te verbergen.

De trigger voor deze waarschuwing is niet officieel vastgelegd, maar deze zou kunnen optreden op basis van een combinatie van (verplichte) metadataelementen. Hierbij kan gedacht worden aan een bepaald concept dat vaker is geregistreerd bij een zorgaanbieder met een identieke datum/tijd en waarde.

## Identificatie binnen één zorgsysteem 
Omdat de duplicaten uit dezelfde bron kunnen komen en daardoor identieke inhoud en metainformatie hebben, kunnen metadataelementen (bijvoorbeeld datum/tijd en waarde) worden gebruikt om te bepalen of het om hetzelfde gegeven gaat. Het is onwaarschijnlijk dat cariësrisico van een patiënt op hetzelfde tijdstip en met dezelfde waarde geregistreerd wordt.

Deduplicatie is niet altijd mogelijk wanneer opeenvolgende gegevens met dezelfde identificerende kenmerken met verschillende inhoud worden ontvangen. Het is dan namelijk niet altijd duidelijk welk gegeven de meest recente is. Onderstaande scenario’s kunnen handvatten bieden om duplicaten te vermijden: 
- Wanneer systeem A gegevens ontvangt en deze vervolgens opslaat, en deze gegevens later door een ander systeem bij systeem A worden opgehaald, kan worden aangenomen dat de laatst opgehaalde versie de meest recente is.
- Een ander scenario is om de verplichte dossiervoering van de PGO optioneel te maken voor de deelnemers van het MedMij Afsprakenstelsel. Er loopt een Service Request voor deze aanpassing in het Afsprakenstelsel. 

## Reconciliatie 
Metadata maakt reconciliatie, i.e. het samenbrengen van patiëntgegevens uit verschillende systemen op een uniforme en consistente manier, mogelijk. 

Een effectieve reconciliatie steunt op vier kernaspecten:
1. Deduplicatie - Een gegevensitem kan uit meerdere bronnen komen, maar moet slechts één keer worden weergegeven. Dit vereist het gebruik van consistente identificatoren tussen verschillende databeheerders.
2. Semantische interpretatie - Gegevens uit verschillende systemen moeten op een consistente manier worden geclassificeerd en geïnterpreteerd. Dit vereist semantische interoperabiliteit, ondersteund door gestandaardiseerde classificaties en terminologieën. HCIM's en de Eenheid van Taal-terminologieservices leveren hiervoor al de benodigde consistentie.
3. Herkomst - Het moet altijd duidelijk zijn waar een gegevensitem vandaan komt. De oorspronkelijke bron moet traceerbaar zijn en, waar mogelijk, benaderbaar blijven. Herkomst wordt vastgelegd via auteurschap en broninformatie (in FHIR bijvoorbeeld via de Provenance-resource). Binnen het Afsprakenstelsel zijn de verantwoordelijkheden van de leveranciers geschetst. De genoemde metadata is volgens *core.dossier.102* en *core.dossier.104* uit [Verantwoordelijkheden, Core](https://afsprakenstelsel.medmij.nl/asverplicht/mmverplicht/verantwoordelijkheden-core) vereist. 
4. Attributie - Patiëntgegevens is informatie over een subject op een bepaald moment in de tijd. Om dit aan het zorgproces te koppelen, heeft elk gegevensitem minimaal informatie nodig over het subject en over datum/tijd.