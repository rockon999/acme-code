README

    Gnome Shell Extension Reloader extension-reloader

    2016-11-12

    This extension is intended for use by Gnome Shell Extension writers.
    It is common practice to restart the Shell during testing to reload
    an extension with changes made to the extension's code. Wayland does
    not allow restarting the Shell.  To reload an extension under Wayland
    a logout and a login is required.  This extension reloads only the
    selected extension with two mouse clicks saving time for the extension
    writer. This extension requires the reload option in the recently
    updated gnome-shell-extension-tool (Gnome Bugzilla #772593).  A copy
    of the new tool from the Gnome Github mirror is included with this
    extension. The new tool is not included in GS 3.22.2.

    The upcoming release of Fedora 25 will default to using Wayland instead
    of Xorg.  I have submitted an enhancement patch to the gnome-tweak-tool
    (Gnome Bugzilla #774072) to include buttons for reloading extensions in
    the Extensions section of the Tweak Tool.

    When the gnome-shell-extension-tool with reload capability is released,
    the borrowed copy of gnome-shell-extension-tool will be removed from this
    extension.

    2016-11-13 Uploaded to ego for review.

    2016-11-23 Extension Reloader - updated copyright due to fsf address changed
               Removed address and added license url instead. Uploaded for review.

    2016-12-23 Extension Reloader - Almost a complete rewrite.
               Removed the gnome-shell-extension-tool, replaced with extension
               code to directly control the shell extenson system.  Added
               display of extension state to menu, sorted extension display by
               state and name. Added scrolling to menu.  Changed notifications
               to indicate info, warning and error as appropriate.

               This extension replaces the need to [ Alt F2 r ] to restart the
               shell during extension development.  This extension will attempt
               to reload the extension when it is in the error state.  The most
               common shell restarts for extension writers are when an extension
               is in the error state.  If the error in the extension code is
               corrected a restart with this extension will reload it successfully
               except in very rare instances.  Gnome Shell extensions can have
               errors that are only exposed if the extension is reloaded. One such
               error is the import of prefs.js into an extension. The the prefs.js
               code is intended only to be executed by gnome-shell-extension-prefs.

   2017-04-05  Added GS3.24 to metadata.json.

   2017-05-21  Translations updated. Thanks to Jonatan Zeidler.

   2018-04-15  Changed to be compatible with Ubuntu 18.04 LTS. Uploaded for review.

   2018-09-03  Thanks to treba123 for merge request which corrected class name
               changes needed for GS 3.29.92 and beyond.

               See https://nls1729.github.io/extension-reloader.html , note when
               an extension is not in the error state reloading will not read
               changes made to disk.  This limits the use of the extension to
               making changes when an extension is in the error state.

               Uploaded for review.

   2018-10-03  Completed changes for ES6.
               Changed code to use arrow notation => instead of Lang.bind for anonymous
               functions. Changed code to use ES6 classes. Updated prefs.js to use GJS ES6
               class wrapper for GObject class. Changed to use Function.prototype.bind()
               instead of Lang.bind for named call backs.

   2018-10-09  Uploaded for review.

zip file: Tue Oct  9 14:36:57 EDT 2018 79049d556ec148cb5bfb19f5af39ff79176ea97b

...
