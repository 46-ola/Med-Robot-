# Med-Robot-
Conception d'un robot utilisable en médecine pour la chirurgie médicale en médecine pour la précision des gestes dans les parties complexes de l'organisme humain comme le cerveau et le cœur.
Un bras chirurgical qui filtre le tremblement de la main et réduit l'amplitude des gestes, pour des opérations plus précises et plus accessibles.
🔗 Démo en ligne : https://46-ola.github.io/med-robot/
Précision : ce dépôt contient une simulation logicielle du principe de fonctionnement. Il ne s'agit pas d'un prototype physique.
Contexte
L'accès à la chirurgie spécialisée reste limité au Bénin et dans de nombreux pays africains : peu de chirurgiens, équipements coûteux, patients éloignés des centres de soins. Med Robot explore une assistance robotisée qui rend le geste chirurgical plus précis et plus sûr.
Ce que montre la simulation
La page index.html simule une chaîne de téléopération :
Main du chirurgien (cadre de gauche) : le geste est suivi à la souris ou au doigt, avec un tremblement synthétique ajouté (environ 8 à 12 Hz).
Champ opératoire (cadre de droite) : l'instrument reproduit le geste après filtrage et réduction d'échelle.
Point pivot (trocart) : le tube de l'instrument passe toujours par un point d'incision fixe, comme en cœlioscopie.
Deux paramètres sont réglables : la réduction d'échelle (de 1:1 à 1:6) et la force du filtre.
Principe mathématique
Réduction d'échelle de la position de la pointe, avec un facteur k :
où c est le centre du champ opératoire et x la position de la main.
Filtre passe-bas du premier ordre, avec 0 < alpha is less than or equal to 1 :
Plus alpha est petit, plus le tremblement est atténué, au prix d'un léger retard.
Utilisation
Ouvrir la page de démonstration (lien ci-dessus), ou le fichier index.html dans un navigateur.
Déplacer la main dans le cadre de gauche. Sans interaction, un geste automatique est joué.
Régler l'échelle et le filtre avec les deux curseurs.
Aucune installation ni dépendance : un seul fichier HTML, CSS et JavaScript.
Technologies
HTML, CSS, JavaScript (canvas).
Limites
Simulation en 2D, sans modèle dynamique du bras ni retour de force.
Le tremblement est synthétique, pas mesuré sur un chirurgien.
Aucune validation clinique.
Pistes de développement
Modèle mécanique du bras (SolidWorks) et cinématique inverse.
Simulation du contrôle sous MATLAB.
Suivi de l'instrument par vision par ordinateur (OpenCV).
Capteurs et actionneurs sur Arduino pour un premier prototype.
Suivi des interventions et des données de santé avec Salesforce.
Auteur
Projet réalisé par 46-ola dans le cadre du Salesforce Hackathon PFE 2027.
