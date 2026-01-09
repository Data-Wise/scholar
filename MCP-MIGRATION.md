# MCP Server Migration Guide

## Scholar Plugin MCP Configuration

Scholar is a **pure plugin** and does **not require** any MCP server configuration! 🎉

### No MCP Dependencies

Scholar uses shell-based API wrappers instead of MCP servers:
- `lib/arxiv-api.sh` - arXiv paper search
- `lib/crossref-api.sh` - DOI lookup via Crossref
- `lib/bibtex-utils.sh` - BibTeX file operations

This makes Scholar:
- ✅ **Faster** - No IPC overhead
- ✅ **Simpler** - No server configuration needed
- ✅ **Portable** - Works everywhere Claude Code runs
- ✅ **Self-contained** - All dependencies included

### Installation

Just install the plugin - no additional configuration needed:

```bash
brew install scholar
# Or
npm install -g @data-wise/scholar
```

### Migration from statistical-research

If you previously used the `statistical-research` plugin from the monorepo:

**No MCP configuration changes needed!**

The statistical-research plugin also used shell-based APIs, so your installation is already compatible.

Just uninstall the old plugin and install scholar:

```bash
rm -rf ~/.claude/plugins/statistical-research
brew install scholar
```

### Optional: MCP Server for Advanced Features (Future)

In a future release (Phase 2), Scholar may optionally integrate with an MCP server for advanced features like:
- R execution for statistical analysis
- Zotero integration
- LaTeX compilation

This will be **optional** - all current commands will continue to work without MCP.

### Questions?

- **Issues:** https://github.com/Data-Wise/scholar/issues
- **Documentation:** https://data-wise.github.io/scholar/

---

**TL;DR:** Scholar requires **no MCP configuration**. Install and use immediately!
