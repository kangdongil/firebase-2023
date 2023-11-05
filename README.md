# When to use Firebase

- 제품의 Prototype 만들기에 적합함
- 규모가 너무 커지면 커스텀 서버로 독립할 필요가 있음

# Create NodeJS Project with Vite

- `npm create vite@latest`
- `React`
- `TypeScript+SWC`

# Check and CleanUp Vite Project

- `npm run dev`
- remove css files and `src/assets/` folder
- `App.tsx`: Remove everything except function `App` and fragment(`<></>`)
- `main.tsx`: Remove import from external file
- `index.html`: Modify <title> and `helment` from <head>

# Install React Development Packages

- `npm i react-router-dom@6.14.2 styled-reset styled-components@6.0.7`
- `npm i @types/styled-components -D`
