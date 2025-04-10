# youtube-live-chat-sentiment
This repository contains Python code to fetch live chat messages from a YouTube live video, perform real-time sentiment analysis on the comments, and display the results. It utilizes the YouTube Data API, the TextBlob library for sentiment analysis, and provides timestamp conversion for better readability.

## Prerequisites

Before running the script, ensure you have the following:

* **Python 3 installed:** You can download it from [https://www.python.org/downloads/](https://www.python.org/downloads/).
* **pip installed:** Python's package installer, usually included with Python.
* **Google Cloud Project and YouTube Data API Key:**
    * You need a Google Cloud Project.
    * The **YouTube Data API v3** must be enabled for your project.
    * You need to create **API credentials** of type "API key".
    * **Important:** Keep your API key secure and do not share it publicly.
* **YouTube Live Video ID:** The unique identifier of the live YouTube video you want to analyze. This is found in the video URL after `v=`. For example, in `https://www.youtube.com/watch?v=sFCnoyKXebU`, the video ID is `sFCnoyKXebU`.

## Installation

1.  **Clone the repository (if you have it on GitHub):**
    ```bash
    git clone [repository-url]
    cd youtube-live-chat-sentiment
    ```
2.  **Install the required Python libraries:**
    ```bash
    pip install google-api-python-client
    pip install textblob
    pip install python-dateutil
    pip install pytz
    ```

## Setup

1.  **Save the Python code:** Save the provided Python script as a `.py` file (e.g., `live_sentiment_analyzer.py`).
2.  **Replace placeholders in the script:**
    * Open `live_sentiment_analyzer.py` in a text editor.
    * Replace `"AIzaSyC-T6qGelPPdbeXGC62p2of076WGhosJbw"` with your **actual YouTube Data API key**.
    * Replace `"sFCnoyKXebU"` with the **ID of the live YouTube video** you want to analyze.

## Usage

1.  **Open your terminal or command prompt.**
2.  **Navigate to the directory where you saved the `live_sentiment_analyzer.py` file.**
    ```bash
    cd path/to/your/project/folder
    ```
3.  **Run the script:**
    ```bash
    python live_sentiment_analyzer.py
    ```

## Output

The script will output the following information for the last 5 live chat messages every 5 seconds (for a maximum of 60 seconds):

* **Current Time:** The current timestamp when the comment was fetched (in IST).
* **Author:** The display name of the user who posted the comment.
* **Message:** The text content of the live chat message.
* **Sentiment:** The sentiment analysis result ("positive", "negative", or "neutral") for the message.
* **Timestamp:** The original timestamp of the comment as provided by YouTube (in a human-readable format with timezone).

If no comments are found, it will print "No comments found." If the maximum duration is exceeded or the script fails after retries, it will indicate that.

## Important Notes

* **API Key Security:** Ensure your API key is kept confidential and not exposed in public code. Consider using environment variables for storing sensitive information.
* **API Quota:** Be aware of the YouTube Data API's usage quotas. Excessive requests might lead to quota exhaustion.
* **Live Video Requirement:** This script is designed to analyze live chat messages from currently active YouTube live videos. It will not work with past broadcasts.
* **Sentiment Analysis:** The sentiment analysis is performed using the `TextBlob` library, which provides a basic level of sentiment analysis. For more advanced or nuanced analysis, consider using other NLP libraries or cloud-based services.
* **Error Handling:** The script includes basic error handling for API quota exceeded errors. You might want to enhance error handling for other potential issues.

## Author

Swetha0515

![image](https://github.com/user-attachments/assets/a779a8ca-302b-40a5-a2f0-62ad30663305)


