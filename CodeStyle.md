# Code Style Frontend
## JavaScript
- Tab = 2 spaces
- Max line length = 200 characters
- Max file length = 200 lines
- Statement must be terminated
- `if`, `for`, `=` and equality statement must be divided by spaces
```js
if (a === b) {
  c = a;
  for (i = 0; i <= 10; i++) {
    console.log(i);
  }
}
```
- Constants should be capitalise
- Any number should be a constant (except 10^n for division or multiplication and numbers in styles)
- Named import should be in curly bracket with spaces: `import React, { Component } from "react";`
- `require` can be used only for dynamic import
## React Components

For UI components U should have folder `ui`, 
for presentation components - `components`, 
for components with business logic - `containers`

CamelCase for components name (and all class names). 

Folder structure:
<pre>
components
  ConponentName
    index.ts(js)
    styles.ts(js)
</pre>

## Styled Components
```js
import * as UI from 'path';

<UI.Container/>
```

Use api instance

## TypeScript
- Don't use any
- `props` and `state` should be interfaces

## npm / yarn scripts
`dev` - start development server fot local development

`build` - build chunks and static for production stage

`start` - run server for production stage

For local development U should copy all files `<name>.example` and rename them to `<name>`

## Redux
Folder store in src, structure:
<pre>
store
  moduleName
    index.ts(js)
  index.ts(js)  
</pre>
`moduleName` - folder with module reducer, actions, actions creators, middleware. 
Can contain either index file or separate files for reduces, actions, actions creators, middleware, action types.

- Action type should be capitalise.
- Reducer should use switch-case construction
