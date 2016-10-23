# Sublime-Text-Style-Guide
## Packages/Plugins
### Install Package Control
(https://packagecontrol.io/installation)

The console is accessed via the **ctrl+`** shortcut or the **View > Show Console** menu. 
Once open, paste the appropriate Python code for your version of Sublime Text into the console. 

**Sublime Text 3**
>
import urllib.request,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by) 

**Sublime Text 2**
>
import urllib2,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler()) ); by = urllib2.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); open( os.path.join( ipp, pf), 'wb' ).write(by) if dh == h else None; print('Error validating download (got %s instead of %s), please try manual install' % (dh, h) if dh != h else 'Please restart Sublime Text to finish installation') 

### Install theme (ex: cobalt2)
1. Open package control **tools → Command Palette** and type Install Package (or **Ctrl + P**)
2. Search for **Cobalt2** and hit **enter**
3. Penultimately, open **Preferences → Settings - User**. Add the following lines. Only the first two are required but I recommend using all of them: 
```ruby
"color_scheme": "Packages/Theme - Cobalt2/cobalt2.tmTheme",
"theme": "Cobalt2.sublime-theme"
```
### ALIGNMENT
To Use: Highlight the lines you want to align and press **ctrl + alt + a**
![](https://cask.scotch.io/2013/12/alignment-before.png)
![](https://cask.scotch.io/2013/12/alignment-after.png)

### BRACKETHIGHLIGHTER
This plugin provides bracket highlighting for all sorts of brackets.
![](https://cask.scotch.io/2013/12/brackethighlighter.png)

### EMMET
To Use: **ctrl + alt + enter** and start typing your Emmet styled HTML
![](https://cask.scotch.io/2013/12/sublime-emmet-start.png)
![](https://cask.scotch.io/2013/12/sublime-emmet-finish.png)
Check out our [Emmet Interactive Guide](https://scotch.io/bar-talk/write-html-crazy-fast-with-emmet-an-interactive-guide) to learn more and try out Emmet for yourself.

### DOCBLOCKR
To Use: Just type in `/**` above your function and press `tab`
![](https://cask.scotch.io/2013/12/sublime-docblockr-example-start.png)
![](https://cask.scotch.io/2013/12/sublime-docblockr-example-finish.png)

# Best config
**References -> Settings - User**
```ruby
{
	"auto_complete": true,
	"bold_folder_labels": true,
	"caret_extra_bottom": 2,
	"caret_extra_top": 2,
	"caret_style": "phase",
	"close_windows_when_empty": true,
	"color_scheme": "Packages/Theme - Cobalt2/cobalt2.tmTheme",
	"draw_white_space": "all",
	"find_selected_text": true,
	"fold_buttons": false,
	"font_size": 11,
	"highlight_line": true,
	"highlight_modified_tabs": true,
	"ignored_packages":
	[
	],
	"indent_guide_options":
	[
		"draw_normal",
		"draw_active"
	],
	"line_padding_bottom": 1,
	"line_padding_top": 1,
	"scroll_past_end": true,
	"tab_completion": false,
	"tab_size": 2,
	"theme": "Cobalt2.sublime-theme",
	"translate_tabs_to_spaces": true,
	"trim_automatic_white_space": true,
	"trim_trailing_white_space_on_save": true,
	"update_check": false,
	"vintage_start_in_command_mode": false,
	"wide_caret": true,
	"word_wrap": true
}

```
**References -> Key bindings - User**
```ruby
[
  { "keys": ["f12"], "command": "reindent"},
  { "keys": ["ctrl+shift+t"], "command": "delete_trailing_spaces" },
  { "keys": ["ctrl+shift+a"], "command": "toggle_side_bar" },
  { "keys": ["ctrl+1"], "command": "toggle_setting", "args": {"setting": "gutter"} }
]
```
