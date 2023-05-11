[![cover][cover-src]][cover-href]
[![npm version][npm-version-src]][npm-version-href] 
[![npm downloads][npm-downloads-src]][npm-downloads-href] 
[![bundle][bundle-src]][bundle-href] 
[![License][license-src]][license-href]

> 🔍🌍 Discover the perfect JavaScript environment with Configorium! This powerful package offers lightning-fast detection of the current environment with incredible accuracy. 🕵️‍♂️ Easily tailor your code to the right environment and avoid compatibility issues with the advanced detection capabilities of Configorium. 💪🏼 Take your development to the next level and ensure optimal performance with Configorium!

## 📦 Installation

Install:

```bash
# nyxi
nyxi configorium

# pnpm
pnpm add configorium

# npm
npm install configorium

# yarn
yarn add configorium
```

Import Configorium into your Node.js project:

```ts
// CommonJS
const { read, update, write } = require('configorium')

// ESM
import { read, update, write } from 'configorium'
```

## 💡 Usage

Read/Write config couldn't be easier with Configorium! See the examples below:

**.conf:**

```ts
db.username=db username
db.password=db pass
db.enabled=true
```

**Update config:**

```ts
update({ 'db.enabled': true })
```

Push to an array:

```ts
update({ 'modules[]': 'test' })
```

**Read/Write config:**

```ts
const config = read()
config.enabled = false
write(config)
```

**User Config:**

It is common to keep config in the user's home directory (MacOS: `/Users/{name}`, Linux: `/home/{name}`, Windows: `C:\users\{name}`). Use the following shortcuts for quick access:

```ts
writeUser({ token: 123 }, '.zoorc') // Will be saved in {home}/.zoorc

const conf = readUser('.zoorc') // { token: 123 }
```

## 🔄 Unflatten

Configorium uses [flat](https://www.npmjs.com/package/flat) to automatically flat/unflat when writing and reading rcfile. It allows you to define nested objects using `.` keys. For example:

- `hello.world = true` <=> `{ hello: { world: true }`
- `test.0 = A` <=> `tags: [ 'A' ]`

**Note:** If you want to disable this feature for keys that can override, pass the `flat: true` option.

## 🌟 Native Values

Configorium uses [nyxjason](https://www.npmjs.com/package/nyxjason) to convert values into native JavaScript values. Reading `count=123` results in `{ count: 123 }` (instead of `{ count: "123" }`). To preserve strings as is, you can use quotes like `count="123"`.

## 🚀 Exports

```ts
const defaults: RCOptions
function parse(contents: string, options?: RCOptions): RC
function parseFile(path: string, options?: RCOptions): RC
function read(options?: RCOptions | string): RC
function readUser(options?: RCOptions | string): RC
function serialize(config: RC): string
function write(config: RC, options?: RCOptions | string): void
function writeUser(config: RC, options?: RCOptions | string): void
function update(config: RC, options?: RCOptions | string): RC
function updateUser(config: RC, options?: RCOptions | string): RC
```

**Types:**

```ts
type RC = Record<string, any>
interface RCOptions {
   name?: string
   dir?: string
   flat?: boolean
}
```

**Defaults:**

```ts
{
  name: '.conf',
  dir: process.cwd(),
  flat: false
}
```

### Why Configorium?

Be the first one to guess 🐇 <!-- Hint: do research about rc files history -->

## 📜 License

[MIT](./LICENSE) 💞

<!-- Badges -->

[npm-version-src]: https://img.shields.io/npm/v/dynot?style=flat&colorA=18181B&colorB=14F195
[npm-version-href]: https://npmjs.com/package/configorium
[npm-downloads-src]: https://img.shields.io/npm/dm/configorium?style=flat&colorA=18181B&colorB=14F195
[npm-downloads-href]: https://npmjs.com/package/configorium
[bundle-src]: https://img.shields.io/bundlephobia/minzip/configorium?style=flat&colorA=18181B&colorB=14F195
[bundle-href]: https://bundlephobia.com/result?p=configorium
[license-src]: https://img.shields.io/github/license/nyxblabs/configorium.svg?style=flat&colorA=18181B&colorB=14F195
[license-href]: https://github.com/nyxblabs/configorium/blob/main/LICENSE

<!-- Cover -->
[cover-src]: https://raw.githubusercontent.com/nyxblabs/configorium/main/.github/cover-github-configorium.png
[cover-href]: https://💻nyxb.ws
