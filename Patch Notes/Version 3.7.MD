* Backend changes
### `Main`
* Added a new configurable value called `Smoothing`
* * Depending on its value it will smooth out the output value according to the selected number
* * * The number means it will take that many seconds to reach the value that get picked up
### `Config`
* Added a new parameter to each element in `OSC.Main.Elements` called `Smoothing`