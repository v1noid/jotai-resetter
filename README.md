<div align="center">
  <a href="https://jotai-resetter.v1noid.com"><img src="https://jotai-resetter.v1noid.com/logo.png" alt="jotai-resetter" width="100"/></a>
  
  [![npm](https://img.shields.io/npm/dt/jotai-resetter.svg)](https://www.npmjs.com/package/jotai-resetter)
  [![GitHub stars](https://img.shields.io/github/stars/v1noid/jotai-resetter.svg)](https://github.com/v1noid/jotai-resetter/stargazers)
</div>

## Jotai Resetter

This package will make it easy for you to reset jotai to it's default values.

Visit our official website: [jotai-resetter.v1noid.com](https://jotai-resetter.v1noid.com)

#### Initialize

First import the `<ResetProvider/>` from `jotai-resetter`, and replace `<Provider/>` from `jotai` with `<ResetProvider/>`

```javascript
// Replace
import { Provider } from "jotai";

<Provider>{/* App */}</Provider>;

// With
import { ResetProvider } from "jotai-resetter";

<ResetProvider>{/* App */}</ResetProvider>;
```

#### How to reset

To reset use the `useResetJotai` hooks it will return the reset function

```javascript
const reset = useResetJotai();

// use reset function to reset jotai
reset();
```

### With Next.js

To use `jotai-resetter` with next.js you have to first make a `CSR` for that

```javascript
// provider.jsx
"use client";
import { ResetProvider } from "jotai-resetter";

export const Provider = ({ children }) => (
  <ResetProvider>{children}</ResetProvider>
);
```

Now use this new `<Provider/>` to wrap your app.

#### Available props

Supports all the native props of `<Provider/>` from `jotai`

That's it now your jotai atoms will be in default state
