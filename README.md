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
```sudo dnf install cascadia-code-nf-fonts```
If the installation was successfull, in you local terminal you should be able to see the cascadia-code-nf-fonts as an option in fonts.

After installing navigate to the alacritty.tmol
```cd .config/alacritty/```
Open to edit the all the lines with 'Jetbrains nerd font' to 'cascadia-code-nf-fonts' as follows;
```nano alacritty.tmol```
from `family = "JetBrains Mono Nerd Font"` to 
```
family = "Cascadia Code NF"
```
save then exit.

