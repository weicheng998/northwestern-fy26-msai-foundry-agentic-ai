# Assignments

## Week 3: Build Your Single Agent + Add External Tools

This week you'll build a single AI agent in Azure AI Foundry and extend it with external tools.

**Start here**: [Single Agent Architecture](single_agent_architecture.md) — Understand the problem and architecture before diving into the labs.

### Deliverables

| Component | Points |
|-----------|--------|
| Architecture diagram + brief reasoning | 15 pts |
| **Choose one:** | |
| → Create a Logic App and connect it to your agent | 10 pts |
| → Create an Azure Function and connect it to your agent | 15 pts |

**Total: 25-30 points** (depending on choice)

### Option A: Logic App (10 pts)

Build a Logic App workflow and connect it to your agent via HTTP.

| Step | Lab |
|------|-----|
| 1. Build your Logic App | [Lab 2: Logic Apps](../notebooks/lab2_logic_apps.ipynb) |
| 2. Connect to your agent | [Lab 3: Single Agent + HTTP Tools](../notebooks/lab3_single_agent_tool_calling.ipynb) |

### Option B: Azure Function (15 pts)

Build an Azure Function and connect it to your agent. You can choose **either** integration approach:

| Approach | Description | Labs |
|----------|-------------|------|
| **HTTP Tool** | Direct HTTP calls from agent to function | [Lab 1](../notebooks/lab1_azure_functions.ipynb) → [Lab 3](../notebooks/lab3_single_agent_tool_calling.ipynb) |
| **MCP Server** | Standardized MCP protocol with auto-discovery | [Lab 4](../notebooks/lab4_mcp_server_azure_functions.ipynb) → [Lab 5](../notebooks/lab5_single_agent_mcp_integration.ipynb) |

### HTTP vs MCP: Which Should I Choose?

| HTTP Tool | MCP Server |
|-----------|------------|
| Simpler to understand | Industry-standard protocol |
| Direct HTTP calls | Auto-discovery of tools |
| One tool per endpoint | Multiple tools per server |
| Good for learning basics | Better for production systems |

Both approaches use Azure Functions — the difference is *how* your agent connects to them.

### What to Submit

1. **Architecture diagram** — Show your agent, tools, and how they connect
2. **Brief reasoning** — Why did you choose this approach? What are the benefits?
3. **Working demo** — Screenshot or recording of your agent using the tool