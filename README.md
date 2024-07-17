Automating WhatsApp Messages with pywhatkit
Install the pywhatkit Module: First, you’ll need to install the pywhatkit module. Open your IDE or compiler and run the following command:
pip install pywhatkit
This will download the necessary module along with any related dependencies.
Setting Up Chrome Driver: To use pywhatkit, you’ll need a Chrome browser and your WhatsApp logged in on the web.whatsapp.com website. If you don’t have Chrome installed, follow these steps:
Download the current stable release of Chrome Driver from here.
Extract the downloaded file and find an application named chromedriver.exe.
Copy its path (e.g., C:/Users/.../chromedriver.exe).
In your Python script, call pywhatkit.add_driver_path(path) and pass the copied path as an argument. If the path is valid, a black window along with Chrome will open and close.
Next, call pywhatkit.load_QRcode() to scan the QR code on the web.whatsapp.com page.
Sending a WhatsApp Message: Here’s a simple example of sending a message using pywhatkit:
Python

import pywhatkit

# Replace with the recipient's phone number and your message
recipient_number = "+919xxxxxxxxx"
message = "Hello from Python!"

# Specify the time (24-hour format) at which you want to send the message
hour = 18
minute = 30

# Send the message
pywhatkit.sendwhatmsg(recipient_number, message, hour, minute)
AI-generated code. Review and use carefully. More info on FAQ.Note:
The time follows the 24-hour format (e.g., 18:30 is 6:30 PM).
Provide at least 2-3 minutes of future time from the current time to avoid errors.
Make sure you’re logged in to WhatsApp web in Google Chrome before running the script.
Execution and Results: After running the script, it will inform you how many seconds until WhatsApp opens and when the message will be sent. For example, in 51 seconds, web.whatsapp.com will open, and after 20 seconds, the message will be delivered. 🚀 And there you have it! Your Python script is now automating WhatsApp messages. Feel free to customize it further or explore other features offered by pywhatkit
