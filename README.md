# Audio Assistant Using XIAO_ESP32_S3

## Overview
This project demonstrates the How to use ESP32-S3 as audio Assistant. The recorded audio file is stored on the ESP32's microSD card. The goal is to convert this audio file into text using Google Cloud Speech-to-Text API and further generate a response from the ChatGPT API.

## Components

- ESP32-S3 Microcontroller
- MicroSD Card (Installed in ESP32)
- Google Cloud Speech-to-Text API
- ChatGPT API

## Setup

1. **Install Dependencies:**
   - Ensure that the required libraries and dependencies are installed on the ESP32-S3. Refer to the `code_for_xiao_Esp32-s3.ino` file for the specific libraries and versions needed.

2. **Hardware Connection:**
   - Go to Official Documentation For hardware installation.

3. **MicroSD Card:**
   - Insert a microSD card into the ESP32-S3 to store the recorded audio file.

4. **Build Local Server and use Google Cloud Speech-to-Text API:**
   - Set up a Google Cloud project and enable the Speech-to-Text API.
   - Obtain the necessary API credentials and configure them in the Server Side Code.

5. **ChatGPT API:**
   - Obtain API key(s) for the ChatGPT API.
   - Configure the API key(s) in the ESP32 code for making requests.

## Workflow

1. **Audio Recording:**
   - Utilize the ESP32-S3 microphone to record audio.
   - Save the recorded audio file to the microSD card.

2. **Send Audio to Server:**
   - Initiate a POST request to a server, passing the recorded audio file.

3. **Server Processing:**
   -#Set Your Authentication environment variable
     For PowerShell: $env:GOOGLE_APPLICATION_CREDENTIALS="KEY_PATH"
   -  The server processes the audio file using the Google Cloud Speech-to-Text API, converting it into text.
   - The text response is sent back to the ESP32 as the result of the POST request.
   -

4. **ChatGPT Interaction:**
   - Use the obtained text transcript as input for the ChatGPT API.
   - Receive the ChatGPT's response.
   #Dont forget to change API key for ChatGPT

## Important Notes

- Ensure that the ESP32-S3 is connected to the internet for API communication.
- Protect sensitive information such as API keys and credentials.
- Verify the compatibility of the ESP32-S3 libraries and firmware.

## Acknowledgments

This project utilizes the Google Cloud Speech-to-Text API and ChatGPT API for audio processing and using text to  generate Response.

Feel free to contribute, report issues, or make suggestions!


