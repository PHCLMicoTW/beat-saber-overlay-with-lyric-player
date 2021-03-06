# `WIP`

# (Unnamed) Beat Saber Overlay - With lyric displayer

![Screenshot](https://i.imgur.com/4mR98Ei.png)

A web-based overlay for Beat Saber

![preview](https://i.imgur.com/fOg4TUp.png)

## Installation (OBS)

1. Download and install the [BeatSaberHTTPStatus plugin](https://github.com/opl-/beatsaber-http-status/releases)
2. Create a Browser source

![image](https://i.imgur.com/WyTjdtd.png)

3. Set the URL as `Local file` and chose `index.html` and the size equal to your canvas size (1280x720, etc.)

![image](https://imgur.com/KxowYrw.png)

4. (Optional) For 1080p canvases, add the `scale` modifier (`<link rel="stylesheet" href="./modifiers/scale.css">`) in the `index.html` ~~(ex. `http://overlay.reselim.io/?modifiers=scale`) to scale the overlay by 1.5x~~

## Options

~~Options are added to the URL query as such:~~

Options are adjust the HTML as such:

add or remove
```
<link rel="stylesheet" href="./modifiers/top.css">
```
in `index.html`

### `modifiers`

Multiple modifiers can be seperated with commas.

- `top`
	* Moves the overlay to the top and reverses the layout vertically
- `rtl`
	* Moves the overlay to the right and uses right-to-left text
- `scale`
	* Scales the overlay by 1.5x, for use on 1080p canvases
- `test`
	* Makes the background black, for testing purposes
	
### `ip` and `port`

Adjust in `manager.js`

# `Dynamic lyric Player`

Auto find lyric of the song if possible, using API from music.163.com (网易云音乐)

`!!!**important**!!!` ->  It only search the song name+Author and use the first song return of API as the result, some time it may be wrong song, use it carefully!!

Somehow it only work for OBS use as local file now, and you must download this project to use it as local file to make it work.

### `LyricGlobalDelay`

If you have a low end pc like me and every time play a song your lyric aren't wait for song start, use this option in `ui.js` to adjust wait time for each song.

Usage: `LyricGlobalDelay = {delay time in second}`
