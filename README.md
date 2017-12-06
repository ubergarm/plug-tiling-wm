[![CC-BY-SA-4.0](https://licensebuttons.net/l/by-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-sa/4.0/legalcode)

*Philadelphia Linux User Group Meetup Tiling Windows Manager Discussion*

or

*Drilling down on Linux Tiling Windows Managers from big bang to "ricing" your configuration with "dank" gaps.*

## Brief History of Human Machine Interfaces
* Big Bang
* Higgs Field Unified Field of Consciousness
* Human Consciousness
* Oral Language
* Cuneiform Script
* Abacus
* Teletype - `In the Beginning... Was the Command Line` essay by Neal Stephenson.
* Dumb Terminals (Glass TTY)
* Smart Terminals
  - graphics cards
  - 4k monitors
  - psychophysics
* Web Browsers
* Mobile Devices
* IoT
* Cloud
* Blockchains / Decentrialized Apps

#### Rhetorical Questions
1. How do you experience Self and other?
1. How does the left hand interface with the right hand?
1. Correlation or Causation between Apple products and frequency of sexual activity? [wired](https://www.wired.com/2010/08/gadget-sex/)
1. Chaos and Fractals?
1. Will AI work for us, or will we work for AI, or will AI work for AI?

## Modern Smart Terminals
* Apple hardware with MacOS X
* Hackintosh
* PC Windows 10 Linux Subsystem Bash Shell (plus unofficial X server) (Direct3D)
* Virtual Machines / Containers
* Linux Desktop
  - X Windows (vs [Mir](https://wiki.ubuntu.com/Mir/)) (OpenGL vs [Vulkan](https://en.wikipedia.org/wiki/Vulkan_(API)))
    + Unity / GTK+ - now defunct
    + KDE / Qt
    + Gnome / GTK+
    + Lightweight / Various - custom
    + Tiling Windows Managers / Various - custom

## Linux Desktops Components
* Desktop
  - Monitor(s)
  - Video Card(s)
  - Resolution
  - Color Depth
  - Refresh
  - Transparency Effects
  - Wallpaper
* Window Managers
  - Tiling
    + [dwm - dynamic window manager](https://dwm.suckless.org/)
    + [xmonad - haskell](http://xmonad.org/)
    + [i3 - improved improved improved](https://i3wm.org/)
  - Floating
* Terminal
  - [st - simple terminal](https://st.suckless.org/)
  - [xterm](http://xterminal.sourceforge.net/)
  - [rxvt](http://software.schmorp.de/pkg/rxvt-unicode.html)
  - Fonts (Unicode)
    + [Dejavu Sans Mono patched for Powerline](https://github.com/powerline/fonts)
  - True Color vs 256
  - Editor
    + [vim 8.0+](https://github.com/vim/vim)
* Status Bar / System Monitor
  - [slstatus](https://github.com/drkhsh/slstatus)
  - [conky](https://github.com/brndnmtthws/conky)
* Menu / Launch Bar
  - [rofi](https://github.com/DaveDavenport/rofi)
  - [dmenu](https://tools.suckless.org/dmenu/)
* Utilities
  - xrandr
  - compton
  - nitrogen
  - xclip
  - scrot
  - xscreensaver
* Applications
  - mupdf
  - sxiv
  - tig
  - pass
  - mpv
  - gimp
  - slack
  - alsamixer
  - pulseaudio (only for firefox)
  - firefox quantum

## Demo
Check out my system.

* [screenshot](https://ubergarm.com/gifs/dwm-tiling-screenshot.png)
* [standing desk](https://ubergarm.com/gifs/desk.jpg)

#### `.xinitrc`
```bash
## setup monitor and resolution
xrandr --newmode "4096x2160" 556.730  4096 4104 4136 4176  2160 2208 2216 2222 +hsync +vsync
xrandr --addmode DP-0 4096x2160
xrandr --output DP-0 --mode 4096x2160
## compositing transparency
compton -b -c -o 0.25
## pretty wallpaper
nitrogen --set-zoom-fill ~/wallpapers/jenaro-bekannt-wie-ein-bunter-hund.jpg
## sreensaver
xscreensaver -no-splash &
## status bar
while true; do
    slstatus
done &
## windows manager
exec dwm
```

## The Upsides
* Cool factor
* Less cruft
* Less mouse
* Forces you to learn CLI tools which work across ssh terminals

## The Downsides
* Clipboards
* Configuration
  - initial setup
  - recompiling binaries
  - wifi networks
  - package management
* The rest of the world sends you XLSX files

## Summary
> Only computer hackers who have delved into the inconvenient guts of
> an operating system that turns their home computer into a giant pile
> of tinker-toys are truly liberated from the cruel manipulation of their
> slipshod corporate taskmasters. You know what I think makes an operating
> system truly great? Its ability to help me GET MY WORK DONE.
> - Garrett Birkel http://garote.bdmonkeys.net/commandline/index.html

## References
* [PLUG Central Meetup](https://www.meetup.com/Philadelphia-Linux-User-Group-Meetup/events/244971579/)
* [dank ricing gaps](https://www.youtube.com/results?search_query=tiling+dank+gaps+i3)
* [Linux Desktop X Windows](https://en.wikipedia.org/wiki/Comparison_of_X_Window_System_desktop_environments)
* [Steam Hardware & Software Survey](http://store.steampowered.com/hwsurvey#cat9)
* [dwm - dynamic window manager](https://dwm.suckless.org/)
* [Neal Stephenson](https://en.wikipedia.org/wiki/In_the_Beginning..._Was_the_Command_Line)

![most interesting man meme](https://i.imgflip.com/20mh53.jpg)
