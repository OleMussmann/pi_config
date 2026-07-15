## NixOS
This is a NixOS system.
Do NOT search `/nix/store/` — it's massive. Use known paths or ask user.
Pi docs: paths in your system instructions (don't search for them).
Missing tools: `nix shell nixpkgs#<pkg> --command <tool>`

## Web Search
Use `ketch` for external research — web pages, OSS code, library docs.
- `ketch search "query"` / `ketch search "query" --scrape` for web results with optional full content (add `--multi` to federate across backends and rank-fuse)
- `ketch scrape <url> [url...]` for clean markdown from one or more URLs
- `ketch extract` for already-fetched/piped HTML (`curl ... | ketch extract`) — no fetch, no cache, no browser
- `ketch code "query" --lang go` for real OSS code with repo/line context
- `ketch docs "query" --library /org/repo` for version-aware library docs
- All commands support `--json`. `ketch config` reports active backends.

### Tool Selection

| Tool | Use for | Avoid for |
|------|---------|-----------|
| `web_search` | Quick AI-synthesized answers, multi-query research | Code search, GitHub repos |
| `ketch` | Code search, docs, raw results without AI synthesis | YouTube videos |
| `fetch_content` | GitHub repos (clone + explore), YouTube transcripts, local files | Simple web pages |

**Decision flow:**
1. GitHub repo or YouTube video → `fetch_content`
2. Code search across repos → `ketch code`
3. Library docs → `ketch docs`
4. Quick factual answer → `web_search`
5. Deep research with full content → `ketch search --scrape`
