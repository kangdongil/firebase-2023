## When to use Firebase

- 제품의 Prototype 만들기에 적합함
- 규모가 너무 커지면 커스텀 서버로 독립할 필요가 있음

## Create NodeJS Project with Vite

- `npm create vite@latest`
- `React`
- `TypeScript+SWC`

## Check and CleanUp Vite Project

- `npm run dev`
- remove css files and `src/assets/` folder
- `App.tsx`: Remove everything except function `App` and fragment(`<></>`)
- `main.tsx`: Remove import from external file
- `index.html`: Modify <title> and `helment` from <head>

## Install React Development Packages

- `npm i react-router-dom@6.14.2 styled-reset styled-components@6.0.7`
- `npm i @types/styled-components -D`

## Configure React-Router-Dom

1. `<RouterProvider>`+`createBrowserRouter` in `App.tsx`

   ```javascript
   import { RouterProvider, createBrowserRouter } from "react-router-dom";

   const router = createBrowserRouter([
      {ROUTER},
      ...
   ])

   function App() {
      <>
         <RouterProvider router={router}>
      </>
   }
   ```

2. Create `components/` and `routes/` folders
3. Describe routes with `dreateBrowserRouter`

   - `App.tsx`

   ```javascript
   {
      path: "/",
      element: <OuterComponent />,
      children: [
         {
            path: "profile",
            element: <InnerComponent />
         }, ...
      ]
   }
   ```

   - `OuterComponent.tsx`

   ```javascript
   import { Outlet } from "react-router-dom";

   export default function layout() {
     return (
       <>
         ...
         <Outlet />
       </>
     );
   }
   ```

   - `InnerComponent.tsx`

   ```javascript
   export default function Home() {
      return ...;
   }
   ```

## Configure Styled-Components

1. Set global style with `createGlobalStyle`

   ```javascript
   import { createGlobalStyle } from "styled-components";
   import reset from "styled-reset";

   const GlobalStyles = createGlobalStyle`
      ${reset};
      * {
         box-sizing: border-box;
      }
      body {
         background-color: black;
         color: white;
         font-family: ~;
      }
   `;

   function App() {
      return (
         <>
            <GlobalStyles />
            <RouterProvider router={router}>
         </>
      );
   }
   ```

2. Define styled component

   ```javascript
   import styled from "styled-components";

   const StyleComponent = styled.div`
     css_property: VALUE;
   `;

   export default function Component() {
     return <StyledComponent>...</StyledComponent>;
   }
   ```
