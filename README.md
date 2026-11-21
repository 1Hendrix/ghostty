# Ghostty fork: single-tab-bar

A personal fork of [Ghostty](https://github.com/ghostty-org/ghostty) with one macOS patch:
with `macos-titlebar-style = tabs`, a window that holds a single tab shows **no bar**, and
the terminal reaches the top edge. A second tab brings the normal tab bar back.

- `patches/single-tab-bar.patch`: the patch (3 Swift files), applied to each Ghostty release.
- `.github/workflows/release.yml`: daily check for a new Ghostty release; builds it with the
  patch and publishes it as a release here. An issue announces it (or says the patch needs updating).
- `scripts/ghostty-fork-update`: installs a release on the Mac (signs it with a local
  self-signed identity, swaps it in when Ghostty quits). `--permissions` reopens the macOS
  permission panes after the first install.
- Branch `single-tab-bar`: the patch as commits on v1.4.0, with a build workflow for development.

Not affiliated with the Ghostty project.
