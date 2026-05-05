# UCAR Pulse - Plateforme d'Intelligence Institutionnelle

UCAR Pulse est une plateforme moderne de pilotage universitaire pour l'Universite de Carthage. Elle centralise les indicateurs cles, automatise l'analyse des donnees institutionnelles et aide les responsables a prendre des decisions rapides grace a des tableaux de bord, des alertes et un assistant IA contextualise.

## 🚀 Fonctionnalites Cles

### 👥 Pour l'Administration UCAR
- **Centre de Commandement** : Vue consolidee sur les institutions, les KPIs et l'etat global du reseau.
- **Comparaison Multi-Institutions** : Analyse des performances academiques, financieres, RH, recherche et infrastructure.
- **Alertes Intelligentes** : Detection des risques critiques comme le taux d'abandon, l'absenteisme ou la sous-execution budgetaire.
- **Rapports Automatises** : Generation de syntheses mensuelles et de rapports prets pour les reunions.

### 🏫 Pour les Institutions
- **Tableau de Bord Local** : Suivi detaille des donnees propres a chaque etablissement.
- **Gestion des Acces** : Validation des demandes du personnel et controle des roles.
- **Suivi des Processus** : Couverture des domaines academique, finance, RH, recherche, logistique, ESG et partenariats.
- **Importation de Donnees** : Integration des donnees institutionnelles pour alimenter les indicateurs et les analyses.

### 🤖 Pour l'Analyse IA
- **Assistant UCARIA** : Reponses en langage naturel sur les KPIs et les documents institutionnels.
- **RAG avec Citations** : Recuperation d'informations contextualisees avec sources et verdict de verification.
- **Ingestion Multi-Format** : Traitement des PDF, images, documents et tableaux via OCR, parsing et embeddings.
- **Moteur Predictif** : Anticipation des risques et tendances par institution.

## 🛠️ Stack Technique

- **Frontend Principal** : [Next.js](https://nextjs.org/) + [React](https://reactjs.org/)
- **Langage** : [TypeScript](https://www.typescriptlang.org/)
- **Styling** : [Tailwind CSS](https://tailwindcss.com/)
- **Animations** : [Framer Motion](https://www.framer.com/motion/)
- **Graphiques** : [Recharts](https://recharts.org/)
- **Icônes** : [Lucide React](https://lucide.dev/)
- **Base de Donnees & Auth** : [Supabase](https://supabase.com/)
- **Backend IA** : [FastAPI](https://fastapi.tiangolo.com/)
- **Recherche Vectorielle** : [Qdrant](https://qdrant.tech/)
- **Orchestration** : [Docker Compose](https://docs.docker.com/compose/)

## 📦 Installation et Lancement

1. **Cloner le depot** :
   ```bash
   git clone https://github.com/rayenchatti/UCAR-Pulse.git
   cd UCAR-Pulse
   ```

2. **Installer les dependances du frontend principal** :
   ```bash
   npm install
   ```

3. **Configurer les variables d'environnement** :
   Creez un fichier `.env.local` a la racine du projet, puis ajoutez vos cles Supabase et les cles necessaires a l'assistant IA.

4. **Lancer l'application Next.js** :
   ```bash
   npm run dev
   ```

5. **Acceder a l'application** :
   Ouvrez [http://localhost:3000](http://localhost:3000) dans votre navigateur.

### Lancer le module UCARIA

Le dossier `ucaria/` contient le backend IA, l'interface RAG et les services associes.

```bash
cd ucaria
docker compose up -d --build
```

Services principaux :
- **Interface UCARIA** : [http://localhost:5173](http://localhost:5173)
- **API FastAPI** : [http://localhost:8000/docs](http://localhost:8000/docs)

## 📂 Architecture du Projet

```text
src/
├── app/                    # Pages Next.js et routes API
│   ├── dashboard/          # Tableaux de bord, rapports, comparaison, assistant IA
│   ├── login/              # Authentification
│   └── api/chat/           # Endpoint de chat IA
├── components/             # Composants UI reutilisables
├── lib/                    # Donnees, helpers et client Supabase
└── app/globals.css         # Styles globaux

ucaria/
├── api/                    # Backend FastAPI, agents IA, ingestion et retrieval
├── ui/                     # Interface React/Vite du module RAG
└── docker-compose.yml      # Services API, UI et dependances
```

## 🔒 Securite et Gouvernance

UCAR Pulse se base sur une approche multi-role : l'administration centrale dispose d'une vue globale, tandis que chaque institution accede a son propre perimetre. Les donnees sensibles doivent etre configurees via des variables d'environnement et les acces Supabase doivent etre limites selon les roles.

---
Developpe par : [Chatti Mohamed Rayen](https://github.com/rayenchatti)
