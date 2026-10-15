# Reconnaissance de panneaux de signalisation (GTSRB)

Projet du cours **Fondamentaux du Deep Learning** (ING3 IA, semestre 1, 2026-2027).

**Binôme :** COMPARETTO Romain - Ait El Hadj Sofiane

[![Ouvrir dans Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/romainc12/gtsrb-deep-learning/blob/main/Projet_Panneaux_GTSRB.ipynb)

## Contenu

| Fichier | Description |
|---|---|
| `Projet_Panneaux_GTSRB.ipynb` | Notebook complet, déjà exécuté (les sorties et les graphiques sont visibles sans relancer) |

## Résumé

Classification des 43 classes du dataset GTSRB (German Traffic Sign Recognition Benchmark).

| Modèle | Accuracy validation |
|---|---|
| Réseau dense (référence) | 84,2 % |
| CNN de base | 96,1 % |
| CNN + Dropout + Data Augmentation + 64/128 filtres (modèle final) | 98,75 % |
| MobileNetV2 fine-tuné (bonus) | 87,0 % |

**Modèle final sur le jeu de test : 97,9 %.**

Plan du notebook : préparation des données (découpage train / validation par série pour éviter les fuites), réseau dense de référence, construction et entraînement du CNN, analyse des erreurs, expériences (Dropout, Data Augmentation, nombre de filtres, learning rate), puis Transfer Learning en bonus.

## Relancer le notebook

1. Cliquer sur le badge « Open in Colab » ci-dessus.
2. Choisir un GPU : *Exécution > Modifier le type d'exécution > GPU*.
3. *Exécution > Tout exécuter*. Le dataset est téléchargé automatiquement depuis Kaggle avec `kagglehub` (un compte Kaggle peut être demandé).

## Données

Le dataset n'est pas inclus dans ce dépôt (environ 600 Mo). Il est téléchargé par le notebook depuis [Kaggle](https://www.kaggle.com/datasets/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign).

Source : J. Stallkamp, M. Schlipsing, J. Salmen, C. Igel, *Man vs. computer: Benchmarking machine learning algorithms for traffic sign recognition*, Neural Networks, 2012. Site officiel : https://benchmark.ini.rub.de/gtsrb_news.html
