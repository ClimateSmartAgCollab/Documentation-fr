---
layout: default
title: Standardisation des schémas de données
parent: Normalisation des données
nav_order: 2
---

# Standardisation des schémas de données
{: .no_toc }

## Table des matières
{: .no_toc .text-delta }

1. TOC
{:toc}

# Standardisation des schémas de données
Les schémas de données, qu’ils décrivent les détails syntaxiques et sémantiques d’une seule table ou qu’ils couvrent plusieurs tables interconnectées ou des transformations entre elles, offrent de nombreuses opportunités de standardisation. Nous commençons par une description et des recommandations sur le langage actuellement utilisé pour décrire le contenu des schémas de données, puis nous discutons de la manière dont des vocabulaires structurés, y compris des ontologies, peuvent être superposés pour aider à déterminer la comparabilité sémantique.

## Valeurs
Un champ de formulaire, un champ d’enregistrement, un champ de ligne de tableau, une cellule de feuille de calcul, un attribut ou une propriété d’objet/class informatique, ou une variable peut contenir une **valeur** (aussi appelée élément de données ou donnée).

## Types de données fondamentaux
Essentiels pour la lisibilité par machine, une valeur peut appartenir à un certain type de données « littéral » ou syntaxique, comme une chaîne de caractères, une date, une heure, un entier ou un nombre décimal, un booléen, une valeur catégorielle ou un type de référence URL. Quelques langages standards d’échange de données permettent d’exprimer cela : [XML](https://www.w3.org/TR/xmlschema11-2/#built-in-datatypes), [JSON](https://json-schema.org/understanding-json-schema/reference/type) et [SQL](https://www.digitalocean.com/community/tutorials/sql-data-types).

- **Unités** : Les valeurs numériques peuvent être accompagnées d’unités (ex. « 1m » pour un mètre, ou « 2d » pour 2 jours). Ces unités peuvent être intégrées dans une chaîne ou stockées séparément. Des représentations codées comme [UCUM](https://units-of-measurement.org/) ou des ontologies comme [QUDT](http://qudt.org/), [OM](http://www.ontology-of-units-of-measure.org/), [UO](https://obofoundry.org/ontology/uo) sont utilisées.
- **Syntaxe des chaînes** : Des contraintes supplémentaires peuvent être imposées sur les chaînes pour exprimer des formats complexes, comme les coordonnées géographiques selon [ISO 19115-1:2014](https://www.iso.org/standard/53798.html), souvent via des [expressions régulières](https://en.wikipedia.org/wiki/Regular_expression).
- Les spécifications de données spécifiques à un projet peuvent permettre des descriptions plus souples, mais les standards visent à minimiser les ambiguïtés (ex. « 04/05/11 » peut être interprété différemment selon le format).

## Attributs
Un enregistrement, une feuille de calcul, un objet informatique ou une entité ontologique peut avoir plusieurs **attributs** obligatoires ou facultatifs. Selon le contexte, un attribut peut aussi être appelé champ, propriété, variable, caractéristique ou slot.

- **Nom d’attribut** : Il peut y avoir ambiguïté entre le nom affiché, le nom standardisé ou le nom utilisé dans les scripts. Il faut distinguer :
  - **Nom en langage naturel** : Pour l’interface utilisateur (ex. « Date de naissance »).
  - **Nom codé** : Pour les scripts ou bases de données (ex. « birth_date »), suivant des conventions comme [PEP8](https://peps.python.org/pep-0008/) ou [R/SQL](https://bookdown.org/content/d1e53ac9-28ce-472f-bc2c-f499f18264a3/names.html).
    - **PascalCase** : Pour les noms de tables/objets.
    - **lower_camel_case** : Pour les noms d’attributs.
    - Expressions régulières pour Excel sont fournies pour automatiser la conversion.
  - **Référence à un terme standardisé** : Via des identifiants permanents (purl), comme [cell type](http://purl.obolibrary.org/obo/CL_0000000).

## Valeur(s) d’un attribut
Un attribut peut avoir plusieurs types de valeurs, comme une date ou une liste de valeurs nulles (ex. données manquantes). Des standards comme [NCBI](https://www.ddbj.nig.ac.jp/biosample/submission-e.html#missing-value-reporting) couvrent cela. Certains champs permettent des sélections multiples, nécessitant des chaînes délimitées ou des structures de données plus complexes.

## Sémantique des attributs
Un attribut a un **type de données** fondamental et un **type sémantique** contextuel. Par exemple, « âge » peut être un entier, mais il existe plusieurs types d’âge ([liste ici](http://purl.obolibrary.org/obo/OBI_0001167)). Les définitions textuelles ne suffisent pas pour les machines, d’où l’importance des vocabulaires standardisés.

- **Mesures** : Un même attribut peut être mesuré différemment (ex. « age_in_years », « age_in_weeks », « gestational_age »).
- **Attributs catégoriels** : Utilisés dans les enquêtes (ex. « jeune / adulte / âgé »). Les schémas doivent indiquer les vocabulaires utilisés ou leurs sources en ligne.

## Attributs composés
Ce sont des structures de données composées de plusieurs attributs (ex. « geo_location » combinant latitude et longitude). Les concepteurs de schémas préfèrent souvent décomposer ces structures en attributs distincts.

## Identifiants permanents
Les références à des ressources web (datasets, documents, termes de vocabulaire) utilisent des **URL permanentes (purl)**, comme [OBI_0001167](http://purl.obolibrary.org/obo/OBI_0001167). Ces liens doivent rester accessibles ou être redirigés vers des versions mises à jour. Des registres comme [w3id.org](https://w3id.org/) ou [bioregistry.io](https://bioregistry.io/) permettent de gérer ces identifiants.

## Vocabulaire structuré
Un **vocabulaire structuré** (ou contrôlé) est un fichier de termes incluant noms, définitions, hiérarchies sémantiques, etc. Les agences peuvent recommander des vocabulaires pour leurs projets. Exemples :

- [Ontologies pour l’agriculture – CGIAR](https://bigdata.cgiar.org/ontologies-for-agriculture/)
- [AgroPortal](https://agroportal.lirmm.fr/)
- [OBO Foundry](https://obofoundry.org/)
- [OLS – EMBL-EBI](https://www.ebi.ac.uk/ols4)
- [Fairsharing.org](https://fairsharing.org/search?fairsharingRegistry=Standard)
- [Wikidata](https://www.wikidata.org/wiki/)
- [GOLD](https://gold.jgi.doe.gov/ecosystem_classification)

## Sources d'attributs standardisés
Les termes d'ontologie peuvent être précis pour décrire une chose mesurée, mais pas la manière dont elle est mesurée. Les attributs de schéma de données vont souvent plus loin que les ontologies dans la mesure où les spécifications d'attribut incluent le type de données de la ou des valeurs. Les attributs standardisés avec des noms de codage se trouvent par exemple dans les normes de référentiel plat [NCBI BioSample](https://www.ncbi.nlm.nih.gov/biosample/docs/packages/) et dans les normes plus structurées [Phenopacket](https://phenopacket-schema.readthedocs.io/). Plus de détails sur l'utilisation du vocabulaire structuré, y compris les ontologies, sont fournis dans la section [ontologie](https://climatesmartagcollab.github.io/Documentation-en/Data_Standardization/ontology.html).

## Ressources de formation
À déterminer

Auteurs : Damion Dooley
