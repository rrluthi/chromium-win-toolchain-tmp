# Temporary Chromium Windows toolchain packager

This public repository exists only to package a Windows VS/SDK toolchain for a
Chromium cross-build. It contains no application code and no secrets.

The workflow:

1. installs the Windows SDK and debugging tools on a GitHub-hosted Windows runner
2. packages Visual Studio 2026 + the SDK with Chromium's `depot_tools`
3. uploads the resulting toolchain zip directly to a build droplet over SSH
4. does not publish the toolchain as a public artifact

The repository can be deleted after the toolchain is uploaded.
