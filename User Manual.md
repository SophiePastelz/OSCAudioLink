[link to Program](https://sophiepastelz.gumroad.com/l/OSCAudioLink)
# OSCAudioLink User guide

* OSCAudioLink is a utility program that process live audio devices and send filtered signals back to vrchat to control avatar parameters
  * You can also read audiolink data and reuse it for avatar parameters

* General Knowledge
  * If you hover over most elements, there will be a tooltip saying what they do

### Refrences
> * [Startup](#startup)
> * [Verification](#verification)
> * [Global Buttons](#global-buttons)
> * [Main tab](#main-tab)
> * [Preview tab](#preview-tab)
> * [Current Avatar tab](#current-avatar-tab)
> * [Audiolink to OSC tab](#audiolink-to-osc-tab)
> * [OSC config tab](#osc-config-tab)
> * [Logging tab](#logging-tab)
> * [Info tab](#info-tab)
> * Config file


# Startup
> * The are things that will happen every time you start up the progran
> * The program will check if youre running the latest version. if youre not you will be promted to update to the latest version
> * The program will attempt to create a config file which will store settings and configurations. if it already exists it will read from it
> * The program will check that your license key is valid on each startup

# Verification
> * This screen is to verify you have a legit copy of OSCAudioLink
> * This screen will aks you from your email and your provided license key that you received when making your OSCAudioLink purchase
>   * This screen will save your credentials for later use and long as program has saved properly

# Global buttons
> #### Open Config file
> * Opens the program's currently used config file in a 3rd party text based editor
>
> #### Save Settings
> * Saves the current state of the program as a yaml file to the a file in the same directory as the program
>
> #### Save on close
> * This determines whenever to automatically save the program's current state to the settings on close

# Main tab
> * This tab is is to configure what microphone and how you wanna send process and masked audio back to vrhchat
>
> ## General Settings
> > ### Enable
> > * determines whenever any audio proccessing or sending to vrchat should be enabled
> >
> > ### Audio Device
> > * determines which audio device on your computed will have its audio signal processed and filtered by each element
> >
> > ### Multiplier 
> > * This multiplies the audio device's volume by what you set the value to
> 
> ## Element(s)
>
> ### Buttons
> 
> > ##### New element
> > * Adds one of these 4 options: Slider, Radial Puppet, Toggle, Selection menu
> >
> > ##### Import
> > * Import a file containing settings for how element(s) should be configured
> >
> > ##### Export all
> > * When clicked it will export each element into a .yaml file you can import later or share with someone else
> >
> > ##### Removed All
> > * Deletes all elements that have been added
> 
> ### Element
> 
> > ### Actions
> >
> > > ##### Delete Element
> > > * Deletes the current element
> > >
> > > ##### Clone Element
> > > * Clones the current Element and its accosiated settings
> > >
> > > ##### Copy Mask settings
> > > * Copies the settings that are in: MaskLeft, MaskRight and MaskBottom from >the current element
> > >
> > > ##### Paste Mask settings
> > > * Overwrites the current mask settings (if any in the clipboard) to the >current element
> > > 
> > > ##### Move up
> > > * Moves the current element's position by 1 step up
> > >
> > > ##### Move Down
> > > * Moves the current element's position by 1 step Down
>
> > ### Enabled
> > * Determines whenever the current element should process any data or send anything to vrchat
> 
> > ### Target
> > * This is where you wanna send the processed data to
>
> > ### Type
> > * Determines what data type the processed data should be converted to to send back to vrchat
> 
> > ### MaskLeft
> > * This determines the start of the mask should capture in hz and where the mask's left wall should be located in the Preview tab
> 
> > ### MaskRight
> > * This determines the end of the mask should capture in hz and where the mask's Right wall should be located in the Preview tab
>
> > ### MaskBottom
> > * This determines how sensitive the maks should be before capturing any data from it and where the bottom box height i located in the preview tab
> 
> >### Start
> > * This is Where the Output value should be located at when the processed audio is completely quiet
>
> > ### End
> > * This is where the Output value should end up when it is completly maxed out (Note this may be overwritten by the Mode)
>
> > ### Multiplier
> > * Multiples the current element's Processed audio Output's value
>
> > ### Smoothing
> > * Makes the output value of the the current element take the configured amount of seconds to reach the Output value's value
>
> > ### Mode
> > * This dropdown menu selects how the output number of the current element behaves
> > > Clamp
> > > * This makes the output number stay between the min and max value
> >
> > > Wrapround
> > > * This makes it so if the input number gets bigger than the max value of less than the min value it will "wrap-around" to the beginning number and continue from there
> >
> > > Bounce
> > > * Bounce makes sure the input number stays between min and max by bouncing backwards and forward to stay inbounds of the range
> >
> > > None Filter
> > > * This will just output the raw input number not affected by min or max
> 
> > ##### Preview
> > * Detemines whenever the current element should be visible in the Preview tab (May save on performance)

# Preview Tab
> * This tab displays the live audio device's audio wave frquencies and where the mask's are configured on the graph
> * its important for visalizing configured elements and how they to the inputted audio
>
> # axes
> > Y Axis 
> > * determines how much power the audio gives (Or how loud it is)
> 
> > X Axis
> > * Displays each frenquency in the audio device from 0hz to 22100hz
>
> # Element
> * The box's Bounds is determinded by the element's: MaskLeft, MaskRight, MaskBottom and Multiplier
> * * The Multiplier setting will determine how tall or how small the height of the box will be
> * The red line will display the raw outpout value
> * The yellow line is the current value
> * * You will only see the yellow line behind the red line if you have smoothing parameter in the current element set high enough
> > ### Label
> > * Diplays the configured address
> > * Displays how many times the output paramenter has wrapped or bounced bwtween start and end
> >
> > ### Start
> > * Displays the configured Start Value
> > 
> > ### End
> > * Displays the configured End Value
> >
> > ### Value
> > * Displays the Current live Output value
> >
> ### Hide masks
> * Hides Every Masks that configured in the [Main tab](#main-tab)

# Current Avatar tab
> This tab (when enabled) will try to fetch the currently worn avatar's data to help you add parameters to sync.
> > The program will attempt to read the latest game logs and osc folders from "%userprofile%\appdata\locallow\VRChat\VRChat" and retreive data such as:
> > * Avatar's input and output parameters
> >   * Current parameters value
> > * Avatar's name
> > * Avatar's ID
>
> ## General Settings
> > ### Enable
> > * Enables fetching the currently worn vrchat avatar and its data
> > ### Record
> > * When pressing this button, it will start recording for 7 seconds. during this period the program will attempt to find avatar parameters that change during this duration. when recording is done it will automatically switch to the recorded tab
> > ### Auto-Add
> > * When Enabled this will Automatically add the the Recorded parameters to the [Main tab](#main-tab) without having to click the add to "Add to [Main tab](#main-tab)" Button
> > ### Fetch values
> > * This will update each parameter's value in the list to its current value
> > ### Search Parameter
> > * This will seach for the inputted parameter name 
> >   * Press the X button to clear the current search
> > ### Copy to clipboard
> > * Copies the avatar name and the avatar's id to the clipboard
>
> # Tabs
> > # Input
> > * This tab is all the paramaters you can use to sync to music 
> > # Output
> > * This tab is all the parameters that arent able to be changed
> >   * These are most of the time vrchat default parameters
> > # Recorded
> > * These are the parameters that got detected during a parameter change recording
>
> # Parameter
> > ### Add to [Main tab](#main-tab)
> > * Adds the current address to the [Main tab](#main-tab) 
> > ### Copy to clipboard
> > * Copies the Current Address to the clipboard
> > ### Address
> > * current parameter's address
> > ### Type
> > * The current parameter's data type
> > ### Value
> > * The current parameter's value
> >   * This can be updated with the "Fetch Values button" 

# AudioLink to OSC tab
> * This is a way to capture data from vrchat worlds with intergrated audiolink and reused that data and sync avatar parameters with them
>   * NOTE: This requires a prefab to properly function
>   * NOTE: This requires the current avatar to be enabled to check if the AudioLinkOSC Prefab is enabled
>   * Note: if vrchat is running from a different location than the "C:" drive you will need to open the config file and sepcify where vrchat is running from 
>
> * Available data to use is:
> > * Bass
> > * LowMids
> > * HighMids
> > * Treble
> > * All
>
> ## General Settings
> > ### Enable
> > * Enabling this will enable the program to look for the AudioLinkOSC prefab and check if its enabled on you current avatar. Once found you will see a 128 by 64 sized block
> >   * If the program cant find the prefab enabled it will send a Error message to The [logging tab](#logging-tab)
> > ### Add new element
> > * Adds a new element to the list
>
> ## Element(s)
> > ### Actions
> >
> > > ##### Delete Element
> > > * Deletes the current element
> > >
> > > ##### Clone Element
> > > * Clones the current Element and its accosiated settings
> > >
> > > ##### Move up
> > > * Moves the current element's position by 1 step up
> > >
> > > ##### Move Down
> > > * Moves the current element's position by 1 step Down
> > ### Enabled
> > * if the current element should send any data
> > ### Target
> > * The address the current elementr should send the data to
> > ### Band
> > * Which Band the the current element should read the data from
> > ### Start
> > * This is what value should be outputted when selected band is completly black or 0'ed out
> > ### End
> > * This is what the value should be outputted when the selected band is completely White or at 1
> > ### Multiplier
> > * This is what the Output value should be multiplied with before (note: doesnt overstep the End value)

# OSC Config tab
> * This is determines where the all the data should be sent to
> ## Config
> > ### OSC Sending Address
> > * The addreess of where the Data from the [Main tab](#main-tab) and the [AudioLinktoOSC](#audiolink-to-osc-tab) tabs should be sent
> > ### OSC Sending Port
> > * The port of where the Data from the [Main tab](#main-tab) and the [AudioLinktoOSC](#audiolink-to-osc-tab) tabs should be sent
> > ### OSC Listening Address
> > * The address of where to listen to the data for the [Current Avatar tab](#current-avatar-tab)
> > ### OSC Listening Port
> > * The port of where to listen to the data for the [Current Avatar tab](#current-avatar-tab)

# Logging tab
> * This tab logs most stuff so you can better understand whats happening in the program

# Info tab
> > ### Patch notes
> > * Patch notes from every release since version 1.0
> > ### Guides 
> > * In heres the is a bunch of frequencies you can expermiment with
> > ### Credits 
> > * in this tab there a links to the store page, discord server, and SophiePastel'z website :3

# Others
>
> ## How to set up with [VOR (Vrhchat OSC Router)](https://github.com/SutekhVRC/VOR)
> VOR allows you to have multiple apps listen to vrchat
>
> This is just an example way of does this
>
> * Go to OSCAudioLink's [OSC Config tab](#osc-config-tab) and configure the [OSC Listening Port](#osc-listening-port) to be 9501 and the [OSC Listening Address](#osc-listening-address) to be 127.0.0.1
> * Now go to [VOR (Vrhchat OSC Router)](https://github.com/SutekhVRC/VOR) 
> * Go to the "Apps" Tab
> * Click "Add new VOR app"
> * Set "App Name" to "OSCAudioLink"
> * Set "App Host" to "127.0.0.1"
> * Set "App Port" to "9501"
> * Click "Save"
> * Go to the "Main" tab
> * Click "Start"
> * That should be it. Optionally click on the "debug" to see if your receving anything from OSCAudioLink
