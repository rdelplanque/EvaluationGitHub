**Identification des étudiants:**

| Pseudonyme GitHub | Nom      | Prénom | Rôle       |
|-------------------|----------|--------|------------|
| @rdelplanque      | Delplanque | Raphael | Étudiant 2 |
| @Lenoxct          | Castel--gicquel      | Lenny | Étudiant 3 |
| @ConstantAKT          | Alankpokinto      | Constant | Étudiant 1 |


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


**Question:**
1. Quel est l’intérêt de séparer développements en cours et versions stables ? \
Par Delplanque Raphael:
Main ne doit contenir que du code validé et livrable. La branch develop contient le travail en cours.
Donc nous pouvons continuer de developper sans risque de déterriorer la version actuellement en production.

2. Pourquoi imposer une revue de code avant intégration ? \
Par Delplanque Raphael:
La revue permet de détecter des erreurs ou des incohérences qui touchent les branches principales.

3. Quelles situations provoquent un conflit Git et pourquoi sa résolution n’est-elle pas toujours 
automatique ? \
Par Delplanque Raphael:
Un conflit Git survient lorsque deux branches modifient les même lignes d'un fichier.
Sa résolution n'est donc pas automatique dans ce cas car Git ne sait pas quelle version conserver.


4. Quelle différence entre correction classique et correction urgente de production ? \
Par Castel-gicquel Lenny:
La correction urgent part directement de la branch "main" pour corriger la version de production et se nomme "hotfix".
La correction classique par de la branch "develop" et est livré dans une version ultérieure, se nomme "bugfix".

5. Pourquoi répercuter une correction de production dans les développements en cours ? \
Par Castel-gicquel Lenny:
Parceque le hotfix par du main et donc nous corrigeons le main. Or le developpement en cours est dans develop, donc les developpeurs travaillent sur une version différentes de la version de production. Nous devons donc répercuter la correction dans la branch "develop".

6. Quel est le rôle d’une branche de release ? \
Par Castel-gicquel Lenny:
La branche release fige tout un ensemble de fonctionnalités pour préparer une version et la fusionner dans la branche main.
L'équipe de production peut continuer de travailler sur la branche "develop".


7. Comment GitHub Projects et les Issues facilitent-ils organisation et traçabilité ? \
Par constant alankpokinto:
Une issue décrit une tache avec un responsable et les critères de réalisation. Le Project permet de suivre les avancée de ces taches.



8. Comment retrouver l’origine d’une modification dans l’historique GitHub ? \
Par constant alankpokinto:
La modification peut se retrouver dans le commit ou par un git log.

