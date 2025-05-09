### WINDEV WEBDEV

## Présentation

L'utilitaire WDTrans

WDTrans est un utilitaire d'annulation de transactions.

Rappel : Une transaction permet de s'assurer que des mises à jours eectuées sur un ou plusieurs chiers
de données se sont déroulées correctement. En cas d'erreur ou de problème (panne de courant pendant les
opérations en transaction par exemple), WDTrans permet de rétablir automatiquement l'état des chiers de
données juste avant le début de la transaction.
Pour plus de détails sur les transactions, consultez la gestion des transactions.

Les opérations pouvant être réalisées avec WDTrans :

```
Annuler les opérations eectuées sur un chier de transaction
Si une transaction est en cours, cette option annule toutes les opérations eectuées sur les chiers en
transaction depuis le début de la transaction. Dans ce cas, la transaction est annulée sans interrompre
l'exécution du programme.
Si aucune transaction n'est en cours, cette option rétablit la cohérence de la base de données et annule
la transaction qui a échoué (cas d'une coupure de courant par exemple).
Libérer les enregistrements en transaction
Cette option transforme tous les enregistrements "en transaction" en enregistrements "normaux" si ces
enregistrements n'appartiennent pas à une transaction actuellement en cours. Si un enregistrement du
chier de données spécié est considéré comme étant en transaction, mais n'appartient à aucune
transaction en cours, il est automatiquement libéré.
Attention : Cette fonctionnalité est une fonctionnalité avancée. Cette fonctionnalité doit être utilisée
lorsqu'il est impossible d'annuler les transactions qui ont échoué (chiers de transaction supprimés par
exemple).
```
## Utilisation

Lancement de WDTrans

Quel que soit son mode de lancement (interactif ou en ligne de commande), l'interface de WDTrans apparaît.

```
WINDEV Mobile Autres
```
# WDTrans : Présentation

```
Disponible uniquement avec ces types de connexion
```

Pour lancer WDTrans en mode interactif, il sut de lancer directement le programme "WDTrans.EXE".

Remarque : L'annulation d'opérations eectuées sur un chier de transaction peut être eectuée en ligne de
commande. Pour plus de détails, consultez Annuler les opérations eectuées sur un chier de transaction.

Conditions d'utilisation

WDTrans est un outil redistribuable. WDTrans peut être installé avec les applications développées avec
WINDEV. La licence d'utilisation de WINDEV s'applique intégralement.

Lors de la création de la procédure d'installation, WDTrans peut être livré avec vos applications.

Rappel : La procédure d'installation peut être créée :

```
soit à partir de l'assistant : sous le volet "Projet", dans le groupe "Génération", déroulez "Procédure
d'installation" et sélectionnez "Créer la procédure d'installation".
soit à partir de l'éditeur d'installation : sous le volet "Outils", dans le groupe "Installation", cliquez sur
"WDInst".
```
Installation de WDTrans

Les chiers nécessaires à l'installation de WDTrans sont les suivants :

```
WDTrans.EXE wd300etat.dll
```
```
wd300hf.dll wd300html.dll
```
```
wd300obj.dll wd300pnt.dll
```
```
wd300prn.dll wd300rtf.dll
```
```
wd300std.dll wd300sql.dll
```
```
wd300trs.dll wd300vm.dll
```
```
wd300xml.dll WDOutil.WDK
```
```
WDTrans_FR.PDF WDTrans_EN.PDF
```

### WINDEV

## Présentation

Le fonctionnement de WDtrans est le suivant :
Si aucune transaction n'est en cours, rétablit la cohérence de la base de données et annule la
transaction qui a échoué (cas d'une coupure de courant par exemple).
Si une transaction est en cours, annule toutes les opérations eectuées sur les chiers en transaction
depuis le début de la transaction. Dans ce cas, la transaction est annulée sans interrompre l'exécution du
programme.

## Comment le faire?

Annuler les opérations eectuées sur un chier de transaction

Pour annuler les opérations eectuées sur un chier de transaction :

1. Lancez WDTrans.
2. Sélectionnez l'option "Annuler une transaction".
3. Sélectionnez le chier de transaction à l'aide du sélecteur de chiers.
    La liste des chiers de données (avec leur chemin complet) en cours de transaction apparaît. Pour chaque
    chier, l'identiant du poste réalisant une opération en transaction est aché.
4. Si certains chiers de données sont protégés par un mot de passe, spéciez ce mot de passe. En eet, ce
    mot de passe est nécessaire pour annuler la transaction.
5. Si nécessaire, débranchez la gestion des doublons et/ou de l'intégrité.
6. Cliquez sur le bouton "Annuler la transaction". La transaction est annulée.

Pour annuler les opérations eectuées sur un chier de transaction en mode ligne de commande :

WDTrans /Fic = <Fichier>
/Mdp = <Mot de passe>
/Option = <Type d'action réalisée>
/Log = <Fichier Log>

```
WEBDEV WINDEV Mobile Autres
```
# WDTrans : Annuler les opérations

# eectuées sur un chier de

# transaction

```
Disponible uniquement avec ces types de connexion
```

Le tableau ci-dessous liste les diérents éléments pouvant être présents sur la ligne de commande :

```
Paramètre Signication
```
```
/Fic = <Fichier> Chemin complet du chier de transaction (chier .TRS)
```
```
/Mdp = <Mot de passe> Mot de passe associé au chier à traiter (traitement d'un seul chier)
```
```
/Option = <Type d'action à
réaliser>
```
```
Option de WDTrans à lancer. Pour annuler les opérations eectuées
sur un chier de transaction, cette option correspond à 6.
```
```
/Log = <Fichier Log> Chemin complet du chier journal (.LOG) à créer.
```
Exemple : Annuler les transactions enregistrées dans le chier "WD Transactions.TRS" :
WDTRANS.EXE /Fic="C:\Temp\WD Transaction.TRS" /option=


### WINDEV WEBDEV

## Présentation

Transforme tous les enregistrements "en transaction" en enregistrements "normaux" si ces enregistrements
n'appartiennent pas à une transaction actuellement en cours. Si un enregistrement du chier de données
spécié est considéré comme étant en transaction, mais n'appartient à aucune transaction en cours, il est
automatiquement libéré.

Attention : Cette fonctionnalité est une fonctionnalité avancée. Cette fonctionnalité doit être utilisée
lorsqu'il est impossible d'annuler les transactions qui ont échoué (chiers de transaction supprimés
par exemple).

## Comment le faire?

Libérer les enregistrements en transaction

Pour libérer les enregistrements en transaction :

1. Lancez WDTrans.
2. Sélectionnez l'option "Libérer des enregistrements en transaction".
3. Sélectionnez le répertoire contenant les chiers de données en cours de transaction. La liste des chiers
    de données présents dans le répertoire apparaît.
    Attention : Aucun chier de transaction ne doit être présent dans ce répertoire.
    Remarque : Si des chiers de données se trouvent dans des sous-répertoires, cochez l'option "Lors de
    l'ajout d'un répertoire, inclure les chiers de tous les sous-répertoires".
4. Si certains chiers de données sont protégés par un mot de passe, spéciez ce mot de passe. En eet, ce
    mot de passe est nécessaire pour libérer les enregistrements en transaction.
5. Cliquez sur le bouton "Libérer tous les enregistrements en transaction". Les enregistrements sont libérés.

Libérer les enregistrements en transaction en mode ligne de commande

Pour libérer les enregistrements en transaction en mode ligne de commande :
WDTrans /Fic = <Répertoire>
/Mdp = <Mot de passe>
/Option = <Type d'action réalisée>

```
WINDEV Mobile Autres
```
# WDTrans : Libérer les

# enregistrements en transaction

```
Disponible uniquement avec ces types de connexion
```

/Log = <Fichier Log>
/ExploresousRep = <Oui/Non>

Le tableau ci-dessous liste les diérents éléments pouvant être présents sur la ligne de commande :

```
Paramètre Signication
```
```
/Fic = <Répertoire> Répertoire contenant les chiers avec des enregistrements à libérer
```
```
/Mdp = <Mot de passe> Mot de passe des chiers. Ce même mot de passe est utilisé pour tous
les chiers.
```
```
/Option = <Type d'action à
réaliser>
```
```
Option de WDTrans à lancer. Pour libérer les enregistrements en
transaction, cette option correspond à 7.
```
```
/Log = <Fichier Log> Chemin complet du chier journal (.log) à créer.
```
```
/ExploresousRep = <Oui/Non> Oui permet d'explorer les sous-répertoires du répertoire spécié dans le
paramètre "/Fic" (Non par défaut).
```
Remarque : Pour utiliser un mot de passe diérent par chier, il est conseillé d'utiliser directement les
fonctions WLangage de gestion des transactions.

Exemple : Libérer les enregistrements en transaction situés dans le répertoire "WD Transaction" :

WDTRANS.EXE /Fic="C:\Temp\WD Transaction" /option=


