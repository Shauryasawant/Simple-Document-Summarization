# Simple-Document-Summarization

# 📄 Document Summarizer – Documentation Overview

This is a document summarization tool built using Gradio for the front-end and the Mistral AI API as the backend model. It allows users to upload documents (PDF or TXT) or paste text, and choose between different summary styles. The app is designed to run efficiently in Google Colab with secure API key management.

# Core Functional Requirements & How They're Handled
| Feature                | Implementation                                                
| ---------------------- | ------------------------------------------------------------- 
| **Text Input**         | Upload `.pdf` or `.txt` files, or paste text manually         
| **LLM Integration**    | Uses **Mistral AI** via the `mistralai` Python SDK            
| **Summary Styles**     | Choose from **Brief**, **Detailed**, or **Bullet Points**     
| **API Error Handling** | Catches errors and provides user-friendly messages            
| **Input Validation**   | Checks for missing input and limits text to 50,000 characters 
| **Web Interface**      | Built with **Gradio** (runs in Colab with public share link)  

# Tech Stack

Frontend: Gradio (As this Requires less efforts for making UI. As if we are in time bound or want to focus more on implementation)

LLM: Mistral (via mistralai)

PDF Parsing: PyPDF2

Platform: Google Colab 

## 🛠 Setup Instruction 
For Downloading Gradio , Mistral_Api , PyPDF

```!pip install gradio mistralai PyPDF2```

## Usage Instructions

1. Run the script in a Google Colab cell.

2. Upload a file (.pdf or .txt) or paste text manually.

3. Select a summary style:

       Brief

       Detailed

       Bullet Points

4. Click the Summarize button.

5. View the generated summary in the output panel.

A public link will be provided via Gradio (share=True) for easy sharing.

## 🧠 Approach & Design Decisions

### 🔹 Multi-Input Flexibility  
The app supports both **file upload** and **text input**, giving users flexibility based on their needs. It detects and processes the input method dynamically.

### 🔹 API Integration  
Used the **Mistral AI API** (`mistral-small-latest` model) for summarization. It's initialized with a secure API key stored in **Colab secrets** (`userdata`), avoiding hardcoded keys.

### 🔹 Prompt Engineering for Styles  
Custom prompt templates are used for three summary styles:
- **Brief**: Short 2–3 sentence summary  
- **Detailed**: Full descriptive summary  
- **Bullet Points**: List of main points  

This allows users to choose how concise or informative they want the output.

### 🔹 Error Handling  
The app includes:
- API key validation  
- Input validation (empty input, file errors)  
- Length limits (max **50,000 characters**)  

This ensures the app fails gracefully and guides the user when needed.

### 🔹 Gradio UI  
Gradio was chosen for its **simplicity** and **Colab compatibility**. It enables fast prototyping and a shareable public interface with minimal code.


## 📎 Be Aware

- Only one input type should be used at a time (**file OR text**)  
- File types supported: `.pdf`, `.txt`  
- Text input limit: **50,000 characters**  
- Requires valid **Mistral API access**


# NOTE
API Key have a Expiry of 15th October 2025. So if run this code after this date it might not work as expected
