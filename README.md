# Consolas (Version 7.00)
## Consolas patched by [nerd-font](https://github.com/ryanoasis/nerd-fonts)

1. Download & unpack nerd fonts patcher
- https://github.com/ryanoasis/nerd-fonts#option-9-patch-your-own-font
2. Get consolas fonts from C:/Windows/Fonts
- or use those in orig
3. install fontforge via package manager
4. Run these

```bash
# check exact command in READMEs in subdirs
fontforge -script font-patcher -s -l -w -c --progressbars -out tmp/font-mono-output orig/consolas.ttf

# install generated font
# Ref.: https://docs.fedoraproject.org/en-US/quick-docs/fonts/
sudo mkdir -p /usr/local/share/fonts/consolas-nf
sudo cp ~/Downloads/robofont.ttf /usr/local/share/fonts/consolas-nf/
sudo chown -R root: /usr/local/share/fonts/consolas-n
sudo chmod 644 /usr/local/share/fonts/consolas-n/*
sudo restorecon -vFr /usr/local/share/fonts/consolas-n
sudo fc-cache -v

# get font name & style
sudo fc-list | grep -i "nf"
```


# Crydsch instructions

1. Download nerd fonts patcher + install dependencies
2. Run `fontforge -script font-patcher CONSOLA.TTF --fontawesome --fontawesomeextension --fontlinux --octicons --powersymbols --pomicons --powerline --powerlineextra --mdi --weathericons --progressbars`
3. Rename file and copy to ~/.fonts
4. Run `fc-cache -v` and check new font in ~/.fonts is detected
5. Run `sudo fc-list | grep -i "Consola"` to get font name and style
