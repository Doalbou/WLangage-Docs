### WEBDEV

## Présentation

L'utilitaire WDDeploy

WDDeploy est un utilitaire permettant de déployer facilement un site Web ou un package de site.

WDDeploy permet de :

```
Déployer un site WEBDEV via un package.
Déployer un webservice SOAP ou REST via un package.
Déployer un site statique.
Déployer un site PHP.
```
Il est également possible de :

```
compresser et regrouper les chiers présents sur un site distant sous forme d'archives.
restaurer les chiers d'un site contenus dans une archive précédemment créée.
```
```
Avertissement
En version 28, cet outil avait pour nom "WDDéploie".
```
## Lancement de WDDeploy

WDDeploy peut être lancé :
sous le volet "Outils", dans le groupe "Utilitaires Web", cliquez sur "WDDeploy".
en lançant directement le programme "WDDeploy.EXE".

## Conditions d'utilisation

WDDeploy est un outil redistribuable. WDDeploy peut être utilisé pour installer n'importe quel site statique
(créé avec WEBDEV ou non).

La licence d'utilisation de WEBDEV s'applique intégralement.

Installation de WDDeploy sur un autre poste

Les chiers nécessaires à l'installation de WDDeploy sont les suivants :

```
WINDEV WINDEV Mobile Autres
```
# Présentation de WDDeploy


WDDeploy.exe

wd300xxx.dll

WDOutil.WDK

WDDeploy_FR.pdf

WDDeploy_EN.pdf


### WEBDEV

## Présentation

WDDeploy permet de :
installer un package de déploiement (généré avec WEBDEV) sur un serveur Web.
installer les chiers d'un site statique ou PHP sur un serveur Web.

## Installer un package de déploiement sur un serveur Web

Lancement direct de WDDeploy

Rappel : la création d'un package de déploiement est une des options de déploiement proposée par
WEBDEV. L'utilisation d'un package de déploiement peut être nécessaire par exemple pour :
déployer un site ou un Webservice à l'identique de celui en production sur un nouveau serveur,
déléguer le déploiement à une équipe infrastructure dédiée.

Lors la création de ce package, certaines informations (les prols) sont soit non connues soit fournies par
l'équipe chargée du déploiement, comme :

```
les adresses de déploiement de serveurs,
les comptes WEBDEV et mots de passe, etc.
```
A la n de l'assistant de création du package, le bouton "Déployer" permet de lancer WDDeploy.

Il est également possible de lancer directement le programme WDDeploy.exe présent dans le sous-répertoire
"Programs" du répertoire d'installation de WEBDEV. Dans ce cas, une fenêtre permet de choisir le type de
déploiement à eectuer. Dans notre cas, il sut de sélectionner "Site WEBDEV".
De la même façon, il est possible de déployer un package d'un Webservice REST ou SOAP.

Contenu du package de déploiement et possibilité d'adaptation du package

Le package de déploiement contient l'ensemble des informations et des données nécessaires au
déploiement du site ou Webservice.
Si certaines informations n'ont pas été renseignées, elles devront être complétées au préalable par
l'équipe chargée du déploiement. Ce package est fourni sous la forme d'une archive zip.
Il est conseillé de nommer cette archive avec un numéro de version et un timestamp et de documenter
l'historique des versions.

Ce chier peut ensuite être transmis au service qui s'occupera du déploiement.

```
WINDEV WINDEV Mobile Autres
```
# WDDeploy : Déployer un package


Le package de déploiement étant fourni sous la forme d'une archive au format zip, il est possible d'en
modier le contenu pour des personnalisations programmées si nécessaire. Par exemple pour un
déploiement spécique dans une infrastructure de pré-production.
Important : le package de déploiement (.zip) utilise un format avancé que l'explorateur Windows ne sait pas
gérer (vous ne verriez pas les chiers du site / Webservice). Pour une édition "visuelle", il est donc nécessaire
d'utiliser WDZip (accessible depuis le menu "Outils" de WINDEV) ou des outils externes (7-Zip, Winzip, etc.).

L'archive contient notamment un chier .wwf de conguration. Ce chier est au format XML et peut donc être
modié par script ou programmation. En cas de modications, il est important de réaliser des tests au
préalable.

Déploiement du package avec WDDeploy : interface interactive

Pour installer un package de déploiement sur un serveur Web via WDDeploy :

1. Sélectionnez si nécessaire le package à traiter (chier ZIP créé par WEBDEV).
2. Créez ou sélectionnez le(s) prol(s) de déploiement correspondant(s) à votre site. Les caractéristiques
    sont saisies dans diérents onglets :
       Nom du prol.
       Lors de la création d'un prol, un nom par défaut est automatiquement donné. Il est possible de
       modier ce nom.
       Onglet "Général" :
          Paramètres du serveur d'application : adresse, compte et mot de passe.
          Paramètres du site : Nom de déploiement, domaine, répertoire des chiers de données HFSQL
          Classic, langues déployées.
       Onglet "Avancé" :
          Mode de transfert des chiers d'installation :
             HTTP (aucune conguration spécique n'est nécessaire).
             FTP : Dans ce cas, les caractéristiques du serveur FTP doivent être indiquées.
          Commandes d'installation : Il est possible d'utiliser :
             le protocole HTTPS (dans ce cas, un certicat SSL doit être installé sur le serveur Web).
             un serveur Proxy pour les connexions HTTP et HTTPS.

```
N'hésitez pas à tester les paramètres spéciés. Ces paramètres peuvent également être exportés ou
importer pour une prochaine utilisation.
Validez. Le prol est créé / modié.
```

3. Vériez (et modiez si nécessaire) les informations du package, disponibles dans les diérents onglets
    de WDDeploy. Ces informations correspondent aux informations saisies dans l'assistant de déploiement :
       l'onglet "Fichiers" liste les diérents chiers contenus dans le package à déployer.
       l'onglet "Paramètres" permet de connaître les paramètres de déploiement du site. Ces informations
       peuvent être modiées.
       l'onglet "Synchro. Données" permet connaître et modier les informations concernant la modication
       automatique des chiers de données.
       l'onglet "Statistiques" permet de congurer la génération du chier de statistiques pour le site.
       l'onglet "Groupware" permet de connaître et modier si nécessaire le répertoire d'indtallation des
       chiers du groupware utilisateur.
4. Cliquez sur "Déployer le site" pour déployer le package.

Déploiement du package avec WDDeploy en ligne de commande

Il est également possible d'eectuer le déploiement en ligne de commande (sans interaction) en indiquant le
chemin de package de déploiement et le nom du prol de déploiement à ajouter :
WDDeploy.exe /DYNAMIQUE="<package déploiement>
/TARGET="nom du prol de déploiement" /AUTO

Détails des paramètres :

```
Paramètre Signication
```
```
/DYNAMIQUE=<package
déploiement .zip>
```
```
Nom et chemin du package de déploiement
```
```
/TARGET=<nom du prol de
déploiement>
```
```
Nom du prol de déploiement utilisé.
```
```
/AUTO Déploiement sans interface.
```

### WEBDEV

## Installer les chiers d'un site statique ou PHP sur un serveur Web

Pour installer les chiers d'un site statique ou PHP sur un serveur Web :

1. Lancez WDDeploy :
    Si le site aché sous WEBDEV est un site statique ou PHP : sous le volet "Outils", dans le groupe
    "Utilitaires Web", cliquez sur "WDDeploy".
    Lancer directement le programme WDDeploy.exe présent dans le sous-répertoire "Programs" du
    répertoire d'installation de WEBDEV. Dans ce cas, une fenêtre permet de choisir le type de
    déploiement à eectuer. Dans notre cas, il sut de sélectionner "Site statique".

```
WINDEV WINDEV Mobile Autres
```
# WDDeploy : Déployer un site

# statique ou PHP


2. Créez ou sélectionnez le prol correspondant à votre site.
    Remarque : Ce prol est créé par un assistant et peut être modié via diérents onglets :
       Informations générales :
          nom du prol.
          Lors de la création d'un prol, un nom par défaut est automatiquement donné. Il est possible de
          modier ce nom.
          emplacement des chiers locaux du site (sous-répertoire "<MonProjet>_WEB" pour un site statique
          WEBDEV).
          adresse du site WEBDEV.
          déploiement d'une seule langue pour le site. Si cette option est sélectionnée, vous pouvez déployer
          votre site uniquement dans une seule des langues gérées par le projet. Attention : dans ce cas,
          votre site ne doit pas utiliser d'options ou de fonctions permettant de changer de langue ou de
          gérer plusieurs langues.
       Connexion
          emplacement des chiers du site déployé (répertoire réseau ou serveur FTP).
          caractéristiques du serveur FTP utilisé pour la mise à jour du site (uniquement lors d'un
          déploiement par FTP).
          Ces caractéristiques sont fournis par l'hébergeur du site.
          Remarque : Pour utiliser un serveur SFTP, saisissez une adresse du type "sftp://<Adresse du
          serveur>".
       Filtres
       Liste des ltres appliqués sur les chiers à installer.
       Les ltres s'appliquent sur les chiers à installer sur le serveur Web. Deux options sont possibles :
          "Ne traiter que les chiers qui correspondent aux ltres" : les chiers installés sur le serveur Web
          seront les chiers concernés par les ltres.
          "Traiter tous les chiers sauf ceux qui correspondent aux ltres" : les chiers installés sur le
          serveur Web seront les chiers non concernés par les ltres.
       Accès distant
       Permet de dénir un accès distant à utiliser avant d'accéder au site FTP (cas par exemple d'utilisation
       d'un modem pour accéder au site).
3. Cliquez sur le bouton "Préparer". WDDeploy prépare la liste des chiers à installer.
    En cas de mise à jour, WDDeploy compare les chiers présents sur le poste de développement et les
    chiers déjà installés.


4. Spéciez si nécessaire les diérentes actions à eectuer lors de la synchronisation sur les diérents
    chiers à installer :
       bouton "Copier en local" : copie les chiers sélectionnés du site distant vers le site local.
       bouton "Copier à distance" : copie les chiers sélectionnés du site local vers le site distant.
       bouton "Eacer à distance" : supprime les chiers sélectionnés du site distant.
       bouton "Ne rien faire" : n'eectue aucune opération sur les chiers sélectionnés.
5. Cliquez sur le bouton "Synchroniser". Les chiers du site sont automatiquement copiés à
    l'emplacement spécié dans le prol.

Remarques :

```
Le bouton "Options" permet de spécier des options de synchronisation des chiers. Pour plus de détails,
consultez les Notes.
Lors de la création d'un nouveau prol, un assistant vous guide dans la saisie des paramètres et propose
des prols pré-congurés pour les principaux hébergeurs.
```
## Compresser et regrouper les chiers d'un site distant sous forme

## d'archive

Pour compresser et regrouper les chiers d'un site distant sous forme d'archive :

1. Lancez WDDeploy : sous le volet "Outils", dans le groupe "Utilitaires Web", cliquez sur "WDDeploy".
2. Cliquez sur le bouton "Sauvegarder".
3. Saisissez le nom de l'archive à créer (chier ".WDZ") et spéciez son répertoire de création. Les chiers
    présents dans le site distant spécié dans le prol sont automatiquement compressés et regroupés dans
    l'archive créé.

## Restaurer les chiers contenus dans une archive

Pour restaurer les chiers contenus dans une archive :

1. Lancez WDDeploy : sous le volet "Outils", dans le groupe "Utilitaires Web", cliquez sur "WDDeploy".
2. Cliquez sur le bouton "Restaurer".
3. Sélectionnez le chier archive (chier ".WDV") à restaurer.
4. Sélectionnez le répertoire dans lequel les chiers contenus dans l'archive doivent être restaurés et
    validez.

## Notes

Les options de WDDeploy sont les suivantes :


"Acher la bulle d'aide sur la table des chiers" : ache une bulle d'aide décrivant pour chaque chier
survolé :

```
le nom et la date et l'heure de création du chier sur le poste de développement.
le nom et la date et l'heure de création du chier sur le poste de déploiement.
```
"Ne pas traiter les sous-répertoires" : ne prend pas en compte les sous-répertoires du site local lors du
déploiement des chiers du site.

"Ne pas proposer de modier le site local, même si les chiers distants sont plus récents" : ne met
pas à jour les chiers distants plus récents sur le poste de développement. Lors de la préparation de la
synchronisation, WDDeploy ne proposera pas de remplacer les chiers locaux par les chiers distants
plus récents.

"Ne pas acher les chiers qui sont déjà synchronisés" : ache uniquement les chiers modiés
depuis la dernière synchronisation.


