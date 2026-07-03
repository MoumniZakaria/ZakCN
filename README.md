# 🎬 VidKing Player Generator

A simple standalone HTML page for generating and launching **VidKing** embedded movie and TV players.

This tool lets you quickly build a VidKing embed URL by entering a TMDB ID and selecting the desired player options. Once generated, the player is loaded directly inside the page using an iframe.

No build tools, frameworks, or installation are required.

---

## ✨ Features

* 🎬 Play movies using a TMDB Movie ID
* 📺 Play TV shows using a TMDB TV ID
* 🎞 Select season and episode for TV series
* 🎨 Customize the player accent color
* ▶️ Enable or disable autoplay
* ⏭ Enable the "Next Episode" button
* 📋 Enable the episode selector
* ⏱ Start playback from a specific timestamp
* 🔗 Automatically generate the VidKing embed URL
* 📺 Embedded player preview
* 📡 Listen for player events (play, pause, progress, ended, seeked)

---

## 📁 Project Structure

```text
.
├── index.html
└── README.md
```

---

## 🚀 Usage

1. Open `index.html` in your browser.
2. Select the media type:

   * Movie
   * TV Show
3. Enter the TMDB ID.
4. If playing a TV show, specify the season and episode.
5. Configure any optional settings:

   * Player color
   * Autoplay
   * Next Episode
   * Episode Selector
   * Start time
6. Click **Play**.
7. The generated embed URL will be displayed, and the player will load automatically.

---

## Example

Movie:

```text
TMDB ID: 1078605
```

Generates:

```text
https://www.vidking.net/embed/movie/1078605
```

TV Show:

```text
TMDB ID: 119051
Season: 1
Episode: 8
```

Generates:

```text
https://www.vidking.net/embed/tv/119051/1/8?color=004741&nextEpisode=true&episodeSelector=true
```

---

## Player Events

The page listens for events sent from the embedded player using `window.postMessage()`.

Supported events include:

* `play`
* `pause`
* `timeupdate`
* `seeked`
* `ended`

The received event data is displayed on the page and logged to the browser console.

---

## Technologies

* HTML5
* CSS3
* Vanilla JavaScript
* VidKing Embed Player

---

## Notes

* A valid TMDB ID is required.
* TV shows require both a season and an episode number.
* This project does not host or stream any media. It simply generates and embeds the official VidKing player.

---

## License

This project is provided as a simple utility for testing and generating VidKing embed URLs. Please ensure you comply with the terms and conditions of any third-party services you use.
