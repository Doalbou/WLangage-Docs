#### WINDEV WEBDEV

Présentation

L'utilitaire WDOptimizer

Les diérentes opérations pouvant être réalisées avec WDOptimizer sont les suivantes :
Optimisation des index
Cette option permet d'eectuer plusieurs types d'opérations :

1. Vérier les index : Vérie la cohérence entre l'index et les chiers de données.
2. Optimiser la vitesse des index (Re-calcul des statistiques) : Optimise les index en calculant les
    statistiques sur les index. Ces statistiques permettent d'optimiser les ltres, les requêtes et les vues
    HFSQL.
    Remarque : Plus le chier de données est modié et moins les statistiques reètent le contenu du
    chier de données HFSQL. Plus le chier de données contient d'enregistrements et moins la
    modication d'un enregistrement a d'impact sur les statistiques.
3. Reconstruire les index : Optimise l'accès aux enregistrements du chier de données et re-calcule les
    statistiques. Tous les enregistrements rayés sont automatiquement supprimés.
4. Reconstruire les index et les mémos : Optimise la totalité du chier de données, de son index et ses
    mémos.
5. Réviser et compresser les index et les mémos : Optimise la totalité du chier de données, de son
    index et ses mémos. Les mémos seront compressés. Des options avancées sont disponibles ("Options
    de compression des mémos").
Visualisation des propriétés d'un chier
Ache les caractéristiques d'un chier de données (nom, extension, format, cryptage, etc.).
Édition et modication d'un chier ".REP"
Optimise l'accès aux chiers de données.
Annulation d'une transaction ou libération d'enregistrements en transaction
Permet d'annuler une transaction sans interrompre l'exécution du programme.

```
Avertissement
En version 28, cet outil avait pour nom "WDOptimiseur".
```
```
WINDEV Mobile Autres
```
### WDOptimizer : Présentation

```
Disponible uniquement avec ce type de connexion
```

Utilisation

Lancement de WDOptimizer

WDOptimizer peut être lancé en mode interactif grâce à une des méthodes suivantes :
Depuis WINDEV, WEBDEV ou WINDEV Mobile, sous le volet "Outils", dans le groupe "Base de données",
cliquez sur "WDOptimizer".
Lancez directement le programme "WDOptimizer.EXE".

Les diérentes opérations pouvant être réalisées avec WDOptimizer sont les suivantes :

1. Optimiser les index. Pour plus de détails, consultez Optimisation des index.
2. Visualiser les propriétés d'un chier. Ce chier de données peut être sélectionné dans la liste achée à
    l'écran, ou sélectionné grâce au sélecteur de chiers.
3. Éditer un chier .REP : Il sut de sélectionner le chier .REP voulu. Pour plus de détails, consultez
    Édition et modication d'un chier ".REP"
4. Manipuler les transactions. Pour plus de détails, consultez
    Annulation d'une transaction ou libération d'enregistrements en transaction

Remarque : Sur le poste de développement, WDOptimizer peut aussi être lancé directement depuis WDTool.

Il est également possible de lancer WDOptimizer en ligne de commande. Pour plus de détails, consultez
Lancer WDOptimizer en ligne de commande.

Conditions d'utilisation

WDOptimizer est un outil redistribuable. WDOptimizer peut être installé avec les applications développées
avec WINDEV ou WEBDEV. La licence d'utilisation de WINDEV ou WEBDEV s'applique intégralement.

Lors de la création de la procédure d'installation, WDOptimizer est automatiquement livré avec vos
applications.

Rappel : La procédure d'installation peut être créée :

```
soit à partir de l'assistant : sous le volet "Projet", dans le groupe "Génération", cliquez sur "Procédure
d'installation".
soit à partir de l'éditeur d'installation : sous le volet "Outils", dans le groupe "Utilitaires", cliquez sur
"WDInst".
```
Fichiers nécessaires

Les chiers nécessaires à l'installation de WDOptimizer sont les suivants :

```
WDOptimizer.EXE wd300etat.dll
```
```
wd300hf.dll wd300html.dll
```

```
wd300mat.dll wd300obj.dll
```
```
wd300pnt.dll wd300prn.dll
```
```
wd300sql.dll wd300std.dll
```
```
wd300vm.dll wd300xml.dll
```
```
wd300com.dll wd300xtrs.dll
```
```
WDOutil.WDK WDOptimizer_FR.PDF
```
```
WDOptimizer_EN.PDF
```
Pour désinstaller WDOptimizer d'un poste, il sut d'eacer son répertoire.

Rappel : Index d'un chier

L'index d'un chier de données est un chier spécique (.NDX). Ce chier est créé en fonction des clés de
parcours dénies sur le chier de données. Il permet de retrouver rapidement des données dans un chier
de données.

Pour un meilleur fonctionnement des recherches dans vos chiers de données, il est conseillé d'optimiser
l'index régulièrement.


#### WINDEV WEBDEV

Présentation

WDOptimizer propose plusieurs modes d'optimisation des index :

1. Vérier les index : Vérie la cohérence entre l'index et les chiers de données.
2. Optimiser la vitesse des index (Recalcul des statistiques) : Optimise les index en calculant les
statistiques sur les index. Ces statistiques permettent d'optimiser les ltres, les requêtes et les vues HFSQL.
Remarque : Plus le chier de données est modié et moins les statistiques reètent le contenu du chier de
données HFSQL. Plus le chier de données contient d'enregistrements et moins la modication d'un
enregistrement a d'impact sur les statistiques.
3. Reconstruire les index : Optimise l'accès aux enregistrements du chier de données et re-calcule les
statistiques. Tous les enregistrements rayés sont automatiquement supprimés.
4. Reconstruire les index et les mémos : Optimise la totalité du chier de données, de son index et ses
mémos.
5. Réviser et compresser les index et les mémos : Optimise la totalité du chier de données, de son index
et ses mémos. Les mémos seront compressés. Des options avancées sont disponibles ("Options de
compression des mémos").
Remarques :

```
Le chier de données est recréé : la date de dernière écriture du dernier enregistrement (obtenue par la
fonction HDateEnreg) est remise à la date du jour.
Les rubriques de type Horodatage sont également modiées et correspondent à la date du jour, au
moment où l'optimisation est eectuée.
```
Remarques :

```
Mis à part l'option 2, toutes les modes d'optimisation entraînent le blocage des chiers de données
pendant l'optimisation. Les utilisateurs sont informés que le chier de données est en cours de
maintenance.
Lorsque la réindexation est eectuée, le contexte HFSQL en cours est rétabli (sauf si l'option de
compression des mémos a été choisie).
```
Comment le faire?

```
WINDEV Mobile Autres
```
### WDOptimizer : Optimiser les index

```
Disponible uniquement avec ces types de connexion
```

Optimiser les index d'un chier de données

Pour optimiser les index d'un chier de données :

1. Lancez WDOptimizer :
    Directement depuis WINDEV, WEBDEV ou WINDEV Mobile : sous le volet "Outils", dans le groupe "Base
    de données", cliquez sur "WDOptimizer".
    en lançant directement le programme "WDOptimizer.EXE".
2. Sélectionnez les chiers de données à traiter. Il est possible :
    soit de réaliser un "Drag and drop" des chiers de données depuis l'explorateur vers WDOptimizer. Les
    chiers droppés apparaissent automatiquement dans la liste.
    soit d'ajouter un ou plusieurs chiers grâce au bouton "Ajouter un chier".
    soit d'ajouter les chiers de données présents dans un répertoire grâce au bouton "Ajouter un
    dossier".
    Il est possible de traiter les sous-répertoires grâce à l'option "Lors de l'ajout d'un répertoire, inclure les
    chiers de tous les sous-répertoires".
3. Sélectionnez les chiers de données à traiter et indiquez si nécessaire le mot de passe de chaque chier
    de données.
    Remarque : Si le mot de passe est identique pour tous les chiers de données, cochez l'option "Le mot de
    passe est identique pour tous les chiers".
4. Cliquez sur le bouton "Optimiser les index" ou "Optimiser les index des chiers sélectionnés" et choisissez
    l'option voulue.

Un rapport est généré en cas de problème.

Options de ré-indexation

Présentation

Les options de ré-indexation apparaissent dans la partie basse de l'écran :


Mode avancé réindexation

Ces options sont prises en compte pour les ré-indexation de type 1 à 4 :
Supprimer les enregistrements inactifs (supprimés ou rayés)
Si cette option est sélectionnée, les enregistrements rayés sont dénitivement supprimés.
Rappel : Lorsqu'un enregistrement est rayé, il est supprimé logiquement et pourra éventuellement être
récupéré par la suite. L'enregistrement est encore présent dans le chier de données. La suppression des
enregistrements rayés supprime dénitivement ces enregistrements et permet ainsi d'optimiser la taille
du chier de données.
Supprimer les enregistrements endommagés
Si cette option est cochée, les enregistrements endommagés sont automatiquement supprimés.
Réindexer sans bloquer les postes clients
Si cette option est cochée, la ré-indexation est eectuée en tâche de fond et les applications clientes ne
seront pas arrêtées.
Attention : Cette option est prise en compte uniquement pour des chiers de données HFSQL
Client/Serveur.
Densité de l'index
Correspond au taux de remplissage des index. Par défaut, ce taux a pour valeur 80.
Plus ce taux est important, plus l'index est dense et de petite taille. Dans ce cas, les parcours, recherches,
ltres et requêtes sont plus rapides. Les ajouts d'enregistrements et les modications d'enregistrements
pourront être ralentis.
Plus ce taux est faible, moins l'index sera dense et plus sa taille sera importante. Dans ce cas, les parcours,
recherches, ltres et requêtes seront ralentis. Les ajouts d'enregistrements et les modications
d'enregistrements seront plus rapides.
Attention : ce paramètre est utilisable uniquement sur les chiers de données au format HFSQL Classic ou
Client/Serveur.
Alphabet
Par défaut, l'alphabet du chier de données est conservé. Mais il est possible d'eectuer une ré-indexation
en changeant l'alphabet du chier de données. Dans ce cas, le nouvel alphabet sera pris en compte lors de
la ré-indexation. Les tris, recherches, ... sur des clés de type chaîne (chaînes, caractères, date et heure)
seront eectuées selon cet alphabet.

Options de compression des mémos

Ces options sont prises en compte lors de la révision avec compression des index et des mémos (option 5) :


```
Conserver les enregistrements rayés
Si cette option est sélectionnée, les enregistrements rayés sont conservés. Dans le cas contraire, ils sont
dénitivement supprimés.
Essayer de récupérer les données du mémo s'il est endommagé
Si cette option est sélectionnée, WDOptimizer tente de récupérer le mémo. Dans le cas contraire, les
enregistrements endommagés sont récupérés sans le mémo associé.
Attention : La récupération du mémo peut être partielle. Vériez vos chiers de données.
```
Options

Ces options permettent de simplier la gestion de la liste de chiers à ré-indexer :
Le mot de passe est identique pour tous les chiers
Si cette option est sélectionnée, le même mot de passe est utilisé pour tous les chiers de données. Il
sut d'indiquer le mot de passe dans la colonne "Mot de passe" pour le premier chier de données de la
liste.
Si cette option est décochée, il est nécessaire d'indiquer le mot de passe dans la colonne "Mot de passe"
de la table pour chaque chier de données.
Lors de l'ajout d'un répertoire, inclure les chiers présents dans tous les sous-répertoires
Si cette option est sélectionnée, l'ajout des chiers de données présents dans les sous-répertoires est
automatique.

Droits d'accès au chier de données

L'optimisation provoque la recréation du chier de données sur disque.

Il convient de vérier les droits du chier optimisé. Ces droits peuvent être diérents de ceux du chier
d'origine. Il est alors nécessaire de les redénir au niveau de Windows après l'optimisation.


#### WINDEV

Présentation

WDOptimizer permet de :
Annuler une transaction.
Libérer des enregistrements d'une transaction.

Rappel : Une transaction permet de s'assurer que des mises à jours eectuées sur un ou plusieurs chiers de
données se sont déroulées correctement. En cas d'erreur ou de problème (panne de courant pendant les
opérations en transaction par exemple), WDOptimizer permet de rétablir automatiquement l'état des chiers
de données juste avant le début de la transaction.

Remarque : WDTrans permet également d'annuler une transaction et/ou libérer des enregistrements d'une
transaction.

Annuler les opérations eectuées sur un chier de transaction

Lors de l'annulation des opérations eectuées sur un chier de transaction :
Si une transaction est en cours, WDOptimizer annule toutes les opérations eectuées sur les chiers en
transaction depuis le début de la transaction. Dans ce cas, la transaction est annulée sans interrompre
l'exécution du programme.
Si aucune transaction n'est en cours, WDOptimizer rétablit la cohérence de la base de données et
annule la transaction qui a échoué (cas d'une coupure de courant par exemple).

Annuler les opérations eectuées sur un chier de transaction

Pour annuler les opérations eectuées sur un chier de transaction :

1. Lancez WDOptimizer.

```
WEBDEV WINDEV Mobile Autres
```
### WDOptimizer : Annulation /

### libération d'enregistrements en

### transaction

```
Disponible uniquement avec ce type de connexion
```

2. Sélectionnez l'option "Annuler une transaction ...", puis "Annuler les opérations eectuées sur un chier
    de transaction".
3. Sélectionnez le chier de transaction. La liste des chiers de données (avec leur chemin complet) en cours
    de transaction apparaît. Pour chaque chier, l'identiant du poste réalisant une opération en transaction
    est aché.
4. Si certains chiers de données sont protégés par un mot de passe, spéciez ce mot de passe. En eet, ce
    mot de passe est nécessaire pour annuler la transaction.
5. Cliquez sur le bouton "Annuler la transaction". La transaction est annulée.

Libérer des enregistrements d'une transaction

La libération des enregistrements d'une transaction permet de transformer tous les enregistrements "en
transaction" en enregistrements "Normaux" (si ces enregistrements n'appartiennent pas à une transaction
actuellement en cours). Si un enregistrement du chier de données spécié est considéré comme étant en
transaction, mais n'appartient à aucune transaction en cours, il est automatiquement libéré.

Attention : Cette fonctionnalité est une fonctionnalité avancée. Cette fonction doit être utilisée lorsqu'il est
impossible d'annuler les transactions qui ont échoué (chiers de transaction supprimés par exemple).

Libérer les enregistrements en transaction

Pour libérer les enregistrements en transaction :

1. Lancez WDOptimizer :
    Directement depuis WINDEV, WEBDEV ou WINDEV Mobile : sous le volet "Outils", dans le groupe "Base
    de données", cliquez sur "WDOptimizer".
    en lançant directement le programme "WDOptimizer.EXE".


2. Sélectionnez l'option "Annuler une transaction", puis "Libérer tous les enregistrements en transaction".
3. Sélectionnez le répertoire contenant les chiers de données en cours de transaction.
    Attention : Aucun chier de transaction ne doit être présent dans ce répertoire. La liste des chiers de
    données présents dans le répertoire apparaît.
    Remarque : Si des chiers de données se trouvent dans des sous-répertoires, cochez l'option "Inclure les
    chiers de tous les sous-répertoires".
4. Si certains chiers de données sont protégés par un mot de passe, spéciez ce mot de passe. En eet, ce
    mot de passe est nécessaire pour libérer les enregistrements en transaction.
5. Cliquez sur le bouton "Libérer tous les enregistrements en transaction". Les enregistrements sont libérés.


#### WINDEV WEBDEV

Syntaxe

Pour lancer WDOptimizer en ligne de commande, utilisez la syntaxe suivante

WDOptimizer /Fic=<Répertoire>
/Mdp=<Mot de passe>
/Option=<Type d'action réalisée>
/Log=<Fichier Log>
/Muet=<Oui/Non>
/ExploreSousRep=<Oui/Non>
/CompactageIndex=<Oui/Non>
/SupprIndex=<Oui/Non>
/RecupMemos=<Oui/Non>
/ConserveRaye=<Oui/Non>
/Alphabet=<Alphabet>
/Densite=<Taux de densité>
/Langue=<Langue d'achage>
/Sauve=<Oui/Non>

Le tableau ci-dessous liste les diérents éléments pouvant être présents sur la ligne de commande :

```
Paramètre Signication
```
```
/Fic=<Répertoire> Pour traiter un seul chier de données : chemin complet du chier de
données à traiter.
Pour traiter un ensemble de chiers de données :
chemin d'un répertoire,
Fichier INI au format d'export généré par WDOptimizer.
```
```
Pour traiter des transactions : chemin complet du chier de transaction.
Exemple : c:\temp\chier.c
```
```
/Mdp=<Mot de passe> Mot de passe associé au chier de données à traiter (traitement d'un seul
chier de données)
```
```
WINDEV Mobile Autres
```
### Lancer WDOptimizer en ligne de

### commande

```
Disponible uniquement avec ce type de connexion
```

/Option=<Type d'action à
réaliser>

```
Numéro correspondant à l'option de WDOptimizer à lancer :
1 : Vérication de l'index.
2 : Optimiser la vitesse des index (Recalculer les statistiques sur les
chiers de données).
3 : Reconstruire les index.
4 : Reconstruire les index et les mémos.
5 : Réviser et compresser les index et les mémos.
```
/Log=<Fichier Log> Chemin complet du chier journal (.log) à créer. Ce chier n'est créé que si
une des options 1 à 5 est sélectionnée.

/Muet=<Oui/Non> Oui permet de valider automatiquement la fenêtre de compte-rendu (Non
par défaut).

/ExploreSousRep=<Oui/Non> Oui permet d'explorer les sous-répertoires du répertoire spécié dans le
paramètre "/Fic" (Non par défaut).

/CompactageIndex=
<Oui/Non>

```
Oui permet de supprimer les enregistrements inactifs lors d'une ré-
indexation (options 3 et 4) (Non par défaut).
```
/SupprIndex=<Oui/Non> Oui permet de supprimer les enregistrements endommagés (options 3 et
4) (Non par défaut).

/RecupMemos=<Oui/Non> Oui permet d'essayer de récupérer les données du mémo s'il est
endommagé (option 5) (Non par défaut).

/ConserveRaye=<Oui/Non> Oui permet de conserver les enregistrements rayés (option 5) (Non par
défaut).

/Alphabet=<Alphabet> Permet de préciser l'alphabet utilisé pour la réindexation. Il est possible
d'utiliser une des constantes correspondant à l'alphabet à utiliser.

```
alphabetArabe Caractères arabes
```
```
alphabetBalte Caractères baltes
```
```
alphabetChinois Caractères chinois (République Populaire
de Chine)
```
```
alphabetChinoisTraditionnel Caractères chinois traditionnel
(République de Taïwan)
```
```
alphabetCoréen Caractères coréens
```
```
alphabetDéfaut Utilise l'alphabet par défaut du poste.
Aucun alphabet n'est forcé.
```

```
alphabetEuropeEst Caractères d'Europe de l'est (polonais, ...)
```
```
alphabetGrec Caractères grecs
```
```
alphabetHébreu Caractères hébreux
```
```
alphabetJaponais Caractères japonais
```
```
alphabetOccidental Caractères romains à la norme ANSI
```
```
alphabetRusse Caractères russes
```
```
alphabetThaï Caractères thaï
```
```
alphabetTurc Caractères turques
```
```
alphabetUTF8 Permet de gérer les pays pouvant utiliser
deux alphabets (Hong Kong) et les pays
n'ayant pas d'alphabet déni dans
Windows (Géorgien et Arménien).
```
```
alphabetVietnamien Caractères vietnamiens
```
```
/Densite=<Taux de densité> Taux de remplissage des index. Par défaut, ce taux a pour valeur 80.
Plus ce taux est important, plus l'index est dense et de petite taille. Dans
ce cas, les parcours, recherches, ltres et requêtes seront plus rapides.
Les ajouts d'enregistrements et les modications d'enregistrements
pourront être ralentis.
Plus ce taux est faible, moins l'index sera dense et plus sa taille sera
importante. Dans ce cas, les parcours, recherches, ltres et requêtes
seront ralentis. Les ajouts d'enregistrements et les modications
d'enregistrements seront plus rapides.
```
```
/Langue=<Langue
d'achage>
```
```
"US" permet de faire fonctionner WDOptimizer en Anglais (Français par
défaut).
```
```
/Sauve=<Non> Par défaut, les chiers à traiter sont sauvegardés (uniquement pris en
compte si /option = 5). Non permet de ne pas faire cette sauvegarde.
```
Exemples

La ligne de commande suivante permet de lancer la ré-indexation des chiers présent dans le répertoire
"C:\MonAppli\Données".

## LanceAppli("C:\MonRépertoire\WDOptimizer.EXE /Fic=C:\MonAppli\Données")


Exemple de procédure de re-indexation


## // Variables globales du projet

# gsNomAppli est une chaîne = "MonAppli"

# gsRepData est une chaîne = ComplèteRep(fRepExe()) + "Data\"


## //Procédure globale au projet

# PROCÉDURE gWdOptimiseAnalyse(_NumOption = 5 ,_bSauvegarde = Faux )

## // Pilotage de WDOPTIMIZER pour tous les fichiers d'une appli

## // avec prise en compte de mot de passe, ExeActif et

## // WDOptimizer bloquant quand il s'exécute.

## // Après chaque réindexation, WDOptimizer affiche le message

## // "La réindexation du fichier 'C:\.....\MonFic.Fic' s'est déroulée correctement".

## // L'utilisateur doit cliquer sur "Ok".

## // Par défaut l'option 5 de WDOptimizer est utilisée

## // Par défaut les fichiers ne sont pas sauvegardés avant optimisation

## // - Requis :

## // - Les fichiers de données peuvent être délocalisés par rapport à l'exe

## // (Variables globales gsNomAppli et gsRepData)

## // - WDOptimizer est toujours à côté de l'exécutable

## // - Les fichiers peuvent avoir un nom physique différent du nom logique

## // ainsi qu'une extension <> ".FIC"

## // Variables locales au traitement

# sListFichier, sNomFichier sont des chaînes

# sSauvegarde est une chaîne = "Faux"

# SI _bSauvegarde = Vrai ALORS sSauvegarde = "Vrai"

# i est un entier = 1

# sRep est une chaîne = ComplèteRep(fRepExe())

# // Nom physique du fichier (nom + extension)

# sNomPhysFichier est une chaîne

## // Mot de passe du fichier

# sMdp est une chaîne

# sLigneCommande est une chaîne

## // Vérification de la présence de WDOptimizer

# SI fRep(sRep + "WDOptimizer.EXE", frFichier ) = "" _OU_ ...

# fRep(sRep + "WDOutil.WDK", frFichier ) = "" ALORS

## Erreur("L'outil WDOptimizer n'a pas été correctement installé")

## RETOUR

## FIN

## // Liste des fichiers de l'analyse

# sListFichier = HListeFichier()

# sNomFichier = ExtraitChaîne(sListFichier, i, RC )

# TANTQUE sNomFichier <> EOT

# sNomPhysFichier = {sNomFichier}..NomPhysique + {sNomFichier}..Extension

# SI fRep(gsRepData + sNomPhysFichier, frFichier ) <> "" ALORS


## // Prise en compte des mots de passe de certains fichiers protégés

# SELON Majuscule(sNomFichier)

# CAS "TOTO" : sMdp = "toto"

# AUTRE CAS : sMdp = ""

## FIN

# SI sMdp <> "" ALORS

# sLigneCommande =

# sRep + "WDOptimizer.EXE /Fic=" + ...

# gsRepData + sNomPhysFichier + " /mdp=" + sMdp + " /" + ...

# _NumOption + " /" + sSauvegarde

## SINON

# sLigneCommande = sRep + "WDOptimizer.EXE /Fic=" + ...

# gsRepData + sNomPhysFichier + " /5 /" + sSauvegarde

## FIN

# LanceAppli(sLigneCommande, exeActif , exeBloquant )

## FIN

## i++

# sNomFichier = ExtraitChaîne(sListFichier, i, RC )

## FIN

# Info("Optimisation des fichiers de '" + gsNomAppli + "' terminée")


#### WINDEV WEBDEV

Présentation

Le chier <MonProjet>.REP est un chier contenant la liste des chiers manipulés par l'application (identiant,
nom logique et chemin complet du chier physique).

Le GUID de l'analyse est l'identiant unique de l'analyse liée au projet, contenant la description des chiers.
Cet identiant peut être connu sous l'éditeur d'analyses, dans la description du de l'analyse (onglet
"Options").

Le GUID du chier correspond à l'identiant du chier logique. Cet identiant peut être connu sous l'éditeur
d'analyses, dans la description du chier (onglet "Notes").

Ce chier est automatiquement créé dans le répertoire de l'application et renseigné par le moteur HFSQL.

Le chier .REP

A quoi sert le chier .REP?

Le chier .REP permet de localiser facilement les chiers de données qui ont été utilisés par l'application
WINDEV ou le site WEBDEV.

L'application WINDEV ou le site WEBDEV met à jour automatiquement le chier .REP mais ne se sert pas (ou
rarement) du chier .REP.

Ce chier est utilisé par tous les outils devant manipuler les chiers de l'application, et principalement par la
mise à jour automatique des chiers, etc.

Exemple : Mise à jour d'une application avec modication de l'analyse

Lors de la mise à jour d'une application WINDEV, la modication automatique des chiers de données est
automatiquement lancée en cas de modications sur la structure de la base de données.

Cette procédure utilise le chier .REP pour retrouver les chiers physiques utilisés par l'application an de les
modier.

Éditer et modier un chier .REP

```
WINDEV Mobile Autres
```
### WDOptimizer : Édition et

### modication d'un chier ".REP"

```
Disponible uniquement avec ce type de connexion
```

Editer et modier un chier .REP

Pour éditer et modier un chier .REP :

1. Lancez WDOptimizer :
    Directement depuis WINDEV, WEBDEV ou WINDEV Mobile : sous le volet "Outils", dans le groupe "Base
    de données", cliquez sur "WDOptimizer".
    en lançant directement le programme "WDOptimizer.EXE".
2. Sélectionnez l'option "Éditer et modier un chier .REP".
3. Sélectionnez le chier .REP. Les chiers contenus dans le chier .REP sélectionné sont listés.
4. Pour supprimer l'ensemble des chiers qui n'existent pas, cliquez sur le bouton "Nettoyer".
5. Pour supprimer le chier sélectionné, cliquez sur le bouton "Supprimer".


