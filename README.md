# SDK Update Center
The Repository containing the Netbeans Modules for every nightly/tagged release, so they can be accessed by the SDK's Auto Updater.

The process is as follows:
 - A new commit is present on the SDK Repository
 - A Build on __this__ repository is triggered
 - This builds the SDK Repository
 - This builds the netbeans modules by invoking the nbm command
 - The nbms are uploaded to github as releases to __this__ repository (so that the main repository stays clean and users still find their regular installer downloads)
 - The build commits the updates.xml (which is what the SDK scans) to the `master-xml` branch.
 - For a dot release (e.g. `3.3.0-sdk2`) the process is the same, however we use different branches, namely one XML Branch per major release
 
 In other words: This is just an infrastructure repository, there is nothing to see here for you, unless you are interested in deploying a Netbeans Update Center for your own RCP.
 
 You are most likely looking for https://github.com/jMonkeyEngine/sdk
