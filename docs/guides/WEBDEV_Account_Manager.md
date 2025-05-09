### WEBDEV

## Présentation

Destiné principalement aux hébergeurs et aux Webmasters, le Gestionnaire de comptes WEBDEV permet
d'aider à héberger plus facilement les sites WEBDEV 2025. Le centre gère bien sur les comptes WEBDEV, mais
également, le compte au niveau du "Serveur Web IIS" (versions 5.xx, 6.xx, 7.xx et 8.xx) et les droits au niveau
du système d'exploitation Windows.

Le Gestionnaire de comptes WEBDEV est installé sur le poste de déploiement (WEBDEV Account
Manager.exe) et fonctionne actuellement uniquement avec Windows et un serveur IIS.

Son utilisation est très simple. Il sut de :

1. Paramétrer les spécicités du serveur. Ce paramétrage sera repris par défaut pour tous les utilisateurs.
2. Créer les comptes de déploiement. Cette création peut être automatisée via l'utilisation d'une
    ligne de commande.

```
Avertissement
En version 28, cet outil avait pour nom "Centre de Contrôle d'hébergement".
```
```
WINDEV WINDEV Mobile Autres
```
# Gestionnaire de comptes WEBDEV


### WEBDEV

## Présentation

Les paramètres d'hébergement dénissent les valeurs par défaut utilisées pour la création de nouveaux
comptes d'hébergement. Ces paramètres sont ensuite modiables à tout moment, lors de la création d'un
compte utilisateur.

Ces paramètres concernent :

```
les diérents répertoires utilisés par les sites WEBDEV,
les groupes Windows,
les comptes utilisateurs,
les bases de données HFSQL Client/Serveur,
les informations sur le moteur WEBDEV.
```
Si le Gestionnaire de comptes WEBDEV n'est pas déjà aché, lancez le Gestionnaire de comptes WEBDEV
depuis le menu "Démarrer" de Windows.

## Les répertoires

Pour congurer les répertoires utilisés par votre serveur :

1. Dans le groupe "Paramètres de l'hébergement", cliquez sur "Répertoires".
    Remarque : Les diérentes options de ce groupe permettent de dénir les paramètres qui seront utilisés
    par défaut pour votre serveur d'hébergement.
2. Choisissez le répertoire racine dans lequel seront créés les sous-répertoires des comptes utilisateurs
    WEBDEV.

```
Utilisez un répertoire local à la machine. Si vous voulez utiliser un répertoire réseau,
indiquez obligatoirement un chemin UNC. L'invité Internet du poste devra avoir accès à
ce chemin sans avoir besoin de s'authentier.
```
```
WINDEV WINDEV Mobile Autres
```
# Paramètres d'hébergement


3. Indiquez :

```
le nom du sous-répertoire des sites WEBDEV (par exemple "Sites").
le nom du sous-répertoire des Webservices SOAP (par exemple "WebservicesSOAP").
le nom du sous-répertoire des Webservices REST (par exemple "WebservicesREST").
le nom du sous-répertoire des serveurs de Websocket (par exemple "ServeursWebSocket").
le nom du sous-répertoire des données des sites WEBDEV (chiers de données HFSQL Classic par
exemple).
le nom du sous-répertoire des sites statiques (par exemple "www").
le nom du sous-répertoire des données d'installation.
```
## Groupes Windows

Chaque compte d'hébergement est associé à deux comptes utilisateurs du système d'exploitation :
un compte pour installer et administrer les sites.
un compte pour exécuter les sites.

Ces deux comptes n'ont pas les mêmes droits.

Il est possible de regrouper tous les comptes d'administration dans un groupe d'utilisateurs et tous les
comptes d'exécution dans un autre groupe.

Vous pouvez donner les noms des groupes à utiliser.

Pour dénir les groupes utilisés :

1. Dans le groupe "Paramètres de l'hébergement", cliquez sur "Groupes Windows".


2. Dénissez dans quels groupes seront aectés les utilisateurs Windows créés pour le déploiement.

```
Pour le déploiement, vous pouvez créer un groupe ou utiliser le groupe standard "Utilisateurs avec
pouvoir".
Pour l'exécution des sites, une bonne pratique consiste à utiliser le groupe "IIS_IUSRS" (sur les versions
de Windows où il existe).
```
3. Cliquez sur le bouton "Appliquer" pour valider vos choix.

Remarque : Tous les groupes dénis sur le système sont listés. Il est nécessaire de créer un groupe
d'utilisateurs avec les droits nécessaires pour que celui-ci apparaisse dans la liste.

Droits d'accès pour l'utilisation d'un site

Pour faire fonctionner le site WEBDEV, un certain nombre de droits d'accès sont nécessaires. Ces droits
concernent l'utilisateur anonyme Internet du serveur (c'est-à-dire le compte Windows qui exécute
WD300AWP.EXE). Le tableau ci-dessus présente un récapitulatif de ces droits.

```
Répertoire Droits
```
```
Répertoire _WEB Lecture
```
```
Répertoire de WEBDEV Lecture/Exécution
```
```
Répertoire des données Lecture/Écriture
```
```
Répertoire du site Lecture
```
```
Base de registre Droits
```
```
HKEY_LOCAL_MACHINE\Software\PC
Soft\WebDev\30.
```
```
Lecture
```
```
Exécutable Mode d'exécution
```

```
WD300AWP.EXE Exécution en mode anonyme en utilisant le compte
invité Internet
```
Droits d'accès pour eectuer une installation distante en mode anonyme

Pour installer et mettre à jour une application à distance en mode anonyme, quelques accès
supplémentaires sont nécessaires :

```
Répertoire Droits
```
```
Répertoire _WEB Lecture/Écriture
```
```
Répertoire de base du compte FTP utilisé pour
l'installation
```
```
Lecture/Écriture
```
```
Répertoire de WEBDEV Lecture/Exécution
```
```
Répertoire des comptes WEBDEV Lecture/Écriture
```
```
Répertoire des données Lecture/Écriture
```
```
Répertoire du site Lecture/Écriture
```
```
Base de registre Droits
```
```
HKEY_LOCAL_MACHINE\Software\PC
Soft\WebDev\30.0\Applications
```
```
Lecture/Écriture
```
```
Exécutable Mode d'exécution
```
```
WD300INSTAWP.EXE Exécution en mode authentié en utilisant
l'authentication de base. Les droits d'exécution
doivent être donnés aux utilisateurs Windows
eectuant l'installation (droits identiques au compte
FTP).
```
Droits d'accès pour une installation distante en mode authentié

Pour installer et mettre à jour une application en mode authentié, il est nécessaire d'aecter des droits à un
deuxième compte.


Le compte doit être un compte Windows ayant les mêmes paramètres que le compte FTP utilisé pour
l'installation distante (automatique dans le cas où le serveur FTP est IIS). Les droits à associer à ce compte
sont les mêmes que dans le tableau ci-dessus.

## Limites des comptes

Un compte utilisateur peut avoir 2 limites :
le nombre maximal de connexions attribué au compte. Ce nombre de connexions devra être réparti entre
les diérents sites WEBDEV du compte.
le nombre de sites associés à un compte.

Pour dénir les limites :

1. Dans le groupe "Paramètres de l'hébergement", cliquez sur "Limites".
2. Indiquez :
    Le nombre maximal de connexions à répartir entre les sites (0 correspond à un nombre illimité),
    Si le nombre de sites associés à un compte doit être limité, ...

## Base HFSQL Client/Serveur

Pour dénir les caractéristiques des serveurs HFSQL Client/Serveur qui pourront être associés à un compte
utilisateur :


1. Dans le groupe "Paramètres de l'hébergement", cliquez sur "Base HFSQL Client/Serveur". Le Gestionnaire
    de comptes WEBDEV permet de dénir les diérents serveurs HFSQL présents sur le serveur. Lors de la
    création d'un compte utilisateur, il sera possible de sélectionner le serveur HFSQL dans lequel les
    données de l'application devront être copiées.
2. Lors de la création d'un serveur HFSQL, les caractéristiques suivantes peuvent être saisies :
    la description,
    l'adresse IP du serveur,
    le port de connexion,
    le login administrateur et son mot de passe.

Remarque : Il est possible de créer ou de supprimer un serveur HFSQL.

Rappel : Ces informations permettent de simplier la création des comptes utilisateurs (surtout lors de la
création de plusieurs dizaines de comptes). Elles ne sont pas obligatoires. Les informations non saisies
pourront être saisies directement lors de la création du compte.

## Caractéristiques du moteur WEBDEV

Le Gestionnaire de comptes WEBDEV permet de connaître rapidement les caractéristiques du moteur
WEBDEV :
Répertoire d'installation.
Répertoire des chiers des comptes utilisateurs.
Répertoire du module AWP.
Informations sur la version du moteur.


Pour obtenir ces informations :

1. Lancez le Gestionnaire de comptes WEBDEV depuis le menu "Démarrer" de Windows.
2. Dans le groupe "Paramètres de l'hébergement", cliquez sur le bouton "Informations".


### WEBDEV

## Présentation

Le Gestionnaire de comptes WEBDEV permet de créer un compte de déploiement. Ce compte pourra être
utilisé pour déployer les sites WEBDEV depuis WEBDEV.

## Créer un nouvel utilisateur

Pour créer un compte de déploiement depuis le Gestionnaire de comptes WEBDEV :

1. Lancez le Gestionnaire de comptes WEBDEV depuis le menu "Démarrer" de Windows.
2. Dans le groupe "Utilisateurs", cliquez sur le bouton "Nouvel utilisateur". L'assistant de création d'un
    nouvel utilisateur se lance. Il sut de suivre les diérentes étapes.
    Remarque : Si vous ne l'avez pas fait, le Gestionnaire de comptes WEBDEV propose de dénir un groupe
    d'administration. Dans cet exemple, répondez "Oui" à la question "Voulez-vous continuer sans ce groupe
    ?".
3. Vous pouvez :
    Créer un compte Windows. Ce compte sera utilisé pour le déploiement et la conguration de vos sites.
    Utiliser un compte Windows existant.
4. Si vous créez un compte Windows, saisissez le nom de l'utilisateur et son mot de passe (vous pouvez
    également générer le mot de passe. Dans ce cas, n'oubliez pas de le noter !).

```
Passez à l'étape suivante de l'assistant.
```
```
WINDEV WINDEV Mobile Autres
```
# Gestion des comptes


5. L'assistant propose de sélectionner des options spéciques WEBDEV associées au compte :

```
Les options (non obligatoires) sont les suivantes :
Ce compte est un compte administrateur WEBDEV : Dans ce cas, ce compte pourra paramétrer les
autres comptes utilisateurs grâce à l'administrateur distant.
Laisser le compte inactif à la création : Dans ce cas, ce compte ne pourra pas être utilisé pour déployer
ou mettre à jour des sites. Ce compte ne permettra pas non plus d'utiliser l'administrateur distant.
```
6. Passez à l'étape suivante.
7. L'assistant propose d'utiliser un compte Windows pour l'exécution des applications. Passez à l'étape
    suivante de l'assistant.
8. Saisissez les informations concernant l'utilisateur. Passez à l'étape suivante.
9. Les répertoires du compte utilisateur sont remplis automatiquement en fonction des données spéciées
    lors du paramétrage du serveur.


10. Passez à l'étape suivante.
11. Indiquez le nombre maximum de connexions autorisées pour le compte, et si nécessaire le nombre
    maximum de site pouvant être installés.
12. Sélectionnez ou indiquez les paramètres du serveur HFSQL Client/Serveur à associer au compte
    utilisateur.
13. L'étape suivante de l'assistant concerne les sites Web virtuels.
    Si vous choisissez de créer un nouveau site virtuel, il sut d'indiquer le nom DNS qui mènera à ce site
    (le DNS doit être conguré en conséquence).
    Si vous choisissez d'utiliser un site virtuel déjà existant, sa conguration sera remplacée.
    Remarque : le répertoire racine du site virtuel va être modié. Si des sites (WEBDEV ou non) sont déjà
    en fonctionnement sur ce même serveur Web virtuel, ils risquent d'être perturbés. Il sera peut-être
    nécessaire de rétablir le répertoire racine initial (par défaut c:\inetpub\wwwroot\).
14. Passez à l'étape suivante.
15. Cette étape permet de spécier si l'accès et le déploiement par FTP doivent être autorisés pour
    l'utilisateur. Si le déploiement est réalisé par HTTP, cette étape n'est pas nécessaire.
16. Passez à l'étape suivante.
17. L'assistant est terminé. Vériez tous les choix. Il est possible de décocher certaines opérations si vous ne
    souhaitez pas que l'assistant les eectue à votre place.
18. Terminez l'assistant. Votre serveur est maintenant prêt à recevoir des sites WEBDEV.

## Modier ou supprimer un compte utilisateur

```
Pour éditer un compte de déploiement depuis le Gestionnaire de comptes WEBDEV :
```
1. Lancez le Gestionnaire de comptes WEBDEV depuis le menu "Démarrer" de Windows.
2. Dans le groupe "Utilisateurs", cliquez sur "Comptes utilisateurs".
3. La liste des comptes utilisateurs s'ache.
    L'édition d'un compte utilisateur est réalisée grâce au bouton "Détails" de chaque compte utilisateur.
    La suppression d'un compte utilisateur est réalisée grâce au bouton "Supprimer" de chaque compte
    utilisateur.


### WEBDEV

## Présentation

Le Gestionnaire de comptes WEBDEV peut être entièrement utilisé en ligne de commande. Il est possible de :
Gérer les comptes de déploiement.
Gérer les sites WEBDEV.
Gérer les webservices (SOAP et REST) et les serveurs de websocket.
Migrer les comptes, les sites et les Webservices.

## Gérer les comptes de déploiement

Fichier de paramètres des comptes de déploiement

Les manipulations des comptes de déploiement WEBDEV sont eectuées à partir d'un chier contenant les
paramètres du compte. Ce chier est un chier texte, d'extension quelconque. Ce chier a la structure
suivante :

[MAIN]
NOM=Durand
PRENOM=Alain
SOCIETE=PCSOFT
CONNEXION=
LOGINOS=Durand

[DIR]
FTP=d:\temp\ftp
APPLI=d:\AppliWW\Durand
FICHIER=d:\DataWW\Durand

Le détail de ces paramètres est le suivant :

```
Section [MAIN]
```
```
NOM Nom de l'utilisateur du compte
```
```
PRENOM Prénom de l'utilisateur du compte
```
```
WINDEV WINDEV Mobile Autres
```
# Manipuler le Gestionnaire de

# comptes WEBDEV en ligne de

# commande


SOCIETE Société de l'utilisateur du compte

CONNEXION Nombre de connexions totales autorisées pour ce compte

EMAIL Adresse email de l'utilisateur du compte

ADRESSE Adresse de l'utilisateur du compte

TELEPHONE Numéro de téléphone de l'utilisateur du compte

DIVERS Remarques supplémentaires

INTERDIT 0 pour un compte activé,

```
1 pour un compte désactivé.
```
ADMIN 2 pour un compte de déploiement administrateur exclusif,

```
1 pour un compte de déploiement administrateur,
0 pour un compte de déploiement.
```
LOGINOS Nom du compte Windows utilisé pour l'installation (déploiement) et
l'administration distante. Le mot de passe associé est celui du compte Windows.

LOGINOSIUSR Nom du compte Windows utilisé pour l'exécution des sites et webservices. Le
mot de passe associé est celui du compte Windows.

PWDOS Mot de passe du compte Windows utilisé pour l'installation (déploiement) et
l'administration distante. Ce mot de passe est utilisé uniquement en mode
cluster.

PWDOSIUSR Mot de passe du compte Windows pour l'exécution des sites et webservices. Ce
mot de passe est utilisé uniquement en mode cluster.

Section [DIR]

FTP Répertoire utilisé pour le transfert par FTP.

APPLI Répertoire des applications et sites WEBDEV associées à ce compte.

FICHIER Répertoire des chiers de données des applications et sites WEBDEV associées à
ce compte.

WEBSERVICE Répertoire des Webservices SOAP associés à ce compte.

WEBSERVICEREST Répertoire des Webservices REST associés à ce compte.

SERVEURSWEBSOCKET Répertoire des serveurs Websocket associés à ce compte.


```
Section [HFCS1] Cette section est optionnelle. Elle permet de décrire le serveur HFSQL dans le cas
d'une utilisation d'une base HFSQL Client/Serveur.
```
```
SERVEUR Adresse IP du serveur HFSQL
```
```
PORT Port du serveur HFSQL
```
```
LOGIN Login de l'utilisateur de la base de données HFSQL Client/Serveur
```
```
PASSE Mot de passe de l'utilisateur de la base de données HFSQL Client/Serveur
```
```
BASE Base de données HFSQL Client/Serveur
```
Créer un compte de déploiement WEBDEV

Pour créer un nouveau compte de déploiement WEBDEV à l'aide d'une ligne de commande et d'un chier de
paramètres :

1. Créez un chier contenant les paramètres du compte à créer.
2. Lancez CCHebergement avec la ligne de commande suivante :
    WEBDEV Account Manager.exe /CREATEUSER /PARAM="<Chemin complet du chier de paramètres>"

Remarque : Le mot de passe est celui du compte Windows.

Attention : Le chier de paramètres n'est PAS détruit à la n de la création du compte.

Modier un compte de déploiement WEBDEV

Pour modier un compte de déploiement WEBDEV à l'aide d'une ligne de commande et d'un chier de
paramètres :

1. Créez un chier contenant les paramètres du compte à modier.
2. Lancez CCHebergement avec la ligne de commande suivante :
    WEBDEV Account Manager.exe /MODUSER /PARAM="<Chemin complet du chier de paramètres>"

Les paramètres non renseignés dans le chier de paramètres ne sont pas modiés.

Attention : Le chier de paramètres n'est PAS détruit à la n de la création du compte.

Supprimer un compte de déploiement

Pour supprimer un compte à l'aide d'une ligne de commande, utilisez la syntaxe suivante :
WEBDEV Account Manager.exe /DELETEUSER /PARAM="<LOGINOS>"

Lire les informations concernant un compte de déploiement

Pour lire les informations concernant un compte à l'aide d'une ligne de commande, utilisez la syntaxe
suivante :


WEBDEV Account Manager.exe /INFOUSER /PARAM="<Chemin complet du chier de paramètres>" /USER="
<LOGINOS>"

Le chier de paramètres est créé avec les informations concernant le compte utilisateur identié par son
LOGINOS.

Obtenir la liste des comptes de déploiement

Pour lire les informations concernant les diérents comptes de déploiement à l'aide d'une ligne de
commande, utilisez la syntaxe suivante :

WEBDEV Account Manager.exe /LISTUSER /PARAM="<Chemin complet du chier de paramètres>"

Le chier de paramètres est créé avec les informations concernant les diérents comptes utilisateur.

## Gestion des applications

Supprimer une application

Pour supprimer une application ou un site WEBDEV à l'aide d'une ligne de commande, utilisez la syntaxe
suivante :

WEBDEV Account Manager.exe /DELETEAPP /APP="<Nom de l'application>"

Attribution d'une application à un compte de déploiement WEBDEV

Pour attribuer une application ou un site WEBDEV à un compte de déploiement WEBDEV à l'aide d'une ligne
de commande, utilisez la syntaxe suivante :

WEBDEV Account Manager.exe /ATTRIBAPP /APPLI="<Nom de l'application>" /USER="<Login>"

Liste des applications d'un compte de déploiement

Pour lister les applications d'un compte de déploiement à l'aide d'une ligne de commande, utilisez la syntaxe
suivante :

WEBDEV Account Manager.exe /LISTAPPUSER /PARAM="<Fichier Liste>" /USER="<Login>"

Les applications sont listées dans le chier <Fichier Liste>.

Liste des applications WEBDEV non attribuées

Pour obtenir la liste des applications non attribuées à l'aide d'une ligne de commande, utilisez la syntaxe
suivante :

WEBDEV Account Manager.exe /LISTAPPFREE /PARAM="<Fichier Liste>"

Les applications sont listées dans le chier <Fichier Liste>.


## Gestion des Webservices (SOAP et REST) et des serveurs de Websockets

Supprimer un Webservice (SOAP ou REST) ou un serveur de Websocket

```
Pour supprimer un Webservice SOAP à l'aide d'une ligne de commande, utilisez la syntaxe suivante :
WEBDEV Account Manager.exe /DELETEWEBSERVICE /WEBSERVICE="<Nom du Webservice>"
Pour supprimer un Webservice REST à l'aide d'une ligne de commande, utilisez la syntaxe suivante :
WEBDEV Account Manager.exe /DELETEWEBSERVICEREST /WEBSERVICEREST="<Nom du Webservice
REST>"
Pour supprimer un serveur de Websocket à l'aide d'une ligne de commande, utilisez la syntaxe suivante :
WEBDEV Account Manager.exe /DELETESERVEURWEBSOCKET /SERVEURWEBSOCKET="<Nom du serveur
de Websocket>"
```
Attribution d'un Webservice (SOAP ou REST) ou un serveur de Websocket à un compte de déploiement
WEBDEV

```
Pour attribuer un Webservice SOAP à un compte de déploiement WEBDEV à l'aide d'une ligne de
commande, utilisez la syntaxe suivante :
WEBDEV Account Manager.exe /ATTRIBWEBSERVICE /WEBSERVICE="<Nom du Webservice>" /USER="
<Login>"
Pour attribuer un Webservice REST à un compte de déploiement WEBDEV à l'aide d'une ligne de
commande, utilisez la syntaxe suivante :
WEBDEV Account Manager.exe /ATTRIBWEBSERVICEREST
/WEBSERVICEREST="<Nom du Webservice REST>" /USER="<Login>"
Pour attribuer un serveur de Websocket à un compte de déploiement WEBDEV à l'aide d'une ligne de
commande, utilisez la syntaxe suivante :
WEBDEV Account Manager.exe /ATTRIBSERVEURWEBSOCKET
/SERVEURWEBSOCKET="<Nom du serveur de Websocket>"
/USER="<Login>"
```
Liste des Webservices (SOAP ou REST) ou les serveurs de Websocket d'un compte

```
Pour lister les Webservices SOAP d'un compte de déploiement à l'aide d'une ligne de commande, utilisez
la syntaxe suivante :
WEBDEV Account Manager.exe /LISTWEBSERVICEUSER /PARAM="<Fichier Liste>" /USER="<Login>"
Pour lister les Webservices REST d'un compte de déploiement à l'aide d'une ligne de commande, utilisez la
syntaxe suivante :
WEBDEV Account Manager.exe /LISTWEBSERVICEUSERREST /PARAM="<Fichier Liste>" /USER="<Login>"
Pour lister les serveurs de Websocket d'un compte de déploiement à l'aide d'une ligne de commande,
utilisez la syntaxe suivante :
WEBDEV Account Manager.exe /LISTSERVEURSWEBSOCKETUSER /PARAM="<Fichier Liste>" /USER="
<Login>"
```

Les webservices et serveurs de websocket sont listés dans le chier <Fichier Liste>.

Liste des Webservices (SOAP ou REST) ou les serveurs de Websocket non attribués

```
Pour obtenir la liste des Webservices SOAP non attribués à l'aide d'une ligne de commande, utilisez la
syntaxe suivante :
WEBDEV Account Manager.exe /LISTWEBSERVICEFREE /PARAM="<Fichier Liste>"
Pour obtenir la liste des Webservices REST non attribués à l'aide d'une ligne de commande, utilisez la
syntaxe suivante :
WEBDEV Account Manager.exe /LISTWEBSERVICERESTFREE /PARAM="<Fichier Liste>"
Pour obtenir la liste des serveurs de Websocket non attribués à l'aide d'une ligne de commande, utilisez la
syntaxe suivante :
WEBDEV Account Manager.exe /LISTSERVEURSWEBSOCKET /PARAM="<Fichier Liste>"
```
Les webservices et serveurs de websocket sont listés dans le chier <Fichier Liste>.

## Migrer les comptes, les sites et les Webservices

Migrer un compte utilisateur

Pour migrer un compte utilisateur à l'aide d'une ligne de commande, utilisez la syntaxe suivante :

WEBDEV Account Manager.exe /MIGREUSER [/VERSIONMIGRATION=<Numéro de version à migrer>]
[/MIGRERESETUSER]

Le paramètre <Numéro de version à migrer> correspond au numéro de version du compte à migrer.
Si ce paramètre correspond à *, toutes les versions précédentes seront migrées, de la version la plus récente
vers la version la plus ancienne. Si le compte existe déjà, il n'est pas remplacé.
Si ce paramètre n'est pas précisé, seule la version précédente la plus récente est migrée.

Le mot-clé MIGRERESETUSER permet de supprimer les utilisateurs de la version actuelle avant la migration.
Ce mot-clé permet notamment de supprimer le compte "admin" créé automatiquement à l'installation.

Migrer un site WEBDEV

Pour migrer un site WEBDEV à l'aide d'une ligne de commande, utilisez la syntaxe suivante :

WEBDEV Account Manager.exe /MIGREAPP [/VERSIONMIGRATION=<Numéro de version à migrer>]

Le paramètre <Numéro de version à migrer> correspond au numéro de version du site à migrer.
Si ce paramètre correspond à *, toutes les versions précédentes seront migrées, de la version la plus récente
vers la version la plus ancienne. Si le site existe déjà, il n'est pas remplacé.
Si ce paramètre n'est pas précisé, seule la version précédente la plus récente est migrée.

Migrer un Webservice SOAP et REST


Pour migrer un Webservice à l'aide d'une ligne de commande, utilisez la syntaxe suivante :

WEBDEV Account Manager.exe /MIGREWEBSERVICE [/VERSIONMIGRATION=<Numéro de version à migrer>]

WEBDEV Account Manager.exe /MIGREWEBSERVICEREST [/VERSIONMIGRATION=<Numéro de version à
migrer>]

Le paramètre <Numéro de version à migrer> correspond au numéro de version du Webservice à migrer.
Si ce paramètre correspond à *, toutes les versions précédentes seront migrées, de la version la plus récente
vers la version la plus ancienne. Si le webservice existe déjà, il n'est pas remplacé.
Si ce paramètre n'est pas précisé, seule la version précédente la plus récente est migrée.

Migrer un serveur de Websocket

Pour migrer un serveur de Websocket à l'aide d'une ligne de commande, utilisez la syntaxe suivante :

WEBDEV Account Manager.exe /MIGRESERVEURSWEBSOCKET [/VERSIONMIGRATION=<Numéro de version à
migrer>]

Le paramètre <Numéro de version à migrer> correspond au numéro de version du serveur de websocket à
migrer.
Si ce paramètre correspond à *, toutes les versions précédentes seront migrées, de la version la plus récente
vers la version la plus ancienne. Si le serveur de websocket existe déjà, il n'est pas remplacé.
Si ce paramètre n'est pas précisé, seule la version précédente la plus récente est migrée.

Migrer tout

Pour migrer les utilisateurs, les sites et les Webservices à l'aide d'une ligne de commande, utilisez la syntaxe
suivante :

WEBDEV Account Manager.exe /MIGREALL
[/VERSIONMIGRATION=<Numéro de version à migrer>] [/MIGRERESETUSER]

Le paramètre <Numéro de version à migrer> correspond au numéro de version du compte à migrer.
Si ce paramètre correspond à *, toutes les versions précédentes seront migrées, de la version la plus récente
vers la version la plus ancienne. Si le compte, le site ou le Webservice existe déjà, il n'est pas remplacé.
Si ce paramètre n'est pas précisé, seule la version précédente la plus récente est migrée.

Le mot-clé MIGRERESETUSER permet de supprimer les utilisateurs de la version actuelle avant la migration.
Ce mot-clé permet notamment de supprimer le compte "admin" créé automatiquement à l'installation.


### WEBDEV

## Présentation

Le Gestionnaire de comptes WEBDEV permet de simplier l'import et l'export de la conguration du Serveur
d'Application WEBDEV. Il est ainsi possible de déplacer un serveur ou de copier sa conguration.

## Comment le faire?

Pour exporter le Serveur d'Application WEBDEV :

1. Lancez le Gestionnaire de comptes WEBDEV.
2. Dans le groupe "Déplacement du serveur", cliquez sur "Export...".
3. Dans l'assistant d'exportation, sélectionnez les comptes à exporter. Passez à l'étape suivante.
4. Sélectionnez les sites à exporter, avec ou sans les données
    Remarque : L'export d'un site force l'export du compte de déploiement associé. Passez à l'étape suivante.
5. Sélectionnez les Webservices SOAP à exporter, avec ou sans les données. Passez à l'étape suivante.
6. Sélectionnez les Webservices REST à exporter, avec ou sans les données. Passez à l'étape suivante.
7. Sélectionnez les serveurs de Websocket à exporter, avec ou sans les données. Passez à l'étape suivante.
8. Indiquez les congurations spéciques à rechercher et à réappliquer : droits sur les clés de registre,
    vérication des droits sur les chiers, vérication de la conguration de IIS. Passez à l'étape suivante.
9. Indiquez le chier "zip" destination, vériez les diérents éléments sélectionnés et validez l'export.

Pour importer le Serveur d'Application WEBDEV :

1. Lancez le Gestionnaire de comptes WEBDEV.
2. Dans le groupe "Déplacement du serveur", cliquez sur "Import...".
3. Dans l'assistant d'importation, indiquez le chier de conguration "zip" précédemment créé lors de
    l'export.
4. Validez l'importation.

```
WINDEV WINDEV Mobile Autres
```
# Import et export d'un Serveur

# d'application WEBDEV


### WEBDEV

## Présentation

Les comptes de déploiement sont nécessaires à l'installation d'un site dynamique WEBDEV sur un serveur
Web. L'import de comptes depuis une version antérieure permet d'utiliser dans la version actuelle les
comptes créés avec une version précédente.

Pour être utilisées avec une version supérieure du moteur WEBDEV, les informations des sites, Webservices
(SOAP et REST), serveurs de WebSocket doivent être également migrées. Par exemple, pour utiliser un site
créé avec WEBDEV 27 avec un moteur WEBDEV en version 2025, il est nécessaire d'importer les informations
concernant ce site.

Le Gestionnaire de comptes WEBDEV permet d'importer des congurations provenant de versions
antérieures :

```
Comptes de déploiement,
Sites,
Webservices SOAP,
Webservices REST,
Serveurs de Websocket.
```
Pour importer les éléments provenant de versions antérieures :

1. Lancez le Gestionnaire de comptes WEBDEV.
2. Dans le groupe "Conguration", déroulez "Import depuis les versions antérieures" et sélectionnez l'option
    correspondant aux éléments à importer.
3. Import des comptes :
    Dans l'assistant qui se lance, sélectionnez :
       La version de WEBDEV à partir de laquelle les éléments doivent être importés,
       La liste des comptes utilisateurs à importer.
4. Import des sites, Webservices (SOAP et REST), serveurs de WebSocket :
    Sélectionnez les éléments à importer dans la liste qui est achée. Les sites, Webservices (SOAP et REST),
    serveurs de Websocket non importés ne fonctionneront pas avec une version supérieure du Serveur
    d'application WEBDEV.
    Remarque : Un site créé avec une version inférieure de WEBDEV peut être utilisée avec un moteur
    WEBDEV 2025. Il est cependant nécessaire de migrer les informations liées au site.

```
WINDEV WINDEV Mobile Autres
```
# Import depuis des versions

# antérieures


5. Validez l'importation des éléments.
    Les comptes importés peuvent désormais être manipulés avec le Gestionnaire de comptes WEBDEV.


