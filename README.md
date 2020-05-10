# FunWithVim

On my winows machine, I had a problem setting ```_vimrc```. I couldn't change the file. The solution was installing vim outside Program Files (86) to my user name. Then as vim where does it read from

```
:version
```

and check
```
:echo $HOME
```

and from there I made ```_gvimrc``` included in this repo


In the .vimrc file, line comments are made by adding a double quote " to the left of the text, this means that everything to the right of the " is a comment; multiline comments can't be made in the .vimrc file except adding a " to the beginning of each line, thus resulting in multiple single-line comment unlike C

you can find color choices you have

```
Vim/vim82/colors/
```

installing plug manager: 
https://github.com/junegunn/vim-plug


to see current git branch (and to have git control, which i couldn't so far)
https://github.com/tpope/vim-fugitive

## Resources

1. And excellent explanation of some great vimrc settings https://dougblack.io/words/a-good-vimrc.html
2. Some nice customization https://nvie.com/posts/how-i-boosted-my-vim/
3. how to color vim (simple without outside packages)
