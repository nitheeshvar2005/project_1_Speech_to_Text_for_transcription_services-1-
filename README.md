# project_1_Speech_to_Text_for_transcription_services-1-
📌 Features
🎧 Supports WAV audio input (MP3 can be converted manually)

🧠 Uses Google Web Speech API for transcription

✂️ Splits long audio into chunks based on silence

💬 Combines individual transcriptions into a final transcript

🗃️ Saves output to a text file (output.txt)

🛠️ Tech Stack
Python 3.x

SpeechRecognition

pydub

wave, contextlib – for audio duration

os, shutil – for file management

📁 File Structure
css
Copy
Edit
project/
│
├── project_1_Speech_to_Text_for_transcription_services.ipynb
├── audio.wav                  # Your input audio file
├── output.txt                 # Final transcription output
└── audio-chunks/             # Directory created to store audio chunks
▶️ How It Works
Load Audio File

Audio is loaded using pydub.AudioSegment.

Silence-Based Chunking

The audio is split into smaller segments where silence is detected.

Parameters like min_silence_len and silence_thresh can be adjusted.

Transcription

Each chunk is saved as a temporary file.

Chunks are passed to the Google Web Speech API for transcription.

Results are written to a text file and displayed.

Output

Final transcription is saved in output.txt.

💻 Getting Started
Install dependencies:

bash
Copy
Edit
pip install SpeechRecognition pydub
Install ffmpeg (required for pydub):

bash
Copy
Edit
# macOS
brew install ffmpeg

# Ubuntu/Debian
sudo apt install ffmpeg
Run the notebook in Jupyter or VS Code.

⚠️ Notes
Only WAV input is supported directly. Convert MP3 using pydub or external tools.

Requires an internet connection to use Google’s Speech API.

Better results with clear speech and minimal background noise.

📜 License
This project is licensed under the MIT License.
