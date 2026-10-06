# Projet TurtleBot3 : Modification 4 Roues et Contrôle en Essaim (Swarm Robotics)

## 🎯 Contexte et Objectif
Ce dépôt présente les travaux **en cours de réalisation** dans le cadre de mon projet académique de **3ème année**. L'objectif final de ce projet est de concevoir et piloter un essaim de 4 robots mobiles capables d'évoluer en formation synchronisée de manière autonome. 

Le projet s'articule autour de deux défis techniques majeurs :
1. **Une refonte mécanique :** Transformation de l'architecture matérielle standard du robot (passage de 2 roues différentielles à 4 roues motrices).
2. **Une conception logicielle multi-agents :** Gestion de la communication réseau, des cinématiques de déplacement et des permutations de position au sein de la flotte.

## 🛠️ Environnement Technique
* **Matériel :** Châssis TurtleBot3 (modèle Burger), microcontrôleur OpenCR, Raspberry Pi.
* **Logiciel :** Système d'exploitation Ubuntu 22.04 LTS.
* **Middleware :** ROS 2 (Robot Operating System, version Humble).
* **Développement :** Programmation orientée objet en Python 3.

## 🚀 État d'avancement (Projet en cours)
Le projet suit une méthode de développement itérative. Avant de déployer l'essaim complet, le travail actuel se concentre sur la maîtrise et la modification d'un robot prototype unique. 

Ce dépôt contient les premiers modules déjà développés et validés sur le matériel physique :

* **Module de Téléopération Dynamique :** Développement d'un nœud ROS 2 permettant le pilotage manuel sécurisé du robot. Ce module gère les interruptions clavier et applique un plafonnement dynamique des vélocités linéaires et angulaires pour protéger les moteurs.
* **Module de Contrôle Autonome (Boucle ouverte) :** Scripts permettant au robot d'exécuter des trajectoires géométriques complexes (cercles, carrés) de manière autonome. Le système calcule en temps réel les vitesses nécessaires en fonction des paramètres dimensionnels (rayons, longueurs) fournis par l'utilisateur.
* **Isolation Réseau :** Configuration des variables d'environnement (`ROS_DOMAIN_ID`) pour isoler les communications des robots, étape préparatoire indispensable avant l'intégration des *namespaces* pour la flotte complète.

## 📅 Prochaines Étapes
* Modélisation 3D et intégration physique des nouvelles roues sur les châssis.
* Adaptation du modèle cinématique ROS 2 pour la prise en charge de la propulsion à 4 roues.
* Déploiement de l'algorithme de contrôle en essaim sur l'ensemble de la flotte.
