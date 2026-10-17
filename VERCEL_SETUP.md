# Vercel MCP Setup Guide

## ✅ Connected Successfully!

Vercel MCP is now integrated with Devin CLI. You can use Devin to manage your Vercel deployments directly.

## Available Tools

### Documentation & Search
- **search_vercel_documentation** - Search Vercel docs for any topic

### Project Management
- **get_git_deployment_context** - List teams, projects, and Git connections
- **create_git_project** - Create/link a Vercel project to your GitHub repo
- **list_teams** - List all your Vercel teams
- **list_projects** - List projects in a team
- **get_project_details** - Get detailed project information

### Deployments
- **list_deployments** - View all deployments for a project
- **get_deployment_details** - Get detailed deployment info
- **get_deployment_status** - Check deployment status
- **get_deployment_events** - View deployment events/logs
- **get_runtime_errors** - Get production runtime errors
- **get_runtime_logs** - Get application logs
- **create_deployment** - Deploy code to Vercel
- **promote_deployment** - Promote preview to production
- **rollback_deployment** - Rollback to a previous deployment

### Analytics & Monitoring
- **get_web_analytics** - Query Web Analytics data
- **get_analytics_metrics** - Get performance metrics

### Configuration
- **list_environment_variables** - View env vars
- **set_environment_variable** - Set env vars
- **list_domains** - View custom domains
- **list_edge_config** - View Edge Config stores

### Advanced
- **get_build_logs** - View build logs
- **get_cache_artifacts** - Manage cache
- **get_firewall_rules** - View security rules
- **get_audit_logs** - View team audit logs

## Quick Start Examples

### 1. Deploy Your 3D Project to Vercel

```bash
# In Devin, ask:
"Create a Vercel project for johnp792/3D and deploy it"
```

Devin will:
1. Create a Vercel project linked to your GitHub repo
2. Set up automatic deployments on every push
3. Create a preview deployment

### 2. Deploy Individual Folders

For each subfolder (liquid-gold, 5sense, getplate), create separate projects:

```bash
# Ask Devin:
"Create a Vercel project for johnp792/3D with root directory set to liquid-gold"
```

### 3. Check Deployment Status

```bash
# Ask Devin:
"Show me the latest deployments for my 3D project"
"Get the runtime errors from my production deployment"
```

### 4. Manage Environment Variables

```bash
# Ask Devin:
"Set the API_KEY environment variable to [value] for my 3D project"
```

## Next Steps

1. **Deploy to Vercel**: Ask Devin to create Vercel projects for your repos
2. **Monitor**: Use Devin to check deployment status and logs
3. **Iterate**: Push to GitHub → Vercel auto-deploys → Monitor with Devin

## Useful Commands

In a Devin session, you can now ask:

- "Deploy my 3D repo to Vercel"
- "Show me the latest deployment logs"
- "What's the status of my production deployment?"
- "Create a new Vercel project for [repo]"
- "Get the Web Analytics for my site"
- "Rollback to the previous deployment"

## Configuration

Your Vercel MCP is configured in:
- `.devin/mcp_config.json` (project-level)

OAuth credentials are stored securely and never committed to git.

## Learn More

- [Vercel MCP Docs](https://vercel.com/docs/agent-resources/vercel-mcp)
- [Vercel MCP Tools Reference](https://vercel.com/docs/agent-resources/vercel-mcp/tools)
