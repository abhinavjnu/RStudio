FROM rocker/rstudio:latest

# Install additional system dependencies useful for R development
RUN apt-get update && apt-get install -y --no-install-recommends \
    curl \
    git \
    libcurl4-openssl-dev \
    libssl-dev \
    libxml2-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Disable RStudio authentication for Codespaces (access is already gated by GitHub)
ENV DISABLE_AUTH=true

EXPOSE 8787
