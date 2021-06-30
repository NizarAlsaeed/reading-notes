# React 3

## Next.js, the React Framework
top Next.js features:
- ability use server-side rendering or client-side rendering.
- ability to write some server-side code to connect your React app to your data store.

### Create a Next.js app

`npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn-starter/tree/master/learn-starter"`

### Run the development server
`npm run dev`

>The Next.js development server has Fast Refresh enabled.
When you make changes to files, Next.js automatically applies the changes in the browser almost instantly.

### Navigate Between Pages
In Next.js, a page is a React Component exported from a file in the pages directory.
Pages are associated with a route based on their file name.

### Link Component
In Next.js, you use the Link Component from next/link to wrap the <a> tag. <Link> allows you to do client-side navigation to a different page in the application.

Client-side navigation means that the page transition happens using JavaScript, which is faster than the default navigation done by the browser.

### Code splitting and prefetching
Next.js does code splitting automatically, so each page only loads what’s necessary for that page. That means when the homepage is rendered, the code for other pages is not served initially.

This ensures that the homepage loads quickly even if you have hundreds of pages.

Only loading the code for the page you request also means that pages become isolated. If a certain page throws an error, the rest of the application would still work.

Furthermore, in a production build of Next.js, whenever Link components appear in the browser’s viewport, 
Next.js automatically prefetches the code for the linked page in the background. By the time you click the link, the code for the destination page will
already be loaded in the background, and the page transition will be near-instant!

