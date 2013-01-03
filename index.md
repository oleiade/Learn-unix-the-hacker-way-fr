## Prelude

TODO

# Introduction

### De quoi s'agit-il

### Pourquoi tout ce tintouin

TODO

### a destination de?

#### To

TODO

### Qui a commis ceci?

TODO

# Au jour le jour

### C'est quoi un file-system

#### Exercices

Faire joujou avec le systeme de fichier

**1**. Trouver comme ouvrir un terminal. (Le mettre en blanc sur noir, celui par defaut d'OSX pique les yeux, genre... aie)

**2**. Te documenter pour savoir ce qu'est une commande

**3**. Quelle est la syntaxe pour passer des options a une commande?

**4**. Trouver les commandes qui permettent d'effectuer les actions suivantes :

* Imprimer a l'ecran l'endroit sur le systeme de fichier ou tu te trouves actuelement

* Lister le contenu d'un dossier + lister recursivement le contenu d'un dossier (c'est une option) + lister les fichiers en affichant leur date de creation, l'utilisateur qui les a creer, et les droits que celui ci a dessus ( on verra plus en profondeur les droits plus tard))

    * Se deplacer dans le systeme de fichier

    * Copier un fichier + copier un dossier

    * Deplacer un fichier + deplacer un dossier

    * Renommer un fichier (pas une commande en soi :) ) + renommer un dossier

    * Effacer un fichier + effacer un dossier

    * Creer un dossier

    * Creer un fichier

    * Ecrire dans un fichier ( tu peux utiliser un petit outil en ligne de commande baptise nano, familiarise toi avec, il est tres tres simple, et tres pratique) + le sauver sur `~/Desktop` ( tiens d'ailleurs, a quoi correspond le tilde? )

**5**. C'est quoi un systeme unix? C'est quoi la difference avec windows?

#### Defi

Maintenant, un vrai defi: je veux que tu trouves avec quelle commande et avec quelles options te connecter au serveur en ftp, en ligne de commande, et que tu rappatries l'episode 4 de borgen dans le dossier `~/Downloads` de ton mac :D

Tu kiff hein?! :D C'est plus simple que ca en a l'air :)

**Nota**

Au prealable, je te conseille de lire quelques petits tutos pour comprendre ce qu'est un systeme de fichiers, a quoi ca correspond, et a quoi ca ressemble :)

En gros, le systeme de fichier, c'est le nom qu'on donne a l'agencement des dossiers sur ton ordinateur, c'est la ou il, toi, et tous les utilisateurs de l'ordi vont ranger leur donne. C'est comme un gros arbre avec des branches. La plupart des systemes unix partagent cette hierarchie.

Ensuite, la commande qui te sauvera toujours la vie, et qui a donne naissance au fameux RTFM (Read The Fucking Manual) est `man`. Pour chaque commande du systeme, tu as ce qu'on appelle un man. Genre, si tu tapes 'man cat' tu auras le manuel utilisateur de la commande cat, detaillant son utilisation, et toutes les options que tu peux lui passer.

Voila, si c'est confus (c'est pas si facile de faire un cheminement clair), hesite pas a hurler pour avoir de l'aide :D

#### Background

TODO


### Les fichiers et les internets

#### Exercices

Sur unix,  il faut le savoir tout est fichier. Un fichier est un fichier, un dossier est un fichier, même une connexion internet est un fichier,  simplement ils représentent tous les informations qu'ils contiennent d'une manière différente.

Tu peux a peu près tout savoir de ton ordinateur en lisant les bons fichiers tu peux a peu près tout faire en modifiant les bons fichiers.

Du coup au programme d'aujourd'hui manipulation de fichier,  et trifouillage avec les internets.

##### Préambule

**1**. Quelle est la différence entre ~/Desktop,  /Users/morganetual/Desktop ?  Quand tu tapes / et que tuappuies deux fois sur tab que se passe t'il ?  Qu'en conclus-tu ?  Ca ne te rappelle rien.
Re-regarde la hiérarchie du système de fichier unix,  ca devrait t'eclaire.  Si tu ne comprends pas cette étape,  HURLE.

**2**. Comment lire un fichier, c'est a dire, simplement l'afficher a l'ecran. (Sans utiliser nano, ou vi: deux commande native existe deja au sein d'unix)

**3**. Comment afficher les derniers lignes d'un fichier? comment afficher les premières? Quelle est l'option commune a ces deux commandes pour lui specifier combien de ligne depuis le debut/la fin on souhaite afficher la l'ecran.

**4**. Quelle commande utiliser pour chercher des occurences (des expressions) dans un fichier. Par exemple, si tu cree un fichier avec le contenu suivant dans ~/Desktop:

    ABC
    Easy as...
    123
    As simple as...
    Do re mi
    ABC, 123, baby, you and me girl
    ABC
    Easy as...
    123
    As simple as...
    Do re mi
    ABC, 123, baby, you and me

* Comment verifier que celui ci contient bien l'occurence 123?
* Comment trouver tous les fichiers dans ~/Desktop qui contienent l'occurence "As simple as..."
* Comment trouver tous les fichiers dans ~/Desktop qui matchent l'expression reguliere `^ABC$` (meme commande)?

**5**. A l'aide de quelle commande peux-tu compter le nombre de lignes dans un fichier? Combien y en a t'il dans le fichier que je t'ai fait creer precedement ? :)

**6**. Quelle commande utiliser pour chercher des fichiers/dossiers sur le file system?

Comment trouver a l'aide de celle-ci tous les dossiers qui se nomment `morganetual` a l'interieur de /Users ?

Comment trouver a l'aide de celle-ci tous les fichiers qui s'appellent morganetual sur le disque dur, c'est a dire, a partir de / ? (n'hesite pas a revoir l'agencement et la hierarchie du filesystem unix :) )

**7**. Qu'est-ce qu'un lien sur un systeme unix? Quelle commande permet d'en faire un ? Quelle difference entre un lien symbolique et un hardlink?

Comment faire un lien symbolique du fichier precedemment creer dans le dossier desktop afin de pouvoir y acceder depuis `~/` ?

*Allez, des trucs plus fun maintenant.*

**8**. Quelle est l'adresse ip `locale` de tous les ordinateurs? (l`ocalhost`)

Comment trouver l'ip d'un domaine? Par exemple: trouve l'ip de `oleiade.com`, celle de botify.com... Il y a plusieurs methodes possibles.

Comment decouvrir le temps que mets un site a te repondre? avec quelle commande?

**9**. Trouve une commande (qui n'est pas curl) qui te permette de telecharger un fichier depuis son url. Rappatrie, et affiche les 42 dernieres lignes du fichier situe a l'url suivante: `http://http://wiki.freebase.com/images/e/eb/Steve-martin-quad-sample.txt`

#### Defi du jour

A l'aide de la commande curl (que tu auras probablement a installer, via homebrew ou autre), je voudrais que tu telecharges et ecrive dans un fichier morganetual_com.html dans `~/` la page d'accueil de http://morganetual.com
Encore une fois, si des etapes ne sont pas assez detaillees, pas assez claires, besoin d'aide, HURLE :D

#### Background

TODO


### Le root et l'anonymous

#### Exercices

##### Un peu plus sur le shell

Jusqu'ici on s'est contente d'operations assez basiques dans l'ensemble: demander au systeme d'effectuer une, et une seule action a la fois.

Cependant le shell sait faire beaucoup plus que ca, et met a disposition ce qu'on appelle des operateurs qui permette par exemple d'exprimer le `AND`(fais ceci, et, cela), le `OR` (fais ceci, ou, si ca ne marche pas, fais cela), le `PIPE`, les superior, inferior.

Leur apprentissage peut etre fastidieux, moi-meme je n'en utilise quotidienement qu'un lot tres restreint. Parcours les internets pour en apprendre un peu plus et c'est parti:

**1**. Quel est l'operateur qui permet de chainer des commandes? C'est a dire de les executer a la suite les unes des autres?

**2**. Tu te rappelles le symbole `~` ? Lorsque tu l'utilise au sein des arguments d'une commande, le shell comprend qu'il doit le remplacer par le dossier principal de ton utiliser (`/Users/morganetual` sur ton mac). Il y a un autre symbole qu'il interprete comme : remplacer ce symbole par le dernier repertoire dans lequel je me situais avant celui-la, quel est-t'il ?

Il y en a encore un autre qu'il interprete comme : remplacer ce symbole par la liste de tous les elements de ce dossier, lequel est-il?

**3**. Trouve le moyen en une seule commande de : te deplacer dans le dossier `/Users/Morganetual/Downloads`, en afficher le contenu, puis te deplacer dans le dossier `/etc`, afficher les 42 dernieres lignes du fichier passwd qui s'y trouve, enfin de retourner dans le dossier `/Users/morganetual/Downloads`.

Attention, ici j'attend que tu utilises ce que tu as appris a point 1. et 2.

**4**. (*optionel parce qu'un peu complexe*)  Il y a un operateur qu'on appelle de redirection (superieur ou inferieur) qui permet, comme son nom l'indique de rediriger la sortie d'une commande dans une autre.

A l'aide de echo, sauras-tu inserer "Hello World" dans un fichier `mypleasure.txt` a l'aide de l'operateur superieur?

**Nota**: Je ne l'avais pas mentione jusqu'ici, mais un programme sur unix, a ce qu'on appelle une entree (les fichiers que tu lui demande de traiter, d'utiliser, (c'est le cas de `ls`), le texte que tu lui demande de manipuler (c'est le cas de cat, ou de grep quand tu lui demande de trouver une occurence), et une sortie: le resultat.

Il est important de garder a l'esprit que toutes ces entrees, et sorties sont dites "normalisees", ces normes sont generalement definies par ce qu'on appelle la norme POSIX (C'est pour la culture generale).

Donc tu peux parfaitement, envoyer la sortie d'un programme, en tant qu'entree d'un autre. C'est trop abstrait?

*Un exemple*:

Je peux trouver tous les fichiers qui contienent "test" dans le dossier `/Users/morganetual` en envoyant le resultat de la commande ls dans l'entree de grep, c'est l'operateur `pipe`:

    ls /Users/morganetual | grep

**5**. Trouve  une commande qui permette de lister tous les processus en cours sur ton ordinateur, et recherche-y firefox :)


##### Le droit de rien, l'envie de tout.

**6**. Qu'est-ce qu'un groupe sur un systeme unix? qu'est-ce qu'un administrateur? quel est son nom? Comment executer une commande en tant qu'administrateur?

**7**. A l'aide de quelles options de la commande ls peut-lister en version longue l'integralite de tous les fichiers d'un dossier (tu peux au passage utiliser l'un des symboles decouverts plus haut) ?

A quelle information correspond chacun des elements de la ligne?

Si tu utilises cette methode sur ton dossier HOME (`/Users/morganetual` ou `~/`), et que tu compares le resultat avec ce que t'affiches le finder dans ce meme dossier, que constate-tu? Qu'est-ce qui en est la cause?


**8**. Puisque dorenavant, tu sais quel element dans ce listing represente les droits afherents a ces fichiers, a quoi correspondent chacun des dix membres de cet elements? (d f ou l, puis r, w, ou x repetes).

**9**. Comment change t'on les droits d'un fichier?
**10**. Comment change t'on les droits d'un dossier?
**11**. Comment change t'on son possesseur? (owner)

**12**. Creer un fichier `/Users/morganetual/test` et change ses droits afin que l'utilisateur ai le droit d'y ecrire, de le lire, de l'executer, son groupe ai les memes droits, et qu'un utilisateur lambda n'ai le droit que de le lire.
* Change le owner de ce fichier afin que ce soit root
* Change le groupe de ce fichier afin que ce soit root egalement
* Est-ce que sans utiliser la commande qui permet d'etre administrateur tu parviens a y ecrire dorenavant? pourquoi?


#### Defi

En preambule de la suite, je voudrais que tu apprenes a utiliser la commande ssh et la commande scp.

Documente toi un peu sur ce que c'est que le protocole ssh (scp en est une extension, est-ce que tu peux deviner juste a l'aide de son nom a quoi elle sert).

Le but du jeu sera dans un premier temps de parvenir a te connecter au serveur ssh oleiade.com, a l'aide de ton identifiant : morgane et de ton mot de passe : asimov, via le port 4242 (tiens, tiens, c'est quoi un port unix?

Et tiens, au fait, c'est quoi tcp, aussi appelle tcp/ip, c'est quoi la difference avec udp? ) et d'y creer un fichier victoire.diditbitch dans lequel tu me mettras un super message d'amour.

Puis de te deconnecter, et de telecharger ce fichier sur ton ordinateur a l'aide de la commande scp.

Enfin, si tu y arrives, tu m'enverras son contenu par mail en chainant la commande cat sur ce fichier, et la command mail (qui permet, comme son nom l'indique d'envoyer des mails, elle est peu abrupte dans un premier temps, hesite pas a googler pour trouver comment l'utiliser)

#### Background

TODO


### Rollback

##### Et si on se revoyait?

**1**. Comment creer le dossier `/Users/morgane/Downdloas/I/Love/You` en une seul commande

**2**. Meme si tu n'as pas internet sur ta machine, connecte toi en ssh a l'ip `127.0.0.1` avec l'utilisateur morgane et le meme mot de passe que ton mac? Est-ce que cela marche? A ton avis, pourquoi?

Qu'est-ce que tu en deduis de ce que represente l'ip 127.0.0.1? qu'est-ce que tu en deduis a propos de ssh?

**3**. Cree le dossier `~/ThisIsATest` et cree y  un fichier abc contenant "easy as" , ainsi qu'un autre fichier 123 contenant "or simple as" a l'aide d'une seule commande. Puis copie le dossier `~/ThisIsATest` dans `~/Downloads` a l'aide de la commande scp.

**4**. Cree un lien symbolique pointant sur le fichier `~/ThisIsATest/abc` dans `~/Desktop`. Ecris dans celui-ci "one, two, three, baby, you and me!" sans utiliser d'editeur.

Si tu te sers d'une commande que tu as deja rencontre pour afficher le contenu du lien symbolique representant le fichier `~/Desktop/abc`, que constates-tu?

Si maintenant tu utilises l'operateur `>>` pour ecrire "Come on, let me love you just a little bit!" a la fin du fichier represente par le lien symbolique `~/Desktop/abc`, qu'est ce qui arrive au fichier `~/ThisIsATest/abc`? pourquoi?

**5**. `cut` : cette commande permet de decouper des morceaux de lignes a l'aide d'un delimiteur. A l'aide cette commande, affiche les colonnes 1 et 5 du fichier `/etc/passwd`. Ce fichier contient des informations sur tous les utilisateurs de ton ordinateur.

Pour info, avoir plusieurs utilisateurs permet de limiter les degats en cas d'attaque/virus/fin du monde, et c'est ce qui explique que Windows est une passoire, et aue ton serveur soit sous Linux (mummmm).

**6**. Affiche le contenu du fichier `/etc/passwd`. Puis compte le nombre de lignes de ce fichier. Maintenant, obtiens le meme resultat en utilisant l'operateur `|` (pipe). Est-ce que son fonctionnement te semble plus clair ?
Continue de jouer avec `|` : refais le #5 en utilisant `|`, plutot que de passer le fichier directement en argument.


##### le shell et l'environnement.

Il y a bien longtemps, quand les ordianteurs prenaient plus de place que ton appartement, on s'y connectait a distance a partir de "terminaux", des ecrans munis d'un clavier, et le programme charge d'interpreter tes commandes et de les transmettre a l'ordinateur s'appelait un shell.

Aujourd'hui, tu as les trois dans le meme objet : ordinateur, ecran et logiciel pour transmettre tes commandes. Citons le poete : le shell est bien un coquillage, mais tu entends les "bruits" de l'ordinateur, et en plus tu peux lui parler.

A chaque fois que tu lances un shell, ou interpreteur de commande, il charge un "environnment", qui lui permet d'avoir un certain nombre d' informations sur ton systeme et tes preferences.

Par exemple, ou sont enregistres les programmes sur ton ordinateur. Le shell te procure un certain nombre d'utilitaires integres pour te faciliter la vie, comme les `|`, les `>>` et `<<`, etc...

**7**. tape la commande `env`

**8**. Dans tout le fratras qui s'affiche, quelle ligne contient :

* ton nom d'utilisateur
* le chemin vers les programmes (aussi appele binaires)
* le chemin vers ton dossier utilisateur
* pour rigoler, es-tu capable de faire ces commandes avec des | et cut ?

**9**. Lis a la fin de ce fichier le man de la commande `export`

Cree une variable biteenbois avec pour valeur popeye.

Pour verifier que tout s'est bien passee, cherche la dans l'environmment avec grep en une seule commande.

**10**. En toute logique, la commande pour supprimer une ligne de l' environnement est `unset`.

Supprime donc la variable que tu viens de creer.

**11**. Recree une nouvelle variable capitaine ave comme value hadock

Ouvre un nouveau terminal et cherche cette valeur dans l'env (pas a la main, fais faire le boulot)

Ouvre un troisieme terminal, et cherche la egalement. Qu'en conclus-tu ?

**12**. L'important c'est le chemin...

Supprime la variable PATH et essaye de lancer quelques commandes selon ton bon plaisir. Rigolo non ?

Qu'en conclus tu ? Est-il possible de retablir la variable path ?

*Man export*

    Set an environment variable. Mark each name to be passed to child processes in the environment.

    Syntax
          export [-fn] [-p] [name[=value]]

    Options
          -f   The names refer to shell functions;
               otherwise the names refer to shell variables
          -n   No longer mark each name for export.
          -p   Display output in a form that may be reused as input.

    If no names are supplied, or if the `-p' option is given, a list of exported names is displayed.

    The return status is zero unless an invalid option is supplied, one of the names is not a valid shell

#### Background

TODO


### Shell scripting

#### Exercices

**Avant toutes choses, un peu de theorie.**

Jusqu'ici, tu t'es contente de papoter avec ton syteme au travers du shell. De lui donner quelques ordres, en les chainant parfois.

C'est très pratique, mais parfois, tu pourrais avoir besoin d'automatiser un peu tout ca. Heuresement, les papas d'Unix ont pense a tout.

C'est ce qu'on appelle le shell scripting, et ça consiste a écrire dans un fichier une série d'instruction. Lorsque tu demanderas au shell d'exécuter ce "script" il effectuera cette série d'instruction les unes a la suite des autres; tu me concéderas que c'est quand meme beaucoup plus pratique que de les retaper une a une a chaque fois.

Le shell script a la réputation d'avoir une syntaxe un peu abrupte pour les débutants, mais c'est aussi une bonne manière d'appréhender pourquoi des langages comme le Python que nous verrons plus tard existent.

Il n'est cependant pas insurmontable, et reste toujours très pragmatique, je t'ai donc trouve une documentation utile qui pourrait t'aider dans ta quête du jour: `http://www.freeos.com/guides/lsst/ch02sec01.html`

**Nota**

On peut considerer le shell comme un telephone avec une ligne direct avec ton système d'exploitation, et plus précisément avec un élément clé de celui qu'on appelle le kernel (plus communément baptise le noyau); c'est lui qui traduit et gère les instructions que tu lui donnes pour les faire exécuter par la machine.

On peut donc considérer que d'une certaine manière, interagir avec le système d'exploitation unix via le shell serait comme donne des instructions a qui on aurait bande les yeux.

  **1**. Creer un fichier hello.sh dans ~/Desktop, qui affiche a l'écran "Hello world \o/", il y a quelques prerequis: s'assurer que le fichier soit exécutable, utiliser un shellbang, et trouver comment l'exécuter, le tutoriel sur le shell script que je t'ai fournis plus haut devrait aider.

  **2**. Modifie le script hello.sh, et cree une variable NAME au sein de laquel tu mettras comme valeur le nom que tu veux, et fait en sorte que le script affiche a l'écran "Hello VALEURDELAVARIABLENAME \o/"

  **3**. Exploitons un peu les variables d'environnement. Les shell script sont comme leur nom l'indique exécute par ton shell, donc elle partage l'environnement de celui-ci (voir les journées précédentes).

  Cree donc une variable d'environnement HELLONAME dont tu setters la valeur selon tes souhaits, et fait en sorte que ton script affiche dorénavant a l'écran "Glad to me meet you VALEURDELAVARIABLE_HELLONAME"

  **4**. Creer un nouveau fichier de script fate.sh, ainsi qu'une variable DESTINY dans l'environement dont la valeur serait 1.

  Au sein de ce script, a l'aide des expressions conditionelles, tu afficheras "Youpi tralala" si la valeur de la variable d'environement DESTINY cree plus tot est 1, "Too bad" si c'est une valeur differente.

  Fait les tests en changeant la valeur de DESTINY dans ton environement avant de lancer le script.

  **5**. A l'aide d'une boucle (indice : for (beaucoup d'exemples sur les internets)), cree dix fichier test_n avec n de 1 a 10 et dans chacun d'entre eux, insere "I'm VALEURDEN" :) dans un dossier suffix_test dans /tmp (la notion de droit peut entrer en ligne de compte)

  **6**. A l'aide d'une boucle et d'expressions conditionelles, affiche les contenu de tous les fichiers precedement cree dont le suffixe n est pair. Puis dont le suffixe n est impair.


#### Defi:

Je voudrais que tu ecrives un premier script shell quicree un dossier "medias" dans ~/Downloads, et qui cree 10 fichiers suffixes (n, comme dans les precedents exercices) avec comme extensions .avi, 10 autres suffixes avec l'extension .jpg, et encore 10 autres suffixes avec l'extension .mp3.

Et qu'ensuite tu ecrives un second script qui cree au sein du dossier "medias" precedemment cree trois autres sous-dossiers : films, photos, musique. Et que celui-ci deplace tous les fichiers dans medias avec l'extension avi dans films, tous ceux avec l'extension jpg dans photos, et tous ceux avec l'extension mp3 dans musique.

Voila voila, si tu trouves ca plus dur, c'est tout a fait normal. Mais comme toujours la cle de tout ca, c'est la pratique, la perseverance, et l'espoir de decouvrir un langage plus simple, plus joli et plus puissant... Un jour il sera tiens, ohhhh oui un jour il sera tiens!


#### Background

TODO