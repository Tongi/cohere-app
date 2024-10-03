# Soundback: Automated Text Capture and Response Application

Soundback is an automated GUI tool designed to streamline question-answering processes, particularly useful for studying, IT support, or any scenario requiring quick and intelligent responses to multiple-choice questions. It monitors the clipboard for new text, allows for submission of questions to a chatbot for evaluation, and provides immediate feedback.

## Features
- **Clipboard Monitoring**: Automatically detects and captures new text copied to the clipboard, using it to populate question and answer fields.
- **Cohere Chatbot Integration**: Utilizes Cohere's API to provide expert answers to questions based on provided options.
- **Text-to-Speech Feedback**: Speaks the current status and responses, enhancing usability.
- **Submit and Reset Actions**: Configurable automatic submission after 20 seconds and auto-reset after 30 seconds, with buttons and keyboard shortcuts for manual control.
- **System Tray Icon**: Minimizes to the system tray to avoid distractions, with restore and quit options.
- **Non-Intrusive UI**: GUI elements remain hidden unless interacted with, maintaining a minimal interface.
- **Window Movement**: Customizable window position, always on top for convenience.

## Requirements
- Python 3.12+
- PyQt5
- Cohere API (`cohere` Python package)
- pyttsx3 (for text-to-speech)

## Installation
1. **Clone the Repository**
   ```
   git clone https://github.com/yourusername/soundback.git
   ```
2. **Navigate to the Project Directory**
   ```
   cd soundback
   ```
3. **Install Dependencies**
   ```
   pip install -r requirements.txt
   ```
4. **Set Up Your Cohere API Key**
   - Open `soundback.py` and replace `"your_api_key_here"` with your Cohere API key:
     ```python
     client = cohere.Client("your_api_key_here")
     ```

## Usage
Run the application by executing the following command:
```
python soundback.py
```
- **Clipboard Text Capture**: Simply copy any text, and Soundback will automatically populate the appropriate input fields.
- **Submit**: Press the **Submit** button or use the **V** key to send the question and options to the chatbot.
- **Reset**: Use the **Reset** button or press the **Z** key to clear all fields and start over.

### Keyboard Shortcuts
- **V**: Submit the current question and options.
- **Z**: Reset all fields.

## Example Usage
1. Copy your question to the clipboard.
2. Copy each answer option sequentially.
3. Press **Submit** or wait for auto-submit after 20 seconds.
4. The chatbot's answer will be displayed and read out.
5. Press **Reset** or wait for auto-reset after 30 seconds to start a new session.

## License
This project is licensed under the [MIT License](LICENSE).

## Contributing
Contributions are welcome! Please open issues and pull requests if you have suggestions for new features or improvements.

To contribute:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add your feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.

## Future Enhancements
- **Conversation History**: Implement persistent conversation history for enhanced context.
- **Configurable Timers**: Add an interface to allow users to set custom auto-submit and auto-reset times.
- **Dark Mode UI**: Provide a dark mode
