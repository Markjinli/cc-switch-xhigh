# CC Switch 3.19.2-xhigh.1

Local fork of farion1231/cc-switch v3.19.2.

## Why

Native Responses providers (`apiFormat = openai_responses`, including xAI Grok OAuth) used `codex_native_responses_template.json` with only `none` / `high`. Codex therefore hid `xhigh`.

Grok 4.6 officially supports `low` / `medium` / `high` / `xhigh`.

## Changes

- Native catalog template now includes `xhigh`
- Grok 4.6+ always gets the official four-level ladder, default `xhigh`, even through the local CC Switch proxy
- Provider `modelCatalog` can persist `defaultReasoningLevel` / `supportedReasoningLevels`
- xAI presets upgraded from Grok 4.5 to Grok 4.6 with `xhigh`

## Build

Requires Node 18+, pnpm, Rust 1.95, and Visual Studio Build Tools (MSVC).

```
pnpm install
pnpm build
```
