This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.js`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

## All installation Sources (&& Steps)

- https://nextjs.org/docs/getting-started

##### Prettier

- https://prettier.io/docs/en/install.html

  - `npm install --save-dev --save-exact prettier`
  - `echo {}> .prettierrc.json`
  - `echo "# Ignore artifacts: \n build \n coverage" > .prettierignore`
  - Add some Files and Dirs from my `.gitignore`
  - `npx prettier --write .`

##### TypeScript

- https://nextjs.org/learn/excel/typescript/create-tsconfig
  - `echo '' > tsconfig.json`
    - https://www.typescriptlang.org/docs/handbook/compiler-options.html
  - `npm install --save-dev typescript @types/react @types/node`
  - `echo '' > next-env.d.ts`
  - update some files suffixes:
    - `mv components/date.js components/date.tsx`
    - `mv components/layout.js components/layout.tsx`
    - `mv lib/posts.js lib/posts.tsx`
    - `mv pages/posts/[id].js pages/posts/[id].tsx`
    - `mv pages/index.js pages/index.tsx`
    - `mv pages/_app.js pages/_app.tsx`
    - `mv pages/api/hello.js pages/api/hello.ts`
- https://nextjs.org/docs/basic-features/typescript
  - `npm run dev`
  - Add 'AppProps' in \_app.tsx:
  - ```import type { AppProps /_, AppContext _/ } from 'next/app'
    import "../styles/globals.css";
    function MyApp({ Component, pageProps }): AppProps {
    return <Component {...pageProps} />;
    }
    export default MyApp;
    ```
  - Update the `hello.ts` Example:
  - ```import type {NextApiRequest, NextApiResponse} from "next";
      type Data = {
      name: string;
      };
      export default (req: NextApiRequest, res: NextApiResponse<Data>) => {
      res.status(200).json({name: "John Doe"});
    };
    ```

##### ESLint

- https://eslint.org/docs/user-guide/getting-started

  - `npm install eslint --save-dev`
  - `npx eslint --init`

    - ✔ How would you like to use ESLint? · `problems`
    - ✔ What type of modules does your project use? · `esm`
    - ✔ Which framework does your project use? · `react`
    - ✔ Does your project use TypeScript? · No / `Yes`
    - ✔ Where does your code run? · `browser`, `node`
    - ✔ What format do you want your config file to be in? · `JSON`
    - SHELL: The config that you've selected requires the following dependencies:
    - SHELL: eslint-plugin-react@latest @typescript-eslint/eslint-plugin@latest @typescript-eslint/parser@latest
    - ✔ Would you like to install them now with npm? · No / `Yes`
    - `npm run prettify`
    - https://github.com/prettier/eslint-config-prettier
    - `npm install --save-dev eslint-config-prettier`
    - Then, add eslint-config-prettier to the "extends" array in your .eslintrc.\* file. Make sure to put it _last_, so it gets the chance to override other configs.
    - e.g.: `"extends": [ "eslint:recommended", "plugin:react/recommended", "plugin:@typescript-eslint/recommended", "prettier" ],`
    - AND add the Rules "react/react-in-jsx-scope": "off" and "@typescript-eslint/explicit-module-boundary-types": "off":
      - `"rules": { "react/react-in-jsx-scope": "off", "@typescript-eslint/explicit-module-boundary-types": "off" }`
    - AND add a Setting Part after the rules ... think of the comma after teh rules Object!!!
      - `"settings": { "react": { "version": "detect" } }`

#### StyleLint

- https://stylelint.io/user-guide/get-started
  - `npm install --save-dev stylelint stylelint-config-standard`
  - `echo '{\n"extends": "stylelint-config-standard"\n}' > .stylelintrc.json`
  - check the installation with: `npx stylelint "**/*.css"`
  - Add a style script `"slint": "stylelint '**/*.css' ",`
- https://github.com/prettier/stylelint-config-prettier
  - `npm install --save-dev stylelint-config-prettier`
  - Then, append stylelint-config-prettier to the extends array in your `.stylelintrc.\*` file. Make sure to put it last, so it will override other configs. ` { "extends": [ "stylelint-config-standard", "stylelint-config-prettier" ] }`
