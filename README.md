sourse : https://gitlab.com/__tpb/monokai-pro.nvim

# Monokai Pro

A Neovim theme written in Lua ported from the Visual Studio Code [Monokai Pro](https://monokai.pro/vscode) theme.

## Default

![image](https://gitlab.com/__tpb/monokai-pro.nvim/uploads/998f64fc003422515847152292d86239/default.png)

## Machine

![image](https://gitlab.com/__tpb/monokai-pro.nvim/uploads/205b81bd3a1f14e6c9f32b534407e239/machine.png)

## Ristretto

![image](https://gitlab.com/__tpb/monokai-pro.nvim/uploads/77d6b0a4553d4c82a83f1548b0c0e204/ristretto.png)

## Octogon

![image](https://gitlab.com/__tpb/monokai-pro.nvim/uploads/214eff3f84f50a875b7ab3d3e6ee1f15/octogon.png)

## Spectrum

![image](https://gitlab.com/__tpb/monokai-pro.nvim/uploads/d02b24c06a323acb59d20ece2a5af33f/spectrum.png)

## Classic

![image](https://gitlab.com/__tpb/monokai-pro.nvim/uploads/0354540f85e597602919eddc058fbc3e/classic.png)

## Features

- supports the latest Neovim 5.0 features like TreeSitter and LSP
- minimal inactive statusline
- vim terminal colors
- darker background for sidebar-like windows
- **lualine** theme

### Plugin Support

- [TreeSitter](https://github.com/nvim-treesitter/nvim-treesitter)
- [LSP Diagnostics](https://neovim.io/doc/user/lsp.html)
- [LSP Trouble](https://github.com/folke/lsp-trouble.nvim)
- [LSP Saga](https://github.com/glepnir/lspsaga.nvim)
- [Git Signs](https://github.com/lewis6991/gitsigns.nvim)
- [Git Gutter](https://github.com/airblade/vim-gitgutter)
- [Telescope](https://github.com/nvim-telescope/telescope.nvim)
- [NvimTree](https://github.com/kyazdani42/nvim-tree.lua)
- [WhichKey](https://github.com/liuchengxu/vim-which-key)
- [Indent Blankline](https://github.com/lukas-reineke/indent-blankline.nvim)
- [Dashboard](https://github.com/glepnir/dashboard-nvim)
- [BufferLine](https://github.com/akinsho/nvim-bufferline.lua)
- [Lualine](https://github.com/hoob3rt/lualine.nvim)
- [Lightline](https://github.com/itchyny/lightline.vim)
- [Neogit](https://github.com/TimUntersberger/neogit)
- [vim-sneak](https://github.com/justinmk/vim-sneak)
- [navigator](https://github.com/ray-x/navigator.lua)
- [lsp_signature](https://github.com/ray-x/lsp_signature.nvim)

## Requirements

- Neovim >= 0.5.0

## Installation

Install the theme with your preferred package manager:

[vim-plug](https://github.com/junegunn/vim-plug)

```vim
Plug 'https://gitlab.com/__tpb/monokai-pro.nvim'
```

[packer](https://github.com/wbthomason/packer.nvim)

```lua
use 'https://gitlab.com/__tpb/monokai-pro.nvim'
```

NOTE: Currently installing a plugin from Gitlab on Windows with Packer is broken ((#858)[https://github.com/wbthomason/packer.nvim/issues/858])

UPDATE: Use alias as workaround for the Packer install issue

```lua
use {
  'https://gitlab.com/__tpb/monokai-pro.nvim',
  as = 'monokai-pro.nvim'
}
```

credit: https://github.com/wbthomason/packer.nvim/issues/858#issuecomment-1172869552

## Usage

Enable the colorscheme:

```vim
" Vim Script
colorscheme monokaipro
```

```lua
-- Lua
vim.cmd[[colorscheme monokaipro]]
```

To enable the `monokaipro` theme for `Lualine`, simply specify it in your lualine settings:

```lua
require('lualine').setup {
  options = {
    -- ... your lualine config
    theme = 'monokaipro'
    -- ... your lualine config
  }
}
```

To enable the `monokaipro` colorscheme for `Lightline`:

```vim
" Vim Script
let g:lightline = {'colorscheme': 'monokaipro'}
```

## Configuration

> ❗️ configuration needs to be set **BEFORE** loading the color scheme with `colorscheme monokaipro`

The theme comes with several filters:

- `default` the default Monokai Pro look
- `machine` a variant with a bluish background
- `ristretto` a variant with a red/brown background
- `octogon` a variant with a purple/indigo background
- `spectrum` a variant with a flat gray background
- `classic` a variant based on original Monokai colors

| Option                              | Default     | Description                                                                                                                                                     |
| ----------------------------------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| monokaipro_filter                   | `"default"` | The theme comes with six filters, `default`, `machine`, `ristretto`, `octogon` `spectrum`, and `classic`                                                        |
| monokaipro_terminal_colors          | `true`      | Configure the colors used when opening a `:terminal` in Neovim                                                                                                  |
| monokaipro_italic_comments          | `true`      | Make comments italic                                                                                                                                            |
| monokaipro_italic_keywords          | `true`      | Make keywords italic                                                                                                                                            |
| monokaipro_italic_functions         | `false`     | Make functions italic                                                                                                                                           |
| monokaipro_italic_variables         | `false`     | Make variables and identifiers italic                                                                                                                           |
| monokaipro_transparent              | `false`     | Enable this to disable setting the background color                                                                                                             |
| monokaipro_hide_inactive_statusline | `false`     | Enabling this option, will hide inactive statuslines and replace them with a thin border instead. Should work with the standard **StatusLine** and **LuaLine**. |
| monokaipro_sidebars                 | `{}`        | Set a darker background on sidebar-like windows. For example: `["vista_kind", "packer"]`                                                                        |
| monokaipro_flat_sidebar             | `false`     | When true sidebar like windows will use the normal background                                                                                                   |
| monokaipro_flat_float               | `false`     | When true float and diagnostic like windows will use the normal background                                                                                      |
| monokaipro_flat_term                | `false`     | When true the integrated terminal will use the normal background                                                                                                |
| monokaipro_colors                   | `{}`        | You can override specific color groups to use other groups or a hex color                                                                                       |

```lua
-- Example config in Lua
vim.g.monokaipro_filter = "machine"
vim.g.monokaipro_italic_functions = true
vim.g.monokaipro_sidebars = { "vista_kind", "packer" }
vim.g.monokaipro_flat_term = true

-- Change the "hint" color to the "orange" color, and make the "error" color bright red
vim.g.monokaipro_colors = { hint = "orange", error = "#ff0000" }

-- Load the colorscheme
vim.cmd[[colorscheme monokaipro]]
```

```vim
" Example config in VimScript
let g:monokaipro_filter = "machine"
let g:monokaipro_italic_functions = 1
vim.g.monokaipro_flat_term = 1
let g:monokaipro_sidebars = [ "vista_kind", "packer" ]

" Load the colorscheme
colorscheme monokaipro
```

## Functions

- Toggle the style live without the need to exit NeoVim

Just call the function for style switching

```vim
"Vim-Script
:lua require('monokaipro.functions').toggle_style()
"This command toggles the style
```

The command can also be mapped to a key for fast style switching

```vim
"Vim-Script:
nnoremap <C-m> :lua require('monokaipro.functions').toggle_style()<CR>
```

```lua
--Lua:
vim.api.nvim_set_keymap('n', '<C-m>', [[<Cmd>lua require('monokaipro.functions').toggle_style()<CR>]], { noremap = true, silent = true })
```

- Change the style to a desired one using the function change_filter("desired style")

```vim
"Vim-Script:
:lua require('monokaipro.functions').change_filter("ristretto")
"This command changes the style to palenight
```

The command can also be mapped to a key for fast style switching

```vim
"Vim-Script:
nnoremap <C-9> :lua require('monokaipro.functions').change_filter('default')<CR>
nnoremap <C-0> :lua require('monokaipro.functions').change_filter('classic')<CR>
```

```lua
--Lua:
vim.api.nvim_set_keymap('n', '<C-9>', [[<Cmd>lua require('monokaipro.functions').change_filter('default')<CR>]], { noremap = true, silent = true })
vim.api.nvim_set_keymap('n', '<C-0>', [[<Cmd>lua require('monokaipro.functions').change_filter('classic')<CR>]], { noremap = true, silent = true })
```

## Also check out

- [Sonokai](https://github.com/sainnhe/sonokai.vim) by [Sainnhe](https://github.com/sainnhe): a theme inspired by Monokai Pro but
  with lower contrast

## Contributing

All pull requests are welcome.

## Credits

Most of the credit for this theme should go to [folke](https://github.com/folke) and
[marko-cerovac](https://github.com/marko-cerovac) for the Tokyonight and material themes
respectively. I did a lot of yanking and pasting! :)
