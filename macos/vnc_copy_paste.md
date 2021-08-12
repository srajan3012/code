## Enable copy paste from mac to vnc
- Modify xstartup
  * open `~/.vnc/xstartup`
  * Add after first uncommented line: `xrdb -merge ~/.Xdefaults`
- Create Xdefaults
  * `echo "*VT100.translations: #override  Meta <KeyPress> V:  insert-selection(PRIMARY, CUT_BUFFER0) \n" > ~/.Xdefaults`
