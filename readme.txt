Description

+ jeu de tir
+ projet solo [Mathilde MERLANGE]
+ unity 2019.2.9f1

Travail effectué

+ sujet complet (SHOOTER.PDF)
+ ajout fond d'écran
+ ajout "game over"
+ ajout "contrôles tactiles"

Game over (le plus problématique à faire)

+ Problème : mettre le jeu en pause à la fin de la partie
+ Tentative : création d'une scène pour la fin du jeu et passage d'une scène à l'autre -> échec
+ Solution : utilisation de "Time.timeScale = 0" pour stopper toutes les animations du jeu.



+ Objectif : afficher un message pour indiquer la fin de la partie
+ Problème : comment n'afficher le message qu'à certaines conditions?
+ Tentative : créer un texte caché et ne le réactiver qu'en fin de partie
+ Solution : modifier l'affichage du score par "score + message" avec un message vide pendant le jeu auquel on ajoute le texte à la fin de la partie

Contrôles tactiles

+ Délimitation des zones de déplacement aux bords de l'écran
+ Assignation d'une direction par bord de l'écran en fonction de l'orientation de celui-ci (portrait ou paysage)

Création d'un astéroïde

+ Objectif : ajouter un autre astéroïde si nombreAsteroid<10
+ Problème : code ajouté à la fonction Update() -> 50 astéroïdes en 1 seconde
+ Solution : 
  + déplacement du code dans la fonction "respawn"
  + utilisation de "InvokeRepeating" pour exécuter "respawn" tous les 8/10 secondes

Tentative

+ Relancer le jeu après le game over -> échec (probablement dû au Singleton)

Contrôles

+ PC
  + ←→↑↓ pour se déplacer
  + "espace" pour tirer
+ Android
  + toucher pour tirer
  + toucher et maintenir les cotés de l'écran pour se déplacer

Tests

+ ubuntu 18.04 (1920*1080)
+ galaxy a5 2017 (android 8) mode paysage
+ galaxy a10 (android 9) mode paysage
+ web gl (firefox 71)
+ Nécessité de lancer le jeu en mode paysage sur mobile pour pouvoir jouer. En mode portrait l'affichage est cassé

Bugs

+ L'affichage du score est toujours "derrière" les éléments du jeu



PS

+ Les fins de lignes des scripts sont toutes au format Unix (LF)
