# MCP Streamable HTTP Sample

This repository provides sample code for the Streamable HTTP implementation of the Model Context Protocol (MCP).

## Overview

MCP (Model Context Protocol) is a communication protocol between clients and servers that supports multiple communication methods. This sample demonstrates an implementation using the Streamable HTTP method.

Streamable HTTP has the following characteristics:

- Sending messages via HTTP POST requests
- Establishing Server-Sent Events (SSE) streams via HTTP GET requests
- Stateful communication through session management

## Features

This sample includes the following features:

- Server-side:
  - Implementation of Streamable HTTP transport
  - Support for multiple client connections
  - Provision of tool functions (echo, add)
  - Session management

- Client-side:
  - Connection to the server
  - Retrieving tool lists
  - Invoking tools

## Prerequisites

- Node.js 18.x or higher
- npm or yarn

## Installation

```bash
# Clone the repository (including submodules)
git clone --recursive https://github.com/moritalous/mcp-streamablehttp-sample.git
cd mcp-streamablehttp-sample

# Install dependencies
npm install

# Set up TypeScript SDK
npm run setup
```

## Build

```bash
npm run build
```

## How to Run

### Starting the Server

```bash
npm run start:server
```

The server starts on port 3001 by default. You can change the port number by setting the `PORT` environment variable.

### Running the Client

```bash
npm run start:client
```

The client connects to `http://localhost:3001/mcp` by default. You can change the connection destination by setting the `MCP_SERVER_URL` environment variable.

## Development

Running in development mode:

```bash
# Server (development mode)
npm run dev:server

# Client (development mode)
npm run dev:client
```

## Project Structure

```
mcp-streamablehttp-sample/
├── src/
│   ├── client.ts     # Client implementation
│   └── server.ts     # Server implementation
├── typescript-sdk/   # MCP TypeScript SDK (Git submodule)
├── dist/             # Compiled code
├── package.json      # Project configuration
└── tsconfig.json     # TypeScript configuration
```

## License

MIT

## References

- [Model Context Protocol Specification](https://spec.modelcontextprotocol.io/)
- [MCP SDK Documentation](https://github.com/modelcontextprotocol/typescript-sdk)

*Note: A Japanese version of this README is available at [README_ja.md](README_ja.md)*
