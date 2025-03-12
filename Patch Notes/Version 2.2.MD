### `Main`
* Changed the behavior of when you have 2 parameters with different types. now it will use the first type and ignore the others
* Fixed how Booleans works in the background
* Added a tooltip basically everywhere
* Renamed the blank column to `Actions`
* Centered the column texts
* Renamed `Device` to `Audio device`
* Renamed Band (Left, Right, Bottom, Top) to be Mask (Left, Right, Bottom, Top)
* Renamed `MinRange` to `Start`
* Renamed `MaxRange` to `End`
* Renamed `IndividualMultiplier` to just `Multiplier`

### `Current Avatar parameter(s)`
* Renamed it to `Current Avatar`
* Renamed `Update on avatar change` to `Enable`
* Added tooltip to `Enable`
* On startup it will now correctly fetch your current wearing avatar without having to reload your avatar
* Added a check for if OSC is even enabled in-game
* Redid how you record parameters:
* * There is now a recorded tab that will add the recorded parameters to the tab instead of automatically adding themselves to the main tab
* Fixed the `Add to OSCAudioLink` button so that it correcly adds the clamp mode
* Renamed the `Add to OSCAudioLink` button to be `Add to main`
* Added tooltips when hovering over the Copy button and `Add to main` button
* Renamed `Auto add changing parameter(s) to Main (5s)` to `Record`
* Added tooltips when hovering over the `record` button
* Changed the recording time from 5 seconds to 7 seconds
* Renamed `Fetch latest values` to `Fetch values`
* Added to tooltips to `Fetch values` when hovering over it
* Made `Record` and `fetch values` buttons be horizontally aligned
* Made current avatar id and name be horizontally aligned and use a different text display
* Added a copy button to get current avatar name and avatarid
* Now when u disable the listening parameter it will remove all data till u enable it again
* Centered tabs

### `Preview`
* Renamed `Hide bands` to `Hide masks`
* Tooltips

### `Backend`
* lots of optimazations

# Note
* Old config files will break unless edited