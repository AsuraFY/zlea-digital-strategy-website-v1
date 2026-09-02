# ZLEA Digital Safety — visual V1

## Current working agreement

This is a design-stage prototype. Work on `update`; do not merge to `main` or deploy without a separate request.
The page copy is visitor-facing: no development, missing-asset or “coming soon” notices.
Implementation status belongs here, not on the pages.

## Pages

- `index.html`: guide-led hero, digital safety introduction, help preview, resource previews and news preview.
- `get-help.html`: message form with optional email, consultation layout and resource recommendation.
- `resources.html`: six example resource cards and category labels.
- `news.html`: seven news categories, original-source links and optional bilingual “Why it matters” text.
- `about.html`: initiative introduction and contact link to `get-help.html#help-form`.

Header/footer navigation and language controls work. EN/FR text is in `main.js`.
The responsive hero subtracts the measured header height and can grow for accessible reading.
News data lives in `content.js`; do not publish invented examples as real reports.

## Deferred integrations

No booking system is needed at this stage. Keep its visual section only.
A business mailbox provider and message-delivery technology will be chosen later.
The guide PDF and final cover are not supplied yet.
Resource article bodies, Privacy and Terms pages are not written yet.
Download, Read Guide, Send My Message, booking and legal controls remain disabled, styled at normal opacity for layout review.
No form submission, success message, email transmission or visitor-data storage is implemented.
Only the language preference is stored locally. The assistant is scripted navigation.

## Before a public launch

Supply the approved assets and resource content; choose and secure message delivery; prepare privacy/terms and retention rules; decide whether booking is wanted.
Do not enable data collection until those decisions are made. No secrets belong in frontend code.
Review the presentation of any remaining example content before publishing.

## Checks

Static HTML/CSS/JavaScript; no build/install step. Existing Bootstrap and Google Fonts CDN dependencies are unchanged.
Use a local static server and open `index.html` for review.
Run `node --check main.js`. Check EN/FR, links, keyboard navigation, mobile sizes and zoom before release.
