# 🎵 TrackSnatch

**TrackSnatch** analyzes the full audio of a YouTube video, identifies the songs inside, and saves them to a text file. It then automatically creates a Spotify playlist with the detected songs, similar to Chaptersnatch but focused on music.

## 🚀 Features

* Downloads audio from any YouTube video
* Splits the audio into fragments to detect multiple songs
* Identifies songs using the AudD API
* Generates a `songs.txt` file with the detected songs
* Creates a Spotify playlist with the results

## ⚙️ Requirements

* Python 3.8+
* AudD account with an API key
* Spotify Developer account for Client ID and Client Secret

## 🛠 Installation

```bash
git clone https://github.com/youruser/TrackSnatch.git
cd TrackSnatch
pip install -r requirements.txt
```

## 📦 Main Dependencies

* pytube
* pydub
* requests
* spotipy

## 🔑 Configuration

1. In `tracksnatch.py`, replace:

   * `AUDD_API_TOKEN` with your AudD token
   * `SPOTIFY_CLIENT_ID`, `SPOTIFY_CLIENT_SECRET`, and `SPOTIFY_REDIRECT_URI` with your Spotify app credentials

2. Make sure the Spotify scope includes `playlist-modify-public`.

## 🖥️ Usage

```bash
python tracksnatch.py
```

Paste the YouTube video URL when prompted, and wait for analysis to complete.

At the end:

* the list of detected songs will be saved in `songs.txt`
* a public Spotify playlist called *YouTube Video Songs* will be created in your account

## 📝 Notes

* Song recognition depends on audio quality and AudD’s database.
* AudD has request limits depending on their free/paid plans.
* Not all songs may be available on Spotify.

## 🤝 Contributions

Pull requests are welcome! Feel free to improve the song detection or add compatibility with other music recognition APIs.

---

**Made with ❤️ by [foliveross](https://github.com/foliveross)**
