set guifont=Inconsolata:h12
color solarized

set list                       " Show special characters
set backspace=indent,eol,start " Make backspace behave
set nohidden                   " Close the buffer when I close the tab
set splitright                 " Open vertical splits to the right
set splitbelow                 " Open horizontal splits to the bottom
"set foldmethod=syntax          " Fold based on the code at hand
"set foldnestmax=20             " Only fold three levels
set autoread                   " Read in changed files
set magic                      " Better regexes
set nobackup                   " Dont' worry about backing up files
set noswapfile
set vb                         " Tired of that noise.
set relativenumber             " Show relative line numbers
set gdefault                   " Search and replace entire buffer by default

" Highlight the current line
set cul
hi CursorLine term=none cterm=none ctermbg=5
 
" Use arrow keys to move buffers
map <up> <C-w>k<cr>
map <down> <C-w>j<cr>
map <left> <C-w>h<cr>
map <right> <C-w>l<cr>
 
" Search mappings: These will make it so that going to the next one in a
" search will center on the line it's found in.
map n Nzz
map n nzz
 
" Auto save on blur!
:au FocusLost * :wa
 
" Change window size with +/-
if bufwinnr(1)
  map + <C-W>+
  map - <C-W>-
endif
 
" Map \w to close a buffer
map <Leader>w :bd<cr>
 
" Map \r to :rspec
map <Leader>r :!rspec %<cr>
 
" Reindent the entire file
map <Leader>I gg=G``<cr>
 
" Show Gundo for awesome undo tree
map <Leader>u :GundoToggle<cr>
 
" I'm lazy.
map :WQ :wq<cr>
 
" I don't need RSI.
imap jj <Esc>:write<cr>
 
" Keep visual blocks around
vmap < <gv
vmap > >gv
 
" Automatically strip whitespace
autocmd! BufWrite * mark ' | silent! %s/\s\+$// | norm ''
 
" Don't search these directories via Command-T
set wildignore+=tmp,coverage,doc,script,log,autotest,.git
 
" Show git stuff in the status line
set statusline=%<%f\ %h%m%r%{fugitive#statusline()}%=%-14.(%l,%c%V%)\ %P
 
" When vimrc is edited, reload it
autocmd! bufwritepost vimrc.local source ~/.vimrc.local
 
" Remove the Windows ^M - when the encodings gets messed up
noremap <Leader>m mmHmt:%s/<C-V><cr>//ge<cr>'tzt'm
 
" Toggle folds with spacebar
"nnoremap <space> za
 
" Clear search result highlighting
nnoremap <Leader><space> :noh<cr>
 
" Enable RSpec snippets in spec files
au BufNewFile,BufRead *_spec.rb set filetype=ruby.rspec.rspec_rails.factory_girl
 
" Enable RSpec snippets in spec files
au BufNewFile,BufRead *.coffee set filetype=coffee
 
" Sudo write the file
cmap w!! %!sudo tee > /dev/null %
 
" tab navigation like firefox
:nmap <C-S-tab> :tabprevious<CR>
:nmap <C-tab> :tabnext<CR>
:map <C-S-tab> :tabprevious<CR>
:map <C-tab> :tabnext<CR>
:imap <C-S-tab> <Esc>:tabprevious<CR>i
:imap <C-tab> <Esc>:tabnext<CR>i
:nmap <C-t> :tabnew<CR>
:imap <C-t> <Esc>:tabnew<CR>

