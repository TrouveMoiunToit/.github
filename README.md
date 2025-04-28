# .github
# Trouve Moi Un Toit 🏠

**www.trouvemoiuntoit.com**  
Plateforme web et mobile qui digitalise et simplifie l'accès au logement tout en proposant une gestion immobilière collaborative et moderne.

---

## 🚀 Objectifs

- Faciliter la publication, la recherche et la gestion de logements
- Digitaliser la gestion locative et les paiements
- Intégrer un système collaboratif pour les coopératives d’habitat
- Améliorer l’expérience utilisateur grâce à un espace personnel
- Renforcer les interactions via la messagerie et les avis
- Fournir un support à travers un système de tickets

---

## 👥 Cibles principales

- Locataires
- Propriétaires / Bailleurs
- Agents immobiliers
- Courtiers
- Coopératives d’habitat

---

## 🧩 Fonctionnalités principales

### 🏡 Gestion des Annonces
- Création, modification, suppression
- Ajout de photos/vidéos
- Filtrage avancé (ville, type, prix…)
- Catégories : vente, location, location-vente

### 🏢 Gestion Immobilière
- Paiement en ligne des loyers (Mobile Money, carte bancaire, virement)
- Tableau de bord propriétaire
- Historique des paiements, échéances, reçus PDF
- Relances automatiques ou manuelles

### 🫂 Gestion des Coopératives d’Habitat
- Création d’un espace coopératif (bailleur ou organisation)
- Paiement **par tranche** des membres
- Suivi des engagements de chaque membre
- Gestion des statuts, parts sociales, et échéances
- Reporting spécifique pour la coopérative

### 📨 Communication et Notifications
- Messagerie interne (locataire ↔ bailleur)
- Notifications push : rappels, nouvelles annonces, échéances
- Alertes personnalisées

### 🎫 Système de Tickets (Support)
- Envoi de tickets pour assistance ou réclamations
- Suivi de l’état (ouvert, en cours, résolu)
- Réponses des propriétaires ou du support

### ⭐ Notation et Avis
- Les locataires peuvent noter :
  - Les bailleurs
  - Les courtiers/agents
  - Les annonces
- Commentaires publics modérés par l’admin

### 🔐 Gestion des Comptes
- Rôles : Locataire, Bailleurs, Agents, Coopératives, Admin
- Authentification sécurisée (JWT)
- Gestion des profils et droits d’accès

---

## 🛠️ Stack Technique

| Frontend Web | Mobile        | Backend     | Base de données |
|--------------|---------------|-------------|-----------------|
| Angular      | Flutter       | NestJS      | PostgreSQL      |

---

Utilisateur Mobile (Flutter)
        ↓
API Gateway (AWS API Gateway ou directement via Load Balancer)
        ↓
Serveur Backend (NestJS - Node.js sur EC2)
        ↓
Base de Données (PostgreSQL - RDS ou instance EC2 sécurisée)
        ↓
Système de stockage (AWS S3) pour images, documents justificatifs
        ↓
Notifications Push (Firebase Cloud Messaging - FCM)
        ↓
Paiement Mobile (Intégration Mobile Money / Stripe / PayDunya etc.)
        ↓
Monitoring & Logs (CloudWatch, Sentry)

## ⚙️ Détails d'Infrastructure

| Composant             | Détail                                                                 |
|------------------------|-----------------------------------------------------------------------|
| Serveur API            | EC2 (Ubuntu/Debian) - déploiement du backend NestJS                   |
| Base de données        | PostgreSQL sur AWS RDS    |
| Stockage des fichiers  | AWS S3 (uploads d'images, documents, pièces justificatives)           |
| Load Balancer          | AWS Elastic Load Balancer (facultatif pour montée en charge)           |
| Domaines et SSL        | AWS Route53 + ACM (certificats SSL gratuits)                           |
| Sécurité               | AWS Security Groups, IAM, chiffrement SSL/TLS                         |
| Notifications          | Firebase Cloud Messaging (push notifications pour mobile)             |
| Suivi des erreurs      | AWS CloudWatch Logs + Sentry (optionnel)                               |
| CI/CD                  | GitHub Actions ou AWS CodePipeline pour les déploiements automatiques |
| Sauvegardes BDD        | Snapshots automatiques RDS / Cron Jobs PostgreSQL                     |





