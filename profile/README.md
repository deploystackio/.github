<a href="https://deploystack.io">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="/profile/deploystack-github-banner-dark.png">
    <source media="(prefers-color-scheme: light)" srcset="/profile/deploystack-github-banner-white.png">
    <img alt="DeployStack" src="/profile/deploystack-github-banner-white.png">
  </picture>
</a>

**Turn MCP from "complex to set up" into "just add a URL"**

[DeployStack](https://deploystack.io) is an open-source MCP management platform that solves two critical problems stopping teams from adopting AI agents: credential sprawl and context window exhaustion.

## The Problems We Solve

### Problem 1: Credential Chaos

Every developer has API keys scattered across local config files. No one knows which credentials need rotation, who's using what tools, or whether keys are exposed in git repos.

Onboarding a new developer? Good luck walking them through installing 10+ MCP servers and configuring credentials for each one.

### Problem 2: Context Window Crisis

Here's what happens when you install multiple MCP servers locally:

- 10 servers with 15 tools each = ~75,000 tokens consumed **before you even start working**
- Claude Code users report 82,000 tokens (41% of context window) eaten by MCP tools at startup
- That leaves minimal space for actual work and degrades LLM accuracy

You're paying for context window tokens just to load tool definitions.

## The Solution

### Just Add a URL

Instead of installing individual MCP servers, configure one HTTPS URL in your MCP client. That's it.

All credentials stay in an encrypted vault. Your team gets instant access to MCP servers. New developers onboard in minutes, not hours.

### Hierarchical Router (The Technical Breakthrough)

Instead of loading 150 tools that consume 75,000 tokens, we expose 2 meta-tools that use only 1,372 tokens:

- `discover_mcp_tools` - Search for tools using keywords
- `execute_mcp_tool` - Run any discovered tool

**That's a 98.3% token reduction** while maintaining full functionality.

Your AI agent discovers tools on-demand instead of loading everything upfront. You get your context window back for actual work.

## Key Features

- **Zero Installation** - Single URL configuration vs. installing 10+ servers
- **Encrypted Credential Vault** - API keys never touch developer machines
- **Team Isolation** - Role-based access control and audit logging
- **Usage Analytics** - See which tools your team actually uses
- **1,000+ MCP Servers** - Ready to use without individual setup

## Repositories

**[deploystack](https://github.com/deploystackio/deploystack)** - Main platform with backend API, frontend dashboard, and satellite service

**[documentation](https://github.com/deploystackio/documentation)** - Deployment guides and API documentation

## Getting Started

**For Teams:**
1. Sign up at [cloud.deploystack.io](https://cloud.deploystack.io)
2. Add credentials for the MCP servers you want to use
3. Share the deployment URL with your team

**For Developers:**
1. Add the DeployStack URL to your MCP client config
2. Authenticate once
3. Start using tools immediately

**For Self-Hosting:**
Check [docs.deploystack.io](https://docs.deploystack.io) for deployment guides.

## Contributing

We're building open infrastructure for AI agents. Whether you're working on security, DevOps, or AI tooling, contributions are welcome.

**Areas where we need help:**
- Satellite service optimization and reliability
- Enterprise features (SSO, advanced audit logging)
- MCP server integrations and catalog expansion
- Documentation and deployment guides
- Testing and bug reports

Check [CONTRIBUTING.md](https://github.com/deploystackio/deploystack/blob/main/CONTRIBUTING.md) in the main repo for details.

## By The Numbers

- **100+** teams using DeployStack worldwide
- **98.3%** token reduction vs. traditional MCP setup
- **Open source** since the beginning

---

**Questions?** Join our [Discord community](https://discord.gg/42Ce3S7b3b) or check the [documentation](https://docs.deploystack.io).

— The DeployStack Team
