# vite-plugin-gql

Similar to [graphql-tag/loader](https://github.com/apollographql/graphql-tag#webpack-loading-and-preprocessing), but for [vite](https://github.com/vitejs/vite).
This is an attempt to take the existing plugin vite-plugin-gql, update it to match the latest code in graphql-tag's loader, and get it to work properly in a
vite project. It does seem to compile the graphql files correct but then at runtime will load them all individually, which is very slow, and fail to execute
them properly. PRs against the project are very welcome, and I would very happily give the name of the project over to someone who can make this work properly
with their own plugin.

## Installation

```sh
npm i vite-plugin-gql
```

```sh
yarn add vite-plugin-gql
```

```sh
pnpm i vite-plugin-gql
```

## Usage

```javascript
const gqlPlugin = require('vite-plugin-gql');

const config = {
  plugins: [gqlPlugin],
};
```

Now all the files ends with `.gql` or `.graphql` will be handled by `vite-plugin-gql`.
