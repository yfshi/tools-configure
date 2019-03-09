# vim配置

## 安装cscope
```shell
yum install cscope
```

## 编辑$HOME/.vimrc或者把vimrc拷贝到$HOME/.vimrc
```shell
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
"                cscope                     "
"""""""""""""""""""""""""""""""""""""""""""""
```shell
let g:cswin = 0
function! OpenCloseQuickfix()
	if g:cswin == 1
		exec 'cclose'
		let g:cswin = 0
	else
		exec 'vert copen 30'
		let g:cswin = 1
	endif
endfunction

set cscopequickfix=s-,c-,d-,i-,t-,e-

:map <F11> :!cscope -RbCkq<CR><CR>
:map <F12> :!cscope -u<CR><CR>
:map <F8> :call OpenCloseQuickfix()<CR><C-w>w<CR>
:map <C-j> :cnext<CR>
:map <C-k> :cprev<CR>
:map <F7> :cs find s <C-R>=expand("<cword>")<CR><CR>
:map <F6> :cs find t <C-R>=expand("<cword>")<CR><CR>
```
