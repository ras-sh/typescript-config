# @ras-sh/typescript-config

⚙️ Shared TypeScript configuration for [ras.sh](https://ras.sh) projects.

## Installation

```bash
pnpm add -D @ras-sh/typescript-config
```

## Usage

Choose the configuration that matches your project type and extend it in your `tsconfig.json`:

### TanStack Start

For TanStack Start applications with file-based routing and server functions:

```json
{
  "extends": "@ras-sh/typescript-config/tanstack-start.json",
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "~/*": ["./src/*"]
    }
  },
  "include": ["**/*.ts", "**/*.tsx"],
  "exclude": ["node_modules", ".output", ".vinxi"]
}
```

### Next.js

For Next.js applications (App Router or Pages Router):

```json
{
  "extends": "@ras-sh/typescript-config/nextjs.json",
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "@/*": ["./*"]
    }
  },
  "include": ["next-env.d.ts", "**/*.ts", "**/*.tsx", ".next/types/**/*.ts"],
  "exclude": ["node_modules", ".next"]
}
```

### React Library

For React component libraries built with bundlers (tsup, Vite, Rollup):

```json
{
  "extends": "@ras-sh/typescript-config/react-library.json",
  "include": ["src/**/*.ts", "src/**/*.tsx"],
  "exclude": ["node_modules", "dist"]
}
```

### Base

For Node.js packages and libraries:

```json
{
  "extends": "@ras-sh/typescript-config/base.json",
  "compilerOptions": {
    "outDir": "dist",
    "rootDir": "src"
  },
  "include": ["src/**/*.ts"],
  "exclude": ["node_modules", "dist"]
}
```

## Available Configurations

- `nextjs.json` - for Next.js projects
- `tanstack-start.json` - for TanStack Start projects
- `react-library.json` - for React libraries
- `base.json` - the base configuration

## License

MIT License - see the [LICENSE](LICENSE) file for details.
