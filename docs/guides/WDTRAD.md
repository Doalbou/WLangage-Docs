## WINDEV WEBDEV

Présentation

WDTRAD est un outil de saisie de traduction des messages associés à une application WINDEV, WEBDEV ou
WINDEV Mobile. Ces messages ont été extraits avec WDMSG ou WDINT.

WDTRAD facilite le travail de saisie de la traduction des messages et limite les risques d'erreurs de traduction.

WDTRAD permet de :

```
visualiser le texte à traduire et de saisir sa traduction.
visualiser les langues 2 à 2 (origine et traduction) même si le chier à traduire (format WDMSG ou HFSQL)
contient plus de 2 langues.
Remarque : Il est également possible d'acher une langue d'origine supplémentaire pour s'assurer des
tournures ou du genre des expressions.
choisir la langue d'origine et la langue de traduction (notamment si le chier à traduire (format WDMSG ou
HFSQL) contient plus de 2 langues).
visualiser dans WINDEV, WEBDEV ou WINDEV Mobile, l'élément correspondant aux textes à traduire
(fenêtre et page uniquement).
proposer une traduction automatique.
traduire automatiquement tous les mots ou expressions identiques (soit dans l'ensemble du chier, soit
uniquement dans les lignes achées).
vérier l'homogénéité des traductions en visualisant l'ensemble du texte initial et du texte traduit.
éviter toute erreur de manipulation en ne travaillant pas directement sur le chier des messages à
traduire.
visualiser en temps réel l'avancement de la traduction et le nombre de lignes restant à traduire.
visualiser directement le nombre de mots ou de caractères alphanumériques à traduire.
Cette option permet d'évaluer le coût de traduction par une société de traduction : la traduction est
généralement facturée en fonction du nombre de mots ou de caractères à traduire.
trier les chaînes à traduire par langue d'origine et par langue de traduction.
trier les chaînes à traduire selon leur type.
visualiser l'interface de l'élément en cours de traduction (option disponible uniquement pour les chiers
d'extraction au format HFSQL et WDMSG).
eectuer un "Rechercher / Remplacer" parmi les ressources à traduire et traduites.
eectuer une recherche sur les ruptures en mode d'achage hiérarchique grâce à une icône "Loupe".
```
```
WINDEV Mobile Autres
```
# WDTRAD


```
gérer des "bookmarks" : Il est possible de mettre une ou plusieurs marques dans le chier en cours de
traduction (matérialisée par un bandeau coloré). Ces marques peuvent par exemple servir à indiquer une
ressource à revoir, le point d'arrêt de la traduction en cours, ...
Pour mettre une marque, utilisez le raccourci Ctrl F7.
Pour se déplacer entre les marques, utilisez la touche F7.
Il est également possible de créer ses propres étiquettes de bookmark (voir ci-dessous).
```
En cas de traduction par une société extérieure, WDTRAD peut être livré à cette société avec le chier des
messages à traduire (chier texte, chier de données HFSQL ou chier WDMSG). Dans ce cas, vous devez
également fournir des chiers nécessaires à l'utilisation de WDTRAD (voir Installer WDTRAD).

Pour plus de détails sur l'utilisation de WDTRAD, consultez Traduire un chier de messages avec WDTRAD.

Remarques :

```
Il est possible de changer la langue de l'interface de WDTRAD (option "? .. Langue").
Seuls les chiers extraits avec WDMSG et/ou WDINT peuvent être manipulés avec WDTRAD.
WDTRAD permet de saisir les traductions en utilisant des alphabets non latins.
```

Gestion des langues :

```
WDTRAD permet de gérer la traduction de messages dans 41 langues diérentes.
WDTRAD permet de gérer les langues personnalisées utilisées dans les projets WINDEV, WEBDEV ou
WINDEV Mobile. Il sut de sélectionner la langue de traduction "Langue personnalisée" pour
congurer les paramètres de cette langue.
Si le nom des langues personnalisées a été modié dans le projet WINDEV, WEBDEV ou WINDEV
Mobile, le nom de cette langue apparaît automatiquement dans la liste des langues. Les paramètres de
cette langue décrits dans WINDEV, WEBDEV ou WINDEV Mobile sont automatiquement pris en compte.
```
Gestion des dictionnaires :

```
WDTRAD est livré avec un dictionnaire français - anglais contenant la traduction de plus de 6000
messages. Ce dictionnaire peut être enrichi grâce à WDTRAD. Ce dictionnaire peut également être
utilisé avec WDDIXIO. Pour plus de détails sur WDDIXIO, consultez l'aide en ligne (mot-clé : WDDIXIO")
ou le chier d'aide "WDDIXIO.chm".
Un dictionnaire peut contenir les traductions d'une même ressource en plusieurs langues. Par
exemple, dans le même dictionnaire, l'expression "Fermer l'application" peut être traduite en anglais,
en espagnol et en allemand.
WDTRAD permet d'utiliser un dictionnaire situé sur une plateforme de développement PCSCloud
(option "Edition .. Localiser le dictionnaire .. Dictionnaire en mode cloud").
Remarque : A la première connexion à un dictionnaire PCSCloud, si ce dictionnaire est vide, l'import
d'un dictionnaire local est automatiquement proposé.
WDTRAD permet d'importer et/ou d'exporter un dictionnaire. Pour plus de détails, consultez
Importer/Exporter un dictionnaire.
WDTRAD permet de gérer des dictionnaires Web (Google et DeepL). Le choix du ou des dictionnaires
Web à utiliser est réalisé dans les options de WDTRAD.
WDTRAD permet d'ajouter une ressource dans le dictionnaire même si aucun chier de traduction
n'est ouvert (option "Ajouter une entrée dans le dictionnaire").
```
Gestion des étiquettes de bookmark :
Pour gérer des étiquettes de bookmark :

1. Pour marquer une ligne, achez le menu contextuel de la ligne et sélectionnez l'option "Bookmark ..
    Appliquer une étiquette" et sélectionnez l'étiquette voulue. Si aucune étiquette n'est proposée, vous
    pouvez en créer grâce à l'option "Gérer les étiquettes". Cette option permet de créer, modier et
    supprimer les étiquettes.
    Remarque : Le création, modication et suppression des étiquettes peut également être réalisée
    depuis les options de WDTRAD.
2. Pour ltrer les ressources selon une étiquette, cliquez sur l'étiquette apparaissant dans la colonne
    "Type" : un menu apparaît permettant de ltrer sur l'étiquette voulue. Ce même menu propose
    également une option pour annuler le ltre.


Lancement de WDTRAD

Pour lancer WDTRAD :
si WINDEV, WEBDEV ou WINDEV Mobile est installé sur votre poste : sous le volet "Projet", dans le
groupe "Traduire", déroulez "Traduire" et sélectionnez "Traduction des messages".
Remarque : Si vous utilisez une version française de WINDEV, WEBDEV ou WINDEV Mobile, WDTRAD
s'exécutera en français. Si vous utilisez une version anglaise de WINDEV, WEBDEV ou WINDEV Mobile,
WDTRAD s'exécutera en anglais. Il est à tout moment possible de changer cette langue dans WDTRAD
(option "? .. Langue").
si WINDEV, WEBDEV ou WINDEV Mobile n'est pas installé sur votre poste : exécutez directement le
chier "WDTRAD.EXE" présent dans le répertoire "Programs" du répertoire d'installation de WDTRAD.
Remarque : Lors du premier lancement de WDTRAD, vous devez spécier la langue dans laquelle
WDTRAD sera exécuté. Il sera à tout moment possible de changer cette langue dans WDTRAD (option "? ..
Langue").


```
WINDEV WEBDEV WINDEV Mobile
```
Comment installer WDTRAD?

WDTRAD est installé automatiquement lors de l'installation de WDMSG et/ou WDINT.

Pour installer uniquement WDTRAD, il est nécessaire d'installer et d'exécuter le chier "InstallWDTRAD.EXE"
(présent dans le package d'installation de WDMSG ou de WDINT).

Remarques

```
Par défaut, le dictionnaire fourni avec WDTRAD est automatiquement installé. Pour utiliser un dictionnaire
personnalisé :
```
1. Utilisez WDTRAD pour créer et personnaliser votre dictionnaire.
2. Récupérez le dictionnaire en copiant le sous-répertoire "Dictionnaire" (contenant le dictionnaire
    personnalisé) présent dans le répertoire d'installation de WDTRAD.
3. Collez ce sous-répertoire dans le répertoire d'installation de WDTRAD voulu.
Lors de la traduction des messages de votre application par une société extérieure, n'oubliez pas de
fournir également à cette société le(s) chier(s) des messages à traduire :
soit un chier texte,
soit le chier de données HFSQL (chiers .c, .ndx et .mmo),
soit le chier wdmsg.
Après la traduction des messages, seul(s) le(s) chier(s) contenant les messages traduits doit être
récupéré. Il sera nécessaire de réintégrer ce(s) chier(s) à l'aide de WDMSG ou de WDINT.
Lors du premier lancement de WDTRAD, vous devez spécier la langue dans laquelle WDTRAD sera
exécuté. Il sera à tout moment possible de changer cette langue dans WDTRAD (option "? .. Langue").

```
Autres
```
# Installer WDTRAD


## WINDEV WEBDEV

Présentation

Il est possible de congurer les options de WDTRAD grâce à l'option "Edition .. Préférences".

Options disponibles

Options générales

WDTRAD propose les options suivantes :
Acher seulement les ressources non traduites : Si cette option est activée, si le chier de traduction a
déjà été traduit, seules les ressources restant à traduire seront achées.
Acher les numéros de ligne : Si cette option est activée, toutes les ressources du chier de traduction
sont numérotées.
Achage hiérarchique des ressources : Si cette option est activée, le tri sera eectué pour chaque
niveau de hiérarchie. Si cette option n'est pas activée, le tri sera réalisé sur l'ensemble du document.
Charger toutes les langues du document : Si cette option est activée, il sera possible de charger une
seconde langue de référence. Attention : cette option peut ralentir le chargement des ressources.
Remarque : Cette seconde langue de référence peut être utile :
pour s'assurer des tournures de certaines phrases (choisir "tu" ou "vous" depuis un texte de référence
en anglais ("you"). En achant le texte de référence dans une 2ème langue comme l'espagnol, il n'y a
plus d'ambiguïté).
pour régler la problématique du genre de certains mots.
Gérer les étiquettes : Cette option permet de :
visualiser les diérentes étiquettes (ou bookmark) disponibles,
d'ajouter et de modier une étiquette en spéciant son intitulé et la couleur associée à l'étiquette.

Options de traduction

Les options sont les suivantes :
Considéré comme traduit quand identique : Si cette option est cochée, les ressources identiques dans
les diérentes langues seront considérées comme traduites et non "à traduire".
Par exemple, la ressource "Note" est identique en Français et en Anglais. Si cette option est cochée :
la ressource anglaise ne sera pas achée sur fond orange
la ressource sera considérée comme traduite dans les statistiques de traduction du chier.

```
WINDEV Mobile Autres
```
# Options de WDTRAD


Autoriser la recherche "full-text" : Par défaut, la recherche d'une ressource dans le dictionnaire est de
type "Commence par", "contient", ... Si cette option est cochée, la recherche est élargie. Ce mode de
recherche permet par exemple de rechercher des morceaux de phrase utilisés dans un contexte diérent.

Enregistrer toutes les langues traduites : Par défaut, lors de l'enregistrement d'une ressource dans le
dictionnaire, seules les langues actuellement utilisées sous WDTRAD sont proposées. Si cette option est
cochée, toutes les langues gérées par le dictionnaire seront proposées lors de l'ajout d'un élément dans ce
dictionnaire.

Calculer les statistiques pendant la saisie : Par défaut, le calcul des statistiques est eectué à
l'enregistrement du chier. Cette option permet de recalculer les statistiques à chaque traduction.

Recherche de traductions immédiate : Par défaut, il faut double-cliquer sur une ressource pour lancer
sa recherche dans les dictionnaires disponibles. Si cette option est cochée, il sut de sélectionner la
ressource pour lancer la recherche dans le dictionnaire.
Attention : Si des dictionnaires Web payants sont utilisés, une recherche peut être lancée sur ce
dictionnaire (et donc entraîner une facturation).

Dictionnaires Web :

```
Google : Si cette option est cochée, il est nécessaire d'indiquer la clé Google API permettant d'utiliser
Google Translate. La traduction Google sera proposée à chaque recherche de traduction ou bien
uniquement si la ressource n'a pas été trouvée dans le dictionnaire (option "Utiliser uniquement
lorsqu'aucune traduction WDTRAD n'est trouvée").
DeepL : Si cette option est cochée, il est nécessaire d'indiquer la clé API permettant d'utiliser le service
DeepL. La traduction DeepL sera proposée à chaque recherche de traduction ou bien uniquement si la
ressource n'a pas été trouvée dans le dictionnaire (option "Utiliser uniquement lorsqu'aucune
traduction WDTRAD n'est trouvée").
```
Remarques :

```
Les èches situées à droite de la liste des dictionnaires permettent donner l'ordre de priorité pour la
recherche des traductions. Si la traduction est trouvée dans le premier dictionnaire Web, elle ne sera
pas eectuée dans les suivants.
Pensez à consulter les licences et les conditions d'utilisation des logiciels de traduction utilisés,
notamment concernant les conditions de facturation.
L'option "Protéger les séquences %1, <%1!s!> ou encore [%variable%] dans les chaînes à traduire"
permet de ne pas faire traduire ces éléments par le dictionnaire Web choisi.
Terminologies personnalisées : Le bouton "Gérer les terminologies" permet de gérer le dictionnaire et
les terminologie. Il est possible de :
générer les statistiques du dictionnaire : nombre de ressources, auteur, ...
réindexer le dictionnaire si nécessaire (bouton "Réindexer"). Cette option est conseillée lorsque de
nombreuses ressources ont été ajoutées ou modiées dans le dictionnaire.
Gérer les terminologies personnalisées.
Faire des recherches dans le dictionnaire.
Voir les ajouts récents eectués dans le dictionnaire.
```

Clavier et saisie

Les options sont les suivantes :
Activer la modication des textes de référence : Si cette option est cochée, le traducteur pourra
également modier les textes de la version de référence (par exemple pour corriger les fautes
d'orthographe).
Activer l'édition en mode che automatique : Si cette option est cochée, toute modication ou saisie
d'une ressource sera eectué en mode che.
Activer la vérication de l'orthographe : Cette option permet d'activer le vérication orthographique. Il
est nécessaire :
d'installer OpenOce 2.0 ou supérieur sur le poste d'utilisation de WDTRAD.
d'installer les diérents dictionnaires voulus de OpenOce.
Activer le changement automatique de langue du clavier : Cette option permet d'installer et d'activer
les claviers manquants dans Windows (à partir de Windows Vista).

Sauvegarde

Les options sont les suivantes :
Activer la sauvegarde automatique (toutes les 10 minutes) : Si cette option est cochée, les chiers de
référence et de traduction seront enregistrés toutes les 10 minutes (par défaut, l'enregistrement est
eectué lors du clic sur le bouton "Enregistrer" ou à la fermeture de WDTRAD).


## WINDEV WEBDEV

Comment traduire un chier de messages avec WDTRAD?

Pour traduire un chier de messages avec WDTRAD :

1. Sélectionnez la langue de référence (langue dans laquelle les messages ont été extraits) et la langue de
    traduction (langue dans laquelle les messages doivent être traduits).
    Remarque : Si la langue de traduction correspond à une langue personnalisée, sélectionnez l'option
    "Langue personnalisée" et renseignez les caractéristiques de la langue (clavier, sens d'écriture, etc.).
2. Sélectionnez le chier contenant les messages à traduire dans le champ "Référence". Ce chier peut être :
    un chier texte (extension ".txt").
    un chier de données HFSQL (extension ".c").
    un chier WDMSG (extension ".wdmsg").
3. Sélectionnez le chier résultat de la traduction dans le champ "Traduction". Ce chier peut être :
    un chier texte (extension ".txt")
    un chier de données HFSQL (extension ".c").
    un chier WDMSG (extension ".wdmsg").
4. Sélectionnez le dictionnaire à utiliser. Ce dictionnaire contient les diérentes traductions déjà réalisées.
    Par défaut, WDTRAD est livré avec un dictionnaire français - anglais contenant la traduction de plus de
    6000 messages.
5. Si WINDEV, WEBDEV ou WINDEV Mobile est installé sur le poste, sélectionnez le projet correspondant aux
    messages à traduire (option "Projet" sous le chemin du dictionnaire). Si le projet est sélectionné, il sera
    possible de visualiser l'élément correspondant aux messages dans le produit concerné (option "Voir dans
    le projet" du menu contextuel du message).
6. Cliquez sur le bouton "Charger" pour acher le contenu des chiers sélectionnés dans WDTRAD. La
    colonne "Référence" ache les messages extraits. La colonne "Traduction" ache les messages traduits à
    réintégrer. Chaque ligne du tableau correspond à un message.
    Remarque : La couleur de fond des messages non traduits est orangée.
7. Cliquez sur le bouton "Autotrad". Toutes les expressions "Référence" trouvées à l'identique dans le
    dictionnaire sont automatiquement traduites.
8. Sélectionnez une ligne du tableau et modiez si nécessaire le message original.
    Remarque : Si des modications sont eectuées sur le chier de référence, il sera nécessaire de réintégrer
    ce chier dans l'application WINDEV, WEBDEV ou WINDEV Mobile originale grâce à WDMSG.

```
WINDEV Mobile Autres
```
# Traduire un chier de messages

# avec WDTRAD


9. Cliquez sur la loupe présente devant le message : une fenêtre s'ouvre permettant de voir le contexte de la
    ressource à traduire. Le champ en cours de traduction est entouré d'un cadre rouge.
10. Double-cliquez sur le message (ou cliquez sur le bouton "Rechercher"). Les diérentes traductions
proposées pour le message apparaissent dans le tableau "Dictionnaire". Les traductions sont listées selon
leur pertinence. L'icône présente devant chaque traduction indique le degré de pertinence de la
traduction.
Remarque : WDTRAD reconstruit automatiquement une traduction quand une traduction proche est
trouvée.
11. Double-cliquez sur la traduction voulue. La traduction est automatiquement copiée dans la colonne
"Traduction" du message en cours.
Remarque : Si aucune traduction ne vous convient, saisissez la traduction voulue dans la colonne
"Traduction" du message en cours. Pour ajouter cette nouvelle traduction au dictionnaire, sélectionnez
l'option "Ajouter au dictionnaire" du menu contextuel du message.
12. Répétez les opérations 8 à 10 pour tous les messages à traduire.
13. Cliquez sur le bouton "Enregistrer" pour enregistrer le chier de référence et le chier de traduction.

```
Remarques :
Pour visualiser les longs messages et/ou les messages au format RTF, sélectionnez l'option "Visualiser en
mode che" du menu contextuel du message.
Le chier des messages traduits :
peut être imprimé pour vérication, avec l'option "Fichier .. Imprimer".
pourra être intégré dans le projet avec WDMSG ou WDINT.
WDTRAD propose deux modes de copie entre les messages extraits et les messages traduits. Pour plus de
détails, consultez les Diérents modes de copie.
Pour paramétrer le dictionnaire (ajouter/modier/supprimer des ressources), sélectionnez l'option
"Propriétés du dictionnaire" du menu contextuel de la table "Dictionnaire". Pour plus de détails, consultez
Propriétés du dictionnaire
Pour paramétrer WDTRAD, utilisez l'option "Edition .. Préférences". Le détail de ces options sont
présentées dans Options de WDTRAD.
WDTRAD permet de diérencier les traductions grâce aux emplacements. Les traductions commercia les
peuvent par exemple être regroupées dans l'emplacement "Commercial" et les traductions d'inter face
dans l'emplacement "Interface". Lors de l'ajout d'un élément dans le dictionnaire et lors de la traduction, il
est possible d'indiquer l'emplacement à utiliser.
Pour créer de nouveaux emplacements, utilisez l'option "Edition .. Editer les emplacements".
Pour chaque langue, il est possible de paramétrer les caractéristiques de la langue : clavier utilisé,
symboles. Pour plus de détails, consultez Propriétés du dictionnaire.
```

```
Les ressources traduites (par exemple lors d'une traduction automatique) peuvent apparaître sur fond
orange, comme si cette ressource n'était pas traduite. En eet, un algorithme spécique permet de
déterminer si une ressource est traduite :
Les mots composés d'une seule lettre sont considérés comme traduits s'ils sont identiques.
Si l'option "Considéré comme traduit si identique" est active, les mots sont considérés comme traduits
si la traduction est identique à la référence.
Dans tous les autres cas, un ratio est calculé entre le nombre de mots traduits et le nombre de mots à
traduire. Si ce ratio est inférieur à un seuil déterminé dynamiquement, la ressource n'est pas considérée
comme traduite. Dans le cas contraire, la ressource est considérée traduite si et seulement si le nombre
de lignes de la ressource est identique entre la traduction et la référence.
```
Comment rechercher un message dans WDTRAD?

Pour chercher un message dans le cher aché sous WDTRAD, vous pouvez :
trier les messages par ordre alphabétique : cliquez sur l'entête de la colonne.
trier les messages par type de message : cliquez sur l'entête de la colonne "Type".
eectuer un ltre pour acher uniquement les lignes marquées avec une étiquette : cliquez sur le picto
de l'étiquette dans la colonne "Type" et sélectionnez l'étiquette à ltrer. Pour supprimer le ltre,
sélectionnez l'option "Annuler le ltre" dans le menu aché via le picto.
eectuer une recherche simple : cliquez sur l'icône présente dans l'entête de colonne et saisissez le
début du message recherché.
Remarque : Cette recherche peut également être eectuée dans les ressources trouvées dans le
dictionnaire.
utiliser un ltre : faites un clic droit sur la loupe présente dans l'entête de colonne et sélectionnez l'option
"Filtrer" avec la description du ltre. Saisissez dans l'entête de la colonne la condition du ltre : seules les
lignes correspondantes s'acheront dans la table. Pour supprimer le ltre, sélectionnez l'option
"Supprimer le ltre" dans le menu contextuel de la colonne.
faire une recherche avancée : utiliser la combinaison de touches Ctrl + F et saisissez les paramètres de la
recherche :
Le texte à rechercher,
Le texte qui remplacera le texte recherché (si nécessaire),
La langue dans laquelle la recherche doit être eectuée,
Les caractéristiques de la recherche ("mot entier uniquement", "Respecter la casse", "boucler").
Utilisez les boutons "Suivant", "Remplacer", "Remplacer tout" pour eectuer la recherche et les
remplacements.

Pour faire une recherche dans le dictionnaire de WDTRAD, vous pouvez :

```
Utiliser la zone de recherche achée sous la liste des ressources. Il sut de saisir le message recherché,
la langue, et de cliquer sur "Rechercher".
```

```
Utiliser l'onglet "Rechercher" des propriétés du dictionnaire. Pour plus de détails, consultez
Propriétés du dictionnaire.
```
Comment forcer un clavier en saisie de message dans WDTRAD?

La saisie dans une langue dans WDTRAD change automatiquement le clavier et l'alphabet dans ceux de la
langue utilisée. Ce mécanisme permet la saisie dans des langues qui utilisent des claviers et alphabets
spéciques (Russe, Chinois, Japonais, Arabe, Grec, etc.).

Cela a également pour eet de basculer le clavier en QWERTY lors de la saisie d'un texte en anglais. Si vous
désirez saisir vos textes anglais avec un clavier français (AZERTY), vous devez changer le clavier associé à la
langue anglaise dans Windows :

1. Achez les préférences de WDTRAD (option "Edition .. Préférences").
2. Sélectionnez l'option "Activer le changement automatique de langue du clavier", et si nécessaire l'option
    "Installer automatiquement les claviers manquants". Cette option permet d'installer et d'activer les
    claviers manquants.
3. Validez la fenêtre des options de WDTRAD.

Notes

Caractères spéciques dans les messages (librairies du framework, messages de programmation, etc.)

Certains messages comportent :
Des chaînes de caractères de type %s, %1, %2, %1!d!, ...
Ces chaînes de caractères sont utilisées dans des messages paramétrés. A l'exécution, ces chaînes sont
automatiquement remplacées par le nom d'un répertoire, le nom d'un chier, ...
Ces chaînes de caractères ne doivent pas être modiées ou supprimées dans la traduction du message.
Cependant, la position de ces chaînes de caractères peut être modiée.
Par exemple, la traduction en anglais du message "Erreur à la ligne %1!d! du traitement %2." devra être
"Error in process %2, line %1!d!.".
Des chaînes de caractères de type [%xxxx%]
Ces chaînes de caractères sont utilisées dans des messages paramétrés. A l'exécution, ces chaînes sont
automatiquement remplacées par le contenu d'une variable, etc.
Ces chaînes de caractères ne doivent pas être modiées ou supprimées dans la traduction du message. Le
contenu de ces chaînes ne doit pas être traduit. Cependant, la position de ces chaînes de caractères peut
être modiée.
Par exemple, la traduction en anglais du message "Conrmez-vous la création du client : [%sNomClient%]"
devra être "Do you conm the creation of the customer : [%sNomClient%]".


Des chaînes de caractères de type \t, \n, \r.
Ces chaînes de caractères permettent de mettre en forme les messages (tabulation, saut de ligne, etc.).
Ces chaînes de caractères ne doivent pas être modiées ou supprimées dans la traduction du message. Il
est déconseillé de modier la position de ces chaînes de caractères.
Par exemple, la traduction en anglais du message "Impossible d'ouvrir le chier xBase <%1!s!>.\r\nCode
d'erreur renvoyé par la DLL xBase : %2!d!." devra être "Unable to open xBase <%1!s!> le.\r\nError code
returned by xBase DLL: %2!d!.".


## WINDEV WEBDEV

Présentation

Il est possible de congurer les options du dictionnaire de WDTRAD grâce à l'option "Edition .. Propriétés du
dictionnaire". La fenêtre qui s'ache est composée de plusieurs onglets dédockables.

Onglet "Général" : Options disponibles

L'onglet "Général" permet :
d'obtenir des statistiques de traduction sur le dictionnaire en cours
d'eectuer des opérations de maintenance.

Statistiques de traduction

Pour obtenir les statistiques de traduction, cliquez sur le lien "Générer les statistiques du dictionnaire". Ces
statistiques permettent d'obtenir le nombre de ressources présentes dans le dictionnaire.

Maintenance

Les opérations de maintenance sont les suivantes :
Paramétrage de la langue : Pour chaque langue, il est possible de paramétrer les caractéristiques de la
langue : clavier utilisé, symboles. Le paramétrage des symboles est utilisé par WDTRAD lors de la
reconstruction d'une traduction à partir d'une traduction existante.
Pour paramétrer les caractéristiques d'une langue :

1. Sélectionnez la langue voulue.
2. Cliquez sur le bouton. L'onglet "Cla vier" et l'onglet "Symboles" permettent de congurer les
    spécicités de la langue sélectionnée.
Réindexation du dictionnaire : Pour chaque langue, il est possible de réindexer le dictionnaire. Cette
réindexation permet d'optimiser les performances d'accès aux données du dictionnaire. Cette
réindexation peut prendre plusieurs minutes.
Pour réindexer une langue :
1. Sélectionnez la langue voulue.
2. Cliquez sur le bouton "Réindexer" et validez.

Onglet "Terminologies personnalisées" : Options disponibles

```
WINDEV Mobile Autres
```
# Propriétés du dictionnaire


L'onglet "Terminologie" permet de ger des traductions à utiliser pour certains termes. Ces traductions seront
utilisées dès que les termes spéciés seront rencontrés lors d'une traduction automatique réalisée via DeepL
par exemple.

L'option "Synchroniser avec Amazon" permet de stocker les terminologies dans Amazon Translate.

Onglet "Recherche" : Options disponibles

L'onglet "Recherche" permet d'eectuer une recherche spécique dans le dictionnaire.

Il sut de :

1. Sélectionner la langue d'origine et la langue destination.
2. Saisir dans la zone "Recherche" le texte à rechercher dans la langue voulue.
3. Cliquer sur le bouton "Rechercher". Selon les options spéciées, les ressources trouvées sont listées et
    peuvent être modiées.

Remarque : Le menu contextuel de la table des ressources trouvées permet d'ajouter une entrée dans le
dictionnaire (option "Ajouter une entrée dans le dictionnaire").

Onglet "Rechercher / Remplacer" : Options disponibles

L'onglet "Rechercher / Remplacer" permet d'eectuer une recherche et un remplacement dans le
dictionnaire.

Il sut de :

1. Sélectionner la langue dans laquelle la recherche doit être eectuée.
2. Saisir dans la zone "Recherche" le texte à rechercher dans la langue spéciée.
    Remarque : Les caractères * et? peuvent être utilisés. Le caractère ~ permet d'exclure un terme de la
    recherche.
3. Indiquer les options de recherche (casse, commence par, ...).
4. Cliquer sur le bouton "Rechercher". Selon les options spéciées, les ressources trouvées sont listées.
5. Indiquer le texte de remplacement.
6. Eectuer le remplacement :
    Cliquer sur "Remplacer" pour remplacer la ressource sélectionnée.
    Cliquer sur "Remplacer tout" pour remplacer toutes les ressources listées.

Onglet "Ajoutés récemment" : Options disponibles


L'onglet "Ajoutés récemment" permet de lister les dernières ressources ajoutées dans le dictionnaire. Il est
possible de sélectionner les langues voulues ainsi que l'auteur de la traduction. Les 100 dernières ressources
sont achées.


## WINDEV WEBDEV

Présentation

WDTRAD permet d'importer et d'exporter un dictionnaire.

Rappel : Un dictionnaire peut contenir les traductions d'une même ressource en plusieurs langues. Par
exemple, dans le même dictionnaire, l'expression "Fermer l'application" peut être traduite en anglais, en
espagnol et en allemand.

Importer le dictionnaire

WDTRAD permet d'importer :
un dictionnaire existant, correspondant à une version précédente de WDTRAD (inférieure à la version 17).
Au lancement de WDTRAD, si un dictionnaire d'une version précédente est trouvée sur le poste
d'utilisation, cette option est proposée automatiquement.
une mémoire de traduction générée :
par un logiciel de traduction (chier au format TMX).
par WDTRAD (chier au format TMX).
une traduction déjà réalisée avec WDTRAD (chiers au format TXT ou FIC).
un dictionnaire WDTRAD existant (version 18 à 2025).
un dictionnaire local dans un dictionnaire présent sur une plateforme PCSCloud.

Cette fonctionnalité permet d'insérer automatiquement des traductions déjà réalisées dans le dictionnaire
manipulé par WDTRAD.

Pour importer un dictionnaire existant :

1. Sous WDTRAD, sélectionnez l'option "Fichier .. Mémoire de traduction .. Importer une version précédente
    d'un dictionnaire WDTRAD".
2. Sélectionnez le chier ".FIC" correspondant au dictionnaire à importer. Validez.
3. Les nouvelles ressources sont automatiquement insérées dans le dictionnaire manipulé par WDTRAD.
    Les ressources identiques sont automatiquement écrasées.

Pour importer une mémoire de traduction :

1. Sous WDTRAD, sélectionnez l'option "Fichier .. Mémoire de traduction .. Importer dans le dictionnaire".

```
WINDEV Mobile Autres
```
# Importer/Exporter un dictionnaire


2. Sélectionnez au choix :
    le chier ".TMX" correspondant à la mémoire de traduction à importer.
    le chier ".TXT" ou "FIC" correspondant aux chiers déjà traduits dont les ressources doivent être
    importées.
    le chier "DICT.FIC" correspondant à un dictionnaire WDTRAD existant (version 18 à 2025).
3. Les nouvelles ressources sont automatiquement insérées dans le dictionnaire manipulé par WDTRAD.
    Les ressources identiques sont automatiquement écrasées.

Pour importer un dictionnaire local dans un dictionnaire PCSCloud :

1. Sous WDTRAD, connectez-vous à un dictionnaire PCSCloud.
2. Sélectionnez l'option "Fichier .. Mémoire de traduction .. Importer dans le dictionnaire".
3. Sélectionnez le chier "Dictionnaire WDTRAD (DICT.FIC)" correspondant au dictionnaire à importer.
    Validez.
4. Les nouvelles ressources sont automatiquement insérées dans le dictionnaire PCSCloud.
    Les ressources identiques sont automatiquement écrasées.

Remarque : A la première connexion à un dictionnaire PCSCloud, si ce dictionnaire est vide, l'import d'un
dictionnaire local est automatiquement proposé.

Exporter le dictionnaire

WDTRAD permet d'exporter les ressources contenues dans le dictionnaire utilisé. Lors de l'exportation d'un
dictionnaire, un chier mémoire de traduction (chier ".TMX") est créé. Ce chier est créé dans le sous-
répertoire "Dictionnaire" du répertoire d'installation de WDTRAD.

Pour exporter le dictionnaire manipulé par WDTRAD, sélectionnez l'option "Fichier .. Mémoire de
traduction .. Exporter le dictionnaire".


## WINDEV WEBDEV

Présentation

WDTRAD propose deux modes de copie entre les messages extraits et les messages traduits :
copie simple.
copie du message "Traduction" pour tous les messages "Référence" identiques.

Copie simple

Cette méthode permet de copier le message "Référence" en cours dans le message "Traduction"
correspondant.

Pour eectuer une copie simple, cliquez sur le bouton "Copier réf.".

Copie du message "Traduction" pour tous les messages "Référence"
identiques

Cette méthode aecte le message "Traduction" en cours à toutes les autres lignes ayant le même message
"Référence".

Pour eectuer ce mode de copie, cliquez sur le bouton "Reporter trad.".

Ce mode de copie recherche toutes les lignes dont la colonne "Référence" est identique à celle de la ligne en
cours. Le message "Traduction" de la ligne en cours est ensuite aecté à l'ensemble des lignes trouvées.

Par exemple, si la ligne en cours contient le message "Annuler" et sa traduction "Cancel", un clic sur le
bouton "Reporter trad." permet de :

```
rechercher tous les messages "Annuler",
renseigner la traduction "Cancel" pour chacun des messages "Annuler" trouvés.
```
```
WINDEV Mobile Autres
```
# Les diérents modes de copie


## WINDEV WEBDEV

Remarque : Si des messages "Traduction" étaient présents dans les messages trouvés, ces messages
"Traduction" sont remplacés avec la nouvelle traduction.

Présentation

WDTRAD est un outil de saisie de traduction des messages associés à une application WINDEV, WEBDEV ou
WINDEV Mobile. Ces messages ont été extraits avec WDMSG ou WDINT.

WDTRAD facilite le travail de saisie de la traduction des messages et limite les risques d'erreurs de traduction.

WDTRAD permet de :

```
visualiser le texte à traduire et de saisir sa traduction.
visualiser les langues 2 à 2 (origine et traduction) même si le chier à traduire (format WDMSG ou HFSQL)
contient plus de 2 langues.
Remarque : Il est également possible d'acher une langue d'origine supplémentaire pour s'assurer des
tournures ou du genre des expressions.
choisir la langue d'origine et la langue de traduction (notamment si le chier à traduire (format WDMSG ou
HFSQL) contient plus de 2 langues).
visualiser dans WINDEV, WEBDEV ou WINDEV Mobile, l'élément correspondant aux textes à traduire
(fenêtre et page uniquement).
proposer une traduction automatique.
traduire automatiquement tous les mots ou expressions identiques (soit dans l'ensemble du chier, soit
uniquement dans les lignes achées).
vérier l'homogénéité des traductions en visualisant l'ensemble du texte initial et du texte traduit.
éviter toute erreur de manipulation en ne travaillant pas directement sur le chier des messages à
traduire.
visualiser en temps réel l'avancement de la traduction et le nombre de lignes restant à traduire.
visualiser directement le nombre de mots ou de caractères alphanumériques à traduire.
Cette option permet d'évaluer le coût de traduction par une société de traduction : la traduction est
généralement facturée en fonction du nombre de mots ou de caractères à traduire.
trier les chaînes à traduire par langue d'origine et par langue de traduction.
trier les chaînes à traduire selon leur type.
visualiser l'interface de l'élément en cours de traduction (option disponible uniquement pour les chiers
d'extraction au format HFSQL et WDMSG).
```
```
WINDEV Mobile Autres
```
# WDTRAD


```
eectuer un "Rechercher / Remplacer" parmi les ressources à traduire et traduites.
eectuer une recherche sur les ruptures en mode d'achage hiérarchique grâce à une icône "Loupe".
gérer des "bookmarks" : Il est possible de mettre une ou plusieurs marques dans le chier en cours de
traduction (matérialisée par un bandeau coloré). Ces marques peuvent par exemple servir à indiquer une
ressource à revoir, le point d'arrêt de la traduction en cours, ...
Pour mettre une marque, utilisez le raccourci Ctrl F7.
Pour se déplacer entre les marques, utilisez la touche F7.
Il est également possible de créer ses propres étiquettes de bookmark (voir ci-dessous).
```
En cas de traduction par une société extérieure, WDTRAD peut être livré à cette société avec le chier des
messages à traduire (chier texte, chier de données HFSQL ou chier WDMSG). Dans ce cas, vous devez
également fournir des chiers nécessaires à l'utilisation de WDTRAD (voir Installer WDTRAD).

Pour plus de détails sur l'utilisation de WDTRAD, consultez Traduire un chier de messages avec WDTRAD.

Remarques :

```
Il est possible de changer la langue de l'interface de WDTRAD (option "? .. Langue").
Seuls les chiers extraits avec WDMSG et/ou WDINT peuvent être manipulés avec WDTRAD.
WDTRAD permet de saisir les traductions en utilisant des alphabets non latins.
```

Gestion des langues :

```
WDTRAD permet de gérer la traduction de messages dans 41 langues diérentes.
WDTRAD permet de gérer les langues personnalisées utilisées dans les projets WINDEV, WEBDEV ou
WINDEV Mobile. Il sut de sélectionner la langue de traduction "Langue personnalisée" pour
congurer les paramètres de cette langue.
Si le nom des langues personnalisées a été modié dans le projet WINDEV, WEBDEV ou WINDEV
Mobile, le nom de cette langue apparaît automatiquement dans la liste des langues. Les paramètres de
cette langue décrits dans WINDEV, WEBDEV ou WINDEV Mobile sont automatiquement pris en compte.
```
Gestion des dictionnaires :

```
WDTRAD est livré avec un dictionnaire français - anglais contenant la traduction de plus de 6000
messages. Ce dictionnaire peut être enrichi grâce à WDTRAD. Ce dictionnaire peut également être
utilisé avec WDDIXIO. Pour plus de détails sur WDDIXIO, consultez l'aide en ligne (mot-clé : WDDIXIO")
ou le chier d'aide "WDDIXIO.chm".
Un dictionnaire peut contenir les traductions d'une même ressource en plusieurs langues. Par
exemple, dans le même dictionnaire, l'expression "Fermer l'application" peut être traduite en anglais,
en espagnol et en allemand.
WDTRAD permet d'utiliser un dictionnaire situé sur une plateforme de développement PCSCloud
(option "Edition .. Localiser le dictionnaire .. Dictionnaire en mode cloud").
Remarque : A la première connexion à un dictionnaire PCSCloud, si ce dictionnaire est vide, l'import
d'un dictionnaire local est automatiquement proposé.
WDTRAD permet d'importer et/ou d'exporter un dictionnaire. Pour plus de détails, consultez
Importer/Exporter un dictionnaire.
WDTRAD permet de gérer des dictionnaires Web (Google et DeepL). Le choix du ou des dictionnaires
Web à utiliser est réalisé dans les options de WDTRAD.
WDTRAD permet d'ajouter une ressource dans le dictionnaire même si aucun chier de traduction
n'est ouvert (option "Ajouter une entrée dans le dictionnaire").
```
Gestion des étiquettes de bookmark :
Pour gérer des étiquettes de bookmark :

1. Pour marquer une ligne, achez le menu contextuel de la ligne et sélectionnez l'option "Bookmark ..
    Appliquer une étiquette" et sélectionnez l'étiquette voulue. Si aucune étiquette n'est proposée, vous
    pouvez en créer grâce à l'option "Gérer les étiquettes". Cette option permet de créer, modier et
    supprimer les étiquettes.
    Remarque : Le création, modication et suppression des étiquettes peut également être réalisée
    depuis les options de WDTRAD.
2. Pour ltrer les ressources selon une étiquette, cliquez sur l'étiquette apparaissant dans la colonne
    "Type" : un menu apparaît permettant de ltrer sur l'étiquette voulue. Ce même menu propose
    également une option pour annuler le ltre.


Lancement de WDTRAD

Pour lancer WDTRAD :
si WINDEV, WEBDEV ou WINDEV Mobile est installé sur votre poste : sous le volet "Projet", dans le
groupe "Traduire", déroulez "Traduire" et sélectionnez "Traduction des messages".
Remarque : Si vous utilisez une version française de WINDEV, WEBDEV ou WINDEV Mobile, WDTRAD
s'exécutera en français. Si vous utilisez une version anglaise de WINDEV, WEBDEV ou WINDEV Mobile,
WDTRAD s'exécutera en anglais. Il est à tout moment possible de changer cette langue dans WDTRAD
(option "? .. Langue").
si WINDEV, WEBDEV ou WINDEV Mobile n'est pas installé sur votre poste : exécutez directement le
chier "WDTRAD.EXE" présent dans le répertoire "Programs" du répertoire d'installation de WDTRAD.
Remarque : Lors du premier lancement de WDTRAD, vous devez spécier la langue dans laquelle
WDTRAD sera exécuté. Il sera à tout moment possible de changer cette langue dans WDTRAD (option "? ..
Langue").


```
WINDEV WEBDEV WINDEV Mobile
```
Comment installer WDTRAD?

WDTRAD est installé automatiquement lors de l'installation de WDMSG et/ou WDINT.

Pour installer uniquement WDTRAD, il est nécessaire d'installer et d'exécuter le chier "InstallWDTRAD.EXE"
(présent dans le package d'installation de WDMSG ou de WDINT).

Remarques

```
Par défaut, le dictionnaire fourni avec WDTRAD est automatiquement installé. Pour utiliser un dictionnaire
personnalisé :
```
1. Utilisez WDTRAD pour créer et personnaliser votre dictionnaire.
2. Récupérez le dictionnaire en copiant le sous-répertoire "Dictionnaire" (contenant le dictionnaire
    personnalisé) présent dans le répertoire d'installation de WDTRAD.
3. Collez ce sous-répertoire dans le répertoire d'installation de WDTRAD voulu.
Lors de la traduction des messages de votre application par une société extérieure, n'oubliez pas de
fournir également à cette société le(s) chier(s) des messages à traduire :
soit un chier texte,
soit le chier de données HFSQL (chiers .c, .ndx et .mmo),
soit le chier wdmsg.
Après la traduction des messages, seul(s) le(s) chier(s) contenant les messages traduits doit être
récupéré. Il sera nécessaire de réintégrer ce(s) chier(s) à l'aide de WDMSG ou de WDINT.
Lors du premier lancement de WDTRAD, vous devez spécier la langue dans laquelle WDTRAD sera
exécuté. Il sera à tout moment possible de changer cette langue dans WDTRAD (option "? .. Langue").

```
Autres
```
# Installer WDTRAD


## WINDEV WEBDEV

Présentation

Il est possible de congurer les options de WDTRAD grâce à l'option "Edition .. Préférences".

Options disponibles

Options générales

WDTRAD propose les options suivantes :
Acher seulement les ressources non traduites : Si cette option est activée, si le chier de traduction a
déjà été traduit, seules les ressources restant à traduire seront achées.
Acher les numéros de ligne : Si cette option est activée, toutes les ressources du chier de traduction
sont numérotées.
Achage hiérarchique des ressources : Si cette option est activée, le tri sera eectué pour chaque
niveau de hiérarchie. Si cette option n'est pas activée, le tri sera réalisé sur l'ensemble du document.
Charger toutes les langues du document : Si cette option est activée, il sera possible de charger une
seconde langue de référence. Attention : cette option peut ralentir le chargement des ressources.
Remarque : Cette seconde langue de référence peut être utile :
pour s'assurer des tournures de certaines phrases (choisir "tu" ou "vous" depuis un texte de référence
en anglais ("you"). En achant le texte de référence dans une 2ème langue comme l'espagnol, il n'y a
plus d'ambiguïté).
pour régler la problématique du genre de certains mots.
Gérer les étiquettes : Cette option permet de :
visualiser les diérentes étiquettes (ou bookmark) disponibles,
d'ajouter et de modier une étiquette en spéciant son intitulé et la couleur associée à l'étiquette.

Options de traduction

Les options sont les suivantes :
Considéré comme traduit quand identique : Si cette option est cochée, les ressources identiques dans
les diérentes langues seront considérées comme traduites et non "à traduire".
Par exemple, la ressource "Note" est identique en Français et en Anglais. Si cette option est cochée :
la ressource anglaise ne sera pas achée sur fond orange
la ressource sera considérée comme traduite dans les statistiques de traduction du chier.

```
WINDEV Mobile Autres
```
# Options de WDTRAD


Autoriser la recherche "full-text" : Par défaut, la recherche d'une ressource dans le dictionnaire est de
type "Commence par", "contient", ... Si cette option est cochée, la recherche est élargie. Ce mode de
recherche permet par exemple de rechercher des morceaux de phrase utilisés dans un contexte diérent.

Enregistrer toutes les langues traduites : Par défaut, lors de l'enregistrement d'une ressource dans le
dictionnaire, seules les langues actuellement utilisées sous WDTRAD sont proposées. Si cette option est
cochée, toutes les langues gérées par le dictionnaire seront proposées lors de l'ajout d'un élément dans ce
dictionnaire.

Calculer les statistiques pendant la saisie : Par défaut, le calcul des statistiques est eectué à
l'enregistrement du chier. Cette option permet de recalculer les statistiques à chaque traduction.

Recherche de traductions immédiate : Par défaut, il faut double-cliquer sur une ressource pour lancer
sa recherche dans les dictionnaires disponibles. Si cette option est cochée, il sut de sélectionner la
ressource pour lancer la recherche dans le dictionnaire.
Attention : Si des dictionnaires Web payants sont utilisés, une recherche peut être lancée sur ce
dictionnaire (et donc entraîner une facturation).

Dictionnaires Web :

```
Google : Si cette option est cochée, il est nécessaire d'indiquer la clé Google API permettant d'utiliser
Google Translate. La traduction Google sera proposée à chaque recherche de traduction ou bien
uniquement si la ressource n'a pas été trouvée dans le dictionnaire (option "Utiliser uniquement
lorsqu'aucune traduction WDTRAD n'est trouvée").
DeepL : Si cette option est cochée, il est nécessaire d'indiquer la clé API permettant d'utiliser le service
DeepL. La traduction DeepL sera proposée à chaque recherche de traduction ou bien uniquement si la
ressource n'a pas été trouvée dans le dictionnaire (option "Utiliser uniquement lorsqu'aucune
traduction WDTRAD n'est trouvée").
```
Remarques :

```
Les èches situées à droite de la liste des dictionnaires permettent donner l'ordre de priorité pour la
recherche des traductions. Si la traduction est trouvée dans le premier dictionnaire Web, elle ne sera
pas eectuée dans les suivants.
Pensez à consulter les licences et les conditions d'utilisation des logiciels de traduction utilisés,
notamment concernant les conditions de facturation.
L'option "Protéger les séquences %1, <%1!s!> ou encore [%variable%] dans les chaînes à traduire"
permet de ne pas faire traduire ces éléments par le dictionnaire Web choisi.
Terminologies personnalisées : Le bouton "Gérer les terminologies" permet de gérer le dictionnaire et
les terminologie. Il est possible de :
générer les statistiques du dictionnaire : nombre de ressources, auteur, ...
réindexer le dictionnaire si nécessaire (bouton "Réindexer"). Cette option est conseillée lorsque de
nombreuses ressources ont été ajoutées ou modiées dans le dictionnaire.
Gérer les terminologies personnalisées.
Faire des recherches dans le dictionnaire.
Voir les ajouts récents eectués dans le dictionnaire.
```

Clavier et saisie

Les options sont les suivantes :
Activer la modication des textes de référence : Si cette option est cochée, le traducteur pourra
également modier les textes de la version de référence (par exemple pour corriger les fautes
d'orthographe).
Activer l'édition en mode che automatique : Si cette option est cochée, toute modication ou saisie
d'une ressource sera eectué en mode che.
Activer la vérication de l'orthographe : Cette option permet d'activer le vérication orthographique. Il
est nécessaire :
d'installer OpenOce 2.0 ou supérieur sur le poste d'utilisation de WDTRAD.
d'installer les diérents dictionnaires voulus de OpenOce.
Activer le changement automatique de langue du clavier : Cette option permet d'installer et d'activer
les claviers manquants dans Windows (à partir de Windows Vista).

Sauvegarde

Les options sont les suivantes :
Activer la sauvegarde automatique (toutes les 10 minutes) : Si cette option est cochée, les chiers de
référence et de traduction seront enregistrés toutes les 10 minutes (par défaut, l'enregistrement est
eectué lors du clic sur le bouton "Enregistrer" ou à la fermeture de WDTRAD).


## WINDEV WEBDEV

Comment traduire un chier de messages avec WDTRAD?

Pour traduire un chier de messages avec WDTRAD :

1. Sélectionnez la langue de référence (langue dans laquelle les messages ont été extraits) et la langue de
    traduction (langue dans laquelle les messages doivent être traduits).
    Remarque : Si la langue de traduction correspond à une langue personnalisée, sélectionnez l'option
    "Langue personnalisée" et renseignez les caractéristiques de la langue (clavier, sens d'écriture, etc.).
2. Sélectionnez le chier contenant les messages à traduire dans le champ "Référence". Ce chier peut être :
    un chier texte (extension ".txt").
    un chier de données HFSQL (extension ".c").
    un chier WDMSG (extension ".wdmsg").
3. Sélectionnez le chier résultat de la traduction dans le champ "Traduction". Ce chier peut être :
    un chier texte (extension ".txt")
    un chier de données HFSQL (extension ".c").
    un chier WDMSG (extension ".wdmsg").
4. Sélectionnez le dictionnaire à utiliser. Ce dictionnaire contient les diérentes traductions déjà réalisées.
    Par défaut, WDTRAD est livré avec un dictionnaire français - anglais contenant la traduction de plus de
    6000 messages.
5. Si WINDEV, WEBDEV ou WINDEV Mobile est installé sur le poste, sélectionnez le projet correspondant aux
    messages à traduire (option "Projet" sous le chemin du dictionnaire). Si le projet est sélectionné, il sera
    possible de visualiser l'élément correspondant aux messages dans le produit concerné (option "Voir dans
    le projet" du menu contextuel du message).
6. Cliquez sur le bouton "Charger" pour acher le contenu des chiers sélectionnés dans WDTRAD. La
    colonne "Référence" ache les messages extraits. La colonne "Traduction" ache les messages traduits à
    réintégrer. Chaque ligne du tableau correspond à un message.
    Remarque : La couleur de fond des messages non traduits est orangée.
7. Cliquez sur le bouton "Autotrad". Toutes les expressions "Référence" trouvées à l'identique dans le
    dictionnaire sont automatiquement traduites.
8. Sélectionnez une ligne du tableau et modiez si nécessaire le message original.
    Remarque : Si des modications sont eectuées sur le chier de référence, il sera nécessaire de réintégrer
    ce chier dans l'application WINDEV, WEBDEV ou WINDEV Mobile originale grâce à WDMSG.

```
WINDEV Mobile Autres
```
# Traduire un chier de messages

# avec WDTRAD


9. Cliquez sur la loupe présente devant le message : une fenêtre s'ouvre permettant de voir le contexte de la
    ressource à traduire. Le champ en cours de traduction est entouré d'un cadre rouge.
10. Double-cliquez sur le message (ou cliquez sur le bouton "Rechercher"). Les diérentes traductions
proposées pour le message apparaissent dans le tableau "Dictionnaire". Les traductions sont listées selon
leur pertinence. L'icône présente devant chaque traduction indique le degré de pertinence de la
traduction.
Remarque : WDTRAD reconstruit automatiquement une traduction quand une traduction proche est
trouvée.
11. Double-cliquez sur la traduction voulue. La traduction est automatiquement copiée dans la colonne
"Traduction" du message en cours.
Remarque : Si aucune traduction ne vous convient, saisissez la traduction voulue dans la colonne
"Traduction" du message en cours. Pour ajouter cette nouvelle traduction au dictionnaire, sélectionnez
l'option "Ajouter au dictionnaire" du menu contextuel du message.
12. Répétez les opérations 8 à 10 pour tous les messages à traduire.
13. Cliquez sur le bouton "Enregistrer" pour enregistrer le chier de référence et le chier de traduction.

```
Remarques :
Pour visualiser les longs messages et/ou les messages au format RTF, sélectionnez l'option "Visualiser en
mode che" du menu contextuel du message.
Le chier des messages traduits :
peut être imprimé pour vérication, avec l'option "Fichier .. Imprimer".
pourra être intégré dans le projet avec WDMSG ou WDINT.
WDTRAD propose deux modes de copie entre les messages extraits et les messages traduits. Pour plus de
détails, consultez les Diérents modes de copie.
Pour paramétrer le dictionnaire (ajouter/modier/supprimer des ressources), sélectionnez l'option
"Propriétés du dictionnaire" du menu contextuel de la table "Dictionnaire". Pour plus de détails, consultez
Propriétés du dictionnaire
Pour paramétrer WDTRAD, utilisez l'option "Edition .. Préférences". Le détail de ces options sont
présentées dans Options de WDTRAD.
WDTRAD permet de diérencier les traductions grâce aux emplacements. Les traductions commercia les
peuvent par exemple être regroupées dans l'emplacement "Commercial" et les traductions d'inter face
dans l'emplacement "Interface". Lors de l'ajout d'un élément dans le dictionnaire et lors de la traduction, il
est possible d'indiquer l'emplacement à utiliser.
Pour créer de nouveaux emplacements, utilisez l'option "Edition .. Editer les emplacements".
Pour chaque langue, il est possible de paramétrer les caractéristiques de la langue : clavier utilisé,
symboles. Pour plus de détails, consultez Propriétés du dictionnaire.
```

```
Les ressources traduites (par exemple lors d'une traduction automatique) peuvent apparaître sur fond
orange, comme si cette ressource n'était pas traduite. En eet, un algorithme spécique permet de
déterminer si une ressource est traduite :
Les mots composés d'une seule lettre sont considérés comme traduits s'ils sont identiques.
Si l'option "Considéré comme traduit si identique" est active, les mots sont considérés comme traduits
si la traduction est identique à la référence.
Dans tous les autres cas, un ratio est calculé entre le nombre de mots traduits et le nombre de mots à
traduire. Si ce ratio est inférieur à un seuil déterminé dynamiquement, la ressource n'est pas considérée
comme traduite. Dans le cas contraire, la ressource est considérée traduite si et seulement si le nombre
de lignes de la ressource est identique entre la traduction et la référence.
```
Comment rechercher un message dans WDTRAD?

Pour chercher un message dans le cher aché sous WDTRAD, vous pouvez :
trier les messages par ordre alphabétique : cliquez sur l'entête de la colonne.
trier les messages par type de message : cliquez sur l'entête de la colonne "Type".
eectuer un ltre pour acher uniquement les lignes marquées avec une étiquette : cliquez sur le picto
de l'étiquette dans la colonne "Type" et sélectionnez l'étiquette à ltrer. Pour supprimer le ltre,
sélectionnez l'option "Annuler le ltre" dans le menu aché via le picto.
eectuer une recherche simple : cliquez sur l'icône présente dans l'entête de colonne et saisissez le
début du message recherché.
Remarque : Cette recherche peut également être eectuée dans les ressources trouvées dans le
dictionnaire.
utiliser un ltre : faites un clic droit sur la loupe présente dans l'entête de colonne et sélectionnez l'option
"Filtrer" avec la description du ltre. Saisissez dans l'entête de la colonne la condition du ltre : seules les
lignes correspondantes s'acheront dans la table. Pour supprimer le ltre, sélectionnez l'option
"Supprimer le ltre" dans le menu contextuel de la colonne.
faire une recherche avancée : utiliser la combinaison de touches Ctrl + F et saisissez les paramètres de la
recherche :
Le texte à rechercher,
Le texte qui remplacera le texte recherché (si nécessaire),
La langue dans laquelle la recherche doit être eectuée,
Les caractéristiques de la recherche ("mot entier uniquement", "Respecter la casse", "boucler").
Utilisez les boutons "Suivant", "Remplacer", "Remplacer tout" pour eectuer la recherche et les
remplacements.

Pour faire une recherche dans le dictionnaire de WDTRAD, vous pouvez :

```
Utiliser la zone de recherche achée sous la liste des ressources. Il sut de saisir le message recherché,
la langue, et de cliquer sur "Rechercher".
```

```
Utiliser l'onglet "Rechercher" des propriétés du dictionnaire. Pour plus de détails, consultez
Propriétés du dictionnaire.
```
Comment forcer un clavier en saisie de message dans WDTRAD?

La saisie dans une langue dans WDTRAD change automatiquement le clavier et l'alphabet dans ceux de la
langue utilisée. Ce mécanisme permet la saisie dans des langues qui utilisent des claviers et alphabets
spéciques (Russe, Chinois, Japonais, Arabe, Grec, etc.).

Cela a également pour eet de basculer le clavier en QWERTY lors de la saisie d'un texte en anglais. Si vous
désirez saisir vos textes anglais avec un clavier français (AZERTY), vous devez changer le clavier associé à la
langue anglaise dans Windows :

1. Achez les préférences de WDTRAD (option "Edition .. Préférences").
2. Sélectionnez l'option "Activer le changement automatique de langue du clavier", et si nécessaire l'option
    "Installer automatiquement les claviers manquants". Cette option permet d'installer et d'activer les
    claviers manquants.
3. Validez la fenêtre des options de WDTRAD.

Notes

Caractères spéciques dans les messages (librairies du framework, messages de programmation, etc.)

Certains messages comportent :
Des chaînes de caractères de type %s, %1, %2, %1!d!, ...
Ces chaînes de caractères sont utilisées dans des messages paramétrés. A l'exécution, ces chaînes sont
automatiquement remplacées par le nom d'un répertoire, le nom d'un chier, ...
Ces chaînes de caractères ne doivent pas être modiées ou supprimées dans la traduction du message.
Cependant, la position de ces chaînes de caractères peut être modiée.
Par exemple, la traduction en anglais du message "Erreur à la ligne %1!d! du traitement %2." devra être
"Error in process %2, line %1!d!.".
Des chaînes de caractères de type [%xxxx%]
Ces chaînes de caractères sont utilisées dans des messages paramétrés. A l'exécution, ces chaînes sont
automatiquement remplacées par le contenu d'une variable, etc.
Ces chaînes de caractères ne doivent pas être modiées ou supprimées dans la traduction du message. Le
contenu de ces chaînes ne doit pas être traduit. Cependant, la position de ces chaînes de caractères peut
être modiée.
Par exemple, la traduction en anglais du message "Conrmez-vous la création du client : [%sNomClient%]"
devra être "Do you conm the creation of the customer : [%sNomClient%]".


Des chaînes de caractères de type \t, \n, \r.
Ces chaînes de caractères permettent de mettre en forme les messages (tabulation, saut de ligne, etc.).
Ces chaînes de caractères ne doivent pas être modiées ou supprimées dans la traduction du message. Il
est déconseillé de modier la position de ces chaînes de caractères.
Par exemple, la traduction en anglais du message "Impossible d'ouvrir le chier xBase <%1!s!>.\r\nCode
d'erreur renvoyé par la DLL xBase : %2!d!." devra être "Unable to open xBase <%1!s!> le.\r\nError code
returned by xBase DLL: %2!d!.".


## WINDEV WEBDEV

Présentation

Il est possible de congurer les options du dictionnaire de WDTRAD grâce à l'option "Edition .. Propriétés du
dictionnaire". La fenêtre qui s'ache est composée de plusieurs onglets dédockables.

Onglet "Général" : Options disponibles

L'onglet "Général" permet :
d'obtenir des statistiques de traduction sur le dictionnaire en cours
d'eectuer des opérations de maintenance.

Statistiques de traduction

Pour obtenir les statistiques de traduction, cliquez sur le lien "Générer les statistiques du dictionnaire". Ces
statistiques permettent d'obtenir le nombre de ressources présentes dans le dictionnaire.

Maintenance

Les opérations de maintenance sont les suivantes :
Paramétrage de la langue : Pour chaque langue, il est possible de paramétrer les caractéristiques de la
langue : clavier utilisé, symboles. Le paramétrage des symboles est utilisé par WDTRAD lors de la
reconstruction d'une traduction à partir d'une traduction existante.
Pour paramétrer les caractéristiques d'une langue :

1. Sélectionnez la langue voulue.
2. Cliquez sur le bouton. L'onglet "Cla vier" et l'onglet "Symboles" permettent de congurer les
    spécicités de la langue sélectionnée.
Réindexation du dictionnaire : Pour chaque langue, il est possible de réindexer le dictionnaire. Cette
réindexation permet d'optimiser les performances d'accès aux données du dictionnaire. Cette
réindexation peut prendre plusieurs minutes.
Pour réindexer une langue :
1. Sélectionnez la langue voulue.
2. Cliquez sur le bouton "Réindexer" et validez.

Onglet "Terminologies personnalisées" : Options disponibles

```
WINDEV Mobile Autres
```
# Propriétés du dictionnaire


L'onglet "Terminologie" permet de ger des traductions à utiliser pour certains termes. Ces traductions seront
utilisées dès que les termes spéciés seront rencontrés lors d'une traduction automatique réalisée via DeepL
par exemple.

L'option "Synchroniser avec Amazon" permet de stocker les terminologies dans Amazon Translate.

Onglet "Recherche" : Options disponibles

L'onglet "Recherche" permet d'eectuer une recherche spécique dans le dictionnaire.

Il sut de :

1. Sélectionner la langue d'origine et la langue destination.
2. Saisir dans la zone "Recherche" le texte à rechercher dans la langue voulue.
3. Cliquer sur le bouton "Rechercher". Selon les options spéciées, les ressources trouvées sont listées et
    peuvent être modiées.

Remarque : Le menu contextuel de la table des ressources trouvées permet d'ajouter une entrée dans le
dictionnaire (option "Ajouter une entrée dans le dictionnaire").

Onglet "Rechercher / Remplacer" : Options disponibles

L'onglet "Rechercher / Remplacer" permet d'eectuer une recherche et un remplacement dans le
dictionnaire.

Il sut de :

1. Sélectionner la langue dans laquelle la recherche doit être eectuée.
2. Saisir dans la zone "Recherche" le texte à rechercher dans la langue spéciée.
    Remarque : Les caractères * et? peuvent être utilisés. Le caractère ~ permet d'exclure un terme de la
    recherche.
3. Indiquer les options de recherche (casse, commence par, ...).
4. Cliquer sur le bouton "Rechercher". Selon les options spéciées, les ressources trouvées sont listées.
5. Indiquer le texte de remplacement.
6. Eectuer le remplacement :
    Cliquer sur "Remplacer" pour remplacer la ressource sélectionnée.
    Cliquer sur "Remplacer tout" pour remplacer toutes les ressources listées.

Onglet "Ajoutés récemment" : Options disponibles


L'onglet "Ajoutés récemment" permet de lister les dernières ressources ajoutées dans le dictionnaire. Il est
possible de sélectionner les langues voulues ainsi que l'auteur de la traduction. Les 100 dernières ressources
sont achées.


## WINDEV WEBDEV

Présentation

WDTRAD permet d'importer et d'exporter un dictionnaire.

Rappel : Un dictionnaire peut contenir les traductions d'une même ressource en plusieurs langues. Par
exemple, dans le même dictionnaire, l'expression "Fermer l'application" peut être traduite en anglais, en
espagnol et en allemand.

Importer le dictionnaire

WDTRAD permet d'importer :
un dictionnaire existant, correspondant à une version précédente de WDTRAD (inférieure à la version 17).
Au lancement de WDTRAD, si un dictionnaire d'une version précédente est trouvée sur le poste
d'utilisation, cette option est proposée automatiquement.
une mémoire de traduction générée :
par un logiciel de traduction (chier au format TMX).
par WDTRAD (chier au format TMX).
une traduction déjà réalisée avec WDTRAD (chiers au format TXT ou FIC).
un dictionnaire WDTRAD existant (version 18 à 2025).
un dictionnaire local dans un dictionnaire présent sur une plateforme PCSCloud.

Cette fonctionnalité permet d'insérer automatiquement des traductions déjà réalisées dans le dictionnaire
manipulé par WDTRAD.

Pour importer un dictionnaire existant :

1. Sous WDTRAD, sélectionnez l'option "Fichier .. Mémoire de traduction .. Importer une version précédente
    d'un dictionnaire WDTRAD".
2. Sélectionnez le chier ".FIC" correspondant au dictionnaire à importer. Validez.
3. Les nouvelles ressources sont automatiquement insérées dans le dictionnaire manipulé par WDTRAD.
    Les ressources identiques sont automatiquement écrasées.

Pour importer une mémoire de traduction :

1. Sous WDTRAD, sélectionnez l'option "Fichier .. Mémoire de traduction .. Importer dans le dictionnaire".

```
WINDEV Mobile Autres
```
# Importer/Exporter un dictionnaire


2. Sélectionnez au choix :
    le chier ".TMX" correspondant à la mémoire de traduction à importer.
    le chier ".TXT" ou "FIC" correspondant aux chiers déjà traduits dont les ressources doivent être
    importées.
    le chier "DICT.FIC" correspondant à un dictionnaire WDTRAD existant (version 18 à 2025).
3. Les nouvelles ressources sont automatiquement insérées dans le dictionnaire manipulé par WDTRAD.
    Les ressources identiques sont automatiquement écrasées.

Pour importer un dictionnaire local dans un dictionnaire PCSCloud :

1. Sous WDTRAD, connectez-vous à un dictionnaire PCSCloud.
2. Sélectionnez l'option "Fichier .. Mémoire de traduction .. Importer dans le dictionnaire".
3. Sélectionnez le chier "Dictionnaire WDTRAD (DICT.FIC)" correspondant au dictionnaire à importer.
    Validez.
4. Les nouvelles ressources sont automatiquement insérées dans le dictionnaire PCSCloud.
    Les ressources identiques sont automatiquement écrasées.

Remarque : A la première connexion à un dictionnaire PCSCloud, si ce dictionnaire est vide, l'import d'un
dictionnaire local est automatiquement proposé.

Exporter le dictionnaire

WDTRAD permet d'exporter les ressources contenues dans le dictionnaire utilisé. Lors de l'exportation d'un
dictionnaire, un chier mémoire de traduction (chier ".TMX") est créé. Ce chier est créé dans le sous-
répertoire "Dictionnaire" du répertoire d'installation de WDTRAD.

Pour exporter le dictionnaire manipulé par WDTRAD, sélectionnez l'option "Fichier .. Mémoire de
traduction .. Exporter le dictionnaire".


## WINDEV WEBDEV

Présentation

WDTRAD propose deux modes de copie entre les messages extraits et les messages traduits :
copie simple.
copie du message "Traduction" pour tous les messages "Référence" identiques.

Copie simple

Cette méthode permet de copier le message "Référence" en cours dans le message "Traduction"
correspondant.

Pour eectuer une copie simple, cliquez sur le bouton "Copier réf.".

Copie du message "Traduction" pour tous les messages "Référence"
identiques

Cette méthode aecte le message "Traduction" en cours à toutes les autres lignes ayant le même message
"Référence".

Pour eectuer ce mode de copie, cliquez sur le bouton "Reporter trad.".

Ce mode de copie recherche toutes les lignes dont la colonne "Référence" est identique à celle de la ligne en
cours. Le message "Traduction" de la ligne en cours est ensuite aecté à l'ensemble des lignes trouvées.

Par exemple, si la ligne en cours contient le message "Annuler" et sa traduction "Cancel", un clic sur le
bouton "Reporter trad." permet de :

```
rechercher tous les messages "Annuler",
renseigner la traduction "Cancel" pour chacun des messages "Annuler" trouvés.
```
```
WINDEV Mobile Autres
```
# Les diérents modes de copie


Remarque : Si des messages "Traduction" étaient présents dans les messages trouvés, ces messages
"Traduction" sont remplacés avec la nouvelle traduction.


