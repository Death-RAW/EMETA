
# EMETA AVATAR TESTING STEPS

A brief description of what this project does and who it's for


## Software and Hardware Requirements 
- [Unity with Unity Hub](https://public-cdn.cloud.unity3d.com/hub/prod/UnityHubSetup.exe)
```
Install Unity Version 2022.3.32f1 LTS
```
- Meta Quest pro, 2, or 3 with USB cable
- [Meta Quest Link app](https://www.meta.com/en-gb/help/quest/articles/headsets-and-accessories/oculus-rift-s/install-app-for-link/)
``` Note : you will need a supported GPU in your laptop, minimum Geforece 1650 ti ```




## Repos and Builds

Server Version is already runnig on the **Ubuntu server 20.4** at **193.167.189.219**
## Runnig without the VR headsets and debugging
- Step 1 : [Download the client build form here](https://unioulu-my.sharepoint.com/:u:/g/personal/ijayasun23_univ_yo_oulu_fi/EYevkTNw27pCnyAR6nAwquEBgEqsemhOsg-rmM74BBiDng?e=t0tN5M)
- Step 2 : 
```Run the exe file```
- Step 3 :
```click on the start cilent button. This should spawn the avatar on to the scene.```

![image](https://github.com/user-attachments/assets/bc2ed08b-79e3-4a67-b2b3-a0254b0be242)
- Step 4 :
```You can run as many clients as needed```
- Step 5
```Use the mouse and W A S D keys to control the Avatar```

## Runnig without the VR headsets in Unity for debugging

- Step 1 : [Download the client repo form here](https://unioulu-my.sharepoint.com/:u:/g/personal/ijayasun23_univ_yo_oulu_fi/EQxkl5rcXOxPuGItI1mNK6IBOJcpFVBY47j0RWOETUah-g?e=t16cEP)
- Step 2 : Unzip the folder
- Step 3 : Open the Project in Unity Hub
```Click on the Projects tab on the left side. Click the Open button. Navigate to the folder where you extracted the project. Select the folder containing the Assets, ProjectSettings, and other subfolders (this is the root folder of the project), then click Select Folder. Let Unity Load the Project```
![image](https://github.com/user-attachments/assets/b1350ff5-0049-4773-906a-0934659ee67e)

**Note : If prompted to upgrade the project, decline if possible, or confirm that it’s okay before proceeding (depending on the Unity version installed).
Check for Missing Packages (if necessary):
If there are missing dependencies or packages, Unity may prompt you to install them. Follow the instructions in the Unity console if any packages need to be installed.**

- Play the Project:

```Once the project is loaded, look for the Scene folder. open the scene v1. ```
```Click the Play button at the top center of the Unity Editor to run the project in the Unity Editor.```

**Note : You can use unity's in build profiler or [FishNet Profiler Plugin](https://github.com/FirstGearGames/FishNet) for analysys.**

## Server debugging and analysys

**The project is inside the ```EMETA/LinuxBuld``` folder of the ubuntu server and runnig on the headless mode (without graphics). (Which I have given access already. use the pem file and the passcode for SSH)**

- To run the Server build issue the command below (I already set it up to run always, and will be uploading new changes)

```ubuntu@emeta:~/EMETA/LinuxBuild$ ./emeta.x86_64 -batchmode -nographics```

- To get the server log to a file issue the following command

```ubuntu@emeta:~/EMETA/LinuxBuild$ ./emeta.x86_64 -batchmode -nographics > server.log 2>&1 &```

[You can download the server repo from here]()

## CSC Poutha Information

VM is hosted on [https://pouta.csc.fi/](https://pouta.csc.fi/) with the following specifications. 
- public ip
```193.167.189.219```
- Configuration

![image](https://github.com/user-attachments/assets/6679edc7-4785-4afa-be73-2f5f6c536674)
![image](https://github.com/user-attachments/assets/f43e52ee-8040-4af4-b0aa-db2935e68e9c)

- Allowed Ports on the server
![image](https://github.com/user-attachments/assets/ad7d59f3-b9d2-47c3-9c08-6f117d989248)
