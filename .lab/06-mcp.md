# Part 6: GitHub MCP Server Integration

[📚 Lab Guide](GUIDE.md) • [← Plan Agent](05-plan-agent.md)

---

**Goal**: Extend Copilot with GitHub integration using MCP (Model Context Protocol).

---

## What is MCP?

MCP allows Copilot to interact with external tools and services. The GitHub MCP Server lets Copilot access your repositories, issues, pull requests, and more directly from the chat.

---

## Setup GitHub MCP Server

1. Open the **Copilot Chat** panel
2. Click the **wrench** icon to open Settings (it opens the **Tools** tab)
3. In the MCP settings:
   - Click **Browse MCP Servers**
   - Find and select **GitHub** from the registry
   - Click **Install**
4. Authenticate with GitHub when prompted
5. Select the GitHub account/organization you want to grant access to
6. In the **Tools** tab, the **Available MCP Tools** list will update automatically—confirm the GitHub MCP Server appears there

---

## Using GitHub MCP Server

Once the GitHub MCP Server is installed, try these prompts in Copilot Chat (Ask or Agent mode):

**Query 1: List Your Repositories**
```
List all repositories in my GitHub account
```

**Query 2: Check Pull Requests**
```
What are the open pull requests in this project?
```

**More Things You Can Try** (Optional):
- `Show me recent issues in the <repository-name> repository`
- `Generate release notes from commits`

---

## ✅ Part 6 Complete!

You've learned how to:
- Install the GitHub MCP Server
- Authenticate and configure MCP tools
- Query repositories and pull requests from Copilot Chat

---

[📚 Lab Guide](GUIDE.md) • [← Plan Agent](05-plan-agent.md)

👉 **[Continue to Part 7: Copilot Vision →](07-vision.md)**
