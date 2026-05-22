# yusufkaracaburun marketplace

Claude Code plugin marketplace by [Yusuf Karacaburun](https://github.com/yusufkaracaburun) — a single catalog of skill / plugin bundles, starting with **ai-kit** (stack-agnostic agile lifecycle).

## Install

Inside Claude Code:

```text
/plugin marketplace add yusufkaracaburun/marketplace
```

That registers this catalog once. Then install any plugin from it:

```text
/plugin install ai-kit@yusufkaracaburun
```

Update later:

```text
/plugin marketplace update yusufkaracaburun/marketplace
/plugin update ai-kit
```

## Plugins

| Plugin | Description | Repo |
| ------ | ----------- | ---- |
| **ai-kit** | Agile lifecycle for Claude Code + Cursor — 20 skills, 3 subagents, 5 slash commands, opt-in skill-logging hook. | [yusufkaracaburun/ai-kit](https://github.com/yusufkaracaburun/ai-kit) |

More plugins planned — see issues in the [ai-kit repo](https://github.com/yusufkaracaburun/ai-kit/issues) for what's being brainstormed.

## What this is (and isn't)

This repo is **only the catalog**. It contains one `.claude-plugin/marketplace.json` listing the plugins, each `source` pointing at the plugin's own repo. No skill code lives here.

Adding a new plugin means:

1. Building the plugin in its own repo (e.g. `yusufkaracaburun/<plugin>`).
2. Adding a new entry to `.claude-plugin/marketplace.json` here with `source.url` pointing at that repo, `source.path` to its plugin subdir (if any), and `source.ref` pinned to a release tag.
3. Tagging + pushing this repo so existing users get the update on `/plugin marketplace update yusufkaracaburun/marketplace`.

## License

MIT — see [LICENSE](LICENSE).
