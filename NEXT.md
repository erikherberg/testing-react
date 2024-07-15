# libraries

- tailwind
- pnpm
- eslint

# styles

- CSS Modules allow you to scope CSS to a component by automatically creating unique class names
- clsx is a library that lets you toggle class names easily. 
- Next.js automatically optimizes fonts in the application when you use the next/font module

# assets

- next/image component to automatically optimize your images.

# routing

- Next.js uses file-system routing where folders are used to create nested routes. Each folder represents a route segment that maps to a URL segment.
- To create a nested route, you can nest folders inside each other and add page.tsx files inside them.
- In Next.js, you can use a special layout.tsx file to create UI that is shared between multiple pages.
  -> on navigation, only the page components update while the layout won't re-render.
  -> root layout

- <Link> allows you to do client-side navigation with JavaScript.
- Next.js automatically code splits your application by route segments.
  -> If a certain page throws an error, the rest of the application will still work.
  -> Next.js automatically prefetches the code for the linked route in the background
