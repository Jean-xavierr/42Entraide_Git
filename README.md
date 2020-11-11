# MasterClass GIT
------
![](https://miro.medium.com/max/380/1*OvMsmQs0Rzs_ScuiTsuWjw.png)


## What is [Git](https://git-scm.com/) 
---
__Git__ est un système de _controle de versionning_.
Cela permet aux développeurs de garder une trace de ce qui a été fait et de revenir à une phase précédente s’ils décident de revenir sur certains des changements qu’ils ont apportés.

__Git__ est un projet open source, il a éteé développé en 2005 par __Linus Torvalds__, auteur du noyau __Linux__.

## La différence entre [Git](https://git-scm.com/) et [GitHub](https://github.com/)
---
__GitHub__ facilite la collaboration en utilisant __git__. C’est une plateforme qui peut contenir des dépôts de code dans un stockage dans le cloud afin que plusieurs développeurs puissent travailler sur un même projet et voir les modifications des autres en temps réel.
Il comprend également _des fonctions d’organisation et de gestion de projets_. Vous pouvez attribuer des tâches à des individus ou à des groupes, définir les autorisations et les rôles des collaborateurs et utiliser la modération des commentaires pour que chacun reste concentré sur sa tâche.

En outre, les dépôts GitHub sont accessibles au public. Les développeurs du monde entier peuvent interagir et contribuer au code des autres afin de le modifier ou de l’améliorer, ce que l’on appelle le « codage social ». D’une certaine manière, cela fait de GitHub un site de mise en réseau pour les professionnels du web.

Pour résumer la différence entre __Git__ et __GitHub__ :

__Git__ est un logiciel qui permet aux développeurs de sauvegarder leur projet de manière local, il est plus adapté à un usage individuel.
__GitHub est une plateforme web qui intègre les fonctionnalités de contrôle de version de git__ afin de pouvoir les utiliser en collaboration. Il comprend également des fonctions de gestion de projets et d’équipes, ainsi que des possibilités de mise en réseau et de codage social.


### Command (Work in progress)
----

__git config__
Command pour configurer les préférences de l'utilisateur.
git config --global user.email student42@gmail.com

__git add__
La commande git add peut être utilisée pour ajouter des fichiers à l’index
exemple : git add exemple.txt 
ajoute le fichier nommé exemple.txt dans le répertoire local de l’index:
 
__git restore__
git restore --staged <fichier>
Enlever un fichier de l'index du répertoir

__git commit__
La commande git commit permet de valider les modifications apportées.

__git status__
La commande git status affiche la liste des fichiers modifiés ainsi que les fichiers qui doivent encore être ajoutés ou validés.

__git push__
Un simple push envoie les modifications locales apportées à la branche principale 

__git pull__
Pour fusionner toutes les modifications présentes sur le dépôt distant dans le répertoire de travail local

__git branch name__
La commande git branch peut être utilisée pour répertorier, créer ou supprimer des branches. Pour répertorier toutes les branches présentes dans le dépôt

__git checkout name__
La commande git checkout peut être utilisée pour créer des branches ou pour basculer entre elles.

__git push --set-upstream origin name__
Push une branche sur le depot en ligne

__git fetch__
Git fetch permet à un utilisateur d’extraire tous les fichiers du dépôt distant qui ne sont pas actuellement dans le répertoire de travail local.

__git merge__
La commande git merge est utilisée pour fusionner une branche dans la branche active.

__git diff (--base name)__
La commande git diff permet de lister les conflits. Pour visualiser les conflits d’un fichier

__git log __
L’ exécution de la commande git log génère le log d’une branche. 

__git reset__
Pour réinitialiser l’index et le répertoire de travail à l’état du dernier commit, la commande git reset est utilisée :

__git reset --hard HEAD__
__git reset --soft HEAD~1__


## GitHunt
---

[Githunt](https://chrome.google.com/webstore/detail/githunt/khpcnaokfebphakjgdgpinmglconplhp?hl=en) est une extension pour Chrome qui affiche les dépôts Github qui font le buzz en ce moment.
Vous pouvez aussi retrouver une version web (https://kamranahmed.info/githunt/)

## Source
---
