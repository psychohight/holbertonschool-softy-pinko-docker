# Utiliser l'image Ubuntu la plus récente comme base
FROM ubuntu:latest

# Mettre à jour la liste des paquets disponibles
RUN apt-get update

# Mettre à jour les paquets installés
RUN apt-get upgrade -y

# Installer Python3 et pip3
RUN apt-get install -y python3 python3-pip

# Installer Flask avec pip3
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED
RUN pip3 install flask

# Définir le répertoire de travail sur /app
WORKDIR /app

# Copier le fichier api.py dans l'image Docker
COPY ./api.py /app/api.py

# Commande par défaut pour lancer l'application Flask
CMD ["python3", "api.py"]
