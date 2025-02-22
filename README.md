# @nuxtjs/dayjs

[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier)
[![donate: Patreon](https://img.shields.io/badge/donate-patreon-orange.svg?style=flat-square)](https://www.patreon.com/potato4d)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![NPM version](https://img.shields.io/npm/v/@nuxtjs/dayjs.svg?style=flat-square)](https://npmjs.com/package/@nuxtjs/dayjs)
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors)
[![NPM downloads](https://img.shields.io/npm/dm/@nuxtjs/dayjs.svg?style=flat)](https://npmjs.com/package/@nuxtjs/dayjs)
[![codecov](https://codecov.io/gh/nuxt-community/dayjs-module/branch/master/graph/badge.svg)](https://codecov.io/gh/nuxt-community/dayjs-module)

> The best way for use Day.js easily in your Nuxt.js project.

<a href="https://patreon.com/potato4d">
  <img src="https://c5.patreon.com/external/logo/become_a_patron_button@2x.png" height="50">
</a>

## Installation

```bash
$ yarn add @nuxtjs/dayjs # or npm install
```

## Usage

### 1. Register dayjs module to your Nuxt Application

```js
export default {
  // ...
  modules: [
    '@nuxtjs/dayjs'
  ],

  // Optional
  dayjs: {
    locales: ['en', 'ja'],
    defaultLocale: 'en',
    defaultTimeZone: 'Asia/Tokyo',
    plugins: [
      'utc', // import 'dayjs/plugin/utc'
      'timezone' // import 'dayjs/plugin/timezone'
    ] // Your Day.js plugin
  }
  // ...
}
```

### 2. Use $dayjs on Context, Vue instance

with Context

```html
<script>
export default {
  asyncData({ $dayjs }) {
    return {
      now: $dayjs().format('YYYY/MM/DD')
    }
  }
}
</script>
```

with Vue instance

```html
<script>
export default {
  data() {
    return {
      latestClicked: null
    }
  },
  methods: {
    handleClickButton() {
      this.latestClicked = this.$dayjs().format('YYYY/MM/DD')
    }
  }
}
</script>
```

### For Typescript users

Add the types to your `"types"` array in `tsconfig.json` after the `@nuxt/types` entry.

#### tsconfig.json

```json
{
  "compilerOptions": {
    "types": [
      "@nuxt/types",
      "@nuxtjs/dayjs"
    ]
  }
}
```

## Development

```bash
$ git clone https://github.com/nuxt-community/dayjs-module.git
$ cd @nuxtjs/dayjs
$ yarn
```

## License

MIT @potato4d

## Note

This project generated by [create-nuxt-module](https://github.com/potato4d/create-nuxt-module)

## Contributors

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://potato4d.me"><img src="https://github.com/potato4d.png?s=100" width="100px;" alt=""/><br /><sub><b>Takuma HANATANI(@potato4d)</b></sub></a><br /><a href="https://github.com/nuxt-community/dayjs-module/commits?author=potato4d" title="Code">💻</a> <a href="https://github.com/nuxt-community/dayjs-module/issues?q=author%3Apotato4d" title="Bug reports">🐛</a> <a href="https://github.com/nuxt-community/dayjs-module/commits?author=potato4d" title="Documentation">📖</a> <a href="#example-potato4d" title="Examples">💡</a> <a href="#question-potato4d" title="Answering Questions">💬</a> <a href="https://github.com/nuxt-community/dayjs-module/pulls?q=is%3Apr+reviewed-by%3Apotato4d" title="Reviewed Pull Requests">👀</a></td>
    <td align="center"><a href="https://github.com/bvelastegui"><img src="https://avatars2.githubusercontent.com/u/16880910?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Bryan Daniel Velastegui Lucero</b></sub></a><br /><a href="https://github.com/nuxt-community/dayjs-module/commits?author=bvelastegui" title="Code">💻</a></td>
    <td align="center"><a href="http://resume.a-wei.tw"><img src="https://avatars0.githubusercontent.com/u/19729705?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Wei</b></sub></a><br /><a href="https://github.com/nuxt-community/dayjs-module/commits?author=a65162" title="Code">💻</a></td>
    <td align="center"><a href="https://kazuemon.me"><img src="https://avatars1.githubusercontent.com/u/12812934?v=4?s=100" width="100px;" alt=""/><br /><sub><b>かずえもん</b></sub></a><br /><a href="https://github.com/nuxt-community/dayjs-module/commits?author=kazuemon" title="Documentation">📖</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!
