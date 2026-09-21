# The Judgment Code — Deploy-Ready Website

Premium, mobile-first sales page built with static HTML, CSS, and vanilla JavaScript. No build process or framework is required.

## Files

- `index.html` — complete sales page, styles, content, and interactions
- `founder.png` — founder portrait used in the hero and philosophy section
- `README.md` — setup and editing instructions

## Change the checkout links

Open `index.html`, search for `STORE_CONFIG`, and replace:

```js
CORE_CHECKOUT_URL: "#",
COMPLETE_CHECKOUT_URL: "#",
```

Every purchase button is connected to these two centralized values.

## Change pricing

In the same `STORE_CONFIG` block, edit:

```js
prices: { core: "17.90", complete: "29.90" }
```

Then update the price wording inside the CTA labels by searching for `$17.90` and `$29.90` in `index.html`.

## Change product contents

Edit the `core` and `complete` arrays under `contents` in `STORE_CONFIG`. The pricing-card lists update automatically.

The descriptive “Inside the System” cards are normal HTML and can be edited by searching for `Inside the system`.

## Founder image

Keep `founder.png` in the repository root, beside `index.html`. Replace it with a new image using the same filename. A vertical portrait is recommended; the current aspect ratio is 2:3.

## Add tracking later

Search `index.html` for:

- `Meta Pixel`
- `Google Analytics / GTM`

Clearly labeled comments show where tracking code should be added. Purchase buttons include `data-plan="core"` and `data-plan="complete"`, plus unique IDs for future conversion events.

## Legal links and support email

The footer policy links currently use `#`. Replace them with the final Terms, Privacy Policy, and Refund Policy URLs. Replace `contact@your-domain.com` with the real support email.

## SEO before launch

Replace `https://your-domain.com/` in the canonical and Open Graph URL tags with the final domain. Add a real social sharing image later if one is created and approved.

## Deploy to Vercel

1. Create a GitHub repository.
2. Upload `index.html`, `founder.png`, and `README.md` to the repository root.
3. In Vercel, select **Add New → Project** and import the repository.
4. Keep **Framework Preset** set to **Other**.
5. Leave Build Command and Output Directory empty, then deploy.

The project is fully static and requires no environment variables or dependencies.
