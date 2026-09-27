# gentle-releases

Published builds of gentle connection and gentle device, read by the gentle device DPC on managed
phones. Written only by the source repos' CI (deploy key).

One branch per app, named by package (`ch.heuscher.gentleconnect`, `ch.heuscher.gentledevice`), force-pushed on every
release: `app.apk`, then `manifest.json` whose `url` points at the APK's commit. The DPC checks
the APK's hash and pinned signing certificate before installing, so the manifest being public
and unauthenticated cannot make a phone install anything that was not signed by us.
