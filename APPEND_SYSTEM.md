## NixOS
This is a NixOS system.
Do NOT search `/nix/store/` — it's massive. Use known paths or ask user.
Pi docs: paths in your system instructions (don't search for them).
Missing tools: `nix shell nixpkgs#<pkg> --command <tool>`

## Web Search
Use the `web` tool (pi-ketch) for external research: web search, OSS code search, library docs, scrape, and crawl.
Run `/skill:ketch` for detailed usage.
For synthesized/summarized answers, delegate to the `subagent-web-search` subagent, if available (via the `subagent` tool).
For full repo clones or YouTube transcripts, use the pi-web-access tools.
