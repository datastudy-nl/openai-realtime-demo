# Real-Time OpenAI GPT-4 Voice Assistant Demo
This repository contains a Python demo that showcases real-time interaction with OpenAI's GPT-4 model using audio streams. The application captures microphone input, sends it to the OpenAI API, and plays back the assistant's audio response in real-time.

## Features
 - Real-Time Communication: Interact with GPT-4 in real-time using your microphone and speaker.
 - Audio Streaming: Sends live audio to the OpenAI API and plays back the assistant's response.
 - Threaded Architecture: Utilizes multithreading for handling audio input/output and WebSocket communication simultaneously.
 - Customizable Session: Configure the assistant's behavior, voice, and other session parameters.
## Prerequisites
 - Python 3.7 or higher
 - OpenAI API Key: You must have an API key from OpenAI with access to the GPT-4 real-time API.
 - Supported Platforms: This demo is designed for Unix-like systems. Windows support may require additional configuration.
## Installation
1. Clone the Repository

```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
```
2. Create a Virtual Environment (Optional but Recommended)
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```
3. Install Dependencies
```bash
pip install -r requirements.txt
```
4. Set Up Environment Variables

Create a .env file in the root directory and add your OpenAI API key:

```env
OPENAI_API_KEY=your-openai-api-key
```
## Usage
1. Run the Demo

```bash
python demo.py
```
2.  Interaction

 - Speak into your microphone.
 - The assistant will process your speech and respond in real-time.
 - Press Ctrl+C to terminate the demo.

## Configuration
You can customize the assistant's behavior by modifying the SESSION_DATA dictionary in demo.py:

 - Instructions: Set the assistant's personality and guidelines.
 - Voice: Choose the assistant's voice (e.g., "voice": "Sol").
 - Temperature: Adjust the creativity level (0.0 to 1.0).
Example:

```python
SESSION_DATA = {
    "type": "session.update",
    "session": {
        "instructions": "You are a helpful assistant.",
        "temperature": 0.7,
        "voice": "Sol",
        "modalities": ["audio", "text"],
        # ... other configurations
    }
}
```
## Project Structure
 - demo.py: The main script that runs the demo.
 - requirements.txt: Python dependencies.
 - .env: Environment variables (not included; you need to create this file).

## Dependencies
The demo relies on the following Python packages:

 - pyaudio: For capturing and playing audio.
 - websocket-client: For WebSocket communication with the OpenAI API.
 - python-dotenv: For loading environment variables from a .env file.
 - logging: For logging events and errors.

Install all dependencies using:

```bash
pip install -r requirements.txt
```
_Note: pyaudio may require additional system dependencies. For example, on Ubuntu:_

```bash
sudo apt-get install portaudio19-dev python3-pyaudio
```

## Troubleshooting
 - Microphone or Speaker Issues: Ensure your microphone and speakers are properly connected and configured.
 - API Errors: Verify that your OpenAI API key is correct and has access to the GPT-4 real-time API.
 - WebSocket Errors: Check your internet connection and firewall settings.

## Contributing
Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch:

```bash
git checkout -b feature/your-feature-name
```
3. Make your changes and commit them:

```bash
git commit -am 'Add some feature'
```
4. Push to the branch:

```bash
git push origin feature/your-feature-name
```
5. Submit a pull request.

## License
This project is licensed under the Apache License 2.0. See the LICENSE file for details.

Attribution Requirement: If you use any part of this code, please provide appropriate credit by mentioning the original author.

_Disclaimer: This is a demo application intended for educational purposes. Use it responsibly and ensure compliance with OpenAI's usage policies._
