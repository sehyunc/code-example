# Retrieving Pathname in Next.js

Learn how to obtain the pathname of the current URL in Next.js using the `usePathname` hook.

## Quick Steps

1. **Import usePathname**: 
   Import `usePathname` from `next/navigation`:
   ```tsx
   import { usePathname } from 'next/navigation';
   ```

2. **Access Pathname**: 
   Use `usePathname` within a Client Component. Ensure your component is client-side rendered by including `'use client'`:
   ```tsx
   'use client';
   const pathname = usePathname();
   return <p>Path: {pathname}</p>;
   ```

3. **Example Usage**: 
   Display the current pathname in a client component:
   ```tsx
   'use client';
   import { usePathname } from 'next/navigation';
   
   export default function CurrentPath() {
     const pathname = usePathname();
     return <div>Path: {pathname}</div>;
   }
   ```

**Note**: `usePathname` is specifically for Client Components, fitting within the Server Components architecture of Next.js. It's efficient as it doesn't require refetching when navigating, making it a crucial tool for modern web development.