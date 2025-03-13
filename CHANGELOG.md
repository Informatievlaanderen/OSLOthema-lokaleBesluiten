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
