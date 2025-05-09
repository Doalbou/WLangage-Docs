#### WINDEV WEBDEV

### Présentation

L'utilitaire WDConver

WDConver est un utilitaire permettant de convertir vers un chier de données HFSQL Classic, les données
d'un chier :
au format Hyper File 5 ou 4.
au format texte.
au format XML.
d'une base de données accédée via un provider OLE DB ou un driver ODBC (Excel, Access, Oracle, SQL
Server, etc.).
d'une base de données accédée via un Connecteur Natif WINDEV (SQL Server, Oracle ou AS/400).

Attention : WDConver permet uniquement de convertir les données d'un chier. Pour eectuer cette
conversion, il est nécessaire de convertir au préalable la structure du chier de données. Pour convertir la
structure d'un chier de données, sous l'éditeur d'analyses, sous le volet "Analyse", dans le groupe
"Création", déroulez "Importer" et sélectionnez "Importer des descriptions de chiers/tables".

Remarque : Par programmation, les importations peuvent être réalisées grâce aux fonctions HImporteHF55,
HImporteTexte, HImporteXML, ...

Exemple d'utilisation : Après une mise à jour importante des données d'un chier externe, WDConver
permet de ré-importer toutes les données dans une base de données WINDEV.

### Utilisation

Conditions d'utilisation

WDConver est un outil redistribuable. WDConver peut être installé avec les applications développées avec
WINDEV. La licence d'utilisation de WINDEV s'applique intégralement.

Lors de la création de la procédure d'installation, il est possible de livrer WDConver avec vos applications.

Rappel : La procédure d'installation peut être créée :

```
soit depuis l'assistant : sous le volet "Projet", dans le groupe "Génération", déroulez "Procédure
d'installation" et sélectionnez "Créer la procédure d'installation",
```
```
WINDEV Mobile Autres
```
## WDConver : Présentation

```
Disponible uniquement avec ce type de connexion
```

```
soit depuis l'éditeur d'installation : sous le volet "Outils", dans le groupe "Utilitaires", cliquez sur "WDInst".
```
Installation de WDConver sur un autre poste

Les chiers nécessaires à l'installation de WDConver sont les suivants :

```
WDConver.EXE wd300cpl.dll
```
```
wdcnv300.dll wd300hf.dll
```
```
wd300mdl.dll wd300obj.dll
```
```
wd300pnt.dll wd300std.dll
```
```
wd300vm.dll wd300xml.dll
```
```
WDOutil.WDK
```
```
DLLs nécessaires à la base à convertir (WD55HF.DLL, wd300oldb.dll, etc.)
```
```
WDConver_FR.PDF WDConver_EN.PDF
```
### Lancement de WDConver

WDConver peut être lancé :
En mode interactif, en lançant directement le programme "WDConver.EXE" ou depuis l'éditeur
d'analyses : sous le volet "Analyse", dans le groupe "Création", déroulez "Importer" et sélectionnez
"Importer des données d'une autre base".
En mode ligne de commande pour exécuter une conversion directement depuis une application
WINDEV.


#### WINDEV WEBDEV

### Présentation

Avant toute utilisation de WDConver, il est nécessaire de disposer de :
L'analyse WINDEV (chier ".WDD") dans laquelle les données doivent être importées. Cette analyse doit
avoir été générée au moins une fois.
Rappel : Cette analyse doit contenir la structure des chiers de données HFSQL dans lesquels les données
seront importées.
La base de données contenant les données à importer.

### Choix de la conversion

A son lancement, WDConver propose de :
Créer une nouvelle description de conversion. A la n de sa description, cette conversion sera
automatiquement exécutée.
Choisir une description de conversion existante (chier ".WDV") déjà créée avec WDConver. La
conversion est automatiquement exécutée.
Il est ainsi possible d'exécuter directement une conversion sans la re-décrire.
Une description de conversion peut également être utilisée pour lancer une conversion depuis une
application WINDEV. Pour plus de détails, consultez
Lancement de WDConver en mode ligne de commande.

### Conversion des données d'un chier d'une base externe vers un chier

### de données HFSQL

Pour décrire et convertir les données d'un chier d'une base de données externe vers un chier de données
HFSQL :

1. Lancez WDConver et validez les diérents écrans jusqu'au plan "Choix de la source de données".
2. Sélectionnez la source de données "Une base externe".
3. Sélectionnez l'analyse HFSQL Classic (chier ".WDD") contenant la structure des chiers externes à
    convertir.

```
WINDEV Mobile Autres
```
## WDConver : Utilisation en mode

## interactif

```
Disponible uniquement avec ce type de connexion
```

4. Précisez si nécessaire le mot de passe en exécution de cette analyse. Ce mot de passe a été déni dans la
    description de l'analyse.
5. Sélectionnez le mode d'accès à la base de données externe (option "Type"). La connexion peut être
    réalisée via :
       un provider OLE DB,
       un driver ODBC,
       un accès natif (AS/400, Oracle, SQL Server, ...).
       Remarque : Pour dénir des paramètres de connexion avancés, cliquez sur le bouton.
6. Spéciez la source de données de la connexion. Cette source de données peut correspondre :
    Soit au nom et au chemin complet de la base de données.
    Par exemple, pour Access : "C:\MonRépertoire\BaseDeDonnéesAccess.MDB"
    Soit au nom ou à l'alias du serveur.
    Par exemple, pour Oracle : "Serveur_Oracle"
    Soit au répertoire contenant le chier xBase (".DBF").
    Par exemple : "C:\MonRépertoirexBase"
7. Saisissez si nécessaire le nom de l'utilisateur utilisé pour se connecter à la base de données.
    Remarque : Ce nom a été déni lors de la création de la base de données. Il peut exister plusieurs
    utilisateurs ayant des droits diérents sur une même base de données.
8. Saisissez si nécessaire le mot de passe utilisé pour se connecter à la base de données. Ce mot de passe a
    été déni lors de la création de la base de données.
9. Sélectionnez les chiers (tables) dont les données doivent être importées. La description de ces chiers
    doit être à la fois présente dans la base de données source et dans l'analyse WINDEV destination.
    Remarque : Si aucune table n'est trouvée, saisissez directement le nom de la table dont les données
    doivent être importées.
10. Indiquez le répertoire dans lequel les chiers de données HFSQL Classic seront créés.
11. Sauvegardez si nécessaire la description de la conversion (chier ".WDV") an de pouvoir la réutiliser.
12. Lancez la conversion des données (bouton de validation de l'assistant). Les chiers de données HFSQL
Classic sont automatiquement créés dans le répertoire indiqué.
Remarque : Si ces chiers existent déjà, la conversion des données ajoutera les enregistrements
convertis à la suite des enregistrements existants.

### Conversion des données d'un chier au format Hyper File 5 vers un

### chier de données HFSQL Classic

```
Pour décrire et convertir un chier au format Hyper File 5 vers un chier de données HFSQL Classic :
```
1. Lancez WDConver et validez les diérents écrans jusqu'au plan "Choix de la source de données".
2. Sélectionnez la source de données "Hyper File 5".


3. Sélectionnez l'analyse au format Hyper File 5 associée aux données à convertir (chier ".WDD") et précisez
    si nécessaire le mot de passe en exécution de cette analyse. Ce mot de passe a été déni dans la
    description de l'analyse.
4. Sélectionnez l'analyse HFSQL Classic (chier ".WDD") contenant la structure des chiers contenant les
    données à convertir et précisez si nécessaire le mot de passe en exécution de cette analyse. Ce mot de
    passe a été déni dans la description de l'analyse.
5. Sélectionnez les chiers (chiers ".FIC") dont les données doivent être importées. La description de ces
    chiers doit être à la fois présente dans la base de données source et dans l'analyse destination. Indiquez
    si nécessaire leur nom logique et leur mot de passe.
6. Indiquez le répertoire dans lequel les chiers de données HFSQL Classic seront créés.
7. Sauvegardez si nécessaire la description de la conversion (chier ".WDV") an de pouvoir la réutiliser.
8. Lancez la conversion de données (bouton de validation de l'assistant). Les chiers de données HFSQL
    Classic sont automatiquement créés dans le répertoire indiqué.
    Remarque : Si ces chiers existent déjà, la conversion des données ajoutera les enregistrements
    convertis à la suite des enregistrements existants.


#### WINDEV WEBDEV

### Présentation

Mode ligne de commande

L'utilisation de WDConver en mode ligne de commande consiste à exécuter une description de conversion
créée et sauvegardée avec WDConver (chier ".WDV").

Pour lancer WDConver en ligne de commande, la syntaxe est la suivante :

WDConver.EXE [-report][-error][-wizard]/SCRIPT=<FichierWDV>

Détails des paramètres :

```
Paramètres Signication
```
```
[-report] Si ce paramètre est précisé, un compte-rendu sera aché à
la n de l'exécution du script.
Par défaut, si ce paramètre n'est pas précisé, aucun compte-
rendu ne sera aché à la n de l'exécution du script.
```
```
[-error] Si ce paramètre est précisé, en cas d'erreur, un message
sera aché à la n de l'exécution du script.
Par défaut, si ce paramètre n'est pas précisé, aucun
message d'erreur ne sera aché à la n de l'exécution du
script.
```
```
[-wizard] Si ce paramètre est précisé, l'assistant de conversion des
données se lancera.
Par défaut, si ce paramètre n'est pas précisé, l'assistant de
conversion des données ne se lancera pas.
```
```
/SCRIPT=<FichierWDV> Chaîne de caractères contenant le nom et le chemin complet
de la description de conversion à utiliser (chier ".WDV").
Ce paramètre est obligatoire sauf si le paramètre "-wizard"
est spécié.
```
```
WINDEV Mobile Autres
```
## WDConver : Utilisation en mode

## ligne de commande

```
Disponible uniquement avec ce type de connexion
```

/WDD=<Chemin analyse> Chaîne de caractères contenant le chemin de l'analyse
WINDEV, WEBDEV ou WINDEV Mobile. Si ce chemin contient
des espaces, il doit être mis entre guillemets.

/PWD=<Mot de passe (non crypté) de
l'analyse>

```
Chaîne de caractères contenant le mot de passe de l'analyse
WINDEV, WEBDEV ou WINDEV Mobile. Si ce mot de passe
contient des espaces, il doit être mis entre guillemets.
```
/WDD55=<Chemin analyse WINDEV 5.5> Chaîne de caractères contenant le chemin de l'analyse
WINDEV 5.5. Si ce chemin contient des espaces, il doit être
mis entre guillemets.

/PWD55=<Mot de passe (non crypté) de
l'analyse WINDEV 5.5>

```
Chaîne de caractères contenant le mot de passe de l'analyse
WINDEV 5.5. Si ce mot de passe contient des espaces, il doit
être mis entre guillemets.
```
/SRCDIR=<Répertoire des chiers de
données Hyper File 5.5 recherchés>

```
Chaîne de caractères contenant le chemin des chiers de
données Hyper File 5.5 à convertir.
```
/DSTDIR=<Répertoire des chiers de
données convertis>

```
Chaîne de caractères contenant le répertoire où les chiers
de données converti au format HFSQL Classic seront créés.
```
/FILE=<Fichier de données source> Chaîne de caractères contenant :
soit le chemin du chier de données Hyper File 5.5 à
convertir
soit le nom de la table à convertir sur le serveur.

/NAME=<Nom logique dans l'analyse
WINDEV 5.5 du chier à convertir>

```
Chaîne de caractères correspondant au nom logique du
chier de données à convertir dans l'analyse WINDEV,
WEBDEV ou WINDEV Mobile.
```
/FILEPWD55=<Mot de passe non crypté du
chier source>

```
Chaîne de caractères correspondant au mot de passe du
chier WINDEV 5.5 à convertir.
```
/FILEDST=<Chemin destination du chier
converti>

```
Chaîne de caractères correspondant au chemin du chier
converti
```
/NOREP Permet d'ignorer le chier .REP au format WINDEV 5.5.

/MODE=[HF5 | EXTERN | XML | TEXT] Type
des chiers sources

```
Dénit le format des chiers à importer :
HF5 : chiers de données Hyper File 5.
EXTERN : chiers/tables externes (exemple : base C/S)
XML : chiers XML
```

```
TEXT : chiers texte
```
```
/PROVIDER=<Provider OLEDB ou
Connecteur Natif>
```
```
Chaîne de caractères permettant de dénir le provider ou le
Connecteur Natif (également appelé Accès Natif) permettant
d'accéder aux données à convertir.
Pour les Connecteurs Natifs, utilisez les chaînes de
caractères suivantes : WinDevOracle, WinDevSQLServer,
WinDevInformix, ...
```
```
/DATASOURCE=<Nom de la source (chier
ou serveur)>
```
```
Chaîne de caractères. Ce paramètre est utilisé lors de la
conversion d'un chier par Connecteur Natif, provider OLE
DB, ...
Correspond au nom de la source de données.
```
```
/USER=<Nom utilisateur> Chaîne de caractères. Correspond au nom de l'utilisateur de
la source de données.
```
```
/USERPWD=<Mot passe non crypté
utilisateur>
```
```
Chaîne de caractères. Correspond au mot de passe de
l'utilisateur de la source de données.
```
```
/DATABASE=<Nom base de données> Chaîne de caractères. Correspond à la base de données
accédée (s'il en existe plusieurs sur le serveur).
```
Remarque : Le tableau ci-dessus présente les diérents paramètres pouvant être utilisés pour lancer
WDConver en mode ligne de commande. Pour obtenir directement ces paramètres lors du lancement de
WDConver, utilisez une des syntaxes suivantes :
WDConver.EXE /help
WDConver.EXE /?

Remarque : Les scripts créés avec une version antérieure de WINDEV 7 ne sont pas utilisables avec
WDConver version 8 et supérieure. Les scripts créés avec WINDEV 7.5 sont utilisables avec WDConver version
8 et supérieure.

### Exemples

Exemple d'utilisation d'un script :

La ligne de commande suivante permet d'exécuter la description de conversion
"C:\MonRépertoire\MaDescription.WDV". En cas d'erreur, un message sera aché à la n de la modication
automatique des chiers de données (paramètre "-error"). L'assistant de la modication automatique des
chiers de données ne se lancera pas.

# LanceAppli("C:\MesOutils\WDConver.EXE " +...

## "-error/SCRIPT=C:\MonRépertoire\MaDescription.WDV")


Exemple d'utilisation

La ligne de commande suivante permet de :
Sélectionner tous les chiers Hyper File 5 accessibles par le chier ".REP" et dans le répertoire "C:\data".
Convertir ces chiers au format HFSQL Classic dans le répertoire "C:\dataclassic".

# LanceAppli("C:\MesOutils\WDConver.EXE " +...

# "/WDD55=C:\WDProjet\Projet5\Projet.WD5\Projet.WDD" +...

# "/WDD=""C:\Mes Projets\Projet\Projet.wdd" +...

## "/SRCDIR=""C:\data"" /DSTDIR=c:\dataclassic")

Exemple de conversion d'un seul chier

La ligne de commande suivante permet de convertir uniquement un chier spécique :

# LanceAppli("C:\MesOutils\WDConver.EXE " +...

# "/WDD55=C:\WDProjet\Projet5\Projet.WD5\Projet.WDD " +...

# "/WDD=C:\Mes Projets\Projet\Projet.wdd " +...

# "/FILE=C:\data\echange.fic /NAME=ECHANGE " +...

## "/DSTDIR=c:\dataclassic /NOREP")

Exemple de conversion en utilisant un Connecteur Natif (ou Accès Natif)

La ligne de commande suivante permet de convertir à l'aide du Connecteur Natif Oracle la table
"DEMO.CUSTOMER". Cette table a pour nom logique "CUSTOMER" sur le serveur "MARS". Le chier de
données HFSQL Classic sera créé dans le répertoire "c:\data".

# LanceAppli("C:\MesOutils\WDConver.EXE " +...

## "/MODE=EXTERN /DATASOURCE=MARS "+...

## "/PROVIDER=WinDevOracle /USER=DEMO "+...

## "/USERPWD=DEMO "+...

## "/WDD=""C:\Mes Projets\test.ANA\test.wdd"""+...

## "/DSTDIR=c:\data /FILE=DEMO.CUSTOMER /NAME=CUSTOMER")


