---
layout: default
title: Normes de fichiers, dossiers et flux de travail
parent: Standardisation des données
nav_order: 5
---

# Normes de fichiers, dossiers et flux de travail
{: .no_toc }

## Table des matières
{: .no_toc .text-delta }

1. TOC
{:toc}

## Normes de fichiers

Les noms de fichiers, les formats et les jeux de caractères ont chacun des aspects de standardisation.

### Pourquoi standardiser les noms de fichiers ?

La standardisation des conventions de nommage des fichiers aide les chercheurs à mieux organiser leur travail et à collaborer avec d'autres. Les avantages incluent :

* Une structure cohérente entre les fichiers, facilitant la localisation et l'identification des documents.
* Des noms de fichiers uniformes facilitent le tri et l'organisation alphabétique ou chronologique.
* Favorise une compréhension partagée de la manière dont les fichiers sont nommés et organisés.
* L'inclusion de numéros de version ou de dates dans les noms de fichiers permet une gestion efficace des versions.

### Recommandations pour le nommage des fichiers

La bibliothèque de Caltech propose une [feuille de travail sur les conventions de nommage des fichiers](https://doi.org/10.7907/894q-zr22) avec une série de questions et de conseils, aboutissant à un modèle de convention de nommage avec des exemples pour le plan de gestion des données du projet.  
Exemple de modèle : `SA-MPL-EID_YYYYMMDD_###_status.tif`  
Exemples : `P1-MUS-023_20200229_051_raw.tif` et `P2-DRS-285_20191031_062_composite.tif`

### Jeux de caractères des fichiers

Les données « sérialisées » dans un fichier texte sont encodées sous forme de chaînes de caractères issues d’un jeu de caractères, pouvant inclure des accents, etc.  
Le standard populaire [UTF-8](https://en.wikipedia.org/wiki/UTF-8) (utilisé pour la majorité des pages web) couvre de nombreuses langues et même des [dingbats](https://en.wikipedia.org/wiki/Dingbat).  
Malheureusement, ce n’est pas le seul jeu de caractères existant, et les logiciels doivent souvent deviner l’encodage d’un fichier d’entrée. Certaines versions de programmes comme [MS Excel](https://support.guidebook.com/hc/en-us/articles/360016372414) utilisent leur propre codage, ce qui peut entraîner des confusions lors de la traduction.  
Si des caractères étranges s’affichent dans une application à partir d’un fichier d’entrée, essayez de réenregistrer ce fichier avec un jeu de caractères approprié avant de l’ouvrir dans l’application.

## Directives sur la structure des dossiers

Comme mentionné dans la section [Analyse des données](https://climatesmartagcollab.github.io/Documentation-en/Data_Analysis/), le [Protocole TIER 4.0](https://www.projecttier.org/tier-protocol/protocol-4-0/) est une structure de fichiers recommandée pour les pipelines analytiques.

## Plans de gestion des données

Tous les projets de recherche de l’initiative *Agriculture et systèmes alimentaires adaptés au climat* de Genome Canada ont créé un [Plan de gestion des données (PGD)](../datamanagementplan.md) en utilisant l’[Assistant PGD de Portage](https://dmp-pgd.ca/).  
Ce PGD inclut généralement des protocoles de nommage de fichiers recommandés pour chaque projet de recherche.

## Recommandations

Briney, Kristin A. 2020. “File Naming Convention Worksheet”. 2 juin.  
[https://doi.org/10.7907/894q-zr22](https://doi.org/10.7907/894q-zr22)

- Auteurs : Carly Huitema, Damion Dooley
