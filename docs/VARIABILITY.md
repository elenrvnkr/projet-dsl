<!-- Q6. Variabilité. Dans docs/VARIABILITY.md, décrivez l’espace de variantes : ce qui varie, les contraintes entre ces variations, des configurations nommées (presets). Faites au moins aussi bien que Ludii, avec au moins 2 variantes que Ludii ne propose pas. Quand une variation est-elle fixée : à l’écriture du programme, au lancement d’une partie, en cours de partie ? C’est un choix technique, qui vous revient ; une variation fixée tard peut, elle aussi, changer les règles. Estimez le nombre de configurations, et lesquelles sont assez petites pour être résolues. Illustrez par 2–3 scénarios d’usage. -->

# Espace de variantes

Types de variations observées sur Ludii :

- Plateau :
  - taille,
  - forme,
  - espace dimensionnel.
- Nombre de joueurs.
- Condition de victoire.
- Comportement des pions :
  - quels placements sont autorisés,
  - disparition au bout d'un certain nombre de tours ou non,
  - interaction avec les autres pions,
  - déplacement autorisé ou non.

Variations non observées sur Ludii :

- blablabla

Contraintes entre les variations :

- La taille du plateau et la condition de victoire doivent être adaptées au nombre de joueurs pour permettre à un joueur de gagner.
- La condition de victoire doit prendre en compte l'espace dimensionnel.
