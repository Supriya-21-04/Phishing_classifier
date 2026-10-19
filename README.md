## Phishing Email Detection using NLP 🛡️

This project detects phishing emails using Natural Language Processing (NLP) and a machine learning model. It includes a Flask application, a Chrome extension, and Gmail inbox scanning via IMAP.

## 📌 Features

- Detect if an email is **phishing or safe**
- Display phishing and safe probability scores (%)
- Fetch recent emails from a Gmail inbox and classify them
- Use the Chrome extension to display the latest fetched email and its classification

## Setup Instructions 🛠️

### 1. Install Dependencies

Run `pip install -r requirements.txt`

### 2. Train the Model

Run `python3 spamming.py`

This trains an `XGBClassifier` using TF-IDF text features and custom text features, then saves the model assets in the `model/` directory. After training, the script starts an interactive command-line classifier; type `exit` to quit.

**Note:** The script creates a train/test split but does not report evaluation metrics. No verified model-performance results are included in this repository.

### 3. Run the Flask Application

Run `python3 app.py`

By default, the application runs at `http://127.0.0.1:5000/`.

## Chrome Extension Setup

1. Open `chrome://extensions/`.
2. Enable Developer mode.
3. Click **Load unpacked**.
4. Select the `extension/` folder.
5. Click the extension icon and choose **Fetch Last Email**.

The extension fetches email through the application; it does not read the email currently open in a browser tab.

