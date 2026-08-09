# Omarchy Overview

An external Omarchy Shell plugin that presents a fullscreen overview of
workspaces and their windows. It supports keyboard navigation, window
activation, and dragging windows between workspaces.

## Demo

https://github.com/user-attachments/assets/801a504a-c0d5-41f9-8cc2-a6e81ac64586



## Install

This directory is ready to use as the root of a plugin repository. To install
it locally for development:

```bash
mkdir -p ~/.config/omarchy/plugins
cp -R "omarchy overview" ~/.config/omarchy/plugins/omarchy-overview
omarchy-shell shell rescanPlugins
omarchy plugin enable omarchy-overview
```

For normal distribution, place these files in a Git repository and install it
with:

```bash
omarchy plugin add https://github.com/sanjyay/omarchy-overview.git
```

## Open

```bash
omarchy-shell shell toggle omarchy-overview '{}'
```

For example, add a Hyprland binding to your user bindings:

```lua
o.bind("SUPER + TAB", "Workspace overview", "omarchy-shell shell toggle omarchy-overview '{}'")
```

The plugin depends only on APIs and shared UI components provided by the
Omarchy Shell. It does not require `hyprexpo`, `hyprpm`, or client polling.
