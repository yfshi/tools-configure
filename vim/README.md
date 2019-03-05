# vim配置

## ctags
```shell
yum install ctags
```

## 插件
把plugins/ctrlp/*拷贝到$HOME/.vim目录下

## 编辑$HOME/.vimrc或者把vimrc拷贝到$HOME/.vimrc
"""""""""""""""""""""""""""""""""""""""""""""
"                common                     "
"""""""""""""""""""""""""""""""""""""""""""""
set autoindent
set cindent
set tabstop=4 shiftwidth=4 noexpandtab
set encoding=utf-8 fileencodings=ucs-bom,utf-8,cp936,gb18030,big5,euc-jp,euc-kr,latin1
set nocompatible
set number

"""""""""""""""""""""""""""""""""""""""""""""
"                ctrlp                      "
"""""""""""""""""""""""""""""""""""""""""""""
let g:ctrlp_map = '<c-p>'
let g:ctrlp_cmd = 'CtrlP'
let g:ctrlp_by_filename = 1
let g:ctrlp_regexp = 1
let g:ctrlp_working_path_mode = '0'
let g:ctrlp_match_window = 'bottom,order:btt,min:1,max:100,results:100'
let g:ctrlp_extensions = ['tag']
:map <F7> <ESC>:CtrlPTag<CR>
:imap <F7> <ESC>:CtrlPTag<CR>
:cmap <F7> <ESC>:CtrlPTag<CR>
