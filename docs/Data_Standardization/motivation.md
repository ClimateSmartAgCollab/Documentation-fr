---
layout: default
title: Motivation
parent: Standardisation des données
nav_order: 1
---

# Motivation pour la standardisation des données
{: .no_toc }

## Table des matières
{: .no_toc .text-delta }

1. TOC
{:toc}

Bien que les ensembles de données d’un projet soient souvent construits et hébergés pour répondre aux besoins immédiats de ses objectifs de recherche, une attention supplémentaire est généralement nécessaire pour créer des produits de données standardisés afin qu’ils puissent être facilement trouvés et réutilisés par d’autres parties prenantes (universitaires, gouvernements, industries, agences de recherche, etc.). Même si les ensembles de données sont enregistrés dans des catalogues FAIR (ou portails de recherche de données), leur découverte et réutilisation peuvent être entravées par des métadonnées et données non harmonisées, surtout dans le contexte de la prolifération des ensembles de données expérimentaux et de surveillance dans de nombreux domaines de recherche. Nous reconnaissons que de nombreuses interfaces de recherche de catalogues de données ne peuvent pas encore exploiter des métadonnées riches, mais en attendant, ce sont des informations que les chercheurs doivent examiner manuellement pour juger de la pertinence des ensembles de données.

## Trouvabilité

Défis rencontrés par les chercheurs et autres utilisateurs de données :

- **Catalogues de données** : Pour la découverte, il faut soumettre les métadonnées des ensembles de données à des catalogues comme [FAIRsharing.org](https://fairsharing.org/) ou [Google Dataset Search](https://datasetsearch.research.google.com/), mais ces catalogues n’utilisent souvent pas le même cadre de description des données (comme [Schema.org Dataset](https://schema.org/Dataset)) ni les mêmes termes sémantiques.
- **Cohérence des mots-clés** : Dans les catalogues, la description sémantique d’un ensemble de données se limite souvent à un ensemble de mots-clés — souvent du texte libre riche en synonymes ou sélectionné à partir d’un menu large mais non exhaustif. Même avec des vocabulaires contrôlés, les changements de terminologie compliquent la récupération des résultats passés et présents (ex. en taxonomie : « Malus pumila » vs. « Malus domestica » pour désigner le pommier).
- **Précision et rappel des résultats de recherche** : Une recherche avec quelques mots-clés généraux peut produire trop de résultats (faux positifs), tandis qu’une recherche plus spécifique peut exclure des ensembles pertinents (faux négatifs). L’utilisation des mots-clés est souvent incohérente et insuffisante pour bien différencier les contenus.
- **Filtres dimensionnels** : Les filtres liés au design expérimental, à la démographie des sujets, ou au contexte biologique/social sont souvent absents, obligeant à des vérifications supplémentaires pour savoir si les types de données sont comparables. Certains champs standards existent (ex. [temporalCoverage](https://schema.org/temporalCoverage), [countryOfOrigin](https://schema.org/countryOfOrigin), [contentLocation](https://schema.org/contentLocation)).

## Réutilisation

Une fois que le chercheur a trouvé des bases de données adaptées, une grande partie de son temps est souvent consacrée à l’harmonisation des champs de données. On estime que 80 % du temps d’un doctorant est consacré au nettoyage et à la préparation des données. C’est pourquoi les [partisans des données FAIR](https://www.nature.com/articles/d41586-020-00505-7) recommandent d’investir 5 % du budget d’un projet dans la standardisation des données pour réduire cette charge en aval et éviter les coûts d’opportunité liés à l’échec de la découverte de données.

Une attention précoce à la standardisation favorise la réutilisation et évite les efforts coûteux de mappage entre ensembles de données lorsque de nouveaux utilisateurs apparaissent. Les sections sur la [standardisation des schémas de données](https://climatesmartagcollab.github.io/Documentation-en/Data_Standardization/schemas.html) et les [ontologies](https://climatesmartagcollab.github.io/Documentation-en/Data_Standardization/ontology.html) proposent des moyens de réduire cette charge.

**Auteur : Damion Dooley**
