<h1 align="center">zerobyte</h1>

<p align="center">
  Small, fast tools for AI agents, written in Rust.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Rust-000000?logo=rust&logoColor=white" alt="Rust">
  <img src="https://img.shields.io/badge/MCP-tools-6f42c1" alt="MCP">
  <img src="https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black" alt="Linux">
</p>

---

### What I build

I make the plumbing that lets coding agents (Claude Code, Codex, Cursor, …)
reach the outside world: lean binaries, no API keys where they can be
avoided, polite to the sites they touch, and safe by default.

### Featured project

<table>
  <tr>
    <td width="140" align="center">
      <a href="https://github.com/haszerobyte/Ratatoskr">
        <img src="https://raw.githubusercontent.com/haszerobyte/Ratatoskr/main/assets/logo.svg" width="110" alt="ratatoskr logo">
      </a>
    </td>
    <td>
      <a href="https://github.com/haszerobyte/Ratatoskr"><b>ratatoskr</b></a>:
      web search and page fetching for AI agents, in pure Rust, with no API key.
      <br><br>
      <ul>
        <li><code>web_search</code>: a meta-search over Yahoo, DuckDuckGo, Bing and Yandex, with web, news, images, videos and books</li>
        <li><code>web_fetch</code>: pages and PDFs as clean text with their links kept; never reaches your local network</li>
        <li>One 10&nbsp;MB binary: an MCP server, a CLI and a library</li>
      </ul>
      <a href="https://crates.io/crates/ratatoskr-web"><img src="https://img.shields.io/crates/v/ratatoskr-web" alt="crates.io"></a>
      <a href="https://docs.rs/ratatoskr-web"><img src="https://img.shields.io/docsrs/ratatoskr-web" alt="docs.rs"></a>
      <a href="https://github.com/haszerobyte/Ratatoskr/releases"><img src="https://img.shields.io/github/v/release/haszerobyte/Ratatoskr" alt="release"></a>
    </td>
  </tr>
</table>

Try it in Claude Code:

```sh
cargo install ratatoskr-web --locked
claude mcp add ratatoskr -- ratatoskr mcp
```

### Get in touch

Found a bug or have an idea? [Open an issue](https://github.com/haszerobyte/Ratatoskr/issues)
on the project.
