<p align="center">
  <img src="https://img.shields.io/badge/HTML-5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS-3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/Zero_Build-Zero_Deps-22C55E?style=for-the-badge" alt="Zero build" />
  <img src="https://img.shields.io/badge/Studio_Builder-Ready-8B5CF6?style=for-the-badge" alt="Studio Builder Ready" />
  <img src="https://img.shields.io/badge/AI-Ready-F59E0B?style=for-the-badge" alt="AI Ready" />
</p>

<h1 align="center">VA Studio HTML Starter — Marketing Email</h1>

<p align="center">
  <strong>A Campaigns-style email template preview with editor chrome, meta bar, and a polished marketing email frame.</strong>
</p>

<p align="center">
  Three-tab editor chrome (Preview / HTML / Settings), inbox meta-bar showing From/To/Subject,<br/>
  hero image with overlay, stat grid, alternating feature blocks, CTA card, and a rich footer.
</p>

<p align="center">
  <a href="#quick-start">Quick Start</a> &bull;
  <a href="#sections">Sections</a> &bull;
  <a href="#studio-builder-integration">Studio Integration</a> &bull;
  <a href="#customizing">Customizing</a>
</p>

---

## Quick Start

```bash
python -m http.server 8000
# or
npx serve .
```

Open [http://localhost:8000](http://localhost:8000).

## Sections

- **Editor chrome** — sticky top bar with Preview / HTML / Settings tabs + Send-test / Schedule-send actions
- **Meta bar** — From / To (recipient count) / Subject, inbox-accurate layout
- **Email frame** — 640px width, rounded container with a subtle outer shadow
- **Topbar** — brand mark + "View in browser" link
- **Hero image** — full-bleed Unsplash photo with a dark gradient overlay and eyebrow tag
- **Greeting + lead** — personal salutation paragraph
- **Stat grid** — 3 headline numbers in accent-soft tiles
- **Feature blocks** — alternating image/copy rows with colored "New / Improved / Update" pills
- **CTA card** — dark navy-violet gradient with a white pill button
- **Signature block** — author avatar + role
- **Email footer** — social icons, address, unsubscribe/preferences links

## Studio Builder Integration

- Styles are CSS-driven (not email-client-safe inline styles — use a premailer step if sending via ESP)
- Every section is labelled (`.email-hero`, `.email-section`, `.feat-block`, `.cta-card`) for AI targeting
- Stat numbers, feature content, and footer links are plain text ready for Studio bindings
- The Preview / HTML / Settings tabs are real sections — Studio can populate them with live editor state

## Tech Stack

| Layer | Technology |
|-------|-----------|
| **Markup** | HTML5 with semantic email structure |
| **Styling** | CSS3 — for preview only, use premailer for inbox sends |
| **Fonts** | Inter + Playfair Display (Google Fonts) |
| **Images** | Unsplash + pravatar for author avatar |
| **Icons** | Inline SVG (social + tab icons) |

## Project Structure

```
va_studio_html_starter_email/
├── index.html      # Editor + email preview
├── styles.css      # Chrome + email frame styles
└── README.md
```

## Customizing

- **Subject line:** `.meta-field` row with label "Subject" in `index.html`
- **Hero:** swap the Unsplash URL and overlay text inside `.email-hero`
- **Stats:** `.stat-grid` — Studio feeds 3 numbers + captions
- **Feature blocks:** `.feat-block` articles — pills map to `new | improved | update`
- **Signature:** replace the pravatar URL and author name inside `.sig-row`
- **Palette:** CSS vars at top of `styles.css` — primary accent drives CTAs and hero tag

## Sending for real

This template renders as HTML+CSS — most email clients don't parse external stylesheets. When sending via an ESP:

1. Run the file through a premailer (e.g. [juice](https://github.com/Automattic/juice)) to inline the CSS
2. Or copy the inlined output into your Studio email pipeline

## License

MIT

---

<p align="center">
  Part of the <strong>VA Studio</strong> starter family · Built for rapid prototyping with an AI copilot.
</p>
