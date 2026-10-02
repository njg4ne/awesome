# Development

[← Back to all awesomes](../README.md)

## Contents

1. [Containers](#containers)
2. [Package Managers](#package-managers)
3. [Operating Systems and Shells](#operating-systems-and-shells)
4. [Terminal](#terminal)
5. [Code Editors](#code-editors)
6. [Version Control](#version-control)

See also [AI-Assisted Programming](../ai/README.md).

## Containers

- [Podman](https://podman.io) is preferred over Docker and the other alternatives for [OCI](https://opencontainers.org) containers. It runs without a daemon and without root.
  - [Podman Desktop](https://podman-desktop.io) is a GUI for it.

### Container Practices

1. **Run tools in containers instead of installing them on the host computer.** It's more portable. It also keeps a bunch of hard-to-track software off the system. Everything lives in one place, so clearing it later is just a matter of emptying the image and container caches with [`podman system prune`](https://docs.podman.io/en/latest/markdown/podman-system-prune.1.html).
2. **Use file system (bind) mounts instead of named volumes.** Mount a real directory with [`-v ./dir:/dir`](https://docs.podman.io/en/latest/markdown/podman-run.1.html) rather than using a bespoke named volume.
3. **Pick small images, but keep familiar tools when it matters.** In rough order of preference:
   - [Debian](https://hub.docker.com/_/debian)-based images when it's necessary to get inside and use `sh`, `bash`, and `apt`
   - very small images, such as [Alpine](https://alpinelinux.org)-based ones
   - binary-only images, such as [distroless](https://github.com/GoogleContainerTools/distroless), that leave out unneeded OS parts

## Package Managers

- [pnpm](https://pnpm.io) is the preferred package manager for the Node.js ecosystem. It's fast and saves disk space by storing each package once and linking to it.

## Operating Systems and Shells

- [Ubuntu](https://ubuntu.com) or [Debian](https://www.debian.org) is the favorite Linux distribution, preferably on [LTS releases](https://ubuntu.com/about/release-cycle).
- On Windows:
  - [Git Bash](https://gitforwindows.org) is the preferred shell.
  - [PowerShell](https://learn.microsoft.com/powershell/) is not bad for some things.
  - [WSL 2](https://learn.microsoft.com/windows/wsl/) is nice, but sharing files between Windows and WSL 2 can get weird.

## Terminal

- [nano](https://www.nano-editor.org) is the terminal text editor of choice.
- [Herdr](https://herdr.dev) ([GitHub](https://github.com/herdrdev/herdr)) is a terminal multiplexer that knows about AI coding agents. It's like [tmux](https://github.com/tmux/tmux), but it also shows which agents are working, blocked, or done.
  - *Note:* It's a newer addition here, and some of its behavior still raises doubts.

## Code Editors

- [Visual Studio Code](https://code.visualstudio.com) is the main code editor here.
- [Zed](https://zed.dev) is a fast newer editor that's also pretty cool.

## Version Control

- [Git](https://git-scm.com), for better or worse, is the source control tool of choice, along with [GitHub](https://github.com).
