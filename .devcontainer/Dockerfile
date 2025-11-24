# .devcontainer/Dockerfile

# Build stage - install Python OS as 3.13 packages
FROM python:3.13-slim-trixie AS builder
COPY --from=ghcr.io/astral-sh/uv:0.8.20 /uv /uvx /bin/

# Set UV environment for build
ENV UV_COMPILE_BYTECODE=1
ENV UV_LINK_MODE=copy

# Copy project files and install packages
COPY pyproject.toml uv.lock ./
RUN uv sync --frozen

# Runtime stage - minimal final image
FROM python:3.13-slim-trixie

# Install only essential system dependencies
RUN apt-get update && apt-get install -y \
    git \
    && rm -rf /var/lib/apt/lists/*

# Create user and setup workspace
RUN useradd --create-home --shell /bin/bash vscode
USER vscode
WORKDIR /home/vscode

# Copy virtual environment from builder and make it writable
COPY --from=builder --chown=vscode:vscode .venv .venv
RUN chmod -R u+w .venv

# Setup Jupyter kernel and shell activation
RUN .venv/bin/python -m ipykernel install --user --name L2D-VE --display-name "L2D-VE" && \
    ls -la ~/.local/share/jupyter/kernels/