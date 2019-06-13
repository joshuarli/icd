# icd

interactive cd (fast travel) in posix shell. assumes emulated terminal is vt100, see notes.

this was inspired by how fast i found i could navigate within `ncdu`, and was fed up with repeating `cd`, `cd ..` or `..`, and `ls`. in fact, implementing d/delete and recursive size reporting (using posix awk to parse ls and do math, or assume `du`) would make `icd` a very naive `ncdu` implementation without the ncurses part, or interactive du "idu", but i digress.


## usage

[demo asciicast](https://asciinema.org/a/251613)

copy `icd` somewhere on path, source `icd-wrapper`, `ft`.

arrow keys or vi-like bindings to navigate, q to quit.


## notes

posix specifies a very limited `tput`, so `icd` relies on some hardcoded vt100 escape sequences.

`icd` can be trivially ported to a more featureful environment, such as `bash` + ncurses `tput`, for some nontrivial compatibility (in the terminal sense) and performance improvements. examples can be found in `ports/`.


## see also

- [fff](https://github.com/dylanaraps/fff)
- [filet](https://github.com/buffet/filet) (actually found this shortly after finishing a working version of icd, it's very similar from a UI standpoint but has slightly more features)
