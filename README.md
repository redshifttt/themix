# themix - the really hacky way to get more themes on tilix automatically

## Usage

If you have an Xresources file that looks like this:

```
! special
*.foreground:   #dfdfaf
*.background:   #1c1c1c
*.cursorColor:  #dfdfaf

! black
*.color0:       #1c1c1c
*.color8:       #878787

! red
*.color1:       #af5f5f
*.color9:       #af5f5f

! green
*.color2:       #87875f
*.color10:      #87875f

! yellow
*.color3:       #af875f
*.color11:      #af875f

! blue
*.color4:       #878787
*.color12:      #878787

! magenta
*.color5:       #af8787
*.color13:      #af8787

! cyan
*.color6:       #87afaf
*.color14:      #87afaf

! white
*.color7:       #dfdfaf
*.color15:      #dfdfaf
```

then you can make a Tilix theme using the colours.

To do so do:

` $ themix <Xresources theme> 'Theme name'`

The theme name will be what comes up under the color tab of your profile. After that select the theme and you're good.

