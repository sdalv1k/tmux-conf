Copy the `.tmux.conf` file to the home directory.

Add this to ~/.bashrc if you want tmux to automatically start when opening a terminal

```
if command -v tmux &> /dev/null && [ -n "$PS1" ] && [[ ! "$TERM" =~ screen ]] && [[ ! "$TERM" =~ tmux ]] && [ -z "$TMUX" ]; then
  exec tmux
fi
```

Add this to specify the path of the plugins directory

```
export TMUX_PLUGIN_MANAGER_PATH="/home/sdalvik/.config/tmux/plugins/"
```