### WINDEV WEBDEV

## Présentation

L'utilitaire WDReplic

WDReplic est un utilitaire permettant de gérer la réplication des données entre plusieurs postes utilisant la
même application.

Rappel : La réplication est l'opération permettant de maintenir à jour des bases de données distantes de
structures identiques, et sur lesquelles des opérations diérentes sont eectuées. Les opérations eectuées
sur chacune des bases de données sont reportées sur toutes les autres bases de données.

Attention : Pour utiliser WDReplic, la base de données de l'application doit être congurée pour gérer la
réplication. Pour plus de détails, contactez le fournisseur de votre application (ou l'aide en ligne de WINDEV).

## Fonctionnalités de WDReplic

WDReplic permet de gérer entièrement la réplication des données.

WDReplic permet de :

```
Mettre en place une réplication.
Exécuter une réplication.
Planier une réplication.
Éditer une réplication.
```
## Quand et comment utiliser WDReplic?

WDReplic doit être utilisé :
Pour congurer la réplication.
Pour exécuter la réplication.

Attention : L'utilisation de WDReplic suppose que l'application a été congurée pour gérer la réplication
(modication de l'analyse nécessaire).

Conditions d'utilisation

WDReplic est un outil redistribuable. WDReplic peut être installé avec les applications développées avec
WINDEV ou WEBDEV. La licence d'utilisation de WINDEV ou WEBDEV s'applique intégralement.

```
WINDEV Mobile Autres
```
# WDReplic : Présentation


Lors de la création de la procédure d'installation, WDReplic peut être ajouté aux modules installés avec vos
applications.

Rappel : La procédure d'installation peut être créée :

```
soit à partir de l'assistant. Pour lancer l'assistant, sous le volet "Projet", dans le groupe "Génération",
déroulez "Procédure d'installation" et sélectionnez "Créer la procédure d'installation".
soit à partir de l'éditeur d'installation. Pour lancer l'éditeur d'installation, sous le volet "Outils", dans le
groupe "Utilitaires", cliquez sur "WDInst".
```
Les chiers nécessaires à l'installation de WDReplic sont les suivants :

```
WDReplic.EXE wd300cpl.dll
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
wd300oldb.dll wd300pnt.dll
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
```
WDReplic_FR.pdf WDReplic_EN.pdf
```

### WINDEV WEBDEV

## Vocabulaire lié à la réplication

Avant de mettre en place la réplication, il est nécessaire de connaître le vocabulaire spécique à la
réplication.

## Bases de données

La réplication distingue deux types de bases de données :
La base de données maître
C'est la base de données de référence. Sur cette base de données sont eectuées toutes les mises à jour :
modications eectuées par l'application exécutée sur ce poste,
modications eectuées sur les postes distants et transmises par la réplication.
La base de données abonnée
Cette base de données distante est identique à la base de données "Maître". Sur cette base de données
sont appliquées les modications eectuées par le poste distant. La réplication transmet ces
modications à la base de données "maître".

## Types de réplication

Deux types de réplication peuvent être mises en place :
Réplication mono-directionnelle
Ce type de réplication consiste à eectuer uniquement une mise à jour de la base de données "Maître"
vers les bases de données "Abonnées" ou bien de la base de données "abonnée" vers la base de données
"Maître".
Réplication bi-directionnelle
Ce type de réplication consiste à eectuer une mise à jour de la base de données "Maître" vers les bases
de données "Abonnées" et des bases de données "Abonnées" vers la base de données "Maître".
Durant la réplication abonné-maître, les modications eectuées sur le poste abonné depuis la dernière
réplication seront enregistrées sur le poste maître.
Durant la réplication maître-abonné, les modications eectuées sur le poste maître depuis la dernière
réplication seront enregistrées sur le poste abonné.

## Vocabulaire lié à WDReplic

```
WINDEV Mobile Autres
```
# Vocabulaire lié à la réplication


WDReplic utilise un vocabulaire spécique :
Le scénario de réplication
Le scénario de réplication est un chier SRP contenant la suite d'opérations à réaliser pour eectuer la
réplication.
Par exemple, pour une réplication par support transportable entre le réplica maître et le réplica abonné,
le scénario est constitué :
du chemin du répertoire du réplica maître,
du chemin du réplica transportable (chier d'extension WDZ) qui doit être créé,
du mode d'envoi du réplica transportable et de ses caractéristiques (pour un envoi par FTP ou par
email),
de l'identiant du site abonné concerné par la réplication,
du mode de gestion des conits lors de la réplication (si deux enregistrements ont été modiés sur
deux postes, quelle est la modication prise en compte).
Réplica transportable
Fichier au format ZIP contenant toutes les informations nécessaires à la réplication. Ce chier est créé
lorsque le site maître et le site abonné sont distants et non connecté.
Lors d'une synchronisation par FTP ou par email, WDReplic envoie directement le chier ZIP par le média
spécié.
Identiant du site abonné
Lors de l'initialisation d'un réplica abonné, ce réplica est associé à un identiant (numérique ou chaîne de
caractères). Cet identiant est utilisé lors de la création d'un scénario de réplication par support
transportable.


### WINDEV WEBDEV

## Présentation

La conguration de la réplication comporte plusieurs étapes :

1. Dénition des caractéristiques de la réplication
    Dénition du mode de réplication (bidirectionnelle, monodirectionnelle, ...).
    Dénition du média de réplication (réplica transportable, réseau, ...).
    Sélection du répertoire de travail.
    Sélection de l'analyse et validation des chiers à répliquer.
2. Dénition des diérents éléments (maître, abonnés)
    Dénition du maître.
    Dénition des sites abonnés.
    Dénition de l'espace commun.
3. Création des procédures d'installation

Lorsque toutes ces étapes sont eectuées, la réplication peut être utilisée.

## Comment le faire?

Pour congurer la réplication, WDReplic doit être lancé sur le poste où la base de données du réplica maître
est installé.

Il sut ensuite de cliquer sur "Je souhaite mettre en place une réplication", puis de se laisser guider par
l'assistant :

```
WINDEV Mobile Autres
```
# WDReplic : Mettre en place une

# réplication


Les procédures d'installation

Les procédures d'installation sont des chiers ZIP auto-extractibles à exécuter sur le poste maître et sur les
postes abonnés.


### WINDEV WEBDEV

## Présentation

Selon le type de réplication à réaliser, WDReplic doit être lancé :
Soit sur le poste maître : cas par exemple d'une réplication par réseau ou d'une réplication Maître vers
Abonné par support transportable.
Soit sur le poste abonné : cas par exemple d'une réplication par réseau ou d'une réplication Abonné
vers maître par support transportable.
Soit sur le poste maître et sur le poste abonné : cas par exemple d'une réplication bi-directionnelle par
support transportable.

## Comment utiliser WDReplic?

Conditions d'utilisation

```
WDReplic permet de lancer la réplication :
soit directement : la synchronisation est immédiate
soit en la planiant : la synchronisation est eectuée à la date et à l'heure indiquée.
La description de la réplication (chiers SRP) est automatiquement générée lors de la mise en place de la
réplication. Ces chiers sont automatiquement installés sur les postes maître et / ou abonnés lors de
l'exécution de la procédure d'installation de la réplication.
```
Exécuter une réplication immédiatement

Pour exécuter une réplication immédiatement :

1. Lancez WDReplic sur le poste voulu.
2. Sélectionnez l'option "Je souhaite exécuter une ou des réplication(s) maintenant".
3. Sélectionnez le chier scénario correspondant à la réplication à eectuer.
4. Lancez le scénario (bouton "Exécuter").

Planier la réplication avec WDReplic

Pour planier la réplication avec WDReplic :

1. Lancez WDReplic sur le poste voulu.

```
WINDEV Mobile Autres
```
# WDReplic : Lancer la réplication


2. Sélectionnez l'option "Je souhaite planier une ou plusieurs réplications". L'assistant de planication se
    lance.
3. Cliquez sur le bouton "Ajouter".
4. Spéciez les caractéristiques du scénario et de son exécution : le jour, l'heure et la fréquence d'exécution.
    Sélectionnez le chier scénario correspondant à la réplication à eectuer.
5. Validez. L'exécution du scénario est planiée. Pour que la synchronisation soit eectuée à la date choisie,
    WDReplic doit être exécuté en tâche de fond sur le poste en cours.


