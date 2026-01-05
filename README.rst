Awesome WM Copycats
===================

-------------------------
Themes for Awesome WM 4.x
-------------------------

:Author: Luca CPZ
:Version: git
:License: BY-SA_
:Source: https://github.com/lcpz/awesome-copycats

Description
===========

A set of themes for the Awesome_ window manager, version 4.x.

Purpose
=======

The main purpose of this repository is to spread ready to use configurations, which can also serve as a cookbook for customisation.

A secondary aim is to add new themes only when they constitute different UI/UX designs.

Features
========

- Modularity
- Autohide widgets
- Autostart windowless processes
- Fast MPD and volume shortcuts (first time this trick has been used in Awesome)
- Shortcuts for copying to the clipboard, toggle wiboxes, widgets popups, screenshots capture, moving and magnifying clients
- Quake drop-down terminal
- Calendar with current day highlighted and months switch with a click/scroll
- Notifications for new mails, current song, volume level, hdd critical state, low battery
- OpenWeatherMap integration
- Net carrier status notifier
- Symbolic tag names
- DWM-like textual layoutbox
- Cairo wibar
- Custom layouts
- No borders when there's only one visible client
- Freedesktop.org compliant menu and desktop icons
- Vi-like client focus
- Non-empty tag browsing
- On-the-fly useless gaps resize
- Dynamic tagging

Installation
============
Just do the following:

.. code-block:: shell

    git clone --recurse-submodules --remote-submodules --depth 1 -j 2 https://github.com/pac-source/awesome-copycats.git
    mkdir -p ~/.config/awesome && mv -bv awesome-copycats/{*,.[^.]*} ~/.config/awesome &&  rm -rf awesome-copycats

Usage
=====

The modular structure allows to

* set variables
* define startup processes
* change keybindings and layouts
* set client properties

in ``rc.lua``, and

* configure widgets
* define wiboxes and screen settings

in ``theme.lua``, so that you just need to change ``chosen_theme`` variable in ``rc.lua`` to preserve your preferences *and* switch the theme, instead of having file redundancy.

Set the variable ``chosen_theme`` in ``rc.lua`` to your preferred theme, do your settings, and restart Awesome (``Mod4 + ctrl + r``).

To customize a theme, head over to ``themes/$chosen_theme/theme.lua``.

Otherwise, if you want to be synced with upstream, modify the theme path in ``rc.lua`` like this:

.. code-block:: diff

    -beautiful.init(string.format("%s/.config/awesome/themes/%s/theme.lua", os.getenv("HOME"), chosen_theme))
    +beautiful.init(string.format("%s/.config/awesome/themes/%s/theme-personal.lua", os.getenv("HOME"), chosen_theme))

then, copy ``theme.lua`` to ``theme-personal.lua`` and do your customizations there.

This way, you can safely ``git pull`` anytime.

Notes
=====

Complements are provided by lain_ and freedesktop_. **Be sure** to satisfy their dependencies_. In particular, mail_ and weather_ widgets have **mandatory** arguments.

The fonts used in the screenshots are: Terminus_, Roboto_ and Tamzen_.

As taglist font, Blackburn and Dremora use Icons_, Vertex uses FontAwesome_: be sure to have bitmaps enabled if running under Debian or Ubuntu_.

Every theme has a colorscheme_.

Additional default software used: ::

    amixer brightnessctl dmenu firefox mpc mpd scrot slock unclutter xsel

.. _BY-SA: https://creativecommons.org/licenses/by-sa/4.0
.. _Awesome: http://github.com/awesomeWM/awesome
.. _branches: https://github.com/lcpz/awesome-copycats/branches
.. _lucamanni: https://github.com/lucamanni/awesome
.. _romockee: https://github.com/romockee/powerarrow
.. _ok100: http://ok100.deviantart.com/art/DWM-January-2013-348656846
.. _amouly: https://bbs.archlinux.org/viewtopic.php?pid=1307158#p1307158
.. _swordfischer: https://github.com/lcpz/awesome-copycats/issues/53
.. _foozer: http://dotshare.it/dots/499
.. _lain: https://github.com/lcpz/lain
.. _freedesktop: https://github.com/lcpz/awesome-freedesktop
.. _Terminus: http://terminus-font.sourceforge.net
.. _Roboto: https://fonts.google.com/specimen/Roboto
.. _Tamzen: https://github.com/sunaku/tamzen-font
.. _Icons: https://github.com/lcpz/dots/tree/master/.fonts
.. _FontAwesome: https://github.com/FortAwesome/Font-Awesome
.. _Ubuntu: https://wiki.ubuntu.com/Fonts#Enabling_Bitmapped_Fonts
.. _colorscheme: https://github.com/lcpz/dots/tree/master/.colors
.. _dependencies: https://github.com/lcpz/lain/wiki#dependencies
.. _mail: https://github.com/lcpz/lain/wiki/mail
.. _weather: https://github.com/lcpz/lain/wiki/weather
