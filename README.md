## tmux/fzf menu

Just your typical fzf menu which also works within tmux as a popup menu.

This project has a fair few hardcoded directories within the scripts so keep that in mind.
For example, the todo script manipulates an obsidian markdown file (hardcoded file location).

Any script with "(wrapper)" within the name automatically gets ran as `tmux popup -E sh EXAMPLE_SCRIPT` if ran within a tmux environment.
Any name appended to the menu will just run as a typical binary file.
Any other script will just get ran using the typical `sh EXAMPLE_SCRIPT`.

#### Installation

```bash
git clone git@github.com:TheStutterNerd/fzfmenu.git ~/.config/tsn/scripts/tmux/menu
```

#### Tmux binding

`bind-key a run-shell -b "/home/$USER/.config/tsn/scripts/tmux/menu/run"`

Above example binding is: Leader + a

#### Script list

- applications (currently only i3 dmenu)
- clipboard (uses tmux paste buffer, otherwise uses xclip)
- configs (hardcoded key names and locations to open within nvim)
- emojis (emoji selector)
- projects (currently only lists folders/files, not finished yet)
- todos (obsidian fzf todo script to add, delete and toggle completion)
- lazygit(wrapper) - wrapper to cd to the correct working directory before executing
- mycli(wrapper) - wrapper to accept input before executing
- ollama(wrapper) - wrapper to accept input before executing
- taskell(wrapper) - wrapper to cd to the correct working directory before executing
