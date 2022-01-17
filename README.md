![Logo](/logo.svg)
# notion-ga

Proxy server that allows you to track pageview events via google analytics. It uses notion's embed image feature to send pageview event to google analytics.

![](preview.gif)

## How to use?

1. Start notion-ga server and deploy it to the internet world (Optional)
2. Build URL with parameters according to the Parameter reference guide
3. Add embed image to notion pages you want to track. (with the URL you built at the previous step)

## Parameter reference

| Key  | Description                                                   | Example                   | Required |
| ---- | ------------------------------------------------------------- | ------------------------- | -------- |
| tid  | Google Analytics tracking ID. GA4 IDs are not supported. [#7](https://github.com/mskims/notion-ga/issues/7)  | UA-99123456-1             | Y        |
| host | Specifies the hostname. It doesn't matter the specified hostname exists or not. It only appears on your GA dashboard.         | mskim.me                  | Y        |
| Page | The path portion of the page URL. Should begin with `/`       | /careers/product-designer | Y        |

### Example URLs

- https://notion-ga.ohwhos.now.sh/collect?tid=UA-97180334-1&host=mskim.me&page=/careers/product-designer
- https://notion-ga.ohwhos.now.sh/collect?tid=UA-97180334-1&host=mskim.me&page=/careers/data-engineer

## Development

### Requirements

- `Node.js@^8`

### 1. Install dependencies

```bash
$ npm install now@^15 --global
```
NOTE: This has been deprecated but still seems to work as of 17 Jan 2022

### 2. Run development server

```bash
$ now dev
```

### 3. Deploy to the internet world

```bash
$ now
```
## Notes
I forked this from the original author and converted to support Google's new Googla Analytics 4 (GA4) tokens instead of their previous Universal Analytics (UA) tokens.

## LICENSE

MIT
