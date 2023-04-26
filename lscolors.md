# LSCOLORS

BSD terminals use LSCOLORS instead of LS_COLORS.    
zsh used in Mac terminals is a notable example.   
It will look something like this:     
```
LSCOLORS=Gxfxcxdxbxegedabagacad
```


## Colors
| # | Color |
|---|-------|
| a | Black| 
| b | Red| 
| c | Green| 
| d | Brown| 
| e | Blue| 
| f | Magenta| 
| g | Cyan| 
| h | White (light grey)| 
| A | Bright Black (dark grey)| 
| B | Bright Red| 
| C | Bright Green| 
| D | Bright Yellow| 
| E | Bright Blue| 
| F | Bright Magenta| 
| G | Bright Cyan| 
| H | Bright White| 
| x | default foreground or background| 

## Attributes
In this order:
| # | Attribute |
|---|-----------|
| 1 | directory| 
| 2 | symbolic link| 
| 3 | socket| 
| 4 | pipe| 
| 5 | executable| 
| 6 | block special| 
| 7 | character special| 
| 8 | executable with setuid bit set| 
| 9 | executable with setgid bit set| 
| 10 | directory writable to others, with sticky bit| 
| 11 | directory writable to others, without sticky bit| 

Two colors per attribute as foreground then background


## Really?
Yes.    
You can trick a Mac into using LS_COLORS by using the gnu version of ls instead of the baked-in bsd version of ls.   
```
brew install coreutils
alias ls='gls --color'
```
