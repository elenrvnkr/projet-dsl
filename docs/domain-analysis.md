<!-- Q3. Analyser. Dans docs/domain-analysis.md : les concepts de vos jeux et leurs variantes, d’après vos sources ; comment Ludii les décrit, et ce que vous en retenez ou non ; ce que votre DSL couvrira, ce qu’il laissera de côté, et pourquoi -->

# Analyse du domaine

## Concepts de la famille alignement

Les jeux du dossier ludi/ sont des jeux d'alignements où l'objectif est soit d'aligner un certain nombre de pion sur un plateau, soit de ne pas le faire. Une fin de partie arrive lorsqu'un joueur gagne ou lorsque le plateau est plein.

Concepts :
- plateau : grille de cases discrètes
- pion : pièce posée sur une case, différente selon le joueur (croix, rond, couleur)
- placement:  règle qui dit où on peut poser les pions (partout, en bas d'une colonne, à côté d'un pion existant)
- ligne : suite de pions du même jour dans la même direction
- but : former une ligne ou éviter d'en former
- fin de partie : victoire ou plateau plein

## Variantes

Leurs variantes reposent selon : 
- si le but est d'aligner des pions ou, au contraire, de faire en sorte que l'adversaire aligne ses pions
- le nombre de pions nécessaires à aligner (3,4,5,6...)
- la taille du plateau
- les modalités de déplacement des pions (par exemple : on peut placer partout sur le plateau du tic tac toe alors qu'on peut pas le faire dans le puissance 4)
- si les lignes formées peuvent être diagonales ou pas, si elles peuvent être horizontales ou pas, verticales ou pas...
- le nombre de pions placés par tour
- le nombre de joueurs
- disparition des pions au bout d'un certain nombre de coups ou pas
- interactions entre les pions (poussée dans Boop)
- Si les lignes formées doivent être strictement égal au nombre de pions nécessaires à aligner ou plus (gomoku)

## Comment Ludii les décrit

Ludii les décrit en utilisant un langage Lud avec des ludemes (board, piece, move, is Line...). Un jeu est décrit par ses joueurs, son équipement (plateau, pièces...) et ses règles (play, end):

```
(game "Tic-Tac-Toe" 
    (players 2) 
    (equipment { 
        (board (square 3)) 
        (piece "Disc" P1) 
        (piece "Cross" P2) 
    }) 
    (rules 
        (play (move Add (to (sites Empty))))
        (end ("Line3Win"))
    )
)
```

On en retient la condition de fin qui

On en retient pas la généralité qui permet à lud de décrire autant des jeux d'alignement que des jeux de blocages, les métadonnées, 

## Ce que notre DSL couvrira, laissera de côté et pourquoi