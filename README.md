# opis
An Ontology for Personal Information Classification on the Sensor Web
Version 1RC

Two versions of OPIS is provided in this repository: 

- Normal version (opis.owl): OPIS importing the SSN ontology and an external importa files for the BFO-based ontologies (opis-external.owl) following files (external_envo.owl, external_gaz.owl, external_go.owl, external_iao.owl, external_ico.owl, external_mf.owl, external_nbo.owl, external_obi.owl, external_ogms.owl, external_ro.owl, external_sio.owl, external_swo.owl, external_vivo-isf.owl).     These files were created using the OntoFox tool (http://ontofox.hegroup.org/), where each external_xxx.owl file has a external_xxx.txt to generate the owl files on this tool. 
  
- Compacted version (opis-compact.owl): the BFO-based ontologies imported by OPIS has been merged into a file 'opis-bfo-based-external-merged.owl' and imported directly into OPIS, similarly to the SSN ontology. 

## Details about imports
- DOLCE+DnS Ultralite version 3.22 downloaded from 'http://www.ontologydesignpatterns.org/ont/dul/' and has its base namespace changed from  (with a change to the base namespace from 'http://www.ontologydesignpatterns.org/ont/dul/DUL.owl' to 'http://www.loa-cnr.it/ontologies/DUL.owl#'. (original and changed version in this repository).

## Use case
This repository contains a use case for an privacy preservation approach in the Internet of Things. 

- The file opis-extended.owl extends the 'virtual sensor' class to represent an access control mechanism and a privacy preserving data mining technique. In addition, it imports the dbpedia.owl (DBPedia ontology), OpenStreetMaps tags (openstreetmaps-point-of-interest.owl), time (time.owl), and geographic location wgs84 (wgs84.owl) to express personal information used and produced by these virtual sensors. Based on these imports, the opis-extended.owl extends classes to express behaviors (AtHome, havingDinner, havingLunch, HealthCaring, Partying, PracticingSport, ReligiousPracticing, Shopping, Socializing, Working), points of interest (bank, cafe, club, gym, home, hospital, mall, office, pharmacy, 'religious temple', PoIRestaurant, 'sport center') and their equivalent classes in the OpenStreetMaps tags.  

- The file virtual_sensors.owl contains individuals for virtual sensor (a virtual sensor for human activity perception), two access control mechanisms (attribute-based access control and role-based access control), and two privacy preserving data mining techniques (k-anonymity, l-diversity). In addition, individuals for behavioral agent (agent007), 

- The file privacy_policy.owl contains classes to define privacy policy conditions extending the DUL class 'classification' based on the time intervals, concept, and virtual sensors (in particular those of access control mechanisms and privacy preserving data mining techniques). 

- The file classification_taxonomy.owl contains classes to extend the DUL class 'concept' as a classification taxonomy to be used with the privacy policy condition definition. 

- The file direct_classification.owl contains mapping between classification concepts and personal information defined using behavioral entities. 

- The file personal_information_individuals.owl contains instances of behavioral entity classes. 



