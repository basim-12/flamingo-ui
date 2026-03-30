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

statedb.admin()
const { sdb } = statedb(defaults)

const wallet = require('flamingo-ui')

async function start() {
  const [{ sid }] = await sdb.watch(() => { })
  document.body.append(await wallet(sid))
}

start()

function defaults() {
  return {
    drive: { style: {}, data: {}, icons: {} },
    _: {
      'flamingo-ui': { $: '', 0: '', mapping: { style: 'style', data: 'data', icons: 'icons' } }
    }
  }
}
```

### Legacy Dev Dashboard

```js
require('flamingo-ui/src/node_modules/dev-wallet')
```

## License

MIT

## Related Repositories

- [flamingo-node](https://github.com/playproject-io/flamingo-node) — Backend: bitcoind, lightningd, WebSocket bridge
- [flamingo-docker](https://github.com/playproject-io/flamingo-docker) — Docker environment for the stack
- [flamingo-wallet](https://github.com/playproject-io/flamingo-wallet) — Main entry point & orchestration
- [flamingo-ui](https://github.com/playproject-io/flamingo-ui) — Reusable UI component library
