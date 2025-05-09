## WINDEV WEBDEV

Présentation

L'utilitaire ReplicEdit
ReplicEdit est un outil permettant de dénir les caractéristiques d'une réplication. Cette réplication sera ensuite
utilisée par la réplication universelle assistée soit en mode automatique (avec les outils ReplicSynchro et
ReplicAdmin), soit en mode programmé.

Lancement de ReplicEdit

Lancement de ReplicEdit
Pour lancer ReplicEdit :
sous le volet "Outils", dans le groupe "Base de données", déroulez "Réplication" et sélectionnez "ReplicEdit -
Editeur de réplication".
lancez directement le programme "ReplicEdit.EXE".

Condition d'utilisation
ReplicEdit est un outil redistribuable.

Fichiers nécessaires
Les chiers nécessaires à l'installation de ReplicEdit sont les suivants :

```
ReplicEdit.EXE wd300com.dll
```
```
wd300action.dll wd300rpl.dll
```
```
wd300hf.dll wd300mat.dll
```
```
wd300obj.dll wd300pnt.dll
```
```
wd300std.dll wd300sql.dll
```
```
wd300vm.dll wd300xml.dll
```
```
WDOutil.WDK ReplicEdit_FR.PDF
```
```
WINDEV Mobile Autres
```
# ReplicEdit : Editeur de réplication


```
ReplicEdit_EN.PDF
```
Fonctionnalités de ReplicEdit

Pour utiliser la réplication universelle assistée

1. Créer une réplication avec ReplicEdit.
2. Ajouter les chiers de données dans cette réplication.
3. Dénir les options de réplication (inutile dans le cas d'une réplication mobile (Android/iOS)).
4. Si la réplication doit être réalisée avec un serveur de réplication, il est nécessaire de publier la réplication
   .


## WINDEV WEBDEV

Présentation

Pour mettre en place une réplication assistée, la première étape consiste à créer la réplication avec ReplicEdit.

La création de la réplication est réalisée grâce à un assistant.

Les paramètres dénis dans cet assistant pourront à tout moment être modiés dans la
description de la réplication.

Création de la réplication

Pour créer une réplication :

1. Lancez ReplicEdit depuis WINDEV, WEBDEV ou WINDEV Mobile : sous le volet "Outils", dans le groupe "Base de
    données", déroulez "Réplication" et sélectionnez "ReplicEdit - Editeur de réplication".
2. Si l'assistant de démarrage se lance, sélectionnez l'option "Créer une nouvelle réplication".

```
Si non, sélectionnez l'option "Fichier .. Nouveau". L'assistant de création de réplication se lance.
```
```
WINDEV Mobile Autres
```
# Créer une réplication


3. Dans l'assistant de création de réplication, indiquez le nom et la description de la réplication. Le nom sera
    donné au chier de réplication qui sera créé (chier d'extension .WER).

```
Passez à l'étape suivante.
```

4. La description des chiers de données à synchroniser doit être chargée dans ReplicEdit an de créer la
    réplication.

```
L'assistant propose 2 possibilités :
Utiliser une analyse (WDD). Il sut de sélectionner le chemin du chier ".WDD" correspondant et le mot
de passe associé (si nécessaire).
Dans ce cas, il est nécessaire que l'analyse contienne une connexion HFSQL Client/Serveur. Cette
connexion doit être associée aux chiers de données
En eet, ReplicEdit ne permet pas de créer une connexion. Il est possible uniquement de modier une
connexion existante.
Importer depuis un serveur HFSQL. Cette option permet d'utiliser directement la description d'une base
de données HFSQL Client/Serveur installée sur un serveur (méthode à utiliser par exemple si l'application
est déployée). Cette solution est à préconiser si vos chiers de données sont décrits en HFSQL
Client/Serveur dans l'analyse. En eet, ReplicEdit va automatiquement aecter aux chiers de données
à répliquer la connexion que vous aurez utilisée.
Dans ce cas, l'assistant demande :
les paramètres de connexion : adresse, port, utilisateur et mot de passe.
la base de données à répliquer.
Dans les deux cas, vous devez vous assurer des points suivants :
La base de données sur le serveur HFSQL ne contient que des chiers de données décrits dans votre
analyse. Dans le cas contraire, une erreur apparaîtra en exécution.
Les structures de ces chiers de données sur le serveur doivent être strictement identiques à leurs
dénitions dans l'analyse.
```

5. L'étape suivante permet de choisir le sens de la réplication.

```
Le sens de la réplication peut être :
Bidirectionnel : les données sont synchronisées sur la base de données maître et sur la base de données
abonnée.
Vers l'abonné uniquement : les données sont synchronisées uniquement du maître vers l'abonné.
Vers le maître uniquement : les données sont synchronisées uniquement de l'abonné vers le maître.
```

6. L'étape suivante permet de choisir la méthode pour gérer les conits de modication.

```
La gestion des conits permet de gérer le cas où le même enregistrement a été modié à la fois par le maître
et par l'abonné. Choisissez la règle à appliquer :
Plus récent prioritaire : seul le dernier enregistrement modié est pris en compte.
Maître toujours prioritaire : l'enregistrement de la base maître est celui pris en compte.
Abonné toujours prioritaire : l'enregistrement de la base abonnée est celui pris en compte.
Attention : pour éviter tout problème, il est important que le serveur et les postes abonnés utilisent la
même heure.
```

7. A la n de l'assistant, il est possible d'ajouter un chier de données à la réplication ou d'aller directement
    dans l'éditeur.


## WINDEV WEBDEV

Présentation

ReplicEdit permet de créer une réplication à l'aide d'un assistant mais des paramètres supplémentaires peuvent
être connus ou congurés via la fenêtre de description de la réplication.

Pour éditer la description d'une réplication, sélectionnez l'option "Réplication .. Description de la réplication".

Les diérentes options

Onglet "Général"
L'onglet "Général" présente les informations suivantes :
Nom de la réplication,
Description de la réplication
Sens de réplication,
Gestion des conits.

Ces informations ont été saisies lors de la création de la réplication et peuvent être modiées à tout moment.

Onglet "Paramètres"
L'onglet "Paramètres" indique les diérents paramètres attendus par la réplication.

Ces paramètres correspondent aux ltres posés sur les chiers à répliquer.

Il est ainsi possible d'obtenir l'ordre des paramètres utilisés par la fonction RéplicInitialise.

Onglet "Fichiers maîtres"
Cet onglet permet d'indiquer :
lors de la réplication d'une base de données HFSQL Classic, le répertoire de base des chiers maîtres HFSQL
Classic.
le mode d'accès et la localisation des chiers maîtres de la réplication.

Onglet "Avancé"
Cet onglet permet d'indiquer les options avancées de la réplication :

```
WINDEV Mobile Autres
```
# Description de la réplication

# (ReplicEdit)


Détermination automatique de l'ordre des chiers de la réplication en tenant compte des contraintes
d'intégrité. : Cette option permet de déterminer automatiquement l'ordre des chiers répliqués (selon les
contraintes d'intégrité). Si cette option n'est pas sélectionné, l'ordre est déterminé par l'ordre déni dans
l'onglet "Paramètres".
Reporter les modications automatiques des chiers de données de la base maître vers les bases
abonnées (possible uniquement si les deux bases utilisent HFSQL Classic et/ou Client/Serveur). : Cette
option permet de prendre en compte la modication automatique des données. Dans ce cas :

```
Une modication de la structure de la base de données maître sera reportée sur la base de données
abonnée.
Les nouvelles rubriques seront prises en compte par la réplication.
Faux (valeur par défaut). La modication automatique des données eectuée sur la base de données
maître n'est pas reportée sur la base de données abonnée. Attention : ce paramètre est disponible
uniquement pour une réplication entre des bases de données HFSQL (Classic ou Client/Serveur).
```

## WINDEV WEBDEV

Présentation

Une réplication est composée de un ou plusieurs chiers de données. RepliEdit permet à tout moment d'éditer la
description d'un chier de données pris en compte par la réplication.

Pour éditer la description d'un chier de données :

1. Sélectionnez le chier de données dans la liste achée sous l'éditeur de réplication.
2. Double-cliquez sur son nom ou sélectionnez l'option "Propriétés" du menu contextuel.

Les diérentes options

Onglet "Général"
L'onglet "Général" présente les informations suivantes :
Nom du chier de données,

```
WINDEV Mobile Autres
```
# Description des chiers de données

# répliqués (ReplicEdit)


```
Mode d'accès au chier de données maître,
Sens de réplication,
Gestion des conits.
```
Ces informations ont été saisies lors de l'ajout du chier dans la réplication et peuvent être modiées à tout
moment.

Onglet "Filtre"
L'onglet "Filtre" permet de ltrer les données à répliquer.

Prenons un exemple simple : Un commercial veut récupérer localement la base des clients. Au lieu de mettre à
jour toute la base, il ne prend que les clients habitant en France.

Pour créer un ltre sur un chier de données :

1. Dans l'onglet "Filtre", sélectionnez l'option "Sélection".
2. La liste des rubriques présentes dans le chier de données apparaît.
3. Sélectionnez la ligne correspondant à la rubrique à ltrer.
4. Dans la colonne "Condition", sélectionnez la condition à appliquer à la rubrique.
5. Dans la colonne "Valeur ou paramètre", indiquez :
    Soit la valeur voulue (par exemple "France").
    Soit un paramètre (par exemple "Ville"). Ce paramètre sera initialisé avec la valeur voulue au moment de la
    synchronisation

Remarque : Il est également possible de saisir directement un ltre manuel.

Conseils :
Filtrez les données répliquées. Ainsi, la réplication sera plus rapide, le nombre d'enregistrements répliqué
étant limité.
Donnez un nom explicite aux paramètres.
Ces paramètres pourront être utilisés dans la fonction ReplicInitialise.
Ces paramètres seront visualisés par les utilisateurs naux qui lanceront la réplication à l'aide de
ReplicSynchro.

Onglet "Rubriques"
L'onglet "Rubriques" permet de congurer les rubriques à répliquer. Par défaut, toutes les rubriques sont
répliquées.

Cet onglet permet également d'indiquer la rubrique de datation utilisée pour la réplication.


## WINDEV WEBDEV

Présentation

Lorsque la réplication est décrite, il est nécessaire d'ajouter les chiers de données pris en compte dans la
réplication. Cette opération est réalisée à l'aide d'un assistant.

Ajouter des chiers de données dans une réplication

Ajout du chier de base

1. Sélectionnez l'option "Réplication .. Ajouter un chier de données". L'assistant d'ajout d'un chier de données
    se lance.
2. La liste des chiers de données décrits dans l'analyse en cours ou présents sur le serveur est achée.

```
Vous pouvez sélectionner un ou plusieurs chiers de données à synchroniser. Par défaut, tous les
enregistrements sont répliqués.
```
```
WINDEV Mobile Autres
```
# Ajouter des chiers de données dans

# une réplication (ReplicEdit)


3. Pour les chiers de données sélectionnés, vous pouvez dénir :
    le sens de réplication des chiers de données :


```
la gestion des conits de modication.
```
```
Il est possible de choisir :
le mode par défaut déni précédemment (conseillé).
un autre mode.
```
4. L'assistant est terminé. La réplication est décrite. L'éditeur de réplication liste les chiers de données pris en
    compte dans la réplication.

Les chiers de données achés en gris sont des chiers de données liés : un chier de données lié est un chier
de données qui est lié à un chier de données de base (appartenant déjà à la réplication). Selon la réplication
eectuée, les données du chier de données lié peuvent être ajoutées ou non.

Vous pouvez enregistrer la réplication (option "Fichier .. Enregistrer"). La réplication est enregistrée sous forme
d'un chier de type ".Wer".

Ce chier contient la description de la réplication. Il devra être présent à côté de l'exécutable sur les postes
abonnés.

Ajout d'un chier de données lié
Pour ajouter un chier de données lié :

1. Double-cliquez sur le chier de données lié (aché en gris) sous ReplicEdit. L'assistant d'ajout d'un chier de
    données lié se lance.


2. Par défaut, les données du chier de données lié sont celles correspondantes au chier de base. Ainsi, si le
    chier de base est ltré, les enregistrements du chier lié utilisent le même ltre.
    Remarque : Pour mettre un ltre sur le chier de base, achez la description du chier de données.
3. Indiquez si un ltrage supplémentaire doit être eectué. Si vous ajouter un ltrage, donnez les
    caractéristiques nécessaires.
4. Dans la suite de l'assistant, indiquez le sens de réplication du chier de données lié ainsi que le mode de
    gestion des conits.
5. Terminez l'assistant. Le chier de données lié apparaît désormais en chier de données à répliquer.


## WINDEV WEBDEV

Présentation

La création d'une réplication avec ReplicEdit permet d'indiquer de nombreux paramètres :
Les caractéristiques de la réplication (sens de réplication, mode de gestion des conits, ...)
Les diérents chiers à répliquer (chiers de base, chiers liés, ...).

Selon le type des chiers à répliquer, des informations complémentaires doivent être indiquées pour
permettre de réaliser une réplication universelle assistée automatique (à l'aide de ReplicSynchro) ou
programmée.

Les options de réplication permettent notamment d'indiquer l'emplacement de la base maître.

Réplication d'une base de données HFSQL Classic

Lors de la réplication d'une base de données HFSQL Classic, il est nécessaire d'indiquer dans le chier de
réplication la localisation des chiers maître de la réplication.

Pour dénir le répertoire des chiers de données maître HFSQL Classic :

1. Achez la description de la réplication (option "Réplication .. Description de la réplication").
2. Sélectionnez l'onglet "Fichiers maîtres". Dans cet onglet, il est possible de :
    Indiquer le répertoire de base pour les chiers maître HFSQL Classic, à l'aide du sélecteur de répertoire.
    Paramétrer les caractéristiques de chaque chier. Il sut de double-cliquer sur le nom du chier : la
    fenêtre de description du chier apparaît. Dans l'onglet "Général", il est possible de préciser :
       le nom physique du chier. Ce paramètre peut correspondre à un chemin complet, à un chemin relatif
       (qui sera ajouté au répertoire de base spécié) ou à un nom de chier. Si seul un nom de chier est
       spécié, il sera recherché dans le répertoire de base spécié.
       le mot de passe du chier (si nécessaire).

Remarque : Ces informations peuvent également être fournies lors de la préparation de la procédure
d'installation ou encore lors de l'installation.

Réplication d'une base de données Client/Serveur

Connexions
Lors de la réplication d'une application Client/Serveur, par défaut, ReplicEdit utilise les connexions dénies dans
l'analyse. Pour des raisons de sécurité, seul le mot de passe n'est pas initialisé.

```
WINDEV Mobile Autres
```
# Options de la réplication (ReplicEdit)


Pour donner le mot de passe associé aux connexions (ou pour modier les connexions), sélectionnez l'option
"Réplication .. Description des connexions".

Pour modier l'association d'un chier à une connexion :

1. Sélectionnez l'option "Réplication .. Description des chiers de données".
2. Sélectionnez le chier voulu et cliquez sur l'icône de recherche.
3. Sélectionnez la connexion voulue.

Remarques :
Réplication universelle assistée automatique (par ReplicSynchro) : Ces paramètres sont modiables lors de la
préparation de l'installation.
Réplication universelle assistée par programmation : Seul ReplicEdit permet de modier ces paramètres.

Rubrique de réplication
Lors de la réplication d'une base de données utilisant un accès natif, il est nécessaire de dénir une rubrique
spécique de type DateHeure dans chaque chier répliqué. Cette rubrique sera mise à jour par l'application lors
de la modication ou lors de l'ajout d'un enregistrement.

Pour indiquer la rubrique de réplication :

1. Sélectionnez l'option "Réplication .. Description des chiers de données".
2. Double-cliquez sur le chier concerné. La fenêtre de description du chier s'ache.
3. Dans l'onglet "Rubriques", indiquez la rubrique de datation des enregistrements.

Sélection des rubriques à répliquer

ReplicEdit permet également de ne pas prendre en compte certaines rubriques des chiers de données lors de la
réplication.

Pour ne pas répliquer toutes les rubriques :

1. Sélectionnez l'option "Réplication .. Description des chiers de données".
2. Double-cliquez sur le chier de données concerné. La fenêtre de description du chier s'ache.
3. Dans l'onglet "Rubriques", seules les rubriques cochées seront répliquées.


## WINDEV WEBDEV

Présentation

Une description de réplication créée avec ReplicEdit peut être publiée directement depuis cet outil sur un serveur
de réplication.

Cette manipulation doit être réalisée notamment lors d'une réplication d'une application Android ou iOS.

Comment le faire?

Publier une réplication
Pour publier une réplication :

1. Sélectionnez l'option "Déploiement .. Déployer la réplication sur un serveur". L'assistant se lance.
2. Sélectionnez le serveur sur lequel la réplication doit être déployée :

```
Un serveur de réplication dédié.
Un serveur de réplication du Cloud PC SOFT. Dans ce cas, vous devez posséder un compte Cloud PC SOFT.
```
```
WINDEV Mobile Autres
```
# Publier la réplication depuis

# ReplicEdit


3. Dans le cas d'un serveur de réplication dédié, ce serveur a été installé précédemment. Pour plus de détails,
    consultez Serveur de réplication pour la réplication universelle assistée.
4. Indiquez :
    l'adresse du serveur (de préférence l'adresse IP),
    un login et un mot de passe,
    le nom de la réplication (nom du chier WER).


5. Dans l'étape suivante, indiquez la périodicité de la préparation des données à répliquer :

```
Préparation immédiate : la préparation des données à répliquer est eectuée lors d'une demande de
réplication. Dans ce cas, la réplication permettra d'obtenir les données les plus à jour. Cependant, la
préparation du réplica peut être lente.
Préparation périodique : la préparation des données à répliquer est eectuée régulièrement, selon une
périodicité dénie. Dans ce cas, lors de la demande de réplication, les dernières données préparées sont
automatiquement utilisées. Cette solution est rapide (le temps de préparation des données à répliquer est
nul) mais les données peuvent ne pas être à jour.
Cette solution est conseillée dans le cas d'une réplication d'une application mobile (Android ou iOS).
```

6. Validez. L'assistant propose le code WLangage à placer dans l'application pour synchroniser les données.


## WINDEV WEBDEV

Présentation

Lors de la modication de l'analyse d'une application répliquée (ajout d'une rubrique, d'un chier, ...), il est
nécessaire de prendre en compte cette modication dans la description de la réplication.

Comment le faire?

Pour prendre en compte les modications eectuées dans l'analyse dans le chier .WER de la réplication :

1. Ouvrez le chier .WER voulu sous ReplicEdit.
2. Sélectionnez l'option "Réplication .. Se mettre à jour de la description de l'analyse".

Attention
Si les connexions dénies dans l'analyse nécessitent des mots de passe, il est nécessaire de ressaisir ces mots de
passe dans ReplicEdit (pour plus de détails, consultez Options de réplication).

```
WINDEV Mobile Autres
```
# ReplicEdit : Prise en compte des

# modications de l'analyse


