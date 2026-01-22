# Deployment options

## Local install (recommended)
```bash
npm install
npm run build
```

## Global CLI install
```bash
npm install -g mermaid2visio
```

## Docker (headless CLI)
```bash
docker build -t mermaid2visio .
docker run --rm -i mermaid2visio - --output diagram.vsdx < diagram.mmd
```

If Chromium sandboxing is blocked in your environment, you can pass Puppeteer args:
```bash
export MERMAID2VISIO_PUPPETEER_ARGS='["--no-sandbox","--disable-setuid-sandbox"]'
```

## Server deployment
For MCP usage, run:
```bash
node dist/mcp/server.js
```
