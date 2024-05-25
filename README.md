# PDF-chat-AI-with-voice
PDF-chat-AI-with-voice is an AI-powered application that enables you to interact with the content of your PDF files using natural language queries. By leveraging AWS Bedrock and Amazon Polly, the application provides detailed answers to your questions and reads them out loud in your chosen voice.

## Features
Natural Language Processing: Ask questions about the content of your PDF files and get detailed, context-aware answers.
Voice Responses: Hear the answers read out loud using Amazon Polly.
Multiple Voice Options: Choose between male and female voices for the audio responses.
Automatic Audio Playback: Responses are played automatically without needing user intervention.

## Requirements
Python 3.7 or higher,
Streamlit,
Boto3,
dotenv,
langchain,
langchain_community,
numpy,
PyPDF2,
IPython


## Installation
Clone the repository:
``` sh
git clone https://github.com/Rithik53/PDF-chat-AI-with-voice.git
cd PDF-chat-AI-with-voice
```
Create a virtual environment and activate it:

``` sh
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```
Install the required packages:

``` sh
pip install -r requirements.txt
```
Set up your environment variables:
Create a .env file in the root directory and add your AWS credentials and ElevenLabs API key:

```makefile
AWS_ACCESS_KEY_ID=your_aws_access_key_id
AWS_SECRET_ACCESS_KEY=your_aws_secret_access_key
ELEVENLABS_API_KEY=your_elevenlabs_api_key
```
## Usage
Data Ingestion:
Ensure your PDF files are in a directory named data in the root of the project.

##Run the Application:
```sh
streamlit run app.py
```
## Interact with the Application:

Navigate to the Streamlit web interface.
Use the sidebar to update or create the vector store from the PDF files.
Ask questions in the text input field and choose the voice for audio responses.
Click on "Claude Output" or "Llama2 Output" to get answers and hear them read out loud.

## Components
Data Ingestion
The application loads PDF files from the data directory and splits the text into manageable chunks for processing.

Vector Store
FAISS is used to create a vector store of the PDF content, allowing for efficient similarity search and retrieval.

LLM Models
Two models are available for generating responses:

Claude (ai21.j2-mid-v1)
Llama2 (meta.llama2-70b-chat-v1)
Voice Synthesis
Amazon Polly is used to synthesize the text response into speech. The audio is played automatically using an embedded HTML audio player.

Customization
You can customize various aspects of the application, such as the chunk size for text splitting, the models used for generating responses, and the voices for audio playback.

Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

License
This project is licensed under the MIT License.

## Acknowledgements
AWS Bedrock,
Amazon Polly,
Streamlit,
LangChain,
ElevenLabs
