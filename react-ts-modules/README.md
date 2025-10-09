# React Modules-Based Architecture

A React project built with Vite + Typescript featuring a modular architecture for developing scalable and maintainable applications.

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Lint code
npm run lint
```

## 📁 Project Structure

``` text
react-ts-modules/
├── public/                # Static public files
│   └── vite.svg           # Vite icon
├── src/
│   ├── assets/            # Static assets (images, icons)
│   │   └── react.svg
│   ├── constants/         # Global constants and variables
│   │   ├── icons.ts       # Icon exports
│   │   ├── images.ts      # Image exports
│   │   └── index.ts       # Consolidated constants export
│   ├── hooks/             # Shared hooks across the application
│   ├── modules/           # Main application modules
│   │   ├── auth/          # Authentication module
│   │   │   ├── api/       # Authentication API logic
│   │   │   │   └── use-login.ts
│   │   │   ├── components/ # Authentication components
│   │   │   │   └── layout.tsx
│   │   │   ├── hooks/     # Authentication-specific hooks
│   │   │   │   └── use-hook.ts
│   │   │   └── index.ts   # Authentication module exports
│   │   ├── dashboard/     # Dashboard module
│   │   │   ├── api/       # Dashboard API logic
│   │   │   │   └── use-statics.ts
│   │   │   ├── components/ # Dashboard components
│   │   │   │   └── layout.tsx
│   │   │   ├── hooks/     # Dashboard-specific hooks
│   │   │   └── index.ts   # Dashboard module exports
│   │   ├── another-module/ # Additional module (example)
│   │   │   ├── api/
│   │   │   │   └── use-logic.ts
│   │   │   ├── components/
│   │   │   │   └── layout.tsx
│   │   │   ├── hooks/
│   │   │   │   └── use-hook.ts
│   │   │   └── index.ts
│   │   ├── components/    # Shared components
│   │   │   └── not-found.tsx
│   │   └── index.ts       # All modules export
│   ├── routes/            # Routing configuration
│   ├── store/             # Global state management
│   │   └── index.ts       # Zustand or any state management setup
│   ├── App.tsx            # Main application component
│   ├── main.tsx           # Application entry point
│   └── index.css          # Global styles
├── eslint.config.ts       # ESLint configuration
├── vite.config.ts         # Vite configuration
├── package.json           # Project info and dependencies
└── README.md              # This file
```

## 🏗️ Project Architecture

### Feature-Based Architecture

The project is divided into separate modules, each containing:

- **api/**: API logic and data handling
- **components/**: Module-specific components
- **hooks/**: Custom hooks for the module
- **index.js**: Module export file

### Main Directories

#### `/src/constants`

Contains all constants used throughout the application:

- Icons and images
- Static text
- Application configuration

#### `/src/modules`

Main application modules:

- **auth**: Everything related to authentication (login, register, etc.)
- **dashboard**: Dashboard and statistics
- **components**: Shared components between modules

#### `/src/store`

Global state management using Zustand or Redux

#### `/src/routes`

Routing configuration and pages

#### `/src/types`

Type definitions for the application

## 🛠️ Technologies Used

- **React 19.1.1**: UI library
- **Vite**: Build tool and development server
- **ESLint**: Code quality checking
- **CSS**: Styling
- **TypeScript**: Typed JavaScript

## 📝 Development Guidelines

### Adding a New Module

1. Create a new folder in `/src/modules/`
2. Add subfolders: `api/`, `components/`, `hooks/`
3. Create an `index.ts` file to export module contents
4. Add the module to `/src/modules/index.ts`

### Adding a New Component

```javascript
// src/modules/[module-name]/components/MyComponent.tsx
import React from 'react';

export const MyComponent = () => {
    return (
        <div>
            {/* Component content */}
        </div>
    );
};
```

### Adding a Custom Hook

```javascript
// src/modules/[module-name]/hooks/useMyHook.ts
import { useState, useEffect } from 'react';

export const useMyHook = () => {
    const [data, setData] = useState(null);
    
    // Hook logic
    
    return { data, setData };
};
```

### Adding API Logic

```javascript
// src/modules/[module-name]/api/useMyApi.ts
export const useMyApi = () => {
    const fetchData = async () => {
        // API call logic
    };
    
    return { fetchData };
};
```

## 🎯 Features

- Organized and scalable modular structure
- Separation of concerns
- Easy maintenance and development
- Code reusability
- Clear file and folder organization
- Consistent naming conventions

## 🤝 Contributing

1. Follow the established folder structure
2. Use clear and descriptive names for files and components
3. Write explanatory comments when needed
4. Follow the established ESLint standards

## 📄 License

This project is open source and available for use and development.
