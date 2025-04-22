# Note Generator & Q/A Assistant

A Flask web application that takes document uploads (.docx, .pdf, .txt) and uses the Google Gemini AI model to either generate structured notes or answer questions paragraph-by-paragraph based on the document content.

## Features

*   **Generate Notes:** Creates structured, summarized notes from the content of one or more uploaded documents.
*   **Answer Questions:** For an uploaded `.docx` file, it provides a general knowledge answer/response for each paragraph, integrating the answers back into the document structure.
*   **File Support:** Accepts `.docx`, `.pdf`, and plain `.txt` files as input.
*   **Output:** Generates downloadable `.docx` files containing the notes or the Q&A results.

## Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Awesomepieman69/notegenerator.git
    cd notegenerator
    ```

2.  **Create a virtual environment (optional but recommended):**
    *   On macOS/Linux:
        ```bash
        python3 -m venv venv
        source venv/bin/activate
        ```
    *   On Windows:
        ```bash
        python -m venv venv
        .\venv\Scripts\activate
        ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Create environment file:**
    Create a file named `.env` in the root directory (`notegenerator/`).

5.  **Add API Key:**
    Open the `.env` file and add your Google AI API key:
    ```
    GOOGLE_API_KEY='YOUR_GOOGLE_AI_API_KEY'
    ```
    Replace `YOUR_GOOGLE_AI_API_KEY` with your actual key.

## Running the Application

1.  **Start the Flask server:**
    ```bash
    python app.py
    ```

2.  **Access the application:**
    Open your web browser and navigate to `http://127.0.0.1:5000` (or the address provided by Flask).

3.  **Use the interface:**
    *   Select either "Generate Notes" or "Answer Questions".
    *   Choose the file(s) to upload.
    *   Click "Process".
    *   A `.docx` file will be downloaded with the results.