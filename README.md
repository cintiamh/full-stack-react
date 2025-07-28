# Modern Fullstack React

## VS Code

Extensions:

- Docker (by Microsoft)
- ESLint (by Microsoft)
- Prettier - Code formatter (by Prettier)
- MongoDB for VS Code (by MongoDB)

## Setting up project with Vite

```
$ npm create vite@latest .
```

Start dev:

```
$ npm run dev
```

Dependencies

```
$ npm install --save-dev prettier@latest eslint@latest eslint-plugin-react@latest eslint-config-prettier@latest eslint-plugin-jsx-a11y@latest
```

Run Eslint

```
$ npx eslint src
```

Automatically fix with Eslint

```
$ npx eslint src --fix
```

Adding lint script

```
$ npm pkg set scripts.lint="eslint src"
$ npm run lint
```
