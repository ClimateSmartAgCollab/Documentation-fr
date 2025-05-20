---
layout: default
title: Écrire un schéma
parent: Documentation des données
nav_order: 3
---

# Écrire un schéma
{: .no_toc }

## Table des matières
{: .no_toc .text-delta }

1. TOC
{:toc}

Tous les ensembles de données ont un schéma, implicite ou explicite. L'objectif du moteur sémantique est de prendre vos connaissances des données et de les documenter explicitement à l'aide d'un schéma.

Pour écrire facilement des schémas lisibles par machine dans le langage de schéma OCA, l'organisation *Agri-food Data Canada (ADC)* de l'Université de Guelph a développé une interface utilisateur conviviale pour documenter les données et utiliser les schémas qui ont été générés.

## Utilisation du moteur sémantique

Le [moteur sémantique](https://www.semanticengine.org) a été développé pour être un site autodirigé permettant aux chercheurs de documenter toutes les données de recherche basées sur des tableaux. Tout au long du site, vous trouverez une documentation utile ainsi qu'une [page Web de didacticiel](https://agrifooddatacanada.github.io/OCA_Composer_help_pages/en/TutorialAll/).

<iframe width="560" height="315" src="https://www.youtube.com/embed/ekMmpx_w45M?si=fZKfGS9Z7QEexCb5" title="Lecteur vidéo YouTube" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Utiliser un schéma

### Créer un fichier Excel de saisie de données

Sur le site Web [Semantic Engine](https://www.semanticengine.org), vous pouvez utiliser la version lisible par machine de votre schéma pour générer une feuille Excel préremplie selon les règles du schéma et prête pour la saisie de données.
![Saisie de données Excel](../assets/images/dee_dataentry.png)

Lorsque vous ouvrez votre fichier Excel de saisie de données, vous verrez qu'il se compose de deux feuilles, une pour la description du schéma et une pour la saisie des données. Les feuilles de description du schéma récupèrent les informations du schéma téléchargé et les placent dans une table d'informations.

### Vérifier les données dans un navigateur Web

Vous pouvez utiliser votre schéma pour saisir et vérifier des données à l'aide de votre navigateur Web.

![Vérification des données](../assets/images/dew_data_verification.PNG)

L'outil Web de saisie de données du [moteur sémantique](https://www.semanticengine.org) vous permet de télécharger votre schéma, puis vous pouvez éventuellement télécharger un ensemble de données. Si vous choisissez de télécharger un ensemble de données, n'oubliez pas que l'outil du moteur sémantique ne reçoit jamais vos données. Au lieu de cela, vos données sont « téléchargées » dans votre navigateur et tout le traitement des données se déroule localement.

Si vous ne souhaitez pas télécharger un ensemble de données, vous pouvez ignorer cette étape et aller directement à la fin où vous pouvez saisir et vérifier vos données dans le navigateur Web. Ajoutez des lignes de données vides à l'aide du bouton « Ajouter des lignes » en bas, puis saisissez les données. Vous pouvez survoler les ? pour voir quelles données sont attendues, ou cliquer sur les « règles de vérification » pour revoir le schéma afin de vous aider à saisir vos données.

### Enregistrez vos données avec votre schéma

Stockez votre schéma de plusieurs manières.

1. Stockez un schéma avec votre ensemble de données et partagez-le lorsque vous partagez vos données.
2. Partagez un schéma avec votre laboratoire ou vos collaborateurs en le stockant dans un lecteur de laboratoire partagé.
3. Stockez votre schéma en tant qu'objet indépendant dans un dépôt de données tel que Borealis ou Zenodo.

Stockez ensemble la version groupée du schéma lisible par machine et la version .txt lisible par l'homme pour une meilleure convivialité.

### Contribuer à la bibliothèque de schémas

Le projet Data Hub de Génome Canada crée une [bibliothèque de schémas](https://climatesmartagcollab.github.io/HUB-Harmonization/) dans le cadre de son mandat visant à aider à l'harmonisation des données et à la création de normes de données entre les membres du projet.

Après avoir créé votre schéma de données à l'aide du moteur sémantique, vous pouvez télécharger votre bundle de schémas lisible par machine et générer le fichier readme Markdown. Sélectionnez le scénario *Data Hub* pour ajouter le nom de votre équipe EID, l'auteur du schéma et l'adresse e-mail afin que votre schéma soit correctement trié dans la bibliothèque et que les autres membres de Data Hub puissent voir quelles données vous produisez.

- écrit par Carly Huitema
