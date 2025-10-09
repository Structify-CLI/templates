# Structify CLI Templates

This directory contains various templates for creating React projects with organized and standardized structures.

## Available Templates

### ✅ Currently Available

- **react-js-modules** - React template with JavaScript and organized modular structure
- **react-js-swc-modules** - React template with SWC compiler and modular structure
- **react-js-pages-component** - Template for creating individual React components
- **react-js-swc-pages-component** - Template for creating React components with SWC
- **react-ts-pages-component** - Template for creating individual React components with TypeScript
- **react-ts-swc-pages-component** - Template for creating React components with TypeScript and SWC

### 🔄 In Development

- **react-ts-modules** - React template with TypeScript and modular structure
- **react-ts-swc-modules** - React template with TypeScript and SWC compiler

## Template Structure

Each template contains:

- Organized folder structure
- Pre-configured tool settings
- Best practices examples
- Essential configuration files

## Usage

```bash
# Using react-js-modules template
structify create my-project --template react-js-modules
structify create my-swc-project --template react-js-swc-modules
structify create my-component --template react-js-pages-component
structify create my-swc-component --template react-js-swc-pages-component
structify create my-ts-component --template react-ts-pages-component
structify create my-ts-swc-component --template react-ts-swc-pages-component

# Using other templates (coming soon)
structify create my-ts-project --template react-ts-modules
structify create my-ts-swc-modules --template react-ts-swc-modules
```

## Contributing

When adding new templates:

1. Create a new folder with the template name
2. Add the basic structure and files
3. Update this file to include the new template
4. Test the template before publishing

## Notes

- All templates follow modern React standards
- Modular structure helps organize code and ease maintenance
- Each template contains practical usage examples
