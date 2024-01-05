```tsx
import { useRouter } from 'next/router'; // [!code --]
import { usePathname } from 'next/navigation'; // [!code ++]

export default Page() {
  const router = useRouter(); // [!code --]
  const { pathname } = router; // [!code --]
  const pathname = usePathname(); // [!code ++]

  return <div>Current Path: {pathname}</div>;
};

export default Page;
```