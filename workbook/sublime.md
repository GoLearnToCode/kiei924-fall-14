# Your Coding Editor: Sublime Text

### Step 1: Download and Install Sublime Text

[Click here to get Sublime Text](http://www.sublimetext.com/3). I recommend the Sublime 3 Beta. Download the appropriate installer for your computer and run it.

It's free to try out, but after 30 days you might get nagged to pay for it (which you should do).

Also don't miss the "unofficial" but excellent [documentation](http://docs.sublimetext.info/en/latest/index.html).

### Step 2 Install the Package Manager

**Package Manager** is a third-party add-on that lets you, well, install more add-ons.

1. In Sublime, select menu item `View > Show Console`. This should bring up the console area at the bottom of the window.
2. In the bottom input bar of the console, copy and paste the entire text below, and then press the Enter key:

```
import urllib.request,os,hashlib; h = '7183a2d3e96f11eeadd761d777e62404' + 'e330c659d4bb41d3bdf022e94cab3cd0'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

For more information, you can read the [Offical Instructions](https://sublime.wbond.net/installation).


### Step 3: Make the UI a bit nicer

1. press Cmd-Shift-P to open Package Manager
1. Begin typing the word `install` to locate and select `Package Control: Install Package` and then press Enter
1. start typing `soda` to select the `Theme - Soda` and press Enter
1. Watch the bottom of the screen for installation progress.

### Step 4 Custom Preferences

Here's how I personalize Sublime to avoid some otherwise annoying defaults.

**On a Mac**, click the menu item `Sublime Text > Preferences > Settings - User`.
**On Windows**, click the menu item `Preferences | Settings - User`

You'll see some text appear, probably just empty `[ ]` brackets.

Replace everything you see with the following text:

``` javascript
{
  "auto_complete_commit_on_tab": true,
  "auto_complete_with_fields": true,
  "caret_style": "smooth",
  "create_window_at_startup": false,
  "draw_indent_guides": false,
  "ensure_newline_at_eof_on_save": true,
  "font_face": "Monaco",
  "font_size": 24.0,
  "hot_exit": false,
  "ignored_packages":
    [
    "Vintage"
    ],
  "remember_open_files": false,
  "save_on_focus_lost": true,
  "tab_size": 2,
  "theme": "Soda Light.sublime-theme",
  "soda_folder_icons": true,
  "translate_tabs_to_spaces": true,
  "trim_trailing_white_space_on_save": true
}
```

then select `File > Save` to save these settings.

### Step 5: Make Coding Easier

Follow the same package installation steps we used in Step 3 to install the following packages:

1. SublimeERB
1. ColorPicker

then select `Preferences > Key Bindings - User` and append this text into the window:

```javascript
[
  { "keys": ["ctrl+shift+."], "command": "erb" }
]
```
then select `File > Save`.

### Mac Only: Terminal Enhancement

**Mac Only** We can add the `subl` Terminal command, so you will have the ability to launch Sublime from the command line. Open a Terminal session, then enter the following two commands:

`sudo ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /bin/subl`
`echo "export EDITOR='subl -w'" >> ~/.bash_profile`

Now quit Terminal and open it up again, and you should be all set.
