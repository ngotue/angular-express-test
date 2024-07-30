# Test pour En Voiture Simone

Ce-ci est un test technique pour En Voiture Simone

## Table des matières

- [Prérequis](#prérequis)
- [Installation](#installation)
- [Lancement de l'application](#lancement-de-lapplication)
- [Accès à l'application](#accès-à-lapplication)

## Prérequis

- **Docker:** Assurez-vous d'avoir Docker installé et en cours d'exécution sur votre système. Vous pouvez le télécharger depuis [https://www.docker.com/get-started](https://www.docker.com/get-started).
- **Docker Compose:** Assurez-vous que Docker Compose est installé. Il est souvent fourni avec Docker Desktop pour Windows et macOS. Si ce n'est pas le cas, suivez les instructions d'installation sur [https://docs.docker.com/compose/install/](https://docs.docker.com/compose/install/).
- **Git:** Installez Git si vous avez besoin de cloner des dépôts privés. Vous pouvez le télécharger depuis [https://git-scm.com/](https://git-scm.com/).

## Installation

1. **Clonez les dépôts git :**
   ```bash
   git clone <URL de votre dépôt backend> backend
   mkdir frontend
   cd frontend
   git clone <URL de votre dépôt Angular> client
   
2. **Préparez les fichiers de docker :**
    ```bash
    cd ../
    mv .dockerignore-back ./backend/.dockerignore
    mv Dockerfile.back ./backend
    mv .dockerignore-front ./frontend/.dockerignore
    mv Dockerfile.front nginx.conf ./frontend

## Lancement de l'application
1. **Placez-vous dans le répertoire racine du projet.**
2. **Construisez et démarrez les conteneurs :**
    ```bash
    docker-compose up -d

## Accès à l'application
1. **Frontend (Angular) :** Ouvrez votre navigateur et accédez à ```http://localhost```
2. **Backend (Express) :** Votre API backend devrait être accessible à l'adresse ```http://localhost:3000/api/items```.