# React Modules-Based Architecture

A React SWC project built with Vite featuring a modular architecture for developing scalable and maintainable applications.

## What is SWC?

SWC stands for **Speedy Web Compiler** and is:

- A fast JavaScript/TypeScript compiler written in Rust
- Up to 20x faster than Babel
- Compatible with most Babel plugins and presets
- Used by major frameworks like Next.js, Parcel, and Vite

## Key Features

### ⚡ Performance

- **20x faster** than Babel in single-threaded scenarios
- **70x faster** when using all CPU cores
- Minimal memory usage
- Built with Rust for maximum performance

### 🔄 Compatibility

- Drop-in replacement for Babel
- Supports most Babel plugins
- Compatible with existing build configurations
- Supports both JavaScript and TypeScript

### 🛠️ Features

- **Transpilation**: ES6+ to ES5, TypeScript to JavaScript
- **Minification**: Code compression and optimization
- **Bundling**: Module bundling capabilities
- **Source Maps**: Full source map support
- **Tree Shaking**: Dead code elimination

## How SWC Works

```javascript
// Input (ES6+/TypeScript)
const greeting = (name: string) => `Hello, ${name}!`;
class MyClass {
  private value = 42;
}

// Output (ES5)
var greeting = function(name) { return "Hello, " + name + "!"; };
var MyClass = function() {
  this.value = 42;
};


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
react-js-swc-modules/
├── public/                 # Static public files
│   └── vite.svg           # Vite icon
├── src/
│   ├── assets/            # Static assets (images, icons)
│   │   └── react.svg
│   ├── constants/         # Global constants and variables
│   │   ├── icons.js       # Icon exports
│   │   ├── images.js      # Image exports
│   │   └── index.js       # Consolidated constants export
│   ├── hooks/             # Shared hooks across the application
│   ├── modules/           # Main application modules
│   │   ├── auth/          # Authentication module
│   │   │   ├── api/       # Authentication API logic
│   │   │   │   └── use-login.js
│   │   │   ├── components/ # Authentication components
│   │   │   │   └── layout.jsx
│   │   │   ├── hooks/     # Authentication-specific hooks
│   │   │   │   └── use-hook.js
│   │   │   └── index.js   # Authentication module exports
│   │   ├── dashboard/     # Dashboard module
│   │   │   ├── api/       # Dashboard API logic
│   │   │   │   └── use-statics.js
│   │   │   ├── components/ # Dashboard components
│   │   │   │   └── layout.jsx
│   │   │   ├── hooks/     # Dashboard-specific hooks
│   │   │   └── index.js   # Dashboard module exports
│   │   ├── another-module/ # Additional module (example)
│   │   │   ├── api/
│   │   │   │   └── use-logic.js
│   │   │   ├── components/
│   │   │   │   └── layout.jsx
│   │   │   ├── hooks/
│   │   │   │   └── use-hook.js
│   │   │   └── index.js
│   │   ├── components/    # Shared components
│   │   │   └── not-found.jsx
│   │   └── index.js       # All modules export
│   ├── routes/            # Routing configuration
│   ├── store/             # Global state management
│   │   └── index.js       # Zustand or any state management setup
│   ├── App.jsx            # Main application component
│   ├── main.jsx           # Application entry point
│   └── index.css          # Global styles
├── eslint.config.js       # ESLint configuration
├── vite.config.js         # Vite configuration
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

## 🛠️ Technologies Used

- **React 19.1.1**: UI library
- **Vite**: Build tool and development server
- **ESLint**: Code quality checking
- **CSS**: Styling

## 📝 Development Guidelines

### Adding a New Module

1. Create a new folder in `/src/modules/`
2. Add subfolders: `api/`, `components/`, `hooks/`
3. Create an `index.js` file to export module contents
4. Add the module to `/src/modules/index.js`

### Adding a New Component

```javascript
// src/modules/[module-name]/components/MyComponent.jsx
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
// src/modules/[module-name]/hooks/useMyHook.js
import { useState, useEffect } from 'react';

export const useMyHook = () => {
    const [data, setData] = useState(null);
    
    // Hook logic
    
    return { data, setData };
};
```

### Adding API Logic

```javascript
// src/modules/[module-name]/api/useMyApi.js
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

## 🤝 Contributing

1. Follow the established folder structure
2. Use clear and descriptive names for files and components
3. Write explanatory comments when needed
4. Follow the established ESLint standards

## 📄 License

This project is open source and available for use and development.
