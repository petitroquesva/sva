#Création environnement virtuel avec python 3.11

python -m venv C:\Users\LEEF6251\GIT\SVA\venv


#Si besoin de bypasser le proxy:
SET HTTP_PROXY=http://127.0.0.1:3128
SET HTTPS_PROXY=http://127.0.0.1:3128

cd C:\Users\LEEF6251\GIT\SVA

#Activer l'environnement virtuel
.\venv\Scripts\activate

python -m pip install --upgrade pip

#Installation MkDocs
python -m pip install mkdocs

#Installtion du thème Bootswatch pour MkDocs
#https://github.com/mkdocs/mkdocs-bootswatch
#https://bootswatch.com/simplex/

python -m pip install mkdocs-bootswatch

#Installation du plugin Redirects pour MkDocs
#https://github.com/mkdocs/mkdocs-redirects

python -m pip install mkdocs-redirects

#Installation du plugin Mermaid2 pour MkDocs
#https://github.com/fralau/mkdocs-mermaid2-plugin

python -m pip install mkdocs-mermaid2-plugin

#Installation du plugin Mkdocs Blogging Plugin
#https://liang2kl.github.io/mkdocs-blogging-plugin/

python -m pip install mkdocs-blogging-plugin

#Créer le fichier requirements.txt
pip freeze > requirements.txt

#Copier les librairies javascript suivantes pour finaliser l'installation de bootstrap:
cd C:\Users\LEEF6251\GIT\SVA
mkdir custom_theme
cd custom_theme
mkdir js
cd js
#Librairies: jquery.min.js et bootstrap.bundle.min.js


#Lancer MkDocs en mode serve
.\venv\Scripts\mkdocs serve