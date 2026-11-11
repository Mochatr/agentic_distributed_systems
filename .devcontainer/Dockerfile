FROM mcr.microsoft.com/devcontainers/java:1-21-bookworm

# The base image ships a Yarn apt source whose signing key has expired, which makes
# every `apt-get update` (and so every apt-based dev container feature) fail.
# Yarn is not needed here, so remove that source.
RUN grep -rl yarnpkg /etc/apt/sources.list.d/ | xargs -r rm -f
