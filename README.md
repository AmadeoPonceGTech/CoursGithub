# CoursGithub 

## 1. Versioning

Le versioning est un système permettant de suivre l'évolution d'un projet au cours du temps en conservant un ***historique des modifications*** . <br>

Chaque étape importante peut être enregistrée, ce qui permet de savoir quelles modifications ont été effectuées, quand elles l'ont été et, selon le système utilisé, par qui. <br>
Cela facilite également le travail en équipe, puisque plusieurs personnes peuvent travailler sur un même projet tout en conservant un historique commun et organisé. <br>
Avec un outil comme Git associé à une plateforme distante comme GitHub, on peut également partager le dépôt entre les membres de l'équipe, travailler avec différentes branches et revenir à un état antérieur du projet en cas de problème.<br>

Si une modification introduit un problème, l'historique permet d'identifier à quel moment le problème est apparu et de revenir à un état antérieur ou d'annuler les changements concernés.
## 2. Git / GitHub / GitHub Desktop

### Git 
Git est un logiciel de gestion de versions distribué permettant de suivre l'évolution d'un projet et de conserver son historique. <br>
Il fonctionne autour d'un dépôt (repository), qui contient les fichiers du projet ainsi que les informations nécessaires au suivi de leurs modifications. <br>
Git permet notamment d'enregistrer des modifications, de consulter et comparer différentes versions du projet, de travailler avec des branches et de revenir sur certains changements en cas de problème. <br>
Il peut fonctionner entièrement en local, sans dépendre de GitHub ni d'une connexion Internet, notamment grâce à des commandes exécutées dans un terminal comme Git Bash. <br>
Les différentes opérations de Git peuvent également être réalisées à travers des interfaces graphiques, comme GitHub Desktop ou certaines fonctionnalités des IDE.

### Git Bash

### GitHub

GitHub est une plateforme en ligne permettant notamment d'héberger des dépôts Git à distance et de faciliter leur partage et leur collaboration.<br>
Contrairement à Git, qui peut fonctionner entièrement en local, GitHub permet de conserver une copie distante du dépôt et de la rendre accessible depuis Internet. <br>
Cela apporte notamment un intérêt en cas de problème avec la machine locale : si le projet a été envoyé sur GitHub, il est possible de récupérer le dépôt sur une autre machine grâce à Git.

Il faut cependant bien distinguer le dépôt local du dépôt distant. <br>
Une fois qu'un dépôt GitHub a été cloné sur une machine, on possède également une copie locale du dépôt et de son historique.<br>
Il est donc possible de continuer à travailler avec Git sans connexion Internet : créer des ```commits```, créer des branches, effectuer des ```merges``` ou consulter l'historique restent possibles. <br>
En revanche, les opérations nécessitant une communication avec GitHub, comme le ```push```, le ```pull``` ou le ```fetch```, nécessitent une connexion Internet. <br>
Les modifications réalisées hors ligne restent donc uniquement sur le dépôt local jusqu'à ce qu'elles soient synchronisées avec le dépôt distant. <br>

GitHub ajoute également de nombreuses fonctionnalités autour de Git afin de faciliter le travail en équipe. <br>
Il est notamment possible d'ajouter des ```collaborateurs```, de gérer leurs permissions, de rendre un dépôt public ou privé et d'utiliser des outils comme les ```Pull Requests```, les Issues ou les règles de protection des branches. <br>
Ces fonctionnalités permettent d'organiser le travail d'une équipe autour d'un même dépôt.

Enfin, GitHub peut également servir à présenter des projets publiquement. <br>
Un profil GitHub peut regrouper différents dépôts et donc servir de vitrine pour des projets personnels ou professionnels. <br>
GitHub propose également GitHub Pages, qui permet de publier certains sites web directement depuis GitHub et peut notamment être utilisé pour créer un portfolio en ligne.

https://GITHUB_NAME.github.io/

### GitHub Desktop

GitHub Desktop est une application graphique permettant d'utiliser Git sans passer directement par la ligne de commande. 
Elle permet de visualiser les différentes opérations effectuées sur un dépôt et de simplifier la gestion des dépôts locaux ainsi que leur synchronisation avec des dépôts distants comme ceux hébergés sur GitHub. 
Après avoir installé l'application et connecté son compte GitHub, il est notamment possible d'accéder aux dépôts auxquels on a accès et de gérer plus facilement ses projets.

GitHub Desktop permet notamment de créer un nouveau dépôt, d'ajouter un projet existant, ou de cloner un dépôt existant depuis GitHub. 
Lorsqu'un projet existe déjà sur l'ordinateur mais n'est pas encore un dépôt Git, GitHub Desktop peut également permettre de l'ajouter puis de le publier sur GitHub.

L'application fournit ensuite une interface visuelle pour effectuer de nombreuses opérations Git.
On peut notamment créer et changer de branche, effectuer des commits, consulter l'historique, comparer les modifications, effectuer des fetch, des pull et des push, ou encore participer à la création de Pull Requests.

Pour les commits, GitHub Desktop permet de renseigner un résumé de la modification ainsi qu'une description plus détaillée. Le résumé doit rester court et permettre de comprendre rapidement ce que le commit apporte. La description peut ensuite préciser davantage le contenu ou le contexte de la modification. La convention utilisée pour rédiger ces messages dépendra de l'organisation du projet et sera détaillée dans la partie consacrée à la nomenclature.

GitHub Desktop facilite également la gestion des conflits. Lorsqu'un conflit survient, l'application peut indiquer les fichiers concernés et permettre d'accéder à leur résolution. Cependant, GitHub Desktop ne décide pas à la place du développeur quelle modification doit être conservée : il faut analyser le conflit et choisir ou combiner manuellement les modifications appropriées.

Il est donc important de comprendre que GitHub Desktop n'automatise pas la correction des erreurs. 
Il fournit une interface plus visuelle et des avertissements permettant de mieux comprendre certaines opérations, mais Git exécute toujours les actions demandées par l'utilisateur. Une mauvaise manipulation reste donc possible. Certaines opérations, comme le force push, peuvent notamment réécrire l'historique d'une branche et avoir des conséquences importantes pour les autres personnes travaillant sur le dépôt. Les branches protégées peuvent toutefois empêcher certaines opérations dangereuses selon la configuration du dépôt.

L'intérêt principal de GitHub Desktop est donc de rendre Git plus accessible visuellement, tout en permettant de réaliser une grande partie des opérations courantes sans connaître immédiatement toutes les commandes Git. Cependant, comprendre ce qui se passe réellement derrière les boutons reste important : GitHub Desktop est une interface pour Git, et non un système qui corrige automatiquement les erreurs du développeur.

## 3. Repository local / distant
Un repository, aussi appelé repo, est le dépôt qui contient notre projet ainsi que les informations nécessaires à Git pour suivre son historique et ses modifications. On peut donc le voir comme l'espace de travail et de stockage de notre projet dans lequel Git va suivre les différentes évolutions.

Dans notre cas, il faut distinguer deux repositories : le repository local et le repository distant.

Le repository local est le dépôt présent directement sur notre ordinateur. C'est celui avec lequel nous travaillons lorsque nous modifions nos fichiers et utilisons Git. Les opérations comme les commits, la création de branches ou les merges peuvent être réalisées localement, sans avoir besoin d'une connexion Internet. Lorsque nous utilisons Git Bash ou GitHub Desktop, nous travaillons donc principalement avec ce dépôt local.

Le repository distant, aussi appelé remote repository, est un dépôt hébergé sur une autre machine ou un serveur accessible à distance. Dans notre cas, il est hébergé sur GitHub. Il permet notamment de partager le projet avec les autres membres de l'équipe et de conserver une copie distante du repository.

Il est important de comprendre que le repository local et le repository distant ne sont pas automatiquement synchronisés. Une modification réalisée sur le dépôt local reste d'abord uniquement sur notre machine. Elle doit être envoyée vers le dépôt distant avec un push. À l'inverse, lorsqu'une autre personne effectue des modifications sur le dépôt distant, il faut récupérer ces modifications avec des opérations comme fetch et pull.

             REPOSITORY DISTANT
                  GitHub
                    ▲
                    │
                  PUSH
                    │
                    │
             REPOSITORY LOCAL
                Notre PC
                    │
             Modifications
                    │
                 COMMIT

Dans un fonctionnement d'équipe classique, le repository distant sur GitHub peut servir de référence commune pour l'équipe : chaque développeur travaille sur son propre repository local, puis synchronise son travail avec le repository distant. <br>
Cependant, il ne faut pas considérer cette organisation comme une règle absolue. Selon l'entreprise, l'équipe ou l'outil utilisé, l'organisation peut être différente. <br>
La « source de vérité » d'un projet dépend notamment du workflow choisi par l'équipe. <br>
Avec Git et GitHub, le dépôt distant est très souvent utilisé comme point de référence commun, mais Git permet également de travailler avec différents dépôts et différentes configurations.

## 4. Commit

Un commit est un enregistrement d'un ensemble de modifications dans l'historique d'un repository Git. Il permet de conserver un état du projet à un moment donné, avec les modifications qui ont été ajoutées à cet enregistrement.

Il ne faut cependant pas confondre un commit avec un simple Ctrl + S. Lorsque l'on sauvegarde un fichier avec Ctrl + S, on enregistre simplement son état actuel sur notre ordinateur. Avec un commit, on demande à Git d'enregistrer les modifications dans l'historique du repository. Le commit est donc une étape importante dans le suivi du projet.

Par exemple, imaginons que l'on ajoute une nouvelle fonction à notre projet. Une fois la modification terminée et vérifiée, on peut créer un commit :

Modification du code
↓
Vérification
↓
COMMIT
↓
Enregistrement dans
l'historique Git

Chaque commit possède notamment un message, qui permet de comprendre rapidement ce qui a été modifié. Dans GitHub Desktop, on peut renseigner un titre court ainsi qu'une description plus détaillée.

```Titre : Add weapon reload function ``` <br>
```Description : Add the reload logic and update the current magazine. ```

L'intérêt est de pouvoir construire progressivement un historique clair du développement :

             Modification du code
                    ↓
               Vérification
                    ↓
                  COMMIT
                    ↓
             Enregistrement dans
              l'historique Git
Cela permet ensuite de consulter l'historique, de comparer les différentes étapes du projet et, selon la situation, de revenir à un état antérieur ou d'annuler certaines modifications.

Il est généralement préférable de faire des commits correspondant à des modifications cohérentes et fonctionnelles, plutôt que d'attendre d'avoir réalisé énormément de changements différents avant d'en créer un. Par exemple, un commit qui ajoute une fonctionnalité précise est généralement plus facile à comprendre et à manipuler qu'un commit contenant plusieurs modifications sans rapport entre elles.

Enfin, un commit est local tant qu'il n'a pas été envoyé au repository distant. On peut donc créer plusieurs commits sur notre machine sans les envoyer immédiatement sur GitHub. C'est ensuite le push qui permet d'envoyer les commits locaux vers le repository distant.

À retenir

Un commit enregistre un ensemble de modifications dans l'historique Git et représente une étape du projet à un moment donné.

Et la distinction importante avec ce qu'on verra juste après :

        Modification
            ↓
          COMMIT
            ↓
        Commit enregistré dans le repo local
            ↓
          PUSH
            ↓
        Commit envoyé vers le repo distant

Donc commit ≠ push : le commit enregistre la modification dans Git localement, tandis que le push sert à synchroniser ces commits avec le repository distant.
## 5. Fetch / Pull / Push

Les commandes fetch, pull et push servent à synchroniser notre repository local avec le repository distant. Elles permettent donc de faire circuler les modifications entre notre machine et le dépôt distant.

### Fetch

fetch permet de récupérer les informations du repository distant afin de vérifier si de nouvelles modifications ou de nouveaux commits sont disponibles.

Il ne modifie pas directement notre branche de travail. Il permet simplement de mettre à jour les informations que Git possède sur le repository distant.

On peut donc le voir comme :

*« Est-ce qu'il y a du nouveau sur le repository distant ? »*

            Repository distant
                    ↓
                  FETCH
                    ↓
        Informations mises à jour
          dans le repository local

### Pull

pull permet de récupérer les nouvelles modifications du repository distant et de les intégrer à notre repository local.

Il est donc utilisé lorsqu'on veut réellement récupérer le travail effectué à distance.

On peut le voir comme :

*« Récupère les nouvelles modifications et applique-les à mon travail local. »*

            Repository distant
                    ↓
                   PULL
                    ↓
         Repository local mis à jour

### Push

push fait le chemin inverse du pull. Il permet d'envoyer vers le repository distant les commits présents dans notre repository local mais qui ne sont pas encore présents sur le distant.

Il est donc utilisé pour partager notre travail avec le repository distant.

On peut le voir comme :

*« Envoie mes commits locaux vers le repository distant. »*

            Repository local
                    ↓
                  PUSH
                    ↓
        Repository distant mis à jour

### *À retenir*

```FETCH → Vérifier / récupérer les informations du distant ```<br>
```PULL  → Récupérer et intégrer les modifications du distant``` <br>
```PUSH  → Envoyer nos commits vers le distant ```<br> 

## 6. Branches

Une branche, ou branch, est une ligne de développement séparée dans un repository. Elle permet de travailler sur des modifications sans modifier directement une autre branche.

Pour comprendre simplement le principe, on peut imaginer le projet comme une route principale. Cette route représente par exemple la branche principale du projet, souvent appelée main ou parfois master.

Selon l'organisation du projet, plusieurs niveaux de branches peuvent exister. Par exemple, main peut représenter une branche de développement principale, parfois appelée Main Dev, dans laquelle les différentes fonctionnalités sont regroupées et vérifiées avant d'être considérées comme suffisamment stables. Une autre branche, comme master, peut dans certains workflows représenter une version destinée à la production. L'organisation exacte dépend cependant des conventions de l'équipe.

À partir de ces branches, on peut créer des branches secondaires pour travailler sur des fonctionnalités ou des tâches précises. Chaque personne peut ainsi faire évoluer son travail indépendamment avant de le réintégrer dans une branche commune.

L'objectif principal des branches est donc de séparer les différentes lignes de développement et d'organiser le travail, notamment lorsque plusieurs personnes travaillent sur le même projet. Elles permettent également d'éviter de modifier directement une branche qui doit rester stable.

Une branche ne supprime cependant pas les conflits : si plusieurs branches modifient les mêmes parties d'un fichier de manière incompatible, un conflit peut apparaître lors de leur fusion.

### À retenir

```Une branche permet de créer une ligne de développement séparée afin de travailler sur une fonctionnalité ou une tâche sans modifier directement une autre branche. ```

## 7. Nomenclature des branches

La nomenclature correspond simplement aux règles utilisées pour nommer les différents éléments d'un projet. Pour les branches, certaines conventions sont très courantes, notamment pour permettre à toute l'équipe de comprendre rapidement le rôle d'une branche.

Pour la branche principale, vous rencontrerez très souvent les noms main ou master. Aujourd'hui, GitHub utilise main comme nom par défaut pour les nouveaux repositories, mais le nom peut être modifié selon les conventions du projet ou de l'équipe.

Pour les branches de travail, il n'existe pas une nomenclature universelle imposée par Git. On retrouve cependant régulièrement des préfixes comme dev/, feature/, fix/, etc.

Par exemple :

```dev/shoot``` <br> 
```dev/enemy``` <br>
```dev/entity``` <br>
```feature/inventory``` <br>
```fix/reload ``` <br>

L'objectif est simplement de rendre le nom de la branche compréhensible. Le nom doit permettre de savoir rapidement sur quoi porte le travail réalisé sur cette branche.

Dans certains projets, on peut également ajouter le nom de la personne ou une référence à une tâche :

```dev/shoot/max``` <br>
```feature/inventory/matteo ```<br>
```fix/reload/123```<br>

Ce type de convention est particulièrement utile dans une équipe, car elle permet de retrouver plus facilement qui travaille sur quoi et éventuellement de faire le lien avec une tâche ou une issue.

Il existe beaucoup de conventions différentes selon les équipes et les studios. L'important est surtout de choisir une convention commune et de la respecter. Dans un projet personnel, vous êtes évidemment libres d'utiliser les noms qui vous conviennent, mais dans un projet d'équipe, il vaut mieux éviter de donner des noms arbitraires aux branches.

### À retenir : 
il n'existe pas une nomenclature obligatoire pour les branches. On utilise principalement des conventions communes pour rendre leur rôle immédiatement compréhensible.

## 8. Organisation des branches

L'organisation des branches dépend du workflow choisi par l'équipe. Contrairement à la nomenclature, Git n'impose pas une organisation particulière : c'est l'équipe qui définit quelles branches sont utilisées et quel rôle elles ont.

Dans une organisation simple, on peut avoir une branche principale, généralement appelée main ou master, et plusieurs branches de travail créées à partir de celle-ci.

En règle générale, lorsqu'on travaille en équipe, on évite de modifier directement la branche principale. Chaque personne travaille sur une branche dédiée à sa fonctionnalité ou à sa tâche.

Par exemple :

    main
    ├── dev/shoot
    ├── dev/enemy
    └── dev/inventory

Une fois la fonctionnalité terminée, la branche peut être fusionnée dans main, puis supprimée si elle n'est plus nécessaire. Pour une nouvelle fonctionnalité, on crée généralement une nouvelle branche à partir d'une branche à jour.

Il est également important de se tenir régulièrement à jour avec le travail des autres membres. Faire régulièrement des fetch et des pull permet de limiter l'écart entre notre travail et celui du reste de l'équipe, et donc de réduire les risques de conflits au moment de l'intégration.

On peut aussi créer une branche à partir d'une autre branche lorsqu'une fonctionnalité nécessite plusieurs développements liés. Cela permet d'organiser plus précisément le travail, mais il faut éviter de rendre l'arborescence inutilement complexe.

Pour intégrer les modifications, on peut simplement effectuer un merge, ou utiliser une Pull Request dans un workflow plus structuré. Les Pull Requests permettent notamment de faire vérifier les modifications avant leur intégration. On reviendra plus en détail sur les merges et les Pull Requests dans les prochaines sections.

Workflow plus structuré

Dans certaines équipes, on trouve également une branche supplémentaire dédiée à l'intégration, par exemple :

    master          → production
    ↑
    main / main-dev → intégration
    ↑
    branches de développement

Dans ce fonctionnement, les développeurs travaillent sur leurs branches, leurs modifications sont regroupées dans main ou main-dev, puis une version suffisamment stable peut être intégrée dans master, qui représente la production.

Ce fonctionnement reste une convention d'équipe : Git n'impose pas cette organisation.

### À retenir : 
on développe principalement sur des branches séparées, puis on intègre le travail dans les branches communes selon le workflow de l'équipe.
## 9. Merge
## 10. Pull Request
## 11. Résolution des conflits
## 12. Synchronisation et workflow d'équipe
## 13. Annulation / Revert
## 14. Avantages et limites de Git/GitHub
## 15. Git dans les projets de jeux vidéo
## 16. Erreurs et risques
## 17. Tags / Releases