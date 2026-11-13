# agent-plugins

A field kit for working alongside coding agents.

This repo is a plugin marketplace. Add it once and you can install every plugin it lists, instead of adding each plugin's repo as its own marketplace. Each plugin lives in its own repo; this one only holds the listing.

Everything here is a Claude Code plugin for now. If you use Codex, Antigravity, or another harness, there's nothing for you to install yet.

## Plugins

| Plugin | What it does |
| --- | --- |
| [handoff-on-compact](https://github.com/kendrick/handoff-on-compact) | Turns Claude Code compaction into a resumable handoff document |
| [ux-punchlist](https://github.com/kendrick/ux-punchlist) | Review a running app one item at a time, with comments and approvals logged to an append-only file |

## Install

From the prompt of a Claude Code session, add the marketplace, then install a plugin by name:

```text
/plugin marketplace add kendrick/agent-plugins
/plugin install handoff-on-compact@kendrick
```

Or from a shell:

```sh
claude plugin marketplace add kendrick/agent-plugins
claude plugin install handoff-on-compact@kendrick
```

The `@kendrick` suffix is the marketplace's name, set in [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json). Some plugins need setup beyond this, so read a plugin's own README before you install it. For example, handoff-on-compact needs the `handoff` skill installed first.

## Issues

This marketplace isn't taking contributions right now. To report a bug in a plugin, open an issue on that plugin's repo.

## License

[MIT](LICENSE)
