# Vite React Template

This is a starter template with all the basic libraries configured and deployment to GitHub Pages.

## Getting Started

### Installation

```sh
pnpm install
```

### Running the Development Server

```sh
pnpm dev
```

### Extracting Translations

```sh
pnpm translations:extract
```

#### How to Work with [Intl](https://formatjs.io/) Translations

#### Configuration

- The extraction/generation is configured in `/src/lang/processLanguages.js`.
- Set the primary language using `PRIMARY_LOCALE`.
- Add other languages you want to use into `SECONDARY_LOCALES` as locale strings.

##### Basic Translation Creation

- The default message is always in the primary language.
- Ensure IDs are unique.

```ts
const intl = useIntl();
```

```ts
intl.formatMessage({
  id: "hello-world.title",
  defaultMessage: "Hello, world!",
});
```

##### Translation Extraction

- Extraction will gather all the Intl translations throughout the code and export them into `/src/lang/messages/{locale}.json`.
- The primary language file will be filled, while the others will have empty strings as IDs.
- Once you fill the other languages, the translations will persist future extractions.
  Removing a translation from the application will remove it from all translation files during the next extraction.

```sh
pnpm translations:extract
```

## Featured Libraries and Tools

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

## VS Code Extensions

- [Headwind](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
