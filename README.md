# Collage Infrastructure — Website

One-page static site approved for Collage Infrastructure. No frameworks, tracking, or third-party dependencies.

## Preview

Open `index.html` in a desktop or mobile browser. All logo assets are local. The site displays the approved wordmark *without small circles* in the upper-left, and the original large overlapping-circles icon on the right.

## Publish using GitHub Pages

1. Log into GitHub and create a new **public** repository, e.g. `collage-website` (GitHub Pages on GitHub Free uses public repositories).
2. Upload **the contents of this directory** to the repository root: `index.html`, `CNAME`, `.nojekyll`, `README.md`, and the `assets` folder. Do not upload only the ZIP itself.
3. Open repository **Settings → Pages**. Select **Deploy from a branch**, `main`, `/ (root)`, then **Save**.
4. Add `collageinfra.com` as the **Custom domain** in GitHub Pages if not already populated by the `CNAME` file.
5. At your domain registrar, add GitHub Pages apex `A` records (name `@`) pointing to: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`. Remove conflicting apex `A` records. If your registrar supports `ALIAS`/`ANAME`, follow GitHub's guidance instead of adding conflicting records.
6. Set `www` as a `CNAME` to **YOUR-GITHUB-USERNAME.github.io** (replace with your real username). Do not set it to the website domain. Make sure `www` also resolves as intended.
7. Once DNS propagates and GitHub issues the certificate, enable **Enforce HTTPS** in Pages settings.
8. Visit `https://collageinfra.com` and `https://www.collageinfra.com` and verify the page works. Test contact mail links and the mobile layout.

## Important: keep your email working

Website DNS records are independent of email DNS records. **Do not delete** existing Microsoft 365 Exchange `MX`, `TXT` (SPF / domain verification), `CNAME` (DKIM/autodiscover as appropriate), or `TXT` (DMARC) records. If email is not set up yet, follow Microsoft's current admin wizard and add the records it specifies. Your email provider can be Microsoft 365 or Google Workspace; neither is required to host this static site.

## Included files

- `index.html`: responsive landing page and SEO/social metadata.
- `assets/collage-wordmark.svg`: original supplied wordmark-only logo, no circles.
- `assets/collage-icon.svg`: original supplied icon (large circles and favicon).
- `assets/favicon-192.png`: browser icon fallback.
- `assets/social-preview.png`: basic preview image.
- `CNAME`: tells GitHub Pages the custom domain.
- `.nojekyll`: disables Jekyll processing.

## Edits

Text lives in `index.html`. Update the headline and description in `<main>` plus page metadata in `<head>` if the copy changes.
