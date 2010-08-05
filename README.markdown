This is a dark scheme for vim, which is designed to work in 88 and 256 colour terminals, as well as in gvim.

To install this file, move it to the vim colours folder:

    mv zenzike.vim ~/.vim/colors

Then add the following line to your `.vimrc`:

    if &term =~ "xterm-debian" || &term =~ "xterm-xfree86"
      set t_Co=16
    elseif &term =~ "rxvt-unicode"
      set t_Co=88
    elseif &term =~ "rxvt" || &term =~ "xterm"
      set t_Co=256
    elseif has("gui_running")
      set t_Co=256
    endif

    colorscheme zenzike.vim
