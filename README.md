# @ras-sh/typescript-config

Shared TypeScript configuration for [ras.sh](https://ras.sh) projects.

## Installation

```bash
pnpm add -D @ras-sh/typescript-config
```

## Usage

Add the following to your `tsconfig.json` file:

```json
{
  "extends": "@ras-sh/typescript-config/nextjs.json",
  "compilerOptions": {
    ...
  },
  "include": ["**/*.ts", "**/*.tsx"],
  "exclude": ["node_modules"]
}
```

## Available Configurations

- `nextjs.json` - for Next.js projects
- `react-library.json` - for React libraries
- `base.json` - the base configuration

## License

MIT
