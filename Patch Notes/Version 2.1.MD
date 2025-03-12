### `Main`
* Replaced wraparound toggle with a dropdown menu
* * This dropdown menu selects how the output number behaves
* * * Clamp
* * * * This makes the output number stay between the min and max value
* * * Wrapround
* * * * This makes it so if the input number gets bigger than the max value of less than the min value it will "wrap-around" to the beginning number and continue from there
* * * Bounce
* * * * Bounce makes sure the input number stays between min and max by bouncing backwards and forward to stay inbounds of the range
* * * None Filter
* * * * This will just output the raw input number not affected by min or max

### `Backend`
* Optimizations

# Note
* Removed version numbers in the exe file name
* Your previous config file will not be compatible