# Opinionated Boilerplate for React Projects with Vite, TypeScript, and Tailwind CSS

[![Node.js][node-version]][node-url]
[![pnpm][pnpm-version]][pnpm-url]
[![React][react-version]][react-url]
[![TypeScript][typescript-version]][typescript-url]
[![Tailwind CSS][tailwindcss-version]][tailwindcss-url]
[![ESLint][eslint-version]][eslint-url]
[![Prettier][prettier-version]][prettier-url]
[![Vite][vite-version]][vite-url]
[![License: MIT][license-shield]][license-url]

## Table of Contents

1. [Introduction and Description](#introduction-and-description)
2. [Prerequisites](#prerequisites)
3. [Local Installation and Setup](#local-installation-and-setup)
4. [Features](#features)
5. Tools and Configurations
   - [ESLint](#eslint-configuration)
   - [Prettier](#prettier-configuration)
   - [Setting Up ESLint and Prettier in VS Code](#setting-up-eslint-and-prettier-in-vs-code)
     - [Recommended VS Code Settings](#recommended-vs-code-settings)
6. [New Component Generator](#new-component-generator)
7. [New Component Source and Modifications](#new-component-source-and-modifications)
8. [Project Structure](#project-structure)
9. [Contributions](#contributions)
10. [License](#license)

## Introduction and Description

Welcome to this opinionated boilerplate for React projects. Designed to streamline your development process, this boilerplate integrates Vite for an optimized build process, TypeScript for scalable and type-safe JavaScript, and Tailwind CSS for utility-first styling. It's thoughtfully configured with a comprehensive set of ESLint rules and Prettier for consistent code formatting, allowing you to focus on building features rather than configuring tools.

## Prerequisites

Before you begin, ensure you have the following installed:

- Node.js (20.10.0 or later)
- `pnpm` for efficient package management

## Local Installation and Setup

Follow these steps to set up and run the project locally using `pnpm`:

1. **Clone the Repository**: Start by cloning the repository to your local machine. Replace `new-directory-name` with the desired name for your project directory. This command clones the repository into a new directory named `new-directory-name` in your current location.

   ```shell
   git clone https://github.com/ucod3/react-vite-typescript-tailwind-boilerplate new-directory-name

   ```

2. **Install pnpm**: If you don't already have pnpm, you can install it globally using npm. This is only needed if you haven't installed pnpm before:

   ```shell
   npm install -g pnpm
   ```

3. **Install Dependencies**: Navigate to the project directory and use pnpm to install the dependencies:

   ```shell
   cd [project-directory]
   pnpm install
   ```

4. **Start the Development Server**: To run the project locally, start the development server with pnpm:

   ```shell
   pnpm run dev
   ```

5. **Access the Project**: The project will be available at `http://localhost:5173` or on another port if this one is in use. Check the terminal output to confirm the port. Open this URL in your browser to view and interact with your project.

## Features

This boilerplate includes the following features:

- [**Vite**](https://vitejs.dev/): Vite is a fast and opinionated build tool that provides a lightning-fast development experience. It's configured to use React Fast Refresh for hot module reloading, allowing you to instantly view changes to your code without having to refresh the page.
- [**TypeScript**](https://www.typescriptlang.org/): TypeScript is a superset of JavaScript that adds static type definitions to the language. It's configured to use the latest version of ECMAScript (2024) and includes support for JSX.
- [**Tailwind CSS**](https://tailwindcss.com/): Tailwind CSS is a utility-first CSS framework that allows you to rapidly build custom designs without leaving your HTML. It's configured to use the Just-in-Time (JIT) compiler for faster builds and includes support for Tailwind UI components.
- [**ESLint**](https://eslint.org/): ESLint is a static code analysis tool that helps you find and fix problems in your JavaScript code. It's configured to use the latest version of ECMAScript (2024) and includes support for React, JSX, security, and best practices.
- [**Prettier**](https://prettier.io/): Prettier is an opinionated code formatter that helps you maintain a consistent code style across your project. It's configured to use the latest version of ECMAScript (2024) and includes support for React, JSX, and TypeScript.

## ESLint Configuration

This project uses ESLint for static code analysis to quickly find and fix problems in your JavaScript code. The configuration includes:

- **Environments**: Browser and ECMAScript 2024 support.
- **Parser**: `@typescript-eslint/parser` for TypeScript linting.
- **Plugins**: ESLint plugins for React, security, and more.
- **Custom Rules**: Specific rules for React components, JSX, security, and best practices.

To modify the ESLint configuration, you can edit the `.eslintrc.cjs` file in the root directory of the project. Please refer to the [ESLint documentation](https://eslint.org/docs/user-guide/configuring/) for more information on configuring ESLint.

## Prettier Configuration

This project uses Prettier for code formatting. The Prettier configuration is set to ensure consistency in code style across the project. The Prettier settings are integrated with ESLint to provide a seamless experience. For specific configurations, refer to the `.prettierrc` file. It is recommend running Prettier as part of your development workflow to maintain consistent coding style.

## Setting Up ESLint and Prettier in VS Code

To ensure a seamless development experience with our project, we recommend installing the following Visual Studio Code extensions:

- [ESLint extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier extension](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

These extensions will help in automatically linting and formatting your code according to the project's configurations.

### Recommended VS Code Settings

After installing these extensions, update your VS Code settings to enhance the linting and formatting experience. You can do this by adding the following configurations to your `settings.json` file in VS Code:

```json
{
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "eslint.probe": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact",
    "markdown"
  ]
}
```

These settings will enable automatic fixing of ESLint issues on file save and ensure ESLint probes the specified file types for linting issues.

To access and edit your settings.json file in VS Code:

Press Ctrl + , (or Cmd + , on Mac) to open Settings.
Click on the {} icon in the top right corner to open the settings.json file.
Add or merge the above configurations into your settings.json file.
Remember, these settings are recommended for a smoother experience with our project and can be adjusted based on your personal preferences or project requirements.

## New Component Generator

This project includes a script for generating new components. You can run this script using the following command:

### Usage Example

To create a new TypeScript component named 'MyComponent':

```bash
pnpm run new-component MyComponent
```

This will create a folder name MyComponent and the following files within it:
MyComponent.tsx
index.ts

## New Component Source and Modifications

The `new-component` used in this project is sourced from [Josh W Comeau's new-component](https://github.com/joshwcomeau/new-component).

Modifications were made to the original `new-component` in `new-component@5.0.2.patch` to better suit the needs of this project. The changes include:

- The default language was changed from JavaScript (`js`) to TypeScript (`ts`).
- The language options were expanded to include JSX (`jsx`).
- The file and index extensions were updated to reflect the chosen language.
- The index template was modified to use a default import and export.
- The component templates for JavaScript and TypeScript were updated to return an empty React fragment (`<></>`) and `null`, respectively, instead of an empty `div`.
- A new template for JSX was added.
- The TypeScript template was updated to include a type for the component's props.

Please refer to `new-component@5.0.2.patch` for the exact changes made.

### Why These Modifications?

Each modification was carefully chosen to enhance the developer experience and align with the TypeScript-centric approach of this boilerplate. For instance, the shift to TypeScript and JSX offers a more type-safe and expressive way to create components.

## Project Structure

```bash
The project structure is as follows:

   ├── patches
   │   └──new-component@5.0.2.patch
   ├── public
   ├── src
   │   ├── assets
   │   ├── components
   │   │   ├── App
   │   │   │   ├── App.tsx
   │   │   │   └── index.ts
   │   │   └── VisuallyHidden
   │   │       ├── VisuallyHidden.module.css
   │   │       ├── VisuallyHidden.tsx
   │   │       └── index.ts
   │   ├── index.css
   │   ├── main.tsx
   │   └── vite-env.d.ts
   ├── .eslintignore
   ├── .eslintrc.cjs
   ├── .gitignore
   ├── .nvmrc
   ├── .prettierrc.cjs
   ├── index.html
   ├── LICENSE.MD
   ├── package.json
   ├── pnpm-lock.yaml
   ├── postcss.config.js
   ├── README.md
   ├── tailwind.config.js
   ├── tsconfig.json
   ├── tsconfig.node.json
   └── vite.config.ts

```

## Contributions

While this project is primarily a personal boilerplate, contributions in the form of feedback, bug reports, or suggestions are welcome. If you have ideas or improvements you'd like to share, please feel free to fork the repository and experiment. Due to the nature of this project as a personal template, direct pull requests might not be merged, but your insights and innovations are valued and can be influential in future updates.

## License

[The MIT License (MIT)](./LICENSE.MD)

<!-- MARKDOWN LINKS & IMAGES -->

[node-version]: https://img.shields.io/badge/Node.js-v21.2.0-10B67F.svg
[node-url]: https://nodejs.org/en/
[pnpm-version]: https://img.shields.io/badge/pnpm-^8.11.0-10B67F.svg
[pnpm-url]: https://pnpm.io/
[react-version]: https://img.shields.io/badge/dynamic/json?url=https://raw.githubusercontent.com/ucod3/react-vite-typescript-tailwind-boilerplate/main/package.json&query=$.dependencies.react&label=React&color=10B67F
[react-url]: https://reactjs.org/
[typescript-version]: https://img.shields.io/badge/dynamic/json?url=https://raw.githubusercontent.com/ucod3/react-vite-typescript-tailwind-boilerplate/main/package.json&query=$.devDependencies.typescript&label=TypeScript&color=10B67F
[typescript-url]: https://www.typescriptlang.org/
[tailwindcss-version]: https://img.shields.io/badge/dynamic/json?url=https://raw.githubusercontent.com/ucod3/react-vite-typescript-tailwind-boilerplate/main/package.json&query=$.devDependencies.tailwindcss&label=Tailwind%20CSS&color=10B67F
[tailwindcss-url]: https://tailwindcss.com/
[eslint-version]: https://img.shields.io/badge/dynamic/json?url=https://raw.githubusercontent.com/ucod3/react-vite-typescript-tailwind-boilerplate/main/package.json&query=$.devDependencies.eslint&label=ESLint&color=10B67F
[eslint-url]: https://eslint.org/
[prettier-version]: https://img.shields.io/badge/dynamic/json?url=https://raw.githubusercontent.com/ucod3/react-vite-typescript-tailwind-boilerplate/main/package.json&query=$.devDependencies.prettier&label=Prettier&color=10B67F
[prettier-url]: https://prettier.io/
[vite-version]: https://img.shields.io/badge/dynamic/json?url=https://raw.githubusercontent.com/ucod3/react-vite-typescript-tailwind-boilerplate/main/package.json&query=$.devDependencies.vite&label=Vite&color=10B67F
[vite-url]: https://vitejs.dev/
[license-shield]: https://img.shields.io/badge/License-MIT-10B67F.svg
[license-url]: ./LICENSE.MD
