**Identification des étudiants:**

| Pseudonyme GitHub | Nom      | Prénom | Rôle       |
|-------------------|----------|--------|------------|
| @rdelplanque      | Delplanque | Raphael | Étudiant 2 |
| @Lenoxct          | Castel--gicquel      | Lenny | Étudiant 3 |
| @ConstantAKT          | Alankpokinto      | Constant | Étudiant 1 |


**Présentation du projet**\
Le projet consiste à réaliser un site web vitrine pour une association étudiante. 
L'association veut présenter: 
- ses activités et évenements à venir
- pouvoir s'inscrire.


**Fonctionnalités**
| Fonctionnalité | Fichier | Responsable | Contenu |
|---|---|---|---|
| A — Présentation et navigation | `index.html`, `style.css` | Étudiant 1 | En-tête, logo, menu, accueil, présentation et valeurs de l'association |
| B — Catalogue d'événements | `catalogue.html` | Étudiant 2 | 4 événements (titre, date, lieu, description) avec lien vers l'inscription |
| C — Inscription | `inscription.html` | Étudiant 3 | Formulaire (nom, prénom, classe, ville, e-mail, choix d'événement), sans backend |


**Étapes du développement**
1. Création du dépôt, des branches `main` et `develop`, et protection des branches.
2. Planification : Issues détaillées avec critères de réalisation, GitHub Project (Kanban + Roadmap).
3. Développement des fonctionnalités A, B et C sur des branches `feature/*`, intégrées par PR avec revue.
4. Améliorations parallèles (identité visuelle et mobile), avec un conflit volontaire et sa résolution.
5. Correction des cartes d'événements sur mobile (`bugfix/`).
6. Release `v1.0`.
7. Hotfix `v1.0.1` après l'incident de production.

**Workflow**
- `main` : versions publiées (tags `v1.0`, `v1.0.1`).
- `develop` : intégration des développements en cours.
- `feature/*` : une branche par fonctionnalité ou amélioration, créée depuis `develop`.
- `release/*` : préparation d'une version (vérifications uniquement), fusionnée dans `main` puis dans `develop`.
- `hotfix/*` : correction urgente créée depuis `main`, fusionnée dans `main` puis dans `develop`.

**Conflit Git et résolution**\
Origine: Deux améliorations ont été développées en parallèle depuis `develop` :
- `feature/visual-identity` a modifié les variables de couleurs, la police (Poppins) et le style des liens de navigation (majuscules, espacement, liens arrondis, survol coloré) ;
- `feature/mobile-layout` a modifié les mêmes blocs `.main-nav a` et `body` pour la mobilité : zone de clic plus grande, taille de police, interligne, retour à la ligne des mots longs.
Une fois la première PR mergée, la seconde a été signalée en conflit sur ces lignes communes de `style.css`, que Git ne pouvait pas fusionner automatiquement.
Le conflit a été résolu en local


**Difficultés rencontrées** 
- Harmonisation de la navigation et du style entre les pages développées séparément.
- Provoquer un vrai conflit, puis le résoudre sans perdre aucune des deux améliorations.
- Respect du temps imparti pour l'ensemble du workflow (release, hotfix, reports dans `develop`).

**Version publiées**\
'V1.0' : Fonctionnalités A, B, C, identité visuelle, adaptation mobile, correction des cartes et responsivité\
'V1.0.1' : Correction du lien de navigation vers les événements

**Question:**
1. Quel est l’intérêt de séparer développements en cours et versions stables ? \
Par Delplanque Raphael:\
Main ne doit contenir que du code validé et livrable. La branch develop contient le travail en cours.
Donc nous pouvons continuer de developper sans risque de déterriorer la version actuellement en production.

2. Pourquoi imposer une revue de code avant intégration ? \
Par Delplanque Raphael:\
La revue permet de détecter des erreurs ou des incohérences qui touchent les branches principales.

3. Quelles situations provoquent un conflit Git et pourquoi sa résolution n’est-elle pas toujours 
automatique ? \
Par Delplanque Raphael:\
Un conflit Git survient lorsque deux branches modifient les même lignes d'un fichier.
Sa résolution n'est donc pas automatique dans ce cas car Git ne sait pas quelle version conserver.


4. Quelle différence entre correction classique et correction urgente de production ? \
Par Castel-gicquel Lenny:\
La correction urgent part directement de la branch "main" pour corriger la version de production et se nomme "hotfix".
La correction classique par de la branch "develop" et est livré dans une version ultérieure, se nomme "fix".

5. Pourquoi répercuter une correction de production dans les développements en cours ? \
Par Castel-gicquel Lenny:\
Parceque le hotfix par du main et donc nous corrigeons le main. Or le developpement en cours est dans develop, donc les developpeurs travaillent sur une version différentes de la version de production. Nous devons donc répercuter la correction dans la branch "develop".

6. Quel est le rôle d’une branche de release ? \
Par Castel-gicquel Lenny:\
La branche release fige tout un ensemble de fonctionnalités pour préparer une version et la fusionner dans la branche main.
L'équipe de production peut continuer de travailler sur la branche "develop".


7. Comment GitHub Projects et les Issues facilitent-ils organisation et traçabilité ? \
Par constant alankpokinto:\
Une issue décrit une tache avec un responsable et les critères de réalisation. Le Project permet de suivre les avancée de ces taches.



8. Comment retrouver l’origine d’une modification dans l’historique GitHub ? \
Par constant alankpokinto:\
La modification peut se retrouver dans le commit ou par un git log.

