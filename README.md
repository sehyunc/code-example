```diff
- import { useRouter } from 'next/router';
+ import { usePathname } from 'next/navigation';

const Page = () => {
-  const router = useRouter();
-  const { pathname } = router;
+  const pathname = usePathname();

  return <div>Current Path: {pathname}</div>;
};

export default Page;
```