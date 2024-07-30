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

## Installation - une fois cloné ce repo, suivez les étapes suivantes :

1. **Clonez les dépôts git :** Rentrez dans le répertoire de ce repo puis exécutez :
    
   ```bash
   git clone git@github.com:ngotue/test-backend.git backend
   mkdir frontend
   cd frontend
   git clone git@github.com:ngotue/test-frontend.git client
   
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
    ```docker-compose up -d```

    ou dans les nouvelles versions de docker:
    ```docker compose up -d```

    ou en cas de problème de permission, et si applicable:
    ```sudo docker compse up -d```

## Accès à l'application
1. **Frontend (Angular) :** Ouvrez votre navigateur et accédez à ```http://localhost```
2. **Backend (Express) :** Votre API backend devrait être accessible à l'adresse ```http://localhost:3000/api/items```.