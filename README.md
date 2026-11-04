# Project Management App

## Description

Application web de gestion de projets développée avec **React.js** pour le frontend et **Node.js / Express.js** pour le backend.

L'application permet aux utilisateurs de créer des projets, de gérer des tâches et de suivre leur avancement.

Les données sont stockées dans une base de données MySQL.

## Fonctionnalités

- Création et gestion de projets.
- Modification et suppression de projets.
- Création et gestion des tâches.
- Attribution des tâches aux utilisateurs.
- Gestion du statut des tâches (À faire, En cours, Terminée).
- Définition des priorités.
- Consultation de la liste des projets et des tâches.
- Authentification des utilisateurs (si implémentée).

## Technologies utilisées

### Frontend
- **React.js** : création de l'interface utilisateur.
- **Vite** : environnement de développement.
- **React Router DOM** : gestion de la navigation.
- **Axios** : communication avec le backend.
- **CSS** : mise en forme de l'application.

### Backend
- **Node.js** : environnement d'exécution JavaScript.
- **Express.js** : création de l'API REST.
- **MySQL** : gestion de la base de données.
- **mysql2** : connexion entre Node.js et MySQL.
- **dotenv** : gestion des variables d'environnement.
- **cors** : gestion des requêtes entre frontend et backend.

## Architecture du projet

```text
project-management-app/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── package.json
│   └── .env
│
├── backend/
│   ├── config/
│   │   └── database.js
│   ├── controllers/
│   ├── routes/
│   ├── models/
│   ├── server.js
│   ├── package.json
│   └── .env
│
├── database/
│   └── database.sql
│
└── README.md
```

## Prérequis

Avant de lancer le projet, il faut installer :

- Node.js et npm.
- MySQL.
- Git.

## Installation

### 1. Cloner le projet

```bash
git clone https://github.com/username/project-management-app.git
cd project-management-app
```

### 2. Installer le frontend

```bash
cd frontend
npm install
```

### 3. Installer le backend

Dans un autre terminal :

```bash
cd backend
npm install
```

## Dépendances

### Frontend

```bash
npm install react react-dom react-router-dom axios
npm install -D vite @vitejs/plugin-react
```

### Backend

```bash
npm install express mysql2 dotenv cors
npm install -D nodemon
```

## Configuration

### 1. Base de données MySQL

Créer une base de données MySQL :

```sql
CREATE DATABASE project_management;
```

Si un fichier `database.sql` est fourni, importer son contenu dans cette base de données.

### 2. Configuration du backend

Créer un fichier `.env` dans le dossier `backend` :

```env
PORT=5000

DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=project_management
DB_PORT=3306
```

### 3. Configuration du frontend

Créer un fichier `.env` dans le dossier `frontend` :

```env
VITE_API_URL=http://localhost:5000/api
```

## Lancement du projet

### Démarrer le backend

Depuis le dossier `backend` :

```bash
npm run dev
```

Le serveur Express sera accessible sur :

`http://localhost:5000`

### Démarrer le frontend

Depuis le dossier `frontend` :

```bash
npm run dev
```

L'application React sera accessible sur :

`http://localhost:5173`

## Scripts disponibles

### Backend

Dans `backend/package.json` :

```json
{
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js"
  }
}
```

### Frontend

Dans `frontend/package.json` :

```json
{
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  }
}
```

## Base de données

La base de données MySQL contient notamment les tables suivantes :

- **users** : informations des utilisateurs.
- **projects** : informations des projets.
- **tasks** : informations des tâches.

Les relations entre les tables sont gérées à l'aide de clés étrangères.

## API

Le backend expose une API REST permettant au frontend de communiquer avec la base de données.

Exemples de routes :

| Méthode | Route | Description |
|---|---|---|
| GET | `/api/projects` | Récupérer les projets |
| POST | `/api/projects` | Créer un projet |
| PUT | `/api/projects/:id` | Modifier un projet |
| DELETE | `/api/projects/:id` | Supprimer un projet |
| GET | `/api/tasks` | Récupérer les tâches |
| POST | `/api/tasks` | Créer une tâche |
| PUT | `/api/tasks/:id` | Modifier une tâche |
| DELETE | `/api/tasks/:id` | Supprimer une tâche |

##Auteur

Axel

**Technologies :** React.js, Node.js, Express.js et MySQL.
