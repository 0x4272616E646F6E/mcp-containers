FROM denoland/deno:alpine

# Set working dir
WORKDIR /app

# Create non-root user
RUN adduser --disabled-password --gecos "" mcp

# Switch to the non-root user
USER mcp

# Expose port
EXPOSE 3001

# Run
CMD ["deno", "run", "--config=deno.json", "--lock=deno.lock", "-N", "-R=node_modules", "-W=node_modules", "--node-modules-dir=auto", "jsr:@pydantic/mcp-run-python", "sse"]