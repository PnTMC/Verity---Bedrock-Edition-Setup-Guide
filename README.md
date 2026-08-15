<h1 align="center" style="font-size: 2em; font-weight: bold; margin: 0;">Verity - Bedrock Edition | Setup Guide</h1>

<p align="center">
  <b>This guide will help you set up Verity - Bedrock Edition (v4.0.0)</b>
</p>

<p align="center">
  <img width="689" height="317" alt="Verity Banner" src="https://github.com/user-attachments/assets/48dea204-5971-4cac-9acd-0e1e9fbd78d6" />
</p>

<p align="center">
  <b>If you encounter any errors or issues, you can contact me via Discord or Tiktok or Youtube XDDD</b>
</p>

<p align="center">
  <a href="https://discord.gg/Ngc96hZs4w"><img src="https://img.shields.io/badge/Discord-%237289DA.svg?logo=discord&logoColor=white" height="50" /></a>
  <a href="https://tiktok.com/@pntmcvietnam"><img src="https://img.shields.io/badge/TikTok-%23000000.svg?logo=TikTok&logoColor=white" height="50" /></a>
  <a href="https://youtube.com/@PnTMCvn"><img src="https://img.shields.io/badge/YouTube-%23FF0000.svg?logo=YouTube&logoColor=white" height="50" /></a>
</p>


## Downloads


You can download Verity - Bedrock Edition (v4.0.0) from:
* [CurseForge](https://www.curseforge.com/minecraft-bedrock/addons/verity-bedrock-edition)
* [MCPEDL](https://mcpedl.com/verity-bedrock-edition/)


## Settings in Minecraft





## Installation

> [!NOTE]
> Voicechat and AI are not officially supported features on Minecraft Bedrock natively!

<br>

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
> After you run this command, open **Minecraft**, install the add-on, enable **Beta APIs**, and turn on **Cheats** <br> - Once you have entered the world, run the command `/connect 127.0.0.1:3000` (When you exit and re-enter the world, make sure to run this command again)

<br>

---

<br>

### Windows

| **Using File Explorer & CMD** |
|:-|
| 1. Extract the `verity-windows-setup.zip` file you downloaded |
| 2. Then, copy the newly extracted folder to this path: `C:\Users\<your-name>\verity-windows-setup` |


<br>

| **SETUP on Windows** |
|:-|
| 1. Download Python 3.10+ : [Here](https://www.python.org/downloads/) |
| 2. Open CMD and test `python --version` , You must see a version number, not "not found" |
| 3. Click on `verity-windows-setup` and open the `.env` file then get the API keys/FishAudio Models ID to insert!! <br> - Groq API Key: [Create your API keys here](https://console.groq.com/keys) <br><br> - FishAudio API Key: [Create your API keys here](https://fish.audio/app/api-keys/) <br><br> - FishAudio Models ID: [Find your favourite Model Id here](https://fish.audio/app/discovery/?q=verity) |
| 4. Open CMD and run : <br> **```cd %USERPROFILE%\verity-windows-setup```** <br> **```python -m pip install -r requirements.txt```** <br> **```python -m pip install --force-reinstall websockets==10.4```** |
| 5. Right-click **`fix_minecraft_loopback.bat`** (inside verity-windows-setup folder) -> Run as administrator <br> If it still fails, also right-click **`fix_firewall_and_loopback.bat`** -> Run as administrator |
| 6. Go to Settings -> Privacy & security -> Microphone then Allow desktop apps to use the mic. |
| 7. Double-click `start_minecraft_stt.bat` inside the extracted folder (`verity-windows-setup`) <br><br> *If any errors occur, follow the repair instructions displayed when the `start_minecraft_stt.bat` file runs* |

<br>

> [!NOTE]
> After you run `start_minecraft_stt.bat`, open **Minecraft**, install the add-on, enable **Beta APIs**, and turn on **Cheats** <br> - Once you have entered the world, run the command `/connect 127.0.0.1:3000` (When you exit and re-enter the world, make sure to run this command again)
