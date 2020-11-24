# MasterClass GIT
---
![](https://miro.medium.com/max/380/1*OvMsmQs0Rzs_ScuiTsuWjw.png)


## What is [Git](https://git-scm.com/) 

__Git__ est un système de _controle de versionning_.
Cela permet aux développeurs de garder une trace de ce qui a été fait et de revenir à une phase précédente s’ils décident de revenir sur certains des changements qu’ils ont apportés.

__Git__ est un projet open source, il a été développé en 2005 par __Linus Torvalds__, auteur du noyau __Linux__.

## La différence entre [Git](https://git-scm.com/) et [GitHub](https://github.com/)

__GitHub__ facilite la collaboration en utilisant __git__. C’est une plateforme qui peut contenir des dépôts de code dans un stockage dans le cloud afin que plusieurs développeurs puissent travailler sur un même projet et voir les modifications des autres en temps réel.
Il comprend également _des fonctions d’organisation et de gestion de projets_. Vous pouvez attribuer des tâches à des individus ou à des groupes, définir les autorisations et les rôles des collaborateurs et utiliser la modération des commentaires pour que chacun reste concentré sur sa tâche.

En outre, les dépôts GitHub sont accessibles au public. Les développeurs du monde entier peuvent interagir et contribuer au code des autres afin de le modifier ou de l’améliorer, ce que l’on appelle le « codage social ». D’une certaine manière, cela fait de GitHub un site de mise en réseau pour les professionnels du web.

Pour résumer la différence entre __Git__ et __GitHub__ :

__Git__ est un logiciel qui permet aux développeurs de sauvegarder leur projet de manière local, il est plus adapté à un usage individuel.
__GitHub est une plateforme web qui intègre les fonctionnalités de contrôle de version de git__ afin de pouvoir les utiliser en collaboration. Il comprend également des fonctions de gestion de projets et d’équipes, ainsi que des possibilités de mise en réseau et de codage social.


## Basic Command 


__git config__
 ```
Command pour configurer les préférences de l'utilisateur.
exemple:
git config --global user.email student42@gmail.com
```

__git add__
```
La commande git add peut être utilisée pour ajouter des fichiers à l’index
exemple : git add exemple.txt 
ajoute le fichier nommé exemple.txt dans le répertoire local de l’index:
```
 
__git rm --cached__
```
git rm --cached <fichier>
Enlever un fichier de l'index du répertoir
```

__git commit__
```
La commande git commit permet de valider les modifications apportées.
```

__git status__
```
La commande git statut va vous permettre d'avoir un aperçu de l'état de votre dépôt. 
Notamment la liste des fichiers modifiés ainsi que les fichiers qui doivent encore être ajoutés ou validés.

Voici une option pratique -u (--untracked-files[=<mode>]):
git status -u
```



__git push__
```
Un simple push envoie les modifications locales apportées à la branche principale 
```

__git pull__
```
Pour fusionner toutes les modifications présentes sur le dépôt distant dans le répertoire de travail local
```

__git branch__
```
La commande git branch peut être utilisée pour répertorier, créer ou supprimer des branches. Pour répertorier toutes les branches présentes dans le dépôt

Exemple:
git branch dev
Créer une branche dev.
```

__git checkout__
```
La commande git checkout peut être utilisée pour créer des branches ou pour basculer entre elles.

Exemple:
git checkout dev
Ce déplace sur la branche dev
```

__git push --set-upstream origin name__
```
Push une branche sur le depot en ligne
```

__git fetch__
```
Git fetch permet à un utilisateur d’extraire tous les fichiers du dépôt distant qui ne sont pas actuellement dans le répertoire de travail local.
```

__git merge__
```
La commande git merge est utilisée pour fusionner une branche dans la branche active.
```

__git diff (--base name)__
```
La commande git diff permet de lister les conflits. Pour visualiser les conflits d’un fichier
```

__git log__
```
L’exécution de la commande git log génère le log d’une branche.
```

__git reset__
```
Pour réinitialiser l’index et le répertoire de travail à l’état du dernier commit, la commande git reset est utilisée :

git reset --soft HEAD~1
git reset --hard HEAD
```

## Branch 

Les branches permettent une meilleur gestion des versions, travailler plus facilement à plusieurs.
Travailler en équipe, c’est bien mais chacun a besoin de son propre espace. Lorsqu’on développe une nouvelle fonctionnalité, c’est essentiel de s’isoler des modifications non-liées à la fonctionnalité sur laquelle on travaille. Pourquoi ? Parce que lorsqu’on développe, notre code peut engendrer des régressions. Et si l’on travaille tous sur la même branche, on aura du mal à trouver l’origine de la régression. Est-ce suite à notre développement, ou à celui d’un collègue ?
Ceci peut nous faire perdre beaucoup de temps.

Si votre équipe ne suis pas une méthodologie de travail pré-déterminée, on se retrouve rapidement avec des conflits à chaque commit/merge ou presque, des pertes de données et un historique fouillis.

Lorsque l'on commence un nouveau projet on se retrouve sur un branch `master` ou `main`. Cette branche servira à la version __production__ de notre projet. On va donc souvent commencer par créer une nouvelle branche servant au développement.

`La branche master` est la branche production. Il est donc logique que l'on ne puisse y `push` nos modifications directement. Sur cette branche ce trouve un coode stable, testé et validé.

`La branche develop` centralise toutes les nouvelles fonctionnalités qui seront livrées dans la prochaine version. Ici il va falloir se forcer à ne pas y faire de modifications directement. Code de la prochaine version de l’application. Une fois que le développement d’une fonctionnalité (feature) est fini, le code est fusionné sur cette branche.

`Les branches features` chaque branche travaillera sur un aspect du projet (parsing, système, interface, algorimth ....), code en cours de développement qui implémente une fonctionnalité à embarquer dans la prochaine version de l’application.

Qu’est-ce que le merge d’une branche feature veut dire ? Lorsqu’on `merge une branche feature` sur la branche `develop`, on indique que la fonctionnalité est terminée et prête pour rejoindre la prochaine version de l'application. Qu’est-ce que « prête » veut dire ? Cela dépend de la définition de terminé accordé sur chaque projet.


_Voici un exemple réaliser par mes soins, d'une bonne utilisations des branches (selon mon point de vue) :_
![](https://zupimages.net/up/20/46/rftq.png)


### command
```bash
$ git branch # Voir la liste des branches
$ git branch [nom_branche] # Créer une branche
$ git branch -v # Voir la liste des branches et leur dernier commit
$ git branch --merged # Voir les branches mergées
$ git branch --no-merged # Voir les branches non mergées
$ git branch -a # Voir toutes les branches
$ git branch -d nom_branche # Supprime une branche mergée
$ git branch -D nom_branche # Supprime une branche
```

## Submodule

Il arrive souvent lorsque vous travaillez sur un __projet__ que vous deviez utiliser _un autre projet comme dépendance_. Cela peut être une bibliothèque qui est développée par une autre équipe ou que vous développez séparément pour l’utiliser dans plusieurs projets parents. Ce scénario provoque un problème habituel : vous voulez être capable de gérer deux projets séparés tout en utilisant l’un dans l’autre.


__Voici un exemple__ : Vous voulez utiliser votre __libft__ dans votre projet __printf__.
Vous pouvez copier le code source dans votre arborescence de printf, le problème d’inclure le code de votre libft dans votre projet, imaginons vous mettez à jour votre libft, car vous venez de coder une fonction très utile que vous aimeriez réutiliser dans plusieurs de vos projets en C. Il faudra donc copier cette nouvelle fonction dans tout vos projets qui utilise la __libft__.

__Git__ gère ce problème avec les __sous-modules__. Les sous-modules vous permettent de gérer un dépôt Git comme un sous-répertoire d’un autre dépôt Git. Cela vous laisse la possibilité de cloner un dépôt dans votre projet et de garder isolés les _commits_ de ce dépôt.

### Démarrer un sous-module

Commençons par ajouter le dépôt d’un projet __Git__ existant comme sous-module d’un dépôt sur lequel nous travaillons. Pour ajouter un nouveau sous-module, nous utilisons la commande `git submodule add` avec l’URL du projet que nous souhaitons suivre. Dans cette exemple, nous ajoutons notre libft.

```console
git submodule add https://github.com/42students/libft
Clonage dans 'libft'...
remote: Counting objects: 11, done.
remote: Compressing objects: 100% (10/10), done.
remote: Total 11 (delta 0), reused 11 (delta 0)
Dépaquetage des objets: 100% (11/11), fait.
Vérification de la connectivité... fait.
```

Si vous lancez `git status` à ce moment, vous trouverez un nouveau fichier  :

```console
$ git status
Sur la branche master
Votre branche est à jour avec 'origin/master'.

Modifications qui seront validées :
  (utilisez "git reset <fichier>..." pour désindexer)

	nouveau fichier :   .gitmodules
	nouveau fichier :   libft
```

`.gitmodules` vient d’apparaître. C’est le fichier de configuration qui stocke la liaison entre l’URL du projet et le sous-répertoire local dans lequel vous l’avez `pull`.


### Cloner un projet avec des sous-modules

Comment cloner un projet contenant des sous-modules. Quand vous récupérez un tel projet, vous obtenez les différents répertoires qui contiennent les sous-modules, mais encore aucun des fichiers :

```console
$ git clone https://github.com/42students/printf
Clonage dans 'printf'...
remote: Counting objects: 14, done.
remote: Compressing objects: 100% (13/13), done.
remote: Total 14 (delta 1), reused 13 (delta 0)
Dépaquetage des objets: 100% (14/14), fait.
Vérification de la connectivité... fait.
$ cd printf
$ ls -la
total 16
drwxr-xr-x   9 42student  staff  306 Sep 17 15:21 .
drwxr-xr-x   7 42student  staff  238 Sep 17 15:21 ..
drwxr-xr-x  13 42student  staff  442 Sep 17 15:21 .git
-rw-r--r--   1 42student  staff   92 Sep 17 15:21 .gitmodules
drwxr-xr-x   2 42student  staff   68 Sep 17 15:21 libft
-rw-r--r--   1 42student  staff  756 Sep 17 15:21 Makefile
drwxr-xr-x   3 42student  staff  102 Sep 17 15:21 includes
drwxr-xr-x   4 42student  staff  136 Sep 17 15:21 src
$ cd libft/
$ ls
$
```

Le répertoire `libft` est présent mais vide. Vous devez exécuter deux commandes : `git submodule init` pour initialiser votre fichier local de configuration, et `git submodule update` pour `pull` toutes les données de ce projet et récupérer le _commit_ approprié tel que listé dans votre super-projet :

```console
$ git submodule init
Sous-module 'libft' (https://github.com/42students/libft) enregistré pour le chemin 'libft'
$ git submodule update
Clonage dans 'libft'...
remote: Counting objects: 11, done.
remote: Compressing objects: 100% (10/10), done.
remote: Total 11 (delta 0), reused 11 (delta 0)
Unpacking objects: 100% (11/11), done.
Checking connectivity... done.
Submodule path 'libft': checked out 'c3f01dc8862123d317dd46284b05b6892c7b29bc'
```

Votre répertoire `libft` est maintenant dans l’état exact dans lequel il était la dernière fois que vous avez validé.

Il existe une autre manière plus simple d’arriver au même résultat. Si vous passez l’option `--recurse-submodules` à la commande `git clone`, celle-ci initialisera et mettra à jour automatiquement chaque sous-module du dépôt.

```console
$ git clone --recurse-submodules https://github.com/42students/printf
```

___Vous voulez en savoir plus :___
- [Docs EN](https://git-scm.com/book/en/v2/Git-Tools-Submodules) 
- [Docs FR](https://git-scm.com/book/fr/v2/Utilitaires-Git-Sous-modules)

## CI (continue integration)

[En cours de construction]

Dans n’importe quel projet, il est recommandé d’avoir une plateforme d’intégration continue. Ceci permet d’intégrer automatiquement les modifications réalisées sur le code et de notifier les développeurs lorsqu’un test ne passe plus. 

![](https://user.oc-static.com/upload/2019/07/03/15621470017041_16.jpg)

## Étiquetez votre projet avec des badges

[En cours de construction]

Les badges permettent de garder le projet à jour et indiquent une certaine qualité. Les badges peuvent être utilisés pour tout un tas de choses.

## GitHunt


[Githunt](https://chrome.google.com/webstore/detail/githunt/khpcnaokfebphakjgdgpinmglconplhp?hl=en) est une extension pour Chrome qui affiche les dépôts Github qui font le buzz en ce moment.
Vous pouvez aussi retrouver une version web (https://kamranahmed.info/githunt/)

## Source 

[Tips Git EN](https://git-scm.com/book/en/v2)

[Tips Git FR](https://git-scm.com/book/fr/v2)


## Contributing, Question or suggestions ?
__42Slack :__ __*jereligi*__

__42Intra :__ [jereligi](https://profile.intra.42.fr/users/jereligi)

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
Please make sure to update tests as appropriate.


Thanks for reading this read me, advice or corrections are welcome
