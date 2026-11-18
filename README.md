# Mach TV apps

The F-Droid repository for Mach apps on Android TV. [machtvapps.github.io](https://machtvapps.github.io/) has its
address and fingerprint, and lists the apps.

In Obtainium, use the "F-Droid Third Party Repo" source with `https://machtvapps.github.io/fdroid/repo` and the
app's ID.

## How it works

`.github/workflows/publish.yml` runs after each app's release and on every push to `main`. It rebuilds the repository
from each app's latest GitHub Release, signs it, and publishes it at `https://machtvapps.github.io/fdroid/repo`, with
the page in `site/` at the root. The apps are the files in `fdroid/metadata/`; adding one adds its app to the
repository and to the page.
