# af_phone (AshFall RP fork of Sky Phone)

This repo is AshFall RP's fork of [sky-systems/sky_phone](https://github.com/sky-systems/sky_phone). The
resource itself is the `sky_phone/` folder; `frontend/` builds its NUI into `sky_phone/source/html`.

## Rules

- **Other resources reach the phone through `lb-phone`.** The manifest has `provide 'lb-phone'` and
  `source/bridge/phones/client/lb.lua` answers `exports['lb-phone']:IsOpen()` / `ToggleOpen()`, which is what
  af_inventory's phone slot calls. Keep that adapter working when pulling updates.
- **Never hand-edit `sky_phone/source/html`;** change `frontend/` and rebuild (see `AGENTS.md`).
- **`dev` is protected:** changes land through pull requests, as upstream's rulesets describe.
- **Keep each patch small, on its own commit,** with a message starting `af:`, and list it below.

## Pulling upstream updates

```sh
git remote add upstream https://github.com/sky-systems/sky_phone.git   # once
git fetch upstream
git merge upstream/dev
```

## Our patches

None yet: this is upstream Sky Phone 1.1.6.
