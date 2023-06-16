---
category: jsx
date: 2023-06-17
---
以下のようなプラグマを記述すれば、そのスクリプト内のみJSXのファクトリー関数を変更できることを知った。

```jsx
/** @jsx h */
import { h } from 'preact';

const div = <div />;

console.log(div);
```

プロジェクト全体ではReactを使用するためにJSXを記述しているが、一部のスクリプトだけReactではない他のモジュールのためにJSXを記述したい、といった場面で有用となりそう。

## Ref

- https://www.typescriptlang.org/tsconfig#jsxFactory
- https://babeljs.io/docs/babel-plugin-transform-react-jsx#customizing-the-classic-runtime-import
