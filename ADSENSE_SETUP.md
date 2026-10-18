# Night Rush 3D — AdSense readiness checklist

**Status: advertising is NOT enabled.** You must first publish the website, verify domain ownership and obtain an approved AdSense account. No approval or revenue is guaranteed.

## 1. Improve quality before applying
- Keep the game reliable and playable on desktop and mobile.
- Publish accurate navigation, instructions, original information, privacy policy and contact details.
- Add original game guides or additional original games over time; a single thin page may not meet approval expectations.
- Consider using a verified custom domain under your control.

## 2. Regular AdSense for content
- Sign up at https://www.google.com/adsense/start/ and follow its site-ownership verification steps.
- Once approved, add **your actual** AdSense auto-ad snippet or responsive units **only in appropriate content-page placements**, not inside the playing canvas.
- Ensure ads are clearly distinguishable from game UI. Do not place ad units around play/start/restart/nitro controls. Google's game-page guidance recommends ads be at least 150 px from the game.
- Avoid unexpected interstitials and automatic ad refreshing. Never click your own ads or solicit clicks.
- Assess consent requirements for your visitors, including applicable EEA/UK/Switzerland requirements and other local laws, before loading personalized advertising.
- Update `privacy.html` with actual providers/data uses BEFORE enabling ads.

## 3. Ads.txt
After approval, create `ads.txt` at your monetized domain root using the **exact line copied from your AdSense account**, typically `google.com, pub-YOUR_REAL_ID, DIRECT, f08c47fec0942fa0`. This example is illustrative; never publish it literally. For AdSense domain-root ownership, custom domains are preferable to a project path on github.io.

## 4. In-game ad formats
If you later want rewarded or game-over interstitial ads, apply for **AdSense H5 Games Ads** access; it is a separately applied-for product, not automatically available to every AdSense publisher. If accepted, use Google's H5 Games Ad Placement API only at natural breaks (such as after a race), with user opt-in for rewarded ads. Do not interrupt continuous driving.

Official references:
- https://support.google.com/adsense/answer/2768340
- https://support.google.com/adsense/answer/9724
- https://support.google.com/adsense/answer/9959170
- https://support.google.com/adsense/answer/1705831
- https://support.google.com/adsense/answer/12171612
- https://support.google.com/adsense/answer/1348695

## Before launching real ads
Provide the actual final domain, `ca-pub-` publisher ID and AdSense approval status. Never assume access to H5 Games Ads.
