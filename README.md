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

# Common C header files and compilation processes

Since your lab is focused on **pure C**, you won't need the C++ Standard Template Library (STL). Here is the cheat sheet of the essential C standard header files you will need for your lab exam, along with their most common functions:

---

### Essential C Standard Headers

| Header File | Description & Common Functions |
| --- | --- |
| **`<stdio.h>`** | **Standard Input/Output**<br>

<br>• `printf()`, `scanf()`<br>

<br>• `fopen()`, `fclose()`, `fprintf()`, `fscanf()`<br>

<br>• `fgets()`, `puts()` |
| **`<stdlib.h>`** | **General Utilities (Memory & Conversion)**<br>

<br>• Memory allocation: `malloc()`, `calloc()`, `realloc()`, `free()`<br>

<br>• Conversions: `atoi()`, `atof()`<br>

<br>• Utilities: `rand()`, `srand()`, `exit()` |
| **`<string.h>`** | **String & Array Manipulation**<br>

<br>• `strlen()`, `strcpy()`, `strcat()`, `strcmp()`<br>

<br>• `memset()`, `memcpy()` |
| **`<math.h>`** | **Mathematical Functions**<br>

<br>• `sqrt()`, `pow()`, `ceil()`, `floor()`, `fabs()`<br>

<br>*(Note: Compile with `-lm`, e.g., `gcc file.c -lm`)* |
| **`<ctype.h>`** | **Character Testing & Conversion**<br>

<br>• Testing: `isdigit()`, `isalpha()`, `isalnum()`, `isspace()`<br>

<br>• Conversion: `toupper()`, `tolower()` |
| **`<stdbool.h>`** | **Boolean Types**<br>

<br>• Enables the use of `bool`, `true`, and `false` instead of using `int` for flags. |
| **`<limits.h>`** | **Data Type Limits**<br>

<br>• Useful for finding max/min limits like `INT_MAX`, `INT_MIN`. |

---

### Quick C Compilation Reminders

* **Standard Compilation:** `gcc -std=c99 -Wall main.c -o main`
* **Using Math Functions:** If you include `<math.h>` and use functions like `sqrt()` or `pow()`, remember to append `-lm` at the end of your compile command:
```bash
gcc -std=c99 -Wall main.c -o main -lm

```



Good luck with your C lab exam today! You've got this.
