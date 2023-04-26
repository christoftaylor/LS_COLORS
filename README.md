# LS_COLORS
I found several pages that descibe dircolors and LS_COLORS partially, but not completely. Here's what I found to fill in the remaining gaps:

## File Attributes:
| short | long  | description                     |
|-------|-------|---------------------------------|
| no | NORMAL, NORM | Normal text. Not a filename. Global Default. |
| fi | FILE | Normal file name. |
| ex | EXEC | Executable file, as in has u+x permissions |
| ln | SYMLINK, LINK, LNK | Symbolic Link. If set to 'target' will follow colors of object is pointed at. |
| di | DIR | Directory name. |
| st | STICKY | Directory with sticky bit set (+t) but not o+w permissions. |
| tw | STICKY_OTHER_WRITABLE | Directory with both sticky bit (+t) and o+w set. |
| ow | OTHER_WRITABLE | Directory with o+w permissions. |
| su | SETUID | File that is setuid (u+s). |
| sg | SETGID | File that is setgid (g+s). |
| bd | BLOCK, BLK | Block device special file. |
| cd | CHAR, CH | Character device special file. |
| do | DOOR | Door special file. |
| mi | MISSING | Target of a symlink that does not exist. | 
| or | ORPHAN | Symlink pointing to an orphaned nonexistent file. |
| pi | PIPE, FIFO | Named pipe or fifo special file. |
| so | SOCK | Socket special file. |
| mh | MULTIHARDLINK | When a file has multiple hard links. |
| rs | RESET | Resets colors. Not supported in every shell. | 
| *.ext |  | File extensions, as either `*.jpg` or `*jpg`, renders those files as specified. |

'rs' and 'mh' not supported in every shell.    
If you include a shortcode your terminal does not support, every execution of ls will throw an error that the code is not recognized.    
  
  
  
## Formatting:
| # | Formatting code |
|---|-----------------|
| 0 | Normal (default), VT100. | 
| 1 | Bold, VT100. | 
| 2 | Faint, decreased intensity, ECMA-48 2nd. | 
| 3 | Italicized, ECMA-48 2nd. | 
| 4 | Underlined, VT100. | 
| 5 | Blink, VT100. | 
| 6 | This appears as Bold in X11R6 xterm. |  
| 7 | Inverse, VT100. (swap fore and background colors) | 
| 8 | Invisible, i.e., hidden, ECMA-48 2nd, VT300. | 
| 9 | Crossed-out characters, ECMA-48 3rd. | 

You can chain multiple together, e.g. `ln=1;4;5;31` == symlinks appear bold, italicized, and blinking in red text.   
  
  
## Basic colors:
8-bit color terminals support colors specified as 30-37 and 40-47.    
16-bit color terminals support those plus additional colors 90-97 and 100-107.     
Terminals that support 256 colors can support referencing colors by RGB codes.     

| #  | Foreground colors  |       | #  | Background colors |      |
|----|--------------------|-------|----|-------------------|------|
| 30 | Black | ![](https://placehold.co/15x15/000000/000000.png)`rgb(0,0,0)` | 40 | Black | ![](https://placehold.co/15x15/000000/000000.png)`rgb(0,0,0)` | 
| 31 | Red | ![](https://placehold.co/15x15/800000/800000.png)`rgb(128,0,0)` | 41 | Red | ![](https://placehold.co/15x15/800000/800000.png)`rgb(128,0,0)` | 
| 32 | Green | ![](https://placehold.co/15x15/008000/008000.png)`rgb(0,128,0)` | 42 | Green | ![](https://placehold.co/15x15/008000/008000.png)`rgb(0,128,0)` | 
| 33 | Yellow | ![](https://placehold.co/15x15/808000/808000.png)`rgb(128,128,0)`  | 43 | Yellow | ![](https://placehold.co/15x15/808000/808000.png)`rgb(128,128,0)` | 
| 34 | Blue | ![](https://placehold.co/15x15/000080/000080.png)`rgb(0,0,128)` | 44 | Blue | ![](https://placehold.co/15x15/000080/000080.png)`rgb(0,0,128)` | 
| 35 | Magenta | ![](https://placehold.co/15x15/800080/800008.png)`rgb(128,0,128)` | 45 | Magenta | ![](https://placehold.co/15x15/800080/800008.png)`rgb(128,0,128)` | 
| 36 | Cyan | ![](https://placehold.co/15x15/008080/008080.png)`rgb(0,128,128)` | 46 | Cyan | ![](https://placehold.co/15x15/008080/008080.png)`rgb(0,128,128)` | 
| 37 | White | ![](https://placehold.co/15x15/C0C0C0/C0C0C0.png)`rgb(192,192,192)` | 47 | White | ![](https://placehold.co/15x15/C0C0C0/C0C0C0.png)`rgb(192,192,192)` | 
| 39 | default, ECMA-48 3rd. | | 49 | default, ECMA-48 3rd. | |
| 90 | Bright Black | ![](https://placehold.co/15x15/808080/808080.png)`rgb(128,128,128)` | 100 | Bright Black | ![](https://placehold.co/15x15/808080/808080.png)`rgb(128,128,128)` | 
| 91 | Bright Red | ![](https://placehold.co/15x15/FF0000/FF0000.png)`rgb(255,0,0)`  | 101 | Bright Red | ![](https://placehold.co/15x15/FF0000/FF0000.png)`rgb(255,0,0)` | 
| 92 | Bright Green | ![](https://placehold.co/15x15/00FF00/00FF00.png)`rgb(0,255,0)` | 102 | Bright Green | ![](https://placehold.co/15x15/00FF00/00FF00.png)`rgb(0,255,0)` | 
| 93 | Bright Yellow | ![](https://placehold.co/15x15/FF0000/FF0000.png)`rgb(255,255,0)` | 103 | Bright Yellow | ![](https://placehold.co/15x15/FF0000/FF0000.png)`rgb(255,255,0)` | 
| 94 | Bright Blue | ![](https://placehold.co/15x15/0000FF/0000FF.png)`rgb(0,0,255)` | 104 | Bright Blue | ![](https://placehold.co/15x15/0000FF/0000FF.png)`rgb(0,0,255)` | 
| 95 | Bright Magenta | ![](https://placehold.co/15x15/FF00FF/FF00FF.png)`rgb(255,0,255)` | 105 | Bright Magenta | ![](https://placehold.co/15x15/FF00FF/FF00FF.png)`rgb(255,0,255)` | 
| 96 | Bright Cyan | ![](https://placehold.co/15x15/00FFFF/00FFFF.png)`rgb(0,255,255)` | 106 | Bright Cyan | ![](https://placehold.co/15x15/00FFFF/00FFFF.png)`rgb(0,255,255)` | 
| 97 | Bright White | ![](https://placehold.co/15x15/FFFFFF/FFFFFF.png)`rgb(255,255,255)` | 107 | Bright White | ![](https://placehold.co/15x15/FFFFFF/FFFFFF.png)`rgb(255,255,255)` | 

The definition of 'Black' and 'White' changed once 8-bit became 16-bit, in what we call 'legacy BS'.    
To further complicate life, the ANSI documentation specifies colors by name, not RGB values, and newer terminals fudge the RBG values to try to make them align with how older terminals displayed those names. Different terminals will use different RGB values for those names.       
Think of 'white' as 'light grey' and 'bright black' as 'dark grey'.   
Also, making text bold can make it appear brighter, adding more values to the scale.    
Here's an example you can use to see the difference, try this in your terminal:   
```
$ touch file.{1..9}
$ export LS_COLORS='*.1=1;30:*.2=37:*.3=90:*.4=97:*.5=0:*.6=40:*.7=47:*.8=100:*.9=107'
$ ls
file.1  file.2  file.3  file.4  file.5  file.6  file.7  file.8  file.9
```
  

## Advanced Colors:   
There are two ways to reference colors from the 256 color palatte - either by index number or RGB values.   
38 = foregound and 48 = background, missing from the table above.   
Follow these values with either a 5 or a 2, respectively, to state how the color will be specified.   
When using RGB, specify a color palatte. This field will be ignored. This field may get skipped when using some shells.    
See the file [`Index_Colors.md`](./Index_Colors.md) for a full list of the values that go here.    

By index:   
38;5;15 = ![](https://placehold.co/15x15/ffffff/ffffff.png) white   
38;5;128 = ![](https://placehold.co/15x15/af00d7/af00d7.png) dark violet   
48;5;222 = ![](https://placehold.co/15x15/ffd787/ffd787.png) light goldenrod   

By RGB value:     
38;2;0;255;255;255 = ![](https://placehold.co/15x15/ffffff/ffffff.png) white   
38;2;0;175,0,215 = ![](https://placehold.co/15x15/af00d7/af00d7.png) dark violet   
48;5;0;255,215,135 = ![](https://placehold.co/15x15/ffd787/ffd787.png) light goldenrod   


## Put it all together:
Each entry will be separated by a colon (:).    
Values within each entry will be separated by semicolon (;).    
Repeating entries will overwrite prior with the last entry standing. 

Basic:    
```
export LS_COLORS='no=0:fi=32:di=34'
```

Bit more complicated:    
```
export LS_COLORS='no=0;38;5;237:fi=0;37:ln=target:ex=31:di=0;38;5;27:st=0;34:tw=0;34:ow=0;34:su=0;4:sg=0;4' 
```





## References:
- [dircolors.c](https://github.com/coreutils/coreutils/blob/master/src/dircolors.c) - source code to dircolors defines the ls codes and slack codes 
- [dircolors.h](https://github.com/coreutils/coreutils/blob/master/src/dircolors.hin) - default settings and examples
- [256 Colors Cheat Sheet](https://www.ditig.com/256-colors-cheat-sheet) - shows the index number for colors
- [XTerm Control Sequences](https://invisible-island.net/xterm/ctlseqs/ctlseqs.html#h3-Functions-using-CSI-_-ordered-by-the-final-character_s_) - scroll down to 'CSI Pm m  Character Attributes (SGR)' for how numbers work behind each attribute or extention.
- [dircolors_solarized](https://github.com/seebi/dircolors-solarized) - example of a fully themed color scheme
- 

