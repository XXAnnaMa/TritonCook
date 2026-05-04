# 🍳 TritonCook

> A full-stack recipe sharing and discovery platform built for UCSD students to find quick meals based on available ingredients and budget.

![React](https://img.shields.io/badge/React-18-61DAFB?logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript)
![Node.js](https://img.shields.io/badge/Node.js-Express-339933?logo=node.js)
![Firebase](https://img.shields.io/badge/Firebase-Auth%20%26%20Storage-FFCA28?logo=firebase)
![CI](https://img.shields.io/badge/CI-GitHub%20Actions-2088FF?logo=github-actions)

---

## 📖 About

TritonCook helps UCSD students plan meals and manage budgets by recommending recipes based on ingredients they already have. Users can browse, post, like, comment on, and save recipes — all in a clean, responsive interface built for busy students.

---

## ✨ Features

### 🔍 Smart Recipe Search
Search and filter recipes by ingredients, cuisine type, and dietary preferences. Results are ranked based on relevance to available ingredients.

### 📋 Recipe Feed
Browse a live feed of community-posted recipes with full details, images, and interaction options.

### ➕ Post Your Own Recipes
Create and share your own recipes with the community, including ingredients, steps, and photos via Firebase media storage.

### ❤️ Likes & Comments
Engage with the community — like recipes you love and leave comments to share tips or feedback.

### 🔖 Save Favorites
Bookmark recipes to your personal favorites list for quick access later.

### 👤 User Profiles
View and edit your profile, see your posted recipes, and manage your account information.

### 👥 Friends System
Connect with other users, view their profiles, and follow their recipe activity.

### 🔐 Authentication
Secure login and account creation, including Google OAuth via Firebase Authentication.

### 📜 History Tracking
Automatically tracks your recipe browsing history so you can easily revisit what you've seen.

---

## 🛠️ Tech Stack

### Frontend
| Technology | Usage |
|---|---|
| React 18 | UI framework |
| TypeScript | Type-safe development |
| React Context API | Global state management (App, Filter, Recipe contexts) |
| CSS Modules | Component-level styling |

### Backend
| Technology | Usage |
|---|---|
| Node.js + Express | REST API server |
| TypeScript | Type-safe backend logic |
| SQLite | Relational database (via initDatabase) |
| Firebase Auth | Google OAuth + user authentication |
| Firebase Storage | Recipe image uploads |

### DevOps & Testing
| Technology | Usage |
|---|---|
| GitHub Actions | CI/CD pipeline |
| Jest + React Testing Library | Frontend & backend unit tests |
| Babel | Test transpilation |

---

## 📁 Project Structure

```
tritoncook/
├── client/                      # React frontend
│   ├── public/                  # Static assets (icons, images)
│   └── src/
│       ├── components/
│       │   ├── recipes/         # RecipeItem, RecipeList, AddRecipe, FullViewRecipe
│       │   ├── searchpage/      # Search and ingredient-based filtering
│       │   ├── results/         # Search results display
│       │   ├── profilePage/     # User info, edit profile, guest view
│       │   ├── friendsPage/     # Friends list and social features
│       │   ├── navbar/          # Navbar and Sidebar navigation
│       │   ├── loginForm/       # Login and account creation forms
│       │   └── google/          # Google OAuth components
│       ├── context/             # AppContext, FilterContext, RecipeContext
│       ├── utils/               # Helper functions (likes, favorites, posts, history)
│       ├── types/               # Shared TypeScript types
│       ├── data/                # Static data (cuisines, ingredients)
│       └── tests/               # Frontend unit tests
│
└── server/                      # Node.js + Express backend
    └── src/
        ├── api/                 # Google OAuth + login endpoints
        ├── database/            # DB initialization and connection
        ├── endpoints/           # REST endpoints (recipes, likes, favorites, history, users)
        ├── utils/               # Backend business logic utilities
        └── tests/               # Backend unit tests
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- npm or yarn
- Firebase project (for Auth and Storage)

### 1. Clone the repository
```bash
git clone https://github.com/XXAnnaMa/TritonCook.git
cd TritonCook
```

### 2. Set up the frontend
```bash
cd client
npm install
```

Create a `.env` file in `/client`:
```env
REACT_APP_FIREBASE_API_KEY=your_key
REACT_APP_FIREBASE_AUTH_DOMAIN=your_domain
REACT_APP_FIREBASE_PROJECT_ID=your_project_id
REACT_APP_FIREBASE_STORAGE_BUCKET=your_bucket
REACT_APP_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
REACT_APP_FIREBASE_APP_ID=your_app_id
```

Start the frontend:
```bash
npm start
```

### 3. Set up the backend
```bash
cd server
npm install
```

Create a `.env` file in `/server`:
```env
PORT=5000
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
```

Start the backend:
```bash
npm start
```

### 4. Open your browser
Navigate to `http://localhost:3000`

---

## 🧪 Running Tests

**Frontend tests:**
```bash
cd client
npm test
```

**Backend tests:**
```bash
cd server
npm test
```

Test coverage includes: Login, Navbar, NewsFeed, SearchPage, Sidebar (frontend) and Accounts, DisplayedRecipes, Favorites, History, Posts, UserInfo (backend).

---

## 🔄 CI/CD

This project uses **GitHub Actions** for continuous integration. On every push, the pipeline automatically runs all frontend and backend tests to ensure code quality.

---

## 🎨 Key Features Breakdown

| Feature | Description | Status |
|---|---|---|
| Recipe Search | Filter by ingredients & cuisine | ✅ Active |
| Recipe Feed | Browse community recipes | ✅ Active |
| Post Recipes | Create & share with images | ✅ Active |
| Likes & Comments | Social interactions | ✅ Active |
| Save Favorites | Bookmark recipes | ✅ Active |
| User Profiles | View & edit account info | ✅ Active |
| Friends System | Connect with other users | ✅ Active |
| Google OAuth | Sign in with Google | ✅ Active |
| History Tracking | Auto-track browsing history | ✅ Active |

---

## 👩‍💻 Contributors

Built as a collaborative full-stack project. Anna Ma contributed to frontend development, REST API integration, and social features (comments, likes) with Firebase support.

---

## 📝 License

Distributed under the MIT License.

---

*Made with ❤️ for UCSD students*
