## WEBDEV

WEBDEV est un environnement complet de développement dédié à Internet et Intranet. WEBDEV est idéal pour
développer des sites Internet et Intranet qui nécessitent ou non un accès à une base de données.
La technologie utilisée assure un fonctionnement des sites sous tous les navigateurs du marché, quelle que soit
leur version, qu'ils fonctionnent sur PC, MAC, Android, iOS, etc.
Cette technologie permet également une utilisation des sites avec tous les serveurs Linux ou Windows du
marché : Apache, IIS, etc.

WEBDEV est constitué de :

```
WEBDEV Version Développement :
Installée sur le poste de développement, cette version permet de développer un site WEBDEV et de le tester
en local.
Serveur d'application WEBDEV :
Installée sur un poste serveur HTTP chez l'hébergeur, cette version permet de déployer un site dynamique
WEBDEV (site avec base de données). Le site WEBDEV peut être utilisé par tous les internautes.
```
Remarque : Pour déployer un site statique (qui n'utilise pas de données), le serveur d'application WEBDEV n'est
pas nécessaire.

Les possibilités du serveur d'application WEBDEV pour Linux

Le serveur d'application WEBDEV doit être installé sur un poste serveur (chez l'hébergeur ou sur un poste
serveur Intranet). Grâce au serveur d'application WEBDEV :
Les internautes peuvent utiliser des sites dynamiques WEBDEV.
L'administrateur du serveur peut :
Gérer et congurer les diérents sites dynamiques WEBDEV présents sur le serveur.
Congurer les comptes Utilisateur associés à chaque responsable de sites.
Contrôler l'installation et la mise à jour de sites dynamiques WEBDEV à distance (par FTP ou HTTP).
Le responsable de sites WEBDEV peut :
Installer ou mettre à jour ses sites dynamiques à distance (par FTP ou par HTTP).
Modier la conguration de ses diérents sites dynamiques WEBDEV.

Avertissement
Vous devez maîtriser l'installation de logiciel sur Linux.
Si vous ne connaissez pas Linux, vous devez d'abord vous former à Linux avant de réaliser l'installation de ce
logiciel.

```
WINDEV WINDEV Mobile Autres
```
# Présentation du Serveur

# d'application WEBDEV Linux


PC SOFT assure le support sur ses logiciels (via le Support technique Gratuit ou le service Assistance Directe
selon les cas).
PC SOFT n'assure donc PAS de support technique gratuit sur les systèmes d'exploitation (ni sur Windows, ni sur
Linux).
Si vous nécessitez un support technique sur un logiciel qui n'est pas édité par PC SOFT, contactez l'éditeur du
logiciel concerné.

Sommaire

Ce document présente les éléments suivants :
Installer un serveur d'application
Créer les comptes utilisateur
Installer un site WEBDEV
Dépannage
Annexe 1 : Vocabulaire de WEBDEV
Annexe 2 : Vérication du serveur
Annexe 3 : Fichier de conguration
Annexe 4 : Modules de WEBDEV
Annexe 5 : Conguration du serveur


## WEBDEV

Présentation

L'installation du serveur d'application WEBDEV sur un serveur Linux 64 bits doit être réalisée en plusieurs
étapes :
Vérication des éléments installés sur le serveur Linux.
Installation du serveur d'application WEBDEV 64 bits pour Linux.
Vérication de l'installation du serveur d'application.
Conguration des utilisateurs et des droits pour le déploiement d'applications WEBDEV.

Remarque : Seule une version 64 bits peut être installée.

Vérication des éléments installés sur le serveur Linux

Pour fonctionner correctement, le serveur d'application WEBDEV pour Linux nécessite :
la présence du serveur Apache. Ce serveur HTTP doit bien entendu fonctionner correctement. Pour vérier
son fonctionnement, il sut de lancer un explorateur Web depuis un autre poste et de saisir l'adresse
"http://<Nom du serveur>".
Remarque : pour installer le serveur d'application WEBDEV pour Linux, il est également nécessaire de
connaître :
le nom et le chemin du chier de conguration du serveur Apache (par exemple :
/etc/httpd/conf/http.conf).
le nom et le chemin du script permettant de recharger la conguration d'apache (par exemple :
/usr/sbin/apachectl -k graceful).
la présence optionnelle d'un serveur FTP (gérant les connexions avec mot de passe).
la présence de la librairie libstdc++ (librairie libstdc++-libc6.2-2.so.3).
Remarque : si un programme bloque l'utilisation de cette librairie, il est nécessaire de le désactiver.
la présence de la librairie QT 4.5 minimale. Cette librairie est nécessaire par exemple pour l'utilisation des
dessins en Linux.

La vérication de ces éléments doit être réalisée avant l'installation de WEBDEV pour Linux.
Vous trouverez dans le chapitre Annexe 2 : Vérication du serveur, le mode opératoire pour eectuer ces
vérications sur les distributions Linux les plus courantes.

Installation du Serveur d'application WEBDEV pour Linux

```
WINDEV WINDEV Mobile Autres
```
# Installer un serveur d'application

# WEBDEV pour Linux


Pour installer le serveur d'application WEBDEV pour Linux, vous pouvez :
soit exécuter sur le serveur Linux le programme "WebDev_Install64" depuis le package d'installation.
soit copier le contenu du package d'installation sur le serveur Linux et exécuter le programme
"WebDev_Install".

Remarque : il est nécessaire d'avoir les droits d'exécution pour exécuter ce programme, sinon le message
"Permission non accordée" apparaît. Pour donner les droits d'exécution, vous devez saisir la ligne suivante :
chmod +x WebDev_Install

Les grandes étapes de l'installation sont les suivantes :

1. Sélectionnez la langue d'installation. Par défaut, l'écran est aché dans la langue du poste d'installation.


2. Acceptez la licence :

```
Pour valider cet écran, il est nécessaire de faire déler entièrement le texte de la licence avec les èches
haut/bas.
```

3. Vériez les pré-requis :


4. Indiquez si le serveur de réplication doit être installé :
5. Saisissez la clé d'activation.


6. Sélectionnez le répertoire d'installation :

```
Il est conseillé de conserver le répertoire proposé.
```

7. Indiquez les paramètres nécessaires à l'installation du serveur d'application WEBDEV pour Linux :

```
le chemin du chier de conguration d'Apache. Pour connaître le nom et le chemin de ce chier, consultez
le chapitre Annexe 2 : Vérication du serveur.
Si le chemin indiqué n'est pas correct, un message d'erreur est aché.
la ligne de commande permettant de recharger la conguration d'Apache après l'ajout d'un alias (cette
opération est eectuée automatiquement lors de l'installation des sites WEBDEV par FTP).
la possibilité d'autoriser le déploiement des sites de versions antérieures.
```

8. Indiquez le nom du groupe Unix correspondant au groupe des administrateurs du serveur d'application
    WEBDEV. Le groupe proposé par défaut est webdevadmin.

```
Si le groupe n'existe pas, il sera automatiquement créé.
```
9. Indiquez également le nom et le mot de passe du premier compte de déploiement. Ce compte est le compte
    Utilisateur utilisé pour se connecter au sites d'administration. il permet également de déployer des sites et
    des webservices. Si ce compte n'existe pas, il sera créé : dans ce cas, conservez bien les caractéristiques du
    compte. Si ce compte existe, le mot de passe spécié dans cet écran ne sera pas pris en compte.


10. Validez l'installation du serveur d'application.
11. L'installation est terminée. Le compte rendu de l'installation est aché.

```
Vérication de l'installation du serveur d'application
Après l'installation du serveur d'application WEBDEV pour Linux, il est conseillé de vérier les points suivants.
```
```
Vérication du serveur Apache
Cette vérication doit être eectuée si l'installation s'est terminée correctement ou si l'installation s'est terminée
avec l'erreur "Cong-broken".
Pour plus de détails sur les diérents points à vérier, consultez Annexe 2 : Vérication du serveur.
```
```
Test depuis un navigateur sous Windows
Pour tester le bon fonctionnement du serveur d'application WEBDEV pour Linux :
```

1. Ouvrez un navigateur Internet.
2. Saisissez l'adresse suivante :
    [http://<Adresse](http://<Adresse) IP Serveur>/WD300AWP/WD300AWP/version
    où "Adresse IP Serveur" correspond à l'adresse IP du poste serveur Linux.
3. Le navigateur ache alors quelques lignes indiquant la version de WEBDEV installée. Par exemple :
    WebDev 30.0 Linux
    Copyright © PC SOFT 1993-
    WD300AWP 30.00Af VI:
    WD300session 30.00Al VI:30-300052g
    WD300admind 30.00Am VI:30-300052g
    (TST) 1303667-1699876806-1394533-YM

Test de l'administrateur distant

L'administrateur distant est l'application permettant de gérer les comptes utilisateurs et les sites WEBDEV sur le
serveur. Pour tester le fonctionnement de l'administrateur distant :

1. Ouvrez un navigateur Internet.
2. Saisissez l'adresse suivante :
    [http://<Adresse](http://<Adresse) IP Serveur>/WDAdminWeb

```
où "Adresse IP Serveur" correspond à l'adresse IP du poste serveur Linux.
Attention : la casse (majuscules / minuscules) de cette adresse doit être scrupuleusement respectée. En cas
d'erreur de connexion, vériez tout d'abord la casse et l'orthographe utilisées.
```
3. L'administrateur demande alors une identication. Entrez le login et le mot de passe spéciés lors de
    l'installation du Serveur d'Application WEBDEV.

Problèmes pouvant être rencontrés lors du test de l'administrateur

```
Une erreur 403 s'ache au lancement de l'administrateur distant :
Cause : La version d'Apache installée a placé une clause "deny from all" dans son chier de conguration.
Solution :
Ajouter dans le chier de conguration de Apache, une clause <Directory> juste avant la dénition du
ScriptAlias :
<Directory "/usr/local/WebDev/30.0/AWP">
allow from all
</Directory>
ScriptAlias /WD300AWP/ "/usr/local/WebDev/30.0/AWP"
```
```
Les images ne sont pas achées dans l'administrateur distant :
Si vous récupérez l'URL de l'image mal achée (Option "Propriétés" du menu contextuel de l'image), et si
vous la testez directement sous le navigateur, l'erreur 403 s'ache.
Cause : L'alias _WEB a bien été déni pour le serveur Apache, mais une option d'Apache verrouille son accès.
Solution : Pour chaque répertoire d'alias, il faut dénir une directive <Directory> dans le chier de
conguration d'Apache.
```

En cas de dysfonctionnement de l'administrateur distant ou des sites WEBDEV

Il est conseillé d'eectuer les opérations suivantes :

```
Consulter les "logs" systèmes (par exemple /var/log/messages). Ces chiers peuvent contenir des
informations sur les erreurs rencontrées (notamment en cas de problèmes de droits).
Relancer le serveur d'application. Il est possible d'utiliser la commande suivante :
killall WD300admind
/etc/init.d/WEBDEV30 restart
Rebooter le serveur si nécessaire.
```
Augmenter le nombre de connexions simultanées autorisées

Le nombre de connexions supportées par le serveur d'application WEBDEV dépend des ressources systèmes
suivantes :
le nombre de sémaphores.
le nombre de segments de mémoire partagée.
la taille minimale de la mémoire partagée.

Nombre de sémaphores

Le serveur d'application WEBDEV utilise un nombre de sémaphores proportionnel au nombre de connexions
maximum simultanées acceptées.
Pour connaître le nombre de sémaphores maximum disponibles, exécutez la ligne de commande suivante :
/sbin/sysctl kernel.sem
Cette ligne de commande renvoie une suite de nombre dont le dernier correspond au nombre de sémaphores
actuels (par exemple 250 32000 32 170 ce qui correspond à environ 32 connexions). Le nombre de sémaphores
nécessaire pour gérer n sessions est connu par la formule suivante : s = 4 +4 * n
Par exemple, pour gérer 100 connexions simultanées, le nombre minimum de sémaphores nécessaires est
donc : 4 + 4 * 100 = 404

Pour modier le nombre de sémaphores :

1. Editez le chier/etc/sysctl.conf avec un éditeur de texte. Par exemple, pour éditer un chier, il sut d'utiliser
    la ligne de commande suivante :
    emacs /etc/sysctl.conf

```
Remarque : il est également possible d'éditer le chier avec :
vi /etc/sysctl.conf
```
2. Rajoutez ou modiez la ligne correspondant à l'entrée "kernel.sem" en indiquant le nouveau paramétrage :
    kernel.sem = xxx xxxxx xx 404

```
où les x représentent les chires précédemment renvoyés.
```

3. Pour prendre en compte ces nouveaux paramètres, utilisez la ligne de commande suivante :
    /sbin/sysctl -p

Nombre de segments de mémoire partagée

Le nombre de segments de mémoire partagée pour gérer n connexions doit être de 4 + n.

Pour connaître le nombre de segments de mémoire partagée, exécutez la ligne de commande suivante :
/sbin/sysctl kernel.shmmni

Pour modier le nombre de segments de mémoire partagée :

1. Editez le chier/etc/sysctl.conf avec un éditeur de texte.
    Par exemple, pour éditer un chier, il sut d'utiliser la ligne de commande suivante :
    emacs /etc/sysctl.conf

```
Remarque : il est également possible d'éditer le chier avec :
vi /etc/sysctl.conf
```
2. Rajoutez ou modiez la ligne correspondant à l'entrée "kernel.shmmni" en indiquant le nouveau
    paramétrage :
    kernel.shmmni = xxx

```
où xxx correspond au nouveau paramétrage.
```
3. Pour prendre en compte ces nouveaux paramètres, utilisez la ligne de commande suivante :
    /sbin/sysctl -p

Taille minimale de la mémoire partagée

La taille minimale de la mémoire partagée doit être également calculée en fonction du nombre de connexions.
Le calcul est le suivant :
(SHMHISTORYSIZE + (SHMDIALOGSIZE * n))*
où :
n est le nombre de connexions simultanées.
SHMHISTORYSIZE correspond à la taille en ko de l'historique des sessions WEBDEV (par défaut, 2048 ko).
SHMDIALOGSIZE correspond à la taille en ko de la requête maximale envoyée au serveur (par défaut 500 ko).

SHMHISTORYSIZE et SHMDIALOGSIZE sont dénis dans les chiers de conguration WEBDEV. Pour plus de
détails, consultez Annexe 3 : Fichier de conguration.

Pour connaître la taille de la mémoire partagée, exécutez la ligne de commande suivante :
/sbin/sysctl kernel.shmmax


Pour modier la taille de la mémoire partagée :

1. Editez le chier/etc/sysctl.conf avec un éditeur de texte. Par exemple, pour éditer un chier, il sut d'utiliser
    la ligne de commande suivante :
    emacs /etc/sysctl.conf

```
Remarque : il est également possible d'éditer le chier avec :
vi /etc/sysctl.conf
```
2. Rajoutez ou modiez la ligne correspondant à l'entrée "kernel.shmmax" en indiquant le nouveau
    paramétrage :
    kernel.shmmax = xxx

```
où xxx correspond au nouveau paramétrage.
```
3. Pour prendre en compte ces nouveaux paramètres, utilisez la ligne de commande suivante :
    /sbin/sysctl -p


## WEBDEV

Présentation

Un compte Utilisateur permet à l'administrateur du serveur de :
regrouper les diérents sites dynamiques d'un responsable de sites. Ces sites dynamiques sont installés sur
un seul serveur Web.
paramétrer le nombre total de connexions accordées pour l'ensemble des sites dynamiques du responsable
de sites.
paramétrer les répertoires d'installation des sites dynamiques sur le serveur Web.
paramétrer le répertoire de transfert de chiers (pour les installations et mises à jour des sites dynamiques
WEBDEV 2025 à distance par FTP).

Ce compte Utilisateur permet au responsable de sites de :

```
utiliser l'administrateur WEBDEV à distance, pour gérer ses sites dynamiques WEBDEV installés sur le serveur.
faire des installations et des mises à jour de sites dynamiques WEBDEV à distance (par HTTP ou FTP).
```
Remarque : Un compte Utilisateur spécique (dont le login et le mot de passe ont été dénis lors de l'installation
du serveur d'application WEBDEV) permet à l'administrateur du serveur d'utiliser l'administrateur WEBDEV à
distance. Dans ce cas, l'administrateur du serveur peut superviser et paramétrer tous les sites dynamiques
WEBDEV installés sur le serveur Web. Si ce compte est supprimé, l'utilisation de l'administrateur WEBDEV à
distance est impossible.

Les comptes WEBDEV sont créés dans l'administrateur distant mais ils nécessitent une conguration spécique
des utilisateurs et de leurs droits sur le serveur Linux.

Note : La gestion de la sécurité des sites WEBDEV est renforcée : les sites (ainsi que le déploiement de site)
s'exécutent sous l'identité du propriétaire du site déni dans l'administrateur distant. Les sites ne peuvent pas
interagir. L'installation d'un site WEBDEV ne requiert aucun droit spécique en plus des droits standard attribués
à chaque utilisateur.

Conguration des utilisateurs et des droits sur le serveur Linux

Avant de créer le premier compte utilisateur WEBDEV dans l'administrateur distant, il est nécessaire de
congurer le serveur Linux.

Création d'un compte FTP sous Linux (nécessaire uniquement lors d'une installation de sites par FTP)

En général, un compte utilisateur d'Unix peut avoir un compte FTP.
Le répertoire de base de ce compte système (Home Directory) correspond au répertoire de téléchargement FTP.
Ce répertoire de base correspond au répertoire où les chiers nécessaires à l'installation du site seront

```
WINDEV WINDEV Mobile Autres
```
# Créer les comptes utilisateur


transférés lors d'une installation d'un site par FTP. Une fois le transfert de chiers réalisé, l'installation est
automatique.

Création des utilisateurs et de leurs répertoires

Pour gérer les utilisateurs sur le serveur :

1. Créez un nouvel utilisateur, en utilisant par exemple la ligne de commande :
    adduser <Nom Utilisateur>

```
Tous les répertoires nécessaires (y compris le compte FTP) sont alors créés.
```
2. Dans le répertoire de cet utilisateur, créez trois répertoires diérents :
    un répertoire pour déployer les sites,
    un répertoire pour les données,
    un répertoire pour le transfert des données WEBDEV.
Vous pouvez par exemple utiliser la syntaxe suivante :
mkdir app
mkdir data
mkdir ftp_webdev
3. Il est conseillé d'aecter ces répertoires au groupe d'administrateurs (groupe webdevadmin par défaut). Il est
    possible d'utiliser la syntaxe suivante :
    chgrp webdevadmin app
    chgrp webdevadmin data
    chgrp webdevadmin ftp_webdev
4. Listez les droits des répertoires d'installation, par exemple en utilisant la ligne de commande :
    s -l

```
Les droits sont achés sous la forme suivante :
drwxr-xr-x 2 root webdevadmin 4096 Mar 1 08:25 data
drwxr-xr-x 2 root webdevadmin 4096 Mar 1 08:26 app
drwxr-xr-x 2 root webdevadmin 4096 Mar 1 08:27 ftp_webdev
```
```
Il est conseillé de donner les droits en lecture au groupe webdevadmin. Pour cela, il est possible d'utiliser la
ligne de commande suivante :
chmod g+rx app
chmod g+rx data
```
```
Si vous listez à nouveau les droits, vous obtenez :
drwxr-x - - - 2 root webdevadmin 4096 Mar 1 08:25 data
drwxr-x - - - 2 root webdevadmin 4096 Mar 1 08:26 app
drwxr-x - - - 2 root webdevadmin 4096 Mar 1 08:27 ftp_webdev
```

Remarque : Le groupe webdevadmin doit avoir les droits de lecture/écriture dans les répertoires ftp, site et
données de l'utilisateur uniquement pour permettre d'eectuer une sauvegarde du site depuis l'administrateur
distant. Si ces droits ne sont pas accordés, cette sauvegarde ne sera pas possible.

Création des comptes Utilisateur

La création des comptes Utilisateur est réalisée grâce à l'administrateur distant.

Comment lancer l'administrateur distant

L'administrateur distant est un site Internet qui peut être lancé depuis n'importe quel poste possédant un
navigateur. Pour lancer l'administrateur distant, il sut d'utiliser l'adresse suivante :
[http://<Adresse](http://<Adresse) IP Serveur>/WDAdminWeb
Après s'être connecté en tant qu'administrateur (login ADMIN, mot de passe : admin), il est possible de créer des
comptes WEBDEV.

Caractéristiques d'un compte Utilisateur

Un compte Utilisateur doit avoir les caractéristiques suivantes :
Login de l'utilisateur,
Mot de passe et sa conrmation.

Le nom du compte Utilisateur DOIT correspondre au nom du compte Unix associé.

Lorsque ces informations sont données, il sut de saisir les caractéristiques du compte :

```
les informations utilisateurs :
Nom, prénom, adresse, etc.
les sites aectés au responsable de sites (si nécessaire)
le nombre maximum de connexions autorisées :
Nombre maximum de connexions simultanées autorisées sur tous les sites dynamiques WEBDEV du compte.
Le responsable de sites pourra ensuite redistribuer ses connexions selon ses sites WEBDEV à l'aide de
l'administrateur WEBDEV distant.
le répertoire des transferts FTP : Le répertoire des transferts FTP correspond au répertoire de base de
l'utilisateur. Ce répertoire a été créé dans le paragraphe Création des utilisateurs et de leurs répertoires
le répertoire de base des sites : Le répertoire de base des sites correspond au répertoire où seront installés
les sites WEBDEV de l'utilisateur. Ce répertoire a été créé dans le paragraphe
Création des utilisateurs et de leurs répertoires.
le répertoire de base des chiers de données : Le répertoire de base des chiers de données correspond au
répertoire où seront installés les chiers de données associés au site de l'utilisateur. Ce répertoire a été créé
dans le paragraphe Création des utilisateurs et de leurs répertoires.
```

## WEBDEV

Présentation

Deux méthodes permettent d'installer un site WEBDEV sur un serveur Unix :

1. Le déploiement à distance directement depuis le poste de développement :
    le responsable de sites WEBDEV pourra déployer directement son site depuis le poste de développement. Les
    chiers nécessaires seront transmis par HTTP (conseillé) ou par FTP (fonctionnement conservé par
    compatibilité avec ls versions précédentes). Ce type de déploiement est nécessaire si le serveur Web n'est pas
    directement accessible par le responsable de sites.
2. Le déploiement à distance depuis un poste d'administration : le développeur n'est pas obligé de
    connaître les caractéristiques du serveur pour créer le programme d'installation (appelé dans ce cas
    "Package"). Les paramètres du serveur ne sont renseignés que lors de l'exécution du package sur un poste
    d'administration. Ce poste d'administration est un poste Windows. Ce type de déploiement est donc conseillé
    lorsque le développeur ne connaît pas les caractéristiques du serveur lors de la création du programme
    d'installation.

Remarque : Pour chaque serveur Web hébergeant des sites WEBDEV 2025, il est nécessaire de posséder une
licence du serveur d'application WEBDEV 2025.

Informations nécessaires au déploiement d'un site par FTP ou HTTP

Rappel : A partir de la version 24, le déploiement d'un site par FTP n'est plus nécessaire. Il est également possible
de déployer à distance un site WEBDEV par HTTP.

Les paramètres nécessaires pour faire une installation à distance (directe ou par package) sont :

```
Nom du serveur Web (Adresse du serveur). Il est possible d'indiquer :
un nom de machine accessible par le réseau (cas d'Intranet par exemple). Exemple : "Serveur Test"
une adresse IP. Exemple : 123.3.250.
une adresse Internet. Exemple : http://www.succes.fr
Nom et mot de passe associé pour le compte Utilisateur.
Remarque : Le nom et le mot de passe associé pour le compte FTP sont identiques à ceux du compte
utilisateur.
```
Ces paramètres doivent être transmis :

```
soit au responsable des sites WEBDEV dans le cas d'une installation à distance directement depuis le poste de
développement. Le responsable de sites WEBDEV pourra installer directement son site WEBDEV depuis son
poste de développement, et faire régulièrement des mises à jour à distance de ses sites.
```
```
WINDEV WINDEV Mobile Autres
```
# Installer un site WEBDEV


```
soit à la personne qui installera le package correspondant au site WEBDEV dans le cas d'une installation à
distance depuis un poste d'administration.
```
Erreurs pouvant être achées lors d'une installation par FTP

La liste des erreurs et leur mode de résolution sont présentés dans le chapitre
Problèmes liés à une installation par FTP.

Informations nécessaires au déploiement par package

Le package a été généré depuis WEBDEV Développement.
Pour installer le package sur un poste :

1. Vériez que vous possédez les éléments suivants :
    le package
    l'outil WDDeploy et son framework (chiers WD300*.DLL et chiers *.WDK).
2. Copiez ces éléments sur un PC Windows. Ce PC doit pouvoir accéder au serveur LINUX par FTP.
3. Lancez WDDeploy et chargez l'archive ZIP correspondant au package.
4. Cliquez sur le bouton permettant de déployer le site.


## WEBDEV

Présentation

Cette page d'aide présente les principaux problèmes (et leurs solutions) pouvant être rencontrés lors de
l'utilisation du serveur d'application WEBDEV 2025.

Problèmes liés à une installation par FTP

La liste ci-dessous présente les diérents messages d'erreur apparaissant dans l'assistant d'installation à
distance (chez le responsable de sites). Certains de ces messages nécessitent des actions spéciques de
conguration au niveau du serveur Web de déploiement.
Pour chaque erreur, diverses solutions sont proposées.
Des messages d'erreur peuvent apparaître à diverses étapes de l'installation à distance.

Etape 1 : Saisie des logins et mot de passe Serveur et FTP (Installation du site)

L'assistant d'installation eectue une vérication de la validité des logins et mots de passe. Voici la liste des
erreurs pouvant apparaître.

La vérication du mot de passe utilisateur a échoué : le serveur n'a pas retourné d'information.

Les problèmes possibles sont les suivants :

```
Le serveur web ne fonctionne pas.
Solution : Relancer le serveur Web sur le poste serveur.
Le serveur FTP ne fonctionne pas.
Solution : Relancer le serveur FTP sur le poste serveur.
Le serveur FTP est mal conguré : nom d'utilisateur incorrect, ...
Solution : Vérier la conguration du serveur FTP pour l'utilisateur.
Le serveur d'application WEBDEV n'est pas installé correctement.
Solution : Réinstaller le serveur d'application WEBDEV.
```
Le mot de passe FTP n'est pas correct ou le serveur FTP n'est pas joignable.

Les problèmes possibles sont les suivants :

```
Le mot de passe FTP indiqué par le responsable de sites n'est pas correct.
Solution : Vérier le mot de passe FTP et communiquer ce mot de passe au responsable de site.
Le serveur FTP ne fonctionne pas.
Solution : Relancer le serveur FTP.
```
```
WINDEV WINDEV Mobile Autres
```
# Dépannage


```
Le nombre de connexions autorisées sur le serveur FTP est dépassé.
Solution : Le responsable de site doit attendre qu'une connexion au serveur FTP soit libérée.
L'adresse du serveur Web est incorrecte.
Solution : Indiquer au responsable de sites l'adresse exacte du serveur Web où l'installation du site doit être
eectuée par FTP.
```
La vérication du mot de passe utilisateur a échoué : l'utilisateur est inconnu du serveur. Vériez
l'adresse du serveur et le nom d'utilisateur.

Les problèmes possibles sont les suivants :

```
Le gestionnaire de comptes ne reconnaît pas le responsable de sites.
Solution : Vérier qu'un compte Utilisateur a été créé dans l'administrateur distant pour ce responsable de
sites et communiquer le "login" correspondant au responsable de sites.
```
La vérication du mot de passe utilisateur a échoué : le serveur n'a pas retourné d'information.

Les problèmes possibles sont les suivants :

```
Le mot de passe saisit lors de l'installation à distance ne correspond pas au mot de passe déni dans
le gestionnaire de comptes.
Solution : Vérier le mot de passe associé au responsable de sites dans l'administrateur distant WEBDEV et
communiquer ce mot de passe au responsable de sites.
```
Etape 2 : Installation du site (installation ou mise à jour)

L'assistant d'installation eectue l'installation ou la mise à jour du site. Voici la liste des erreurs pouvant
apparaître.

Impossible de créer un répertoire temporaire sur le serveur. Contactez l'administrateur du serveur.

Les problèmes possibles sont les suivants :

```
Le répertoire où le site est installé appartient à l'utilisateur root.
Solution : associer le répertoire à l'utilisateur déclaré dans Apache.
```
Le nom de client annoncé est inconnu. Vériez votre nom de client et le mot de passe associé.

Les problèmes possibles sont les suivants :

```
Le gestionnaire de comptes ne reconnaît pas le responsable de sites.
Solution : Vérier qu'un compte Utilisateur a été créé dans l'administrateur WEBDEV pour ce responsable de
sites et communiquer le "login" correspondant au responsable de sites.
```

Les chiers nécessaires à l'installation n'ont pas été transmis correctement.
Vériez que le nom d'utilisateur et le mot de passe du FTP sont corrects et correspondent bien au compte
propriétaire du site.

Les problèmes possibles sont les suivants :

```
Une erreur a eu lieu pendant le transfert FTP et le chier installé sur le serveur n'est pas lisible.
Solution : Le responsable de sites doit recommencer son installation.
Attention : S'il s'agit d'une première installation, le responsable de sites doit supprimer la description du
serveur dans la liste "Mise à jour à distance".
```
Le chier d'installation est invalide. La transmission du chier ne s'est pas passée correctement ou le
chier transmis a été endommagé.

Les problèmes possibles sont les suivants :

```
Une erreur a eu lieu pendant le transfert FTP et le chier installé sur le serveur n'est pas lisible.
Solution : Le responsable de sites doit recommencer son installation.
Attention : S'il s'agit d'une première installation, le responsable de sites doit supprimer la description du
serveur dans la liste "Mise à jour à distance".
```
Erreur pendant le décryptage des informations d'installation. Vériez le mot de passe utilisé.

Les problèmes possibles sont les suivants :

```
Le mot de passe saisit lors de l'installation à distance ne correspond pas au mot de passe déni dans
le gestionnaire de comptes.
Solution : Vérier le mot de passe associé au responsable de sites dans l'administrateur distant WEBDEV et
communiquer ce mot de passe au responsable de sites.
```
Impossible d'ajouter la programmation à cause de l'erreur suivante : XXX

Lors de la programmation d'une installation diérée, un des problèmes suivants est survenu :

```
Pas assez de mémoire disponible.
Solution : Il est nécessaire de libérer de la mémoire sur le serveur Web, puis de retenter l'installation diérée.
Impossible de trouver l'administrateur local WEBDEV, vérier que le serveur d'application WEBDEV est
correctement installé sur le serveur.
L'administrateur local WEBDEV ne répond pas à la demande de programmation.
Erreur lors du lancement de l'administrateur local WEBDEV : vériez que le serveur d'application WEBDEV est
correctement installé sur le serveur.
```

Un site de même nom est déjà installé sur ce serveur. Un même serveur ne peut pas abriter deux sites
portant le même nom. Vous devez renommer votre site ou désinstaller l'existant. S'il s'agit du même site,
vous devez faire une mise à jour au lieu d'une installation.

Lors d'une installation par FTP, deux sites du même nom ne peuvent pas être installés sur un même serveur
Web, même si ces sites appartiennent à des responsables de sites diérents.
Dans le cas d'une première installation du site sur le poste serveur, le responsable de sites WEBDEV doit
renommer son site (renommer son projet).
Remarque : Pour eectuer une mise à jour par FTP, le responsable de sites doit utiliser l'option "Mise à jour à
distance" lors de l'installation de son site par FTP (et non l'option "Installation à distance").

Impossible de créer le répertoire du site. Contactez l'administrateur du serveur.

Les problèmes possibles sont les suivants :

```
Le répertoire de base des sites n'existe pas.
Solution : Vérier le répertoire de base des sites indiqué dans le gestionnaire de comptes. Vérier l'existence
de ce répertoire.
Les droits d'accès au répertoire de base des sites sont insusants.
Solution : les droits accordés au répertoire doivent correspondre aux droits du propriétaire du site.
```
Impossible de créer le répertoire des chiers de données. Contactez l'administrateur du serveur.

Les problèmes possibles sont les suivants :

```
Le répertoire de base des données n'existe pas.
Solution : Vérier le répertoire de base des données indiqué dans le gestionnaire de comptes. Vérier
l'existence de ce répertoire.
Les droits d'accès au répertoire de base des données sont insusants.
Solution : les droits accordés au répertoire doivent correspondre aux droits du propriétaire du site.
```
Impossible d'acquérir les privilèges du propriétaire du chier XXXX.

L'identité du propriétaire du site concerné n'a pas pu être validée.
Solution : Vériez le compte Unix du propriétaire du chier concerné. Il doit correspondre au compte Utilisateur
associé.

Etape 3 : Mise à jour d'un site

Lors de la mise à jour du site, l'assistant d'installation vérie la bonne installation du site et sa conguration.
Voici la liste des erreurs pouvant apparaître.

Nom du site inconnu


Les problèmes possibles sont les suivants :

```
Le site n'est pas installé sur le serveur.
Solution : Faire une installation distante complète.
Le site n'est plus référencé dans l'administrateur WEBDEV.
Solution : Référencer le site WEBDEV dans l'administrateur WEBDEV à distance.
```
Le nom du client demandeur et le propriétaire du site ne correspondent pas

Les problèmes possibles sont les suivants :

```
Le site a été installé par un autre responsable de sites.
Solution : Dans l'administrateur WEBDEV distant, attribuer le site au compte Utilisateur correspondant.
Vérier que les répertoires de base (de données, du site, et de transfert FTP) sont corrects.
```
Echec lors du cryptage

Les problèmes possibles sont les suivants :

```
Le cryptage de la mise à jour a échoué.
Solution : Libérer de l'espace mémoire et / ou disque sur le poste eectuant la mise à jour (poste du
responsable de sites par exemple).
```
Erreur lors de la récupération du chier d'information. Le chier ou le répertoire XXXX.WINFO n'existe
pas ou est inaccessible

Les problèmes possibles sont les suivants :

```
Impossibilité de copier le chier temporaire décrivant l'état du site. L'utilisateur n'a pas les droits
nécessaires dans le répertoire FTP.
Solution : Les droits sur le répertoire de transfert FTP doivent correspondre aux droits du propriétaire du site.
Impossibilité de copier le chier temporaire décrivant l'état du site. Il n'y a pas assez de place
disponible sur le disque.
Solution : Libérer de l'espace disque sur le serveur.
```
Messages d'erreurs pouvant être achés dans le navigateur

Un site développé avec WEBDEV peut acher des messages d'erreur sur le navigateur des postes clients.
Ces messages d'erreurs sont détaillés dans l'aide en ligne du serveur d'application WEBDEV.


## WEBDEV

Cette page regroupe les principaux termes spéciques à WEBDEV utilisés dans la documentation du serveur
d'application WEBDEV.

Administrateur du serveur
Personne responsable de l'installation de logiciels ou sites sur un ou plusieurs postes serveurs chez l'hébergeur.
Dans le cas d'un serveur mutualisé, l'administrateur du serveur est responsable de la répartition des connexions
par responsable de sites, responsable de la localisation physique des sites sur le serveur, ...

Administrateur WEBDEV distant
Site installé sur le serveur Web, permettant :

```
au responsable de site de vérier / modier à distance la conguration de ses sites WEBDEV installés sur un
serveur.
à l'administrateur du serveur de vérier / modier à distance la conguration de tous les sites WEBDEV
installés sur le serveur. L'administrateur du serveur peut aussi gérer les comptes Utilisateur.
```
Administrateur WEBDEV
Application Windows installée sur le serveur permettant à l'administrateur du serveur de paramétrer les
diérents sites dynamiques WEBDEV installés sur le serveur en cours.
L'administrateur WEBDEV permet aussi de créer les comptes Utilisateur.

Compte Utilisateur
Compte associé à un responsable de sites.
Ce compte permet à l'administrateur du serveur :

```
de regrouper les sites d'un responsable de sites.
de paramétrer le nombre de connexions autorisées pour un responsable de sites.
de paramétrer les répertoires d'installation des sites.
de paramétrer le répertoire de transfert des chiers (pour une installation ou des mises à jour par FTP).
```
Ce compte permet au responsable de sites :

```
d'utiliser l'administrateur à distance.
de faire des installations et des mises à jour de sites à distance.
```
Ce compte est créé sur un serveur Web par l'administrateur du serveur à l'aide :

```
soit de l'administrateur local.
soit de l'administrateur à distance.
```
```
WINDEV WINDEV Mobile Autres
```
# Annexe 1 : Vocabulaire de WEBDEV


Développeur de sites
Personne qui crée et modie des sites WEBDEV avec WEBDEV version Développement.

Hébergeur
Société proposant d'héberger des sites Internet sur des serveurs WEB.

Internaute
Utilisateur de sites Internet.

Responsable de sites
Personne responsable du déploiement et de la maintenance d'un ou de plusieurs sites WEBDEV. Cette personne
est directement en contact avec l'administrateur du serveur.


## WEBDEV

Avant d'installer le serveur d'application WEBDEV pour Linux, il est nécessaire de vérier la conguration du
serveur Linux.
Les diérentes étapes de cette conguration sont les suivantes :
Vérication de la présence du serveur Apache.
Recherche du chier de conguration de Apache.
Vérication de la présence d'un serveur FTP (uniquement si une installation par FTP doit être eectuée).
Vérication de la présence de la librairie libstdc++
Vérication de la présence de la librairie QT version 4.5 minimale.

Après l'installation, il est également nécessaire de vérier si le serveur Apache a bien été modié.

Les paragraphes suivants expliquent comment faire ces vérications sous diverses distributions :

```
Debian,
Mandrake 10,
Redhat 9.
```
1. Vérication de la conguration du serveur sous Débian

1.1. Serveur Apache

Vérication de la présence d'un serveur WEB Avant d'installer le serveur d'application WEBDEV, il est
nécessaire de savoir si un serveur WEB Apache est installé.
Remarque : pour eectuer les manipulations suivantes, il est nécessaire d'être connecté en tant que "root".

Un moyen simple pour vérier si le serveur Apache est lancé sur le serveur Linux, est d'utiliser la commande
suivante :
dpkg-l apache

Installation d'un serveur Apache L'installation d'un serveur Apache peut par exemple être lancée par la ligne
de commande suivante :
apt-get install apache

```
WINDEV WINDEV Mobile Autres
```
# Annexe 2 : Vérication du serveur


Recherche du chier de conguration de Apache

Avant de lancer l'installation du serveur d'application WEBDEV Linux, il est nécessaire de connaître le répertoire
et le nom du chier de conguration de Apache.
Pour cela, exécutez les lignes de commande suivantes :

1. Lister les programmes correspondants aux services utilisés :
    netstat --tcp --listen --numeric --program

```
Cette ligne de commande permet de lister les services en cours d'utilisation avec le nom du programme
correspondant.
```

2. En connaissant le nom du programme, il est possible d'obtenir des renseignements sur sa conguration. Il
    sut d'utiliser la ligne de commande suivante :
    <Nom Programme> -V

```
Dans notre exemple, correspond à http2 :
http2 -V
```
Vous obtenez les informations suivantes :

Dans ces informations, les deux points importants sont :
le chemin du répertoire du serveur.
le nom du chier de conguration et son chemin. Son chemin est le plus souvent un chemin relatif au
répertoire du serveur.

Le chier de conguration nécessaire pour l'installation du serveur d'application WEBDEV pour Linux doit
contenir le mot "User". Il est conseillé d'éditer le chier de conguration trouvé précédemment et de rechercher
le mot "User".
Si ce mot n'est pas trouvé, il est conseillé de faire une recherche dans les chiers inclus dans ce chier de
conguration (pour trouver les chiers inclus, il sut de rechercher le mot "Include" dans le chier de
conguration).
Par exemple, pour éditer un chier sous Débian, il sut d'utiliser la ligne de commande suivante :
editor /etc/apache/httpd2.conf
Lorsque vous avez trouvé le chier de conguration contenant le mot "User", notez son chemin et son nom, il
vous sera demandé lors de l'installation du serveur d'application WEBDEV pour Linux.

1.2. Serveur FTP (uniquement en cas d'installation par FTP)

Le serveur FTP permet de réaliser simplement et directement les installations des sites WEBDEV. Ce serveur FTP
doit être installé sur le poste serveur et doit pouvoir gérer les échanges sécurisés (avec mot de passe).
Un moyen simple pour vérier si un serveur FTP est installé sur le serveur Linux, est d'utiliser la commande
suivante :


netstat --tcp --listen |grep ftp
Cette ligne renvoie les services FTP actuellement installés sur le serveur. Si le service FTP n'est pas présent, il est
nécessaire d'installer un serveur FTP.
L'installation d'un serveur FTP peut par exemple être lancée par la ligne de commande suivante :
apt-get install vsftpd
Dans ce dernier cas, vous pouvez modier les paramètres de conguration de la façon suivante :
Editer "/etc/vsftpd.conf".
Décommenter la ligne "local_enable=YES" pour autoriser les logins du poste à se connecter par FTP.
Décommenter la ligne "write-enable=YES" pour autoriser les écritures.
Décommenter la ligne "local_umask=022".
Redémarrer le serveur ftp par la ligne de commande suivante :
/etc/init.d/vsftpd restart

1.3. Librairie libstdc++

Pour vérier la présence de la librairie libstdc++, il est conseillé d'utiliser la ligne de commande suivante :
ldcong -p | grep libstdc++
Si ce chier n'existe pas, il est conseillé de consulter la documentation de la distribution pour l'installer.

1.4. Librairie QT

Pour vérier la présence de la librairie QT (Core et GUI), il est conseillé d'utiliser la ligne de commande suivante :
qtcong
Si ce chier n'existe pas, il est conseillé de consulter la documentation de la distribution pour l'installer (au
minimum version 5.3). La ligne de commande suivante peut également être utilisée :
apt-get install libQt5Core
apt-get install libQt5Gui
apt-get install libQt5Widgets

1.5. Vérication du serveur Apache après installation du serveur d'application

Cette vérication doit être eectuée aussi bien si l'installation s'est terminée correctement ou si l'installation
s'est terminée avec l'erreur "Cong-broken".

Les étapes sont les suivantes :

1. Vériez la conguration du serveur Apache grâce à la ligne de commande suivante :
    apache2ctl congtest

```
Si une erreur apparaît, eectuez les manipulations suivantes.
```
2. Allez dans le répertoire "/etc/apache2/mods-enabled" :
    cd /etc/apache2/mods-enabled
3. Activez les modules "action" et "cgi" via les lignes de commande suivantes :
    ln -s ../mods-available/actions.load ./actions.load
    ln -s ../mods-available/actions.conf ./actions.conf
    ln -s ../mods-available/cgi.load ./cgi.load


Lorsque la conguration de Apache est correcte, il est conseillé de redémarrer Apache en utilisant par exemple
la ligne de commande suivante :
apache2ctl graceful
Remarque : Juste après installation, le service WEBDEV30 est actif. Mais dans certains cas, si la machine Linux est
redémarrée, le service ne sera pas relancé au boot.
Pour savoir si le serveur d'application WEBDEV est lancé, wd300admind doit être lancé. Pour connaître cette
information, tapez la ligne de commande suivante :
ps -ef | grep wd300admind
Pour que le service WEBDEV30 se relance automatiquement au boot, tapez la ligne de commande suivante :
update-rc.d WEBDEV30 defaults 91

2. Vérication de la conguration du serveur sous Mandrake

2.1. Serveur Apache

Vérication de la présence d'un serveur WEB

Avant d'installer le serveur d'application WEBDEV, il est nécessaire de savoir si un serveur WEB Apache est
installé.
Remarque : pour eectuer les manipulations suivantes, il est nécessaire d'être connecté en tant que "root".
Un moyen simple pour vérier si le serveur Apache est lancé sur le serveur Linux, est d'utiliser la commande
suivante :
netstat --tcp --listen
Cette ligne renvoie les services actuellement installés sur le serveur. Par exemple :
Proto Recv-Q Send-Q Local Address Foreign Address State
tcp 0 0 *:time *:* LISTEN
tcp 0 0 *:discard *:* LISTEN
tcp 0 0 *:daytime *:* LISTEN
tcp 0 0 *:http *:* LISTEN
tcp 0 0 *:ssh *:* LISTEN
Si le service http n'est pas présent, cela signie qu'aucun serveur WEB n'est actuellement lancé sur le poste en
cours.

Une autre méthode pour vérier la présence d'un serveur WEB, est d'utiliser la ligne de commande suivante :
netstat --tcp --listen --numeric
Si le port 80 apparaît dans le résultat, cela signie qu'un serveur WEB est installé.


Installation d'un serveur Apache L'installation d'un serveur Apache peut par exemple être lancée par la ligne
de commande suivante :
urpmi apache

Recherche du chier de conguration de Apache

Avant de lancer l'installation du serveur d'application WEBDEV Linux, il est nécessaire de connaître le répertoire
et le nom du chier de conguration de Apache.

Pour cela, exécutez les lignes de commande suivantes :

1. Lister les programmes correspondants aux services utilisés :
    netstat --tcp --listen --numeric --program

```
Cette ligne de commande permet de lister les services en cours d'utilisation avec le nom du programme
correspondant.
```

2. En connaissant le nom du programme, il est possible d'obtenir des renseignements sur sa conguration. Il
    sut d'utiliser la ligne de commande suivante :
    <Nom Programme> -V

```
Dans notre exemple, correspond à http2 :
http2 -V
```
Vous obtenez les informations suivantes :

Dans ces informations, les deux points importants sont :
le chemin du répertoire du serveur.
le nom du chier de conguration et son chemin. Son chemin est le plus souvent un chemin relatif au
répertoire du serveur.

Le chier de conguration nécessaire pour l'installation du serveur d'application WEBDEV pour Linux doit
contenir le mot "User". Il est conseillé d'éditer le chier de conguration trouvé précédemment et de rechercher
le mot "User".
Si ce mot n'est pas trouvé, il est conseillé de faire une recherche dans les chiers inclus dans ce chier de
conguration (pour trouver les chiers inclus, il sut de rechercher le mot "Include" dans le chier de
conguration).
Par exemple, pour éditer un chier, il sut d'utiliser la ligne de commande suivante :
emacs /etc/apache/httpd2.conf
Remarque : il est également possible d'éditer le chier avec :
vi /etc/apache/httpd2.conf
Lorsque vous avez trouvé le chier de conguration contenant le mot "User", notez son chemin et son nom, il
vous sera demandé lors de l'installation du serveur d'application WEBDEV pour Linux.

2.2. Serveur FTP (uniquement en cas d'installation par FTP)

Le serveur FTP permet de réaliser simplement et directement les installations des sites WEBDEV. Ce serveur FTP
doit être installé sur le poste serveur et doit pouvoir gérer les échanges sécurisés (avec mot de passe).


Un moyen simple pour vérier si un serveur FTP est installé sur le serveur Linux, est d'utiliser la commande
suivante :
netstat --tcp --listen |grep ftp
Cette ligne renvoie les services FTP actuellement installés sur le serveur. Si le service FTP n'est pas présent, il est
nécessaire d'installer un serveur FTP.
L'installation d'un serveur FTP peut par exemple être lancée par la ligne de commande suivante :
urpmi proftpd

2.3. Librairie libstdc++

Pour vérier la présence de la librairie libstdc++, il est conseillé d'utiliser la ligne de commande suivante :
ldcong -p | grep libstdc++-libc6.2-2.so.3
Si ce chier n'existe pas, il est conseillé de consulter la documentation de la distribution pour l'installer.
Remarque : il est nécessaire de s'assurer que la librairie libstdc++ ne soit pas congurée en mise à jour
automatique vers la dernière version stable : en eet, une mise à jour vers un module non compatible pourrait
être eectuée.

2.4. Librairie QT

Pour vérier la présence de la librairie QT (Core et GUI), il est conseillé d'utiliser la ligne de commande suivante :
qtcong
Si ce chier n'existe pas, il est conseillé de consulter la documentation de la distribution pour l'installer (au
minimum version 5.3).

2.5. Vérication du serveur Apache après installation du serveur d'application

Cette vérication doit être eectuée aussi bien si l'installation s'est terminée correctement ou si l'installation
s'est terminée avec l'erreur "Cong-broken".
Les étapes sont les suivantes :

1. Vériez la conguration du serveur Apache grâce à la ligne de commande suivante :
    apachectl congtest

```
Si une erreur apparaît, eectuez les manipulations suivantes.
```
2. Editez le chier de conguration de Apache.
    Par exemple, utilisez la ligne de commande suivante :
    emacs /etc/apache/httpd2.conf

```
Remarque : il est également possible d'éditer le chier avec :
vi /etc/apache/httpd2.conf
```
3. Recherchez la ligne suivante et supprimez le caractère # en début de ligne :
    # LoadModule actions_module /usr/lib/apache/1.3/mod_actions.so

```
Remarque : selon la version d'apache, cette ligne peut varier. Cette ligne doit être de la forme :
# LoadModule actions_module <path des modules du serveur>/
mod_actions.so
```
4. Sauvez le chier de conguration et vériez à nouveau la conguration du serveur Apache (point 1).


Lorsque la conguration de Apache est correcte, il est conseillé de redémarrer Apache en utilisant par exemple
la ligne de commande suivante :
apachectl graceful
Remarque : Juste après installation, le service WEBDEV30 est actif. Mais dans certains cas, si la machine Linux est
redémarrée, le service ne sera pas relancé au boot.
Pour savoir si le serveur d'application WEBDEV est lancé, wd300admind doit être lancé. Pour connaître cette
information, tapez la ligne de commande suivante :
ps -ef | grep wd280admind
Pour que le service WEBDEV30 se relance automatiquement au boot, tapez la ligne de commande suivante :
chkcong --level2 service on

3. Vérication de la conguration du serveur sous RedHat

3.1. Serveur Apache

Vérication de la présence d'un serveur WEB

Avant d'installer le serveur d'application WEBDEV, il est nécessaire de savoir si un serveur WEB Apache est
installé.
Remarque : pour eectuer les manipulations suivantes, il est nécessaire d'être connecté en tant que "root".

Un moyen simple pour vérier si le serveur Apache est lancé sur le serveur Linux, est d'utiliser la commande
suivante :
netstat --tcp --listen
Cette ligne renvoie les services actuellement installés sur le serveur. Par exemple :
Proto Recv-Q Send-Q Local Address Foreign Address State
tcp 0 0 *:time *:* LISTEN
tcp 0 0 *:discard *:* LISTEN
tcp 0 0 *:daytime *:* LISTEN
tcp 0 0 *:http *:* LISTEN
tcp 0 0 *:ssh *:* LISTEN
Si le service http n'est pas présent, cela signie qu'aucun serveur WEB n'est actuellement lancé sur le poste en
cours. Le nom utilisé pour le service peut varier d'un poste à l'autre.
Une autre méthode pour vérier la présence d'un serveur WEB, est d'utiliser la ligne de commande suivante :
netstat --tcp --listen --numeric


Si le port 80 apparaît dans le résultat, cela signie qu'un serveur WEB est installé.

Installation d'un serveur Apache

L'installation d'un serveur Apache doit être eectuée à partir du CD d'installation de Redhat.

Recherche du chier de conguration de Apache

Avant de lancer l'installation du serveur d'application WEBDEV Linux, il est nécessaire de connaître le répertoire
et le nom du chier de conguration de Apache.

Pour cela, exécutez les lignes de commande suivantes :

1. Lister les programmes correspondants aux services utilisés :
    netstat --tcp --listen --numeric -- program

```
Cette ligne de commande permet de lister les services en cours d'utilisation avec le nom du programme
correspondant.
```
2. En connaissant le nom du programme, il est possible d'obtenir des renseignements sur sa conguration. Il
    sut d'utiliser la ligne de commande suivante :
    <Nom Programme> -V

```
Dans notre exemple, <Nom programme> correspond à http2 :
http2 -V
```
Vous obtenez les informations suivantes :


Dans ces informations, les deux points importants sont :
le chemin du répertoire du serveur.
le nom du chier de conguration et son chemin. Son chemin est le plus souvent un chemin relatif au
répertoire du serveur.

Le chier de conguration nécessaire pour l'installation du serveur d'application WEBDEV pour Linux doit
contenir le mot "User". Il est conseillé d'éditer le chier de conguration trouvé précédemment et de rechercher
le mot "User".
Si ce mot n'est pas trouvé, il est conseillé de faire une recherche dans les chiers inclus dans ce chier de
conguration (pour trouver les chiers inclus, il sut de rechercher le mot "Include" dans le chier de
conguration).
Par exemple, utilisez la ligne de commande suivante :
emacs /etc/apache/httpd2.conf
ou :
vi /etc/apache/httpd2.conf
Lorsque vous avez trouvé le chier de conguration contenant le mot "User", notez son chemin et son nom, il
vous sera demandé lors de l'installation du serveur d'application WEBDEV pour Linux.

3.2. Serveur FTP (uniquement en cas d'installation par FTP)

Le serveur FTP permet de réaliser simplement et directement les installations des sites WEBDEV. Ce serveur FTP
doit être installé sur le poste serveur et doit pouvoir gérer les échanges sécurisés (avec mot de passe).
Un moyen simple pour vérier si un serveur FTP est installé sur le serveur Linux, est d'utiliser la commande
suivante :
netstat --tcp --listen |grep ftp
Cette ligne renvoie les services FTP actuellement installés sur le serveur. Si le service FTP n'est pas présent, il est
nécessaire d'installer un serveur FTP.

L'installation d'un serveur FTP peut être eectuée à partir du CD d'installation de Redhat.


3.3. Librairie libstdc++

Pour vérier la présence de la librairie libstdc++, il est conseillé d'utiliser la ligne de commande suivante :
ldcong -p | grep libstdc++-libc6.2-2.so.3
Si ce chier n'existe pas, il est conseillé de consulter la documentation de la distribution pour l'installer.
Remarque : il est nécessaire de s'assurer que la librairie libstdc++ ne soit pas congurée en mise à jour
automatique vers la dernière version stable : en eet, une mise à jour vers un module non compatible pourrait
être eectuée.

3.4. Librairie QT

Pour vérier la présence de la librairie QT (Core et GUI), il est conseillé d'utiliser la ligne de commande suivante :
qtcong
Si ce chier n'existe pas, il est conseillé de consulter la documentation de la distribution pour l'installer (au
minimum version 5.3).

3.5. Vérication du serveur Apache après installation du serveur d'application

Cette vérication doit être eectuée aussi bien si l'installation s'est terminée correctement ou si l'installation
s'est terminée avec l'erreur "Cong-broken".
Les étapes sont les suivantes :

1. Vériez la conguration du serveur Apache grâce à la ligne de commande suivante :
    apachectl congtest

```
Si une erreur apparaît, eectuez les manipulations suivantes.
```
2. Editez le chier de conguration de Apache.
    Par exemple, utilisez la ligne de commande suivante :
    emacs /etc/apache/httpd2.conf

```
ou
vi /etc/apache/httpd2.conf
```
3. Recherchez la ligne suivante et supprimez le caractère # en début de ligne :
    # LoadModule actions_module /usr/lib/apache/1.3/mod_actions.so

```
Remarque : selon la version d'apache, cette ligne peut varier. Cette ligne doit être de la forme :
# LoadModule actions_module <path des modules du serveur>/
mod_actions.so
```
4. Sauvez le chier de conguration et vériez à nouveau la conguration du serveur Apache (point 1). Lorsque
    la conguration de Apache est correcte, il est conseillé de redémarrer Apache en utilisant par exemple la
    ligne de commande suivante :
    apachectl graceful

Remarque : Juste après installation, le service WEBDEV30 est actif. Mais dans certains cas, si la machine Linux est
redémarrée, le service ne sera pas relancé au boot.
Pour savoir si le serveur d'application WEBDEV est lancé, wd300admind doit être lancé. Pour connaître cette
information, tapez la ligne de commande suivante :


ps -ef | grep wd300admind
Pour que le service WEBDEV30 se relance automatiquement au boot, tapez la ligne de commande suivante :
ntsysv
et cochez le service wd300admind.


## WEBDEV

Fichier de conguration lié à l'installation de WEBDEV

Lors de l'installation du serveur d'application WEBDEV sur un serveur Linux, les renseignements
concernant WEBDEV (serveur d'application et gestionnaire de protocole) et l'administrateur WEBDEV sont
automatiquement enregistrés dans le chier de conguration suivant :
/etc/PC SOFT/WEBDEV/29.0/WEBDEV.conf

Ces renseignements sont automatiquement mis à jour lors de la modication des paramètres de
l'administrateur WEBDEV à distance.
Remarque : les diérentes entrées sont données à titre d'information et permettent de vérier la bonne
installation du serveur d'application WEBDEV.

Les entrées du chier de conguration créées sont les suivantes :
ADMINLOG :
Chemin du chier journal des installations par FTP. Ce paramètre est déni dans l'administrateur WEBDEV.
ALLOW_REMOTEINSTALL :
Autorisation de faire des installations de sites à distance (par FTP). Ce paramètre est déni dans
l'administrateur WEBDEV.
ALLOW_REMOTEUPDATE :
Autorisation de faire des mises à jour de sites à distance (par FTP). Ce paramètre est déni dans
l'administrateur WEBDEV.
BINPATH :
Chemin du programme WD300SESSION.EXE
BINPATHAWP :
Chemin du répertoire contenant WDxxxAWP (utilisé uniquement par Unix pour la mise à jour diérée).
CACHED_SESSIONS_A :
Activation des sessions prélancées (CACHED_SESSIONS donne le nombre de sessions prélancées dans une
application).
COMPTEPATH :
Chemin des chiers de données des comptes Utilisateur.
COOKIE_SESSION_HTTPONLY :
Activation de l'option "httponly" pour le cookie de session des sessions AWP.
COPIEIMGREPWEB :
Activation de la copie de chiers dans le répertoire _WEB.

```
WINDEV WINDEV Mobile Autres
```
# Annexe 3 : Fichier de conguration


## DEBUGPORT :

Port d'écoute du débogueur distant.

DEBUGPORTMIN :
Borne inférieure des ports auxiliaires de débogage distant.

DEBUGPORTMAX :
Borne supérieure des ports auxiliaires de débogage distant.

DEBUGREMOTE :
Autorisation de déboguer des sites WEBDEV à distance.

DOUBLELOG :
Force la génération en double des logs.

ERRORFILE :
Nom complet du chier HTML à utiliser pour acher les messages d'erreur.

LANCEUR :
Nom du moteur AWP

LOCALHOST :
Permet de personnaliser la valeur du hostname utilisé pour le mode test.

MAXCONNECT :
Nombre maximum de connexions autorisées (c'est-à-dire nombre maximum de moteurs lancés
simultanément). Ce paramètre est déni dans l'administrateur WEBDEV.

MAXCONNECTAPP :
Nombre maximum de connexions au même site (déni dans l'administrateur WEBDEV)

MAXRECONNECTAPP :
Nombre maximum d'accès simultanés à un même site par le même utilisateur (déni dans l'administrateur
WEBDEV).

NOIPCHECK :
Si cette clé est absente ou diérente de 0, aucune vérication de l'adresse IP l'appelant : cette adresse IP peut
changer pendant la session.
Si cette clé est présente et est égale à 0, l'IP de l'utilisateur ne doit pas changer pas pendant la session.

NOMAILSPOOLER :
Permet de désactiver le spooler de mails.

NOREMOTEPARAM :
Autorisation de modier les paramètres des sites à l'aide de l'administrateur distant.

ONERROR_AUTORECONNECT :
Indique si la reconnexion automatique est autorisée en cas de "BAD CONTEXT" (erreurs avec le tag
<szERR_RECONNECT_TOKEN>).

ONERROR_AUTORECONNECTTIME :
Temps en secondes avant la reconnexion automatique en cas de "BAD CONTEXT" (erreurs avec le tag
<szERR_RECONNECT_TOKEN>).

RECONNECTMESSAGE :
Texte du lien à acher lorsque l'utilisateur a la permission de se reconnecter à une application (erreurs avec
le tag <szERR_RECONNECT_TOKEN>).


## SERVERSOCKET :

```
Permet d'autoriser les sockets serveurs.
TIMEOUT_NORQ :
Temps avant la déconnexion de l'utilisateur si aucune nouvelle requête n'est reçue (déni dans
l'administrateur WEBDEV).
TIMEOUT_NORQ_AWP :
Temps avant la destruction d'une session AWP.
TIMEOUT_NORQ_WEBSERVICE :
Temps avant la déconnexion de l'utilisateur si aucune nouvelle requête n'est reçue pour les contextes de
Webservices SOAP ou REST.
TIMEOUT_REMOTEINSTALL :
Temps avant l'installation ou la mise à jour d'une application Web à distance.
TIMEOUT_RQ :
Temps d'attente maximum du lanceur (déni dans l'administrateur WEBDEV).
TIMEOUT_TACHES :
Durée maximum pour les tâches de fond et les tâches planiées.
VDIR :
Nom du répertoire virtuel déclaré dans le serveur HTTP qui contient le lanceur WD300AWP.EXE
WBADMIN :
Nom du compte d'administration WEBDEV.
WBGROUPADMIN :
Nom du groupe d'administration WEBDEV.
WEBSERVER :
Indique le serveur Web à congurer automatiquement.
WEBSERVERCONF :
(Linux seulement) Indique le chier de conguration du serveur Web à congurer automatiquement.
WEBSERVERMAINCONF :
(Linux seulement) Chemin du chier principal d'Apache contenant les mots-clés ‘User' et ‘Group'.
WEBSERVERGROUP_TMP :
Nom du groupe Apache : clé temporaire initialisée par WDADMIN.
WEBSERVERRESTART :
Indique la ligne de commande à utiliser pour recharger la conguration du serveur Web après une
modication.
WEBSERVERUSER_TMP :
Nom de l'utilisateur Apache : clé temporaire initialisée par WDADMIN.
```
En cas de personnalisation des messages d'erreur pour tous les sites installés sur le poste, une nouvelle entrée
est créée pour chaque message d'erreur.

Fichier de conguration lié à l'installation d'un site WEBDEV


Lors de l'installation d'un site WEBDEV sur un serveur Linux, les renseignements concernant le site sont
automatiquement enregistrés dans le chier de conguration suivant :
/etc/PC SOFT/WEBDEV/29.0/Applications/<NomSite>.conf
Où <NomSite> est le nom du site installé. Ce nom respecte la casse utilisée pour le nom du projet.

Remarques :

```
Les diérentes entrées dans le chier de conguration sont données à titre d'information et permettent de
vérier la bonne installation d'un site réalisé avec WEBDEV.
Ces entrées sont congurées automatiquement lors de l'installation d'un site WEBDEV.
Attention : Le nom du site est sensible à la casse ("Case sensitive"). Il ne faut pas modier ce paramètre.
```
Les entrées créées sont les suivantes :
APPLICATIONMULTIPLE :
Indique si un même application est déployable sur plusieurs sites virtuels.
APPLICATIONNAME :
Nom de l'application en déploiement.
AS400 :
Indique si le site utilise des chiers AS/400 (Valeur 1) ou non.
CACHED_SESSIONS :
Nombre de sessions prélancées pour cette application.
COOKIE_SESSION_HTTPONLY :
Activation de l'option "httponly" pour le cookie de session des sessions AWP.
ERRORFILE :
Nom complet du chier HTML à utiliser pour acher les messages d'erreur.
GPUHISTOCNX :
Indique si le Groupware Utilisateur doit enregistrer l'historique des connexions.
GPUPATH :
Localisation des chiers de données communs (HFSQL Classic) du Groupware Utilisateur (chemin complet).
GPUPATH_R :
Localisation des chiers de données des droits (HFSQL Classic) du Groupware Utilisateur pour le site ou le
Webservice (chemin complet).
HFPATH :
Localisation des chiers de données (HFSQL Classic) du site WEBDEV/Webservice (chemin complet).
HTTPS :
Permet d'indiquer si la connexion au site utilise une connexion HTTPS exclusivement.
LOGDIR :
Localisation des chiers de statistiques d'accès du site WEBDEV/Webservice (chemin complet).
LOCKFORUPDATE :
Indique si la connexion au site ou au Webservice est bloquée pour une mise à jour.


## NOIPCHECK :

Si cette clé est absente ou diérente de 0, aucune vérication de l'adresse IP l'appelant : cette adresse IP peut
changer pendant la session.
Si cette clé est présente et est égale à 0, l'IP de l'utilisateur ne doit pas changer pas pendant la session.

ONERROR_AUTORECONNECT :
Indique si la reconnexion automatique est autorisée en cas de "BAD CONTEXT".

ONERROR_AUTORECONNECTTIME :
Temps en secondes avant la reconnexion automatique en cas de "BAD CONTEXT".

MAXCONNECTAPP :
Nombre maximum de connexions au site ou au Webservice (déni dans l'administrateur WEBDEV).

MAXRECONNECTAPP :
Nombre maximum d'accès simultanés à un même site par le même internaute (déni dans l'administrateur
WEBDEV).

PROJECTERRORFILE :
Nom de la page statique dénie dans le projet comme template de la page d'erreur.

PROJECTPATH :
Chemin des chiers du site ou du Webservice.

PROJECTNAME :
Nom du site ou du Webservice (il s'agit du nom du projet si le site a été déployé sous un nom diérent).

RECONNECTMESSAGE :
Texte du lien à acher lorsque l'utilisateur a la permission de se reconnecter à une application.

SAAS_ADMINISTRATION_URL :
(SaaS) URL du site d'administration SaaS pour l'application.

SAAS_WEBSERVICE_URL :
(SaaS) L'URL du webservice SaaS que doit utiliser l'application.

TIMEOUT_NORQ :
Temps avant la déconnexion de l'internaute si aucune nouvelle requête n'est reçue (déni dans
l'administrateur WEBDEV).

TIMEOUT_TACHES :
Durée maximum pour les tâches de fond et les tâches planiées.

VERSION :
Version du site.

VIMAGEDIR :
Répertoire virtuel des images du site.

VIRTUALHOST :
Nom d'en-tête d'hôte du site web virtuel sur lequel est déployé un site ou un Webservice.

WEBSERVICE_DESCRIPTION :
Permet d'indiquer si la description d'un Webservice est publique (1) ou non (0).


## WEBDEV

Présentation

Le tableau ci-dessous présente les diérents modules installés par le serveur d'application WEBDEV pour Linux
et leurs principales fonctions.

```
Modules nécessaires au fonctionnement des sites WEBDEV
```
```
Nom Fonctions Lancé par ...
```
```
Gestionnaire AWP (Active Web
Pages) :
```
```
Décode les informations
provenant du site WEBDEV.
Transmet les informations
décodées au serveur
d'application WEBDEV.
```
```
Lancé par le serveur Web à
chaque requête d'un
internaute dans un site
dynamique WEBDEV.
```
```
Serveur d'application WEBDEV : Exécute les informations
transmises par le protocole
AWP. Construit la page HTML
dynamique achée par le
serveur Web sur le navigateur
de l'internaute.
```
```
Lancé par WD300AWP à
chaque connexion d'un
internaute sur un site
dynamique WEBDEV.
```
```
Administrateur WEBDEV distant : Permet aux responsables de
sites WEBDEV de gérer
directement leurs diérents
sites WEBDEV installés sur le
serveur.
Permet à l'administrateur du
serveur de congurer à distance
les diérents sites WEBDEV
installés sur le serveur, les
comptes Utilisateur, ...
Cet outil est nécessaire au
fonctionnement des sites
dynamiques WEBDEV.
```
```
Lancé par :
soit le responsable de sites
directement depuis son
navigateur.
soit l'administrateur du
serveur depuis un poste
diérent du serveur,
directement par son
navigateur.
```
L'administrateur WEBDEV à distance

```
WINDEV WINDEV Mobile Autres
```
# Annexe 4 : Modules de WEBDEV


L'administrateur WEBDEV à distance est un site WEBDEV, installé sur le serveur Web de Déploiement. Ce site
permet :
au responsable de sites de gérer directement ses sites WEBDEV, installés sur le serveur Web.
à l'administrateur du serveur de gérer directement les comptes Utilisateur et les sites WEBDEV installés sur le
serveur Web.

Sur un serveur Linux, l'administrateur distant est l'outil recommandé pour administrer le serveur et les
sites WEBDEV dynamiques installés sur le serveur.

Pour plus de détails, consultez l'aide en ligne de l'administrateur WEBDEV à distance.


## WEBDEV

Fichiers de conguration de Apache

Lors de l'installation du serveur d'application WEBDEV pour Linux, les informations suivantes sont ajoutées dans
le chier de conguration de Apache :

Le serveur Apache doit donc autoriser l'accès à ces répertoires.
Il peut être nécessaire d'ajouter des directives "<directory>" sur le répertoire de WEBDEV et sur les répertoires
des sites. Ces opérations ne sont pas réalisées par l'installation du serveur d'application WEBDEV pour Linux.
Pour plus de détails, consultez Test de l'administrateur distant.

Fichiers du serveur d'application WEBDEV pour Linux

Les diérents chiers et répertoires installés par le serveur d'application WEBDEV 2025 pour Linux sont les
suivants :
Fichier de conguration de WEBDEV 2025 : /etc/PC SOFT/WEBDEV/30.0/WEBDEV.conf

```
WINDEV WINDEV Mobile Autres
```
# Annexe 5 : Conguration du serveur


Fichier de conguration des sites installés : /etc/PC SOFT/WEBDEV/30.0/Applications/<Nom site>.conf

Répertoire d'installation du serveur d'application WEBDEV pour Linux : /usr/local/WebDev/30.0


Répertoire d'installation du protocole AWP : /usr/local/WebDev/30.0/AWP

Répertoire d'installation de l'administrateur distant : /usr/local/WebDev/30.0/WDAdminWeb


```
Répertoire d'installation des programmes permettant le déploiement des sites sur le serveur :
/usr/local/WebDev/30.0/WDInstalle
```
Fichiers installés lors du déploiement d'un site dynamique WEBDEV

Lors du déploiement d'un site WEBDEV, plusieurs types de chiers sont installés :


les pages, les images, ... sont installées dans le sous-répertoire du site correspondant à l'utilisateur. Dans cet
exemple, les chiers sont installés dans le sous-répertoire app\<nom du site> de l'utilisateur Pat. Ces
informations (répertoire d'installation des pages, ...) ont été fournies lors de la création du compte Utilisateur
sous l'administrateur distant (Créer les comptes utilisateur).

les chiers de données (HFSQL uniquement) sont installés dans le sous-répertoire des données
correspondant à l'utilisateur. Dans cet exemple, les chiers sont installés dans le sous-répertoire data\<nom
du site> de l'utilisateur Pat.
Ces informations (répertoire d'installation des données, ...) ont été fournies lors de la création du compte
Utilisateur sous l'administrateur distant (Créer les comptes utilisateur).



