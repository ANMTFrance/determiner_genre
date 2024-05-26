Le script nécessite l'installation de l'environnement Python : https://www.python.org/

L'ensemble des documents se présente ainsi :
- le script proprement dit (determiner_genre.py),
- une liste de prénoms féminins en CSV,
- une liste de prénoms masculins en CSV,
- une extraction CSV issue de l'IR 1994 8 des ANMT, qui sert d'exemple.

Le script est prévu pour fonctionner avec Ligeo Gestion (il est adaptable à d'autres SIA), sur un export CSV "Notices (classer > recherche)" qui comprend les XPath suivants :
- identifiant (par défaut dans Ligeo)
- type_c (par défaut dans Ligeo)
- formulaire (par défaut dans Ligeo)
- cote
- intitule

Il est bien sûr adaptable pour d'autres types d'exports, y compris non-issus de Ligeo.

Le script produira, à partir du fichier source, un nouveau fichier qui comportera une colonne supplémentaire "genre". Celle-ci est générée par comparaison du fichier source avec les listes de prénoms. Il y a dans cette nouvelle colonne trois mentions possibles :
- "masculin" : la structure conditionnelle if/elif/else vérifie en premier si le prénom est masculin (et s'arrête là si c'est le cas) ;
- "féminin" : si le prénom n'est pas masculin, la fonction vérifie si le prénom est féminin ;
- "à contrôler" : c'est le dernier cas possible. Il s'agit d'un prénom qui n'est pas dans les listes.

Il est important, dans tous les cas, de procéder à un contrôle par échantillonage à l'oeil humain après production du nouveau fichier.

Le fichier est ensuite réimportable sur Ligeo avec une configuration CSV export/réimport adaptée : XPaths similaires et ajout d'un nouvel XPath qui correspond à l'élément où devra se retrouver la nouvelle information.

Exemple de données traitées par le script : https://recherche-anmt.culture.gouv.fr/archive/recherche/mineursfond/n:85
