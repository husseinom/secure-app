# 🔐 Secure App

Application web sécurisée avec authentification JWT et communication HTTPS.

## 🏗️ Architecture

- **Frontend** : Angular + Nginx (HTTPS)
- **Backend** : Express + TypeScript (HTTPS)  
- **Database** : PostgreSQL
- **Admin** : Adminer (interface web)

## 🚀 Lancement rapide

### Prérequis
- Docker et Docker Compose
- Ports libres : 8080, 4000, 5432, 8081

### Installation

```bash
# 1. Cloner le projet
git clone https://github.com/husseinom/secure-app.git
cd secure-app

# 2. Lancer l'application
docker-compose -f docker-compose.db.yml -f docker-compose.prod.yml up --build

# 3. Attendre 1-2 minutes que tous les services démarrent
```

## 🌐 Accès

| Service | URL | Description |
|---------|-----|-------------|
| **Frontend** | https://localhost:8080 | Interface utilisateur |
| **Backend** | https://localhost:4000 | API REST |
| **Adminer** | http://localhost:8081 | Administration DB |

## 👤 Compte Admin par défaut

```
Login: admin
Password: admin
```

## 🛑 Arrêt

```bash
docker-compose -f docker-compose.db.yml -f docker-compose.prod.yml down
```

## 🔧 Base de données (Adminer)

1. Aller sur http://localhost:8081
2. Connexion :
   - **Système** : PostgreSQL
   - **Serveur** : db
   - **Utilisateur** : secureapp  
   - **Mot de passe** : secureapp
   - **Base** : secureapp

## 🔒 Sécurité

- Communication HTTPS
- Authentification JWT
- Headers de sécurité HTTP
- Mots de passe hashés (bcrypt)

---

⚠️ **Certificats SSL auto-signés inclus pour l'évaluation uniquement**
