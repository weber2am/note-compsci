# vi cheatsheet


## Movement

```
hjkl   left down up right

w    word
b    back a word
e    end of word
W,B,E    only whitespace breaks word

gg   go first line
G    go last line
:n   go to line n
zz   move current line to center of screen

0    first column
^    first non-whitespace
$    end of line
%    go to matching ( { [
```

## Insert

```
i    insert at cursor
I    insert before first non-whitespace
a    append
A    append end of line
o    open above
O    open below
r    replace char
R    replace (until esc)
c    change
cc   change line
C    change to end of line
```

## Delete Yank Put

```
x    delete (and yank) char

d    delete <movement> (and yank)
dd   delete line
D    delete to end of line

y    yank <movement>
yy   yank line

p    put after cursor
P    put before cursor
```

## Do Command Multiple Times

Some commands can be modified by a count.
```
nw   forward n words
nj   down n lines

dnw  delete n words
ndw  delete n words

nx   delete n chars
```


## Ex mode, aka Command Mode

```
:q    quit
:w    write
:wq   write and quit
:set wrap       turn on word wrap
:set nowrap     turn off word wrap
:set number     turn on line numbers
:set nonumber   turn off line numbers
:set paste      turn off auto indent
:set nopaste    turn on auto indent
```

## Search

```
*    find next instance of word under cursor
#    find previous instance of word under cursor
n    next
N    previous
```


## Other Search

```
/pattern    search for pattern
    /\Cpattern    case sensitive
?pattern    search backward for pattern
n    next
N    previous
```


## Misc

```
.    repeat
u    undo
J    join lines
```


