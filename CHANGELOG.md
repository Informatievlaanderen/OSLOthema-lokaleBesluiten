# 12-03-2025
  - start wijziging voor toolchain 4 processing
  - tag rollout-toolchain4 om de laatste commit aan te duiden voor de rollout van toolchain4

## mandaat/mandatendatabank

fix EAP issues:
2025-03-12T15:28:23.623Z error: [AttributeConverterHandler]: Package tag was defined (Besluit), but unable to find a related package object for attribute (Model:OSLO²_applicatieprofiel_Mandaat_mandatendatabank:OSLO-Generiek:Activiteit:geplandeStart).
   > verwijder annotatie package besluit 
2025-03-12T15:28:23.625Z error: [ElementConverterHandler]: Package tag was defined for element Model:OSLO²_applicatieprofiel_Mandaat_mandatendatabank:OSLO-Wetgeving:Legale Verschijningsvorm Onderdeel, but unable to find the object for package Besluit.
   > verwijder annotatie package besluit
Error: [AttributeConverterHandler]: Unable to find domain object for attribute (Model:Domain Model:OSLO²_vocabularium:OSLO-Mandaat:Lidmaatschap:lidVanTot).
   > verwijder de ignore tag op de associatieklasse lidmaatschap
Error: Unable to find the assigned URI for class http://www.w3.org/ns/prov#Entity which acts as a parent.
   > verwijder parentURI annotatie voor Generiek:Versie

gebruik de juiste basistemplates
   - verwijder links naar niet onderhouden pagina's
   - vervang de feedback issue list met deze repo specifieke
   - gebruik de default JSON-LD generator output

TODO:
  herconfiguratie voor de associatieklasse in het AP.

## besluit/besluit-publicatie

EAP besluit-publicatie: verwijder alles wat niet relevant is van OSLO-Mandaat vocabularium
EAP besluit-voc: verwijder niet relevante vocabularia om zo een beperkere EAP te bekomen.
    - eigenschap vergunt is ambigue in de range: via een tag is het rdfs:Resource en via UML is het Object (prov:Entity)
    - geef alle connectoren card 0..*

aanpassing basistemplates

TODO: https://data.vlaanderen.be/doc/applicatieprofiel/besluit-publicatie/#Documentonderdeel%3Ais%20onderdeel%20van ontbreekt
teveel https://data.test-vlaanderen.be/doc/applicatieprofiel/besluit-publicatie/ontwerpstandaard/toolchain4/#Mandataris%3Aistijdelijkvervangendoor

http://data.vlaanderen.be/ns/besluit#heeftVoorwaarde heeft ontbrekende definitie
toolchain 4 issue: vocabularia ondersteunen geen subproperties

## besluit-mobiliteit
Deze standaard is nog steeds Kandidaat. Contact moet opgenomen worden met de huidige editoren.

EAP:
  - pas verschillende range herlinkingen toe
  - verwijder OSLO-Mandaat

template:
  - aanpassing naar nieuwe basistemplates
  - verwijding referntie naar JSON-LD, om de default generatie te gebruiken

TODO:
  - status in de template staat ontwerp.

# bestuur
Deze standaard is een lege placeholder.
  Beter dit op te lossen in de template.


TODO: 
  - verwijder branch master-node-toolchain
