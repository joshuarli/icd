# icd

interactive cd (fast travel) in posix shell. assumes emulated terminal is vt100, see notes.


## usage

copy `icd` somewhere on path, source `icd-wrapper`, `ic`.

arrow keys or vi-like bindings to navigate, q or ^C to quit.


## notes

posix specifies a very limited `tput`, so `icd` relies on some hardcoded vt100 escape sequences.

`icd` can be trivially ported to a more featureful environment, such as `bash` + ncurses `tput`, for some nontrivial compatibility (in the terminal sense) and performance improvements. examples can be found in `ports/`.
