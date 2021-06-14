<p align="center">
 <img width="20%" height="20%" src="./logo.svg">
</p>

<br />

> The simple storage implementation with support for Observable and Promise

[![MIT](https://img.shields.io/packagist/l/doctrine/orm.svg?style=flat-square)]()
[![commitizen](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg?style=flat-square)]()
[![PRs](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)]()
[![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier)
[![All Contributors](https://img.shields.io/badge/all_contributors-0-orange.svg?style=flat-square)](#contributors-)
[![ngneat-lib](https://img.shields.io/badge/made%20with-%40ngneat%2Flib-ad1fe3?logo=angular)](https://github.com/ngneat/lib)
[![spectator](https://img.shields.io/badge/tested%20with-spectator-2196F3.svg?style=flat-square)]()
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)


The 'storage' library is dedicated to support various implementation of storage which implements API similar to the 'localStorage.'. The biggest advantage is support for Observable and Promise. It's allow us to add support of the custom persistence manager within following libs: [@ngneat/reactive-forms](https://github.com/ngneat/reactive-forms), [@ngneat/forms-manager](https://github.com/ngneat/forms-manager), [@ngneat/cashew](https://github.com/ngneat/cashew)

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)

## Installation

`ng add @ngneat/storage`

### NPM

`npm install @ngneat/storage --save-dev`

### Yarn

`yarn add @ngneat/storage --dev`


## Usage

By default the library provides LocalStorageManager and SessionStorageManager. It's possible to store the form value into a custom storage. Just implement the PersistManager interface, and use it when calling the upsert function. Storage supports Promise and Observable

```ts
export class StateStoreManager<T> implements PersistManager<T> {
  setValue(key: string, data: T) {
     ...
  }
  getValue(key: string) {
    ...
  }
}
```

Library also export's helper methods and types: 

###Types
- `MaybeAsync` - Type that indicates that value might be Observable or Promise

###Class
- `StorageFacade` - Accepts PersistManager implementation as parameter and implements get and update methods.
  - `get` Return value for the given key
  - `update` - Update storage under specific key using provided callback function.
## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!

<div>Icons made by <a href="https://www.flaticon.com/authors/nhor-phai" title="Nhor Phai">Nhor Phai</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div>
