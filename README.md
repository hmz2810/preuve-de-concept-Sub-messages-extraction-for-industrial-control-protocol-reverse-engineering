# Proof of Concept (POC) : Extraction des Sous-Messages pour l'Ingénierie Inverse des Protocoles de Communication Industriels

## Description du projet
Ce projet représente un **Proof of Concept (POC)** basé sur l'article de **Liu et al. (2022)** intitulé **"Sub-messages extraction for industrial control protocol reverse engineering"**. L'objectif est de démontrer la faisabilité d'extraction des **sous-messages** à partir de protocoles de communication industriels **inconnus** en utilisant des **méthodes SIEP**.

Le projet propose une méthode pour :
- **Segmenter** les messages capturés dans un protocole inconnu.
- **Extraire les sous-messages** en analysant les motifs récurrents à l'aide d'outils comme l'entropie, l'autocorrélation et l'analyse de diversité.
- **Identifier un protocole spécifique** à partir d'une adresse réseau donnée sans avoir besoin de la documentation officielle du protocole.

Cette approche **POC** vise à prouver qu'il est possible de réaliser une analyse **d'ingénierie inverse** sur des protocoles inconnus pour découvrir leur structure sans documentation préalable.

## Méthodologie
Ce projet suit les étapes méthodologiques proposées par **Liu et al. (2022)**, avec quelques ajustements pour créer un **Proof of Concept** fonctionnel :

1. **Identification de la séparation entre l'en-tête et les données** : L'entropie est utilisée pour détecter la frontière entre l'en-tête fixe et les données variables.
2. **Analyse de la périodicité** des sous-messages via l'autocorrélation.
3. **Segmentation des messages** en utilisant la périodicité déterminée.
4. **Inférence de la signature du protocole** basée sur la diversité des valeurs dans les segments extraits.
5. **Visualisation de la stabilité** des sous-messages à l'aide d'une carte de chaleur pour analyser les zones fixes et dynamique

