## ReactJS

### What is Server-Side Rendering (SSR)?

- Pre-render content on the server to improve initial page load times and enhance SEO.

### How to bundle react app? (Webpack or Default?)

### What is code splitting?

- Break down large bundles into smaller chunks to reduce initial load times.

### What is lazy loading?

- It is a technique used to improve the performance by splitting the code into small chunks.
- Load component only when its required instead of loading on initial load.

```jsx linenums="1"
import React, { lazy, Suspense } from "React";

const LazyComponent = lazy(() => import("./LazyComponent"));

function App() {
  return (
    <div>
      <Suspense fallback={<div>Loading...</div>}>
        <LazyComponent />
      </Suspense>
    </div>
  );
}

export default App;
```

### What is suspense in React?

- Lazy loading components are wrapped by Suspense.
- Suspense component receives a fallback prop which is displayed until the lazy loading component in rendered.

### What are higher order components?

- HOC is a function which takes the component as an argument and returns a new component that wraps the original component.

### What is useMemo?

- useMemo is useful for performance optimization.
- It is used to cache the result of a function between re-renders.

## What is useCallback?

- useCallback is useful for performance optimization.
- It is used to cache the function defination between re-renders.

### What are Ref's?

- Ref's are the way to access the dom elements created in the render method.
- They are helpful when we want to update the component without using state and props.

### What are forward ref?

- Forward ref is a technique which is used to send the ref from parent component to one of its children.
- This is helpful when we want to access the child component dom node from the parent component.

```jsx linenums="1"
// ChildComponent.jsx
import React, { forwardRef } from "react";

const ChildComponent = forwardRef((props, ref) => {
    return <input ref={ref} />
})

export default ChildComponent;

// ParentComponent.jsx
import React, { useRef} from "react";
import ChildComponent from "./ChildComponent";

const ParentComponent() {
    const inputRef = useRef(null);

    return (
        <div>
            <ChildComponent ref={inputRef} />
            <button onClick={() => inputRef.current.focus()}>Focus</button>
        </div>
    )
}

export default ParentComponent;
```

### What is props drilling?

- Props drilling is the process of sending the data from one component to other component.

### What are the disadvantages of props drilling?

- **Code complexity**: It make code difficult to read and maintain.
- **Risk of errors**
- **Performance**: Makes application slower.
- We can avoid props drilling by using context api or Redux or any state management libraries.

### What are the different ways to pass data from child component to parent component?

- Callback functions
- Context API
- React Hooks (useRef)
- Redux

## Redux

### What are reducers?

### Is reducer pure function?

### Can we dispatch an action in reducer?
