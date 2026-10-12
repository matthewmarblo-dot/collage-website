# Collage Infrastructure — Website

One-page static site for Collage Infrastructure. No frameworks, tracking, or third-party dependencies.

## Preview

Open `index.html` in a desktop or mobile browser. All logo assets are local. The site displays the corrected wordmark *without small circles or the stray black SVG artifact* in the upper-left, and the original large overlapping-circles icon on the right.

## Publish using GitHub Pages

1. Log into GitHub and create a new **public** repository, e.g. `collage-website` (GitHub Pages on GitHub Free uses public repositories).
2. Upload **the contents of this directory** to the repository root: `index.html`, `custom-domain CNAME (add only after ready to connect the domain)`, `.nojekyll`, `README.md`, and the `assets` folder. Do not upload only the ZIP itself.
3. Open repository **Settings → Pages**. Select **Deploy from a branch**, `main`, `/ (root)`, then **Save**.
4. Add `collageinfra.com` as the **Custom domain** in GitHub Pages if not already populated by the `custom-domain CNAME (add only after ready to connect the domain)` file.
5. At your domain registrar, add GitHub Pages apex `A` records (name `@`) pointing to: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`. Remove conflicting apex `A` records. If your registrar supports `ALIAS`/`ANAME`, follow GitHub's guidance instead of adding conflicting records.
6. Set `www` as a `custom-domain CNAME (add only after ready to connect the domain)` to **YOUR-GITHUB-USERNAME.github.io** (replace with your real username). Do not set it to the website domain. Make sure `www` also resolves as intended.
7. Once DNS propagates and GitHub issues the certificate, enable **Enforce HTTPS** in Pages settings.
8. Visit `https://collageinfra.com` and `https://www.collageinfra.com` and verify the page works. Test contact mail links and the mobile layout.

## Important: keep your email working

Website DNS records are independent of email DNS records. **Do not delete** existing Microsoft 365 Exchange `MX`, `TXT` (SPF / domain verification), `custom-domain CNAME (add only after ready to connect the domain)` (DKIM/autodiscover as appropriate), or `TXT` (DMARC) records. If email is not set up yet, follow Microsoft's current admin wizard and add the records it specifies. Your email provider can be Microsoft 365 or Google Workspace; neither is required to host this static site.

## Included files

- `index.html`: responsive landing page and SEO/social metadata.
- `assets/collage-wordmark.svg`: original supplied wordmark-only logo, no circles.
- `assets/collage-icon.svg`: original supplied icon (large circles and favicon).
- `assets/favicon-192.png`: browser icon fallback.
- `assets/social-preview.png`: basic preview image.
- `custom-domain CNAME (add only after ready to connect the domain)`: tells GitHub Pages the custom domain.
- `.nojekyll`: disables Jekyll processing.

## Edits

Text lives in `index.html`. Update the headline and description in `<main>` plus page metadata in `<head>` if the copy changes.

## Replacing an existing GitHub Pages deployment

Open the repository Code tab → Add file → Upload files, then upload **the contents** of this replacement folder. Commit directly to `main`. GitHub may require removing files with the same names first through the web UI; the simplest reliable method is to open `index.html` and paste the revised source using GitHub’s pencil editor, then replace `assets/collage-wordmark.svg` similarly. The files in this package are complete. Keep `custom-domain CNAME (add only after ready to connect the domain)` and email DNS records unchanged.

The layout is designed to fit common desktop viewport heights without vertical scrolling. On exceptionally short or narrow/mobile screens, content may scroll to preserve readability rather than hide text.

## Final polish (October 2026)
- The header wordmark uses `assets/collage-wordmark-clean.png` extracted directly from the approved original artwork; the flawed auto-traced SVG was removed.
- The headline displays as one line on standard desktop widths; smaller viewports use responsive text wrapping.
- The page fits within standard desktop viewport heights; on very small displays, content may scroll for accessibility.
