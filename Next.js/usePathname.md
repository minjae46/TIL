# usePathname

by **next/navigation**

현재 url(pathname)이 무엇인지 확인해주는 hook.

아래와 같이 현재 url에 따라 다른 UI를 보여주는 데 활용할 수 있다.

```js
import { usePathname } from "next/navigation";

const pathname = usePathname();
{
  pathname === "/" ? (
    <SolidHomeIcon className="w-7 h-7" />
  ) : (
    <OutlineHomeIcon className="w-7 h-7" />
  );
}
```
