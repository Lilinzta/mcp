# ScreenshotOne MCP Server

An official implementation of an [MCP (Model Context Protocol)](https://modelcontextprotocol.io/) server for [ScreenshotOne](https://screenshotone.com).

[A few more words about why it was built and some thoughts about the future of MCP](https://screenshotone.com/blog/mcp-server/).

## Tools

-   `render-website-screenshot`: Render a screenshot of a website and returns it as an image.

## Usage

### Build it

Always install dependencies and build it first:

```bash
npm run install && npm run build
```

### Get your ScreenshotOne API key

Sign up at [ScreenshotOne](https://screenshotone.com) and get your API key.

### With Claude for Desktop

Add the following to your `~/Library/Application\ Support/Claude/claude_desktop_config.json`:

```json
{
    "mcpServers": {
        "screenshotone": {
            "command": "node",
            "args": ["path/to/screenshotone/mcp/build/index.js"],
            "env": {
                "SCREENSHOTONE_API_KEY": "<your api key>"
            }
        }
    }
}
```

### Standalone or for other projects

```bash
SCREENSHOTONE_API_KEY=your_api_key && node build/index.js
```

## License

`ScreenshotOne MCP Server` is licensed [LICENSE](under the MIT License).
