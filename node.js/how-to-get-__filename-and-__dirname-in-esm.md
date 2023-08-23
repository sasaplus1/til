---
category: node.js
date: 2023-08-023
---

node.jsでES Modulesを書いている時に`__filename`や`__dirname`がほしくなる時がある。以下のようにして作ることができる。

```js
import * as path from 'node:path';
import * as url from 'node:url';

const __filename = url.fileURLToPath(import.meta.url);
const __dirname = path.dirname(__filename);

console.log(__dirname, __filename);
```

`url.fileURLToPath` を使用しないとWindows環境で意図しないファイルパスになることがある。
