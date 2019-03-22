# Ramsay's React Boilerplate

Features: 

## Requirements

Node>=9

## Configuration

### WebpackConfig

Webpack configuration is based purely of the `NODE_ENV` that is set when one of the `npm run start` scripts is exectued. Refered to the `package.json` scripts object for the different npm scripts that can be executed.

Shared configuration settings between environments go into `webpack.common.js` and environment-specific settings should go in their respective environment files. 

### App Config

By default, the app config is also determined by using the `NODE_ENV` environment variable. You can tell the application to use a specific config file by adding a `--config` flag like so:

```bash
npm run start --config=localprod.json
```

In the above example, `localprod.json` would be a file inside the `config` directory. Without the `--config` flag, the application loads the `dev.json` config file by default. 

## Development

```bash
npm install
npm run start
```

To start a local server in production mode:
```bash
npm run start:prod --config=localprod.json
```

In the above example, this will look for a `localprod.json` config file in the `config` directory. You can create your own custom config as needed. 

If you want to see the webpack bundle analyzer render in a browser window:
```bash
npm run start:stats
```

## Production



## Testing


## Linting

```bash
npm run lint
```

You can pass a `--fix` flag to automatically fix linting errors, if possible.

```bash
npm run lint --fix
```
