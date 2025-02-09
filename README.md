# Next-Expo Monorepo

A monorepo containing a Next.js web application and Expo React Native mobile application with shared code.

## Project Structure

    ├── apps/
    │ ├── mobile-app/ # Expo React Native app (file-based routing)
    │ └── web-app/ # Next.js 15 application
    ├── shared/ # Shared utilities between web and mobile
    ├── package.json # Root workspace config
    └── pnpm-workspace.yaml # Monorepo configuration

## Features

- 🚀 Cross-platform development (iOS, Android, Web)
- ♻️ Shared code between mobile and web (see `shared/utils/generateRandomId.ts`)
- 📦 Modern monorepo setup with PNPM workspaces

## Prerequisites

- Node.js 20+
- PNPM 10+
- iOS/Android simulators (for mobile development)

## Package Management

This monorepo uses PNPM workspaces. To install packages for specific parts of the project:

```bash
pnpm install --filter <package-name>
```

**Web app only** (Next.js):

```bash
pnpm install --filter web-app
```

**Mobile app only** (Expo):

```bash
pnpm install --filter mobile-app
```

**Shared library only**:

```bash
pnpm install --filter shared
```

## Getting Started

1. **Install dependencies**

```bash
pnpm install
```

2. **Run the mobile app (Expo)**

```bash
pnpm dev:mobile
```

3. **Run the web app (Next.js)**

```bash
pnpm dev:web
```

3. **Open apps:**

- Mobile: Scan QR code in Expo Go app or use simulator
- Web: http://localhost:3000

## Learning Resources

- [Expo Documentation](https://docs.expo.dev/)
- [Next.js Documentation](https://nextjs.org/docs)
- [React Native Web](https://necolas.github.io/react-native-web/)
- [PNPM Workspaces](https://pnpm.io/workspaces)
