# Vite React Template

Starter template with all the basic libs configured and deployment to GitHub Page

## Getting Started

### Installation

```sh
pnpm install
```

### Running dev server

```sh
pnpm install
```

### Extracting translations

```sh
pnpm translations:extract
```

#### How to work with [Intl](https://formatjs.io/) translations

#### Configuration

- The extraction/generation is configured in `/src/lang/processLanguages.js`
- You have to set the primary language `PRIMARY_LOCALE`
- And into `SECONDARY_LOCALES`, write all the other languages you want to use (as a locale strings)

##### Basic translation creation

- Default message is always in the primary language
- ids need to be unique

```ts
const intl = useIntl();
```

```ts
intl.formatMessage({
  id: "hello-world.title",
  defaultMessage: "Hello, world!",
});
```

##### Translation extraction

- Extraction will take all the Intl translations throughout the code and export them into `/src/lang/messages/{locale}.json`
- The file for the primary language will be filled, the other ones will be empty (ids with empty strings)
- Once you fill the other languages, the translations will persist future extractions
- When you remove a translation from the application, it will be removed from all the translation files during the next extraction

```sh
pnpm translations:extract
```

## Featured libs

- [Vite with TypeScript](https://vitejs.dev/)
- [shadcn](https://ui.shadcn.com/)
- [Tailwind](https://tailwindcss.com/)
- [Intl](https://formatjs.io/)
- [React router](https://reactrouter.com/en/main)
- [Tanstack Query](https://tanstack.com/query/latest)
- [Lucide icons](https://lucide.dev/icons/)
- [zod](https://zod.dev/)
- [ESLint](https://www.npmjs.com/package/eslint-plugin-react)
- [Prettier](https://prettier.io/)

## VS Code extensions

- [Headwind](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
