# The Royal Prediction — VIP Telegram Landing Page

A single-page, mobile-first landing page that invites visitors to join **The Royal Prediction** Telegram channel. It shows a gold-and-obsidian "VIP" card with a pulsing **Join Now Telegram** button and a 15-second circular countdown that redirects visitors to the channel automatically.

## Key technologies

- Plain HTML, CSS and vanilla JavaScript in one file (`index.html`) with no build step
- Google Fonts (Cinzel, Plus Jakarta Sans)
- Meta Pixel for `PageView` and `Lead` conversion tracking
- Hosted on Netlify as a static site

## Run locally

Open `index.html` in a browser, or serve the folder with Netlify CLI:

```bash
netlify dev --port 8889
```

## Customising

- Telegram invite link: change it in the `href` of `#joinBtn` and in `telegramUrl` in the script.
- Countdown length: `totalSeconds` in the script.
- Meta Pixel ID: the `fbq('init', ...)` call and the `<noscript>` image URL.
