* Backend changes to how the audio is calculated
* Changed the default bands when starting program for first time or after reseting config file

### `main`
* Elements in main now need to be adjusted due to how audio is calculated now

### `Preview`
* Renamed `block-size` to `Frequency(Hz)`
* Renamed `Magnitude(dB)` to `Power(dB)`
* Added more number divisions and made the texts smaller
* Added a grid to better visualize numbers
* Made the text label texts inside
* Label texts now has a outline and italic text
* Made the whole preview thing be full-screen
* No longer white background (Eyes can finally rest)
* Made the frequencies way more accurate

### `Config`
* Added a version parameter
* * This will say the last version of the config file it was saved with