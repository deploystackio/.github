<a href="https://deploystack.io">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="/profile/deploystack-github-banner-dark.png">
    <source media="(prefers-color-scheme: light)" srcset="/profile/deploystack-github-banner-white.png">
    <img alt="DeployStack" src="/profile/deploystack-github-banner-white.png">
  </picture>
</a>

[DeployStack](https://deploystack.io) is an open-source Enterprise Control Plane for the Model Context Protocol (MCP) ecosystem. We provide secure, centralized management of AI agent tools, eliminating credential sprawl and enabling enterprise governance over the entire MCP landscape.

## The Problem We Solve 🎯

Enterprise MCP adoption faces critical security and governance blind spots. Developers copy-paste API keys into local files, organizations have zero visibility into AI tool usage, and complex configurations create onboarding nightmares. DeployStack transforms MCP into an enterprise-ready platform with centralized security and seamless developer experience.

## Our Solution ⚡

**Enterprise Control Plane:** Think of us as the Identity and Access Management (IAM) layer for AI agents and tools. Administrators manage all MCP servers and credentials in our cloud platform, while developers get instant access through our secure local gateway.

**Key Features:**
- 🔐 **Zero Credential Exposure** - Developers never touch API keys or tokens
- 🏢 **Enterprise Governance** - Complete visibility and control over AI tool usage
- ⚡ **Instant Developer Onboarding** - One login gives access to all authorized tools
- 🔒 **Zero-Trust Architecture** - All requests proxied through secure gateway
- 📊 **Audit & Compliance** - Full logging and analytics for your requirements (comming soon)
- 🌐 **Team-Based Access Control** - Granular permissions by team and role

## Architecture Overview 🏗️

**Control Plane (`cloud.deploystack.io`):** Centralized web platform for administrators to manage teams, MCP servers, credentials, and access policies.

**Data Plane (DeployStack Gateway):** Secure local application that runs on developer machines, providing a single endpoint for all MCP tools while enforcing enterprise policies.

```
VS Code/Cursor → DeployStack Gateway (localhost:9095/sse) → Persistent MCP Processes (stdio) → External APIs
```

## Repositories 🔧

Our open-source platform consists of three core services:

1. **[<img src="https://github.githubassets.com/favicons/favicon.png" width="15"> deploystack](https://github.com/deploystackio/deploystack):** Complete Enterprise Control Plane platform with backend API, frontend dashboard, and secure gateway

2. **[<img src="https://github.githubassets.com/favicons/favicon.png" width="15"> awesome-mcp-server](https://github.com/deploystackio/awesome-mcp-server):** Curated collection of enterprise-ready MCP servers

3. **[<img src="https://github.githubassets.com/favicons/favicon.png" width="15"> Documentation](https://github.com/deploystackio/documentation):** Comprehensive guides for enterprise MCP deployment and governance

## Get Started 🚀

- **For Organizations:** Sign up at [cloud.deploystack.io](https://cloud.deploystack.io) to create your free account
- **For Developers:** Install the DeployStack Gateway and connect to your team's authorized MCP tools
- **Documentation:** Visit [docs.deploystack.io](https://docs.deploystack.io) for complete setup guides

### Quick Start for Developers

```bash
# Install the gateway
npm install -g @deploystack/gateway

# Login to your organization
deploystack login

# Start the gateway with all your team's tools
deploystack start
```

Configure VS Code to use the single gateway endpoint:
```json
{
  "mcpServers": {
    "deploystack": {
      "url": "http://localhost:9095/sse",
      "name": "DeployStack Gateway"
    }
  }
}
```

## Contributing 💻

We're building the future of enterprise AI infrastructure. Whether you're a security engineer, DevOps specialist, or AI developer, your contributions help make AI tools secure and accessible for organizations worldwide.

### How You Can Contribute

- **Platform Development:** Enhance our [Control Plane services](https://github.com/deploystackio/deploystack) (Backend API, Frontend Dashboard, Gateway)
- **Security Features:** Help build enterprise-grade security and compliance features
- **MCP Server Integration:** Add support for new MCP servers in our catalog
- **Documentation:** Improve guides for enterprise deployment and governance
- **Bug Reports & Features:** Open issues to help us improve the platform

### Areas of Focus

- **Gateway Development:** SSE transport, process management, and security features
- **Enterprise Features:** Audit logging, SSO integration, and advanced analytics
- **MCP Ecosystem:** Integration with new MCP servers and AI agent frameworks

---

**Our Mission:** Secure AI tools. Empower developers. Control everything. We're transforming how enterprises manage their AI infrastructure by providing the first enterprise-grade control plane for the MCP ecosystem.

**Market Position:** #1 Enterprise Control Plane for MCP

Happy Building!

— The DeployStack Team
