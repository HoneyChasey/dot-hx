# Helix Cheatsheet

Quick reference for the most useful default keybindings. Modes: **Normal** (default, press `Esc` to return), **Insert** (`i`), **Select** (`v`).

## Movement

| Key | Action |
| --- | --- |
| `h` `j` `k` `l` | Left / Down / Up / Right |
| `w` / `b` | Next / previous word start |
| `e` | Next word end |
| `f<char>` / `t<char>` | Find / till next char (whole file) |
| `Home` / `End` | Start / end of line |
| `G` | Go to line number `<n>` |
| `gg` | Go to start of file |
| `ge` | Go to end of file |
| `Ctrl-u` / `Ctrl-d` | Half page up / down |
| `Ctrl-o` / `Ctrl-i` | Jump backward / forward in jumplist |

## Selection

| Key | Action |
| --- | --- |
| `x` | Select current line, repeat to extend downward |
| `X` | Extend selection to full lines |
| `%` | Select entire file |
| `v` | Enter select/extend mode (then move to grow selection) |
| `;` | Collapse selection to a single cursor |
| `,` | Keep only the primary selection |
| `s` | Select all regex matches inside selection |
| `C` | Add a cursor on the next line |
| `Alt-C` | Add a cursor on the previous line |
| `Alt-o` / `Alt-i` | Expand / shrink selection to syntax node |

## Changes

| Key | Action |
| --- | --- |
| `i` / `a` | Insert before / after selection |
| `I` / `A` | Insert at start / end of line |
| `o` / `O` | Open new line below / above |
| `c` | Change (delete + insert mode) |
| `d` | Delete selection |
| `r<char>` | Replace with a character |
| `y` / `p` / `P` | Yank / paste after / paste before |
| `>` / `<` | Indent / unindent |
| `=` | Format selection (LSP) |
| `u` / `U` | Undo / redo |
| `Ctrl-c` | Toggle comments |
| `~` | Switch case |

## Copy / paste

**Internal registers** (stay inside Helix, not shared with other apps):

| Key | Action |
| --- | --- |
| `y` | Yank (copy) selection |
| `p` / `P` | Paste after / before selection |
| `d` | Delete selection (also yanks it) |
| `"<reg>` | Choose a register before yank/paste, e.g. `"ay` then `"ap` |

**System / host clipboard** (shared with the rest of your OS — copy here to paste into a browser, and vice versa):

| Key | Action |
| --- | --- |
| `Space y` | Yank selection to system clipboard |
| `Space Y` | Yank main selection only to system clipboard |
| `Space p` / `Space P` | Paste system clipboard after / before selection |
| `Space R` | Replace selection with system clipboard contents |

> Note: system clipboard support needs a clipboard provider (e.g. `wl-clipboard` on Wayland, `xclip`/`xsel` on X11, native on macOS/Windows). Run `hx --health clipboard` to check.

## Search

| Key | Action |
| --- | --- |
| `/` | Search for pattern |
| `n` / `N` | Next / previous match |
| `*` | Search for current selection |

## Goto mode (`g`)

| Key | Action |
| --- | --- |
| `gd` | Go to definition (LSP) |
| `gr` | Go to references (LSP) |
| `gi` | Go to implementation (LSP) |
| `gh` / `gl` | Start / end of line |
| `gn` / `gp` | Next / previous buffer |
| `ga` | Last accessed file |

## Window mode (`Ctrl-w`)

| Key | Action |
| --- | --- |
| `Ctrl-w w` | Switch to next window |
| `Ctrl-w h/j/k/l` | Move to left / bottom / top / right split |
| `Ctrl-w v` | Vertical split |
| `Ctrl-w s` | Horizontal split |
| `Ctrl-w q` | Close current window |
| `Ctrl-w o` | Close all other windows |
| `Ctrl-w H/J/K/L` | Swap window in that direction |

## Space mode (`Space`)

| Key | Action |
| --- | --- |
| `Space f` | File picker |
| `Space b` | Buffer picker |
| `Space g` | Changed files picker |
| `Space s` | Document symbols (LSP) |
| `Space r` | Rename symbol (LSP) |
| `Space a` | Code action (LSP) |
| `Space d` | Diagnostics picker (LSP) |
| `Space /` | Global search in workspace |
| `Space k` | Show docs for item under cursor (LSP) |
| `Space '` | Reopen last picker |
| `Space ?` | Command palette |

## Command mode (`:`)

| Command | Action |
| --- | --- |
| `:w` | Save |
| `:q` | Quit |
| `:wq` | Save and quit |
| `:o <path>` | Open file |
| `:theme <name>` | Change theme |
| `:config-reload` | Reload config |
| `:config-open` | Open config file |

---
*Run `hx --tutor` in a terminal for the built-in interactive tutorial.*
