# Screen Recorder

A simple, browser-based screen recording application built with HTML, CSS, and vanilla JavaScript. No installation required - just open the HTML file in your browser and start recording!

## Features

- **Multiple Recording Sources**: Choose between full screen, application window, or browser tab
- **Audio Recording**: Optional audio capture alongside screen video
- **Dark/Light Mode**: Toggle between themes for comfortable viewing
- **Live Preview**: Watch your recording in real-time
- **Easy Download**: Save recordings as WebM files instantly
- **No Dependencies**: Pure HTML/CSS/JavaScript - no build tools or libraries needed

## Usage

1. Open `index.html` in a modern web browser (Chrome, Firefox, Edge, etc.)
2. Select your recording source from the dropdown:
   - **Full Screen**: Record your entire monitor
   - **Application Window**: Record a specific application window
   - **Browser Tab**: Record a specific browser tab
3. Optionally enable audio recording by checking the "Record Audio" box
4. Click **Start Recording** to begin capturing your screen
5. Click **Stop Recording** when finished
6. Preview your recording in the video player
7. Click **Download** to save the recording as a `.webm` file

## Browser Compatibility

This application uses the [MediaDevices API](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices) and requires a modern browser:

- ✅ Chrome 70+
- ✅ Firefox 66+
- ✅ Edge 79+
- ✅ Opera 57+
- ⚠️ Safari: Limited support (check version compatibility)

## File Format

Recordings are saved in **WebM** format, which is:
- Widely supported by modern browsers
- Compatible with most video players (VLC, etc.)
- Easily convertible to other formats if needed

## Privacy & Security

- All recording happens locally in your browser
- No data is sent to external servers
- Screen sharing permissions are handled by your browser's built-in security

## Customization

You can customize the appearance by modifying the CSS in the `<style>` section of `index.html`. Key styles include:

- `body`: Background color and layout
- `.dark-mode`: Dark theme colors
- `button`: Button styling and colors
- `#preview`: Video player dimensions

## License

See the [LICENSE](LICENSE) file for details.
