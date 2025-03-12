# Real-time Voice Translator

![Real-time Voice Translator Logo](icon-192.png)

A progressive web application that provides real-time speech translation between Japanese and English. This application utilizes modern web technologies to deliver a seamless translation experience directly in your browser.

## Features

- **Real-time Voice Translation**: Instantly translate spoken Japanese to English or English to Japanese
- **Streaming Responses**: See translations appear as you speak with minimal delay
- **Language Selection**: Explicitly choose your input language for improved accuracy
- **Mobile-Friendly Design**: Optimized for both desktop and mobile devices
- **Offline Capability**: Install as a PWA for quick access even with limited connectivity
- **Clean User Interface**: Simple, intuitive controls with visual feedback

## Demo

[View Live Demo](#) *(Add your deployment link here)*

![App Screenshot](screenshot.png)

## Technologies Used

- **Web Speech API**: Browser-native speech recognition for real-time audio processing
- **OpenAI API**: Leverages the o3-mini model for high-quality translations
- **Gladia API**: Used as a fallback for speech recognition when Web Speech API is unavailable
- **Fetch Streaming**: Implements streaming responses for real-time translation output
- **Progressive Web App**: Installable on mobile and desktop devices

## Getting Started

### Prerequisites

- An OpenAI API key ([Get one here](https://platform.openai.com/api-keys))
- A Gladia API key ([Get one here](https://app.gladia.io/))

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/real-time-voice-translator.git
   cd real-time-voice-translator
   ```

2. Set up a local development server:
   
   Using Python:
   ```bash
   python -m http.server 8000
   ```
   
   Or using Node.js:
   ```bash
   npx serve
   ```

3. Open your browser and navigate to `http://localhost:8000` (or the port specified by your server)

4. Enter your API keys when prompted on first use

### Deployment

This application can be deployed to any static hosting service:

- GitHub Pages
- Netlify
- Vercel
- Firebase Hosting
- AWS S3

Remember to ensure your hosting uses HTTPS, as this is required for accessing the microphone.

## Usage

1. Click the "開始" button to start recording in Japanese
2. Click the "Start" button to start recording in English
3. Speak clearly into your microphone
4. See your speech transcribed in real-time in the "Original" box
5. Watch as the translation appears in the "Translation" box
6. Click the "Stop" button when you're finished speaking

## Key Components

- **Language Selection**: Choose between Japanese and English input
- **Real-time Transcription**: See what the system is hearing as you speak
- **Streaming Translation**: Translations appear word by word as they're generated
- **Visual Feedback**: Status indicators show when the system is listening or translating

## How It Works

1. **Speech Recognition**: The app uses Web Speech API (with Gladia as fallback) to convert speech to text
2. **Language Detection**: Explicitly selected by the user via language buttons 
3. **Translation Processing**: Text is sent to OpenAI's API with appropriate context
4. **Streaming Response**: Translation results are streamed back word-by-word
5. **UI Updates**: Both original text and translation are displayed in real-time

## Browser Compatibility

- Chrome (desktop & mobile): Full support
- Edge: Full support
- Safari (iOS & macOS): Full support
- Firefox: Limited support (uses Gladia API fallback)

## Known Limitations

- Requires an internet connection for API access
- Translation quality depends on clear speech and good microphone input
- Limited to Japanese-English language pair
- API usage incurs costs based on usage volume

## Customization

To customize the application:

1. **Appearance**: Modify the CSS styles in the `<style>` section
2. **Behavior**: Adjust the JavaScript parameters like debounce timing
3. **Languages**: The core logic can be extended to support additional languages

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- OpenAI for providing the translation API
- Gladia for the speech recognition fallback API
- Web Speech API for enabling browser-based speech recognition

---

*Note: This application uses API services that may have usage costs. Please check the pricing details for OpenAI and Gladia APIs before extensive use.*
