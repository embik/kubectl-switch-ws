# kubectl-switch-ws
A `kubectl` plugin to quickly switch kcp workspaces interactively.

![kubectl-switch-ws demo](./docs/kubectl-switch-ws.gif)

## Installation

### Prequisites

To run this `kubectl` plugin you need:

- Bash
- [fzf](https://github.com/junegunn/fzf)
- [kubectl-workspace](https://github.com/kcp-dev/kcp/tree/main/cli/cmd/kubectl-workspace) ([Installation instructions](https://docs.kcp.io/kcp/main/setup/kubectl-plugin/))

### Krew

This installation method requires [krew](https://krew.sigs.k8s.io/) installed.

Add the [krew index](https://github.com/embik/krew-index) and synchronize the local copy of it:

```
$ kubectl krew index add embik https://github.com/embik/krew-index.git
$ kubectl krew update
```

kubectl-switch-ws can now be installed with the following command:

```
$ kubectl krew install embik/switch-ws
```

### Manual

Copy [kubectl-switch\_ws](./kubectl-switch_ws) into our `$PATH` (e.g. `~/bin` or `~/.local/bin`, depending on your system setup).

## Usage

Run `kubectl switch-ws` to start the interactive workspace switcher. Navigate the list of child workspaces in the current workspace and press enter to switch to a specific workspace.

Use the pseudo element `[parent]` to go up one level.

Use `[exit]` or press ESC when you have reached the workspace you intended to navigate to.
