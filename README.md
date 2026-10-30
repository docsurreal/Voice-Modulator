# Voice Modulator

A browser-based text-to-speech playground with voice selection, adjustable speech settings, looping, a musical tone keyboard, and an animated waveform.

Built as a standalone HTML, CSS, and JavaScript project by **Doc Surreal**.

## Features

- **Text to speech:** Enter text and play it with your browser's available synthesized voices.
- **Voice selection:** Browse available voices grouped by language and region.
- **Speech controls:** Adjust speaking rate, pitch, and volume.
- **Additional modulation controls:** Adjust speech parameters through FM Mod, AM Mod, and a third modulation slider. These are parameter offsets, not true FM/AM audio processing.
- **Looping playback:** Repeat speech until stopped.
- **Musical notes:** Play notes C through C5 with Web Audio oscillators.
- **Animated waveform:** Interactive p5.js visualization responsive to speech events and playback state.
- **Responsive interface:** Dark-themed single-page layout.

## Getting started

No build step, package installation, or backend is required.

1. Clone the repository:

   ```bash
   git clone https://github.com/docsurreal/Voice-Modulator.git
   cd Voice-Modulator
   ```

2. Open `index.html` in a modern browser. You can also serve the directory with a simple static file server:

   ```bash
   python3 -m http.server 8000
   ```

   Then visit `http://localhost:8000`.

3. Enter text, select an available voice, change the controls, and select **Speak**. Use **Stop** to cancel playback or **Loop** to repeat it.

> **Note:** The page loads p5.js and Lucide icons from CDNs, so those assets require an internet connection unless you host them locally.

## Technologies

| Technology | Purpose |
| --- | --- |
| HTML, CSS, JavaScript | Interface and application logic |
| Web Speech API (`speechSynthesis`) | Browser-provided text-to-speech voices |
| Web Audio API | Musical tone generation |
| [p5.js](https://p5js.org/) | Interactive waveform animation |
| [Lucide](https://lucide.dev/) | Interface icons |

## Usage notes and limitations

- This project **synthesizes spoken text**. It does **not** currently process microphone input or modify a live person's voice.
- Available voices and speech quality depend on the browser and operating system.
- The FM/AM-labeled sliders modify speech rate/pitch and other parameters; they do not implement actual frequency or amplitude modulation of the speech audio stream.
- The waveform is an animated visualization driven by speech state and events, **not** a measured waveform of the audio output.
- Speech synthesis behavior, including voice availability and boundary events, may vary across browsers.
- The page is intended as a creative experiment; automated cross-browser testing has not been established.

## Project structure

```text
Voice-Modulator/
├── index.html      # Interface, styling, and application code
├── README.md       # Project documentation
└── LICENSE         # MIT License
```

## License

This project is licensed under the [MIT License](LICENSE). Copyright © 2026 Doc Surreal.

Third-party libraries and browser APIs remain subject to their respective terms and licenses.
