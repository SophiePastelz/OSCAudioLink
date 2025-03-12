### `Backend`
* Redid how things are threaded and calculated aka optimizations

### `Main`
* Added a new parameter called `innerheight`
* * This is a scale from 0-1 that moves the bottom line between the top and bottom values

### `Config file`
* Added `innerheight` to each item at `OSC.AudioLink.Elements`

### `Preview`
* Due to how the backend got changed. the audioline is now less laggy
* Added a visualizer for the new `innerheight` parameter (its a green line)

### `Current avatar parameter(s)`
* Added a button to record your current avatar's parameters change and automatically add them to the main tab for 5 seconds

# Note:
* Your old config file will not be compatible with this version