# Zed Configs and Extensions

## Configs

Copy settings file to the zed config directory:

```zsh

> cp common/applications/zed/config/*.json ~/.config/zed/

```

## Working Extensions

These extensions work well and are essential:

```

dart
docker-compose
dockerfile
html
java
julia
latex
lua
make
pylsp
r
ruby
sql
toml
zig


```

## Theme Extensions

These extensions work well and are optional:

```

adwaita-pastel
catppuccin
catppuccin-icons
new-darcula
sublime-mariana-theme
vscode-classic-theme
vscode-dark-modern
vscode-dark-plus

```

## Problem Extensions

These extensions do not play nicely with other extensions:

```
...

```

## Example Keymap Config

```

// Zed keymap
//
// For information on binding keys, see the Zed
// documentation: https://zed.dev/docs/key-bindings
//
// To see the default key bindings run `zed: open default keymap`
// from the command palette.
[
  {
    "context": "Workspace",
    "bindings": {
      // "shift shift": "file_finder::Toggle"
    }
  },
  {
    "context": "Editor && vim_mode == insert && !menu",
    "bindings": {
      // "j k": "vim::SwitchToNormalMode"
    }
  }
]


```
