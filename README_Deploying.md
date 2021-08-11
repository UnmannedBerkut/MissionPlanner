Building for deployment.
Taken from: https://discuss.ardupilot.org/t/how-do-i-create-an-installer-for-a-custom-build-of-mission-planner/53429

Setup Wix toolset https://github.com/wixtoolset/wix3/releases/tag/wix3112rtm
Build a release version of MissionPlanner and Plugins
Build the WIX project from the MissionPlanner solution, it outputs to the msi folder
go to the msi folder
run installer.bat
open create.bat and edit to match your settings and tool locations, delete the section which supposed to copy packages to the distribution servers.
run create.bat


Tips for a hung build:
If a build gets hung for more than a minute or two try:
-clean
-close Viusal studio
-reopen
-build

Also...
-Right click on project -> "Manage NuGet packages"
-Select gear in upper right hand corner
-Under "general" unselect: "Automatically check..." and "Allow format selection..."