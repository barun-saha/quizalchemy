# QuizAlchemy: Transmute text into knowledge 💎

QuizAlchemy is a quiz generation application that leverages Google's [Agent Development Kit (ADK)](https://google.github.io/adk-docs/) and Streamlit to create quizzes from any file or text. It allows users to input text or upload files, which are then transformed into a structured quiz format with multiple-choice questions of varying difficulty.


## Architecture
![QuizAlchemy Architecture](https://github.com/barun-saha/quizalchemy/blob/main/assets/quizalchemy_arch.png?raw=true)


## Features

QuizAlchemy can:
- Extract content from web URLs or uploaded files (PDF, DOCX, HTML)
- Generate a question bank using Google Gemini models via ADK
- Store questions in an SQLite database
- Create quizzes with a customizable mix of question difficulties (easy, medium, hard)

It uses three ADK agents:
- `DataIngestionAgent`: For extracting content from web pages or files.
- `QuizMasterAgent`: For generating quizzes based on the extracted content.
- `CoordinationAgent`: For coordinating the workflow and managing the question generation process.


## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/barun-saha/quizalchemy
   cd quizalchemy
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up environment variables:
   - Create a `.env` file and set the `GEMINI_API_KEY` key to use Google's Gemini. To use any other model via LiteLLM, change `MODEL_GEMINI` in the code and set the appropriate environment variable.


## Usage

1. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```
2. Open the provided local URL in your browser.
3. Input a web URL or upload a supported file.
4. Generate a quiz and test your knowledge!


## Credits

- Built with [Streamlit](https://streamlit.io/), [Google ADK](https://google.github.io/adk-docs/), and [Gemini](https://ai.google.dev/gemini-api/docs)
- Uses [MarkItDown](https://github.com/microsoft/markitdown/) for file content extraction
- Supported by GitHub Copilot and Gemini for development assistance


## License

See [LICENSE](LICENSE) for details.
