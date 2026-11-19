# talos-hq/homebrew-tap

```sh
brew install talos-hq/tap/clud
brew install --cask talos-hq/tap/voxtype
```

| Path | Package | Updated by |
|---|---|---|
| `Formula/clud.rb` | [clud](https://github.com/talos-hq/clud) | the clud release workflow (talos-hq/clud) |
| `Casks/voxtype.rb` | [Voxtype](https://github.com/talos-hq/talos-vox), push-to-talk voice-to-text for macOS | the `package-manifests` job in talos-vox's `build-macos.yml`, on every stable `vX.Y.Z` tag |

Do not edit these files by hand: each release workflow overwrites its own file.

## Voxtype

**First release pending.** `Casks/voxtype.rb` appears with the first stable
talos-vox release tag; until then `brew install --cask talos-hq/tap/voxtype`
reports that the cask doesn't exist.

The cask installs the notarized, stapled `Voxtype.app` from the GitHub
release DMG and links its `voxtype` CLI. It is rendered from the template in
talos-vox (`packaging/homebrew-tap/Casks/voxtype.rb.in`) with the DMG's
SHA-256, and passes `brew style` and `brew audit --cask --strict` before it
is pushed here. Prerelease tags (any tag with a `-`, such as `v1.2.0-rc1`)
are not published to the tap.
