# groovy-constantsx

Public runtime configuration for the tV client (owner-hosted fork of the
constants feed). Contains only JSON config and this README. No app binaries,
keystores, secrets, credentials, cookies, or tokens.

## Files
- `apps.json` — home-screen catalog. `movieApps` empty; `decodedWebsites` lists
  only Xgroovy and Xvideos. `trialExpiry` is set in the past (trial inert).
- `xgroovy` — no file: Xgroovy uses the client's built-in screens
  (`navigateTo: "Home"`); its behavior is entirely in the app and unchanged.
- `xvideos.json` — Framework source config for `FrameworkNavigationScreen`.
- `home-animation.json` — copied verbatim from the original feed.

## UNVERIFIED — xvideos.json
The Framework SCHEMA (section types, prop names, `${src}/${page}/${searchQuery}/${sublistValue}`
placeholders, the `url` = {quality: streamURL} player contract) is verified against
the client code and mirrors the working pornhub config. The xvideos.com DOM
selectors, URL/pagination templates, and stream extraction (`html5player.setVideoUrlHigh/Low/HLS`)
are BEST-EFFORT and were NOT validated against the live site. Validate and adjust
on an Android TV device before relying on them (see the test checklist in the patch report).
