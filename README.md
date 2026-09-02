# ZLEA Digital Safety V1

Static HTML, Bootstrap 5, custom CSS and vanilla JavaScript. Work on `update`; `main` is unchanged until explicitly approved for merging.

## Pages

- `index.html`: guide hero, introduction to digital safety, Get Help preview, four resource previews and News & Updates preview.
- `get-help.html`: open message form with an always-visible optional email field, consultation section and resource recommendation.
- `resources.html`: free resources collection; planned guides are explicitly marked as coming soon.
- `news.html`: Digital Safety Watch with category filters and original source links.
- `about.html`: introduction, scope and a link to the message form on `get-help.html#help-form`.

Shared navigation: Get Help, Learn (Free Resources / News & Updates), About, EN/FR.
The hero fills the available viewport below the measured navigation, growing when needed to avoid clipping.
The language preference is stored locally; message drafts and email addresses are never stored locally.

## Not yet connected

- No guide PDF, final cover or download URL has been supplied. Download is disabled.
- No message backend exists. The send button is disabled and the form never transmits.
- The form allows a message without a name/email, or an optional email reply. No email means no direct reply. This is not a promise of technical anonymity.
- No booking link or calendar has been supplied. Booking is disabled.
- Privacy and Terms are visibly unavailable until approved policies are supplied.
- News data is empty until reviewed source links are supplied. No fabricated reports, cases or dates are displayed.
- The assistant is local scripted navigation, not AI or a human support channel.

Before enabling message delivery, agree a backend, restricted recipient access, retention/deletion policy, privacy notice and abuse protection. Keep all credentials server-side; never add secrets to frontend code.
Connect booking only after its URL and privacy implications are reviewed.
Replace the guide's disabled control with a real download link only after the approved document is present.
Replace planned-resource statuses with links only when the actual guides are ready.

## Content updates

Bilingual UI copy is in `main.js`; English HTML is readable without JavaScript.
News entries are in `content.js`. Required fields:
`category`, `title: {en, fr}`, `summary: {en, fr}`, optional `whyItMatters: {en, fr}`, `source`, `date` (YYYY-MM-DD) and a real HTTPS `url`.
Rendering uses textContent, not HTML interpolation from editorial data.

## Local use and checks

Pull `update`, then open `index.html` with a local static server (for example VS Code Live Server).
No bundler or installation is required. Bootstrap and Google Fonts are existing CDN dependencies.
Run `node --check main.js` and `node --check content.js`.
Before release, visually check desktop/mobile in EN/FR, the Learn menu, anchors, 50%/100% zoom and keyboard navigation.

## Approved V1 copy (September 2026)
The five pages follow the supplied page-by-page script. The six resource-page cards and four homepage cards are planned guides, not published downloads. Categories are labels, not filters yet. News supports the seven requested tags, including Law & Policy, plus optional bilingual “Why it matters” commentary. Example news in the copy is a format illustration and is not published as real news.
The hero has a clearly labeled cover placeholder until the actual approved book cover is supplied. Anonymous-message wording is accompanied by a technical-anonymity limitation. Sending remains disabled. Footer language controls work on every page.

No deployment or merge to `main` is performed as part of these content updates.
