# PK CUT — rebranded build of Concat

**PK CUT** is a rebranded build of **Concat** by jub0t
(https://github.com/jub0t/Concat), an open-source CapCut-style video
editor. This build is based on Concat v0.2.6.

## License

This project remains licensed under **AGPL-3.0-or-later** (plus the plugin
exception), exactly as the upstream project. All upstream license files are
kept intact:

- `LICENSE`
- `LICENSE-EXCEPTIONS.md`
- `THIRD_PARTY_NOTICES.md`
- `TRADEMARK.md`

Copyright stays with Jareer and the Concat contributors. In line with the
upstream `TRADEMARK.md`, this build does not use the "Concat" name or marks
in user-visible places; it is distributed under its own name, "PK CUT".

## What was changed from upstream

1. **App name**: "Concat" → "PK CUT" in all user-visible strings
   (14 shipped UI languages; key names in code unchanged).
2. **New Urdu (اردو) UI translation** added: `src/crates/concat/locales/ur.json`,
   registered in `src/crates/concat/src/i18n.rs`. Strings not yet translated
   fall back to English, as the i18n system is designed to do.
3. **Android package id**: `app.concat.editor` → `com.pkcut.app`
   (`src/crates/concat-android/Cargo.toml`).
4. **Launcher icons** replaced with original PK CUT artwork
   (`src/crates/concat-android/res/mipmap-*/ic_launcher.png`).
5. **Window title**: "Concat" → "PK CUT" (`src/crates/concat/ui/app.slint`).
6. **Android Java bridge**: `app.concat.editor.ConcatFiles` →
   `com.pkcut.app.PkcutFiles` (package, class and file renamed).
7. **Default project folder**: "Concat" → "PK CUT" (desktop/Android).
8. **In-app updater** now reads releases from `playhogasab/pk-cut`
   (`src/crates/concat-host/src/updates.rs`) instead of upstream, so it
   can never offer upstream Concat builds. It becomes functional once
   releases are published to that repository.
9. **Version** bumped to 1.0.0 for this release.

Nothing else was modified: no features added or removed, no telemetry
added. The app stays 100% offline, with no watermark, no account and no
paywall — as upstream.
