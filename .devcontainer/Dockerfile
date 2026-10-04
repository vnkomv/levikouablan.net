# See here for image contents: https://github.com/devcontainers/images/tree/main/src/go

# [Choice] Go version (Debian bookworm or newer is required by current Hugo extended builds)
ARG VARIANT="1-bookworm"
FROM mcr.microsoft.com/devcontainers/go:${VARIANT}

# Keep in sync with HUGO_VERSION in netlify.toml
ARG HUGO_VERSION="0.167.0"
RUN wget -qO hugo.tar.gz https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_extended_${HUGO_VERSION}_linux-amd64.tar.gz \
    && mkdir hugo \
    && tar -xzf hugo.tar.gz -C hugo \
    && cp hugo/hugo /usr/local/bin \
    && rm -rf hugo hugo.tar.gz
