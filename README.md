L'ensemble des documents se présente ainsi :
- le script proprement dit (determiner_genre.py),
- une liste de prénoms féminins,
- une liste de prénoms masculins,
- une extraction CSV issue de l'IR 1994 8 des ANMT, qui sert d'exemple.

Le script est prévu pour fonctionner avec Ligeo Gestion, sur un export CSV "Notices (classer > recherche)" qui comprend les XPath suivants :
- identifiant (par défaut dans Ligeo)
- type_c (par défaut dans Ligeo)
- formulaire (par défaut dans Ligeo)
- cote
- intitule

Il est bien sûr adaptable pour d'autres types d'exports, y compris non-issus de Ligeo.
