Voici la structure du dossier data (dans lequel mettre les dem issus de USGS). Pas besoin de modifier les autres dossiers/fichiers :

data/
├── dem/
    ├── Mali/ (on met ici tous les dem élémentaires associés au Mali)
    ├── BF/ (on met ici tous les dem élémentaires associés au BF)
    ├── etc.
├── pixels/
    ├── Mali/ (on met ici les fichiers Mali_rainfedcropland_ls.tfw et Mali_rainfedcropland_ls.tif envoyés par François)
    ├── etc.
└── results/ (rien à mettre à la main ici)
    ├── temp/ (le script main.py stockera ici les fichiers temporaires)
    Le script main.py stockera ici les fichiers permanents et finaux (map_Mali.csv, map_BF.csv, etc.)


Voici les commandes à écrire dans la console à la racine du projet :

1. Pour créer un environnement python
python -m venv hydro_wb_env 

2. Pour activer l'environnement tout juste crée
Si Windows:
.\hydro_wb_env\Scripts\activate
Si Linux or MacOS:
source hydro_wb_env/bin/activate

3. Pour upgrade pip
Si Windows:
python.exe -m pip install --upgrade pip
Si Linux or MacOS:
python -m pip install --upgrade pip

4. Pour installer les dépendances
pip install -r .\requirements.txt

5. Pour lancer le script qui générera les fichiers csv avec les estimations des profondeurs des nappes pour les 6 pays 
(prévoir plusieurs jours) :
python .\src\main.py

Ce dernier script stocke des fichiers intermédiaires dans data/results/temp/. Si le script plante, vous pouvez le relancer et il 
reprendra normalement où il en était sans créer de doublons.
