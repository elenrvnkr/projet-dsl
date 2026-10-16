# Comparaison : 

Références choisies : Tic-Tac-Mo

## Tic-Tac-Mo.lud :

Langage utilisé pour le Tic-Tac-Mo disponible dans le folder ludii de ce projet. Pour une version du Tic-Tac-Toe à trois personnes (O,X,Y).

Il définit l'équipement( taille du board, les différentes pièces qui appartiennent aux différents joueurs,...) les règles, et la condition de fin

## Boop.lud : 

Celui-ci est un peu différent car il définit des fonctions qui lui sont propres, comme le recul, que fait le boop lorsqu'on pose un chat à côté d'un autre (uniquement si la case sur laquelle il se fait pousser est libre). Il a aussi la fonction promoteLine3 qui permet de tester si une ligne de 3 chats de la même couleur a été crée, auquel cas la fonction 

(issus du cours)

## GDL: Stanford General Game Playing (excerpt) : 
(role x) (role o)
(init (cell 1 1 b)) ... (init (control x))
(<= (legal ?p (mark ?m ?n))
(true (cell ?m ?n b)) (true (control ?p)))
(<= (next (cell ?m ?n ?p))
(does ?p (mark ?m ?n)))
(<= terminal (line ?p))
(<= (goal ?p 100) (line ?p)
GDL: logic programming (Datalog-like). General game players read the rules of a game they have never seen, then play it.
GDL-II adds chance and hidden information (cards!)

## Ludii (.lud): the complete game

(game "Tic-Tac-Toe"
(players 2)
(equipment {
(board (square 3))
(piece "Disc" P1)
(piece "Cross" P2)
})
(rules
(play (move Add (to (sites Empty))))
(end (if (is Line 3) (result Mover Win)))))

Ludii: hundreds of ludemes (board, piece, move, Line…) as domain concepts; 1,000+ traditional games and generic AI
players included

## RBG

RBG (regular languages, fast reasoning)

## un autre protocole (mort)