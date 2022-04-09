# Config

Config scripts for TypeScript projects

## Script Configurations

- [commitlint-config](./packages/commitlint-config)
- [eslint-config](./packages/eslint-config)
- [eslint-config-react](./packages/eslint-config-react)
- [prettier-config](./packages/prettier-config)
- [stylelint-config](./packages/stylelint-config)
- [tsconfig](./packages/tsconfig)

## Quickstart

### Client
These steps will setup `eslint`, `prettier`, and `stylelint` for a TypeScript React app.

```bash
npm install --save-dev @its-edmund/eslint-config-react @its-edmund/prettier-config @its-edmund/stylelint-config eslint prettier stylelint

yarn add --dev @its-edmund/eslint-config-react @its-edmund/prettier-config @its-edmund/stylelint-config eslint prettier stylelint
```

Add these lines to your `package.json`

```json
"eslintConfig": {
  "extends": "@its-edmund/eslint-config-react"
},
"prettier": "@its-edmund/prettier-config",
"stylelint": {
  "extends": "@its-edmund/stylelint-config"
}
```

To run, add a `lint` script to `package.json`

```json
"scripts": {
  "lint": "eslint src/ --fix; stylelint src/**/*.css --fix; prettier src/ --write"
}
```

### Server
These steps will setup `eslint`, `prettier`, and `tsconfig` for a TypeScript Node app.

```bash
npm install --save-dev @its-edmund/eslint-config @its-edmund/prettier-config @its-edmund/tsconfig eslint prettier

yarn add --dev @its-edmund/eslint-config @its-edmund/prettier-config @its-edmund/tsconfig eslint prettier
```

Add these lines to your `package.json`

```json
"eslintConfig": {
  "extends": "@its-edmund/eslint-config"
},
"prettier": "@its-edmund/prettier-config"
```

Replace your `tsconfig.json` with

```json
"extends": "@its-edmund/tsconfig"
```

To run, add a `lint` script to `package.json`

```json
"scripts": {
  "lint": "eslint src/ --fix; prettier src/ --write"
}
```

## Attribution
Inspired by [jdp-scripts](https://github.com/john-d-pelingo/jdp-scripts) and [hexlabs-config](https://github.com/hackgt/config)

## License

[MIT](LICENSE) &copy; HexLabs