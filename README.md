# next-pwa

> Next.js plugin for [Progressive Web App](https://developers.google.com/web/progressive-web-apps/)

# Install

```sh
npm install --save-dev next-pwa
```
# Features

- Support build `<ServiceWorker>` Components
- Generate `sw.js` and `workbox.js` powered by `next-workbox-webpack-plugin`
- Generate `manifest.json` serving without extra configuration
- Support more cli options to build PWA like generator icons for PWA

# Usage

```
// ./pages/_document.js
import Document, { Head, Main, NextScript } from 'next/document'
import { ServiceWorker } from 'next-pwa'

export default class PWADocument extends Document {
  render() {
    return (
      <html>
        <Head>
        </Head>
        <body>
          <Main />
          <ServiceWorker />
          <NextScript />
        </body>
      </html>
    )
  }
}
```

# Configuring Next.js

```sh
const withPWA = require('next-pwa')

module.exports = withPWA({
  webpack(config, options) {
    return config
  }
})
```

# License

MIT @ [Jimmy Moon](https://ragingwind.me)
