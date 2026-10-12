# my_vs_code_settings

https://gist.github.com/hasnath1/d1c2220958ac181daf752d238d6ca5b5
# Study resources 
https://drive.google.com/drive/folders/1_M1XvQWGhlsIverSBh-psHlnkDXSO0cQ

# C programming language ref
https://hlevkin.com/hlevkin/92usefulBooks/C/CNotesForProfessionals.pdf

# Notes for everything
https://goalkicker.com/

# Setup vim for c/c++ coding 

```
sudo apt update && sudo apt install -y clangd git vim && \
mkdir -p ~/.vim/pack/plugins/start && \
git clone --depth=1 https://github.com/prabirshrestha/vim-lsp.git ~/.vim/pack/plugins/start/vim-lsp && \
git clone --depth=1 https://github.com/mattn/vim-lsp-settings.git ~/.vim/pack/plugins/start/vim-lsp-settings && \
git clone --depth=1 https://github.com/prabirshrestha/asyncomplete.vim.git ~/.vim/pack/plugins/start/asyncomplete.vim && \
git clone --depth=1 https://github.com/prabirshrestha/asyncomplete-lsp.vim.git ~/.vim/pack/plugins/start/asyncomplete-lsp.vim && \
cat << 'EOF' > ~/.vimrc
syntax on
set number
set relativenumber
set tabstop=4
set shiftwidth=4
set expandtab
set autoindent
set smartindent
set hidden
set completeopt=menuone,noinsert,noselect

inoremap <expr> <Tab> pumvisible() ? "\<C-n>" : "\<Tab>"
inoremap <expr> <S-Tab> pumvisible() ? "\<C-p>" : "\<S-Tab>"
inoremap <expr> <cr> pumvisible() ? asyncomplete#close_popup() : "\<cr>"
EOF

```
