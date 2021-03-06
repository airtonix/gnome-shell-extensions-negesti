Put Window
==========


If you enable this extension the metacity move window keybindings are
replaced.


ChangeLog
-------

__May 12, 2012__

 * Added GTK Settings window 
  * Open from [extensions.gnome.org](https://extensions.gnome.org/local/)
  * Open from command line `gnome-shell-extension-prefs putWindow@clemens.lab21.org`

__April 26, 2012__

 * Extension is now **3.4** compatible (Tested with 3.4.1)
 * SettingsWindow is disabled for the moment (will be replaced by tweak-tool "plugin")
 * **The shell uses gsettings now!**

__January 15, 2012__

 * added a config ui
 * position.x/y/width/height must be integers between 0 and 100 (was 0...1)

__December 17, 2011__

 * fix a bug that occures if the top panel is hidden.
  * checkout https://extensions.gnome.org/extension/42/auto-hide-top-panel/ it's awesome!

__December 11, 2011__

 * reduced the horizontal and vertical "gap" between windows
 * hitting move_to_center twice will now correctly maximize evolution

Keybindings
-----------

Details how to configure can be found in the [wiki](https://github.com/negesti/gnome-shell-extensions-negesti/wiki)

Keybindings are configured using gsettings. Currently a predefined schema is used

                org.gnome.desktop.wm.keybindings

The following keys are used:

* move-to-side-n
  *  move to north edge, height: 50% width 100%
* move-to-side-e
  *  move to easth edge, height: 100% width 50%
* move-to-side-s
  *  move to south edge, height: 50% width 100%
* move-to-side-w
  *  move to west  edge, height: 100% width 50%
* move-to-corner-XY   width 50% height 50%
  *  move-to-corner-ne
  *  move-to-corner-se
  *  move-to-corner-sw
  *  move-to-corner-nw
* move-to-center
  *  move to center of the screen, widht 50% height 50%. Press twice to maximize the window
* move-to-workspace-1
  *  resize to a configured location (see wiki for details)

To modify this keybinding you can use dconf-editor or gsettings  

                apt-get install dconf-tools (for debian/ubuntu)  
                gsettings set org.gnome.desktop.wm.keybindings KeyName value

* **KeyName**... as described above (move-to-side-n,...)  
* **Value**..... for example "['<Alt>KP_8']" (with all both quotes) 



2 screen setup support
-------

the extention works well with 2 screens in horizontal setup.

Moving windows from one screen to another only possible widh side_e and side_w  
and only if windows was at side_e (or side_w) before. eg.

* a window in corner_nw of the right screen is not move to the left screen.
* a window at side_e of the right screen is move to the left screen (side_w)


- - -
TODO
----

* 2 screens support vor vertical alignment
* a lot of things i currently dont remember :)


Check https://github.com/negesti/gnome-shell-extensions-negesti/tree/master/putWindow@clemens.lab21.org
for more details.
