# Integrate MCP Server

A Model Context Protocol (MCP) server implementation for the Integrate project.

## Prerequisites

- Node.js 16+
- Neynar API key (for Farcaster access)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/NexusX-MCP/integrate-mcp-server.git
cd integrate-mcp-server
```

2. Install dependencies:
```bash
npm install
```

3. Copy the example environment file:
```bash
cp .env.example .env
```

4. Update the `.env` file with your configuration:
- You can obtain a Neynar API key from Neynar

## Usage

### Development

Start the development server:
```bash
npm run dev
```

### Production

Build the project:
```bash
npm run build
```

Start the production server:
```bash
npm start
```

## Configuration

The server can be configured through environment variables:

- `ENABLE_FARCASTER`: Enable/disable Farcaster integration (default: true)
- `NEYNAR_API_KEY`: Your Neynar API key
- `NODE_ENV`: Environment (development/production)

## Integration with Claude Desktop

To integrate with Claude Desktop, add the following to your Claude Desktop configuration file:

* macOS: ~/Library/Application Support/Claude/claude_desktop_config.json
* Windows: %APPDATA%\Claude\claude_desktop_config.json

```json
{
  "integrations": [
    {
      "name": "Integrate MCP",
      "type": "mcp",
      "path": "/full/path/to/integrate-mcp-server/dist/index.js",
      "enabled": true
    }
  ]
}
```

## Development

### Project Structure

```
integrate-mcp-server/
├── src/
│   ├── mcp/           # MCP protocol implementation
│   ├── providers/     # Content providers
│   ├── server.ts      # HTTP server
│   └── index.ts       # Entry point
├── test/             # Tests
└── package.json      # Project configuration
```

### Testing

Run the test suite:
```bash
npm test
```

Run tests in watch mode:
```bash
npm test -- --watch
```

### Linting

Run the linter:
```bash
npm run lint
```

Fix linting issues:
```bash
npm run lint:fix
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

DelbertHesselink <DelbertHesselink86032@outlook.com>

## Changelog

### [1.0.0] - 2025-Mar-10
- Initial release
- Basic MCP server implementation
- Farcaster integration

### [1.0.1] - 2025-Mar-19
- Added support for thread conversations
- Improved error handling
- Updated dependencies

### [1.0.2] - 2025-Mar-21
- Added user profile support
- Improved search functionality
- Bug fixes

### [1.0.3] - 2025-Mar-24
- Added trending topics support
- Performance improvements
- Documentation updates 