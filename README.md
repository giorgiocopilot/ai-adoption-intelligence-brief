# AI Adoption Intelligence Brief

An interactive, public-safe AI adoption briefing designed for **client interview purposes**.

It is a dependency-free static website that explains an enterprise adoption approach for a Google Workspace to Microsoft 365 Copilot transition. It is optimised for live screen sharing, Cloudflare Pages and Cloudflare Workers static-assets deployment.

## Purpose

The brief is designed to help a hiring manager or client sponsor understand:

- The practical corporate tensions that shape AI adoption: overhype, underuse and overwhelm.
- The difference between access, activation, engagement, habitual use and optimisation.
- How adoption telemetry can drive human interventions: segmentation, diagnosis, benchmarking and targeted enablement.
- A proposed first-90-days operating model for enterprise adoption and organisational change.

It is not a product claim, a public client case study, an endorsement or a performance guarantee.

## Public-safety rules

This repository intentionally excludes:

- Client names and prospective-client names.
- Internal dashboards, screenshots, source exports and Jira data.
- Internal URLs, email content, employee names and raw operational data.
- Non-public recruitment details.

The site uses anonymised, aggregated evidence and a public statement that approximately 32,000 Copilot licences are expected in the source programme, pending regulatory and legal approvals.

Before adapting this brief for another client, confirm that every metric, logo, quote and named reference is approved for the intended audience.

## Local preview

No build step is required.

1. Download or clone this repository.
2. Open `index.html` in Microsoft Edge, Google Chrome or another modern browser.
3. For the most reliable local preview, start a static server:

```bash
npx serve .
```

Then open the localhost address displayed by the command.

## Cloudflare Pages deployment

1. In Cloudflare, go to **Workers & Pages**.
2. Select **Create application** then **Pages** then **Connect to Git**.
3. Connect the `ai-adoption-intelligence-brief` repository.
4. Use these settings:

| Setting | Value |
|---|---|
| Production branch | `main` |
| Framework preset | `None` |
| Build command | Leave blank |
| Build output directory | `/` |
| Node version | Not required |

5. Deploy.

The repository includes `_headers` for security headers and `X-Robots-Tag: noindex, nofollow`.

## Cloudflare Workers deployment

The repository also includes `wrangler.toml` for Cloudflare Workers static-assets deployment.

```bash
npm run deploy
```

This invokes Wrangler through `npx`. Authenticate when prompted and update the worker name in `wrangler.toml` if your desired Cloudflare worker name is unavailable.

For a preview deployment:

```bash
npm run deploy:preview
```

## Replace CSS placeholders with images

The initial public version uses CSS-built visual placeholders for:

- Microsoft AI Transformation Leader certification badge.
- Google Workspace mark.
- Microsoft Copilot mark.

This avoids publishing image files before they have been checked, optimised and cleared for public use.

When ready:

1. Optimise the images as WebP or AVIF.
2. Place them under `assets/`.
3. Replace the corresponding CSS placeholder `div` in `index.html` with an accessible `img` element.
4. Add descriptive `alt` text.
5. Verify the page on desktop and mobile before publishing.

## Accessibility and interaction

- Responsive layout for desktop and mobile.
- Reduced-motion support through the `prefers-reduced-motion` media query.
- Animated metrics and bar charts activate as they enter the viewport.
- Hover interactions reinforce the migration and adoption-maturity story.
- A print stylesheet supports a landscape PDF export.

## Resources

- [Copilot ROI Calculator](https://roi-calculator-copilot.giorgiotsoupis.workers.dev/)
- [Peer reviews on LinkedIn](https://www.linkedin.com/in/george-tsoupis-ai-program-manager/details/recommendations/?detailScreenTabIndex=0)

## Licence

MIT. See [LICENSE](LICENSE).
