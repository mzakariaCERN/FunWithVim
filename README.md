# FunWithVim

On my winows machine, I had a problem setting ```_vimrc```. I couldn't change the file. The solution was installing vim outside Program Files (86) to my user name. Then as vim where does it read from

```
:version
```

and check
```
:echo $HOME
```

and from there I made _gvimrc 

```
"MZ curated vim settings
if has('gui_running')
  set guifont=Lucida_Console:h18
"This tells vim, everytime I start gVim to chose font Lucida Console and the font size should be 18
  
  endif
  
"set indentation  
set autoindent

"check syntax
syntax enable  

" below are from https://dougblack.io/words/a-good-vimrc.html                                                           
" UI Layout {{{ 
set number              " show line numbers
set showcmd             " show command in bottom bar 
set cursorline        " highlight current line 
set wildmenu                        
set lazyredraw      
set showmatch           " higlight matching parenthesis 
""set fillchars+=vert:| "don't know what this deos                                                                      " }}}                                                                                                                                                                                                                                           "colorscheme badwolf         " awesome colorscheme                                                                                                                                                                                              set tabstop=4       " number of visual spaces per TAB           

filetype indent on      " load filetype-specific indent files

set incsearch           " search as characters are entered
set hlsearch            " highlight matches

" turn off search highlight
nnoremap <leader><space> :nohlsearch<CR>


"move all backup files to temp
set backup
set backupdir=~/.vim-tmp,~/.tmp,~/tmp,/var/tmp,/tmp
set backupskip=/tmp/*,/private/tmp/*
set directory=~/.vim-tmp,~/.tmp,~/tmp,/var/tmp,/tmp
set writebackup

```


In the .vimrc file, line comments are made by adding a double quote " to the left of the text, this means that everything to the right of the " is a comment; multiline comments can't be made in the .vimrc file except adding a " to the beginning of each line, thus resulting in multiple single-line comment unlike C


## Resource

And excellent explanation of some great vimrc settings https://dougblack.io/words/a-good-vimrc.html
