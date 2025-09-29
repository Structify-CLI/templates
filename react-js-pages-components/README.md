# React JS Pages & Components

> A Vite + React boilerplate demonstrating a clean structure for pages, components, context, hooks, and services.
> Ideal as a starting point for dashboards, admin panels, or scalable React apps.

---

## 🚀 Technologies Used

* **React 19.1.1** – Core library for building UI components.
* **Vite** – Fast build tool and dev server.
* **React Router (planned in routes/AppRoutes.jsx)** – For page routing.
* **Context API** – Used for global state management (e.g., authentication).
* **Custom Hooks** – Encapsulate logic like authentication and data fetching.
* **ESLint** – For linting and keeping the code style consistent.

---

## 📂 Project Structure

```
react-js-pages-components/
├── .gitignore               # Ignored files for Git
├── eslint.config.js         # ESLint configuration
├── index.html               # App entry HTML
├── package.json             # Dependencies and scripts
├── vite.config.js           # Vite configuration
└── src/
    ├── App.jsx              # Main App component
    ├── main.jsx             # Entry point, renders <App />
    ├── index.css            # Global styles
    │
    ├── assets/              # Static assets (images, icons, etc.)
    │   ├── index.js         # Exports assets
    │   └── react.svg
    │
    ├── components/          # Reusable UI and layout components
    │   ├── dashboard/       # Dashboard widgets
    │   │   ├── RecentActivities.jsx
    │   │   └── StatsOverview.jsx
    │   ├── layout/          # Page layout (shared across pages)
    │   │   ├── Footer.jsx
    │   │   ├── PageHeader.jsx
    │   │   └── Sidebar.jsx
    │   └── ui/              # Basic UI components
    │       ├── Button.jsx
    │       ├── Card.jsx
    │       └── Modal.jsx
    │
    ├── context/             # React Contexts
    │   └── AuthContext.jsx  # Provides authentication state
    │
    ├── hooks/               # Custom React hooks
    │   ├── useAuth.js       # Hook to access AuthContext
    │   └── useFetch.js      # Hook for API requests
    │
    ├── pages/               # Application pages
    │   ├── abouts-us/
    │   │   └── about-us-page.jsx
    │   └── home/
    │       └── home-page.jsx
    │
    ├── routes/              # Centralized app routes
    │   └── AppRoutes.jsx
    │
    ├── services/            # API and business logic
    │   ├── api.js           # Axios/fetch base configs
    │   └── authService.js   # Auth-related API calls
    │
    └── utils/               # Utility functions
        └── formatDate.js    # Helper for date formatting
```

---

## 📘 Explanation of Each Section

* **App.jsx / main.jsx**: Main entry point and root component of the app.
* **components/**:

  * `ui/`: Generic reusable UI elements like buttons and modals.
  * `layout/`: Structural components used across pages (sidebar, header, footer).
  * `dashboard/`: Page-specific widgets for dashboards.
* **context/AuthContext.jsx**: Provides global authentication state using React Context.
* **hooks/**: Encapsulates logic like fetching data or accessing context.
* **pages/**: Contains application screens (home, about-us).
* **routes/AppRoutes.jsx**: Central place to configure app routing.
* **services/**: Handles API integration and business logic.
* **utils/**: Small helpers like date formatting.

---

## 🛠 Development Guidelines

1. **Folder Structure**

   * Keep UI components small and reusable.
   * Place business logic inside `hooks/` or `services/`.
   * Use `pages/` for top-level screens only.
2. **Code Style**

   * Follow ESLint rules.
   * Use functional components with hooks.
   * Keep components clean: separate logic (hooks) from UI (components).
3. **Naming Conventions**

   * Components: `PascalCase` (e.g., `Sidebar.jsx`).
   * Hooks: `camelCase` starting with `use` (e.g., `useAuth.js`).
   * Utilities: `camelCase` (e.g., `formatDate.js`).
4. **Extending the Project**

   * Add new pages inside `src/pages/`.
   * Add new routes in `src/routes/AppRoutes.jsx`.
   * Create new reusable UI elements under `src/components/ui/`.

---

## 📜 License

MIT © structify-CLI