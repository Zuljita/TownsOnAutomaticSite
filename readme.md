# Towns on Automatic — public site

Landing site for [Towns on Automatic](https://townsonautomatic.com), the
settlement lens of the On Automatic family — in design, not yet released.
Same design system as the sibling sites, with a hearth-orange primary. The
hero shows a real settlement stub from a Hexes-exported Campaign Vault; the
worklist figure is a real Campaigns on Automatic screenshot.

One content page (`index.html`) plus `privacy.html` and `404.html`. No build
step, no release data — when the app exists this site grows the family's
releases page and download plumbing.

## Deploy

`.github/workflows/deploy.yml` deploys to Cloudflare Pages on push to `main`
(`wrangler pages deploy . --project-name townsonautomatic`). It needs:

- repo secret `CLOUDFLARE_API_TOKEN` (same token the sibling sites use)
- repo variable `CLOUDFLARE_ACCOUNT_ID`
- a Pages project named `townsonautomatic` (direct upload) in the account

The public home is `https://townsonautomatic.com/` — the zone is already in
the same Cloudflare account. Add apex + `www` as custom domains on the Pages
project and Cloudflare writes the proxied CNAMEs itself.

Towns on Automatic is an original, unofficial, non-resale fan game aid by
Kyle Norton for GURPS and the Dungeon Fantasy Roleplaying Game, used per the
SJ Games Online Policy. Not affiliated with or endorsed by Steve Jackson
Games.
