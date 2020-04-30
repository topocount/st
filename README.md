# st - suckless terminal

My build of st, with focus on productivity and keyboard-driven workflow.

## Features

- transparency (need a third-party compositor)
- select URL to open with alt+l
- scroll with alt + {j, k, u, d}
- zoom with alt+shift+ {j, k} or ctrl+ {-, =}
- reset zoom with ctrl+shift+ =
- insert arbitrary Unicode character with ctrl+shift+u
- synchronized rendering support
- fallback fonts
- spawn a new terminal in the same directory with ctrl+shift+return

## Third-Party Dependencies

- any window compositor
- [dmenu](https://tools.suckless.org/dmenu/)

## Applied Patches

- [alpha](https://st.suckless.org/patches/alpha/)
- [anysize](https://st.suckless.org/patches/anysize/)
- [bold is not bright](https://st.suckless.org/patches/bold-is-not-bright/)
- [externalpipe](https://st.suckless.org/patches/externalpipe/)
- [scrollback](https://st.suckless.org/patches/scrollback/)
- [iso14755](https://st.suckless.org/patches/iso14755/)
- [synchronized rendering](https://st.suckless.org/patches/sync/)
- [xresources](https://st.suckless.org/patches/xresources/)
- [font2](https://st.suckless.org/patches/font2/)
- [newterm](https://st.suckless.org/patches/newterm/)

## References

I used these as sources of inspiration to see some examples of what can be done with st without painful experimentation. Also, the suckless website is a primary source for patches, which are obligatory for any decent st build.

- [Official Website](https://st.suckless.org)
- [Luke Smith's build](https://github.com/lukesmithxyz/st)

## Original README

st - simple terminal
--------------------
st is a simple terminal emulator for X which sucks less.


Requirements
------------
In order to build st you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

Credits
-------
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

