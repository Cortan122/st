# st - simple terminal
st is a simple terminal emulator for X which sucks less.

## changes in code
+ `^L` keeps scrollback buffer intact
+ selected text no longer turns invisible when alpha is 0
+ faster zoom (костыль)
+ simplified [anysize](https://st.suckless.org/patches/anysize/) patch that doesn't center the screen

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
+ applied [bold-is-not-bright](https://st.suckless.org/patches/bold-is-not-bright) patch version [is-not-bright-20190127-3be4cf1.diff](https://st.suckless.org/patches/bold-is-not-bright/st-bold-is-not-bright-20190127-3be4cf1.diff)
+ applied [alpha](https://st.suckless.org/patches/alpha) patch version [osc11-20220222-0.8.5.diff](https://st.suckless.org/patches/alpha/st-alpha-osc11-20220222-0.8.5.diff)
