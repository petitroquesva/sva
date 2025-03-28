######################### GIT repositories ###########################################################
## petitroquesva.github.io: https://github.com/petitroquesva/petitroquesva.github.io.git            ## 
## git remote show origin: https://github.com/petitroquesva/petitroquesva.github.io.git             ##
## SVA: https://github.com/petitroquesva/sva.git                                                    ##
## git remote show origin: https://github.com/petitroquesva/sva.git                                 ##
######################################################################################################
##                                                                                                  ##
## Répertoire bureau: C:\Users\LEEF6251\GIT\SVA                                                     ##
## Répertoire maison: D:\Users\laurf\Documents\Git\SVA                                              ##
##                                                                                                  ##
######################################################################################################

cd C:\Users\LEEF6251\GIT\

mkdir SVA
mkdir petitroquesva.github.io


SVA_HOME_DIR=C:\Users\LEEF6251\GIT\SVA
SVA_HOME_DIR=D:\Users\laurf\Documents\Git\SVA 

cd $SVA_HOME_DIR

#Création environnement virtuel avec python 3.11

python -m venv $SVA_HOME_DIR\venv


#Si besoin de bypasser le proxy:
SET HTTP_PROXY=http://127.0.0.1:3128
SET HTTPS_PROXY=http://127.0.0.1:3128

cd $SVA_HOME_DIR

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
cd $SVA_HOME_DIR
mkdir custom_theme
cd custom_theme
mkdir js
cd js
#Librairies: jquery.min.js et bootstrap.bundle.min.js


#Lancer MkDocs en mode serve
.\venv\Scripts\mkdocs serve

#Déployer le site sur gitHub Pages
cd ..\petitroquesva.github.io\

..\SVA\venv\Scripts\mkdocs gh-deploy --config-file ../SVA/mkdocs.yml --remote-branch master
