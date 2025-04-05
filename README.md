# Wiztron AI Assistant

An intelligent AI companion that combines facial recognition, natural language processing, and a 3D interface to create a personalized assistant experience.

## Features

- **Face Recognition**: Identifies users and remembers their preferences
- **Speech Recognition**: Converts voice to text for natural interaction
- **Memory System**: Stores and recalls information about users
- **3D Interface**: Provides visual feedback through an animated character
- **Calendar Integration**: Connects with Google Calendar for scheduling
- **Weather Information**: Retrieves current weather data
- **YouTube Music**: Plays music from YouTube based on user requests

## Requirements

- Python 3.9+
- Webcam
- Microphone
- MongoDB Atlas account
- Various API keys (included in .env file)

## Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/wiztron-ai.git
cd wiztron-ai
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Create a `.env` file with your API keys (or use the provided one):
```
MONGO_URI=your_mongodb_uri
TOGETHER_API_KEY=your_together_api_key
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
WEATHER_API_KEY=your_weather_api_key
YOUTUBE_API_KEY=your_youtube_api_key
```

4. Download the face-api.js models (already included in this package):
```bash
cd public
node download_models.js
```

## Usage

1. Run the main application:
```bash
python 2calendar.py
```

2. The application will:
   - Start the web server for the 3D interface
   - Open a browser window with the Spline character
   - Activate your camera for face recognition
   - Listen for voice commands

3. Wake Word:
   - The default wake word is "wake up"
   - The assistant will enter sleep mode after 30 seconds of inactivity
   - Say "wake up" to reactivate it

## System Architecture

- **NeuroMemoryCore**: Neural network for user memory management
- **SplineManager**: Handles the 3D character animation and communication
- **AICompanion**: Main class integrating all components

## Troubleshooting

- **Camera Issues**: Ensure your webcam is connected and permissions are granted
- **Audio Issues**: Check microphone settings and permissions
- **Web Interface**: If the browser doesn't open automatically, navigate to http://localhost:8000/spline_connector.html

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Face Recognition library by Adam Geitgey
- Sentence Transformers by UKPLab
- Together API for LLM access
- Google API services 
