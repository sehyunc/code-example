# Retrieving Pathname in Next.js

This guide demonstrates how to obtain the pathname of a current route in Next.js using the `useRouter` hook.

## Quick Steps

1. **Import usePathname**: 
   ```tsx
   import { usePathname } from 'next/navigation';
   ```

2. **Access Pathname**: 
   In your component, use usePathname to access the router object
   ```tsx
   'use client';
   const pathname = usePathname();
   return <p>Path: {pathname}</p>;
   ```

3. **Example Usage**: 
   Display the current pathname:
   ```tsx
   'use client';
   import { usePathname } from 'next/navigation';
   
   const CurrentPath = () => {
     const pathname = usePathname();
     return <div>Path: {pathname}</div>;
   };
   export default CurrentPath;
   ```

**Note**: `usePathname` is specifically for Client Components, fitting within the Server Components architecture of Next.js. It's efficient as it doesn't require refetching when navigating, making it a crucial tool for modern web development.