# INF8225 - Étude Comparative de SegFormer et U-Net

Ce dépôt contient le projet final pour le cours **INF8225 (Intelligence Artificielle)** à Polytechnique Montréal. Nous comparons deux architectures majeures pour la segmentation d'images dans un contexte de conduite autonome.

## 📋 Aperçu du Projet
L'objectif est d'analyser le compromis entre la **précision** des résultats et la **vitesse d'exécution** (temps réel). 

Nous opposons deux approches :
* **U-Net (ResNet-18) :** Un modèle classique basé sur les convolutions, reconnu pour sa précision sur les détails locaux.
* **SegFormer (MiT-B0) :** Une approche moderne basée sur les Transformers, conçue pour capturer un contexte plus large tout en restant très légère.

## 🧠 Méthodologie (Vue d'ensemble)

Le projet suit un pipeline simplifié :
1.  **Données :** Utilisation du dataset **CamVid** (scènes routières). Les images sont redimensionnées et normalisées.
2.  **Entraînement :** Les deux modèles sont entraînés avec les mêmes paramètres de base (optimiseur AdamW, perte de type Cross-Entropy) pour assurer une comparaison équitable.
3.  **Évaluation :** Nous mesurons la performance selon deux critères :
    * **mIoU :** Est-ce que le modèle identifie correctement les pixels (route vs piéton) ?
    * **FPS :** Est-ce que le modèle est assez rapide pour être utilisé sur une voiture en mouvement ?

 ## 👥 Équipe

Guillaume Gauthier

Van-Truong David Vo

Jonathan Kim

## 📚 Références

SegFormer: Simple and Efficient Design for Semantic Segmentation with Transformers (Xie et al., 2021)

U-Net: Convolutional Networks for Biomedical Image Segmentation (Ronneberger et al., 2015)
