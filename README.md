# Add Copyright for Vim

vim-copyright is a plug for your file to add/update copyright by bbxytl.

## Installation

Copy the file on your .vim/plug folder.

### Vundle

```
Bundle "OceanEyeFF/vim-copyright"
```
### VimPlug

```
Plug 'OceanEyeFF/vim-copyright'
```

## Useg

add the config to your .vimrc to set your name / email :

```
let g:file_copyright_company = "your company, default: null"
let g:file_copyright_rights = "custom_rights, default:'All rights reserved.'"
let g:file_copyright_name = "your nam e"
let g:file_copyright_email = "your email"

" auto update copyright when save file. Default: 1; 0:close auto.
let g:file_copyright_auto_update = 1
```

### HotKey

- use `:CopyrightAdd` to add copyright for your file.
- use `:CopyrightUpdate` to update copyright.
- use `nmap uh :CopyrightUpdate<cr>` to your .vimrc file as hotkey.

### CustomConfig

add the config to auto add copyright to your file:

Default:
```
let g:file_copyright_auto_filetypes = [
        \ 'sh', 'plx', 'pl', 'pm', 'py', 'python',
        \ 'h', 'hpp', 'c', 'cpp', 'java',
        \ 'ruby', 'rb', 'rake',
        \ 'uml', 'plantuml'
        \ 'go',
        \ 'markdown', 'md', 'pandoc',
]
```

custom filetype:
```
let g:file_copyright_auto_filetypes = [
        \ 'py', 'python'
]
```

you can set comment_prefix map:

```

let g:file_copyright_comment_prefix_map_default = {
      \"python": "\#", "py":"\#",
      \"cpp":"/*", "c":"/*", "h":"/*", "hpp":"/*",
      \"go":"/*",
      \"vim":"\"", "vim9script": "\#",
      \"sh":"\#", "shell":"\#",
      \"ruby":"\#", "rb":"\#", "rake":"\#",
      \"uml":"/'", "plantuml":"/'",
\}

let g:file_copyright_comment_mid_prefix_map_default = {
      \"python": "\#", "py":"\#",
      \"cpp":"\#", "c":"\#", "h":"\#", "hpp":"\#",
      \"go":"\#",
      \"vim":"\"", "vim9script": "\#",
      \"sh":"\#", "shell":"\#",
      \"ruby":"\#", "rb":"\#", "rake":"\#",
      \"uml":"'", "plantuml":"'",
      \"md":"", "markdown":"", "pandoc":"",
\}

let g:file_copyright_comment_end_map_default = {
      \"cpp":"*/", "c":"*/", "h":"*/", "hpp":"*/",
      \"go":"*/",
      \"uml":"'/", "plantuml":"'/",
\}

```

or set for filetype(default):

```
    let g:file_copyright_comment_prefix = "\#"
    let g:file_copyright_comment_mid_prefix = "\#"
    let g:file_copyright_comment_end = ""
```


## Copyright.eg

- python file:

```
# ====================================================
#   Copyright (C) 2018 All rights reserved.
#
#   Author        : your name
#   Email         : your email
#   File Name     : eg.py
#   Last Modified : 2024-09-09 13:17
#   Describe      :
#
# ====================================================
```

- cpp file:

```
/* ====================================================
#   Copyright (C) 2018 All rights reserved.
#
#   Author        : your name
#   Email         : your email
#   File Name     : README.md
#   Last Modified : 2018-04-06 14:27
#   Describe      :
#
# ====================================================*/
```





