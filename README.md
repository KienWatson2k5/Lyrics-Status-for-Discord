[README.md](https://github.com/user-attachments/files/24064837/README.md)
# 🎧 Lyrics Status for Discord

**Display Lyrics and Now Playing Status on your Discord Profile!**

Lyrics Status for Discord is a cross-platform application that allows you to synchronise the song you are listening to from music services like **Spotify** and **YouTube Music** with your Discord profile. Notably, it enables you to display **synced lyrics** in real-time on your Discord custom status.


## ✨ Main Features

* **Multi-Source Support:** Connects with **Spotify** and **YouTube Music** (via external and internal APIs).
* **Custom Status:** Displays the song name, artist, real-time duration, lyrics, and allows customisation with a Custom Emoji on Lyrics Status for Discord.
* **Lyrics Editor:** An intuitive interface for you to create or edit synchronous lyric files (LRC) for your songs.
* **Music Analytics:** Tracks the songs you have listened to and creates personalised charts (`Top Charts`) over different time ranges (e.g., Last 6 Months).
* **Last.fm Integration (Optional):** Option to Scrobble music to Last.fm to track your listening habits.
* **Dark Mode Dashboard UI:** Modern, minimalist, and eye-friendly design.

## 🧠 Hidden Feature: Smart Idle Logic

The system is programmed to automatically manage your Discord status when you stop listening to music, helping your account appear less *spammy* and tidier on Discord. More specifically:
The system uses an `idleStage` variable to manage different phases when the user stops listening to music, preventing status spam or keeping an old status active for too long.

* **Pause Phase (0 - 15 seconds):** When you pause the music, the status changes to **"Currently Stopping..."** to let your friends know you are taking a break.
* **"Recently Played" Phase (15 seconds - 5 minutes):** If you do not resume playback, the status will switch to **"Last played: [Song Name]"** (if enabled in Settings).
* **Idle Phase (5 minutes - 10 minutes):** The system transitions to **Idle Mode** to signal that you are inactive.
* **Automatic Cleanup (> 10 minutes):** If no music has played for more than 10 minutes, the application will **completely clear the status** from your Discord profile to avoid displaying old information or permanently keeping the Custom Status created by Lyrics Status for Discord.
* **System Clears Discord Custom Status on Exit:** If you completely shut down the Lyrics Status for Discord system, it will completely clear the status from your Discord, and only after 1 second, the system will fully shut down.

## 🚀 Installation & Usage Guide

### Requirements

* Operating System: Windows.
* Discord account.
* Spotify account (for Spotify music source).
* YT Music Desktop.

### 1. Installation

1.  **Download:** Download the latest release from the Release tab.
2.  **Launch:** Run the **`Lyrics Status.exe`** file.

### 2. Configuration Setup (Settings)

Go to the **Settings** tab and enter the following information:

* **Discord Authentication:** Log in to your Discord account, and the system will automatically recognise it.
* **Spotify/Last.fm:** Enter the **Client ID** and **Client Secret** (for Spotify) and the **API Key** (for Last.fm). **(Note: You will need to register a Last.fm/Spotify application to obtain these keys.)**.
* **YT Music Server API (External):** If you use the YT Music Desktop source, follow these steps:
    1.  Download YT Music Desktop and extract the .rar file via this link: `https://shorturl.at/iqNjN`.
    2.  After extraction, run Youtube Music.exe.
    3.  When you open Youtube Music, look on the left side corner for the "plugins" section, select it, and find "API Server [Beta]".
    4.  Select both "Hostname" and "Port" and create your own private local server.
    5.  Once your private local server is created, switch to the "Authorisation strategy" section and select "No authorisation".
    6.  Try playing any song on YT Music Desktop.
    7.  Next, open the browser you are using (Chrome, FireFox, Opera, Microsoft Edge, etc.).
    8.  Open the link according to the following template: `http://[Hostname]:[Port]/api/v1/song`.
    9.  Ensure the local server API (e.g., `http://127.0.0.1:12345/api/v1/song`) is running. The page should display song information in JSON format like this:

{"title":"Never Gonna Give You Up","artist":"Rich Asley","views":1720815434,"uploadDate":"2009-10-25T08:13:15-08:00","imageSrc":"https://xyz.jpg","isPaused":true,"songDuration":[number],"elapsedSeconds":[number],"url":"https://www.youtube.com/watch?v=dQw4w9WgXcQ",...}

  10. Then paste that link into the "YT Music Server API (External)" input box.
  *Note: If you cannot connect, restart YT Music Desktop and re-check the Hostname/Port.*
### 3. Activity Monitoring

1.  Go to the **System Monitor** tab.
2.  Select the **Default Source** as **Spotify** or **YT Music**.
3.  Start playing music on the selected service.
4.  The **Live Activity** status will update on your Dashboard and Discord.
5.  You can press the **Full Screen** button to switch to Media Player mode, complete with a "karaoke" style running text effect for the synced lyrics.

## 🖋️ Lyrics Editor

Use the **Lyrics Editor** tab to manage local lyric files.

1.  Select the song from the list on the left.
2.  Paste the synchronous lyric content (using the time format `[mm:ss.xx]`) into the editing frame.
3.  The system will automatically save and convert it to the `.json` format for use.

## ⚡ Performance & Optimisation

* **VSync & High Refresh Rate Monitors:** By default, the application enables **Vertical Sync (VSync)**. This means the application's frame rate (FPS) will match your monitor's refresh rate.
* **Resource Usage:** If you use a high refresh rate monitor (e.g., 144Hz, 240Hz, or higher), the application will render at higher frames per second. Consequently, you may notice increased **CPU and GPU usage**. This is expected behavior to ensure smooth animations for lyrics and visualisers.

## ⚠️ Disclaimer & Warning

The use of this software involves automatically updating the **Custom Status** on a personal Discord user account.

1.  **Discord Terms of Service (TOS):** According to Discord's rules, automating user accounts ("Self-botting") may violate the terms of service. Although this application attempts to operate within safe limits by using reasonable delays, the risk always exists.
2.  **Responsibility:** The developer is not responsible for any issues that occur with your Discord account (including temporary or permanent bans) due to the use of this software.

**🔴 USE AT YOUR OWN RISK.**

## 🆘 Support and Bug Reports

If you encounter any problems, please open an Issue on the GitHub repository, or you can send an email to me: baokien268gamingofcfparkourvn@gmail.com.

---

**Developed by Barry Watson (me)**
