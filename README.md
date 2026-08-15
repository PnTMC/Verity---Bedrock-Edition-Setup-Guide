<h1 align="center" style="font-size: 2em; font-weight: bold; margin: 0;">Verity - Bedrock Edition | Setup Guide</h1>

<p align="center">
  <b>This guide will help you set up Verity - Bedrock Edition (v4.0.0)</b>
</p>

<p align="center">
  <img width="689" height="317" alt="Verity Banner" src="https://github.com/user-attachments/assets/48dea204-5971-4cac-9acd-0e1e9fbd78d6" />
</p>


## Downloads


You can download Verity - Bedrock Edition (v4.0.0) from:
* [CurseForge](https://www.curseforge.com/minecraft-bedrock/addons/verity-bedrock-edition)
* [MCPEDL](https://mcpedl.com/verity-bedrock-edition/)


## Installation

> [!NOTE]
> Voicechat and AI are not officially supported features on Minecraft Bedrock natively!

### Android

| **Using Termux & Termux:API** |
|:-|
| 1. Download and install **[F-Droid](https://f-droid.org/)** |
| 2. Open F-Droid, search for, and install both **Termux** and **Termux:API** <br> (Ensure both are installed from F-Droid , If you're having trouble, ask AI for help) |
| 3. <br> - Press & hold the **Termux:API** app icon $\rightarrow$ Tap **App Info**. <br> - Go to **Battery** $\rightarrow$ Choose **Unrestricted** (or No restrictions). <br> - Go to **Permissions** $\rightarrow$ **Microphone** $\rightarrow$ Select **Allow** |

<br>

| **SETUP on Android** |
|:-|
| 1. Extract the `verity-android-setup.zip` file you downloaded directly in the `Download` folder |
| 2. Click on `verity-android-setup` and open the `.env` file then get the API keys/FishAudio Models ID to insert!! <br> - Groq API Key: [Create your API keys here](https://console.groq.com/keys) <br><br> - FishAudio API Key: [Create your API keys here](https://fish.audio/app/api-keys/) <br><br> - FishAudio Models ID: [Find your favourite Model Id here](https://fish.audio/app/discovery/?q=verity) |
| 3. Open **Termux** and run the following commands sequentially : |

<br>

1. **Update packages & install dependencies** :
```
pkg update -y && pkg install -y termux-api play-audio which python-pip
```

<br>

2. **Grant storage permission** :
```
termux-setup-storage
```
> [!NOTE]
> Tap Allow when prompted for storage access permission

<br>

3. **Check Microphone** :
```
which termux-microphone-record
```
> [!IMPORTANT]
> Must print a path, For Example : /data/data/com.termux/files/usr/bin/termux-microphone-record

4. **Create new folder in Termux** :
```
mkdir -p ~/verity-android-setup
cp -a /storage/emulated/0/Download/verity-android-setup/. ~/verity-android-setup/
```

> [!NOTE]
> If cp fails, try "cp -a /sdcard/Download/verity-android-setup/. ~/verity-android-setup/" <br> If fails again , try "cp -a ~/storage/downloads/verity-android-setup/. ~/verity-android-setup/"

5. 
```
cd ~/verity-android-setup
```

6.
```
dos2unix start_android.sh
chmod +x start_android.sh
```

7.
```
pip install python-dotenv httpx websockets==10.4 --break-system-packages
```

8. **Run Verity** :
```
bash start_android.sh
```

> [!NOTE]
> After you run this command, open **Minecraft**, install the add-on, enable **Beta APIs**, and turn on **Cheats**.



<br>
<br>

