# Extraktor plugins

[Extraktor](https://extraktor.app) reads live web pages as Markdown and searches the web for AI agents. The plugin adds the Extraktor MCP server (`https://extraktor.app/mcp`) and two skills to Claude Code and Codex. The agent opens a sign-in page the first time it uses Extraktor. Each account gets 25 free credits each month.

## Claude Code

```sh
claude plugin marketplace add DennisKo/extraktor-plugins
claude plugin install extraktor@extraktor
```

Then run `/mcp` in Claude Code, select `plugin:extraktor:extraktor`, and sign in.

## Codex

```sh
codex plugin marketplace add DennisKo/extraktor-plugins
codex plugin add extraktor@extraktor
codex mcp login extraktor --scopes profile
```

Sign in on the page that opens. Then start a new chat.

## Other agents

Add the MCP server to each coding agent on your computer (Claude Code, Codex, Cursor, VS Code, Gemini CLI and Windsurf):

```sh
npx -y @extraktor/cli mcp add
```

For a different MCP client, add `https://extraktor.app/mcp` as a remote Streamable HTTP server. See [extraktor.app](https://extraktor.app/#connect) for each client.

## What the plugin contains

| Part | Use |
| --- | --- |
| MCP server `extraktor` | The `extract` tool reads a public page. The `search` tool finds pages. |
| Skill `read-source` | Check a claim or find a fact on a page, with the source as evidence. |
| Skill `compare-sources` | Compare facts from several pages, with a citation for each fact. |

## Source

This repository is a copy of the plugin files from the Extraktor repository. Report problems in the [issues](https://github.com/DennisKo/extraktor-plugins/issues).

## License

[MIT](LICENSE)
