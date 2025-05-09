### WINDEV WEBDEV

Présentation

Le robot de surveillance permet de gérer des groupes d'utilisateurs qui seront concernés par les diérents
rapports d'erreur des contrôles.

Pour gérer les groupes d'utilisateurs :

1. Dans le menu du moniteur, dans le groupe "Paramétrage", cliquez sur "Gérer les groupes".
2. La fenêtre qui s'ache permet de :
    Ajouter ou supprimer un utilisateur dans un groupe.
    Ajouter un groupe.
    Renommer un groupe.
    Supprimer un groupe.

Caractéristiques d'un groupe

Lors de l'ajout d'un groupe, il sut d'indiquer son nom dans la fenêtre qui s'ache. Le nouveau groupe
apparaît ensuite dans la liste des groupes.
Pour associer un utilisateur à un groupe, il sut de sélectionner le groupe voulu dans la liste des groupes et
de "cocher" les utilisateurs membres de ce groupe.

Lorsque le groupe est créé, il peut être utilisé comme destinataire du rapport d'erreur d'un contrôle (dans les
paramètres généraux du contrôle).

```
WINDEV Mobile Autres
```
## Conguration des groupes

## d'utilisateurs


### WINDEV WEBDEV

Présentation

Un robot de surveillance est livré avec WINDEV, WEBDEV et WINDEV Mobile. Ce robot permet de vérier
qu'une application ou un serveur fonctionne. En cas de défaillance de l'élément surveillé (panne matérielle,
arrêt de la liaison Internet, arrêt du système, etc.), le robot a pour mission de lancer les alertes qui ont été
dénies.

Principe

Composé de trois exécutables lancés sur diérents postes, le robot de surveillance permet d'exécuter
diérents tests : test Internet, test serveur FTP, test réseau, etc.

Le robot de surveillance est un ensemble logiciel composé de :

```
un moniteur permettant de congurer et visualiser l'état du robot et des diérents contrôles.
un robot de surveillance réalisant de manière périodique des contrôles sur l'infrastructure ou les
applications.
éventuellement un contre-robot qui vérie le fonctionnement du robot lui-même.
```
En cas de problèmes lors du passage d'un test, le robot de surveillance peut vous avertir de diérentes
façons :

```
Message envoyé aux personnes indiquées dans la messagerie intégrée (WDBal).
Message email envoyé aux adresses indiquées.
Message envoyé à une application spécique.
Utilisation d'un écran de contrôle (message visuel et/ou sonore).
Lancement d'une procédure WLangage.
Exécution d'un programme tiers.
```
```
WINDEV Mobile Autres
```
## Présentation du robot de

## surveillance


Comment installer le robot de surveillance?

Pour utiliser le robot de surveillance, il est nécessaire d'installer les diérents programmes du robot de
surveillance. Le pack d'installation (WX2025PACKROBOT.EXE) est disponible dans le sous-répertoire
"Install\Robot" du produit utilisé.

L'installation des diérents modules doit être faite selon l'ordre suivant :

1. Installation du robot de surveillance. Le robot de surveillance doit être installé sur un poste qui ne sera
    jamais éteint.
2. Installation si nécessaire du contre-robot. Le contre-robot est une sécurité supplémentaire. Il permet de
    surveiller le bon fonctionnement du robot de surveillance.
3. Installation du moniteur. Le moniteur peut être installé sur plusieurs postes. Le moniteur permet de
    congurer les diérents tests eectués par le robot de surveillance.

Remarque : Les trois programmes doivent être installés sur le même réseau local ou sur le même domaine.

Comment utiliser le robot de surveillance?

Utilisation

Pour utiliser le robot de surveillance, le robot doit être lancé (et le contre-robot si nécessaire).


Le moniteur peut être lancé pour gérer les tests à eectuer.

Utilisation du moniteur

Le moniteur du robot de surveillance permet d'avoir à tout moment accès aux diérents contrôles lancés par
le robot de surveillance.

Il permet de :

```
Créer, modier ou supprimer un contrôle.
Créer, modier ou supprimer un modèle de contrôle.
Dupliquer un contrôle.
Rechercher un contrôle.
Exécuter un contrôle.
Congurer :
le moniteur
le robot
le contre-robot
les utilisateurs
Acher l'historique.
```
Composant ComposantsRobots

Un composant permettant de gérer le robot de surveillance est livré avec WINDEV. Ce composant est un
composant utilitaire, nommé "ComposantsRobots".

Le composant du robot de surveillance permet à l'application :

```
de signaler son activité par écriture dans un chier .ini.
de parcourir un rapport d'erreur au format XML fourni par le robot de surveillance.
```

### WINDEV WEBDEV

Présentation

Le robot de surveillance est constitué de trois exécutables.

Le premier exécutable à installer est l'exécutable correspondant au robot. Le robot de surveillance tourne en
permanence sur un poste et lance tous les tests demandés. Il doit être installé sur un poste qui ne sera jamais
éteint.

Le second exécutable est le contrôleur du robot (ou contre-robot). Son installation n'est pas obligatoire. Le
contre-robot est une sécurité en plus. Il permet de surveiller le bon fonctionnement du robot de surveillance.
S'il est installé, le contre-robot doit être installé sur un poste qui ne sera jamais éteint, diérent du poste
d'installation du robot de surveillance.

Le troisième exécutable est le moniteur des robots. Le moniteur peut être installé sur n'importe quel poste. Il
permet d'éditer les tests et les diérents paramètres du robot.

Assistant d'installation du moniteur

Installer le moniteur

Pour installer le moniteur :

1. Lancez le pack d'installation (WX2025PACKROBOT.EXE) sur le poste où le moniteur doit être installé.
    L'assistant d'installation se lance.
    Rappel : Le pack d'installation (WX2025PACKROBOT.EXE) est disponible dans le sous-répertoire
    "Install\Robot" du produit utilisé.
2. Validez la licence.
3. Sélectionnez l'option "Installer le moniteur des Robots" et passez à l'étape suivante.
4. Sélectionnez le répertoire d'installation du moniteur des robots. Passez à l'étape suivante.
5. L'installation est terminée. Validez. L'installation du moniteur des robots est réalisée. Il vous sut
    maintenant de paramétrer le moniteur des robots.

Paramétrage du moniteur des robots

A la n de l'installation du moniteur, un assistant est automatiquement aché pour congurer le moniteur.

1. Passez à l'étape suivante.

```
WINDEV Mobile Autres
```
## Installation du moniteur


2. Indiquez l'emplacement de la base de données du robot de surveillance. Cette base de données peut être :
    Une base de données HFSQL Client/Serveur. Dans ce cas, indiquez :
       l'adresse du serveur, son port,
       le nom d'utilisateur et le mot de passe associé,
       la base de données à utiliser.
    Une base de données HFSQL Classic, présente dans un répertoire partagé. Ce répertoire correspond au
    répertoire partagé créé sur le poste où le robot a été installé.
3. Passez à l'étape suivante.
4. Sélectionnez les options d'alerte du moniteur. Ces options correspondent à l'alerte eectuée sur le
    moniteur en cas d'erreur. Il est possible :
       d'utiliser une alerte visuelle.
       d'utiliser une alerte sonore.
5. Passez à l'étape suivante. Validez. Le paramétrage du moniteur est réalisé.

Vous pouvez créer des tests.


### WINDEV WEBDEV

Présentation

Le robot de surveillance est constitué de trois exécutables.

Le premier exécutable à installer est l'exécutable correspondant au robot. Le robot de surveillance tourne en
permanence sur un poste et lance tous les tests demandés. Il doit être installé sur un poste qui ne sera jamais
éteint.

Le second exécutable est le contrôleur du robot (ou contre-robot). Son installation n'est pas obligatoire.
Le contre-robot est une sécurité en plus. Il permet de surveiller le bon fonctionnement du robot de
surveillance. S'il est installé, le contre-robot doit être installé sur un poste qui ne sera jamais éteint, diérent
du poste d'installation du robot de surveillance.

Le troisième exécutable est le moniteur des robots. Le moniteur peut être installé sur n'importe quel poste. Il
permet d'éditer les tests et les diérents paramètres du robot.

Assistant d'installation du contrôleur du robot

Installer le contrôleur du robot

Pour installer le contrôleur du robot :

1. Lancez le pack d'installation (WX2025PACKROBOT.EXE) sur le poste où le contrôleur du robot doit être
    installé. Rappel : Le pack d'installation (WX2025PACKROBOT.EXE) est disponible dans le sous-répertoire
    "Install\Robot" du produit utilisé.
2. Validez la licence.
3. Sélectionnez l'option "Installer le Contrôleur du Robot" et passez à l'étape suivante.
4. Sélectionnez le répertoire d'installation du contrôleur du robot. Passez à l'étape suivante.
5. L'installation est terminée. Validez. L'installation du contrôleur du robot est réalisée. Il vous sut
    maintenant de paramétrer le contrôleur du robot.

Paramétrage du contre-robot

A la n de l'installation du contre-robot, un assistant est automatiquement aché pour congurer le contre-
robot. Dans cet assistant :

1. Indiquez le nom du contre-robot. Ce nom sera utilisé dans les diérents rapports envoyés. Il est conseillé
    d'utiliser un nom facilement identiable. Passez à l'étape suivante.
2. Indiquez l'emplacement des chiers de données du robot. Ce répertoire correspond au répertoire partagé
    créé sur le poste où le robot a été installé. Passez à l'étape suivante.

```
WINDEV Mobile Autres
```
## Installation du contrôleur du robot


3. Sélectionnez les options d'alerte du contre-robot. Ces options seront utilisées par défaut pour tous les tests
    réalisés par le robot de surveillance. Il est possible :
       d'utiliser la messagerie interne de WINDEV et WEBDEV : WDBal. Cette option suppose que la base de
       données des Centres de Contrôle est accessible depuis le poste du robot de surveillance.
       d'envoyer les messages par emails. Cette option suppose que le poste du robot de surveillance à accès
       à un serveur d'emails.
       d'utiliser un programme tiers, qui eectuera un traitement spécique des messages. Ce programme
       tiers devra être accessible depuis le poste du robot de surveillance.
       Le choix des alertes du contre-robot peut être également réalisé dans le moniteur. Il est conseillé de
       sélectionner au moins une des options d'alerte pour le contre-robot.
4. Passez à l'étape suivante. Ce plan dépend des options cochées précédemment.
    Si la messagerie WDBal doit être utilisée, indiquez :
       le nom de l'expéditeur du message (et si nécessaire le mot de passe associé). Ce nom doit
       correspondre à celui d'un intervenant existant dans la base des Centres de Contrôle.
       les destinataires par défaut. Le nom indiqué dans le tableau doit correspondre à celui d'un
       intervenant existant dans la base des Centres de Contrôle.
       Remarque : Il sera possible d'ajouter de nouveaux destinataires depuis le moniteur.
       les paramètres d'accès à la base de données des Centres de Contrôle :
          répertoire de la base de données si les chiers utilisent un partage réseau.
          caractéristiques de la base de données HFSQL Client/Serveur (Serveur, Port, Base).

```
Si un email doit être envoyé, indiquez :
l'adresse email de l'expéditeur. Cette adresse est celle achée dans l'email.
les caractéristiques du serveur SMTP à utiliser pour l'envoi des messages : serveur, port, utilisateur
et mot de passe associé (ces caractéristiques sont fournies par le fournisseur d'accès Internet).
les adresses email des destinataires par défaut.
Remarque : Il sera possible d'ajouter de nouveaux destinataires depuis le moniteur.
Si un programme tiers doit être utilisé, indiquez le chemin de l'exécutable à lancer.
```
5. Indiquez le compte Windows (et le mot de passe associé) permettant de créer la tâche planiée qui lancera
    le contre-robot. Attention : ce compte doit avoir les droits d'administration pour eectuer cette opération.
    Si un domaine est utilisé, précisez le nom du domaine.
    Remarque : Si des noms de domaine sont utilisés, les trois programmes (robot, contre-robot et moniteur)
    doivent être installés sur le même domaine.
    Passez à l'étape suivante.
6. L'installation est terminée. Validez. Le paramétrage du contre-robot est réalisé.

Remarque : Pour exécuter à nouveau l'assistant de paramétrage, le contre-robot doit être lancé en ajoutant le
paramètre /CONFIG dans sa ligne de commande.
Par exemple :


C:\Program Files (x86)\PC SOFT\Contrôleur du robot\RobotController.exe /CONFIG

Vous pouvez installer un moniteur de surveillance.


### WINDEV WEBDEV

Présentation

Le robot de surveillance est constitué de trois exécutables.

Le premier exécutable à installer est l'exécutable correspondant au robot. Le robot de surveillance tourne
en permanence sur un poste et lance tous les tests demandés. Il doit être installé sur un poste qui ne sera
jamais éteint.

Le second exécutable est le contrôleur du robot (ou contre-robot). Son installation n'est pas obligatoire. Le
contre-robot est une sécurité en plus. Il permet de surveiller le bon fonctionnement du robot de surveillance.
S'il est installé, le contre-robot doit être installé sur un poste qui ne sera jamais éteint, diérent du poste
d'installation du robot de surveillance.

Le troisième exécutable est le moniteur des robots. Le moniteur peut être installé sur n'importe quel poste. Il
permet d'éditer les tests et les diérents paramètres du robot.

Assistant d'installation du robot de surveillance

Installation du robot

Pour installer le robot de surveillance :

1. Lancez le pack d'installation (WX2025PACKROBOT.EXE) sur le poste où le robot doit être installé. Rappel : Le
    pack d'installation (WX2025PACKROBOT.EXE) est disponible dans le sous-répertoire "Install\Robot" du
    produit utilisé.
2. Dans l'assistant d'installation, acceptez les termes de la licence et passez à l'étape suivante.
3. Sélectionnez l'option "Installer le Robot de surveillance" et passez à l'étape suivante.
4. Sélectionnez le répertoire d'installation du robot de surveillance. Passez à l'étape suivante.
5. L'installation est terminée. Validez. L'installation du robot de surveillance est réalisée. Il vous sut
    maintenant de paramétrer le robot de surveillance.

Paramétrage du robot de surveillance

A la n de l'installation du robot de surveillance, un assistant est automatiquement lancé pour congurer le
robot de surveillance.

1. Indiquez le nom du robot. Ce nom sera utilisé dans les diérents rapports et messages envoyés. Il est
    conseillé d'utiliser un nom facilement identiable. Passez à l'étape suivante.

```
WINDEV Mobile Autres
```
## Installation du robot de surveillance


2. Indiquez si un contre-robot va être déployé. Le contre-robot est chargé de contrôler régulièrement l'activité
    du robot de surveillance. L'installation d'un contre-robot n'est pas obligatoire mais c'est une sécurité
    supplémentaire.
    Si un contre-robot doit être installé, indiquez le nom de la machine sur lequel sera installé le contre-robot.
    Passez au plan suivant.
3. Sélectionnez les options d'alerte du robot de surveillance. Ces options seront utilisées par défaut pour tous
    les tests réalisés par le robot de surveillance. Il est possible :
       d'utiliser la messagerie interne de WINDEV, WEBDEV, WINDEV Mobile : WDBal. Cette option suppose
       que la base de données des Centres de Contrôle est accessible depuis le poste du robot de surveillance.
       d'envoyer les messages par emails. Cette option suppose que le poste du robot de surveillance à accès
       à un serveur d'emails.
       d'utiliser un programme tiers, qui eectuera un traitement spécique des messages. Ce programme
       tiers devra être accessible depuis le poste du robot de surveillance.
       Si aucune de ces options n'a été sélectionnée, la seule alerte congurée sera une alerte sonore et
       visuelle sur le moniteur.
       A tout moment, il sera possible depuis le moniteur, de modier ces options.
4. Passez au plan suivant. Ce plan dépend des options cochées précédemment.
    Si la messagerie WDBal doit être utilisée, indiquez :
       le nom de l'expéditeur du message (et si nécessaire le mot de passe associé). Ce nom doit
       correspondre à celui d'un intervenant existant dans la base des Centres de Contrôle.
       les destinataires par défaut. Le nom indiqué dans le tableau doit correspondre à celui d'un
       intervenant existant dans la base des Centres de Contrôle.
       Remarque : Pour chaque test, il sera possible d'ajouter de nouveaux destinataires.
       les paramètres d'accès à la base de données des Centres de Contrôle :
          répertoire de la base de données si les chiers utilisent un partage réseau.
          caractéristiques de la base de données HFSQL Client/Serveur (Serveur, Port, Base).

```
Si un email doit être envoyé, indiquez :
l'adresse email de l'expéditeur. Cette adresse est celle achée dans l'email.
les caractéristiques du serveur SMTP à utiliser pour l'envoi des messages : serveur, port, utilisateur
et mot de passe associé (ces caractéristiques sont fournies par le fournisseur d'accès Internet).
les adresses email des destinataires par défaut.
Remarque : Pour chaque test, il sera possible d'ajouter de nouveaux destinataires.
Si un programme tiers doit être utilisé, indiquez le chemin le chemin de l'exécutable à lancer.
```

5. Indiquez le compte Windows (et le mot de passe associé) permettant de créer la tâche planiée qui lancera
    le robot de surveillance. Attention : ce compte doit avoir les droits d'administration pour eectuer cette
    opération.
    Si un domaine est utilisé, indiquez également le nom du domaine.
    Remarque : Si des noms de domaine sont utilisés, les trois programmes (robot, contre-robot et moniteur)
    doivent être installés sur le même domaine.
    Passez au plan suivant.
6. Indiquez le nom du répertoire partagé (par exemple "MonRobot") qui permettra aux moniteurs (installés
    sur d'autres postes) et/ou au contre-robot d'accéder aux données des tests. Ce répertoire sera créé sur le
    poste en cours et automatiquement partagé.
7. L'installation est terminée. Validez. Le paramétrage du robot de surveillance est réalisé.

Vous pouvez :

```
soit installer le contre-robot (optionnel).
soit installer un moniteur de surveillance.
```

### WINDEV WEBDEV

Présentation

Le robot de surveillance permet de gérer les utilisateurs qui seront concernés par les diérents rapports
d'erreur des contrôles.

Pour gérer les utilisateurs :

1. Dans le menu du moniteur, dans le groupe "Paramétrage", cliquez sur "Gérer les utilisateurs".
2. La fenêtre qui s'ache permet de :

```
Fusionner deux utilisateurs.
Ajouter un utilisateur.
Editer un utilisateur.
Supprimer un utilisateur.
```
Caractéristiques d'un utilisateur

Lors de l'ajout ou de la modication d'un utilisateur, la fenêtre des caractéristiques d'un utilisateur est
achée.

```
WINDEV Mobile Autres
```
## Conguration des utilisateurs


Il est possible de dénir :

```
les options d'alerte :
Ces options permettent de dénir si une alerte visuelle ou sonore doit être utilisée en cas d'erreur. Si une
option sonore est choisie, il est possible de choisir un son personnalisé (chier ".Wav") grâce au bouton
"Choisir".
```

les options utilisateur :
Ces options permettent de dénir :

```
le login WDBal associé à l'utilisateur. Ce login sera utilisé pour les rapports à envoyer par l'application
de messagerie WDBal.
l'adresse email de l'utilisateur. Cette adresse email sera utilisée pour les rapports à envoyer par email.
```
les options concernant le rapport de synthèse :
Le rapport de synthèse contient :

```
l'historique des modications réalisées sur les contrôles.
les erreurs des diérents contrôles.
```
Ce rapport est conseillé aux administrateurs. Il est possible de spécier :

```
la fréquence de l'envoi du rapport,
le mode d'envoi utilisé (application WDBal ou email).
```
les options concernant les récapitulatifs :
Le récapitulatif contient la liste des contrôles en erreur. Il permet un point régulier sur les problèmes
rencontrés. Il est possible de spécier :

```
les heures d'envoi du récapitulatif,
la liste des contrôles à prendre en compte dans le récapitulatif (bouton de sélection).
le mode d'envoi du récapitulatif (application WDBal ou email).
```
les niveaux d'erreurs gérés pour l'utilisateur :
Chaque utilisateur peut selon le niveau de l'erreur du contrôle demander ou non l'envoi du rapport. Ainsi,
le responsable réseau peut par exemple ne pas vouloir les informations de débogage.


### WINDEV WEBDEV

Présentation

Depuis le moniteur, il est possible de modier les options de conguration :
du robot,
du contre-robot,
du moniteur.

Conguration des paramètres du robot

Les paramètres du robot correspondent aux paramètres indiqués dans l'assistant de conguration du robot.

Pour acher les paramètres du robot :

1. Dans le menu, dans le groupe "Paramétrage", cliquez sur "Paramétrer" puis sélectionnez l'option
    "Paramètres du robot de surveillance".
2. La fenêtre qui s'ache reprend les caractéristiques du robot :
    Nom, machine, répertoire d'accès.
    Options d'alerte. Ces options d'alerte sont congurables pour :
       alerte via WDBal,
       alerte via Email,
       alerte via programme tiers,
    En cas d'alerte par Email ou WDBal, il est possible de paramétrer le rapport envoyé.

Options d'alerte

Alerte par WDBal

L'onglet "WDBal" permet de paramétrer l'envoi de rapport d'erreurs par la messagerie PC SOFT nommée
WDBal. Pour utiliser ce mode de message d'alerte, la base de données des Centres de Contrôle doit être
accessible depuis le poste où le robot est installé.

```
WINDEV Mobile Autres
```
## Robot de surveillance :

## Conguration des paramètres du

## robot


Si l'option d'envoi de messages par WDBal est activée (option "Envoi par WDBal activé" cochée), ce mode
d'alerte sera utilisé par défaut pour tous les contrôles présents dans le moniteur. Il est ensuite possible pour
chaque utilisateur de dénir des paramètres spéciques.

La section "Conguration de WDBal" permet de dénir le mode d'accès aux données des Centres de Contrôle :

```
En mode partage réseau : répertoire des chiers de données.
En mode HFSQL Client/Serveur : serveur utilisé, port et base de données, ainsi que l'utilisateur et le mot de
passe.
```
Alerte par email

L'onglet "Email" permet de paramétrer l'envoi de rapport d'erreurs par email. Pour utiliser ce mode de
message d'alerte, un serveur SMTP doit être accessible depuis le poste où le robot est installé.

Si l'option d'envoi de messages par email est activée (option "Envoi par Email activé" cochée), ce mode d'alerte
sera utilisé par défaut pour tous les contrôles présents dans le moniteur. Il est ensuite possible pour chaque
utilisateur de dénir des paramètres spéciques.

La section "Conguration de l'envoi d'emails" permet de dénir les caractéristiques du serveur SMTP utilisé :

```
Serveur et port SMTP.
```

```
Utilisateur et mot de passe associé pour utiliser le serveur SMTP.
Sécurité utilisée.
```
Utilisation d'un programme tiers

L'onglet "Programme tiers" permet de :
paramétrer l'envoi du rapport d'erreurs à un programme spécique. Ce programme tiers se chargera de
traiter les messages d'alerte.
Pour utiliser ce mode de message d'alerte, indiquez le chemin de l'exécutable voulu. Cet exécutable doit
être accessible depuis le poste d'installation du robot.
spécier une Webhook. L'appel à la webhook sera réalisé après chaque exécution de tests, en passant en
paramètre un chier JSON.
Pour utiliser une webhook, il sut de spécier l'URL de la Webhook à appeler.

Envoi du rapport d'erreur à un programme tiers
Dans ce mode d'envoi, le rapport d'erreur est un chier XML. Le chemin du rapport d'erreur sera passé en
ligne de commande au programme tiers et devra être traité par ce programme.

Le format du chier XML est le suivant :
<Test>
<NumeroTest>%1</NumeroTest>
<NomTest>%2</NomTest>
<CategorieTest>%3</CategorieTest>
<PrioriteTest>%4</PrioriteTest>
<SyntaxeTest>
%
</SyntaxeTest>
<SolutionTest>
%


</SolutionTest>
<DateErreur>%7</DateErreur>
<HeureErreur>%8</HeureErreur>
<MessageErreurPersonnel>
%
</MessageErreurPersonnel>
<MessageErreur>
%
</MessageErreur>
</Test>
<Test>
...
</Test>

Dans ce code :

```
%1 = Numéro identiant le test
%2 = Nom du test
%3 = Nom de la catégorie du test
%4 = Priorité du test
%5 = Syntaxe du test (paramètres associées)
%6 = Solution proposée pour le test
%7 = Date de l'erreur
%8 = Heure de l'erreur
%9 = Message d'erreur renseigné dans la che du test
%10 = Message d'erreur renvoyé par le robot
```
Si l'option d'envoi de messages par programme tiers est activée (option "Envoi par programme tiers activé"
cochée), ce mode d'alerte sera utilisé par défaut pour tous les contrôles présents dans le moniteur.

Appel d'une webhook
L'appel sera réalisé après chaque test exécuté, en passant en paramètre un chier JSON.

Le chier JSON a le format suivant :

{
 "RobotName": "Nom robot",
 "ControlName": "Nom du contrôle",
 "ControlCategory": "Nom de la catégorie",
 "Severity": "Niveau erreur"
 "ResponsibleList": "Responsable",
 "FirstError": "DateHeure de la première erreur",
 "ErrorMessage": "Message d'erreur",
 "IsError": 0/


 "CustomError" : "Message personnalisé"
}

Les éléments présents dans le chier JSON sont les suivants :

```
RobotName : nom du robot de surveillance (utile si vous avez plusieurs robots dans votre organisation et si
vous souhaitez tous les orienter vers la même webhook).
ControlName : nom (libellé) du contrôle.
ControlCategory : nom (libellé) de la catégorie du contrôle.
Severity : niveau de gravité du contrôle. En version 26, ce paramètre vaut toujours "Erreur".
ResponsibleList : liste des utilisateurs recevant les alertes de ce contrôle.
FirstError : date et heure de la première erreur signalée. Ce membre est utile pour savoir depuis combien
de temps un contrôle est en erreur.
IsError : booléen indiquant si le contrôle est en erreur.
ErrorMessage : message d'erreur du contrôle.
CustomError : message de complément d'erreur (qui a été saisi dans les paramètres du contrôle, depuis le
moniteur du robot).
```
Remarque : Si vous souhaitez réaliser une Webhook en WEBDEV :

1. Créez un projet WEBDEV avec une page AWP vide.
2. Dans la page AWP :
    Déclarez la structure d'export :

## // Structure d'export

# STWebHookExport est une Structure

# RobotName est une chaîne

# ControlName est une chaîne

# ControlCategory est une chaîne

# Severity est une chaîne

# ResponsibleList est une chaîne

# FirstError est une DateHeure

# ErrorMessage est une chaîne

# IsError est un booléen

# CustomError est une chaîne

## FIN

# gtabInfoWebhook est un tableau de STWebHookExport

```
Récupérez et désérialisez les données avant de les utiliser :
```
# bufDonnéesPOST est un Buffer = PageParamètre( paramBuffer )

## Désérialise(gtabInfoWebhook,bufDonnéesPOST, psdJSON )

Liste des exemples associés :


```
Exemples didactiques (WEBDEV) : WW_Statut_Liste
```
Paramétrage du rapport

L'onglet "Paramétrage du rapport" permet de paramétrer le sujet du message envoyé (par email ou par
WDBal).

```
La section "Objet de l'email envoyé" permet de construire le titre du message. Des macros permettent
d'obtenir des informations spéciques (nom du robot, nombre de contrôles en erreur, ...).
```
```
[ + ] Cet exemple est une implémentation très simple de la webhook mise à disposition par le robot
```

La section "Mode d'alerte" permet de choisir le mode d'alerte retenu :

```
Mode "Alerte continue" (par défaut) :
Si un contrôle donné est en erreur plusieurs fois de suite (par exemple, si le serveur ne répond pas
pendant plusieurs minutes), le robot enverra systématiquement une alerte pour chaque erreur.
Mode "Panne/reprise"
Si un contrôle donné est en erreur plusieurs fois de suite (par exemple, si le serveur ne répond pas
pendant plusieurs minutes), le robot eectue les opérations suivantes :
```
1. Le robot enverra une alerte lors de la première erreur détectée.
2. Le robot enverra des alertes intermédiaires, toutes les xx minutes. Le délai entre chaque envoi est
paramétrable.
Il est également possible de n'envoyer aucun message intermédiaire.
3. Le robot enverra un message lorsque le contrôle ne sera plus en erreur (par exemple si le serveur est
redémarré).
Notes :
    Le mode "Panne/Reprise" s'applique à tous les contrôles (il n'est pas possible de préciser ce mode
    pour un contrôle en particulier).
    Si ce mode est activé et que le robot surveille des éléments sensibles, il est conseillé d'envoyer des
    messages intermédiaires.
    Exemple de déroulement :

```
Temps Etat du contrôle Mode Alerte
continue
```
```
Mode Panne/Reprise
```
```
Instant T Contrôle en erreur Alerte envoyée Alerte envoyée
```
```
Instant T+1 Contrôle en erreur Alerte envoyée Aucune alerte
envoyée
```
```
Instant T+2 Contrôle en erreur Alerte envoyée Aucune alerte
envoyée
```
```
Instant T+3 Contrôle en erreur Alerte envoyée Aucune alerte
envoyée
```
```
Instant T+4 Contrôle en erreur Alerte envoyée Aucune alerte
envoyée
```
```
Instant T+5 Contrôle correct Aucune alerte
envoyée
```
```
Alerte envoyée
```

### WINDEV WEBDEV

Présentation

Depuis le moniteur, il est possible de modier les options de conguration :
du robot,
du contre-robot,
du moniteur.

Conguration des paramètres du contre-robot

Les paramètres du contre-robot correspondent aux paramètres indiqués dans l'assistant de conguration du
contre-robot.

Pour acher les paramètres du contre-robot :

1. Dans le menu du moniteur, dans le groupe Paramétrage", cliquez sur "Paramétrer" puis sur "Paramètres
    du contre-robot".
2. La fenêtre qui s'ache reprend les caractéristiques du contre-robot :
    Nom, Machine.
    Options d'alerte.

Options d'alerte

Alerte par WDBal

L'onglet "WDBal" permet de paramétrer l'envoi de rapport d'erreurs par la messagerie PC SOFT nommée
WDBal. Pour utiliser ce mode de message d'alerte, la base de données des Centres de Contrôle doit être
accessible depuis le poste où le contre-robot est installé.

La section "Conguration de WDBal" permet de dénir le mode d'accès aux données des Centres de Contrôle :

```
En mode partage réseau : répertoire des chiers de données.
En mode HFSQL Client/Serveur :
serveur utilisé, port et base de données.
utilisateur et mot de passe.
```
```
WINDEV Mobile Autres
```
## Robot de surveillance :

## Conguration des paramètres du

## contre-robot


La section "Conguration des intervenants" permet de dénir le ou les destinataires par défaut du message
envoyé par la messagerie (bouton "Dénir les destinataires"). Les destinataires proposés sont les utilisateurs
ayant activé un envoi par WDBal.

Alerte par email

L'onglet "Email" permet de paramétrer l'envoi de rapport d'erreurs par email. Pour utiliser ce mode de
message d'alerte, un serveur SMTP doit être accessible depuis le poste où le contre-robot est installé.

La section "Conguration de l'envoi d'emails" permet de dénir les caractéristiques du serveur SMTP utilisé :

```
Serveur et port SMTP
Utilisateur et mot de passe associé pour utiliser le serveur SMTP.
Type de sécurité utilisé.
```
La section "Conguration des intervenants" permet de dénir :

```
L'expéditeur du message, c'est-à-dire l'adresse email utilisée comme expéditeur.
Les destinataires par défaut du message envoyé par la messagerie. Il sut d'indiquer les adresses email
des destinataires.
```
Utilisation d'un programme tiers

L'onglet "Programme tiers" permet de paramétrer l'envoi de rapport d'erreurs par un programme spécique.
Pour utiliser ce mode de message d'alerte, indiquez le chemin de l'exécutable voulu. Cet exécutable doit être
accessible depuis le poste d'installation du contre-robot.

Dans ce mode d'envoi, le rapport d'erreur est un chier XML. Le chemin du rapport d'erreur sera passé en
ligne de commande au programme tiers et devra être traité par ce programme.

Le format du chier XML est le suivant :

<Test>
<NumeroTest>%1</NumeroTest>
<NomTest>%2</NomTest>
<CategorieTest>%3</CategorieTest>
<PrioriteTest>%4</PrioriteTest>
<SyntaxeTest>
%5
</SyntaxeTest>
<SolutionTest>
%6
</SolutionTest>
<DateErreur>%7</DateErreur>
<HeureErreur>%8</HeureErreur>
<MessageErreurPersonnel>
%9


</MessageErreurPersonnel>
<MessageErreur>
%10
</MessageErreur>
</Test>
<Test>
...
</Test>

Dans ce code :

```
%1 = Numéro identiant le test
%2 = Nom du test
%3 = Nom de la catégorie du test
%4 = Priorité du test
%5 = Syntaxe du test (paramètres associées)
%6 = Solution proposée pour le test
%7 = Date de l'erreur
%8 = Heure de l'erreur
%9 = Message d'erreur renseigné dans la che du test
%10 = Message d'erreur renvoyé par le robot
```
Paramétrage du rapport

L'onglet "Paramétrage du rapport" permet de paramétrer le sujet du message envoyé (par email ou par
WDBal).

La section "Objet de l'email envoyé" permet de construire le titre du message. Des macros permettent
d'obtenir des informations spéciques (nom du contre-robot, ...).


### WINDEV WEBDEV

Présentation

Le moniteur du robot de surveillance permet de créer les diérents contrôles à eectuer par le robot de
surveillance.

Comment le faire?

Les catégories permettent de regrouper les contrôles par thèmes. Chaque contrôle est associé à une
catégorie.

Par défaut, si un contre-robot a été installé, une catégorie "Contre-robot" est créée. Cette catégorie contient
un test de surveillance du contre-robot.

Créer une catégorie

Pour créer une catégorie :

1. Dans le menu, dans le groupe "Catégories et contrôles", cliquez sur "Ajouter" et sélectionnez l'option
    "Ajouter une catégorie" (ou utilisez l'option "Créer une catégorie" du menu contextuel de la table des
    contrôles).
2. Dans la fenêtre qui s'ache, indiquez le nom de la catégorie.
3. Validez. La nouvelle catégorie apparaît dans le moniteur.

Créer un contrôle

Pour créer un contrôle :

```
WINDEV Mobile Autres
```
## Robot de surveillance : Créer un

## contrôle


1. Dans le menu, dans le groupe "Catégories et contrôles", cliquez sur "Ajouter" et sélectionnez l'option
    "Ajouter un contrôle" (ou utilisez l'option "Créer un contrôle" du menu contextuel de la table des
    contrôles).
2. La fenêtre de conguration du contrôle s'ache.
3. Indiquez :
    le nom du contrôle.
    la catégorie du contrôle.
    le type de contrôle à eectuer.
    Si le contrôle dépend ou non d'un autre contrôle.
    Remarque : Si le contrôle dépend d'un autre contrôle, il sera exécuté uniquement si le contrôle dont il
    dépend s'est exécuté sans erreur.
4. Indiquez les paramètres généraux du contrôle.


5. Indiquez les paramètres spéciques du contrôle. Ces paramètres dépendent du type de contrôle
    sélectionné.
       Connectivité machine (ping).
       Connectivité FTP.
       Connectivité HTTP.
       Connectivité Serveur HFSQL Client/Serveur.
       Connectivité bases tierces (par ODBC).
       Connectivité NNTP.
       Activité d'une application WINDEV.
       Envoi d'un email.
       Log d'un site WEBDEV.
       SNMP.
       Espace disque (par SNMP).
       WLangage (code).
       Serveur WEBDEV.
       Connectivité SMTP.
       Etat d'un cluster.
       Activité d'un serveur de Télémétrie.
       Sonde température.
       Sonde température (par chier).
       Etat SMART d'un disque.
       Validité d'un certicat SSL.
6. A tout moment, le bouton "Tester" permet d'exécuter le test en cours d'édition. Le test est exécuté depuis
    le moniteur.
7. Validez. Le test apparaît dans le moniteur du robot de surveillance.


### WINDEV WEBDEV

Présentation

Le moniteur du robot de surveillance permet d'avoir à tout moment accès aux diérents contrôles lancés par
le robot de surveillance.

Il permet de :

```
Créer, modier ou supprimer un contrôle.
Dupliquer un contrôle.
Créer un modèle de contrôle.
Rechercher un contrôle.
Congurer :
le moniteur
le robot
le contre-robot
Acher l'historique.
Acher les statistiques.
Exporter ou importer des contrôles.
Gérer les utilisateurs.
```
Dupliquer un contrôle

Pour dupliquer un contrôle existant :

1. Sélectionnez le contrôle à dupliquer dans le moniteur.
2. Dans le menu du moniteur, dans le groupe "Catégories et contrôles", cliquez sur "Dupliquer".
3. Validez la duplication. Un nouveau test est créé reprenant toutes les caractéristiques du test dupliqué.
4. La fenêtre de description du contrôle apparaît.
5. Modiez les éléments voulus (notamment le nom du contrôle) et validez.

```
WINDEV Mobile Autres
```
## Manipuler les contrôles


Remarque : Lors de la validation, il est possible de saisir les raisons de la modication du contrôle. Ces
informations sont conservées dans l'historique de modication.

Rechercher un contrôle

Pour rechercher un contrôle :

1. Dans le menu du moniteur, cliquez sur "Rechercher".
2. Indiquez les critères de recherche. Ces critères peuvent porter sur le nom, la catégorie, le type ou le sujet
    du contrôle.
3. Validez. Les contrôles correspondant à la recherche sont automatiquement achés avec une loupe en
    début de ligne.

Exécuter un contrôle

Pour exécuter un contrôle :

1. Sélectionnez le contrôle voulu dans le moniteur.
2. Achez le menu contextuel du contrôle (clic droit) et sélectionnez "Tester le contrôle".
3. Indiquez si vous désirez que le résultat du test soit sauvegardé dans l'historique.
4. Le contrôle est exécuté et le moniteur ache les diérentes étapes de l'exécution.
5. Fermez la fenêtre d'exécution du contrôle.

Acher l'historique

Pour eectuer une recherche dans l'historique :

1. Dans le menu du moniteur, dans le groupe "Paramétrage", cliquez sur "Historique".
2. Saisissez les critères de recherche :
    Période de recherche.
    Type d'historique :
       l'historique des erreurs concerne les contrôles en erreur.
       l'historique des modications concerne les modications eectuées sur les contrôles.
    Contrôles concernés.
3. Cliquez sur le bouton "Rechercher" pour lancer la recherche. La liste des historiques correspondants est
    achée. Pour chaque historique, le détail est aché.


### WINDEV WEBDEV

Présentation

Pour simplier la création des contrôles, il est possible de créer et d'utiliser des modèles de contrôles. Ces
modèles permettent de dénir les options de planication des contrôles.

Ainsi, lors de la création d'un contrôle, au lieu de dénir à chaque fois les options de planication du contrôle,
il sut de sélectionner le modèle de contrôle correspondant.

Gestion des modèles de contrôle

Pour gérer les modèles de contrôle, dans le menu de RobotMonitor, dans le groupe "Catégories et contrôles",
cliquez sur "Modèle de contrôle".

La fenêtre de gestion des contrôles est la suivante :

```
WINDEV Mobile Autres
```
## Modèle de contrôle


Cette fenêtre permet de :

```
Créer un nouveau modèle,
Modier un modèle.
Voir les tests (contrôles) associés à un modèle.
Supprimer un modèle.
```
Créer un modèle

Pour créer un nouveau modèle :

1. Cliquez sur le bouton "Ajouter un nouveau modèle. Les champs de la fenêtre se vident.


2. Indiquez les diérentes caractéristiques du modèle :
    Nom du modèle : Ce nom sera utilisé dans la description du contrôle pour sélectionner les options de
    planications voulues.
    Délai entre deux contrôles : Temps entre deux exécutions du contrôle. Par exemple, si le délai est de 2
    heures, le contrôle sera lancé toutes les 2 heures.
    Nombre de tentatives : Nombre de fois où le contrôle est relancé avant d'être considéré en erreur.
    Attente entre deux tentatives : Les tests sont lancés par période de 2 minutes. Le temps entre deux
    tentatives ne doit pas dépasser 2 minutes (120 secondes).
    Tranches horaires d'exécution : Période de temps pendant laquelle le contrôle doit être eectué. Pour
    eectuer le contrôle sur toute la journée, le début doit être "00:00" et la n "23:59".
    Jours d'exécution : Jours de la semaine où le contrôle doit être eectué.
3. Cliquez sur le bouton "Valider". Le modèle de contrôle est automatiquement créé. Il est ajouté à la liste des
    modèles et peut être associé à un contrôle.

Modier un modèle

Pour modier un modèle :

1. Sélectionnez le modèle voulu dans la liste des modèles.
2. Modiez les caractéristiques voulues.
3. Cliquez sur le bouton "Valider". Le modèle de contrôle est automatiquement mis à jour. Si le modèle est
    associé à des contrôles, les contrôles sont également mis à jour.

Voir les contrôles associés à un modèle

Pour voir les contrôles associés à un modèle :

1. Sélectionnez le modèle voulu dans la liste des modèles.
2. Les caractéristiques du modèle sont achées dans la partie gauche de la fenêtre (zone "Paramètre du
    modèle").
3. Les contrôles associés au modèle sont achés dans la partie droite de la fenêtre (zone "Tests associés au
    modèle").

Supprimer un modèle

Pour supprimer un modèle :

1. Sélectionnez le modèle voulu dans la liste des modèles.
2. Cliquez sur le bouton.


Attention : Pour supprimer un modèle, ce modèle ne doit plus être associé à un contrôle.

Remarque : Le bouton "Supprimer les modèles sans contrôles" permet de supprimer tous les modèles qui ne
sont plus associés à un contrôle.


### WINDEV WEBDEV

Présentation

Lors de la création d'un contrôle ou de sa modication, il est nécessaire de dénir les paramètres généraux du
contrôle. Ces paramètres permettent de dénir :

```
les options d'activation du contrôle.
les options de planication du contrôle.
les options de traitement de l'erreur.
```
Options d'activation du contrôle

```
WINDEV Mobile Autres
```
## Robot de surveillance : Paramètres

## généraux des contrôles


Les options d'activation du contrôle permettent de savoir et de dénir :
si le contrôle est activé ou non,
à quelle date le contrôle doit être réactivé automatiquement.

Remarque : Le menu contextuel du contrôle permet de désactiver simplement un contrôle (option "Désactiver
le contrôle"). Cette option permet de désactiver le contrôle :

```
pendant 1 jour,
pendant 1 semaine,
pendant 1 mois,
pendant une durée personnalisée. Dans ce cas, une fenêtre permet de spécier la date de réactivation du
contrôle.
indéniment.
```
Modèle et options de planication

Les options de planication permettent de dénir quand le contrôle va être exécuté.

Ces options de planications sont dénies dans un modèle de contrôle. Les modèles de contrôle permettent
de créer rapidement plusieurs contrôles ayant les mêmes options de planication.

Options de traitement des erreurs

Les options de traitement des erreurs permettent de dénir :
Le contenu du message.
Les destinataires des rapports d'erreur.
Le programme à lancer en cas d'erreur.

Contenu du message

Les options de traitement des erreurs permettent de dénir :
le message personnalisé pouvant apparaître dans le rapport d'erreurs.
la solution conseillé pour solutionner le problème.
le destinataire des rapports d'erreur avec le niveau de gravité pour ce destinataire.

Exemple de message :

```
2 Alerte(s) Réseau | Priorité maximale : Normale
[----------------------------------------------------------------------]
Priorité : Normale
Catégorie : FTP
Contrôle : FTP Etats Et Requetes (xxxx) (n° 38)
```

```
Erreur :
Erreur lors de la connexion au serveur FTP
Echec de la connexion au serveur FTP "ftp.pcsoft.com" sur le port 21 avec le nom d'utilisateur.
La dernière réponse du serveur est :
Solution :
```
```
Détails interne :
```
- Syntaxe :
Adresse du serveur FTP : ftp.pcsoft.com
Port de connexion : 21
Connexion en mode passif : Vrai
Fichier à chercher : /wx11/latest/WD2025PACKER.exe
Nombre d'utilisateurs max pour check : 0
Télécharger le chier : Faux

Destinataires des rapports d'erreur

Pour chaque contrôle (test), il est possible de dénir les destinataires des rapports d'erreur, avec le niveau de
gravité de l'erreur pour ce destinataire. Ainsi un contrôle en erreur peut être important pour une personne et
mineur pour une autre.
Ces destinataires peuvent correspondre à :
un utilisateur.
un groupe de destinataires. Dans ce cas, tous les utilisateurs du groupe recevront le rapport d'erreur.

Pour ajouter un destinataire pour un contrôle :

1. Appuyez sur "+".
2. Dans la fenêtre qui s'ache, sélectionnez le groupe ou l'utilisateur et validez.
3. L'utilisateur ou le groupe sélectionné apparaît dans la liste des destinataires. Par défaut, la gravité de
    l'utilisateur est "Erreur".
4. Modiez si nécessaire le niveau de gravité de l'utilisateur. Les niveaux de gravité sont :
    Débogage,
    Information,
    Notication,
    Avertissement,
    Erreur,
    Erreur critique.

Rappel :

```
Les caractéristiques des utilisateurs sont dénies dans la fenêtre de gestion des utilisateurs (pour plus de
détails, consultez Conguration des utilisateurs).
```

```
Les groupes et la liste des utilisateurs associés sont dénis dans la fenêtre de gestion des groupes (pour
plus de détails, consultez Conguration des groupes d'utilisateurs).
```
Programme à lancer en cas d'erreur

Pour chaque test, il est possible d'indiquer un programme spécique à lancer en cas d'erreur. Ce programme
doit être accessible depuis le poste d'installation du robot. Il est possible d'indiquer une ligne de commande.


```
WINDEV WEBDEV WINDEV Mobile
```
Présentation

Le robot va vérier que la durée avant l'expiration est supérieure à la durée indiquée.

Le contrôle sera :

```
réussi si la durée avant la date d'expiration est supérieure à la durée spéciée.
en échec dans la cas contraire.
```
Paramètres spéciques au contrôle du certicat SSL

Informations sur le serveur possédant le certicat

Pour tester la validité du certicat SSL, il est nécessaire d'indiquer :
l'adresse du serveur.
le port de connexion.
la durée avant le déclenchement de l'alerte (en nombre de jours). Cette durée sera comparée au nombre
de jours restant avant l'expiration du certicat.

```
Autres
```
## Validité d'un certicat SSL


### WINDEV WEBDEV

Présentation

Le robot de surveillance propose de tester l'activité d'une application WINDEV.

Dans ce cas, le robot va contrôler l'activité de l'application en lisant la date et l'heure présentes dans un chier
.INI. Ce chier INI est un chier d'activité, rempli périodiquement par l'application WINDEV testée. L'activité
peut également être lue dans la base de données du robot (par exemple pour tester l'activité du robot ou d'un
contre-robot).

Le contrôle sera :

```
réussi si la date et l'heure lues ne dépassent pas le délai d'alerte.
en échec dans le cas contraire.
```
Remarque : Le chier à contrôler peut être un chier présent sur un serveur FTP.

Paramètres spéciques au contrôle d'activité d'une application

Informations sur l'application

Ces paramètres concernent l'application WINDEV à tester. Il est nécessaire d'indiquer :
le nom du poste où l'application est installée (poste accessible par le robot).
le nom de l'application WINDEV.
le délai d'inactivité avant alerte. Ce délai correspond au délai maximum autorisé entre la date et l'heure
indiquées dans le chier INI et la date et l'heure du test.

Informations sur l'activité

Trois possibilités pour tester l'activité de l'application :
Fichier INI en réseau : Ces paramètres concernent le chier INI permettant de tester l'activité de
l'application. Dans ce cas, il est nécessaire d'indiquer :
le nom du répertoire où le chier INI est installé (poste accessible par le robot).
le nom du chier INI.
la section à lire dans le chier INI.
le nom du mot-clé contenant la date et l'heure au format AAAAMMJJHHmmSS.

```
WINDEV Mobile Autres
```
## Contrôle : Activité d'une application


```
Fichier INI par FTP : Le chier INI de l'application peut être accessible sur un serveur FTP. Dans ce cas, il est
nécessaire de préciser les caractéristiques du serveur FTP à utiliser :
l'adresse du serveur FTP.
le numéro de port du serveur et le mode de connexion (passif ou non).
l'utilisateur et le mot de passe associé.
Base de données du robot : Ces paramètres peuvent également être enregistrées dans la base de données
du robot, dans le chier de données "ApplicationActivity". Dans ce cas, il est nécessaire de spécier
l'identiant de l'application.
```
Informations sur le relancement de l'application

Ces informations permettent de tenter de relancer l'application WINDEV. Si l'option "Relancement activé" est
cochée, il est possible de spécier :
le nombre de relances maximum.
le nom de l'utilisateur et son mot de passe. L'application sera relancée avec ces informations.
le chemin de l'application et la ligne de commande si nécessaire.


### WINDEV WEBDEV

Présentation

Le robot de surveillance va tenter de se connecter à une base de données tierce (MySQL, SQL Server, ...) par
ODBC.

Le contrôle sera :

```
réussi si la connexion est eective.
en échec dans le cas contraire.
```
Paramètres spéciques au contrôle de la connectivité des bases tierces

Il est nécessaire d'indiquer le nom de la source ODBC à tester. Cette source ODBC doit être dénie sur le poste
d'installation du robot de surveillance.

Remarque : Pour eectuer un test en local, depuis le moniteur, il est nécessaire de dénir la même source
ODBC sur ce poste.

```
WINDEV Mobile Autres
```
## Contrôle : Connectivité bases tierces

## (par ODBC)


### WINDEV WEBDEV

Présentation

Le robot de surveillance va tenter de se connecter à un serveur HFSQL Client/Serveur. Il est également
possible de tester l'ajout d'un enregistrement sur le serveur.

Le contrôle sera :

```
réussi si la connexion a pu être eectué.
en échec dans le cas contraire.
```
Paramètres spéciques au contrôle de la connectivité au serveur HFSQL

Informations sur le serveur HFSQL

Pour tester un serveur HFSQL, il est nécessaire d'indiquer :
l'adresse du serveur,
le port de connexion,
le login utilisé et le mot de passe associé.

Tester l'ajout d'enregistrements

Pour tester l'ajout d'un enregistrement sur un serveur HFSQL, il est nécessaire d'indiquer :
la base de données manipulée,
le chier de données où l'ajout doit être eectué,
le mot de passe du chier de données si nécessaire,
la liste des valeurs pour chaque rubrique à ajouter dans le chier de données.

Attention :

```
L'enregistrement ajouté lors de ce test ne sera pas supprimé.
L'enregistrement sera ajouté avec les droits associés à l'utilisateur précisé dans les informations de
connexion (login et mot de passe associé).
```
```
WINDEV Mobile Autres
```
## Contrôle : Connectivité Serveur

## HFSQL Client/Serveur


### WINDEV WEBDEV

Présentation

Le robot de surveillance va eectuer un ping sur l'adresse IP spéciée.

Le contrôle sera :

```
réussi si l'adresse répond au ping,
en échec dans le cas contraire.
```
Paramètres spéciques au contrôle de la connectivité machine

Informations sur la machine

Il sut de préciser le nom ou l'adresse IP de la machine à tester.

```
WINDEV Mobile Autres
```
## Contrôle : Connectivité machine

## (requête PING)


### WINDEV WEBDEV

Présentation

Le robot de surveillance va tenter de se connecter au serveur FTP avec les paramètres du serveur indiqués. Il
est possible de tester l'existence d'un chier sur le serveur FTP, ainsi que le nombre d'utilisateurs connectés.

Le contrôle sera :

```
réussi si la connexion est eective (et si le chier indiqué existe).
en échec dans le cas contraire.
```
Paramètres spéciques au contrôle de la connectivité FTP

Informations de connexion au serveur FTP

Il est nécessaire de préciser les caractéristiques de connexion au serveur FTP :
l'adresse du serveur FTP.
le numéro de port du serveur et le mode de connexion (passif ou non).
l'utilisateur et le mot de passe associé.

Informations sur le chier à contrôler

Il est possible de tester la présence d'un chier sur le serveur ainsi que son téléchargement. Les informations
à donner sont :
le nom complet du chier sur le serveur FTP.
si le chier doit être téléchargé ou non.

Contrôle du nombre d'utilisateurs connectés

Il est possible de tester le nombre d'utilisateurs connectés. Les informations à donner sont :
l'adresse de la page retournant la liste des utilisateurs.
le nombre d'utilisateurs maximum.

```
WINDEV Mobile Autres
```
## Contrôle : Connectivité FTP


### WINDEV WEBDEV

Présentation

Le robot de surveillance va lire l'entête et le contenu d'une page Web.

Le contrôle sera :

```
réussi si la page existe et si son entête ne contient aucune erreur.
en échec dans le cas contraire.
```
Paramètres spéciques au contrôle de la connectivité HTTP

Informations sur la page Web

Indiquez :
l'adresse de la page Web à tester.
le port de connexion utilisé.
la méthode HTTP à utiliser pour vérier que le serveur répond : GET, POST, PUT, DELETE, HEAD ou PATCH.
Ce paramètre permet notamment de tester certains Webservices.

Informations sur le contrôle à eectuer

Il est possible de contrôler la validité du contenu de la page. Dans ce cas, il est également possible de vérier
que le contenu est identique d'un contrôle à l'autre.

Gestion des cas d'erreurs personnalisés

Il est possible de dénir des cas d'erreurs spéciques en ajoutant des conditions sur l'en-tête et/ou sur le
contenu de la page. Le bouton "+" permet d'ajouter des conditions. Ces conditions permettent de dénir :
la condition d'erreur.
le contenu du message d'alerte si la condition est vériée.

Entêtes supplémentaires

Il est possible d'ajouter des entêtes supplémentaires qui seront passés à la requête. Exemple :
Authorization:WSSE prole="UsernameToken"

```
WINDEV Mobile Autres
```
## Contrôle : Connectivité HTTP


### WINDEV WEBDEV

Présentation

Le robot de surveillance va tenter de se connecter au serveur NNTP précisé (serveur de news).

Le contrôle sera :

```
réussi si la connexion est eective.
en échec dans le cas contraire.
```
Paramètres spéciques au contrôle de la connectivité NNTP

Informations sur le serveur NNTP

Pour tester un serveur NNTP, il est nécessaire d'indiquer :
l'adresse du serveur NNTP.
le port de connexion.

```
WINDEV Mobile Autres
```
## Contrôle : Connectivité NNTP


### WINDEV WEBDEV

Présentation

Le robot de surveillance va tenter d'eectuer une connexion à un serveur SMTP avec l'utilisateur indiqué.

Le contrôle sera :

```
réussi si la connexion est eective.
en échec dans le cas contraire.
```
Paramètres spéciques au contrôle de la connectivité SMTP

Informations de connexion au serveur SMTP

Il est nécessaire de préciser les caractéristiques de connexion au serveur SMTP :
l'adresse du serveur SMTP.
le numéro de port de connexion.
l'utilisateur et le mot de passe associé.

```
WINDEV Mobile Autres
```
## Contrôle : Connectivité SMTP


### WINDEV WEBDEV

Présentation

Le robot de surveillance va :
envoyer un email à une adresse email.
lire la boîte de réception de l'adresse email pour vérier que l'email a été reçu.

Le contrôle sera :

```
réussi si l'email a été envoyé et s'il est présent dans la boîte de réception.
en échec dans le cas contraire.
```
Paramètres spéciques au contrôle d'envoi d'email

Paramètres SMTP (pour l'envoi du message)

Les paramètres SMTP sont ceux du serveur utilisé pour l'envoi d'emails :
l'adresse email à laquelle le message de test doit être envoyé.
le serveur SMTP à utiliser et le port associé.
l'utilisateur et mot de passe associé.

Paramètres POP3 (pour la lecture du message reçu)

Les paramètres SMTP sont ceux du serveur utilisé pour l'envoi d'emails :
l'adresse email à laquelle le message de test doit être relu.
le serveur POP3 à utiliser et le port associé. La connexion peut être une connexion SSL.
l'utilisateur et mot de passe associé.

```
WINDEV Mobile Autres
```
## Contrôle : Envoi d'un email


### WINDEV WEBDEV

Présentation

Le robot de surveillance récupère l'espace disque disponible via un agent SNMP.

Le contrôle sera :

```
réussi si l'espace disponible est supérieur au seuil d'alerte.
en échec dans le cas contraire.
```
Paramètres spéciques au contrôle d'espace disque

Informations sur l'agent SNMP

Pour vérier l'espace disque, indiquez :
l'adresse de l'agent SNMP à utiliser,
la communauté de l'agent.

Informations sur le disque à contrôler

Lorsque l'adresse de l'agent SNMP est indiquée, il est possible de lister les disques accessibles par cet agent
(bouton "Lister les disques").

Sélectionnez ensuite le ou les disques à contrôler et indiquez le seuil d'alerte.

```
WINDEV Mobile Autres
```
## Contrôle : Espace disque par SNMP


```
WINDEV WEBDEV WINDEV Mobile
```
Présentation

Le robot de surveillance va interroger les attributs SMART des disques durs d'un serveur.

Le contrôle sera :

```
réussi si aucun problème n'est détecté.
en échec dans le cas contraire.
```
Présentation de SMART

SMART est l'acronyme de "Self-Monitoring Analysis and Reporting Technology", en français : Technologie
d'auto-surveillance, d'analyse et de rapport.

SMART est une technologie proposée par les fabricants de disques durs. Cette technologie permet de suivre
l'état d'usure d'un disque dur et ainsi d'anticiper une probable défaillance imminente.
Les disques durs compatibles avec cette technologie exposent un certain nombre de compteurs. Le nombre et
la nature de ces compteurs peuvent varier selon les fabricants.

Ces compteurs peuvent être lus par programmation. Il devient ainsi possible de détecter une usure
prématurée des disques durs et même d'être prévenu avant qu'un disque ne tombe en panne.

Attention : la technologie SMART ne détecte pas tous les cas possibles de défaillance d'un disque dur. Elle ne
se substitue jamais à un système de sauvegarde.

Les attributs SMART

La technologie SMART dénit un certain nombre de compteurs appelés attributs. Chacun de ces attributs
permet de mesurer un paramètre du disque dur :
la température interne,
le nombre de tentatives pour la lecture d'une donnée,
le taux d'erreur,
le temps de fonctionnement, ...

L'évolution de ces attributs permet de prédire une défaillance. Par exemple, une augmentation rapide et
importante de la température est généralement un signe fort d'une défaillance proche.

Pour faciliter l'interprétation de ces attributs, les systèmes d'exploitation proposent généralement des outils
ou des API qui permettent d'obtenir une synthèse de l'état d'un disque. Il est ainsi possible de savoir si le
disque dur est dans un état correct ou s'il montre des signes de faiblesse.

```
Autres
```
## Contrôle : Etat SMART des disques


Paramètres spéciques au contrôle des attributs SMART

Le contrôle de l'état SMART d'un disque dur s'eectuant à distance, il est nécessaire de :
spécier la manière dont le robot de surveillance accède au serveur. Deux protocoles sont proposés :
SNMP et SSH. Selon le protocole spécié, les options demandées varient.
demander au robot de surveillance :
soit de vérier tous les disques,
soit de vérier uniquement une liste de disques donnée.

Contrôle via le protocole SNMP

Dans le cas de l'utilisation du protocole SNMP, les informations suivantes doivent être fournies dans le
paramétrage du contrôle :

```
l'adresse du serveur (nom ou adresse IP),
le port du service SNMP (par défaut, il s'agit du port 161),
le nom de la communauté SNMP à interroger,
la liste des OID correspondant aux états SMART à vérier. La conguration des OID à interroger est
détaillée plus loin.
```
Attention : le protocole SNMP n'est pas sécurisé. Il n'est pas recommandé de l'utiliser pour des serveurs
exposés sur un réseau public ou sur Internet. Il est préférable de réserver l'utilisation du protocole SNMP à
des serveurs internes ou accessibles à travers un réseau privé (VPN par exemple).

Contrôle via le protocole SSH

Dans le cas de l'utilisation du protocole SSH, les informations suivantes sont nécessaires :


```
l'adresse du serveur (nom ou adresse IP),
le port du service SSH (par défaut, il s'agit du port 22),
le nom d'utilisateur,
le mot de passe de l'utilisateur ou une clé privée (et son mot de passe) permettant de se connecter avec ce
nom d'utilisateur.
```
Selon le système utilisé par le serveur (Windows ou Linux), plusieurs options sont proposées :
Les serveurs Linux doivent être interrogés en utilisant l'outil "Smartmontools".
Dans ce cas, l'option "Utiliser 'sudo'" permet d'indiquer si les commandes envoyées doivent être préxées
de la commande "sudo". La commande "sudo" permet à des utilisateurs non privilégiés d'exécuter des
commandes réservées au root.
Les serveurs Windows peuvent être interrogés soit en utilisant l'outil WMI, soit en utilisant Powershell. Les
deux options sont équivalentes en termes de fonctionnalités.

Conguration des serveurs pour remonter les informations SMART

Conguration d'un serveur Windows pour remonter les informations SMART par SSH

Le serveur Windows doit proposer (au choix) l'utilitaire WMI ou l'utilitaire Powershell.
Pour vérier que WMI est correctement installé sur le serveur, il sut d'ouvrir une ligne de commande et
de taper :
wmic diskdrive get PNPDeviceID,Status
Pour vérier que Powershell est correctement installé sur le serveur, il sut d'ouvrir une ligne de
commande en tant qu'administrateur et de saisir :
powershell -Command "& {Get-WmiObject -Namespace root/wmi -Class
MSStorageDriver_FailurePredictStatus Property PredictFailure,InstanceName}"

Conguration d'un serveur Linux pour remonter les informations SMART par SSH

Pour que les contrôles du robot fonctionnent correctement sur un serveur Linux, les commandes suivantes
doivent être disponibles : blkid et smartctl.


Sur un serveur de la famille Debian (Ubuntu,...), ces commandes s'installent avec la ligne de commande :
apt install util-linux smartmontools
De plus, si la connexion avec l'utilisateur root n'est pas possible (ou pas souhaitée), il sera nécessaire :

```
d'installer l'utilitaire sudo,
de le congurer pour autoriser l'utilisateur à lancer les commandes blkid et smartctl sans saisir son mot
de passe dans la console.
```
Conguration d'un serveur Linux pour remonter les informations SMART par SNMP

Il faut :
installer les mêmes paquets que pour le contrôle par SSH.
installer un serveur SNMP.

Sur une machine serveur de la famille Debian (Ubuntu, ...), le serveur SNMP s'installe avec la commande :
apt install snmpd

Ensuite, il est nécessaire de congurer le service SNMP. Cette page ne présente pas en détail la conguration
de SNMP, reportez-vous pour cela à la documentation du service SNMP.

Pour permettre de lire l'état SMART d'un disque par SNMP, il faut ajouter la directive suivante dans le chier
de conguration (généralement /etc/snmp/snmpd.conf) :
extend smart_test /bin/sh /etc/snmp/
smart_test.sh /dev/sda1
où :

```
smart_test est une chaîne arbitraire,
/etc/snmp/smart_test.sh est le chemin du script de lecture des informations (voir ci-dessous),
/dev/sda1 est le disque à analyser.
```
Cette directive doit être ajoutée pour chaque disque à analyser.

Chaque directive va créer un nouvel OID personnalisé qui sera lisible par le robot.

Astuce : Pour récupérer l'OID exact créé par la commande "extend", il sut de lancer la commande suivante
sur le serveur :
snmpwalk -c public -v 2c localhost
1.3.6.1.4.1.8072.1.3.2.4.1.2
Le script smart_test.sh contient la commande suivante :
sudo smartctl -H $1 | grep "SMART
overall-health self-assessment test result"
| cut -d : -f 2
Il est nécessaire de l'adapter selon le système (par exemple pour utiliser ou non la commande "sudo").


### WINDEV WEBDEV

Présentation

Le robot de surveillance va récupérer le log du jour d'une application WEBDEV sur le serveur FTP associé. Le
contenu du log est analysé pour trouver d'éventuelles erreurs.

Le contrôle sera :

```
réussi si le log est récupéré et ne comporte aucune erreur.
en échec dans le cas contraire.
```
Paramètres spéciques au contrôle du log d'un site WEBDEV

Informations sur le serveur WEBDEV

Les informations nécessaires pour vérier les logs d'un serveur WEBDEV sont les suivantes :
Adresse du serveur.
Port de connexion (avec si nécessaire une connexion en mode passif).
L'utilisateur et le mot de passe associé.
Le répertoire sur le serveur contenant les logs du site voulu.

```
WINDEV Mobile Autres
```
## Contrôle : Log d'un site WEBDEV


### WINDEV WEBDEV

Présentation

Le robot de surveillance va tester le fonctionnement du Serveur d'application WEBDEV.

Le contrôle sera :

```
réussi si le serveur d'application WEBDEV répond.
en échec dans le cas contraire.
```
Paramètres spéciques au contrôle d'un serveur d'application WEBDEV

Informations sur le serveur d'application WEBDEV

Les informations sur le serveur d'application WEBDEV à tester sont :
l'adresse du serveur d'application WEBDEV.
la version du serveur d'application WEBDEV (par exemple 30).
la plateforme (Windows ou Linux)

```
WINDEV Mobile Autres
```
## Contrôle : Serveur d'application

## WEBDEV


### WINDEV WEBDEV

Présentation

Le robot de surveillance va compiler et exécuter le code WLangage saisi.

Le contrôle sera :

```
réussi si le code WLangage a été compilé et s'il renvoie Vrai.
en échec dans le cas contraire.
```
Paramètres spéciques au test WLangage

Code WLangage

Saisissez le code WLangage permettant d'eectuer le test voulu. Ce code est automatiquement compilé et les
erreurs de compilation (si elles existent) sont achées dans la partie basse de l'écran.

Remarques

```
Le code WLangage saisi doit obligatoirement renvoyer Vrai en exécution pour être considéré comme
valide.
Il est possible d'indiquer un compte-rendu spécique grâce à la variable [[COMPTERENDU]]. Ce compte-
rendu sera intégré au compte-rendu d'erreur.
Le bouton "Tester" permet de tester directement le code WLangage. Si la variable [[COMPTERENDU]] a été
utilisée, son contenu est aché lors du test.
Le robot de surveillance gère des chaînes Unicode en exécution. Toutes les chaînes déclarées dans le code
WLangage sont donc des chaînes Unicode par défaut. Lorsqu'un contrôle doit échanger des données avec
un autre processus (via sockets, chiers d'échange, ...), il peut être nécessaire de déclarer les chaînes en
ANSI si l'autre processus est compilé pour gérer les chaînes en ANSI. Il est alors nécessaire de préciser que
la chaîne est une chaîne ANSI (déclaration du type : MaChaîne est une chaîne Ansi).
```
```
WINDEV Mobile Autres
```
## Contrôle : Test d'un code WLangage


### WINDEV WEBDEV

Présentation

Le robot de surveillance va lire la valeur de l'OID indiquée et comparer sa valeur avec la valeur de référence.

Le contrôle sera :

```
réussi si la valeur de l'OID a pu être lue et correspond à la valeur de référence.
en échec dans le cas contraire.
```
Paramètres spéciques au contrôle SNMP

Informations sur l'agent SNMP

Pour eectuer un test SNMP, indiquez :
l'adresse de l'agent SNMP à utiliser,
la communauté de l'agent.

Informations sur l'OID à contrôler

Pour eectuer un test SNMP, indiquez :
l'OID prédéni s'il existe,
les conditions de test de la valeur.

Remarque : Pour ajouter un OID prédéni :

1. Saisissez son nom (champ "OID prédénis").
2. Saisissez sa valeur (champ "OID à lire").
3. Cliquez sur le bouton "+".

```
WINDEV Mobile Autres
```
## Contrôle : SNMP


