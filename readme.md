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

•For UI components U should have folder `ui`, 
for presentation components - `components`, 
for components with business logic - `containers`.

•CamelCase for components name (and all class names). 

•Folder structure:
<pre>
components
  ComponentName
    index.ts(js)
    styles.ts(js)
</pre>

•Props should be desctructed:
```
import React from 'react';

//For functional components

const SmallComponent = ({ title, value }) => {};
// or
const BigComponent = props => {
  const {
    title,
    value,
    options,
    onClick,
    onChange
  } = props;
};

//For classes

class ClassComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  
  handleChange() {
    const { value } = this.props;
    onChange(value);
  }
};

```

## Styled Components
```js
import * as UI from './styles';

<UI.Container />
```

We have mixin-helpers *smaller* and *bigger* for adaptive layout and colors constants in almost all projects.

## TypeScript
- Don't use any
- `props` and `state` should be interfaces:

```
import { Component } from 'react';

interface IComponentProps = {
  // ...
}

interface IComponentState = {
  // ...
}

class Component<IComponentProps, IComponentState> extends Component {
  // ...
}
```

## npm / yarn scripts

For `next`-based projects:

•`dev` - start development server fot local development

•`build` - build chunks and static for production stage

•`start` - run server for production stage

For local development you should copy all files `<name>.example` and rename them to `<name>`

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

Use api instance

## GIT
•Every task must be in branch named as task number, like `AIZHKNDSUP-699`.

•Commit message must describe what you have did in this commit (this is obvious, but someone forget it).

•Commit message must contain the task number. If you stick to the first paragraph, it's easy to use [pre-commit-message git-hook](https://gist.github.com/bartoszmajsak/1396344)
