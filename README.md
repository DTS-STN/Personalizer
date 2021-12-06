This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You will also need to run a local version of the [Personalizer API](https://github.com/DTS-STN/Personalizer-API). Once downloaded create a ```.env``` file in the root directory and add the following:

```
NODE_ENV=dev
PORT=3008
PERSONALIZER_SERVICE_KEY=[PUT SERVICE KEY HERE]
PERSONALIZER_BASE_URL=[PUT BASE URL HERE]
ACCESS_TOKEN_SECRET=[PUT TOKEN HERE]
```

Now run the following command:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3008/api-docs](http://localhost:3008/api-docs) with your browser to see the result.

If you receive an error with the code ```EADDRINUSE``` then the port is in use and needs to be changed. To fix this find an open port and update the ```PORT``` section of the ```.env``` file as seen above.

If you do change the port you will also need to update the ```.env.development``` file in the Personalizer repo as such:

```
NEXT_PUBLIC_API_URL=http://localhost:[NEW PORT HERE]
```

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
