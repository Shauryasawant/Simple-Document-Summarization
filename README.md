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

Frontend: Gradio (As this Requires less efforts for making UI.if we are in time bound or want to focus more on implementation)

LLM: Mistral (via mistralai)

PDF Parsing: PyPDF2

Platform: Google Colab 

## 🛠 Setup Instruction 
For Downloading Gradio , Mistral_Api , PyPDF

```!pip install gradio mistralai PyPDF2```

## Usage Instructions

Run the script in a Google Colab cell.

Upload a file (.pdf or .txt) or paste text manually.

Select a summary style:

Brief

Detailed

Bullet Points

Click the Summarize button.

View the generated summary in the output panel.

A public link will be provided via Gradio (share=True) for easy sharing.

# NOTE
API Key have a Expiry of 15th October 2025. So if run this code after this date it might not work as expected
