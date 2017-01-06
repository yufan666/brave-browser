# browser-laptop-bootstrap
Everything you need to compile [Muon](https://github.com/brave/muon) and run [Brave](https://github.com/brave/browser-laptop)
- fetches syncs code from all projects we define in package.json
  - fetches all 3rd party source code (Chromium) via depot_tools
  - sets the branch for Chromium (ex: 54.0.2840.100)
  - checks out [Muon](https://github.com/brave/muon)
  - checks out [our fork of node](https://github.com/brave/node/tree/chromium54) as a dependency under Muon (along with other deps)
  - checks out [browser-laptop](https://github.com/brave/browser-laptop)
- applies [patches we have](https://github.com/brave/muon/tree/master/patches) for 3rd party code (Chromium, node)

Please [check out our wiki](https://github.com/brave/browser-laptop-bootstrap/wiki) for more in-depth information

## Quick Start

`npm install`

Setup submodule and gclient config:

`npm run init`

Build release:

`npm run build`

Build debug:

`npm run build -- Debug`


To setup `browser-laptop`:

```
cd src/browser-laptop/
npm install
npm run watch
```

To start `browser-laptop` using your debug  build:


`npm start -- Debug`
