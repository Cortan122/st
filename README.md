# st - simple terminal
st is a simple terminal emulator for X which has all the features i need, because i implemented them myself.
The original st and community around it is sadly a bit of a _dead dove do not eat_ situation. 
So i'm not that happy that this is the only terminal that has all the features.
Maybe i will fork [foot](https://codeberg.org/dnkl/foot) in the future... 

## changes in code
+ `^L` keeps scrollback buffer intact
+ selected text no longer turns invisible when alpha is 0
+ faster zoom (`XftTextExtentsUtf8` is only called once)
+ simplified [anysize](https://st.suckless.org/patches/anysize/) patch that doesn't center the screen
+ smart copy with `^C`
+ scroll beyond last line
+ external pipe patch modified to use history
<!-- TODO: resizing in alt screen fucks up cursor pos -->

## changes in config
+ keyboard input [patch](https://st.suckless.org/patches/fix_keyboard_input/)
+ fix for `ctrl+shift+delete`, `shift+space` and `ctrl+shift+backspace`
+ Ubuntu color scheme and Unifont as fallback
+ scroll 3 lines at a time (and also in `nano`)
+ selected text no longer turns invisible when alpha is 0
+ mouse wheel shortcuts for zoom and alpha
+ everything uses `CLIPBOARD` insted of `PRIMARY`
+ both right click and middle click to paste

## applied patches
+ applied [scrollback](https://st.suckless.org/patches/scrollback) patch version [ringbuffer-0.8.5.diff](https://st.suckless.org/patches/scrollback/st-scrollback-ringbuffer-0.8.5.diff)
+ applied [scrollback](https://st.suckless.org/patches/scrollback) patch version [mouse-20220127-2c5edf2.diff](https://st.suckless.org/patches/scrollback/st-scrollback-mouse-20220127-2c5edf2.diff)
+ applied [scrollback](https://st.suckless.org/patches/scrollback) patch version [mouse-altscreen-20220127-2c5edf2.diff](https://st.suckless.org/patches/scrollback/st-scrollback-mouse-altscreen-20220127-2c5edf2.diff)
+ applied [iso14755](https://st.suckless.org/patches/iso14755) patch version [0.8.5.diff](https://st.suckless.org/patches/iso14755/st-iso14755-0.8.5.diff)
+ applied [bold-is-not-bright](https://st.suckless.org/patches/bold-is-not-bright) patch version [20190127-3be4cf1.diff](https://st.suckless.org/patches/bold-is-not-bright/st-bold-is-not-bright-20190127-3be4cf1.diff)
+ applied [alpha](https://st.suckless.org/patches/alpha) patch version [osc11-20220222-0.8.5.diff](https://st.suckless.org/patches/alpha/st-alpha-osc11-20220222-0.8.5.diff)
+ applied [font2](https://st.suckless.org/patches/font2) patch version [20190416-ba72400.diff](https://st.suckless.org/patches/font2/st-font2-20190416-ba72400.diff)
+ applied [boxdraw](https://st.suckless.org/patches/boxdraw) patch version [0.8.5.diff](https://st.suckless.org/patches/boxdraw/st-boxdraw_v2-0.8.5.diff)
+ applied [externalpipe](https://st.suckless.org/patches/externalpipe) patch version [0.8.4.diff](https://st.suckless.org/patches/externalpipe/st-externalpipe-0.8.4.diff)

## other branches in this repo

I have been fiddling with st for a very long time. The other branches in this repo are my older attempts. You probably shouldn't touch them. 

+ branch [original](https://github.com/Cortan122/st/tree/original) is source code from the [suckless](https://st.suckless.org/) website
+ branch [2019-fork](https://github.com/Cortan122/st/tree/2019-fork) is my old version based on [Luke Smith's](https://github.com/LukeSmithxyz/st) fork, with all the changes squished to one commit
+ branch [based-fork](https://github.com/Cortan122/st/tree/based-fork) is a newer version, also based on [Luke's](https://github.com/LukeSmithxyz/st) fork, with an explicit list of changes and separate commits
+ branch [master](https://github.com/Cortan122/st/tree/master) is my current based on the original source code with the [ringbuffer](https://st.suckless.org/patches/scrollback/st-scrollback-ringbuffer-0.8.5.diff) scrollback patch
