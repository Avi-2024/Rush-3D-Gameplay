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

Desktop: A/D or left/right to steer, Space/Up for nitro, P/Escape to pause. Mobile: touch controls and horizontal swipes. Use the pre-race setup to choose tracks, modes, quality and separate music/effects switches.

Requires WebGL. The game currently saves best score, garage ownership, credits, progression and settings in localStorage. It does not use remote libraries, ads, or a backend.

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

## Gameplay upgrade (October 18, 2026)

- **Six original sports cars:** Vortex, Blaze, Solar, Nova, Phantom, Viper; five are unlockable with local garage credits.
- **Persistent progression:** credits from distance, coins, daily challenges, achievements and four milestone missions; save data stored in localStorage.
- **Three visual environments:** neon city, sunset highway and animated rainstorm. These are thematic variations of the same highway geometry, not separate full racing circuits.
- **Two modes:** Endless and 90-second Sprint (against the clock, not multiplayer).
- **Audio:** original procedural synth BGM, an engine layer and coin/collision effects with independent Music/Effects toggles, saved across visits. Audio requires a user gesture.
- **Graphics:** Auto, Battery and Quality render-resolution options, with reduced scene detail on Battery; WebGL context loss handling.
- **Effects:** six stylized car meshes, reflective roadway lights, nitro glow and flame effects, collision screen shake and flash.

### Manual smoke test

Open `play.html`, verify menu, select track and mode, toggle Music and Effects, start, steer and boost, crash, then restart. Check credits and achievements persist after reloading. Test all three tracks and quality settings in Chrome/Edge and on a touch browser. Browser audio must be started with a click. `window.nightRush3D.getState()` exposes a read-only runtime summary for debugging.

**Implementation boundaries:** Road movement is lane-based, not full free-steering physics. The game is a standalone static WebGL app, not yet an online leaderboard, multiplayer title or AdSense-approved property.

## Planned improvements

More detailed car meshes and driving physics, additional modes and environment variety, stronger accessibility, optional analytics with proper disclosure and cross-device cloud saves (future backend required).

## License

No open-source license is currently granted by this repository. Contact the repository owner before reusing or redistributing source code.
