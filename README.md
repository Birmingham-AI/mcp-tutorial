# MCP Tutorial

## Browser Tools MCP

**Note: you already have the BrowserTools & MCP-LOGO-GEN MCP servers in this directory, so you do not need to clone them again.**

1. Starting at step 2, follow the [BrowserTools MCP server](https://browsertools.agentdesk.ai/installation) installation steps.
2. Start the server.

### Experiment

1. Open /web-app/index.html in your browser as the focused tab.
2. Right click and click inspect. Click "BrowserToolsMCP".
3. In Cursor/Windsurf, copy the path to your current directory. Paste this in Screenshot Settings path.
4. Open your agent chat. Say `Our text colors do not look right. Take a screenshot and fix @index.html`

## Image Generation MCP

1. `cd MCP-LOGO-GEN` and follow the installation steps [MCP Logo Gen MCP server](https://github.com/sshtunnelvision/mcp-logo-gen).
2. Add your [FAL AI](https://fal.ai/) API key to a `.env` file in the root directory **of the MCP-LOGO-GEN server**. You can get one for free after registering.
3. Add the MCP server to your client configuration.
4. Run the server with `python run_server.py`.

## `mcp.json`

### MacOS

{
  "mcpServers": {
    "FAL Image": {
      "url": "<http://127.0.0.1:7777/sse>"
    },
    "browser-tools": {
      "command": "npx",
      "args": [
        "-y",
        "@agentdeskai/browser-tools-mcp@1.2.0"
      ],
      "enabled": true
    }
  }
}

### Windows

{
  "mcpServers": {
    "FAL Image": {
      "url": "<http://127.0.0.1:7777/sse>"
    },
    "browser-tools": {
      "command": "wsl",
      "args": [
        "bash",
        "-c",
        "cmd /c npx -y @agentdeskai/browser-tools-mcp@1.2.0"
      ],
      "enabled": true
    }
  }
}
