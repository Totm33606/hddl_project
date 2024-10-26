# Utiliser une image de base pytorch
FROM pytorch/pytorch

# Créer un répertoire de travail
WORKDIR /app

# Copier tous les fichiers dans le workdir
COPY requirements.txt /app 

# Installation des dépendances manquantes
# La commande 'rm' permet de limiter le poids de
# l'image Docker
RUN apt-get update && apt-get install -y build-essential unzip && rm -rf /var/lib/apt/lists/* 

# Installer les dépendances manquantes
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# Exposer le port pour le notebook
EXPOSE 8888