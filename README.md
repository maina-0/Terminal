## Setting up Alacritty,Fish and Nerd Font in Fedora.'''

# Setting up Alacritty.'''


Command for installing Alacritty in fedora is 

```
sudo dnf install Alacritty
```

Adding color schemes to Alacritty

```
mkdir -p ~/.config/alacritty/themes
git clone https://github.com/alacritty/alacritty-theme ~/.config/alacritty/themes
```

Now to install Jetbrains nerd font, run,
'''sudo dnf install cascadia-code-nf-fonts'''
If the installation was successfull, in you local terminal you should be able to see the cascadia-code-nf-fonts as an option in fonts.

After installing navigate to the alacritty.tmol
'''cd .config/alacritty/'''
Open to edit the all the lines with 'Jetbrains nerd font' to 'cascadia-code-nf-fonts' as follows;
'''nano alacritty.tmol'''

the alacritty.tmol


'''
import = [
    "~/.config/alacritty/themes/themes/catppuccin_mocha.toml"
]

[env]
TERM = "xterm-256color"

[font]
size = 18.0

[font.bold]
family = "Cascadia Code NF"
style = "Bold"

[font.bold_italic]
family = "Cascadia Code NF"
style = "Bold Italic"

[font.italic]
family = "Cascadia Code NF"
style = "Italic"

[font.normal]
style = "Regular"

# [font.offset]
# x = 0

# y = 0

[[keyboard.bindings]]
action = "Paste"
key = "V"
mods = "Control|Shift"

[[keyboard.bindings]]
action = "Copy"
key = "C"
mods = "Control|Shift"

[[keyboard.bindings]]
action = "PasteSelection"
key = "Insert"
mods = "Shift"

[[keyboard.bindings]]
action = "ResetFontSize"
key = "Key0"
mods = "Control"

[[keyboard.bindings]]
action = "IncreaseFontSize"
key = "Equals"
mods = "Control"

[[keyboard.bindings]]
action = "IncreaseFontSize"
key = "Plus"
mods = "Control"

[[keyboard.bindings]]
action = "DecreaseFontSize"
key = "Minus"
mods = "Control"

[[keyboard.bindings]]
action = "ToggleFullscreen"
key = "F11"
mods = "None"

[[keyboard.bindings]]
action = "Paste"
key = "Paste"
mods = "None"

[[keyboard.bindings]]
action = "Copy"
key = "Copy"
mods = "None"

[[keyboard.bindings]]
action = "ClearLogNotice"
key = "L"
mods = "Control"

[[keyboard.bindings]]
chars = "\f"
key = "L"
mods = "Control"

[[keyboard.bindings]]
action = "ScrollPageUp"
key = "PageUp"
mode = "~Alt"
mods = "None"

[[keyboard.bindings]]
action = "ScrollPageDown"
key = "PageDown"
mode = "~Alt"
mods = "None"

[[keyboard.bindings]]
action = "ScrollToTop"
key = "Home"
mode = "~Alt"
mods = "Shift"

[[keyboard.bindings]]
action = "ScrollToBottom"
key = "End"
mode = "~Alt"
mods = "Shift"

[scrolling]
history = 5000

[window]
dynamic_padding = true
opacity = 1.0
title = "Alacritty"

[window.class]
general = "Alacritty"
instance = "Alacritty"

# [window.padding]
# x = 0
# y = 0
'''

save then exit:
