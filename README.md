# Projet DSL

On explore la famille alignement. 

Le périmètre contient les jeux où des joueurs posent des pions à tour de rôle sur un plateau discret et où le résultat dépend de la formation d'une ligne de pions d'une longueur donnée. Elle est assez riche pour un DSL : il y a un bon nombre de paramètres (taille et forme du plateau, longueur de ligne, directions autorisées, mode de placement, nombre de joueurs, but du jeu) ce qui produit des milliers de variantes. Ce n'est pas non plus trop compliqué : le moteur est simple (poser des pions, tester les lignes). Plusieurs de ces jeux sont dans Ludii, qui sert d'oracle. Elle exclut les jeux solitaires et les jeux dont le but n'est pas un alignement (connexion comme Hex, semailles comme Awari...).

Utilisation de l'IA : rien du tout