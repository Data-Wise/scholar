# MCP Server Implementation

This directory will contain Model Context Protocol (MCP) server tools for scholar functionality.

## Planned Structure

```
mcp-server/
├── src/
│   ├── index.ts           # MCP server entry point
│   └── tools/             # MCP tool implementations
│       ├── literature.ts  # Literature search tools
│       ├── manuscript.ts  # Writing assistance tools
│       └── teaching.ts    # Teaching tools
├── package.json           # TypeScript dependencies
└── tsconfig.json          # TypeScript configuration
```

## Status

**Phase 2: Future Work**

This directory is currently a placeholder for the MCP Server Integration phase. MCP tools will be implemented using TypeScript and Zod schemas, consuming the shared `core/` business logic.

**Benefits of MCP Integration:**
- Accessible from Claude Desktop app
- Type-safe tool schemas with Zod
- Reusable across multiple MCP clients
- Shares core logic with Plugin API

See `README.md` Phase 2 roadmap for details.
