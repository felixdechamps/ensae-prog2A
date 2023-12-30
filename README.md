# ensae-prog2A
## Projet Python pour la Data Science
 Auteurs : *Thomas Chen, Félix de Champs, David Premachandra*  

# Sujet :
<div align="justify">
En octobre 2022, le Président de la République avait annoncé la création d’une météo des forêts destinée à mieux informer les Français sur le risque de feux.  
Depuis le 1er juin 2023, tous les jours à 17h, Météo France diffuse donc ce nouveau dispositif pour indiquer le niveau de danger de feux en France métropolitaine. Cette information est établie à partir des prévisions de plusieurs paramètres météorologiques qui influencent fortement le départ et la propagation des feux : pluie, humidité de l’air, température, force du vent et état de sécheresse de la végétation.  
La météo des forêts n’informe pas sur les incendies en cours ou à venir, c’est un outil d’information et de prévention destiné au public. Son objectif est d’indiquer les zones dans lesquelles les conditions météorologiques peuvent aggraver le risque de feux et de rappeler les bons réflexes pour éviter les départs de feux.  
Nous nous sommes donc dit qu'il serait intéressant dans le cadre de ce projet de produire un outil de prévention se rapprochant de ce qui se fait dans le cadre de la météo des forêt. Ainsi, nous nous sommes fixé comme objectif d'étudier l'influence des paramètres climatiques sur la probabilité d'occurrence d’un incendie forestier. Essayer de prédire l'apparition d'un incendie dans la journée en fonction des paramètres météorologiques.

# Problématique : 
Est-il possible de prédire un feu de forêt grâce à des données climatiques ? Quelle est la pertinence d'un tel modèle ?  

# Modèle utilisé : 
Nous avons utilisé principalement la [**régression logistique**](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjQxOfE-raDAxVSTqQEHRVZAgAQFnoECBgQAQ&url=https%3A%2F%2Ffr.wikipedia.org%2Fwiki%2FR%25C3%25A9gression_logistique&usg=AOvVaw0pr6iR-aWOZYLMdamo873p&opi=89978449) qui permet d'estimer la probabilité de la variable cible (ici l'occurence ou non d'un feu de forêt) sachant les variables explicatives i.e ici principalement les variables météorologiques.  

# Données utilisées :
- [BDIFF](https://bdiff.agriculture.gouv.fr/incendies) (Base de Données sur les Incendies de Forêts en France), base de données sur les feux de forêts en france de 2006 à 2022.  
- [Meteonet](https://meteonet.umr-cnrm.fr/), données météo fournies par Météo France toutes les 6 minutes pour 532 stations dans le quart Sud-Est de la France.
- [Base de données sur les communes françaises](https://www.data.gouv.fr/fr/datasets/communes-de-france-base-des-codes-postaux/), contenant notamment leurs coordonnées GPS.
- [Base de données Geojson des forêts françaises](https://transcode.geo.data.gouv.fr/services/5e2a1f74fa4268bc255efbc3/feature-types/ms:PARC_PUBL_FR?format=GeoJSON&projection=WGS84)

- [Base de données Geojson des communes françaises](https://public.opendatasoft.com/explore/dataset/georef-france-commune/information/?disjunctive.reg_name&disjunctive.dep_name&disjunctive.arrdep_name&disjunctive.ze2020_name&disjunctive.bv2022_name&disjunctive.epci_name&disjunctive.ept_name&disjunctive.com_name&disjunctive.ze2010_name&disjunctive.com_is_mountain_area&sort=-com_name&refine.dep_name=Bouches-du-Rh%C3%B4ne) et sur les [régions françaises](https://france-geojson.gregoiredavid.fr/repo/regions.geojson) qui permettent de retracer sur un fond de carte les communes touchées par les incendies.

# Navigation au sein du projet : 
Il suffit d'exécuter successivement les cellules du notebook : [notebookincendie.ipynb](notebookincendies.ipynb)

# Remarque sur la reproductibilité : 
**Attention** à ce que le dossier **ensae-prog2A** ne soit pas dans le **work**, afin que les chemins utilisés pour accéder aux fichiers correspondent bien au code du notebook.

Autres sources : [Ministère de l'écologie](https://www.ecologie.gouv.fr/feux-foret-en-france)