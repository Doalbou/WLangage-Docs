## WINDEV

Présentation

Lors de l'installation en réseau d'une application WINDEV, un programme de contrôle à distance des exécutables
de l'application est automatiquement créé : WDADMINEXE.

WDADMINEXE permet à partir du poste serveur de :

```
Contrôler l'application à distance :
Le responsable d'une application utilisée en réseau peut gérer l'arrêt (automatique ou forcé) de
l'application pour tous les utilisateurs en cours.
Le responsable d'une application utilisée en réseau peut paramétrer la fréquence de la vérication des
mises à jour pour les applications clientes.
Informer sur la dernière mise à jour disponible : Le responsable d'une application utilisée en réseau peut
connaître le numéro de la version courante et de la dernière version compatible.
Connaître les caractéristiques des utilisateurs de l'application.
Gérer les versions installées sur les postes clients.
Gérer les installations avec prise en charge du Push.
```
Lancement

Pour lancer WDADMINEXE, double-cliquez sur "WDADMINEXE.EXE" présent dans le sous-répertoire "INSTALL" du
répertoire d'installation de l'application sur le poste serveur.

Remarque : Les options de contrôle de l'application à distance et les informations concernant la dernière mise à
jour sont contenues dans un chier de type "INI". Par défaut, ce chier est nommé "WDUPDATE.NET". Ce chier
contient les références des diérentes applications à contrôler et, pour chacune d'entre elles, les caractéristiques
du contrôle à eectuer (pour plus de détails, consultez Structure du chier de contrôle).

```
WEBDEV WINDEV Mobile Autres
```
# Centre de Contrôle des exécutables

# WINDEV (WDADMINEXE)


## WINDEV

Présentation

Le Centre de Contrôle des applications WINDEV permet au responsable d'une application utilisée en réseau :
de gérer l'arrêt (automatique ou forcé) de l'application pour tous les utilisateurs en cours. Cet arrêt de
l'application peut être nécessaire par exemple lors d'une mise à jour de l'application ou de la base de
données.
Pour plus de détails, consultez le Principe du contrôle à distance.
Remarque : Il est possible de personnaliser la gestion du contrôle à distance grâce à la fonction AppliContrôle
du WLangage.
de gérer la fréquence de vérication des mises à jour.

Le paramétrage de cette gestion s'eectue dans l'onglet "Contrôle" de WDADMINEXE.

Important : Si les options de contrôle à distance sont modiées directement dans le programme
d'administration "WDADMINEXE", ces options seront réinitialisées à chaque installation avec les options
spéciées lors de la création du programme d'installation.

Etat de l'application

L'onglet "Contrôle" de WDADMINEXE permet de gérer l'état de l'application et les messages achés selon l'état
de l'application :

```
WEBDEV WINDEV Mobile Autres
```
# WDADMINEXE : Contrôle de

# l'application à distance


```
Fonctionnement normal : la gestion de la déconnexion des utilisateurs de l'application sera automatique.
Pour plus de détails, consultez Gestion de déconnexion automatique.
Connexion interdite : les utilisateurs ne pourront pas se connecter à l'application. Lors de l'exécution de
l'application, le message associé à la connexion interdite s'achera pendant la "durée d'achage des
messages" spéciée.
Les utilisateurs déjà connectés pourront utiliser l'application normalement.
Avertissement d'un arrêt imminent : le message d'avertissement associé s'achera sur les postes
utilisateurs connectés actuellement à l'application. Ce message s'achera :
pendant la "durée d'achage des messages" spéciée.
à chaque fois que l'application vériera son état en se connectant au poste serveur. Cette vérication est
eectuée à intervalle de temps régulier (déni dans l'option "Délai de vérication de l'état").
Si des utilisateurs tentent de se connecter à l'application, le message associé à la connexion interdite
s'achera.
Arrêt forcé : le message d'arrêt forcé associé s'achera sur les postes utilisateurs connectés actuellement à
l'application. Ce message s'achera :
pendant la "durée d'achage des messages" spéciée.
dès que l'application vériera son état en se connectant au poste serveur. Cette vérication est eectuée à
intervalle de temps régulier (déni dans l'option "Délai de vérication de l'état").
Après l'achage du message, les utilisateurs seront automatiquement déconnectés et ne pourront pas se
reconnecter.
Si des utilisateurs tentent de se connecter à l'application, le message associé à la connexion interdite
s'achera.
```
Les options de durée des contrôles sont les suivantes :


```
Délai de vérication de l'état : Dans une application installée en réseau, l'application utilisateur vérie à
intervalle de temps régulier :
son état en fonction de l'application serveur (application de référence).
si une mise à jour est disponible (après mise à jour de l'application de référence).
Durée d'achage des messages : Les diérents messages de WDADMINEXE (message de connexion
interdite, d'avertissement d'un arrêt imminent et d'arrêt forcé) sont achés pendant une durée spéciée. Les
utilisateurs peuvent fermer la fenêtre achant ce message avant la n de la durée spéciée.
```
Remarque : Lors de l'installation d'une mise à jour de l'application, les paramètres modiés dans WDADMINEXE
sont conservés. Pour retrouver les valeurs spéciées lors de la préparation de l'installation, cliquez sur le lien
"Rétablir les valeurs par défaut".

Gestion de déconnexion des utilisateurs automatique

Pour que la gestion de la déconnexion des utilisateurs de l'application soit automatique, il sut de sélectionner
l'option "Fonctionnement normal".

Si cette option est sélectionnée, lors de la mise à jour obligatoire de l'application sur le poste serveur, les
opérations suivantes sont automatiquement réalisées :

```
Les utilisateurs connectés actuellement à l'application sont listés.
Dès que l'application utilisateur vériera son état en se connectant au poste serveur, le message
d'avertissement d'arrêt imminent s'achera sur les postes utilisateurs. Ce message s'achera pendant la
durée d'achage des messages spéciée.
Après que tous les utilisateurs aient reçu le message d'avertissement d'arrêt imminent, la mise à jour de
l'application sur le poste serveur passe en mode "Arrêt forcé" pendant deux minutes.
Pendant ces deux minutes, le message d'arrêt forcé s'achera sur les postes utilisateurs.
Après ces deux minutes, les utilisateurs seront automatiquement déconnectés et ne pourront pas se
reconnecter jusqu'à la n de la mise à jour de l'application sur le poste serveur.
Après que la mise à jour de l'application sur le poste serveur soit eectuée, les utilisateurs se reconnectant à
l'application devront mettre à jour leur application utilisateur.
```
Si cette option est sélectionnée, lors de la mise à jour non obligatoire de l'application sur le poste serveur, les
opérations suivantes sont automatiquement réalisées :

```
La mise à jour de l'application sur le poste serveur s'eectue normalement.
Les utilisateurs connectés actuellement à l'application ne seront pas déconnectés.
```

```
Après que la mise à jour de l'application sur le poste serveur soit eectuée, les utilisateurs se reconnectant à
l'application pourront au choix installer la mise à jour ou lancer directement l'application.
```
Vérication des mises à jour

L'onglet "Contrôle" de WDADMINEXE permet de gérer la vérication des mises à jour :

Par défaut, la vérication de la disponibilité éventuelle d'une mise à jour sur le serveur est eectuée à chaque
lancement de l'application. Cette fréquence de vérication est paramétrable. Elle peut être eectuée :

```
A chaque ouverture de l'application.
Tous les X jours.
```
Une application installée via une installation réseau vérie à chaque lancement si une mise à jour est disponible
sur le serveur de référence.

```
Si une version plus récente est disponible sur le serveur, la mise à jour de l'application est proposée à
l'utilisateur nal.
Si la connexion réseau n'est pas trouvée à l'ouverture de l'application, le traitement par défaut est d'acher
un message d'avertissement.
Ce message peut être inutile dans le cadre d'une application utilisée sur un portable, connecté par
intermittence. Dans ce cas, il sut de sélectionner l'option "Vérication silencieuse : Ne pas informer
l'utilisateur"
```

## WINDEV

Présentation

L'onglet "Paramètres" de WDADMINEXE contient les informations concernant la dernière mise à jour disponible
de l'application :

```
Le chemin de WDADMINEXE (chier "WDADMINEXE.EXE") sur le poste serveur.
Le numéro de la version courante. Ce numéro correspond au numéro de version du dernier exécutable
installé.
Le numéro de la plus ancienne version compatible. Ce numéro correspond au numéro de version de
l'exécutable présent sur les postes utilisateurs à partir duquel la mise à jour n'est pas obligatoire.
Cette information a été spéciée lors de la création du programme d'installation :
soit dans l'assistant, étape "Live-update : Exécutable de référence pour le contrôle des versions".
soit dans l'éditeur d'installation WDInst, option "Paramètres de l'installation .. Assistant" puis option
"Installation réseau avec mise à jour automatique".
L' historique de la version courante. Cet historique contient les modications eectuées par le développeur
dans l'application pour la version courante. Cet historique a été saisi lors de la création du programme
d'installation de la version en cours. Il correspond à l'aide des nouveautés de la version.
La saisie de l'historique peut être eectuée :
Grâce à l'assistant de création du programme d'installation. Pour plus de détails, consultez les
Paramètres de la mise à jour d'une application installée en réseau.
Sous l'éditeur d'installation WDInst. Pour plus de détails, consultez
Options avancées pour l'installation réseau.
```
```
WEBDEV WINDEV Mobile Autres
```
# WDADMINEXE : Informations sur la

# dernière mise à jour disponible


## WINDEV

Présentation

L'onglet "Utilisateurs" de WDADMINEXE permet de connaître à partir du poste serveur :
Les utilisateurs connectés actuellement à l'application.
Pour chaque utilisateur connecté :
le poste de lancement de l'application,
la version de l'application utilisée.

```
Nom de l'exécutable de l'application dont les informations sont achées. Une même
application peut être associée à plusieurs exécutables.
```
```
Cadence de rafraîchissement d'achage des caractéristiques des utilisateurs.
```
```
WEBDEV WINDEV Mobile Autres
```
# WDADMINEXE : Caractéristiques des

# utilisateurs


```
Nom du poste à partir duquel l'application a été lancée. Ce nom a été déni dans les
propriétés réseau du poste.
```
```
Adresse IP du poste à partir duquel l'application a été lancée.
```
```
Nom de l'utilisateur du poste à partir duquel l'application a été lancée. Ce nom a été spécié
lors du lancement du poste.
```
```
Date de début de la connexion de l'utilisateur à l'application.
```
```
Heure de début de la connexion de l'utilisateur à l'application.
```
```
Version de l'application utilisée.
```
Notes

```
Les données achées proviennent des chiers "LOKxxx.tmp" présents dans le sous-répertoire
"\INSTALL\LOCK" du répertoire d'installation de l'application sur le poste serveur. Ces chiers sont
temporaires (présent uniquement pendant la durée de la connexion).
Si la gestion des utilisateurs n'est pas intégrée dans le programme d'installation de l'application, l'onglet
"Utilisateurs" sera grisé. Pour intégrer la gestion des utilisateurs dans le programme d'installation, consultez
Gestion des utilisateurs d'une application.
```

## WINDEV

Présentation

L'onglet "Versions" de WDADMINEXE permet de gérer à partir du poste serveur les versions installées sur les
postes client.

Gestion des versions

L'onglet "Versions" permet de :
Connaître la version actuelle. Cette version est utilisée par les postes clients qui sont à jour.
Voir les versions disponibles : Ces versions sont installées sur le poste serveur. Il est possible de choisir le type
de version à acher grâce au bouton "Acher" :
version active : version actuellement utilisée.
version disponible : version disponible sur le serveur.
version interdite : version disponible sur le serveur mais dont l'utilisation est interdite.

Pour chaque version sélectionnée, il est possible de :

```
Voir l'aide des nouveautés.
Interdire la version : La version sélectionnée ne pourra pas être installée sur les postes client.
Autoriser la version : Permet d'autoriser une version précédemment interdite.
```
```
WEBDEV WINDEV Mobile Autres
```
# WDADMINEXE : Gestion des versions


```
Forcer la version : Permet de forcer l'utilisation de la version sélectionnée. Seule une version activée peut
être forcée. Si la version est forcée, lors du prochain contrôle de la mise à jour, le poste client ne pourra pas
refuser la mise à jour.
Libérer la version : Permet de libérer une version précédemment forcée.
Activer la version : Active la version sélectionnée. Par défaut, une version installée est automatiquement
activée. Mais il est possible de l'installer sans l'activer puis de l'activer plus tard, via WDADMINEXE.
```
Remarque : Les informations disponibles dans cet onglet sont achées uniquement si l'historique des versions
a été activé lors de la création du programme d'installation :

```
Dans l'assistant de création d'installation, cette activation est réalisée dans l'étape "Installation de référence -
Historique des versions".
```

Dans l'éditeur WDInst, cette activation est réalisée grâce à l'option "Paramètres de l'installation .. Assistant",
option "Installation réseau avec mise à jour automatique", bouton "Options avancées", onglet "Mise à jour
automatique", bouton "Paramètres de l'historique des versions".


## WINDEV

Présentation

WDADMINEXE permet de déployer des applications réseau en push via l'onglet "Push". L'installation avec prise en
charge du Push permet de déployer une application sur tous les postes clients d'un réseau depuis un unique
poste d'administration.

Ce mode d'installation est une option de l'installation en réseau local avec mise à jour automatique (Live Update).

Comment le faire?

Déployer en Push sur les postes clients

Pour déployer en push sur les postes clients :

1. Lancez WDAdminExe (voir ci-dessus).
2. Achez l'onglet "Push" de la fenêtre principale :

```
WEBDEV WINDEV Mobile Autres
```
# WDADMINEXE : Gestion des

# installations en mode push


3. Saisissez dans "Listage des machines" (1) le nom d'utilisateur et le mot de passe d'un compte Windows
    disposant d'assez de droits pour énumérer les machines du réseau.
    Remarques :
       Dans un Active Directory, le nom d'utilisateur doit être au format DOMAINE\UTILISATEUR et/ou au format
       UTILISATEUR@DOMAINE.
       Ce compte n'a pas besoin d'être un administrateur.
       Il est possible de mémoriser les informations de connexion. Si cette option est utilisée, il est important de
       ne pas mémoriser le mot de passe d'un administrateur.
       Il est également possible de charger une liste de machines à partir d'un chier texte. Le chier texte peut
       contenir :
          des noms de machines ou des adresses IP.
          des commentaires sous la forme "// Commentaire".
       Chaque ligne doit contenir un nom (ou adresse IP) et un commentaire. Par exemple :
       VIB //Machine de Vincent
       FP //Machine de Florence
4. Cliquez sur "Lister les machines" pour valider les informations de connexion et commencer l'énumération des
    postes clients.
    Attention : en fonction des stratégies LDAP dénies dans Active Directory, l'importation peut être limitée à 1
    000 utilisateurs. Dans ce cas, pour supprimer cette limitation, il faut intervenir sur le paramètre LDAP
    MaxPageSize. Pour plus de détails, consultez https://support.microsoft.com/kb/315071.
5. Vous pouvez utiliser les critères (2) ainsi que la liste des groupes (3) pour ltrer les machines à acher. La
    liste des groupes est disponible uniquement sur un domaine Active Directory.
6. La table des machines (4) ache :
    les postes clients trouvés,
    le commentaire s'il existe du chier texte.
    le numéro de version de l'application si elle est déjà installée,
    le résultat des précédentes installations en Push.
7. Sélectionnez les postes clients sur lesquels l'application doit être déployée en mode Push.


8. Cliquez sur "Lancer l'installation en PUSH..." pour déclencher l'installation.
    La fenêtre de lancement de l'installation s'ache :
9. Si plusieurs versions de l'application sont présentes dans l'installation de référence, sélectionnez la version de
    l'application à déployer en Push (1).
10. Le résumé (2) vous rappelle la liste des machines cibles de l'installation. Il est possible de supprimer des
machines dans cette liste grâce au menu contextuel.
11. Vous pouvez utiliser un compte Windows diérent de celui qui a servi à énumérer les machines si nécessaire
(3).
12. Vous pouvez programmer l'installation en Push pour qu'elle soit réalisée en diéré (4). Cette option permet
de mettre automatiquement à jour un parc complet de postes clients en dehors des heures de travail par
exemple.
13. La validation de cette fenêtre provoque le début des installations en Push. L'avancement peut être suivi dans
la table des machines de la fenêtre principale de WDADMINEXE.

```
Remarque : Un bouton "Avancé" permet de paramétrer la durée d'attente des installations en Push. Si de
nombreuses installations échouent avec des erreurs de timeout, il peut être nécessaire d'ajuster ce paramètre.
```
```
Services nécessaires sur les postes cibles
Remarque : Selon les versions de Windows utilisées, les noms de ces services dans la panneau de conguration
peuvent varier.
Sur les postes cibles de l'installation en mode Push, les services suivants doivent être démarrés :
Partage de chiers (Service "lanmanserveur")
Accès au registre à distance / Registre Distant (Service "RemoteRegistry")
```

De plus, le partage administratif (ADMIN$) doit exister. Ce partage peut être vu dans l'outil d'administration
"Gestion de l'ordinateur", dans la partie "Outils système .. Dossiers partagés .. Partages".

Services nécessaires sur le poste réalisant l'installation en Push

Sur le poste réalisant l'installation en mode Push, le service "Station de travail" ("lanmanworkstation") doit être
démarré.


