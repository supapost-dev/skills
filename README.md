# Supapost Skills

Agent skills for [Supapost](https://supapo.st) — the end-to-end studio for AI-native content creators. These skills teach coding agents (Claude Code, Cursor, OpenCode, OpenClaw, Cline, and any other tool that supports the [Agent Skills](https://github.com/vercel-labs/skills) convention) how to drive Supapost through its MCP server.

## Install

```bash
npx skills add supapost-dev/skills
```

Or pull a single skill directly from supapo.st:

```bash
npx skills add https://supapo.st/skill.md
```

## Skills in this repo

| Skill | Description |
| --- | --- |
| [`supapost`](./supapost/SKILL.md) | Generate images and video, manage AI influencers, build TikTok slideshows, and schedule posts across connected social accounts. |

## Connect the MCP

Installing a skill teaches the agent how Supapost works — it doesn't connect the actual tools. Create an API key at [supapo.st/settings/developer](https://supapo.st/settings/developer), then register the remote MCP:

```bash
claude mcp add --transport http supapost \
  https://api.supapo.st/mcp \
  --header "Authorization: Bearer sp_..."
```

See each skill's `SKILL.md` for the full setup and tool reference.

## Links

- Product: https://supapo.st
- Developer portal: https://developers.supapo.st
- stdio MCP package: https://www.npmjs.com/package/@supapost/mcp

## License

MIT
