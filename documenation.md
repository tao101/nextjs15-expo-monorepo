# Documentation

## Overview

This project is a monorepo showcasing a cross-platform application built with Next.js for the web and Expo for mobile (iOS and Android). It leverages a shared package for common utilities and components to ensure code reusability and consistency across platforms.

## Project Structure

The project is structured as a monorepo managed with `pnpm`. The main directories are:

- **`apps/`**: Contains the source code for the applications.
  - **`web-app/`**: A web application built with Next.js.
  - **`mobile-app/`**: A mobile application built with Expo (React Native).
- **`shared/`**: Contains shared packages and libraries.
  - **`shared/`**: A shared package containing common code (e.g., utilities, components) used by both `web-app` and `mobile-app`.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (>=18)
- [pnpm](https://pnpm.io/) (>=8)
- [Expo CLI](https://docs.expo.dev/get-started/installation/) (for mobile app development)
- [Yarn](https://yarnpkg.com/) or [npm](https://www.npmjs.com/) (alternatively to pnpm, but pnpm is recommended)

### Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install dependencies using pnpm:
   ```bash
   pnpm install
   ```

### Managing Dependencies

To add platform-specific or shared dependencies:

#### Web Application Dependencies

Add a web-only package

```bash
pnpm add <package-name> --filter web-app
```

#### Mobile Application Dependencies

Add a mobile-only package

```bash
pnpm add <package-name> --filter mobile-app
```

#### Shared Package Dependencies

Add a shared package

```bash
pnpm add <package-name> --filter shared
```

### Running the Applications

#### Web Application

1. Navigate to the `web-app` directory:

   ```bash
   cd apps/web-app
   ```

2. Start the development server:

   ```bash
   pnpm dev
   ```

   or using the root command:

   ```bash
   pnpm dev:web
   ```

3. Open your browser and navigate to [http://localhost:3000](http://localhost:3000).

#### Mobile Application

1. Navigate to the `mobile-app` directory:

   ```bash
   cd apps/mobile-app
   ```

2. Start the Expo development server:

   ```bash
   pnpm start
   ```

   or using the root command:

   ```bash
   pnpm dev:mobile
   ```

3. Follow the instructions in the terminal to run the app on a simulator/emulator or a physical device using the Expo Go app.

#### Running Both Applications Simultaneously

From the root directory, you can run both applications concurrently using:

```bash
pnpm dev
```

### Building the Applications

#### Web Application

```bash
pnpm build:web
```

This command builds the Next.js web application for production. The output will be in the `.next` directory within `apps/web-app`.

#### Mobile Application

```bash
pnpm build:mobile
```

This command builds the Expo mobile application. Refer to the Expo documentation for specific build configurations and platform targets (iOS, Android, web).

## Technologies Used

### Web Application (`web-app`)

- [Next.js](https://nextjs.org/) - React framework for building web applications.
- [React](https://reactjs.org/) - JavaScript library for building user interfaces.
- [TypeScript](https://www.typescriptlang.org/) - Superset of JavaScript that adds static typing.
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS framework.
- [pnpm](https://pnpm.io/) - Package manager.

### Mobile Application (`mobile-app`)

- [Expo](https://expo.dev/) - Framework for building universal React applications.
- [React Native](https://reactnative.dev/) - Framework for building native mobile apps with React.
- [TypeScript](https://www.typescriptlang.org/) - Superset of JavaScript that adds static typing.
- [React Native Reanimated](https://docs.swmansion.com/react-native-reanimated/) - Library for creating smooth animations.
- [Expo Router](https://docs.expo.dev/router/introduction/) - File-based routing for Expo apps.
- [pnpm](https://pnpm.io/) - Package manager.

### Shared Package (`shared`)

- [TypeScript](https://www.typescriptlang.org/) - Superset of JavaScript that adds static typing.

## Shared Code

The `shared` directory is intended for code that is shared between the web and mobile applications. This can include:

- **Utility functions**: Helper functions that are used across both platforms.
- **Components**: React components that can be rendered in both Next.js and React Native environments (with platform-specific adaptations if necessary).
- **Types and interfaces**: Shared type definitions to ensure consistency.

## Deployment

### Web Application

The `web-app` built with Next.js can be deployed to any platform that supports Next.js applications, such as:

- [Vercel](https://vercel.com/) (recommended for Next.js)
- [Netlify](https://www.netlify.com/)
- [AWS Amplify](https://aws.amazon.com/amplify/)
- and more...

Refer to the [Next.js deployment documentation](https://nextjs.org/docs/deployment) for detailed instructions.

### Mobile Application

The `mobile-app` built with Expo can be deployed to app stores (Apple App Store and Google Play Store) and the web using Expo's build and submission services.

Refer to the [Expo documentation on deployment](https://docs.expo.dev/distribution/) for detailed instructions on building and submitting your app.

## Learn More

- **Next.js Documentation**: [https://nextjs.org/docs](https://nextjs.org/docs)
- **Expo Documentation**: [https://docs.expo.dev/](https://docs.expo.dev/)
- **React Native Documentation**: [https://reactnative.dev/docs/](https://reactnative.dev/docs/)
- **TypeScript Documentation**: [https://www.typescriptlang.org/docs/](https://www.typescriptlang.org/docs/)
- **Tailwind CSS Documentation**: [https://tailwindcss.com/docs/](https://tailwindcss.com/docs/)
- **React Native Reanimated Documentation**: [https://docs.swmansion.com/react-native-reanimated/](https://docs.swmansion.com/react-native-reanimated/)
- **Expo Router Documentation**: [https://docs.expo.dev/router/introduction/](https://docs.expo.dev/router/introduction/)
- **pnpm Documentation**: [https://pnpm.io/](https://pnpm.io/)

---

This documentation provides a starting point for understanding and working with this codebase. For more specific details, please refer to the code itself and the documentation of the respective technologies used.
