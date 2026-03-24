# Flamingo UI

Reusable component library for Bitcoin Lightning wallet interfaces.

## Install

```bash
npm install basim-12/flamingo-ui
```

## Usage

### Wallet UI

```js
const STATE = require('STATE')
const statedb = STATE(__filename)
const wallet = require('flamingo-ui')

function defaults () { return { drive: {}, _: {} } }

const { sdb } = statedb(defaults)
const [{ sid }] = sdb.onwatch(() => {})

document.body.append(wallet(sid))
```

### Legacy Dev Dashboard

```js
const dev_wallet = require('flamingo-ui/src/node_modules/dev-wallet')
dev_wallet()
```

## License

MIT

## Related Repositories

- [flamingo-node](https://github.com/playproject-io/flamingo-node) — Backend: bitcoind, lightningd, WebSocket bridge
- [flamingo-docker](https://github.com/playproject-io/flamingo-docker) — Docker environment for the stack
- [flamingo-wallet](https://github.com/playproject-io/flamingo-wallet) — Main entry point & orchestration
- [flamingo-ui](https://github.com/playproject-io/flamingo-ui) — Reusable UI component library
