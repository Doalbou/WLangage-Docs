## WEBDEV

Présentation

WDStatistics est un utilitaire permettant d'eectuer des statistiques de fréquentation de vos sites WEBDEV
dynamiques (classiques et AWP) et des Webservices déployés sur un Serveur d'Application WEBDEV.

Ces statistiques sont réalisées à partir de chiers journal (extension ".LOG") générés par le Serveur
d'Application WEBDEV. Ces chiers peuvent être enregistrés pour l'ensemble des sites ou pour un site
spécique.

Quelques exemples des statistiques automatiquement réalisées par WDStatistics :

```
Liste des connexions : détail de toutes les connexions eectuées sur le serveur Web (adresse IP, date et
heure, navigateur utilisé, système d'exploitation, etc.).
Connexions par site : nombre de connexions par site WEBDEV et durée de connexion.
Liste des pages visitées par un internaute.
Nombre de connexions réalisées pour un type de navigateur (Google Chrome, etc.).
Nombre de connexions réalisées par plage horaire.
Nombre de connexions réalisées par système d'exploitation.
Liste des sites sur lesquels les internautes se trouvaient avant d'arriver sur votre site.
Liste des mot-clés utilisés sur les moteurs de recherche permettant d'arriver sur votre site.
Statistiques sur l'origine géographique des visiteurs (par pays).
```
Ces diérentes statistiques sont présentées sous forme de :

```
Tableau récapitulatif. Ces tableaux peuvent être enregistrés au format Word, Excel ou XML (clic droit sur le
tableau).
Graphique. Ces graphiques peuvent être personnalisés (clic droit sur le graphique). Il est ainsi possible de
changer le type de graphe, d'ajouter des légendes, de modier la police utilisée, etc.
Rapport imprimable. Il est possible de choisir le type de rapport à imprimer ainsi que la période voulue.
Ces rapports peuvent être imprimés, enregistrés au format PDF, envoyés par email, etc.
```
```
WINDEV WINDEV Mobile Autres
```
# WDStatistics : Présentation


WDStatistics peut être lancé directement en double-cliquant sur le programme "WDStatistics.EXE".

WDStatistics est un outil non redistribuable. WDStatistics ne peut pas être installé sur le serveur Web où
votre site est déployé.

Pour utiliser WDStatistics, WEBDEV version Développement doit obligatoirement être installé sur le poste en
cours.

Remarque : L'outil WDStatistics est également disponible en ligne, à partir de l'administrateur distant. Pour
plus de détails, consultez Visualiser les statistiques dans l'administrateur distant.

```
Avertissement
En version 28, cet outil avait pour nom "WDStatistique".
```
Utilisation de WDStatistics

Pour connaître les statistiques de fréquentation de vos sites dynamiques, il sut de :

1. Congurer l'administrateur WEBDEV an de générer le(s) chiers journal(aux) (extension ".LOG").
2. Importer le(s) chier(s) journal(aux) dans WDStatistics.
3. Utiliser WDStatistics.

Fichier journal

Les statistiques de fréquentation de vos sites dynamiques sont calculées à partir de chiers de type journal
(extension ".LOG"). Ces chiers sont générés par le moteur WEBDEV.

Il est possible de créer ce type de chier :

```
Soit pour chacun des sites WEBDEV dynamiques installés sur le serveur Web. Dans ce cas, un seul
chier journal sera créé par jour dans un répertoire spécique à chaque site. Ce chier contiendra
l'historique des manipulations eectuées uniquement dans le site WEBDEV dynamique concerné.
Soit pour l'ensemble des sites WEBDEV dynamiques installés sur le serveur Web. Dans ce cas, un seul
chier journal sera créé par jour dans un répertoire commun. Ce chier contiendra l'historique des
manipulations eectuées dans l'ensemble des sites WEBDEV dynamiques installés sur le serveur Web.
```
Ces chiers de type journal sont enregistrés en continu dès que le(s) site(s)associé(s) au chier sont utilisés.

Le format du nom de ces chiers de type journal est le suivant : "WDSession_<AnnéeEnregistrement>
<MoisEnregistrement><JourEnregistrement>"

Fichiers de données

Les chiers de données de WDStatistics sont présents dans le répertoire "C:\Documents and
Settings\Utilisateur\Application Data\PC SOFT\WDStatistics\". Il est possible de transférer ces chiers d'un
poste à un autre.



## WEBDEV

Présentation

Après avoir importé les chiers journal, l'utilisation de WDStatistics peut commencer.

La fenêtre principale de WDStatistics est la suivante :

```
WINDEV WINDEV Mobile Autres
```
# WDStatistics : Utiliser WDStatistics


```
Paramètres des données à acher.
Sélectionnez les diérents paramètres concernant les statistiques à acher : Nom du
serveur, nom du site, période, etc.
```
```
Types de statistiques à acher
Cliquez sur le type de statistiques à acher.
```
```
Statistiques demandées.
Ces diérentes statistiques sont présentées sous forme de :
tableaux récapitulatifs.
Ces tableaux peuvent être enregistrés au format Word, Excel ou XML (clic droit sur
le tableau).
graphiques. Ces graphiques peuvent être personnalisés (clic droit sur le
graphique). Il est ainsi possible de changer le type de graphe, d'ajouter des
légendes, de modier la police utilisée, etc.
```
Les statistiques disponibles

Les statistiques proposées par WDStatistics sont les suivantes :

```
Tableau de bord : Tableau de bord récapitulant :
le nombre de visiteurs.
le nombre de pages vues.
le nombre de pages moyen par visiteur.
le nombre moyen de visiteurs par jour.
le nombre moyen de pages vues par jour.
le nombre maximum de connexions.
le nombre minimum de connexions.
la date de dernière importation des chiers journal.
le fuseau horaire du site.
le type de site (Classique ou AWP).
```
```
Moteurs de recherche : Liste des mot-clés utilisés sur les moteurs de recherche
permettant d'arriver sur le site.
```
```
Répartition : Liste des systèmes d'exploitation des internautes et des
navigateurs.
```

Fréquentation : Graphe récapitulant le nombre de visites selon diérentes
répartitions temporelles.

Vue Géographique : Répartition de chaque visiteur selon le pays.

Parcours des visiteurs : Parcours eectués pour chaque visiteur sur le site (temps
de parcours et durée passée sur chaque page).


## WEBDEV

Présentation

Pour créer les chiers journal nécessaires aux calculs des statistiques de fréquentation de vos sites, un
paramétrage spécique est nécessaire dans l'administrateur WEBDEV.

Ce paramétrage peut être réalisé :

```
soit depuis l'administrateur WEBDEV Distant accessible directement depuis le poste en cours (conseillé).
soit depuis l'administrateur WEBDEV installé chez votre hébergeur (livré avec le serveur d'application
WEBDEV).
```
Conguration de l'administrateur WEBDEV Distant

Pour créer les chiers journal pour chacun des sites WEBDEV dynamiques installés sur le serveur Web :

1. Achez la page générale de l'administrateur WEBDEV Distant.
    Rappel : L'administrateur WEBDEV Distant peut être lancé à partir de n'importe quel poste possédant un
    navigateur Internet. Il sut d'utiliser l'adresse suivante :
    [http://<ServeurWeb>/WDAdminWeb](http://<ServeurWeb>/WDAdminWeb)
2. Sélectionnez le site WEBDEV voulu.
3. Cochez l'option "Générer le chier journal".
4. Spéciez le répertoire dans lequel les chiers journal doivent être créés.

Remarque : L'administrateur WEBDEV Distant ne permet pas de congurer la création d'un chier journal
commun pour l'ensemble des sites WEBDEV dynamiques installés sur le serveur Web.

Conguration de l'administrateur WEBDEV (Serveur d'application
WEBDEV)

Créer les chiers journal pour chacun des sites WEBDEV dynamiques installés sur le serveur Web

Pour créer les chiers journal pour chacun des sites WEBDEV dynamiques installés sur le serveur Web :

1. Achez l'onglet "Sites" de l'administrateur WEBDEV (version utilisée sur le serveur d'application).
2. Sélectionnez le site WEBDEV voulu.
3. Cochez l'option "Paramètres personnalisés".

```
WINDEV WINDEV Mobile Autres
```
# WDStatistics : Conguration de

# l'administrateur WEBDEV


4. Cochez l'option "Générer un chier journal particulier à ce site pour les statistiques de fréquentation
    (.log)".
5. Spéciez le répertoire dans lequel les chiers journal doivent être créés.
6. Cliquez sur le bouton "Appliquer".
7. Recommencez ces opérations pour chacun de vos sites (si nécessaire).

Créer les chiers journal commun pour l'ensemble des sites WEBDEV dynamiques installés sur le
serveur Web

Pour créer les chiers journal commun pour l'ensemble des sites WEBDEV dynamiques installés sur le serveur
Web :

1. Achez l'onglet "Conguration" de l'administrateur WEBDEV (version utilisée avec le serveur
    d'application).
2. Cochez l'option "Générer un chier journal pour les statistiques de fréquentation (.log)".
3. Spéciez le répertoire dans lequel les chiers journal doivent être créés.
4. Cliquez sur le bouton "Appliquer".


## WEBDEV

Présentation

Pour visualiser les statistiques de fréquentation de vos sites grâce à WDStatistics, il est nécessaire d'importer
les chiers journal sur le poste en cours.

Cette importation peut être :

```
manuelle :
Cette importation est conseillée :
pour visualiser occasionnellement les statistiques de fréquentation de vos sites.
quand le répertoire contenant les chiers journal est directement accessible depuis le poste en cours
(site Intranet par exemple).
automatique :
Cette importation est conseillée pour réaliser un suivi régulier de la fréquentation de vos sites.
```
Avant de lancer une importation de chiers journal, il est nécessaire de congurer les informations sur le site
dont on souhaite obtenir les statistiques.
Pour congurer un site, il sut de lancer WDStatistics et de cliquer sur le bouton "Gestion des sites".

Importation manuelle des chiers journal

Pour importer manuellement un chier journal :

1. Lancez WDStatistics (double-cliquez sur le programme "WDStatistics.EXE").
2. Congurez la manière d'importer les chiers journal en cliquant sur le bouton "Gestion des sites" (via
    WebDep, FTP ou directement un chemin).
3. Cliquez sur le bouton "Importation". La fenêtre permettant de paramétrer l'importation s'ache.
4. Sélectionnez le site dont il faut importer les chiers journal.
5. Saisissez la date à partir de laquelle vous souhaitez importer les chiers journal.
6. Cliquez sur le bouton "Lancer maintenant une importation".
7. WDStatistics ache les statistiques concernant le (ou les) chier(s) journal importé(s).

Importation automatique des chiers journal

Congurer l'importation automatique de chiers journal

```
WINDEV WINDEV Mobile Autres
```
# WDStatistics : Importation des

# chiers journal


Pour congurer l'importation automatique de chiers journal :

1. Lancez WDStatistics (double-cliquez sur le programme "WDStatistics.EXE").
2. Cliquez sur le bouton "Importation". La fenêtre de paramétrage de l'importation s'ache.
3. Sélectionnez le site dont vous souhaitez automatiser l'importation des chiers journal.
4. Cochez la case "Planier l'importation des logs".
5. Sélectionnez la fréquentation d'importation (occasionnelle, journalière, hebdomadaire ou mensuelle).
6. Spéciez les informations de lancement (date et heure).
7. Valider la fenêtre.

Remarque importante

L'importation automatique des chiers journal s'appuie sur le mécanisme des tâches planiées de Microsoft
Windows.
Il est donc très important de renseigner correctement les informations concernant l'utilisateur Windows de la
machine et le mot de passe associé au compte.
Sans ces informations, il est impossible de planier automatiquement l'importation des chiers journal.


