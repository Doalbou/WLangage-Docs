#### WINDEV WEBDEV

Présentation

L'utilitaire WDLog

Les diérentes opérations pouvant être réalisées avec WDLog sont les suivantes :
Sauvegarde des chiers de données HFSQL liés à une application WINDEV, WEBDEV ou WINDEV Mobile
Permet de créer une sauvegarde des chiers de données. En cas de problème, ces chiers de données
pourront être restaurés.
Restauration de chiers de données précédemment sauvegardés
Permet de restaurer une sauvegarde de chiers de données HFSQL précédemment eectuée avec
WDLog.
Mise à jour de chiers de données grâce à un chier journal
Permet d'eectuer toutes les opérations présentes dans un journal sur un chier de données.
Visualisation du journal
Permet de visualiser les informations enregistrées dans le chier Journal. Il est également possible
d'eectuer des recherches dans le journal.

Remarque : Lors d'une modication de l'analyse, le chier journal sera automatiquement sauvegardé au
moment de la modication automatique des chiers de données. Le chier journal sera ensuite purgé.

```
Avertissement
En version 28, cet outil avait pour nom "WDJournal".
```
Utilisation

Lancement de WDLog

WDLog peut être lancé :
En mode interactif :
depuis WINDEV, WEBDEV ou WINDEV Mobile : sous le volet "Outils", dans le groupe "Base de données",
cliquez sur "WDLog".
en lançant directement le programme "WDLog.EXE" présent dans le sous-répertoire "Programs" du
répertoire d'installation de WINDEV, WEBDEV et WINDEV Mobile.
Depuis une ligne de commande.

```
WINDEV Mobile Autres
```
### WDLog : Présentation


En mode interactif, les diérentes options du menu déroulant permettent d'accéder à toutes les
fonctionnalités de WDLog.

Conditions d'utilisation

WDLog est un outil redistribuable. WDLog peut être installé avec les applications développées avec WINDEV
et/ou WEBDEV. La licence d'utilisation de WINDEV, WEBDEV ou WINDEV Mobile s'applique intégralement.

Lors de la création de la procédure d'installation, il est possible d'intégrer WDLog à vos applications.

Rappel : La procédure d'installation peut être créée :

```
soit à partir de l'assistant. Pour lancer l'assistant, sous le volet "Projet", dans le groupe "Génération",
déroulez "Procédure d'installation" et sélectionnez "Créer la procédure d'installation".
soit à partir de l'éditeur d'installation. Pour lancer l'éditeur d'installation, sous le volet "Outils", dans le
groupe "Utilitaires", cliquez sur "WDInst".
```
Les chiers nécessaires à l'installation de WDLog sont les suivants :

```
WDLog.EXE wd300com.dll
```
```
wd300etat.dll wd300grf.dll
```

```
wd300hf.dll wd300mat.dll
```
```
wd300obj.dll wd300pnt.dll
```
```
wd300std.dll wd300sql.dll
```
```
wd300vm.dll wd300zip.dll
```
```
WDOutil.WDK WDLog_FR.pdf
```
```
WDLog_EN.pdf
```
Rappel : Journal d'un chier de données

WINDEV, WEBDEV et WINDEV Mobile orent la possibilité de créer un chier journal pour chaque chier de
données. Ce chier journal peut être :
Un chier des écritures seulement
Un chier des lectures et des écritures

Le journal contient l'historique de l'utilisation des chiers journalés :

```
Les valeurs des rubriques de l'enregistrement avant modication du chier de données,
Les valeurs des rubriques de l'enregistrement après modication du chier de données,
L'auteur de l'opération,
La date de l'opération,
Le poste ayant réalisé l'opération,
Un commentaire libre,
L'adresse IP du poste ayant réalisé l'opération,
Le nom de l'application,
Le nom réseau de l'utilisateur,
La nature de l'opération (ajout, modication, suppression, lecture, etc.).
```
La journalisation d'un chier de données est réalisée sous l'éditeur d'analyses de WINDEV, WEBDEV ou
WINDEV Mobile.


#### WINDEV WEBDEV

Présentation

WDLog permet d'appliquer à une sauvegarde d'un chier de données les diérentes opérations enregistrées
dans le journal de ce chier.

Il est ainsi possible, à partir d'une sauvegarde d'un chier de données de réappliquer toutes les modications
eectuées sur ce chier (et enregistrées dans le journal) jusqu'à une date donnée.

Cette re-génération d'un chier de données ne peut être réalisée que en mode interactif. Cette opération
nécessite :

```
Le chier journal associé au chier de données (*JNL.FIC).
Le mot de passe du chier journal (si ce mot de passe existe).
Le chier de données sur lequel les opérations du journal doivent être ré-eectuées. Si ce chier n'existe
pas, il est possible de re-créer le chier à partir des informations du journal.
```
Mode Interactif

Pour re-générer des chiers de données HFSQL

1. Lancez l'outil WDLog.
2. Sélectionnez l'option "Fichier .. Gestion des journaux" (ou cliquez sur le livre).
3. Cliquez sur le bouton "Restaurer un chier à partir de son journal".

```
WINDEV Mobile Autres
```
### WDLog : Restaurer un chier de

### données à partir de son journal


4. Indiquez :
    Le chier journal associé au chier de données.
    Le chier de données sera mis à jour grâce à ce chier journal. Ce chier doit être un chier de type
    <NomFichier>JNL.FIC.
    Le mot de passe associé au chier journal (s'il existe).
    Le chier de données sur lequel le chier journal doit être appliqué.
    Ce chier doit être le dernier chier de données correct existant. Si ce chier n'existe pas, WDLog peut
    tenter de re-créer le chier de données à partir du journal.
    Le répertoire dans lequel le chier de données sera créé.
    Ce répertoire doit être précisé et doit être diérent du répertoire contenant le chier de sauvegarde.
    La date et l'heure limite.
    Date et heure jusqu'auxquelles les opérations présentes dans le chier journal seront re-jouées sur le
    chier de sauvegarde. Le chier de données sera mis à jour. Si aucune date et heure ne sont précisées,
    toutes les opérations présentes dans le chier journal seront eectuées.
5. Cliquez sur le bouton "Restaurer" pour eectuer la restauration du chier.


#### WINDEV WEBDEV

Présentation

WDLog permet de visualiser le contenu d'un chier journal :
en mode HFSQL Classic. Le chier visualisé sous WDLog est le chier <NomFichierJournalé>JNL.FIC.
en mode HFSQL Client/Serveur. Il est cependant conseillé d'utiliser le Centre de Contrôle HFSQL.

Rappel :

```
Le mode de fonctionnement de la journalisation comporte quelques diérences en HFSQL Classic et
HFSQL Client/Serveur.
En programmation, la fonction HHistoriqueModication renvoie les modications apportées à une ou
plusieurs rubriques d'un enregistrement donné.
```
Mode Interactif

```
Visualiser le chier JournalOperation.FIC (HFSQL Classic)
```
Pour visualiser le chier JournalOperation.FIC (HFSQL Classic)

1. Lancez WDLog.
2. Sélectionnez l'option "Fichier .. Gestion des journaux" (ou cliquez sur le livre).
3. Cliquez sur le bouton "Ouvrir un journal HFSQL Classic".
4. Sélectionnez le chier journal de votre application (chier XXXJNL.FIC).
5. Le contenu du chier est aché.

```
Visualiser le chier Journal (HFSQL Client/Serveur)
```
Pour visualiser le chier Journal (HFSQL Client/Serveur)

1. Lancez WDLog.
2. Sélectionnez l'option "Fichier .. Gestion des journaux" (ou cliquez sur le livre).
3. Cliquez sur le bouton "Ouvrir un journal HFSQL Client/Serveur".
4. Décrivez la connexion au serveur HFSQL dans l'assistant qui s'ouvre.
5. Sélectionnez le chier journalé.

```
WINDEV Mobile Autres
```
### WDLog : Visualisation d'un chier

### journal

```
Disponible uniquement avec ces types de connexion
```

6. Le contenu du chier est aché.

Les diérentes informations achées

```
Adresse IP Adresse IP du poste qui a eectué l'opération.
```
```
Application Nom de l'application qui a eectué l'opération (utile dans le cas de chiers partagés
entre plusieurs applications).
Cette information est une chaîne sur 12 caractères.
```
```
Clé Valeur de la première clé unique du chier.
```
```
Date Date à laquelle l'opération a été eectuée.
```
```
Heure Heure à laquelle l'opération a été eectuée.
```
```
HPoste Identiant du poste qui a eectué l'opération (identiant déterminé par la fonction
HPoste).
Cette information est une chaîne de 16 caractères.
```
```
Nom Réseau Nom de la machine (limité à 12 caractères). Si ce nom comporte plus de 12
caractères, le début du nom est tronqué (c'est souvent la n du nom de la machine
qui est le plus déterminant).
Il est possible d'obtenir le nom de la machine du client grâce au chier
JNLUSER.Fic.
```
```
Notes Notes personnalisées dénies par la fonction HJournalInfo.
Cette information est une chaîne de 12 caractères.
```
```
Opération Opération eectuée sur le chier de données. Dans le chier de données, cette
opération est identiée par un numéro. La correspondance "Numéro - fonction
HFSQL" est disponible dans le chier ListeDenitionHF.WL présent dans le sous-
répertoire "\Personal\External" de WINDEV.
```
```
Valeurs La loupe permet de visualiser les diérentes valeurs de l'enregistrement :
Lors d'un ajout, la valeur ajoutée est visualisée.
Lors d'une modication, les valeurs avant et après modication sont visualisées.
Lors d'une suppression, les valeurs supprimées sont visualisées.
```
```
Opérations possibles
```
Cette fenêtre permet d'eectuer des recherches avancées sur tous les éléments enregistrés dans le journal. Il


est ainsi possible par exemple de rechercher toutes les modications eectuées par un poste sur une période
dénie ou encore de rechercher toutes les opérations eectuées par un poste spécique.


#### WINDEV WEBDEV

Présentation

WDLog permet de restaurer les chiers de données précédemment sauvegardés avec WDLog.

Cette restauration des chiers de données peut être réalisée :

```
En mode interactif (WDLog est lancé).
En mode "Ligne de commande". Le mode "Ligne de commande" permet d'inclure la gestion des
sauvegardes de vos chiers de données directement dans vos applications. Dans ce cas, l'utilisateur n'a
aucune manipulation spécique à réaliser.
Attention : Ce type de restauration doit être utilisé uniquement si aucun des chiers de données
sauvegardés n'est journalé.
```
Mode Interactif

Restaurer des chiers de données HFSQL précédemment sauvegardés

Pour restaurer des chiers de données HFSQL précédemment sauvegardés :

1. Lancez WDLog.
2. Sélectionnez l'option "Sauvegardes .. Restauration de données" (ou cliquez sur la èche verte).
3. Sélectionnez le répertoire contenant les chiers de données précédemment sauvegardés. Utilisez le
    bouton "Parcourir" si nécessaire. Validez.
4. Le nom de la sauvegarde et la liste des chiers de données présents dans la sauvegarde s'achent.
    Sélectionnez les chiers de données à restaurer (option cochée = chier de données à restaurer).

```
WINDEV Mobile Autres
```
### WDLog : Restauration de chiers de

### données HFSQL


5. Sélectionnez si nécessaire :
    Le répertoire de restauration. Par défaut, le répertoire de restauration est identique au répertoire
    contenant les chiers de données originaux. Il est possible de restaurer les chiers de données dans
    un autre répertoire (pour eectuer une comparaison par exemple). L'arborescence de la sauvegarde
    est restaurée.
    Il sut :
    - de cocher l'option "Modier le répertoire de restauration des données",
    - d'indiquer le répertoire de restauration (bouton "Parcourir").
    "Ne pas restaurer les journaux et mettre les chiers de données à jour avec les journaux
    actuels". Par défaut, cette option est cochée si des chiers journaux sont présents dans la
    sauvegarde : les chiers journaux (chiers XXXJNL.FIC) ne sont pas restaurés et sont automatiquement
    appliqués aux chiers de données restaurés.
6. Validez. La restauration est automatiquement eectuée.

Remarque : Si des chiers de données de même nom sont déjà présents dans le répertoire de restauration,
les chiers de données existants sont automatiquement renommés.

Mode ligne de commande

Pour restaurer des chiers de données, la syntaxe est :

WDLog /REST=<RepSauve> /REP_REST=<RepRestauration> /SANSREINDEXE=<Vrai ou Faux>
Le tableau ci-dessous liste les diérents éléments pouvant être présents sur la ligne de commande :

```
Paramètre Signication
```
```
/REST=<RepSauve> Chemin contenant les chiers de données sauvegardés
```
```
/REP_REST=<RepRestauration> Chemin où la restauration doit être eectuée
```
```
/SANSREINDEXE=<Vrai ou Faux> Si cette option est à Vrai, aucune ré-indexation des chiers de
données restaurés ne sera eectuée
```
Exemple : La ligne de commande suivante permet de restaurer les chiers de données présents dans le
répertoire "D:\Sauvegarde".

## LanceAppli("WDLog /REST=D:\Sauvegarde")


#### WINDEV WEBDEV

Présentation

WDLog permet de sauvegarder tous les chiers de données HFSQL utilisés par une application WINDEV ou
WEBDEV.

Pour réaliser cette sauvegarde, le chier suivant est nécessaire :

```
soit le chier de l'analyse (.WDD),
soit le chier .REP contenant les diérents chemins des chiers de données gérés par le projet.
```
Cette sauvegarde peut être réalisée :

```
En mode interactif (WDLog est lancé).
En mode "Ligne de commande". Le mode "Ligne de commande" permet d'inclure la gestion des
sauvegardes de vos chiers de données directement dans vos applications. Dans ce cas, l'utilisateur n'a
aucune manipulation spécique à réaliser.
```
Important : N'oublier pas de noter les références de toutes les sauvegardes eectuées (date de la
sauvegarde, répertoire de la sauvegarde, nature de la sauvegarde, emplacement de la sauvegarde, etc.). Ces
informations seront fondamentales pour restaurer les chiers de données.

Mode Interactif

Sauver des chiers de données HFSQL associés à une analyse

Pour sauver des chiers de données HFSQL associés à une analyse :

1. Lancez WDLog.
2. Sélectionnez l'option "Sauvegardes .. Sauvegarde de données" (ou cliquez sur la èche orange).
3. Sélectionnez à l'aide du bouton "Parcourir" :
    Soit le chier de l'analyse (.WDD) contenant la description des chiers de données gérés par le projet.
    Soit le chier .REP contenant les diérents chemins des chiers de données gérés par le projet.

```
WINDEV Mobile Autres
```
### WDLog : Sauvegarde de chiers de

### données HFSQL

```
Disponible uniquement avec ces types de connexion
```

4. La liste des chiers de données présents dans le .REP de l'application apparaît. Dans cette liste, il est
    possible de :
       Supprimer des chiers de données HFSQL (chiers .FIC, .MMO ou .NDX) avec le bouton "Enlever".
       Ajouter des chiers de données HFSQL (chiers .FIC, .MMO ou .NDX) avec le bouton "Autres".
       Enregistrer la liste des chiers de données sous forme d'un chier "Liste" (extension LST) avec le
       bouton "Enregistrer". Ce chier liste pourra être relu directement avec WDLog ou utilisé en mode ligne
       de commande.
       Attention : A chaque enregistrement, le chier "liste" n'est pas vidé.
       Ouvrir une liste de chiers de données existante avec le bouton "Ouvrir".
5. Validez la sauvegarde des chiers de données listés en cliquant sur le bouton "OK".
6. Dans la fenêtre de sauvegarde qui s'ouvre, renseignez les éléments suivants :
    Répertoire de la sauvegarde : Répertoire dans lequel le répertoire de sauvegarde sera créé.
    Nom de la sauvegarde : Nom du répertoire dans lequel la sauvegarde va être réalisée.
    Spéciez les options de sauvegarde :
       Ne pas créer de sous-répertoire du nom de la sauvegarde : Le répertoire de sauvegarde n'est
       pas créé.
       Compression : permet de compacter les chiers lors de la sauvegarde. Cette option permet de
       réduire la taille de stockage des sauvegardes. Un seul chier archive de type WDZ sera créé.
       Si cette option n'est pas cochée, les chiers seront uniquement copiés dans le répertoire de
       sauvegarde.
       Multi-volumes : permet de compacter les chiers lors de la sauvegarde et de regrouper les chiers
       dans des archives de 1.4 Mo. Cette option active automatiquement le mode "Compression".
       Ne pas sauver les index (.NDX) : permet de réduire la taille de la sauvegarde. Si cette option est
       cochée, il sera nécessaire de réindexer les chiers de données après leur restauration.
       Rappel : WINDEV propose diérentes solutions pour réindexer des chiers de données : WDTool
       (non redistribuable), WDOptimizer, WDMAP (non redistribuable), ou par programmation avec la
       fonction du WLangage HRéindexe.
       Ne pas bloquer les chiers : permet de sauvegarder les chiers même s'ils sont en cours
       d'utilisation. Cette option est déconseillée car la sauvegarde risque de contenir des enregistrements
       bloqués, qui ne seront plus accessibles.
       Cette option est conseillée dans des cas très spéciques, par exemple pour des applications
       lancées en tâche de fond, ouvrant les chiers mais n'utilisant pas de transactions, ... Cette option
       peut aussi être utilisée avec des applications manipulant des chiers de données indépendants
       (non reliés dans l'analyse).
7. Lancez la sauvegarde en cliquant sur le bouton "OK".

Mode ligne de commande

Le mode ligne de commande permet deux types de sauvegardes :


```
Sauvegarde de tous les chiers de données décrits soit dans une analyse, soit dans le chier .REP de
l'application.
Sauvegarde d'une liste de chiers de données.
```
Pour plus de détails sur les diérentes options, consultez le paragraphe précédent "Mode interactif".

Remarque : Un chier WDLog.LOG est automatiquement créé. Ce chier contient les opérations réalisées.

Sauver tous les chiers de données d'un chier WDD ou d'un chier .REP

Pour sauver tous les chiers de données d'un chier WDD ou d'un chier .REP, la syntaxe est :

WDLog /APPLI=<NomCompletWdd ou NomCompletREP>
/REP = <RepSauve>
/COMPRESS = <Vrai / Faux>
/MUET = <Vrai / Faux>
/MULTI = <Vrai / Faux>
/SANSBLOCAGE = <Vrai / Faux>
/SANSINDEX = <Vrai / Faux>
/SANSSOUSREP = <Vrai / Faux>

Détail des paramètres :

```
Paramètre Signication
```
```
/APPLI = <NomCompletWdd ou
NomCompletREP>
```
```
Chaîne de caractères contenant le nom complet de l'analyse (chier
".WDD") ou le nom complet du chier ".REP" de l'application.
```
```
/REP=<RepSauve> Chemin où sont sauvegardés les chiers
```
```
/COMPRESS=<Vrai / Faux> Si cette option correspond à la chaîne de caractères "Vrai", compresse
les chiers de données. Les chiers seront enregistrés dans une archive
(chier .WDZ).
Dans le cas contraire, les chiers ne seront pas compressés.
Par défaut, cette option vaut "Vrai".
```
```
/MUET=<Vrai / Faux> Si cette option correspond à la chaîne de caractères "Vrai", en cas
d'erreur bloquante, toutes les opérations eectuées seront inscrites
dans un chier résultat (chier .LOG). L'exécution de WDLog ne sera pas
bloquée.
Dans le cas contraire, une fenêtre s'achera en cas d'erreur.
Par défaut, cette option vaut "Faux".
```
```
/MULTI=<Vrai / Faux> Si cette option correspond à la chaîne de caractères "Vrai", découpe
l'archive de sauvegarde en chiers de 1.4 Mo. Si cette option est utilisée,
il n'est pas nécessaire de spécier l'option de compression.
```

```
Dans le cas contraire, l'archive n'est pas découpée.
Par défaut, cette option vaut "Faux".
```
```
/SANSBLOCAGE=<Vrai / Faux> Si cette option correspond à la chaîne de caractères "Vrai", seuls les
chiers de données qui ne sont pas bloqués seront sauvegardés.
Dans le cas contraire, tous les chiers de données sont sauvegardés.
Par défaut, cette option vaut "Faux".
```
```
/SANSINDEX=<Vrai / Faux> Si cette option correspond à la chaîne de caractères "Vrai", les index des
chiers de données ne sont pas sauvegardés.
Dans le cas contraire, les index sont sauvegardés.
Par défaut, cette option vaut "Faux".
```
```
/SANSSOUSREP=<Vrai / Faux> Si cette option correspond à la chaîne de caractères "Vrai", le sous-
répertoire de sauvegarde ne sera pas créé. La sauvegarde sera
eectuée directement dans le répertoire <RepSauve>.
Dans le cas contraire, un sous-répertoire de sauvegarde est créé.
Par défaut, cette option vaut "Faux".
```
Exemple : La ligne de commande suivante permet de sauvegarder l'ensemble des chiers de l'analyse
"C:\MonProjet\MonAnalyse.WDD" dans le répertoire "D:\Sauvegarde de mes projets". Ces chiers sont ensuite
compressés. Les chiers d'index ne sont pas sauvegardés.

Attention : Si les noms de répertoire utilisent des espaces, il est nécessaire d'entourer le paramètre de
guillemets.

# LanceAppli("WDLog /APPLI= C:\MonProjet\MonAnalyse.WDD " + ...

## "/REP=""D:\Sauvegarde de mes projets"" /COMPRESS=Vrai /SANSINDEX=Vrai")

Sauver tous les chiers de données d'une base Client/Serveur HFSQL

Pour sauver tous les chiers de données d'une base Client/Serveur HFSQL, la syntaxe est :

WDLog /SERVEUR = <Nom Serveur>
/BD = <Nom de la base>
/NOM = <Nom de l'utilisateur>
/MDP_DB = <Mot de passe>
/REP = <RepSauve>
/COMPRESS = <Vrai / Faux>
/MUET = <Vrai / Faux>
/MULTI = <Vrai / Faux>
/SANSSOUSREP = <Vrai / Faux>


/LISTE = <NomFichier>
/APPLI = <NomAppli>

Détail des paramètres :

```
Paramètre Signication
```
```
/SERVEUR=<Nom du serveur> Chaîne de caractères contenant le nom du serveur HFSQL Client/Serveur
ou l'adresse IP du serveur.
```
```
/BD = <Nom de la base> Chaîne de caractères contenant le nom de la base HFSQL Client/Serveur à
sauver.
```
```
/NOM = <Nom de
l'utilisateur>
```
```
Chaîne de caractères contenant le nom de l'utilisateur se connectant à la
base.
```
```
/MDP_DB = <Mot de passe> Chaîne de caractères contenant le mot de passe associé à l'utilisateur
pour la base de données.
```
```
/REP=<RepSauve> Chemin où sont sauvegardés les chiers
```
```
/COMPRESS=<Vrai / Faux> Si cette option correspond à la chaîne de caractères "Vrai", compresse les
chiers de données. Les chiers seront enregistrés dans une archive
(chier .WDZ).
Dans le cas contraire, les chiers ne seront pas compressés.
Par défaut, cette option vaut "Vrai".
```
```
/MUET=<Vrai / Faux> Si cette option correspond à la chaîne de caractères "Vrai", en cas d'erreur
bloquante, toutes les opérations eectuées seront inscrites dans un
chier résultat (chier .LOG). L'exécution de WDLog ne sera pas bloquée.
Dans le cas contraire, une fenêtre s'achera en cas d'erreur.
Par défaut, cette option vaut "Faux".
```
```
/MULTI=<Vrai / Faux> Si cette option correspond à la chaîne de caractères "Vrai", découpe
l'archive de sauvegarde en chiers de 1.4 Mo. Si cette option est utilisée, il
n'est pas nécessaire de spécier l'option de compression.
Dans le cas contraire, l'archive n'est pas découpée.
Par défaut, cette option vaut "Faux".
```
```
/SANSSOUSREP=<Vrai / Faux> Si cette option correspond à la chaîne de caractères "Vrai", le sous-
répertoire de sauvegarde ne sera pas créé. La sauvegarde sera eectuée
directement dans le répertoire <RepSauve>.
Dans le cas contraire, un sous-répertoire de sauvegarde est créé.
Par défaut, cette option vaut "Faux".
```

```
/LISTE = <NomFichier> Nom complet du chier contenant la liste des chiers de données à
sauvegarder. Ce chier au format texte contient un nom de chier par
ligne. Il peut être créé par WDLog (bouton "Enregistrer").
Exemple :
```
# E:\WD Graphe Boursier\Exe\Action.FIC

# E:\WD Graphe Boursier\Exe\Action2000.FIC

# E:\WD Graphe Boursier\Exe\Cours.FIC

```
/APPLI=<NomAppli> Nom de l'application qui sera utilisé pour identier la sauvegarde
("Sauvegarde automatique de " + <NomAppli>).
```
Exemple : La ligne de commande suivante permet de sauvegarder l'ensemble des chiers de la base
"MabaseHF" dans le répertoire "D:\Sauvegarde de mes projets". Ces chiers sont ensuite compressés. Les
chiers d'index ne sont pas sauvegardés.

# LanceAppli("WDLog /SERVEUR=123.123.123.1" + "/BD=MaBaseHF /NOM=Flo /MDP_DB=Test" + ...

# "/REP=""D:\Sauvegarde de mes projet""" + ...

## "/COMPRESS=Vrai /SANSINDEX=Vrai /APPLI=MaBaseHF")

Sauver tous les chiers de données présents dans une liste

Pour sauver une liste de chiers de données, il sut de créer un chier texte contenant les diérents noms
physiques des chiers à sauvegarder. Ce chier peut être créé avec WDLog lancé en mode interactif.

La ligne de commande est la suivante :
WDLog /LISTE = <NomFichier>
 /REP = <RepSauve>
 /COMPRESS = Vrai
 /MUET = Vrai
 /MULTI = Vrai
 /SANSBLOCAGE = Vrai
 /SANSINDEX = Vrai
 /SANSSOUSREP = Vrai

Le tableau ci-dessous liste les diérents éléments pouvant être présents sur la ligne de commande :

```
Paramètre Signication
```
```
/LISTE = <NomFichier> Nom du chier contenant la liste des chiers de données à sauvegarder.
Ce chier au format texte contient un nom de chier par ligne. Il peut être
créé par WDLog (bouton "Enregistrer").
Exemple :
```

```
E:\WD Graphe Boursier\Exe\Action.FIC
E:\WD Graphe Boursier\Exe\Action2000.FIC
E:\WD Graphe Boursier\Exe\Cours.FIC
```
```
/REP=<RepSauve> Chemin où sont sauvegardés les chiers
```
```
/COMPRESS=Vrai Si cette option correspond à la chaîne de caractères "Vrai", compresse les
chiers de données. Les chiers seront enregistrés dans une archive
(chier .WDZ)
```
```
/MUET=Vrai Si cette option correspond à la chaîne de caractères "Vrai", en cas d'erreur
bloquante, toutes les opérations eectuées seront inscrites dans un
chier résultat (chier .LOG). L'exécution de WDLog ne sera pas bloquée.
```
```
/MULTI=Vrai Si cette option correspond à la chaîne de caractères "Vrai", découpe
l'archive de sauvegarde en chiers de 1.4 Mo. Si cette option est utilisée, il
n'est pas nécessaire de spécier l'option de compression.
```
```
/SANSBLOCAGE=Vrai Si cette option correspond à la chaîne de caractères "Vrai", seuls les
chiers de données qui ne sont pas bloqués seront sauvegardés.
```
```
/SANSINDEX=Vrai Si cette option correspond à la chaîne de caractères "Vrai", les index des
chiers de données ne sont pas sauvegardés.
```
```
/SANSSOUSREP=Vrai Si cette option correspond à la chaîne de caractères "Vrai", le sous-
répertoire de sauvegarde ne sera pas créé. La sauvegarde sera eectuée
directement dans le répertoire <RepSauve>.
```
Exemple : La ligne de commande suivante permet de sauvegarder les chiers de données présents dans la
liste "C:\MaListe.LST" dans la répertoire "D:\Sauvegarde". Les chiers en cours d'utilisation ne seront pas
sauvegardés.

## LanceAppli("WDLog /LISTE=C:\MaListe.LST /REP=D:\Sauvegarde/SANSBLOCAGE=Vrai")


