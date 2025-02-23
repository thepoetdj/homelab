# Homelab Setup

Clone this repository on your system:

```bash
cd /opt
git clone https://github.com/thepoetdj/homelab.git
cd homelab
```

## Shell

### Oh My Posh

1. [Install](https://ohmyposh.dev/docs/installation/linux) `oh-my-posh`

2. Install `FiraCode Nerd Fonts`

```bash
oh-my-posh font install FiraCode
```

3. Add this line in `~/.zshrc` to load custom theme during oh-my-posh initialization:

```bash
eval "$(oh-my-posh init zsh --config /opt/homelab/ohmyposh/theme.omp.yaml)"
```

## Editors

### Zed

1. [Download](https://zed.dev/download) and install Zed editor

2. The zed settings of this repository requires `Catppuccin Theme` zed extension to be installed. Open `zed: extensions` (press `Ctrl + Shift + P`) and search for `Catppuccin Theme`

3. Create a symlink of `homelab/zed/settings.json`

```bash
mkdir ~/.config/zed && cd ~/.config/zed
ln -s /opt/homelab/zed/settings.json
```

**Note:** These settings will automatically change zed's active theme to `Catppuccin Mocha` along with ui & terminal fonts set to `FiraCode Nerd Font`

## Dev Tools

### mise

1. [Install](https://mise.jdx.dev/getting-started.html#installing-mise-cli) mise CLI

2. Add this at the end of `~/.zshrc` if not present already:

```bash
eval "$(/path/to/mise activate zsh)"
```

3. Create a symlink of `homelab/mise/config.toml`

```bash
mkdir ~/.config/mise && cd ~/.config/mise
ln -s /opt/homelab/mise/config.toml
```
