# vim-spell-check
Step by step configuration of Vim for spell-check & autocomplete.

##First install vim
```
sudo apt-get install vim
```
##Create vim config file
```
cd ~/
vi .vimrc
```
##Paste following lines in your vim config file
```
set spell
set spelllang=en_us
set complete+=k	
autocmd FileType mail setlocal spell spelllang=en_us
autocmd BufRead COMMIT_EDITMSG setlocal spell spelllang=en_us
autocmd BufNewFile,BufRead *.md,*.mkd,*.markdown set spell spelllang=en_us
```
##Press `ctrl + N` to get suggestions of words

##To check spell or typo do following
```
1)Exit from insert mode
2)Go to highligted word and press `z=` to get list of suggestions
3)In normal mode press `]s` & `[s` to navigate left and righ highlighted word respectively
```
#Make sure to use Vim as default editior for Git
```
git config --global core.editor "vim"
```
#References
1)http://vimdoc.sourceforge.net/htmldoc/spell.html
2)http://vim.wikia.com/wiki/Dictionary_completions

