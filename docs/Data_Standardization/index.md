---
layout: default
title: Standardisation des données
nav_order: 6
---

# Standardisation des données
{: .no_toc }

## Table des matières
{: .no_toc .text-delta }

1. TOC
{:toc}

La vision FAIR de la **découverte et réutilisation** des ensembles de données repose sur plusieurs [motivations et défis](https://github.com/ClimateSmartAgCollab/Documentation-en/blob/main/docs/Data_Standardization/motivation.md). Les opportunités de standardisation existent à plusieurs niveaux : format syntaxique des données du projet, provenance/processus/workflow/fichiers/dossiers, ainsi qu’au niveau sémantique ou du « sujet » des ensembles de données, ce qui nécessite souvent des références au design expérimental, aux protocoles et autres données contextuelles. Cela permet de déterminer si les ensembles de données ou les points de données sont comparables, ce qui est essentiel pour les catalogues de données en aval.

Un élément clé de réussite est un **langage technique bien coordonné pour décrire les objectifs et méthodes de recherche du projet, ainsi que les tableaux et champs des ensembles de données**. À l’avenir, l’intelligence artificielle pourrait associer les descriptions en langage naturel des utilisateurs aux contenus des catalogues de données. Quoi qu’il en soit, cette vision nécessite que les gestionnaires de données de projet fournissent des informations suffisantes à différents niveaux comme illustré ci-dessous.

## Couches de standardisation

### Standardisation des schémas de données

Des [schémas de données harmonisés](https://climatesmartagcollab.github.io/Documentation-en/Data_Documentation/schemas.html) facilitent le partage de données entre pairs et la visibilité dans les catalogues. Cela implique de standardiser les schémas jusqu’au niveau des noms de champs et des valeurs de listes déroulantes, ou au moins de les mapper à leurs équivalents sémantiques. Les noms idiosyncratiques sont remplacés par des termes issus de standards. Voir la page [Standardisation des schémas de données](https://climatesmartagcollab.github.io/Documentation-en/Data_Standardization/schemas.html).

#### Niveau attribut du schéma de données

Les attributs peuvent être standardisés ou personnalisés à partir d’éléments de standards tiers :

- La spécification [NCBI BioSample](https://www.ncbi.nlm.nih.gov/biosample/docs/attributes/) est une bonne source pour décrire le contexte environnemental/agricole ou humain/animal/végétal des biosamples.
- Le standard JSON [Phenopacket](https://phenopacket-schema.readthedocs.io/en/latest/index.html) pour les données cliniques propose des « blocs de construction » incluant des [attributs de biosample](https://phenopacket-schema.readthedocs.io/en/latest/biosample.html), avec des vocabulaires structurés et des ontologies recommandées.
- **Ontologies** : Voir la section [ontologie](https://climatesmartagcollab.github.io/Documentation-en/Data_Standardization/ontology.html) pour une liste d’ontologies recommandées et leur mise en œuvre.

#### Niveau enregistrement du schéma de données

La production de données standardisées se fait souvent par copie ou mappage de spécifications cibles dans le [schéma de données](https://climatesmartagcollab.github.io/Documentation-en/Data_Standardization/schemas.html) du projet. Le NCBI BioSample est organisé en [packages](https://www.ncbi.nlm.nih.gov/biosample/docs/packages/) pour faciliter la compréhension. Ces spécifications ont été converties en format [MIxS LinkML](https://github.com/turbomam/mixs-subset-examples-first), avec une [documentation consultable](https://turbomam.github.io/mixs-subset-examples-first/).

Même si un schéma réutilise des éléments existants, il est important d’imposer des [conventions de nommage](https://climatesmartagcollab.github.io/Documentation-en/Data_Standardization/schemas.html) pour éviter des problèmes lors de la validation ou transformation des données.

#### Résumé du contenu des ensembles de données

La découvrabilité des ensembles de données est améliorée par :

- **Informations dérivées du schéma** : standards et vocabulaires utilisés.
- **Informations dérivées des données** : nombre d’enregistrements, taille, fréquence des mots-clés contextuels, etc.
- **Résumé métadonnées** : mots-clés standardisés via des ontologies (ex. [EDAM](https://bioportal.bioontology.org/ontologies/EDAM?p=classes&conceptid=topic_0003), [OBO Foundry](https://obofoundry.org/)), métadonnées spatio-temporelles (ex. [Canada](https://www.wikidata.org/wiki/Q16)).

### Fichiers, dossiers et workflow

Un projet contient de nombreux fichiers et dossiers générés par des workflows, qui doivent être organisés systématiquement, comme expliqué [ici](https://climatesmartagcollab.github.io/Documentation-en/Data_Standardization/files.html).

### Métadonnées de design expérimental et de protocole

Ces métadonnées permettent d’évaluer la pertinence d’un ensemble de données, surtout si les groupes expérimentaux ou le contexte ne sont pas évidents :

- [Experimental Design Assistant](https://nc3rs.org.uk/our-portfolio/experimental-design-assistant-eda)
- Ontologies comme [OBI](http://purl.obolibrary.org/obo/OBI_0500000) et [NCIT](http://purl.obolibrary.org/obo/NCIT_C15320)
- [Protocols.io](https://www.protocols.io/)

### Provenance

L’origine des ensembles de données, les projets, les personnes et les agences impliquées :

- Hébergement, auteurs, dates de publication, institutions, etc.
- Ontologie de provenance [PROVO](https://www.w3.org/TR/prov-overview/)
- Métadonnées Dublin Core [DCMI](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/)
- Identifiants auteurs [ORCID](https://orcid.org/)

### Gouvernance

La standardisation de la [gouvernance des données](https://github.com/ClimateSmartAgCollab/Documentation-en/blob/main/docs/Data_Sharing/index.md#administrative) inclut les critères d’accès et les processus d’authentification, avec des ontologies comme [DUO](https://github.com/EBISPOT/DUO) et des systèmes comme [OAuth 2.0](https://oauth.net/2/).

## Mise en œuvre

Les chercheurs ne devraient pas avoir à gérer seuls la standardisation, qui demande des compétences techniques et une connaissance des vocabulaires contrôlés. L’équipe DCC peut aider !

Si anticipée tôt, la standardisation peut se faire par copie de composants standards. Sinon, une transformation est nécessaire via des scripts ou des modèles programmatiques pour convertir les données vers des formats standardisés (ex. formats pris en charge par les [référentiels de stockage](https://climatesmartagcollab.github.io/Documentation-en/storage/)). Ce processus est souvent itératif.

## Ressources de formation

À définir

**Auteur : Damion Dooley**
