<!-- Q6. Variabilité. Dans docs/VARIABILITY.md, décrivez l’espace de variantes : ce qui varie, les contraintes entre ces variations, des configurations nommées (presets). Faites au moins aussi bien que Ludii, avec au moins 2 variantes que Ludii ne propose pas. Quand une variation est-elle fixée : à l’écriture du programme, au lancement d’une partie, en cours de partie ? C’est un choix technique, qui vous revient ; une variation fixée tard peut, elle aussi, changer les règles. Estimez le nombre de configurations, et lesquelles sont assez petites pour être résolues. Illustrez par 2–3 scénarios d’usage. -->

# Espace de variantes

## Variations

Types de variations observées sur Ludii :

- Plateau :
  - taille (longueur, largeur, hauteur),
  - forme,
  - espace dimensionnel.
- Nombre de joueurs.
- Condition de victoire.
- Comportement des pions :
  - quels placements sont autorisés,
  - combien de pions par tour peuvent être placés,
  - disparition au bout d'un certain nombre de tours ou non,
  - interaction avec les autres pions,
  - déplacement autorisé ou non.
- Dimension des lignes :
  - longueur des lignes,
  - directions comptées (horizontal, vertical, diagonal)

Variations non observées sur Ludii :

à vérifier mais j'ai pas vu :
- cases bloquées sur le plateau ?
- bords reliés ???
- pie rule ???
- blablabla

## Contrainte entre variations

- La taille du plateau et la condition de victoire doivent être adaptées au nombre de joueurs pour permettre à un joueur de gagner.
- La condition de victoire doit prendre en compte l'espace dimensionnel.
- La longueur de ligne doit tenir sur le plateau dans au moins une des directions choisies
- Si on fait disparaitre les pions au bout d'un nombre de tour N, il faut que N soit supérieur ou égal à la longueur de ligne
- Quand on ne peut placer le pion qu'à côté d'un pion déjà placé, le premier pion peut être placé partout

## Configurations nommées

- TicTacToe : plateau 3x3, placement libre, un pion placé par tour, 2 joueurs, faire une ligne de 3
- MisereTicTacToe : plateau 3x3, placement libre, un pion placé par tour, 2 joueurs, éviter une ligne de 3
- ConnectFour : plateau 7x6, placement selon la gravité, un pion placé par tour, 2 joueurs, faire une ligne de 4
- Connect6 : 	plateau 19x19, placement libre, un ou deux pions placés par tour, 2 joueurs, faire une ligne de 6
- TicTacMo : 	plateau 3x3, placement libre, un pion placé par tour, 3 joueurs, faire une ligne de 3

## Quand une variation est-elle fixée ?

- à l’écriture du programme : plateau (taille, cases bloquées, bords reliés), longueur et directions de ligne, but, mode de placement, pions par tour, disparition des pions, nombre de joueurs
- au lancement d’une partie : choix du preset, qui joue en premier, IA de chaque joueur
- en cours de partie : 

## Nombre de configurations

## Scénarios d'usage