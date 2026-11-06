# Parallel Voices

Send one prompt to several Pollinations models at once and compare every answer side by side â€” with latency and token counts per model.

**App:** https://ezzelddin-abdallah.github.io/pollinations-parallel-voices/

## How it uses Pollinations

- `GET https://gen.pollinations.ai/text/models` â€” loads the live text-model list.
- `POST https://gen.pollinations.ai/v1/chat/completions` â€” one request per selected model, with the visitor's own Pollen (BYOP). A random `seed` per request avoids the cache, so each model genuinely answers.
- Sign-in goes to `https://enter.pollinations.ai/authorize?redirect_uri=â€¦&state=â€¦&budget=0.5&expiry=1`; the key returns in the URL fragment, is immediately stripped from the address bar, and is kept in `sessionStorage` for the tab only. No server, no keys in the repository.

## Run

Static single page â€” open the URL above, sign in, pick models, ask.

[![Made with pollinations.ai](https://raw.githubusercontent.com/pollinations/pollinations/main/packages/ui/src/brand/badge-made-with.svg)](https://pollinations.ai/?ref=badge)
