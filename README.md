# Rapport Technique : ENT DE L’UNVERSITE DE CORSE

## 1. Objectif du Projet
L'objectif était de développer un site web statique composé de trois pages interconnectées, reproduisant fidèlement l'expérience utilisateur du portail universitaire.

## 2. Architecture des Fichiers
La structure du projet est organisée autour de trois fichiers HTML principaux et un fichier JavaScript utilitaire :
* **index.html** : Page d'authentification (Landing page).
* **cours.html** : Tableau de bord principal (Liste des cours).
* **dev_web.html** : Page de détail d'un cours spécifique.
* **heure.js** : Script global pour l'affichage de l'heure en temps réel.

## 3. Analyse Technique et Choix de Développement

### A. Structure et Mise en Page (HTML5 & Tailwind CSS)
Le projet utilise le framework Tailwind CSS via CDN pour un prototypage rapide et un code CSS minimaliste.
* L'utilisation de Flexbox (flex flex-col justify-center items-center) assure un centrage vertical et horizontal harmonieux du contenu principal.

### B. Interactivité (JavaScript)
Un script léger, heure.js, a été implémenté pour dynamiser l'interface.
* **Fonctionnement** : il récupère l'heure système via l'objet Date() et met à jour le document.getElementById('live-clock') chaque seconde via setInterval.
* **Intégration** : Ce script est appelé en fin de sur les pages connectées pour afficher l'heure à côté du titre du cours.

## 4. Parcours Utilisateur
Le site statique propose une navigation fluide et fonctionnelle à travers trois étapes clés :

* **Étape 1 : Authentification (index.html)**
  L'utilisateur arrive sur une interface imitant le CAS (Central Authentication Service).
  * **Interface** : Formulaire avec champs "Identifiant" et "Mot de Passe"..
  * **Action** : Le bouton "SE CONNECTER" redirige l'utilisateur vers le tableau de bord (cours.html).

* **Étape 2 : Tableau de Bord (cours.html)**
  Une fois connecté, l'étudiant accède à son espace personnel.
  * **Action** : Le module "3LSTI41-DEVELOPPEMENT-WEB" dispose d'un bouton "ENTRER" actif qui mène vers la page de cours détaillée (dev_web.html).

* **Étape 3 : Contenu du Cours (dev_web.html)**
  * **Fonctionnalités Visuelles** :
    * Section "Notifications" simulant des messages non lus.
    * Section "Annonces".
  * **Navigation Retour** : Des liens permettent de revenir à "Mes cours en ligne" (cours.html).

## 5. Conclusion
Le rendu final est un site statique cohérent, esthétique et fonctionnel. Il respecte la demande de trois pages HTML liées, intègre du JavaScript pour l'affichage dynamique de l'heure, et utilise Tailwind CSS pour garantir un design moderne et responsive conforme à l'identité visuelle de l'Université de Corse.