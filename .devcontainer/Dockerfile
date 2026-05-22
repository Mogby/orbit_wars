FROM mcr.microsoft.com/devcontainers/python:3-3.14-trixie

# Install Node.js (needed for Claude Code)
RUN curl -fsSL https://deb.nodesource.com/setup_20.x | bash - \
    && apt-get install -y nodejs \
    && rm -rf /var/lib/apt/lists/*

# Install Claude Code globally
RUN npm install -g @anthropic-ai/claude-code

# Install Kaggle CLI for the vscode user
USER vscode
RUN pip install --user kaggle