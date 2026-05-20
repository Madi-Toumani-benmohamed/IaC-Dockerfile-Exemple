# IaC-Dockerfile-Exemple


Cette **collection** regroupe plusieurs exemples de Dockerfile simples pour illustrer différentes bonnes pratiques Docker et des cas d’usage courants (application web, multi‑stage build, image utilitaire, etc.). 

## Objectifs du repository

- Montrer des patterns de base pour écrire des Dockerfile propres et reproductibles. 
- Proposer des exemples pour différents types d’applications (web, binaires, scripts, etc.). 
- Servir de support pour des ateliers/TP autour de Docker et de l’Infrastructure as Code. 

## Structure du projet

Le dépôt est organisé en dossiers, chacun contenant un exemple de Dockerfile autonome. 

| Dossier                    | Description rapide                                                                 |
|----------------------------|-------------------------------------------------------------------------------------|
| `Dockerfile-exemple`      | Exemple de base (FROM, RUN, COPY, CMD…) pour découvrir la structure d’un Dockerfile.   |
| `Dockerfile-webapache`    | Conteneur web basé sur Apache (server HTTP simple de démonstration).   |
| `Dockerfile-multi-build`  | Exemple de multi‑stage build pour construire puis alléger l’image finale.   |
| `Dockerfile-bin`          | Image orientée exécution d’un binaire (C, Java, Python… selon l’exemple utilisé).   |
| `Dockerfile-barcode`      | Exemple d’image pour une application de génération/lecture de codes‑barres.   |
| `Dockerfile-User`         | Exemple autour de la gestion d’utilisateur dans le conteneur (USER, permissions).   |

> Les langages utilisés dans les exemples incluent principalement Dockerfile, Java, Python, C et HTML. 

## Prérequis

- Docker installé et fonctionnel sur votre machine (Docker Desktop, Docker Engine, etc.).  
- Accès à Internet si les images de base doivent être téléchargées depuis Docker Hub.  

## Utilisation des exemples

Chaque sous-dossier contient un Dockerfile que vous pouvez construire et lancer indépendamment. 

1. Cloner le dépôt :

```bash
git clone https://github.com/Madi-Toumani-benmohamed/IaC-Dockerfile-Exemple.git
cd IaC-Dockerfile-Exemple
```

2. Se placer dans l’exemple souhaité, par exemple :

```bash
cd Dockerfile-webapache
```

3. Construire l’image :

```bash
docker build -t webapache-exemple .
```

4. Lancer un conteneur :

```bash
docker run --rm -d -p 8080:80 webapache-exemple
```

5. Adapter ensuite les Dockerfile pour vos propres besoins (changer l’image de base, ajouter des dépendances, optimiser les couches, etc.).

 

## Auteur

- Repository maintenu par **Madi Toumani Benmohamed**. 

N’hésitez pas à forker le projet, ouvrir des issues ou proposer des pull requests pour ajouter d’autres exemples de Dockerfile. 
