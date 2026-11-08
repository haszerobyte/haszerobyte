<p align="center">
  <img src="assets/haszerobyte-banner.svg" width="100%" alt=">_ haszerobyte: small, fast tools for AI agents, written in Rust">
</p>

<p align="center">
  <a href="https://github.com/haszerobyte/Ratatoskr"><img src="assets/badges/featured.svg" alt="featured: ratatoskr"></a>
  <img src="assets/badges/rust.svg" alt="Rust">
  <img src="assets/badges/mcp.svg" alt="MCP">
</p>

### >_ Hi, I'm haszerobyte

I build the plumbing that lets coding agents (Claude Code, Codex, Cursor, …)
reach the outside world. My rules for it:

- **Lean.** One small binary that starts instantly and idles at a few megabytes.
- **No keys if avoidable.** It works out of the box; paid APIs are optional fallbacks.
- **Polite.** Paces itself per site and backs off when a site says no.
- **Safe by default.** Never lets an agent reach into your local network.

### >_ Featured: ratatoskr

<table>
  <tr>
    <td width="180" align="center">
      <a href="https://github.com/haszerobyte/Ratatoskr">
        <img src="assets/ratatoskr-logo.svg" width="160" alt="ratatoskr logo">
      </a>
    </td>
    <td>
      <a href="https://github.com/haszerobyte/Ratatoskr"><b>ratatoskr</b></a>:
      web search and page fetching for AI agents, in pure Rust, with no API key.
      <br><br>
      <ul>
        <li><code>web_search</code>: a meta-search over Yahoo, DuckDuckGo, Bing and Yandex for web pages, news, images, videos and books</li>
        <li><code>web_fetch</code>: pages and PDFs as clean text with their links kept</li>
        <li>An MCP server, a CLI and a Rust library, all in one 10&nbsp;MB binary</li>
      </ul>
      <a href="https://crates.io/crates/ratatoskr-web"><img src="https://img.shields.io/crates/v/ratatoskr-web?color=e5323b&labelColor=1a0a0c" alt="crates.io"></a>
      <a href="https://docs.rs/ratatoskr-web"><img src="assets/badges/docs.svg" alt="docs: docs.rs"></a>
      <a href="https://github.com/haszerobyte/Ratatoskr/releases"><img src="assets/badges/download.svg" alt="download binaries"></a>
      <a href="https://github.com/haszerobyte/Ratatoskr/stargazers"><img src="https://img.shields.io/github/stars/haszerobyte/Ratatoskr?style=flat&color=e5323b&labelColor=1a0a0c&label=stars" alt="stars"></a>
    </td>
  </tr>
</table>

Compared with the reference MCP fetch server, run as MCP servers:

| | ratatoskr | [mcp-server-fetch](https://github.com/modelcontextprotocol/servers/tree/main/src/fetch) |
|---|---|---|
| ready to answer | **0.01 s** | 3.58 s |
| memory at idle | **6 MB** | 95 MB |
| memory after the calls | **44 MB** | 143 MB |

#### Add it to your agent

Install it from the [releases](https://github.com/haszerobyte/Ratatoskr/releases),
or with `cargo install ratatoskr-web --locked`. Then:

<details>
<summary><b>Claude Code</b></summary>

```sh
claude mcp add ratatoskr -- ratatoskr mcp
```
</details>

<details>
<summary><b>Codex</b> (<code>~/.codex/config.toml</code>)</summary>

```toml
[mcp_servers.ratatoskr]
command = "ratatoskr"
args = ["mcp"]
```
</details>

<details>
<summary><b>Claude Desktop, Cursor</b> and most other clients</summary>

```json
{
  "mcpServers": {
    "ratatoskr": { "command": "ratatoskr", "args": ["mcp"] }
  }
}
```
</details>

<details>
<summary><b>VS Code</b> (<code>.vscode/mcp.json</code>)</summary>

```json
{
  "servers": {
    "ratatoskr": { "type": "stdio", "command": "ratatoskr", "args": ["mcp"] }
  }
}
```
</details>

Or try it in a terminal:

```sh
ratatoskr search "tokio select macro"
ratatoskr fetch https://www.rust-lang.org/
```

### >_ Tools I use

<p>
  <img src="https://skillicons.dev/icons?i=rust,linux,git,githubactions,bash&theme=dark" alt="Rust, Linux, Git, GitHub Actions, Bash">
</p>

### >_ Get in touch

Found a bug or have an idea? [Open an issue](https://github.com/haszerobyte/Ratatoskr/issues)
on ratatoskr. Stars are welcome too ⭐
