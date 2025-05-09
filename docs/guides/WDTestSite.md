### WEBDEV

## Présentation

L'utilitaire WDTestSite

WDTestSite est un utilitaire permettant de réaliser diérents tests sur un site WEBDEV.

Les diérents tests possibles sont les suivants :

```
Test de montée en charge :
Le test de montée en charge consiste à simuler la connexion de plusieurs internautes à un site WEBDEV.
Chacun internaute exécute une suite d'opérations (scénario) simultanément.
Test de non-régression :
Le test de non-régression consiste à vérier le fonctionnement d'un site WEBDEV entre deux mises à jour.
Le test de non-régression consiste à vérier qu'un scénario réalisé avec une précédente version du site
fonctionne correctement avec la mise à jour du site.
Test d'un site en mode multi-utilisateurs :
Le test d'un site en mode multi-utilisateurs permet de vérier que les accès concurrentiels aux chiers de
données sont correctement gérés. Ce test consiste à simuler la connexion simultanée de plusieurs
internautes à un site WEBDEV. Chacun internaute exécute une suite d'opérations (scénario)
simultanément.
Comparaison de diérents serveurs :
WDTestSite permet de comparer la vitesse de diérents serveur. Il sut de lancer un scénario sur
diérents serveurs et de comparer le temps d'exécution de ce scénario.
Optimisation de traitements réalisés en WLangage :
WDTestSite permet de comparer le temps d'exécution d'un scénario avant et après une optimisation du
code WLangage.
```
## Lancement de WDTestSite

WDTestSite peut être lancé :
sous le volet "Outils", dans le groupe "Utilitaires", en cliquant sur "WDTestSite" (depuis WEBDEV version
Développement).
directement en double-cliquant sur le programme "WDTestSite.EXE".

## Conditions d'utilisation

```
WINDEV WINDEV Mobile Autres
```
# WDTestSite : Présentation


WDTestSite est un outil non redistribuable.

Cependant, pour réaliser les tests en mode multi-utilisateurs, WDTestSite peut être installé sur plusieurs
postes.

## Utilisation de WDTestSite

Principe d'utilisation

WDTestSite permet de :
créer un scénario. Ce scénario contient une suite d'actions à eectuer sur un site WEBDEV.
tester directement un scénario.
lancer consécutivement plusieurs exécutions du même scénario à partir d'un même poste ou de postes
diérents
.
Le scénario est exécuté sur le poste serveur.
tester le lancement d'un même scénario par plusieurs utilisateurs simultanés à partir d'un même poste
ou de postes diérents
.
Le scénario est exécuté sur le poste serveur.

## Installation de WDTestSite sur diérents postes

Pour réaliser des tests de montée en charge sur un serveur, ou encore des tests de rapidité de traitement du
serveur, il est conseillé d'utiliser diérents postes pour lancer l'exécution d'un scénario. Le scénario est
toujours exécuté sur le même serveur Web.

Les chiers à copier sur chaque poste de test sont :

```
l'exécutable : WDTestSite.exe
les diérentes librairies : httputil.dll, wd300hf.dll, wd300mat.dll, wd300obj.dll, wd300pnt.dll, wd300std.dll,
wd300vm.dll.
le chier d'aide de WDTestSite : WDTestSite.pdf
le scénario (chier ".WCN") : ce chier doit être copié dans un sous-répertoire "Scenario" du répertoire
d'installation de WDTestSite.exe.
```
Lorsque ces chiers sont copiés sur les postes de test, il sut de lancer le scénario ou de lancer le test de
montée en charge sur chacun des postes de test.


### WEBDEV

## Présentation

Le scénario est un chier texte (extension ".WCN") contenant toutes les manipulations eectuées pendant
l'enregistrement du scénario.

## Création d'un scénario

Pour créer un scénario, les éléments suivants doivent être installés sur le poste en cours :
WEBDEV version Développement ou Serveur d'application WEBDEV.
le site WEBDEV utilisé pour créer le scénario.

Il est conseillé de créer le scénario directement sur le serveur Web où le site WEBDEV est installé (poste de
déploiement).

Créer un scénario sur le poste de déploiement

Pour créer un scénario sur le poste de déploiement :

1. Lancez WDTestSite (double-clic sur WDTestSite.EXE par exemple).
2. Vériez que le serveur WEBDEV utilisé correspond à l'option "Machine locale".
3. Vériez que l'administrateur WEBDEV est lancé (option "Programmes .. WEBDEV 2025 .. Administrateur
    WEBDEV" du menu "Démarrer").
4. Cliquez sur le bouton "Nouveau".
5. Indiquez le nom du scénario et sa description. La description peut par exemple correspondre à un
    résumé des fonctionnalités testées dans le scénario. Cette description vous permettra d'identier
    facilement le scénario et ses fonctionnalités.
    Attention :
       La description du scénario ne pourra pas être modiée par la suite.
       Si le nom du scénario correspond à un scénario existant sur ce poste, le scénario existant sera
       remplacé par le nouveau scénario.
6. Cliquez sur le bouton "Enregistrement" : la page de test de l'administrateur de WEBDEV s'ache.
7. Sélectionnez le site WEBDEV utilisé pour créer le scénario.

```
WINDEV WINDEV Mobile Autres
```
# WDTestSite : Création d'un scénario


8. Eectuez toutes les manipulations nécessaires dans le site WEBDEV.
    Remarques :
       Pour tester la capacité du serveur à supporter un nombre important de connexions simultanées, il est
       conseillé de laisser le site connecté après la dernière action : pendant l'enregistrement du scénario,
       n'utilisez pas de bouton ou de lien permettant de fermer le site.
       Pour tester la non-régression d'un site ou la gestion des accès concurrentiels, vous pouvez quitter le
       site (par un lien ou un bouton) lors de l'enregistrement du scénario.
9. Pour terminer l'enregistrement du scénario, cliquez sur le bouton "Terminer" de WDTestSite.
    Le scénario (chier d'extension ".WCN") est alors créé dans le sous-répertoire "Scénario" du répertoire
    contenant le programme "WDTestSite.EXE".


### WEBDEV

## Présentation

Le scénario est un chier texte (extension ".WCN") contenant toutes les manipulations eectuées pendant
l'enregistrement du scénario.

Ce scénario est exécuté directement avec WDTestSite.

## Exécution d'un scénario

Exécuter un scénario permet par exemple de vérier la non-régression d'un site WEBDEV. En eet, un
scénario eectué avec une version précédente du site doit fonctionner avec une mise à jour du site.

Exécuter un même scénario plusieurs fois consécutivement permet par exemple de tester les capacités du
serveur lors de connexions simultanées, ... Dans ce cas, il est conseillé d'utiliser un scénario ne fermant pas le
site.

Dans tous les cas, il est conseillé d'exécuter le scénario :

```
depuis un poste quelconque (poste de développement par exemple).
sur le serveur Web de déploiement du site WEBDEV.
```
Exécuter un scénario

Pour exécuter un scénario :

1. Paramétrez l'administrateur WEBDEV du poste sur lequel le scénario va être exécuté (serveur Web).
    Vériez les paramètres du site correspondant au scénario :
       le nombre maximum de connexions au site :
       Ce nombre doit correspondre au nombre maximum de connexions simultanées voulues (ou
       successives si les sites ne se terminent pas).
       le nombre maximum de re-connexions d'un utilisateur au site :
       Dans le cas d'un scénario exécuté depuis un poste plusieurs fois, ce chire doit correspondre au
       nombre d'exécutions du scénario.
       le temps de déconnexion des utilisateurs inactifs :
       Dans le cas d'un test des capacités du serveur, le temps de déconnexion des utilisateurs inactifs doit
       être élevé (plus de 30 minutes par exemple).
2. Lancez WDTestSite sur le poste de test (poste de développement par exemple).

```
WINDEV WINDEV Mobile Autres
```
# WDTestSite : Exécution d'un

# scénario


3. Sélectionnez le serveur Web sur lequel le scénario doit être exécuté. Ce serveur doit être accessible
    depuis le poste de test. L'administrateur WEBDEV (version Développement ou version Déploiement) doit
    être lancé sur le serveur.
    Vous pouvez saisir dans la liste "Machine Cible" :
       un nom de machine accessible par le réseau. Exemple : "Serveur Test"
       une adresse IP. Exemple : 123.3.456.
       une adresse internet. Exemple : [http://www.op.fr](http://www.op.fr)
       Le bouton "Voisinage" permet de lister les postes directement accessibles par le réseau (non
       disponible sous Windows 98 ou Me).
4. Sélectionnez votre scénario dans la liste des scénarios disponibles.
5. Cliquez sur le bouton "Exécuter". La fenêtre d'exécution apparaît et le test s'exécute automatiquement.
6. Pour exécuter plusieurs fois le scénario consécutivement, indiquez un nombre de tours supérieur à 1 et
    cliquez sur le bouton "Ré-exécuter".

Remarques

```
Lors de l'exécution du scénario, toutes les actions réalisées dans le site sont achées. En cas de problème
(erreur, ...), le scénario s'arrête et la dernière ligne ache l'erreur rencontrée.
En cas d'erreur, un chier HTML contenant l'erreur est enregistré dans le répertoire "C:\TEMP" du poste
en cours. Attention : l'utilisateur Internet doit avoir les droits d'écriture sur le répertoire "C:\Temp".
Pour tester les capacités du serveur lors de connexions simultanées, il est conseillé d'exécuter un même
scénario depuis plusieurs postes. Pour plus de détails, consultez Installation de WDTestSite sur diérents
postes.
```
## Exécution d'un scénario en ligne de commande

Pour exécuter un scénario en ligne de commande :

1. Paramétrez l'administrateur WEBDEV du poste sur lequel le scénario va être exécuté (serveur Web).
    Vériez les paramètres du site correspondant au scénario :
       le nombre maximum de connexions au site :
       Ce nombre doit correspondre au nombre maximum de connexions simultanées voulues (ou
       successives si les sites ne se terminent pas).
       le nombre maximum de re-connexion d'un utilisateur au site :
       Dans le cas d'un scénario exécuté depuis un poste plusieurs fois, ce chire doit correspondre au
       nombre d'exécutions du scénario.
       le temps de déconnexion des utilisateurs inactifs :
       Dans le cas d'un test des capacités du serveur, le temps de déconnexion des utilisateurs inactifs doit
       être élevé (plus de 30 minutes par exemple).
2. Lancez WDTestSite sur le poste de test en utilisant la syntaxe suivante :


WDTestSite /AUTO = <Nom de scénario>

Par exemple : "WDTestSite /AUTO = MonScenario.wcn". Le scénario est automatiquement exécuté, et
WDTestSite se termine.

Le scénario doit être présent dans le répertoire des scénarios.
Rappel : Le scénario (chier d'extension ".WCN") est créé dans le sous-répertoire "Scénario" du répertoire
contenant le programme "WDTestSite.EXE".


### WEBDEV

## Présentation

Les tests de montée en charge permettent par exemple de vérier :
le nombre d'internautes pouvant être connectés simultanément à un site WEBDEV.
la gestion des accès concurrentiels à un site WEBDEV.

## Réalisation d'un test de montée en charge

Pour eectuer un test de montée en charge depuis un poste :

1. Paramétrez l'administrateur WEBDEV du poste sur lequel le scénario va être exécuté (serveur Web).
    Vériez les paramètres du site correspondant au scénario :
       le nombre maximum de connexions au site :
       ce nombre doit correspondre au nombre maximum de connexions simultanées voulues (ou
       successives sans terminer le site).
       le nombre maximum de re-connexions d'un utilisateur au site :
       Dans le cas d'un scénario exécuté depuis un poste plusieurs fois, ce chire doit correspondre au
       nombre d'exécutions du scénario.
       le temps de déconnexion des utilisateurs inactifs :
       Dans le cas d'un test des capacités du serveur, le temps de déconnexion des utilisateurs inactifs doit
       être élevé (plus de 30 minutes par exemple).
2. Lancez WDTestSite sur le poste de test (poste de développement par exemple).
3. Sélectionnez le serveur Web où le scénario doit être exécuté. Ce serveur doit être accessible depuis votre
    poste et l'administrateur WEBDEV (version développement ou version déploiement) doit être lancé sur ce
    poste.
    Vous pouvez saisir dans la liste "Machine Cible" :
       un nom de machine accessible par le réseau. Exemple : "Serveur Test"
       une adresse IP. Exemple : 123.3.456.
       une adresse internet. Exemple : [http://www.op.fr](http://www.op.fr)
       Le bouton "Voisinage" permet de lister les postes directement accessibles par le réseau (non
       disponible sous Windows 98 ou Me).
4. Sélectionnez votre scénario dans la liste des scénarios disponibles.
5. Cliquez sur le bouton "En charge".

```
WINDEV WINDEV Mobile Autres
```
# WDTestSite : Test de montée en

# charge


6. Indiquez le nombre d'utilisateurs (c'est-à-dire d'internautes) simulés à partir du poste.
    Pour chaque utilisateur, un "Robot" de test sera créé sur le poste en cours.
    Attention : le nombre d'utilisateurs simulé doit être choisi en fonction des ressources du poste
    permettant de lancer le test. Chaque robot consomme des ressources mémoire du poste (RAM).
7. Indiquez la temporisation (en centièmes de seconde). Cette temporisation correspond au temps séparant
    chaque action du scénario.
8. Créez les diérents utilisateurs (bouton "Créer les robots").
9. Lancez le test (bouton "Lancer les robots"). Les tests sélectionnés s'eectuent.
10. Pour terminer les tests ou pour relancer un nouveau test avec plus d'utilisateurs simulés, cliquez sur le
bouton "Tuer les robots".

## Notes

```
Lors de l'exécution du scénario, toutes les actions réalisées dans le site sont achées. En cas de problème
(erreur, ...), le scénario s'arrête.
En cas d'erreur, le chier HTML contenant l'erreur est enregistré dans le répertoire "C:\TEMP" du poste.
Pour tester les capacités du serveur lors de connexions simultanées, il est conseillé d'eectuer le test de
montée en charge depuis plusieurs postes. Pour plus de détails, consultez
Installation de WDTestSite sur diérents postes.
```

