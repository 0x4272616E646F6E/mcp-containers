FROM node:18-alpine

# Install the latest version globally
RUN npm install -g @upstash/context7-mcp@latest

# Set working dir
WORKDIR /app

# Create non-root user
RUN adduser --disabled-password --gecos "" mcp

# Switch to the non-root user
USER mcp

# Expose port
EXPOSE 3000

# Run
CMD ["context7-mcp"]