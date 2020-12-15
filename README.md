# Projet-Python-2A- Julia Nicolas, Mathilde Kubiak, Clara Le Gallic-Ach 
#### Chargée de TD : Anne Muller 

Ci-dessus, veuillez trouver dans le fichier `Bases de données` toutes les bases utilisées lors de notre travail. Celles-ci sont détaillées dans notre notebook. 
L'une d'elles provient du webscraping du site IMDb, le détail du code est dans notre notebook mais nous vous la fournissons après téléchargement si vous voulez éviter de faire tourner cette cellule. 

## Introduction
A l’heure de la télévision et de la digitalisation de la consommation, quelles ont été les mutations de l'économie du cinéma et de son public ?
Notre étude s'appuiera sur l'analyse de milliers de films sortis entre 1950 et 2020 ainsi que sur des données socio-économiques françaises relatives à l’industrie cinématographique. 
Nous commencerons par faire une étude de la composition et de l'évolution du box office aux Etats-unis. Ensuite nous comparerons cette évolution avec l'évolution française et nous approfondirons en analysant les relations entre box office, fréquentation des cinémas, prix des billets, âges et facteurs socio-économiques. Finalement, nous chercherons à mettre en lumière ce qui fait du cinéma une industrie qui sait, malgré ses mutations, toujours être au cœur des habitudes culturelles des français. 
 
## Définitions 
- **Box-office** : valeur monétaire fondée sur le nombre de ticket écoulés à la sortie d’un film
- **Metascore** : moyenne pondérée des notes attribuées à un film par des critiques internationaux
- **Score imdb** : moyenne des notes attribuées par les visiteurs du site IMDb, le nombre de notes total correspond à la variable nombre de votes dans la base
- **Elasticité prix** : indicateur de la réaction de la demande à la suite d’une variation du prix de 1%
- **Bien ordinaire** : bien dont la consommation diminue lorsque son prix augmente
 
## Outils de travail 
Nos bases de données sont nombreuses mais se divisent en deux catégories : 

- Une base scrapée depuis le site d’IMDb regroupant, après nettoyage, 6658 films de 1950 à 2020 et leurs caractéristiques (Titre, année, durée, genre, réalisateur, score du public sur imbd, metascore, nombre de votes constituant le score du public, chiffre d’affaire généré par la diffusion du film aux USA).

- Des bases récupérées et copiées depuis le site du CNC. Pour ces bases, nous avons feuilleté toutes les bases du CNC concernant les films, leurs public, le streaming, … Quand une information nous intéressait, nous la copions dans un nouveau fichier .csv. 
 
## Lors de notre travail nous avons utilisé des méthodes de :
* Webscraping
* Manipulation des bases de données 
* Statistiques descriptives et visualisation
* One hot encoding des données textuelles
* Régression linéaire
 
## Analyses et conclusions 
Après avoir fait un état des lieux de la base IMDb et constaté une augmentation du chiffre d'affaires annuel moyen des films aux Etats-Unis, nous avons notamment trouvé, en France, une augmentation du chiffre d'affaires des cinémas mais pourtant une baisse de leur fréquentation de 1950 aux années 1990.. 

Nous avons tout d’abord remarqué que le prix du billet augmentait lui aussi chaque année ce qui semble être un frein chez les 15-40 ans sans toucher les populations plus âgées pour qui le billet de cinéma ne peut être assimilé à un bien ordinaire. Nous étions cependant étonnées de découvrir que cette croissance du prix n'impactait pas différemment les différentes classes socio-professionnelles. Par ailleurs, alors que nous pensions que le succès croissant des plateformes de streaming aurait une influence directe sur la fréquentation des cinémas, nous observons que les années 2000 sont synonymes d’une légère reprise du nombre d’entrées qui reste très variable chaque année. Nous avons suggéré que cette reprise pourrait être liée à l’augmentation du nombre de films distribués chaque année, visible à partir des années 1990.
En effet, les français semblent toujours préférer consommer certains genres de films dans une salle de cinéma. Ainsi la fréquentation en salle annuelle sera extrêmement sensible à quelques sorties. En France, les pics de fréquentation des dix à vingt dernières années sont généralement associés à de grosses productions américaines de fantastique/science-fiction/animation, généralement des sagas (Harry Potter, Star Wars, Toy Story, L’age de glace, …) ou bien des comédies françaises qui décrochent toujours des premières places au box-office (Intouchables, Les Tuche, …). 

Finalement, nous observons que le cinéma garde une place centrale dans les habitudes culturelles des français. Bien que l’introduction de télévision dans les années 1960 ait considérablement réduit le temps accordé par les français aux ‘sorties ciné’, la privatisation de celle-ci dans les années 1980 puis l’arrivée du streaming dans les années 2000 n’ont pas enlevé l’envie du public de consommer les films les plus populaires et les plus spectaculaires sur un écran géant.   
 
## Difficultés rencontrées et limites

**Prise en compte de l’inflation** : Pour les Etats-Unis comme pour la France il aurait été plus juste de normaliser le box-office avec l’inflation. Nous avons essayé de le faire “à la main” en utilisant les informations trouvées sur internet ainsi qu’en utilisant le module cpi de python mais nous n’arrivions pas à vérifier la véracité de ces résultats. Nous avons donc préféré traiter les données brutes.
 
**Streaming** : Nous ne disposions que de données concernant le streaming légal, or le streaming illégal existe également. C’est pourquoi nous n’avons pas discuté du streaming en volume mais plutôt de l’usage du streaming en fonction de l'âge et de l’évolution de l’orientation du streaming. Implicitement, nous avons supposé que le streaming illégal représentait une part constante du streaming global.
