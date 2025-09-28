# 🏧 ATM Management System

Une plateforme moderne de gestion des distributeurs automatiques de billets (ATM) pour la République Démocratique du Congo, développée avec les dernières technologies web.

## 🚀 Fonctionnalités

### 👨‍💼 Pour les Administrateurs
- **Dashboard complet** avec statistiques en temps réel
- **Gestion des utilisateurs** (opérateurs, administrateurs)
- **Gestion géographique** des provinces et communes
- **Vue d'ensemble des ATM** de tous les opérateurs
- **Système de rôles** et permissions avancées

### 🏦 Pour les Opérateurs
- **Gestion personnalisée** de leurs propres ATM
- **Interface intuitive** pour ajouter/modifier/supprimer des ATM
- **Localisation GPS** précise des distributeurs
- **Suivi des informations** techniques (modèle, numéro de série, etc.)

### 🌍 Fonctionnalités Géographiques
- **Couverture complète** de la RDC (26 provinces, 145 communes)
- **Navigation par slug** pour un SEO optimisé
- **Recherche avancée** par province et commune
- **Coordonnées GPS** obligatoires pour chaque ATM

## 🛠️ Technologies Utilisées

### Frontend
- **[Next.js 15](https://nextjs.org/)** - Framework React avec App Router
- **[TypeScript](https://www.typescriptlang.org/)** - Typage statique pour plus de robustesse
- **[Tailwind CSS](https://tailwindcss.com/)** - Framework CSS utilitaire
- **[Shadcn/ui](https://ui.shadcn.com/)** - Composants UI modernes et accessibles
- **[Lucide React](https://lucide.dev/)** - Icônes élégantes et cohérentes

### Backend & Base de Données
- **[Prisma](https://www.prisma.io/)** - ORM moderne pour TypeScript
- **[PostgreSQL](https://www.postgresql.org/)** - Base de données relationnelle robuste
- **[NextAuth.js](https://next-auth.js.org/)** - Authentification sécurisée
- **[bcryptjs](https://www.npmjs.com/package/bcryptjs)** - Hachage des mots de passe

### Outils de Développement
- **[ESLint](https://eslint.org/)** - Linting et qualité du code
- **[PostCSS](https://postcss.org/)** - Transformation CSS
- **[Turbopack](https://turbo.build/pack)** - Bundler ultra-rapide

## 📦 Installation

### Prérequis
- Node.js 18+ 
- PostgreSQL
- npm ou yarn

### Configuration

1. **Cloner le projet**
```bash
git clone https://github.com/allegriakinzola/atm.git
cd atm
```

2. **Installer les dépendances**
```bash
npm install
```

3. **Configuration de l'environnement**
```bash
cp .env.example .env.local
```

Configurer les variables dans `.env.local` :
```env
# Base de données
DATABASE_URL="postgresql://username:password@localhost:5432/atm_db"

# NextAuth
NEXTAUTH_SECRET="your-secret-key"
NEXTAUTH_URL="http://localhost:3000"

# OAuth (optionnel)
GOOGLE_CLIENT_ID="your-google-client-id"
GOOGLE_CLIENT_SECRET="your-google-client-secret"
GITHUB_CLIENT_ID="your-github-client-id"
GITHUB_CLIENT_SECRET="your-github-client-secret"
```

4. **Configuration de la base de données**
```bash
# Générer le client Prisma
npx prisma generate

# Exécuter les migrations
npx prisma migrate dev

# Peupler la base de données
npx prisma db seed
```

5. **Lancer le serveur de développement**
```bash
npm run dev
```

Ouvrir [http://localhost:3000](http://localhost:3000) dans votre navigateur.

## 🗂️ Structure du Projet

```
├── app/                    # App Router de Next.js
│   ├── (public)/          # Pages publiques
│   ├── admin/             # Interface administrateur
│   ├── operateur/         # Interface opérateur
│   └── api/               # API Routes
├── components/            # Composants réutilisables
│   └── ui/                # Composants UI Shadcn
├── lib/                   # Utilitaires et configurations
│   ├── actions/           # Server Actions
│   ├── utils/             # Fonctions utilitaires
│   ├── auth.ts            # Configuration NextAuth
│   └── prisma.tsx         # Client Prisma
├── prisma/                # Schéma et migrations
├── public/                # Assets statiques
└── types/                 # Définitions TypeScript
```

## 🔐 Authentification

Le système supporte plusieurs méthodes d'authentification :
- **Credentials** - Email/mot de passe
- **Google OAuth** - Connexion Google
- **GitHub OAuth** - Connexion GitHub

### Comptes par défaut (après seed)
- **Admin** : `admin@atm.cd` / `admin123`
- **Opérateur** : `operator@atm.cd` / `operator123`

## 🚀 Déploiement

### Vercel (Recommandé)
```bash
npm run build
vercel --prod
```

### Docker
```bash
docker build -t atm-app .
docker run -p 3000:3000 atm-app
```

## 🤝 Contribution

Les contributions sont les bienvenues ! Voici comment contribuer :

1. Fork le projet
2. Créer une branche (`git checkout -b feature/nouvelle-fonctionnalite`)
3. Commit les changements (`git commit -m 'Ajout nouvelle fonctionnalité'`)
4. Push vers la branche (`git push origin feature/nouvelle-fonctionnalite`)
5. Ouvrir une Pull Request

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 👨‍💻 Développeur

**Allegria Kinzola** - Développeur Full Stack passionné de JavaScript 💖

- 🌐 Portfolio: [allegriakinzola.com](https://allegriakinzola.com)
- 📧 Email: contact@allegriakinzola.com
- 💼 LinkedIn: [Allegria Kinzola](https://linkedin.com/in/allegriakinzola)
- 🐙 GitHub: [@allegriakinzola](https://github.com/allegriakinzola)

> "Ma plus grande motivation est de développer des technologies innovantes permettant de résoudre les problèmes quotidiens des êtres humains." ⚡

---

<div align="center">
  <p>Fait avec ❤️ en République Démocratique du Congo</p>
  <p>© 2024 Allegria Kinzola. Tous droits réservés.</p>
</div>
