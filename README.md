# AI Video Assistant

Summarize a YouTube video or local audio/video file, extract action items, decisions, and open questions, then chat with the transcript.

## Setup

1. Install Python and [FFmpeg](https://ffmpeg.org/) (make sure `ffmpeg` is available on your PATH).
2. Install dependencies:

   ```bash
   pip install -r Requirements.txt
   ```

3. Create a `.env` file in the project root:

   ```env
   MISTRAL_API_KEY=your_mistral_api_key
   SARVAM_API_KEY=your_sarvam_api_key
   WHISPER_MODEL=small
   SARVAM_STT_MODEL=saaras:v2.5
   ```

   `MISTRAL_API_KEY` is required for summaries, extraction, and transcript chat. `SARVAM_API_KEY` is only required for Hinglish transcription. `WHISPER_MODEL` and `SARVAM_STT_MODEL` are optional; the values shown are their defaults.

## Run

Launch the web app:

```bash
streamlit run app.py
```

Or use the command-line interface:

```bash
python main.py
```

Enter a YouTube URL or a local media file path, then select English or Hinglish. The first English run downloads the configured Whisper model.
