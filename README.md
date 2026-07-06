# Game of Life Python exhibit

A Python program to run Game of Life exhibits/demos, complete with trifold flyer.

When I was 15 I got interested in John Conway's Game of Life reading an article about it in the October 1970 issue of the *Scientific American* magazine.

This project is Python code designed to run Game of Life exhibits endlessly running on TV monitors. (I used a Raspberry Pi with HDMI to the monitor.)

As well as the Python code, `life.py`, there is a Latex flyer (`flyer.pdf` and `flyer.tex`) and a short Mathematica notebook to generate 3D-looking colored stones for live cells. The PDF of the flyer and the stone PNG files are part of this repository, so you don't need either Latex or PDF to get things to work.

## There are two exhibits and a tryfold flyer:

- A pre-planned collection of named life forms

- A random initial grid, which changes every time it is run

- Plus a trifold flyer `flyer.pdf`

## Configuring

The code includes hard-wired design decisions:

- Size of grid
- Size of invisible border (e.g., so gliders can run off the visible part of the screen and not fall apart at the edges)
- Font to use
- Detectable cycle length (automatically stop when pattern repeats)
- Maximum iterations (may have long repeat cycles or not repeat at all)
- Sequence of pre-planned and random exhibits
- Mathematica code to generate life cell images (the Python knows how many images you are using)

It is perhaps easiest to configure it to have a single run (alternating preplanned and random grids) and record it all to a MP4 file on a USB stick, then put the USB in the back of a suitable monitor to play endlessly. (This means you don't need to keep a Raspberry Pi running somewhere all the time - and everyone understands switching TV monitors on/off.)

If you use a saved run, you may like to record several random grids so they are all different. Just set the `demoSchedule` variable to `[False, True, False, True, False, True]` etc
