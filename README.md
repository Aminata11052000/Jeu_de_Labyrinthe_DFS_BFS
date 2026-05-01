# Jeu de Labyrinthe — DFS et BFS

Projet pédagogique en Python implémentant deux algorithmes classiques de parcours de graphes (DFS et BFS) appliqués à la génération et à l'exploration interactive de labyrinthes.

## Table des matières

- [Présentation](#présentation)
- [Algorithmes implémentés](#algorithmes-implémentés)
- [Fonctionnalités](#fonctionnalités)
- [Stack technique](#stack-technique)
- [Prérequis](#prérequis)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Structure du projet](#structure-du-projet)
- [Comparaison DFS vs BFS](#comparaison-dfs-vs-bfs)

---

## Présentation

Ce projet illustre de manière concrète et visuelle comment les algorithmes DFS (parcours en profondeur) et BFS (parcours en largeur) permettent de générer et d'explorer un labyrinthe. Le joueur contrôle un personnage qui doit atteindre la sortie dans un temps imparti.

---

## Algorithmes implémentés

### DFS — Parcours en profondeur (Depth-First Search)

- Utilise une **pile (stack)** pour explorer les cellules
- Génère des labyrinthes avec de longs couloirs sinueux
- Temps imparti : 60 secondes
- Taille de cellule : 50 pixels

**Principe :** à chaque étape, l'algorithme choisit un voisin non visité, avance au maximum dans cette direction avant de revenir en arrière (backtracking) si aucun chemin n'est disponible.

### BFS — Parcours en largeur (Breadth-First Search)

- Utilise une **file (deque)** pour explorer les cellules
- Génère des labyrinthes plus ouverts avec de nombreuses bifurcations
- Temps imparti : 30 secondes
- Taille de cellule : 40 pixels

**Principe :** à chaque étape, l'algorithme explore tous les voisins au même niveau de distance avant de progresser plus loin, garantissant le chemin le plus court.

---

## Fonctionnalités

- Génération procédurale du labyrinthe au lancement
- Grille de 15x15 cases
- Déplacement du joueur avec les touches directionnelles
- Affichage des cellules visitées en bleu
- Détection automatique de l'arrivée à la sortie
- Chronomètre avec limite de temps
- Mesure du temps d'exécution de l'algorithme au démarrage

---

## Stack technique

| Composant | Outil |
|-----------|-------|
| Langage | Python 3 |
| Interface graphique | Pygame |
| Structure de données BFS | collections.deque |
| Structure de données DFS | Stack (liste Python) |

---

## Prérequis

- Python 3.7 ou supérieur
- pip

---

## Installation

1. Cloner le dépôt :

```bash
git clone https://github.com/Aminata11052000/Jeu_de_Labyrinthe_DFS_BFS.git
cd Jeu_de_Labyrinthe_DFS_BFS
```

2. Créer et activer un environnement virtuel :

```bash
python -m venv venv
source venv/bin/activate      # Linux / macOS
venv\Scripts\activate         # Windows
```

3. Installer les dépendances :

```bash
pip install pygame
```

---

## Utilisation

Lancer la version DFS :

```bash
python "labyrinthe_DFS_v2 (1).py"
```

Lancer la version BFS :

```bash
python "labyrinthe_BFS (1).py"
```

Commandes en jeu :

| Touche | Action |
|--------|--------|
| Fleche haut | Déplacer le joueur vers le haut |
| Fleche bas | Déplacer le joueur vers le bas |
| Fleche gauche | Déplacer le joueur vers la gauche |
| Fleche droite | Déplacer le joueur vers la droite |

Objectif : atteindre la sortie avant la fin du chronomètre.

---

## Structure du projet

```
Jeu_de_Labyrinthe_DFS_BFS/
├── labyrinthe_DFS_v2 (1).py    # Implémentation avec DFS (pile)
├── labyrinthe_BFS (1).py       # Implémentation avec BFS (file)
├── image1.jpeg                  # Sprite du joueur
├── image2.jpeg                  # Sprite des cases
└── README.md
```

---

## Comparaison DFS vs BFS

| Critère | DFS | BFS |
|---------|-----|-----|
| Structure utilisée | Pile (stack) | File (deque) |
| Style de labyrinthe généré | Longs couloirs sinueux | Nombreuses bifurcations |
| Temps imparti | 60 secondes | 30 secondes |
| Taille de cellule | 50 px | 40 px |
| Garantit le chemin le plus court | Non | Oui |
| Consommation mémoire | Faible | Plus élevée |
