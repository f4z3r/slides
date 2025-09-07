# VISCon Hands-On on wasmCloud

Presentation for the VISCon conference on wasmCloud.

This uses `presenterm`. DevBox provides the necessary tooling and shell scripts to directly present
it in the terminal. Note that using Kitty as a terminal provides the best results for rendering
images and animated GIFs.

Thus the best way to launch this is:

```sh
# in a terminal WITHOUT tmux running, launch kitty
devbox run kitty
# in the kitty terminal, launch the presentation
devbox run present
# in a different terminal, if desired, launch the speaker notes
devbox run notes
```

You can then increase the font size using `ctrl-+`, decrease with `ctrl-_`, and reset with
`shft-ctrl-bspc`.
