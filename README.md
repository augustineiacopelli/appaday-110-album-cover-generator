# AppADay 110: Album Cover Generator

Part of [AppADay](https://augustineiacopelli.github.io/appaday/), a daily discipline project by Augustine Iacopelli. One complete, functional, mobile-friendly web app, designed and shipped every single day.

## What it does

Describe a mood or vibe and get back a fictional album cover: Claude invents a band name and song title that fit the description, while Pollinations generates the cover art from the same prompt. Both calls run independently, so a failure on one side (a missing API key, a Claude error, an image timeout) never blocks the other from rendering. The finished card shows the artwork, band name, and song title with a one-tap download for the cover image.

## How it works

A single self-contained `index.html` with no build step and no dependencies beyond Google Fonts. The Claude API is called directly from the browser using a key stored in this browser's local storage only, entered through the Settings gear icon. Pollinations' image endpoint needs no key; it is a plain URL built from the mood text that returns an image, which the app fetches as a blob and converts to a downloadable object URL. Generation is capped at once every fifteen seconds to keep API usage reasonable.

## Tech

Vanilla HTML, CSS, and JavaScript. Claude Sonnet 5 via the Anthropic Messages API for the band name and song title, returned as strict JSON. Pollinations for the cover art. Google Fonts (Space Grotesk, Archivo Black) for type.

## Category

AI-Powered, Creative

---

[Back to the AppADay portfolio](https://augustineiacopelli.github.io/appaday/)
