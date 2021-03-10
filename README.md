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

## All installation Sources

- https://nextjs.org/docs/getting-started
- https://prettier.io/docs/en/install.html

  - `npm install --save-dev --save-exact prettier`
  - `echo {}> .prettierrc.json`
  - `echo "# Ignore artifacts: \n build \n coverage" > .prettierignore`
  - Add some Files and Dirs from my `.gitignore`
  - `npx prettier --write .`

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
    - `mv pages/api/hello.js pages/api/hello.tsx`
- https://nextjs.org/docs/basic-features/typescript
  - `npm run dev`
- ESLINT
