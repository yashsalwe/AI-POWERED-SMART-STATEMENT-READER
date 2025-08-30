# AI-POWERED-SMART-STATEMENT-READER
Smart Statement Reader - Project Setup &amp; Installation Guide

Project Description:
Smart Statement Reader is an AI/ML-powered tool designed to automatically extract and structure financial data from PDF documents. It leverages OCR, Camelot, pdfplumber, and Google Generative AI to: • Detect and classify various financial document formats. • Extract tabular and text-based data (with header recovery techniques). • Export the processed data into CSV or Excel formats. • Improve extraction accuracy over time through user feedback.

Prerequisites:
• Python 3.7 or above • Git (optional, for cloning the repository) • A valid Google API Key (required for Google Generative AI features)

Installation & Setup:
Clone the Repository:
Open your terminal and run: git clone https://github.com/<YOUR_GITHUB_USERNAME>/smart-statement-reader.git cd smart-statement-reader

Set Up a Virtual Environment:
It is recommended to use a virtual environment to manage dependencies.

For Linux/Mac: python3 -m venv venv source venv/bin/activate

For Windows: python -m venv venv venv\Scripts\activate

Install Dependencies:
Ensure you have a 'requirements.txt' file in the project directory that includes: streamlit camelot-py[cv] pdfplumber google-generativeai pandas Pillow

Then install the dependencies: pip install -r requirements.txt

Configure the Google API Key:
To use Google Generative AI features, obtain your API key by following these steps:

a. Visit the Google Cloud Console: https://console.cloud.google.com/ b. Create a new project or select an existing one. c. Enable the necessary API (e.g., Google Generative AI API). d. Navigate to "APIs & Services" > "Credentials". e. Click "Create Credentials" and choose "API Key". f. Copy your new API key.

Next, update the API key in the project:

Open the main project file (e.g., your_streamlit_app.py).
Locate the line: API_KEY = "AIzaSyALSG1EoSyS7NZfqGloBp-HsRxc5M2aXBc"
Replace the value with your actual API key: API_KEY = "YOUR_GOOGLE_API_KEY_HERE"
Alternatively, you can set an environment variable (e.g., GOOGLE_API_KEY) and modify the code to read from it.

Run the Application:
Use Streamlit to launch the app: streamlit run your_streamlit_app.py (Replace 'your_streamlit_app.py' with the actual name of your main Python file.)

Usage:
• Open the Streamlit web interface in your browser. • Upload PDF or image files containing financial data. • Review the extracted data, provide feedback if needed, and export results as CSV or Excel files.
