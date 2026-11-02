<img width="100%" src="https://alova.js.org/img/cover.jpg" />

<p align="center">
  <strong>The unit of a request isn't a call, it's a scenario.</strong><br/>
  <em>alova is a fullstack request strategy library, organizing request logic into ready-to-use request strategies.</em>
</p>

<p align="center">
  <a href="https://alova.js.org">Documentation</a> | 
  <a href="https://alova.js.org/examples">Demos</a>
</p>

## What is alova

alova (pronounced /əˈləʊva/) is a **fullstack request strategy library**. It treats a request as a scenario with a lifecycle — not a one-time instantaneous call — and organizes the request logic you've hand-written countless times, such as pagination, forms, uploads, and authentication, as well as server-side logic like retries, verification services and BFF, into ready-made **request strategies**.

You don't have to throw away the axios or fetch you already know: alova builds right on top of your existing request library and takes over the request logic you keep rewriting. The same API set runs across React, Vue, Svelte, Solid, mini-programs and the server, so you learn it once and use it everywhere.

You can read the backstory in [Why alova was created](https://alova.js.org/about/faqs), and learn how alova differs in [Comparison with other request libraries](https://alova.js.org/about/comparison).

## Why use alova

### 1. What you get is a complete scenario, not just a working request

In the AI Coding era, what sets applications apart is user experience — not that AI isn't capable enough, but that your prompt is unlikely to spell out the following request features, because no one has ever handed you a checklist for how to manage your requests. For example:

- **Input debounce**: without it, fast typing fires requests back to back
- **Cache hits for identical conditions**: without it, the same endpoint is called over and over
- **Discarding stale responses**: without it, an older response may overwrite a newer one
- **Automatic retry on failure**: without it, a single failed request leaves the page blank
- **Next-page preloading**: without it, users stare at the loading state on every page turn
- ...

[RSM (Request Scenario Model)](https://alova.js.org/tutorial/getting-started/rsm) is exactly that checklist — alova maps it onto the configuration options of the scenario hooks.

### 2. No need to review AI-written code

Request-layer code takes up a large share of your pages, and AI-written code always needs another round of review. With alova, the request layer is reduced to configuration you only need to verify — saving you time while improving stability.

## Features

- Easy to use, [watch the video](https://alova.js.org/video-tutorial) to get started in 5 mins.
- Client request strategies: `usePagination` / `useForm` / `useUploader` / `useSSE` / `useWatcher` / `useFetcher` / `useCaptcha` / `useSQRequest` and more — see the [Request Strategy List](https://alova.js.org/tutorial/client/strategy).
- Server request strategies: `atomize` / `retry` / `createRateLimiter` and more — see [server hooks](https://alova.js.org/tutorial/server/strategy).
- One API set spans React, Vue, Svelte, Solid, mini-programs and Node.js / Deno / Bun, fully compatible with your favorite HTTP clients and UI frameworks.
- Request sharing and multi-level cache, end-to-end type safety, for better app performance.
- Advanced OpenAPI solution `worma`: from one OpenAPI spec, generate type-safe calling code, TypeScript types, full API docs, and API knowledge for your AI coding assistant.
- Building with an AI coding assistant? Install alova's [Agent Skills](https://alova.js.org/tutorial/getting-started/agent-skills) so your agent writes code following official best practices.

## Is there any difference?

Unlike `@tanstack/react-query` and `swr`, which abstract requests as **data synchronization** (unit: query), alova abstracts a request as a **scenario** (unit: scenario). That is a definitional difference, not a matter of how many features each has.

In a piece of request code, the "execution" is usually just one line — axios / fetch are enough for that. What actually takes time is the trigger timing, whether to really send this time, and what to do with the response once it returns — the three stages alova takes over. For a paginated list, one `usePagination` declaration covers paging, prefetch and create/update/delete sync.

See [Comparison with other request libraries](https://alova.js.org/about/comparison) for more.

## Join the community

- [Follow us on X](https://x.com/alovajs)
- [Join the Discord](https://discord.gg/S47QGJgkVb)
- [Join the WeChat group](https://alova.js.org/img/wechat_qrcode.jpg)

## We need your support

If you like alova, we are very grateful for giving us a star in the upper right corner, which is a recognition and encouragement for our work.

## Welcome to contribute

We are honored to receive active participation from developers around the world in Issues and Discussions.

We hope to make alova a common project for everyone who is willing to participate. We encourage everyone to become a contributor to the alova community with an open and inclusive attitude. Even if you are a junior developer, as long as your ideas meet the development guidelines of alova, please participate generously.

Effective contributions will win you a certain reputation in the Alova community. Before contributing, please be sure to read the [Contribution Guide](./CONTRIBUTING.md) in detail to ensure your contribution is effective.

## Changelog

[Link](https://github.com/alovajs/alova/releases)

## Contributors

<a href="https://github.com/alovajs/alova/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=alovajs/alova&max=30&columns=10" />
</a>

## LICENSE

[MIT](https://en.wikipedia.org/wiki/MIT_License)
