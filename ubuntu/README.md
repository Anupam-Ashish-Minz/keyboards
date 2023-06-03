Using Ubuntu
-----------

Download the real-prog-dvorak file and do the following 

```
mkdir -p ~/.config/xkb/{rules,symbols} 
cp /usr/share/X11/xkb/rules/evdev.xml ~/.config/xkb/rules/
cp /usr/share/X11/xkb/symbols/us ~/.config/xkb/symbols/
cat real-prog-dvorak >> ~/.config/xkb/symbols/us
```


Then you have to update the `~/.config/xkb/rules/evdev.xml` with the following, add it near the other English keyboards

```
<variant>
    <configItem>
        <name>real-prog-dvorak</name>
        <description>English (Real Programmers Dvorak)</description>
        <vendor>MichaelPaulson</vendor>
    </configItem>
</variant>
```

To load the changes setxkbmap with -I flag can be used. 
Some DE like gnome might already load this from the start.

If this doen't work it that case you might want to diretly edit the xkb files is /usr/share/X11/xkb ... 
but be warned as update to this file will cause you changes to be reset.
