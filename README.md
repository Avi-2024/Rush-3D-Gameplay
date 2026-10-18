# Night Rush 3D — free browser racing game

A lightweight, self-contained **WebGL 3D endless highway racer** with a responsive public website.

## Files

- `index.html` — landing page and gameplay information
- `play.html` — playable full-screen 3D game (vanilla JS/WebGL)
- `how-to-play.html` — player instructions and scoring
- `about.html`, `privacy.html`, `terms.html`, `contact.html` — supporting website pages
- `assets/site.css` — responsive marketing-site styles
- `favicon.svg`, `robots.txt`, `sitemap.xml` — static site metadata
- `ADSENSE_SETUP.md` — monetization and policy checklist

## Play locally

Open `index.html` in Chrome, Edge, or Firefox. Alternatively run `python -m http.server 8080` and visit `http://localhost:8080`.

Desktop: A/D or left/right to steer, Space/Up for nitro, P/Escape to pause. Mobile: touch controls and horizontal swipes.

Requires WebGL. The game currently stores its best score in localStorage and does not use remote libraries, ads, or a backend.

## Deploy (Cloudflare Pages — recommended for monetized hosting)

1. Open https://dash.cloudflare.com/ and go to **Workers & Pages → Create application → Pages → Connect to Git**.
2. Authorize GitHub and choose `Avi-2024/Rush-3D-Gameplay`.
3. Set production branch to **main**, framework to **None**, build command to `exit 0` (or leave it blank), and build output directory to `.` (repository root).
4. Click **Save and Deploy** and test the resulting `*.pages.dev` URL and `/play.html`.
5. For AdSense, prefer a custom domain that you control, then update `sitemap.xml` and `robots.txt` to that exact public URL.

**Hosting policy:** Vercel's free Hobby tier is non-commercial only; use a suitable commercial plan if monetizing on Vercel. GitHub Pages has business-hosting restrictions, so do not rely on it as your long-term commercial advertising host. Review your chosen host's current terms.

## Deploy (GitHub Pages — demo/testing)

1. Open [repository Settings → Pages](https://github.com/Avi-2024/Rush-3D-Gameplay/settings/pages).
2. Under **Build and deployment**, choose **Deploy from a branch**, branch **main**, folder **/(root)**, then **Save**.
3. After the site publishes, check `https://avi-2024.github.io/Rush-3D-Gameplay/` and `https://avi-2024.github.io/Rush-3D-Gameplay/play.html`.
4. If you use a custom domain later, update sitemap, metadata and AdSense site settings to match the final domain.

## Deploy (Vercel — commercial plan if monetized)

Import `Avi-2024/Rush-3D-Gameplay` at https://vercel.com/new. Choose **Other** framework with no build step and repository root as output/root. Vercel may request an explicit output directory (use `.` for static files) depending on UI. Check the deployment before adding a custom domain.

## Monetization

Read [ADSENSE_SETUP.md](ADSENSE_SETUP.md). **Ads are not activated.** Do not paste fake publisher IDs, show regular AdSense units within the active game, encourage clicks, or request interstitials during continuous gameplay. Obtain your own approved AdSense publisher identifier first.

## Planned improvements

New car/track variety, more polished physics, missions, garage, collectibles, procedural levels, accessibility, performance options and analytics with proper disclosure.

## License

No open-source license is currently granted by this repository. Contact the repository owner before reusing or redistributing source code.
