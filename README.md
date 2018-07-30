# Installation

### Pour OS X / Mac

#### Pré-requis : installation de Python et Mysql
Vous devez avoir installé Python et Mysql sur votre poste. Avant l’installation de Python, vous devez installer le gestionnaire de paquets HomeBrew (équivalent apt-get sous Linux)
Pour installer Homebrew, ouvrez le Terminal et exécutez /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)

Pour installer Python 3 tapez : brew install python3
Maintenant, nous pouvons installer Python 3: brew install python3

Installation virtualenv: pip install virtualenv

#### Installation Mysql: brew install mysql

Avant la première utilisation créez un environnement virtuel pour ne pas modifier l'environnement général de l'ordinateur  
Lancez le dossier projet-erasmus/ dans un terminal et tapez :
virtualenv ~/.erasmus -p python3
Cela crée un environnement virtuel dans lequel pourront être installés les packages utilisés. Pour activer cet environnement virtuel, tapez :
source activate erasmus 
Cette commande sera nécessaire à chaque fois que vous voudrez activer l'environnement virtuel pour utiliser l'application.

Dans le même terminal, tapez :
pip install -r requirements.txt
Cela installe les packages requis pour faire fonctionner l'application.

#### Pour lancer l'application, tapez :
python3 run.py

Utilisations ultérieures :
Lancez le terminal depuis le dossier principal et entrez :
source activate erasmus -> python3 run.py

### Linux (Ubuntu/Debian)
Pré-requis
Vous devez avoir installé MySQL sur votre poste.

Première utilisation
Vous aurez sûrement besoin d'installer python3, virtualenv et pip, pour cela, ouvrez un terminal et tapez :
sudo apt-get install python3 python3-pip python3-virtualenv python3-dev libmysqlclient-dev libfreetype6-dev
puis :
sudo apt install virtualenv

Téléchargez le repository de l'application, lancez le dossier projet-erasmus/ dans un terminal et tapez :
virtualenv ~/.erasmus -p python3
Cela crée un environnement virtuel dans lequel pourront être installés les packages utilisés. Pour activer cet environnement virtuel, tapez :
source ~/.erasmus/bin/activate
Cette commande sera nécessaire à chaque fois que vous voudrez activer l'environnement virtuel pour utiliser l'application.

Dans le même terminal, tapez :
pip install -r requirements.txt
Cela installe les packages requis pour faire fonctionner l'application.

Pour lancer l'application, tapez :
python3 run.py

Utilisations ultérieures :
Lancez le terminal depuis le dossier principal et entrez :
source ~/.erasmus/bin/activate -> python3 run.py

Creation de la base de données "erasmus"
Vous pouvez trouver dans le dossier principal le fichier "datamodel.sql".

Prérequis pour créer la base de données : MySQL installé sur votre ordinateur accès administrateur à cette base de données

En utilisant MySQL Workbench, copiez le contenu du fichier "datamodel.sql" et exécutez-le. La base est installée. Si elle n'apparait pas dans le menu de gauche, faites "refresh".

La base contient beaucoup de données ce qui peut provoquer les problèmes avec Workbench. Pour éviter ces problèmes tapez dans le terminal : mysql -uroot -p < projet-erasmus/datamodel.sql
