**Identification des étudiants:**

| Pseudonyme GitHub | Nom      | Prénom | Rôle       |
|-------------------|----------|--------|------------|
| @rdelplanque      | Delplanque | Prénom | Étudiant 2 |
| @pseudo1          | Nom      | Prénom | Étudiant 1 |
| @pseudo3          | Nom      | Prénom | Étudiant 3 |

Question:
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
Par:
La correction urgent part directement de la branch "main" pour corriger la version de production et se nomme "hotfix".
La correction classique par de la branch "develop" et est livré dans une version ultérieure, se nomme "bugfix".

6. Pourquoi répercuter une correction de production dans les développements en cours ? \
Par:
Parceque le hotfix par du main et donc nous corrigeons le main. Or le developpement en cours est dans develop, donc les developpeurs travaillent sur une version différentes de la version de production. Nous devons donc répercuter la correction dans la branch "develop".

8. Quel est le rôle d’une branche de release ? \


9. Comment GitHub Projects et les Issues facilitent-ils organisation et traçabilité ? \



10. Comment retrouver l’origine d’une modification dans l’historique GitHub ? \


