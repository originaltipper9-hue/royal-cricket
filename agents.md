# AGENTS.md

## Architecture
A static, single-file site. Everything (markup, styles, script) lives in `index.html`. `netlify.toml` publishes the repo root with no build command. There is no framework, package.json, or server code.

## Behaviour
- Meta Pixel fires `PageView` on load.
- Clicking the Join button, or the 15-second countdown reaching zero, calls `triggerRedirect(source)`. It fires a single `Lead` event (`source` is `button_click` or `auto_timer`) and then navigates to the Telegram invite URL.
- The countdown ring uses an SVG circle (r=28). Its `stroke-dashoffset` is set from the circumference in JS.

## Conventions
- Keep it a single, dependency-free file unless the owner asks for more pages.
- The Telegram URL appears in two places (the button `href` and `telegramUrl`). Keep them in sync.
- The page is intentionally non-scrollable (`overflow: hidden`) and sized for mobile ad traffic. Check that the card still fits small viewports after any content change.
