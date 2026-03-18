# Flamingo UI

Reusable component library for Bitcoin Lightning wallet interfaces.

## Install

```bash
npm install basim-12/flamingo-ui
```

## Usage

### New Wallet UI (STATE-based)

```js
const STATE = require('STATE')
const statedb = STATE(__filename)
statedb.admin()

// Load the wallet module
require('flamingo-ui/src/node_modules/wallet')
```

### Legacy Dev Wallet (full dashboard)

```js
// Just require it — runs immediately
require('flamingo-ui/src/node_modules/dev-wallet')
```

## License

MIT
