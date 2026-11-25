# Metogram iOS build status

This branch prepares a separate Metogram app configuration while retaining Telegram's native iOS interface and Telegram account/network compatibility.

## Configuration required before an IPA can be built

1. Create an API application at https://my.telegram.org/apps and provide its `api_id` and `api_hash` to the build environment as protected secrets. Do not commit credentials.
2. Set an Apple Team ID and valid signing material for a signed device IPA. A free Apple ID has limited provisioning and does not provide a durable public IPA distribution method.
3. Build on macOS with the Xcode/Bazel versions pinned in `versions.json`. This repository cannot be compiled into an iOS IPA on Railway/Linux or on an iPhone itself.

## Current status

- [x] Dedicated branch: `metogram/initial-build`
- [x] Separate Metogram bundle/config template added
- [ ] Verify branding assets and app display name in the Xcode/Bazel project definitions
- [ ] Supply Telegram API credentials securely
- [ ] Configure Apple signing
- [ ] Run macOS build and verify IPA installation

The app keeps the upstream Telegram iOS interface. Metogram-only gifts, NFT, badges and balances are not implemented by this configuration and require a separate backend/API integration.
