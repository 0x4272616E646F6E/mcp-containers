# MCP-SSE-Containers

A collection of Model Context Protocol (MCP) Server-Sent Events (SSE) containers for seamless integration with AI applications. This repository makes these containers available when the original authors did not publish official container images.

## Overview

These containers implement the MCP protocol via Server-Sent Events, allowing for easy integration with LLM applications. Each container is packaged as a Docker image with all necessary dependencies.

## Available Containers

### context7
- **Source**: [upstash/context7](https://github.com/upstash/context7)
- **Description**: A vector embeddings service for semantic search and retrieval
- **Port**: 3000
- **Base Image**: Node.js 18 Alpine

### run-python
- **Source**: [pydantic/pydantic-ai/mcp-run-python](https://github.com/pydantic/pydantic-ai/tree/main/mcp-run-python)
- **Description**: Run Python code securely in a sandboxed environment
- **Port**: 3001
- **Base Image**: Deno Alpine

## Usage

To build and run these containers locally:

```bash
# Example
cd context7
docker build -t mcp-context7 .
docker run -p 3000:3000 mcp-context7

