### Auto Updater
* Added a text that specifies what version you are updating to
* Added it so it will only update if the version is behind instead of if the version is just incompatible
* Program is now packaged correctly

### Current Avatar
* If the user had multiple user folders, fetching the current avatar could failed. now the program looks through all user folders to find the current avatar's json file
* It will now tell you in the logging tab if the current avatar does not have the necessary json file 

### Import/Exporting
* Replaced broken values with fallback values

### AudioLinkToOSC
* Made the default value for "Enabled" be off by default when reseting config file

### Logging
* Added timestamp to each logged message

* Made MarkDown Text in the info tabs seletable and links clickable for current and future links
* Also added a user manual link in the guides tab in the info tab
* Redid how the backend is done