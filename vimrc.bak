"Intendation fixes
set smartindent
set shiftwidth=4

" Highlight and Incremental Searches
set incsearch
set hlsearch
" Better splits with :split , :new (Horizontally) and :vsplit (Vertically)
set splitbelow
set splitright

" Saving unsaved Buffers
set hidden

" Increasing scroll offs
set scrolloff=8

" Setting undofile file and to use UndoTreeToggle Plugin for Git like
" UndoHistory - 'Undo History with F5'
set undofile
set undodir=~/.vim/undo

" Case insensitive searches
set ignorecase
set smartcase

"Unicode Support
set encoding=utf-8

"Modifying lines and numbers
set number
set numberwidth=4

"Title and Background
set title

" Enable Mouse (Use y , d and p for copy , cut , paste in mouse visual mode)
set mouse=a

"Colors
syntax on
"set termguicolors

"Modifying Tab Spaces , number of spaces in a <Tab>
set tabstop=4
set softtabstop=4
set expandtab




"  Intalling vim-plug For Plugins manager: `curl -fLo ~/.vim/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim`
" Commands To Add Plugins

" NERDTree for Tree syntax of directory , AirLine for interface theme
call plug#begin()
Plug 'preservim/NERDTree'
Plug 'vim-airline/vim-airline'
Plug 'gruvbox-community/gruvbox'
Plug 'mbbill/undotree'
call plug#end()

" Commands to Install and Update Plugins: `:PlugInstall`  , `:PlugUpdate`
" Plugin Name to execute Plugin like: `:NERDTree`


"Mapping Commands

" Map Ctrl + Left Arrow to go to the previous tab
noremap <C-l> :tabp<CR>

" Map Ctrl + Right Arrow to go to the next tab
noremap <C-k> :tabn<CR>

" Map Ctrl + N to create a new tab
noremap <C-n> :tabnew<CR>

" Map Ctrl + W to close the current tab
noremap <C-w> :tabclose<CR>

" Map Ctrl + T to toggle NERDTree
noremap <C-t> :NERDTreeToggle<CR>

" F5 for Undo History
nnoremap <F5> :UndotreeToggle<CR>

"NERDTree Commands and Shortcuts

" Start NERDTree when Vim is started without file arguments.
autocmd StdinReadPre * let s:std_in=1
autocmd VimEnter * if argc() == 0 && !exists('s:std_in') | NERDTree | endif

" Start NERDTree. If a file is specified, move the cursor to its window.
autocmd StdinReadPre * let s:std_in=1
autocmd VimEnter * NERDTree | if argc() > 0 || exists("s:std_in") | wincmd p | endif

" Mirror the NERDTree before showing it. This makes it the same on all tabs.
nnoremap <C-n> :NERDTreeMirror<CR>:NERDTreeFocus<CR>

" If another buffer tries to replace NERDTree, put it in the other window, and bring back NERDTree. (Code not runs in NERDTree)
autocmd BufEnter * if bufname('#') =~ 'NERD_tree_\d\+' && bufname('%') !~ 'NERD_tree_\d\+' && winnr('$') > 1 |
    \ let buf=bufnr() | buffer# | execute "normal! \<C-W>w" | execute 'buffer'.buf | endif

" Close the tab if NERDTree is the only window remaining in it.
autocmd BufEnter * if winnr('$') == 1 && exists('b:NERDTree') && b:NERDTree.isTabTree() | quit | endif



" GruvBox Theme Settings
"Dark / Light
set background=dark

" Gruvbox configuration options (Hard , medium , soft)
let g:gruvbox_contrast_dark = 'hard'
let g:gruvbox_contrast_light = 'hard'
let g:gruvbox_invert_selection = 1        " Visuals must be super cool
let g:gruvbox_termcolors = 256             " Terminal colors

" Horizontal and vertical cursor line
set cursorline
"set cursorcolumn       " For vertical Line, if needed

" Maybe Change Font in future
if has("gui_running")
    set guifont=Monospace\ 15
endif

" Customizing Visual Mode (BCz I love highlightings) 
highlight Visual guibg=#504945 cterm=bold
highlight VisualNOS guibg=#7c6f64 cterm=bold

" Setting Folds and Opeing all (Folds of classes, funcs like in vscode)
set foldmethod=syntax
set foldlevel=99

" color scheme
colorscheme gruvbox

" Add codium for autocomplete
" Add https://github.com/junegunn/fzf?tab=readme-ov-file#vimneovim-plugin
