```
WINDEV WEBDEV WINDEV Mobile
```
Présentation

WDScript est un éditeur de scripts WLangage, livré avec WINDEV, WEBDEV et WINDEV Mobile. WDScript
permet :
d'écrire des scripts en WLangage.
d'exécuter des scripts WLangage existants.

Il est ainsi possible d'automatiser certaines tâches qui ne nécessitent pas d'interface et qui doivent être
lancées en mode "batch" (par exemple le traitement de journaux d'erreurs).

Utilisation

Lancement de WDScript

WDScript peut être lancé en mode interactif :
directement depuis WINDEV, WEBDEV ou WINDEV Mobile : sous le volet "Outils", dans le groupe
"Utilitaires", cliquez sur "WDScript".
en lançant directement les chiers suivants présents dans le sous-répertoire "Programs" du répertoire
d'installation de WINDEV, WEBDEV ou WINDEV Mobile :
WDScript.exe : Lance WDScript en version 32 bits.
WDScript64.exe : Lance WDScript en version 64 bits.

Pour plus de détails, consultez WDScript : utilisation en mode interactif.

WDScript peut être lancé en mode ligne de commande pour exécuter directement le script WLangage
spécié.

WDScript peut être lancé en mode "console" grâce aux exécutables suivants :

```
WDScriptConsole.exe : Lance WDScript en mode console en version 32 bits.
WDScriptConsole64.exe : Lance WDScript en mode console en version 64 bits.
```
Pour plus de détails, consultez WDScript : utilisation en ligne de commande et en mode console.

Conditions d'utilisation

WDScript est un outil redistribuable. WDScript peut être installé avec les applications développées avec
WINDEV, WEBDEV ou WINDEV Mobile. La licence d'utilisation de WINDEV s'applique intégralement.

Chaînes ANSI/Unicode

```
Autres
```
# Présentation WDScript


Attention : En mode interactif et en mode ligne de commande, le code exécuté par WDScript utilise les
chaînes congurées en Unicode. Il est donc nécessaire de :
utiliser la syntaxe Unicode des fonctions (si cette syntaxe est spécique).
déclarer explicitement les chaînes ANSI si elles doivent contenir des données non Unicode.

Installation de WDScript

```
Cas 1 : Installation avec vos applications WINDEV
```
Lors de la création de la procédure d'installation, WDScript peut être livré avec vos applications WINDEV.
Rappel : La procédure d'installation peut être créée :
soit à partir de l'assistant : sous le volet "Projet", dans le groupe "Génération", déroulez "Procédure
d'installation" et sélectionnez "Créer la procédure d'installation".
soit à partir de l'éditeur d'installation : sous le volet "Outils", dans le groupe "Utilitaires", cliquez sur
"WDInst".

Cas 2 : Installation indépendante
Les chiers nécessaires à l'installation de WDScript sont les suivants :

```
WDScript.exe (32 bits) ou WDScript64.exe (64 bits) : Ce module est présent dans le répertoire "\Programs\"
de WINDEV, WEBDEV ou WINDEV Mobile,
WDScriptConsole.exe (32 bits) ou WDScriptConsole64.exe (64 bits) : Ce module est présent dans le
répertoire "\Programs\" de WINDEV, WEBDEV ou WINDEV Mobile,
Le Framework correspondant : comme toutes les fonctions du WLangage peuvent être utilisées, il est
nécessaire d'installer le Framework complet. Il est disponible dans le répertoire :
"\Programs\Framework\Win32x86" pour WDScript.exe (32 bits),
"\Programs\Framework\Win64x86" pour WDScript.exe (64 bits).
Le composant WDOutil.wdk : il est également présent dans le répertoire "\Programs\" de WINDEV,
WEBDEV ou WINDEV Mobile.
Les chiers d'aide WDScript_FR.pdf et WDScript_EN.pdf. Ces chiers sont présents dans le répertoire
"\Help\" de WINDEV, WEBDEV ou WINDEV Mobile.
```

```
WINDEV WEBDEV WINDEV Mobile
```
Présentation

En mode interactif, l'éditeur WDScript se décompose en plusieurs zones :
Le ruban qui permet d'accéder aux options les plus courantes,
L'éditeur de code qui permet de saisir le script en WLangage.
La console de sortie qui permet notamment d'acher les diérents résultats ainsi que les erreurs
rencontrés en exécution.

Le ruban de WDScript

Le ruban de WDScript est composé de deux volets :
Le volet "Accueil" qui propose les diérentes options permettant de manipuler les scripts WLangage.
Le volet "Code" qui permet de manipuler le code WLangage.

Volet "Accueil"

Les options du volet "Accueil" sont regroupées par fonctionnalités.

```
Autres
```
# WDScript : utilisation en mode

# interactif


Les options du groupe "Général" permettent de créer et manipuler un chier script WLangage, grâce aux
options "Nouveau", "Ouvrir", "Enregistrer" et "Fermer".

L'option "Go" du groupe "Exécution" permet de lancer le script aché.

Dans le groupe "Options" :

```
L'option "Options" permet de :
Gérer l'association des chiers "wl" générés par WDScript à WDScript ou WDScriptConsole.
```
```
Si le chier wl est associé à WDScript, il sera automatiquement ouvert dans l'interface de WDScript
lors du double-clic sur son nom.
Si le chier wl est associé à WDScriptConsole, il sera automatiquement exécuté en mode console
lors du double-clic sur son nom.
Proposer l'option "Ouvrir dans WDScript" dans l'explorateur de chiers Windows. Cette option sera
proposée dans le menu contextuel du chier sous l'explorateur de chier Windows.
Activer la complétion. Dans ce cas, lors de la saisie du code sous WDScript, les diérentes fonctions
possibles seront proposées lors de la saisie.
L'option "Aide" permet de :
Acher l'aide en ligne de la fonction WLangage sélectionnée (via le site de documentation de PC SOFT).
Choisir la langue d'achage de WDScript.
```
Volet "Code"

Le volet "Code" permet de manipuler le code aché dans l'éditeur de code de WDScript.


Il est possible de :
Commenter / Décommenter une ou plusieurs lignes de code.
Annuler ou rétablir la dernière opération eectuée.
Aller à la ligne spéciée : il sut d'indiquer le numéro de ligne.
Faire une recherche d'un texte dans le script.

L'éditeur de code de WDScript

L'éditeur de code de WDScript est un éditeur de code simplié par rapport à l'éditeur de code de WINDEV,
WEBDEV ou WINDEV Mobile. Il est destiné à des scripts contenant un code plus court et plus simple que celui
saisi dans l'éditeur de code de WINDEV, WEBDEV ou WINDEV Mobile.


Caractéristiques de l'éditeur de code de WDScript :

```
Coloration du code.
Présence des raccourcis simples.
Complétion simple du code.
Les erreurs de compilation s'achent directement dans le code, sous forme de bulle.
```
Plusieurs contraintes existent :

```
Le script WLangage doit contenir un seul bloc de code.
Les procédures doivent être des procédures internes.
Les procédures internes doivent être déclarées avant leur exécution.
Pas de débogueur.
Pas d'utilisation de nom de champ, de page, de fenêtre ou d'état.
```

Console de sortie de WDScript

La console de sortie permet de :
Acher les résultats renvoyés par le script lors de l'exécution du script en mode interactif (utilisation de la
fonction Trace par exemple).

```
La valeur de retour du code exécuté est également achée.
Acher les erreurs d'exécution lors de l'exécution du script en mode interactif.
```
Ce volet est détachable et peut être réduit. Les erreurs sont achées en rouge. Le bouton

```
permet d'eacer le contenu de la
```
fenêtre de sortie.


```
WINDEV WEBDEV WINDEV Mobile
```
Présentation

Les scripts créés avec WDScript peuvent être exécutés :
en ligne de commande.
en mode console. En appelant le script depuis la console Windows, il est possible d'écrire dans la sortie
standard.

Comment le faire

Exécuter WDScript en mode ligne de commande

Pour exécuter WDScript en mode ligne de commande, saisissez la ligne de commande suivante :
<Chemin de WDScript> /SCRIPT=<Chemin du script>
où :
<Chemin de WDScript> correspond au chemin complet de l'exécutable de WDScript.exe (ou
WDScript64.exe).
"/SCRIPT=" est l'instruction permettant de préciser le script à lancer.
<Chemin du script> correspond au chemin complet du script à lancer.

Exemple :
c:\WinDev64\Programs\WDScript64.exe /SCRIPT="C:\Temp\test.wl"

Exécuter WDScript en mode console

Pour exécuter WDScript en mode console :

1. Ouvrez le mode console de Windows (raccourci "Windows R").
2. Saisissez "cmd" et validez.
3. Saisissez la ligne de commande suivante :
    <Chemin de WDScriptConsole> /SCRIPT=<Chemin du script>
    où :
       correspond au chemin complet de WDScriptConsole.exe (ou WDScriptConsole64.exe).
       "/SCRIPT=" est l'instruction permettant de préciser le script à lancer.
       <Chemin du script> correspond au chemin complet du script à lancer.

Exemple :

```
Autres
```
# WDScript : utilisation en ligne de

# commande et en mode console


c:\WinDev64\Programs\WDScriptConsole.exe /SCRIPT="C:\Temp\test.wl" >"c:\temp\log.log"

Remarque : Le résultat de la fonction Trace sera aché dans la sortie standard. Il est également possible
d'utiliser dans le script la fonction WLangage ConsoleEcrit.


