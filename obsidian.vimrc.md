" Have j and k navigate visual lines rather than logical ones
nmap j gj
nmap k gk
" I like using H and L for beginning/end of line
nmap H ^
nmap L $

" turn hybrid line numbers on
:set number relativenumber
:set nu r

" Smart way to move between windows
map <C-j> <C-W>j
map <C-k> <C-W>k
map <C-h> <C-W>h
map <C-l> <C-W>l

" Yank to system clipboard
set clipboard=unnamed