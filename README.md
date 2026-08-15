<h1 align="center" style="font-size: 2em; font-weight: bold; margin: 0;">Verity - Bedrock Edition | Setup Guide</h1>

**This is the page that guide you how you can set up Verity - Bedrock Edition (version 4.0.0)**

<img width="689" height="317" alt="image" src="https://github.com/user-attachments/assets/48dea204-5971-4cac-9acd-0e1e9fbd78d6" />


## Downloads


You can download Verity - Bedrock Edition (version 4.0.0) from [Curseforge](https://www.curseforge.com/minecraft-bedrock/addons/verity-bedrock-edition) & [MCPEDL](https://mcpedl.com/verity-bedrock-edition/)


## Installation

> [!NOTE]
> Voicechat, AI are not officially supported on Minecraft Bedrock!

### Android

| **Using Termux & Termux:API** |
|:-|
| 1. Install [F-Droid](https://f-droid.org/) |
| 2. Open F-Droid, search for, and install both Termux and Termux:API <br> (Ensure both are installed from F-Droid , If you're having trouble, ask an AI for help) |
| 3. <br> - Press & hold the Termux:API app icon $\rightarrow$ Tap App Info. <br> - Go to Battery (or Power) $\rightarrow$ Choose Unrestricted (or No restrictions). <br> - Go back $\rightarrow$ Tap Permissions $\rightarrow$ Microphone $\rightarrow$ Choose Allow. |

<br>

| **SETUP on Android** |
|:-|
| 1. Extract the "verity-android-setup.zip" file you downloaded directly in the "Download" folder |
| 2. Click on verity-android-setup and open the .env file then get the API keys/FishAudio Models ID to insert!! <br> - Groq API Keys : [Create your API keys here](https://console.groq.com/keys) <br><br> - FishAudio API Keys : [Create your API keys here](https://fish.audio/app/api-keys/) <br><br> - FishAudio Models ID : [Find your favourite Model Id here](https://fish.audio/app/discovery/?q=verity) |
| 3. Open **Termux** and run the following commands sequentially : |

<br>

1. Update packages & install dependencies :
```
pkg update -y && pkg install -y termux-api play-audio which unzip python python-pip dos2unix
```

<br>

2. Grant storage permission :
```
termux-setup-storage
```
> [!NOTE]
> Tap Allow when prompted for storage access permission

<br>

3. Check Microphone :
```
which termux-microphone-record
```
> [!IMPORTANT]
> Must print a path, For Example : /data/data/com.termux/files/usr/bin/termux-microphone-record








<br>
<br>

