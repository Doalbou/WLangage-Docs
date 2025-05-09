#### WINDEV WEBDEV

### Présentation

WDSQL est un utilitaire permettant de :
Réaliser et d'exécuter des requêtes SQL sur une base de données aussi bien depuis le poste de
développement que depuis le poste de l'utilisateur nal.
Tester la validité des paramètres d'une connexion à une base de données et son fonctionnement.
Convertir la structure d'une base de données HFSQL en script SQL. Ce script pourra ensuite être exécuté
sur une base de données SQL pour créer la base de données correspondante à l'analyse HFSQL.

Remarque : WDSQL est disponible en 32 bits et en 64 bits. La version 64 bits permet par exemple d'accéder à
des bases de données tierces pour lesquelles seul le pilote ODBC en 64 bits est disponible.

### Utilisation

Lancement de WDSQL

Si WINDEV est installé, WDSQL peut être lancé :
Depuis l'éditeur : sous le volet "Outils", dans le groupe "Base de données", cliquez sur "WDSql".
En lançant directement le programme "WDSQL.EXE" (version 32 bits).
En lançant directement le programme "WDSQL64.EXE" (version 64 bits).

Si WINDEV n'est pas installé, WDSQL peut être lancé en lançant directement le programme "WDSQL.EXE".

Dès le lancement de WDSQL, un assistant de connexion apparaît permettant de dénir la base de données à
manipuler.

Conditions d'utilisation

WDSQL est redistribuable. WDSQL peut donc être installé avec les applications développées avec WINDEV. La
licence d'utilisation de WINDEV s'applique intégralement.

Lors de la création de la procédure d'installation, il est possible de livrer WDSQL avec vos applications.

Rappel : La procédure d'installation peut être créée :

```
soit à l'aide de l'assistant : sous le volet "Projet", dans le groupe "Génération", déroulez "Procédure
d'installation" et sélectionnez "Créer la procédure d'installation".
```
```
WINDEV Mobile Autres
```
## WDSQL, Interrogateur SQL :

## Présentation


```
soit depuis l'éditeur d'installation : sous le volet "Outils", dans le groupe "Utilitaires", cliquez sur "WDInst".
```
Installation de WDSQL sur un autre poste

Les chiers nécessaires à l'installation de WDSQL sont les suivants :

```
WDSQL.EXE (32 bits) ou WDSQL64.EXE (64 bits) wd300cpl.dll
```
```
wd300com.dll wd300etat.dll
```
```
wd300hf.dll wd300html.dll
```
```
wd300mat.dll wd300obj.dll
```
```
wd300oledb.dll wd300pnt.dll
```
```
wd300prn.dll wd300rpl.dll
```
```
wd300rtf.dll wd300std.dll
```
```
wd300sql.dll wd300vm.dll
```
```
wd300xml.dll WDOutil.WDK
```
#### WDSQL_FR.PDF WDSQL_EN.PDF

### Fonctionnalités de WDSQL

Pour utiliser WDSQL, les diérentes étapes sont les suivantes :

1. Connexion à une base de données (HFSQL ou non).
2. Création d'une requête SQL.
3. Exécution d'une requête SQL.

Il est également possible de :

```
Exporter et imprimer le résultat d'une requête SQL.
Créer et exécuter un script.
Convertir la structure d'une base de données.
```

Connaître la structure d'une base de données.


#### WINDEV WEBDEV

### Présentation

La première opération à eectuer pour utiliser WDSQL est la connexion avec une base de données. Lorsque
cette connexion est établie, il est possible de créer et d'exécuter des requêtes SQL sur la base de données
manipulée.

Plusieurs types de connexion sont possibles :

```
Connexion directe à une base de données HFSQL Classic.
Connexion à une base de données via un provider OLE DB.
Connexion à une base de données via un driver ODBC.
Connexion à une base de données via un accès natif.
```
Remarque : WDSQL permet de mémoriser les paramètres de plusieurs connexions. Pour plus de détails,
consultez le paragraphe "Connexion personnelle".

### Comment le faire?

Etablir une connexion avec une base de données

Pour établir une connexion avec une base de données :

1. Lancez WDSQL : un assistant permet de dénir les paramètres de connexion.
    Si WDSQL est déjà lancé, sélectionnez l'option "Fichier .. Connexion" (ou cliquez sur l'icône ). La
    connexion en cours est automatiquement fermée.
    Remarque : Les paramètres de la dernière connexion établie sont automatiquement proposés.
2. Sélectionnez le mode d'accès à la base de données (option "Connexion par").
    Remarque : WDSQL permet :
       Soit de dénir les paramètres d'une connexion. La connexion peut être réalisée via :
          un provider OLE DB,
          un driver ODBC,
          un accès natif (AS/400, Oracle, SQL Server, ...).
       Soit d'utiliser une connexion mémorisée (appelée "Connexion personnelle"). Pour plus de détails,
       consultez le paragraphe Connexion personnelle.

```
WINDEV Mobile Autres
```
## WDSQL : Connexion à une base de

## données


3. Spéciez la source de données de la connexion.

```
Cette source de données peut correspondre :
soit au nom et au chemin complet de la base de données.
Par exemple :
pour HFSQL : "C:\MonRépertoire\BaseDeDonnéesHF.WDD"
pour Access : "C:\MonRépertoire\BaseDeDonnéesAccess.MDB"
soit au nom ou à l'alias du serveur.
Par exemple pour Oracle : "Serveur_Oracle"
soit au répertoire contenant le chier xBase (".DBF").
Par exemple : "C:\MonRépertoirexBase"
```
4. Saisissez si nécessaire le nom de l'utilisateur permettant de se connecter à la base de données.
    Remarque : Ce nom a été déni lors de la création de la base de données. Il peut exister plusieurs
    utilisateurs ayant des droits diérents sur une même base de données.
5. Saisissez si nécessaire le mot de passe. Ce mot de passe correspond :
    Soit au mot de passe en exécution de l'analyse WINDEV (cas d'une base de données HFSQL). Ce mot
    de passe a été déni dans la description de l'analyse.
    Soit au mot de passe utilisé pour se connecter à la base de données (cas d'une base de données
    Oracle, SQL Server, ...). Ce mot de passe a été déni lors de la création de la base de données.
    Remarque : Pour proposer automatiquement ce mot de passe lors du prochain lancement de
    l'assistant de connexion, cochez l'option "Mémoriser le mot de passe de la connexion".


6. Passez à l'étape suivante. La liste des diérents chiers (ou tables) présents dans la base de données
    s'ache.
7. Cochez les chiers (ou tables) à manipuler avec SQL sous WDSQL. Pour chaque chier sélectionné,
    spéciez si nécessaire le mot de passe et le chemin correspondant.
    Remarque : Si un mot de passe identique a été utilisé pour tous les chiers sélectionnés, saisissez ce mot
    de passe pour le premier chier sélectionné et cochez l'option "Le mot de passe est identique pour tous
    les chiers".
8. Passez à l'étape suivante.
    Remarque : Si certains chiers sélectionnés proviennent d'une analyse WINDEV 5.5, précisez le répertoire
    de cette (ou ces) analyse.
9. La connexion est établie. Spéciez l'opération à eectuer :
    Création d'une nouvelle requête SQL.
    Édition d'une requête SQL déjà créée avec WDSQL.
    Lancement de l'outil WDSQL.

Remarque : Si les paramètres de connexion spéciés ne sont pas corrects, la connexion n'est pas établie et
l'assistant de connexion se relance automatiquement.

### Connexion personnelle

WDSQL permet de mémoriser les paramètres de 20 connexions. Ces connexions sont alors appelées
"Connexions personnelles".


Pour mémoriser les paramètres d'une connexion personnelle :

1. Cliquez sur le bouton présent à droite de la liste "Connexion par". La fenêtre des connexions
    personnelles s'ache.
2. Saisissez le nom de la connexion (combo "Nom de la connexion").
3. Spéciez les paramètres de connexion et validez. Ces paramètres sont détaillés dans les opérations 2 à 5
    du paragraphe précédent.

Pour utiliser les paramètres d'une connexion personnelle :

1. Cliquez sur le bouton présent à droite de la liste "Connexion par". La fenêtre des connexions
    personnelles s'ache.
2. Sélectionnez le nom de la connexion (liste "Nom de la connexion") et validez.


#### WINDEV WEBDEV

### Présentation

Lorsque la connexion à la base de données est établie, WDSQL permet de créer diérents types de requêtes
SQL :
Requête de sélection (instruction SELECT) : visualisation d'une sélection d'enregistrements dans la base
de données.
Requête d'insertion (instruction INSERT) : ajout d'enregistrements dans un chier de le base de données.
Requête de modication (instruction UPDATE) : modication des enregistrements d'un chier de la base
de données.
Requête de suppression (instruction DELETE) : suppression des enregistrements d'un chier de la base
de données.

### Créer une requête SQL

Il est possible de créer des requêtes :

```
WINDEV Mobile Autres
```
## WDSQL : Création d'une requête

## SQL


```
Directement depuis la fenêtre principale de WDSQL.
```
```
A l'aide de l'assistant de création de requêtes de WDSQL.
```
Après création, ces requêtes peuvent être :

```
Enregistrées (option "Fichier .. Enregistrer une requête" ou raccourci F4 ou icône ). Le chier créé
est de type ".SQL".
Exécutées.
```
```
Imprimées (cliquez sur l'icône ).
```
```
Modiées directement sous WDSQL.
```
Attention : Une requête créée sous WDSQL ne peut pas être modiée sous WINDEV. Pour utiliser une
requête créée sous WDSQL, il sut de réaliser un copier-coller du code SQL :

```
soit vers une fenêtre de code SQL sous WINDEV,
soit dans le paramètre "Texte de la requête en SQL" de la fonction HExécuteRequêteSQL du WLangage.
```
### Créer une requête SQL directement depuis la fenêtre principale de


### WDSQL

Pour créer une requête directement depuis la fenêtre principale de WDSQL

WDSQL propose diérents moyens pour vous aider dans la création de la requête en SQL :
Visualisation et/ou utilisation des rubriques existantes dans la base de données en cours : cliquez sur
l'icône. Pour plus de détails, consultez Structure d'une base de données.

```
Visualisation et/ou utilisation des diérents mot-clés SQL : cliquez sur l'icône.
```
### Créer une requête SQL à l'aide de l'assistant

Pour l'opération suivante, nous considérons que la connexion à la base de données a été établie.

Pour créer une requête de sélection à l'aide de l'assistant :

1. Sélectionnez l'option "Fichier .. Créer une requête" (ou cliquez sur l'icône ).
2. Dans l'assistant, sélectionnez l'option "Une requête de sélection" et passez à l'étape suivante.
3. Sélectionnez les diérentes rubriques de la requête.
    Remarque : Si la base de données en cours est une base de données Oracle ou SQL Server, il est possible
    de visualiser les tables créées par un utilisateur donné. Il sut de sélectionner l'utilisateur dans la combo
    "Utilisateur".
4. Dénissez si nécessaire les conditions de sélection pour chaque rubrique.
5. Triez si nécessaire les enregistrements selon une ou plusieurs rubriques :
    Dans l'ordre croissant : cliquez dans la colonne "Tri" correspondant à la ou les rubriques de tri.
    L'icône apparaît.
    Dans l'ordre décroissant : cliquez dans la colonne "Tri" correspondant à la ou les rubriques de tri.
    L'icône apparaît.
6. Si l'option "Ne pas acher les doublons" est cochée, chaque enregistrement du résultat de la requête
    sera unique.
    Par exemple, si une requête ache tous les clients ayant passé au moins une commande, les clients
    ayant passé plusieurs commandes n'apparaîtront qu'une seule fois dans le résultat de la requête.
7. Si des rubriques de tri ont été dénies, spéciez l'enchaînement de ces rubriques de tri. Pour plus de
    détails, consultez le paragraphe Dénition de plusieurs rubriques de tri.
8. Validez. Le code SQL de la requête créée s'ache automatiquement dans la fenêtre principale de WDSQL.

Pour l'opération suivante, nous considérons que la connexion à la base de données a été établie.

Pour créer une requête d'insertion à l'aide de l'assistant :

1. Sélectionnez l'option "Fichier .. Créer une requête" (ou cliquez sur l'icône ).


2. Dans l'assistant, sélectionnez l'option "Une requête d'insertion" et passez à l'étape suivante.
3. Sélectionnez le chier de données dans lequel des données vont être insérées. La liste des rubriques du
    chier s'ache automatiquement.
    Remarque : Si la base de données en cours est une base de données Oracle ou SQL Server, il est possible
    de visualiser les tables créées par un utilisateur donné. Il sut de sélectionner l'utilisateur dans la combo
    "Utilisateur".
4. Saisissez les nouvelles valeurs à insérer dans la colonne "Valeur" et validez. Le code SQL de la requête
    créée s'ache automatiquement dans la fenêtre principale de WDSQL.

Pour l'opération suivante, nous considérons que la connexion à la base de données a été établie.

Pour créer une requête de modication à l'aide de l'assistant :

1. Sélectionnez l'option "Fichier .. Créer une requête" (ou cliquez sur l'icône ).
2. Dans l'assistant, sélectionnez l'option "Une requête de modication" et passez à l'étape suivante.
3. Sélectionnez le chier de données dans lequel des données vont être modiées. La liste des rubriques du
    chier s'ache automatiquement.
    Remarque : Si la base de données en cours est une base de données Oracle ou SQL Server, il est possible
    de visualiser les tables créées par un utilisateur donné. Il sut de sélectionner l'utilisateur dans la combo
    "Utilisateur".
4. Saisissez les nouvelles valeurs dans la colonne "Valeur".
5. Dénissez les conditions de sélection pour chaque enregistrement à modier et validez. Le code SQL de la
    requête créée s'ache automatiquement dans la fenêtre principale de WDSQL.

Pour l'opération suivante, nous considérons que la connexion à la base de données a été établie.

Pour créer une requête de suppression à l'aide de l'assistant :

1. Sélectionnez l'option "Fichier .. Créer une requête" (ou cliquez sur l'icône ).
2. Dans l'assistant, sélectionnez l'option "Une requête de suppression" et passez à l'étape suivante.
3. Sélectionnez le chier de données dans lequel des données vont être supprimées. La liste des rubriques
    du chier s'ache automatiquement.
    Remarque : Si la base de données en cours est une base de données Oracle ou SQL Server, il est possible
    de visualiser les tables créées par un utilisateur donné. Il sut de sélectionner l'utilisateur dans la combo
    "Utilisateur".
4. Dénissez les conditions de sélection pour chaque enregistrement à supprimer et validez. Le code SQL de
    la requête créée s'ache automatiquement dans la fenêtre principale de WDSQL.

### Dénition de plusieurs rubriques de tri


Lorsque plusieurs rubriques de tri sont dénies, les tris sont imbriqués. Le tri commence par la première
rubrique du tableau des rubriques de tri.

Par exemple, lors de la création de la requête, dans la fenêtre ci-dessous, le résultat de la requête est trié :

```
tout d'abord par le total TTC des commandes (ordre croissant),
ensuite par la ville des clients (ordre décroissant),
pour nir par le nom des clients (ordre croissant).
```
Dans l'étape suivante de l'assistant, les èches situées à droite de la fenêtre permettent de modier
l'enchaînement des rubriques de tri.

Le code SQL correspondant à cet exemple sera le suivant :

# SELECT CLIENT.NomClient, CLIENT.Ville, COMMANDE.TotalTTC

# FROM CLIENT, COMMANDE

# WHERE CLIENT.Ville LIKE'Paris'

# ORDER BY TotalTTC ASC, Ville DESC, NomClient ASC


#### WINDEV WEBDEV

### Présentation

WDSQL permet d'exécuter toutes les requêtes SQL créées avec WDSQL.

```
Lors de l'exécution de : Résultat :
```
```
Une requête de sélection Le résultat de la requête peut être visualisé :
sous forme d'une table (icône ou option "Exécution
.. Exécuter en mode table").
```
```
sous forme de ches (icône ou option "Exécution ..
Exécuter en mode che").
```
```
Remarque : Le résultat peut également
être exporté et/ou imprimé.
```
```
Une requête d'insertion (icône
```
```
ou indiéremment).
```
```
Les enregistrements sont directement ajoutés.
```
```
Une requête de modication (icône
ou indiéremment).
```
```
Les enregistrements sont directement modiés.
```
```
Une requête de suppression (icône
ou indiéremment).
```
```
Les enregistrements sont directement supprimés.
```
### Exécuter une requête de sélection en mode table

Présentation

Lors de l'exécution d'une requête de sélection en mode table, le résultat de la requête est présenté dans une
table. Cette table permet d'obtenir une vision globale du résultat de la requête.

```
WINDEV Mobile Autres
```
## WDSQL : Exécution d'une requête

## SQL


Par exemple :

Exécuter une requête de sélection en mode table :

Pour exécuter une requête de sélection en mode table :

1. Chargez si nécessaire la requête à exécuter sous WDSQL (option "Fichier .. Charger une requête" ou icône
    ).
2. Sélectionnez l'option "Exécution .. Exécuter en mode table" (ou cliquez sur l'icône ). Le résultat de la
    requête s'ache sous forme de table. Ce résultat peut être exporté et/ou imprimé.

Remarque : La visualisation du résultat sous forme de table :

```
Rechercher un enregistrement : cliquez sur l'icône et saisissez les premières lettres de la valeur
recherchée.
Trier les enregistrements selon une rubrique : cliquez sur l'entête de la colonne à trier.
```
### Exécuter une requête de sélection en mode che

Présentation

Lors de l'exécution d'une requête de sélection en mode che, le résultat de la requête est présenté sous
forme de ches : chaque rubrique de l'enregistrement est visualisée dans son ensemble et il est possible de


se déplacer d'une che à l'autre (grâce aux boutons , ...).

Par exemple :

Exécuter une requête de sélection en mode che

Pour exécuter une requête de sélection en mode che :

1. Chargez si nécessaire la requête à exécuter sous WDSQL (option "Fichier .. Charger une requête" ou icône
    ).
2. Sélectionnez l'option "Exécution .. Exécuter en mode che" (ou cliquez sur l'icône ). Le résultat de la
    requête s'ache sous forme de che. Ce résultat peut être exporté et/ou imprimé.


#### WINDEV WEBDEV

### Présentation

Le résultat d'une requête de sélection peut être au choix :
exporté vers un chier texte, Excel, XML ou Word,
imprimé.

Remarque : Pour les opérations suivantes, nous considérons que le résultat de la requête est aché sous
WDSQL.

### Exporter le résultat d'une requête de sélection

Exporter le résultat de la requête de sélection vers un chier texte

Pour exporter le résultat de la requête de sélection vers un chier texte :

1. Cliquez sur le bouton "Exporter". La fenêtre de sélection du chier texte s'ache.
2. Spéciez le nom et l'emplacement du chier texte (extension ".TXT" par défaut).
3. Choisissez le type de séparateur utilisé entre les diérentes rubriques de chaque enregistrement (option
    "Type") :
       Séparateur : Tabulation : Les rubriques seront séparées par des tabulations.
       Séparateur : Point virgule : Les rubriques seront séparées par des points virgule.
4. Validez. Les enregistrements du résultat de la requête sont automatiquement exportés dans le chier
    texte.

Exporter le résultat de la requête de sélection vers Excel, Word ou XML

Pour exporter le résultat de la requête de sélection vers Excel, Word ou XML :

1. Eectuez un clic droit de la souris sur la table contenant le résultat de la requête.
2. Sélectionnez le mode d'export voulu : Word, Excel ou XML.

```
WINDEV Mobile Autres
```
## WDSQL : Exportation et impression

## du résultat d'une requête SQL


3. Indiquez le nom du chier d'export et validez.

### Imprimer le résultat d'une requête de sélection

Pour imprimer le résultat de la requête de sélection :

1. Cliquez sur le bouton "Imprimer". La fenêtre de sélection des rubriques à imprimer s'ouvre.
2. Spéciez et validez les rubriques à imprimer. Le résultat de la requête est aché dans un aperçu avant
    impression.
3. Cliquez sur l'icône pour imprimer le résultat de la requête.


#### WINDEV WEBDEV

### Présentation

Un script correspond à une suite d'instructions SQL permettant de réaliser une opération précise (création
d'une nouvelle table dans la base de données, insertion multiple d'enregistrements, ...).

Un script est composé de plusieurs lignes. Chaque ligne du script comporte un code SQL pouvant être
exécuté indépendamment.

Un script doit être exécuté ligne par ligne, par un mode Batch.

Remarque : Les opérations suivantes sont possibles uniquement sur les chiers accédés via un provider OLE
DB, un driver ODBC ou un accès natif :

```
Création de la structure d'un chier / table.
Modication de la structure d'un chier / table.
Suppression de la structure d'un chier / table.
```
### Créer un script

Un script peut être créé :
directement depuis la fenêtre principale de WDSQL,
à l'aide de l'assistant de création d'une nouvelle table (script de création de table).

Remarques :

```
Pour enregistrer un script, sélectionnez l'option "Fichier .. Enregistrer une requête" ou cliquez sur l'icône
.
```
```
Pour imprimer le code SQL d'un script, sélectionnez l'option "Fichier .. Imprimer le source de la requête"
ou cliquez sur l'icône.
```
Créer un script directement depuis la fenêtre principale de WDSQL

WDSQL propose diérents moyens pour vous aider dans la création du script en SQL :
Visualisation et/ou utilisation des rubriques existantes dans la base de données en cours : cliquez sur
l'icône. Pour plus de détails, consultez Structure d'une base de données.

```
WINDEV Mobile Autres
```
## WDSQL : Création et exécution d'un

## script


```
Visualisation et/ou utilisation des diérents mot-clés SQL : cliquez sur l'icône.
```
```
Visualisation des diérents types de variables reconnus par la base de données en cours : cliquez sur
l'icône.
```
Créer un script de création d'une nouvelle table dans la base de données en cours

Pour créer un script de création d'une nouvelle table dans la base de données en cours :

1. Sélectionnez l'option "Fichier .. Créer une requête" (ou cliquez sur l'icône ). L'assistant se lance.
2. Sélectionnez l'option "Un script de création d'une nouvelle table". Passez à l'étape suivante.
3. Saisissez le nom de la table à créer (option "Nom de la table").
4. Pour chaque rubrique de la table :
    Saisissez le nom de la rubrique (option "Nom du champ").
    Cliquez sur le bouton "Ajouter".
    Spéciez le type de la rubrique. Les types proposés dépendent de la base de données en cours.
    Spéciez la taille de la rubrique.
    Indiquez si la rubrique doit être indexée.
    Indiquez si la rubrique peut être nulle ou non.
5. Cochez si nécessaire l'option "Générer la commande DROP TABLE" pour générer automatiquement la
    commande "DROP TABLE".
    Rappel : La commande DROP TABLE permet de supprimer une table.
6. Terminez l'assistant. Le code SQL du script de création de table s'ache automatiquement dans la fenêtre
    principale de WDSQL.

### Exécuter un script

Pour exécuter un script :

1. Chargez si nécessaire le script à exécuter sous WDSQL (option "Fichier .. Charger une requête" ou icône
    ).
2. Sélectionnez l'option "Exécution .. Exécuter un script en batch" (ou cliquez sur l'icône ).


#### WINDEV WEBDEV

### Présentation

WDSQL permet de connaître la structure complète de la base de données accédée.

Pour acher la structure de la base de données, cliquez sur l'icône.

Cette fonctionnalité est disponible :

```
sur les bases de données Oracle ou SQL Server,
sur les autres types de bases de données.
```
### Structure d'une base de données Oracle ou SQL Server

Si la base de données en cours est une base de données Oracle ou SQL Server, lors d'un clic sur l'icône

```
, la fenêtre suivante s'ache :
```
Les informations achées sont réparties dans diérents onglets.

```
WINDEV Mobile Autres
```
## WDSQL : Structure d'une base de

## données


Remarque : Les informations achées concernent tous les utilisateurs de la base de données (et non
uniquement l'utilisateur connecté).

```
Onglet Contenu
```
```
Tables Liste des tables de la base de données créées par l'utilisateur sélectionné (dans la
combo "Utilisateur").
Pour chaque table, les informations suivantes sont achées :
Le nom des colonnes.
Le type HFSQL des colonnes. Ce type correspond au type utilisé sous WINDEV.
Le type Oracle des colonnes. Ce type correspond au type des colonnes sous Oracle.
La taille des colonnes.
```
```
Vues Liste des vues de la base de données créées par l'utilisateur sélectionné (dans la combo
"Utilisateur").
Pour chaque vue, les informations suivantes sont achées :
Le nom des colonnes.
Le type HFSQL des colonnes. Ce type correspond au type utilisé sous WINDEV.
Le type Oracle des colonnes. Ce type correspond au type des colonnes sous Oracle.
La taille des colonnes.
```
```
Synonymes Liste des synonymes de la base de données visibles par l'utilisateur sélectionné (dans la
combo "Utilisateur").
Pour chaque synonyme, les informations suivantes sont achées :
La visibilité du synonyme.
Le nom du propriétaire du synonyme.
Le nom du synonyme.
Le nom d'origine de l'objet.
La base de données distante à laquelle l'objet appartient (si nécessaire).
```
```
Index Liste des index de la base de données créés par l'utilisateur sélectionné (dans la combo
"Utilisateur").
Lors de la sélection d'un index, le nom de la (ou des) colonne(s) associée(s) à cet index
s'ache.
```
```
Procédures Liste des procédures stockées, des fonctions et des packages de la base de données
créés par l'utilisateur sélectionné (dans la combo "Utilisateur"). L'icône précédant le
nom d'une procédure indique que la procédure contient au moins une erreur de
compilation.
Il est possible de créer, de modier ou de supprimer une procédure stockée, une
```

```
fonction ou un package.
Pour créer une procédure stockée (une fonction ou un package), il sut de préciser :
Le nom de la procédure stockée (de la fonction ou du package).
Le code de la procédure stockée (de la fonction ou du package).
```
```
La procédure stockée (la fonction ou le package) est automatiquement créée dans la
base de données et compilée. La liste des erreurs détectées à la compilation est
achée si nécessaire.
Exemple d'utilisation d'une procédure : la syntaxe suivante permet d'acher le résultat
d'une fonction :
SELECT <NomFonction>(<Paramètres>) from dual
```
```
Liens
(uniquement
pour les bases
de données
Oracle)
```
```
Liste des diérentes bases de données distantes accessibles depuis la base de données.
Pour chaque base de données, les informations suivantes sont achées :
Le nom du propriétaire de la base de données distante.
Le nom du lien à utiliser pour accéder à la base de données distante.
La chaîne de connexion utilisé par Oracle pour accéder à la base de données
distante.
La visibilité de la base de données distante.
```
```
Exemple : la syntaxe suivante permet de sélectionner les données présentes dans une
table d'une base de données distante :
SELECT * from <NomTable>@<NomDuLlien>
```
```
Utilisateurs Liste des utilisateurs dénis sur la base de données.
Pour chaque utilisateur, la date et l'heure de création de cet utilisateur sont achées.
```
### Structure d'une base de données diérentes de Oracle et SQL Server

Si la base de données en cours n'est pas une base de données Oracle ou SQL Server, lors d'un clic sur l'icône

```
, la fenêtre suivante s'ache :
```

Les informations achées sont réparties dans diérents onglets.

```
Onglet Contenu
```
```
Tables Liste des tables de la base de données.
Pour chaque table, les informations suivantes sont achées :
le nom des colonnes,
le type des colonnes,
la taille des colonnes.
```
```
Vues Liste des vues de la base de données.
Pour chaque vue, les informations suivantes sont achées :
le nom des colonnes,
le type des colonnes,
la taille des colonnes.
```

#### WINDEV WEBDEV

### Présentation

WDSQL permet de convertir la structure d'une base de données HFSQL en script SQL. Ce script pourra
ensuite être exécuté sur une base de données SQL pour créer la base de données correspondante à l'analyse
HFSQL.

Cette option permet par exemple de simplier la création d'une analyse sur une base Oracle à partir d'une
analyse existante au format WINDEV.

Remarque : Pour convertir la structure d'une base de données HFSQL, il est nécessaire d'être connecté à une
base SQL. En eet, cette connexion permet d'identier les types de colonnes reconnus par la base SQL
sélectionnée. Ces types de colonnes seront alors utilisés lors de l'exportation de la base HFSQL vers la base
SQL.

### Comment le faire?

Convertir la structure d'une base de données à partir de WDSQL

Pour convertir la structure d'une base de données à partir de WDSQL :

1. Connectez-vous si nécessaire à une base SQL. Pour plus de détails, consultez
    Connexion à une base de données.
2. Sélectionnez l'option "Outils .. Conversion d'analyse" ou cliquez sur l'icône. L'assistant de
    conversion d'analyse se lance.
3. Sélectionnez l'analyse WINDEV à convertir (chier ".WDD").
4. Spéciez si nécessaire le mot de passe de cette analyse (mot de passe en exécution déni dans la
    description de l'analyse).
5. Sélectionnez le répertoire contenant les chiers de données de l'analyse à convertir et passez à l'étape
    suivante.
6. Sélectionnez les chiers de données à convertir au format SQL et passez à l'étape suivante.
7. Le script de conversion généré s'ache directement dans l'assistant.
    Remarque : Dans l'assistant, il est possible de :
       modier directement ce script,
       rechercher une expression spéciée dans ce script,
       remplacer la ou les expressions trouvée(s) par une autre expression.

```
WINDEV Mobile Autres
```
## WDSQL : Convertir la structure

## d'une base de données HFSQL


8. Validez. Le code SQL du script généré s'ache automatiquement dans la fenêtre principale de WDSQL.

Remarque : Ce script peut ensuite être :

```
modié directement dans la fenêtre principale de WDSQL,
```
```
enregistré (option "Fichier .. Enregistrer une requête" ou icône ),
```
```
exécuté (option "Exécution .. Exécuter un script en batch" ou icône ).
```

