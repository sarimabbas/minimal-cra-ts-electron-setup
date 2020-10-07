# Minimal CRA (Create React App), TypeScript and Electron setup

- [Minimal CRA (Create React App), TypeScript and Electron setup](#minimal-cra-create-react-app-typescript-and-electron-setup)
  - [Development](#development)
  - [Production](#production)
  - [Citations](#citations)

## Development

Install dependencies

```
yarn
```

Start Electron + React

```
yarn electron:dev
```

## Production

```
yarn electron:build
```

## FAQ

### How to import Electron in renderer process

```js
import React from "react"
const { ipcRenderer } = window.require("electron")
```

### How to hot reload the main process

```bash
yarn add electron-reloader -D
```

```js
// at the top of electron.js
try {
  require("electron-reloader")(module);
} catch (_) {}
```

## Citations

- https://medium.com/@kitze/%EF%B8%8F-from-react-to-an-electron-app-ready-for-production-a0468ecb1da3
- http://people.loyno.edu/~rharvey/teaching/cosc-a319/2019f/converting-cra-to-electron/
