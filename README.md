# Système d'Analyse de Tennis basé sur l’IA avec YOLO

L'objectif du projet est de développer un système d'analyse de matchs de tennis à l'aide de techniques avancées d'***intelligence artificielle (IA)*** et d’***apprentissage automatique (ML)***. Le système doit être capable de détecter et suivre les joueurs et la balle de tennis, ainsi que d’analyser le mouvement à partir de points clés extraits du terrain. Il fournit des indicateurs essentiels comme :
1. Vitesse du joueur et distances parcourues.
2. Fréquence des coups de raquette.
3. Détection des balles "in" ou "out".
4. Trajectoire et vitesse de la balle tout au long du match.

Ce projet s’intègre dans les systèmes d’analyse de performance sportive et peut être utilisé pour des ***recherches avancées***, des ***rapports techniques*** ou pour les ***entraîneurs*** et ***analystes sportifs***.

## Fonctionnalités du Système:
1. **Détection des Joueurs et de la Balle :** Utilisation de YOLOv8 pour détecter les joueurs et YOLOv5 affiné pour capturer les balles rapides, avec des boîtes englobantes et un score de confiance.
2. **Suivi des Objets (Object Tracking) :** Chaque joueur reçoit un ID unique conservé à travers les frames, facilitant l’analyse des mouvements. Le suivi de la balle permet de calculer sa vitesse et sa trajectoire.
3. **Extraction des Points Clés du Court :** Un CNN détecte les lignes et coins du terrain. Ces points aident à mesurer les distances parcourues et à déterminer si la balle est "in" ou "out".
4. **Entraînement et Affinage des Modèles :** Le modèle YOLOv5 est affiné avec des datasets annotés. Le modèle CNN est optimisé pour détecter les points clés, en s’entraînant sur Google Colab avec GPU.
5. **Interpolation des Détections Manquantes :** Si certaines frames manquent de détection, Pandas est utilisé pour interpoler les positions et garantir une trajectoire continue.
6. **Visualisation et Sauvegarde des Résultats :** Les résultats sont visualisés avec des couleurs distinctes pour les joueurs et la balle. Pickle permet de sauvegarder les détections pour accélérer le développement, et OpenCV génère les vidéos annotées.

## Cas d’Utilisation:
- **Analyse de performance sportive :** aide les entraîneurs à identifier les forces et faiblesses des joueurs.
- **Analyse automatique des matchs :** détection des moments clés, mesure des statistiques (vitesse des joueurs et de la balle, distances parcourues).
- **Outils pour arbitres :** aide à déterminer si une balle est "in" ou "out".
- **Recherche en vision par ordinateur :** un exemple pratique de détection et de suivi d’objets dans un environnement sportif.

## Timeline:
- Semaine 1 : Planification et Configuration du Projet
- Semaine 2 : Collecte et Préparation des Données
- Semaine 3 : Détection des Joueurs avec YOLOv8
- Semaine 4 : Entraînement du Modèle YOLOv5 pour la Balle
- Semaine 5 : Suivi et Tracking des Objets
- Semaine 6 : Interpolation des Positions Manquantes
- Semaine 7 : Extraction des Points Clés du Terrain
- Semaine 8 : Intégration et Génération de Rapports Vidéo
- Semaine 9 : Test et Validation du Système
- Semaine 10 : Rapport final du projet et Présentation

## Conclusion:
Ce projet fournit un système d’analyse complet pour le tennis, combinant YOLO, PyTorch et techniques de tracking. Il permet une analyse approfondie des matchs grâce à une détection précise des objets, un suivi continu et une extraction pertinente des points clés du court.

Avec quelques ajustements, ce projet peut être utilisé non seulement dans le tennis mais aussi dans d’autres sports ou domaines nécessitant suivi et analyse d’objets en temps réel.