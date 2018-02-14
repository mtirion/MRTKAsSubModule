# MRTKAsSubModule
Sample repository how to setup a Unity project using MRTK as a sub module.

## Create a Unity project and put it in github ##
	1. Create a repository in github for [PROJECTNAME]
       Select .gitignore for Unity
       Add readme
	2. Git clone [PROJECTNAME] on your local machine
	3. Rename [PROJECTNAME] to [PROJECTNAME]-GIT
	4. Create the Unity project with name [PROJECTNAME] and save
	5. Copy the contents of [PROJECTNAME] to the [PROJECTNAME]-GIT folder
	6. Delete [PROJECTNAME] folder
	7. Rename [PROJECTNAME]-GIT to [PROJECTNAME]
    8. Publish to git

       git add .
       git commit -m "[comment]"
       git push

## To add a link to MRTK ##
	1. In the root directory of [PROJECTNAME] clone MRTK as submodule:
       
       git submodule add https://github.com/Microsoft/MixedRealityToolkit-Unity.git

	2. Make a folder link in Assets to the HoloToolkit folder. Run this command from within the project folder:

       mklink /j .\Assets\HoloToolkit .\MixedRealityToolkit-Unity\Assets\HoloToolkit

	3. Open the project in Unity to import the MRTK. 
    4. Set the project settings using the MRTK menu [Configure - Apply Mixed Reality Project Settings]
    5. Set the MRTK specific scene settings using the MRTK menu [Configure - Apply Mixed Reality Scene Settings]
    6. Build the UWP project
    7. Modify the .gitignore to ignore the HoloToolkit folder in the Assets folder. Add:
    
       /Assets/[Hh]olo[Tt]oolkit*

	8. Publish to git
       
       git add .
       git commit -m "[comment]"
       git push

## To retrieve the project (first time) ##

	1. Clone the repository
       
       git clone --recursive [project github url]

	2. Make a folder link in Assets to the HoloToolkit folder. Run this command from within the project folder:

       mklink /j .\Assets\HoloToolkit .\MixedRealityToolkit-Unity\Assets\HoloToolkit

	3. Open the project in Unity
	4. Open the main scenario
	5. Set the project settings using the MRTK menu [Configure - Apply Mixed Reality Project Settings]

