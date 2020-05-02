# st - suckless terminal

My build of st, with focus on productivity and keyboard-driven workflow.

## Features

- transparency (need a third-party compositor)
- open a URL with alt+l
- copy a URL with alt+y
- scroll with alt + {j, k, u, d}
- zoom with alt+shift+ {j, k} or ctrl+ {-, =}
- reset zoom with ctrl+shift+ =
- insert arbitrary Unicode character with ctrl+shift+u
- synchronized rendering support
- fallback fonts
- spawn a new terminal in the same directory with ctrl+shift+return
- copy a command's output with alt+o
- read colorscheme and alpha from Xresources
- edit the terminal's visible contents in $EDITOR with alt+e

## Third-Party Dependencies

- any window compositor
- [dmenu](https://tools.suckless.org/dmenu/)
- [copyq](https://github.com/hluk/copyq) (scripts can be modified by hand to work with any clipboard manager)

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
- [boxdraw](https://st.suckless.org/patches/boxdraw/)

## Installation

In order to build st you need the Xlib header files.

Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install

Additionally, to make all the custom features added by me available
you will need all the files preceding with `st-script-` to be marked
executable and added to your PATH. There are multiple ways to do this,
but here's a oneliner that I use (execute from the repo root directory):

    find . -maxdepth 1 -name "st-script-*" -print0 | xargs -0 -I % sudo ln -sTf -- "$(realpath -- "%")" "/usr/local/bin/$(basename -- "%")"

The above command will find all the files beginning with `st-script-` and create symlinks to them in `/usr/local/bin`.

## References

I used these as sources of inspiration to see some examples of what can be done with st without relying solely on painful experimentation.
Also, the suckless website is a primary source for patches, which are obligatory for any decent st build.

- [Official Website](https://st.suckless.org)
- [Luke Smith's build](https://github.com/lukesmithxyz/st)


## Credits

st is based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

