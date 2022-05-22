<p align="center"><img src="https://raw.githubusercontent.com/negezor/vk-io/master/docs/logo.svg?sanitize=true"></p>
<p align="center">
<a href="https://www.npmjs.com/package/vk-io"><img src="https://img.shields.io/npm/v/vk-io.svg?style=flat-square" alt="NPM version"></a>
<a href="https://github.com/negezor/vk-io/actions/workflows/tests.yml"><img src="https://img.shields.io/github/workflow/status/negezor/vk-io/VK-IO CI?style=flat-square" alt="Build Status"></a>
<a href="https://www.npmjs.com/package/vk-io"><img src="https://img.shields.io/npm/dt/vk-io.svg?style=flat-square" alt="NPM downloads"></a>
<a href="https://www.codacy.com/app/negezor/vk-io"><img src="https://img.shields.io/codacy/grade/25ee36d46e6e498981a74f8b0653aacc.svg?style=flat-square" alt="Code quality"></a>
</p>

> **VK-IO** - This is a powerful [Node.js](https://nodejs.org) module that allows you to easily interact with the VK API 🚀

| 📖 [Documentation](https://negezor.github.io/vk-io/) | 🤖 [Examples](docs/examples/) |
| ---------------------------------------------------- | ----------------------------- |

## Features

1. **Complete.** `100%` coverage of the VK API
2. **Simple.** Predictable abstraction of VK API. 1 to 1 mapping of API method
   ```javascript
   vk.api.users.get({...})
   ```
3. **Reliable.** The library is written in **TypeScript** and covered by tests.
4. **Powerful.** Supports following additional features:
   -

## 📦 Installation

> **[Node.js](https://nodejs.org/) 12.20.0 or newer is required**

- **Using `Yarn`** (recommended)
  ```shell
  yarn add vk-io
  ```
- **Using `npm`**
  ```shell
  npm i vk-io
  ```
- **Using `pnpm`**
  ```shell
  pnpm add vk-io
  ```

## Example usage

```javascript
import { VK } from 'vk-io';

const vk = new VK({
	token: process.env.TOKEN
});

async function run() {
	const response = await vk.api.wall.get({
		owner_id: 1
	});

	console.log(response);
}

run().catch(console.log);
```

## Community

### Useful modules that may be useful to you

- [@vk-io/stateless-prompt](packages/stateless-prompt): Simple implementation of stateless prompt
- [@vk-io/authorization](packages/authorization): Authorization by login & password, and etc...
- [@vk-io/streaming](packages/streaming): Receiving data with Streaming API
- [@vk-io/session](packages/session): Simple implementation of the sessions
- [@vk-io/scenes](packages/scenes): Simple implementation of middleware-based scene management
- [@vk-io/hear](packages/hear): Simple implementation of the hears
- [vk-io-question](https://github.com/fakemancat/vk-io-question): Simple promise-based prompt
- [vk-io-pages](https://github.com/MrZillaGold/vk-io-pages): Dynamic pages pagination module
- [henta](https://github.com/u14-team/henta): Simple VK bot engine
- [vk-io-redis-storage](https://github.com/xtcry/vk-io-redis-storage): Simple storage add-on for [@vk-io/session](packages/session)

> If you want to add your module in the list, create a [new issue](https://github.com/negezor/vk-io/issues/new) in the repository.
