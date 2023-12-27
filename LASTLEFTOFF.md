Found out that Dracula.itermcolors is wrong in a bunch of different ways

Went through and fixed every single color based on the official specification:

<https://spec.draculatheme.com/>

Also, referenced the Dracula VS Code theme, which allegedly implements the
specification:

<https://github.com/dracula/visual-studio-code/blob/master/src/dracula.yml>

Use this for printing 256 ANSI colors:

<https://askubuntu.com/a/1103356>

```sh
for i in {0..255}; do printf '\e[48;5;%dm%3d ' $i $i; (((i+3) % 18)) || printf '\e[0m\n'; done
```

Referenced this article for 16 ANSI colors:

<https://www.warp.dev/blog/how-we-designed-themes-for-the-terminal-a-peek-into-our-process>

Used this tool for hex to RGB:

<https://www.rapidtables.com/convert/color/hex-to-rgb.html>


```python
print("██████")
```

iTerm issue that has some more information:

<https://gitlab.com/gnachman/iterm2/-/issues/3989>

---

LAST LEFT OFF:

Working on Dracula-patched-reformat.itermcolors


