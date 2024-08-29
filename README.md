# RE.DFINED Y99 BIO

## Introduction

Y99 Bio Updater is a Python application designed to automatically update your Y99 bio with the current song you're listening to. By integrating with YouTube and Last.fm APIs, this app fetches the song information and updates your bio accordingly. This README provides a comprehensive guide to set up and configure the app.

## Prerequisites

Before you start, ensure you have the following:
- Python 3.6 or higher
- pip (Python package installer)
- Access to YouTube Data API and Last.fm API

## Install Instructions

### On Windows

1. **Install Python:**
   - Download the Python installer from the [official Python website](https://www.python.org/downloads/).
   - Run the installer and make sure to check the box "Add Python to PATH" before clicking "Install Now".

2. **Install pip:**
   - Pip is included by default with Python installations. You can verify it by running `pip --version` in Command Prompt.

3. **Install required modules:**
   - Open Command Prompt and run:
     ```bash
     pip install flask requests
     ```

### On Linux

1. **Install Python:**
   - Use your package manager to install Python. For Debian-based systems (like Ubuntu), run:
     ```bash
     sudo apt update
     sudo apt install python3 python3-pip
     ```

2. **Install required modules:**
   - Open a terminal and run:
     ```bash
     pip3 install flask requests
     ```

## Getting API Keys for YouTube and Last.fm

1. **YouTube Data API:**
   - Go to the [Google Developers Console](https://console.cloud.google.com/apis/api/youtube.googleapis.com/).
   - Create a new project or select an existing one.
   - Navigate to the "Credentials" section.
   - Click "Create Credentials" and choose "API Key".
   - Save the API Key for use in the app.

2. **Last.fm API:**
   - Visit the [Last.fm API page](https://www.last.fm/api/).
   - Sign up for a Last.fm account if you don't have one.
   - Go to the "Create an API Account" section.
   - Follow the instructions to obtain your API Key.

## Filling the API Keys into `app.py`

Open the `app.py` file and locate the following lines:

```python
# API-Daten
api_key = 'LAST_FM_API_HERE'
youtube_api_key = 'YOUTUBE_API_HERE'
```

# API-Daten
api_key = 'LAST_FM_API_HERE'
youtube_api_key = 'YOUTUBE_API_HERE'
Replace `'LAST_FM_API_HERE'` with your Last.fm API Key and `'YOUTUBE_API_HERE'` with your YouTube Data API Key.

## Getting the Session Token

1. Open the Y99 web application and press `F12` to open Developer Tools.
2. Navigate to the "Network" tab.
3. Look for a request with the name "whatsup".
4. Click on this request and go to the "Payload" tab.
5. Find the `auth` field in the payload section. The `session-token` value is what you need.

Copy this session token and ensure it is used in your application as required.

## Usage

1. **Run the App:**
   - Execute the following command in your terminal or command prompt:
     ```bash
     python app.py
     ```
2. **Monitor:**
   - The app will fetch the current song from Last.fm and update your Y99 bio accordingly.

## Troubleshooting

- **API Errors:** Ensure that your API keys are correctly configured and have the necessary permissions.
- **Network Issues:** Verify your internet connection and check the network settings.

For further assistance, please refer to the [official documentation](https://example.com) or contact support.

Have fun with your cool new Bio
```

This version maintains proper Markdown formatting throughout the entire document. Let me know if you need any additional changes!
