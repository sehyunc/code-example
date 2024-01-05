# Retrieving Pathname in Next.js

This guide demonstrates how to obtain the pathname of a current route in Next.js using the `useRouter` hook.

## Quick Steps

1. **Import useRouter**: 
   ```tsx
   import { useRouter } from 'next/router';
   ```

2. **Access Pathname**: 
   In your component, use `useRouter` to access the router object, and then extract the `pathname`:
   ```tsx
   const router = useRouter();
   const { pathname } = router;
   ```

3. **Example Usage**: 
   Display the current pathname:
   ```tsx
   const CurrentPath = () => {
     const { pathname } = useRouter();
     return <div>Path: {pathname}</div>;
   };
   export default CurrentPath;
   ```

Remember, `pathname` excludes base path, locale, or trailing slash configurations. It's immediate on the client-side but may require different handling during server-side rendering.