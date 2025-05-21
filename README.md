Web UI Setup Guide (Browser-Use Project)
This document provides a complete, step-by-step guide to setting up and running the browser-use/web-ui project locally.

✅ Prerequisites
1. OS: Linux (Tested on Ubuntu-based system)
2. Required Python Version
Python 3.11 (Recommended)

If you don’t have Python 3.11:
sudo apt update 
sudo apt install software-properties-common
sudo add-apt-repository ppa:deadsnakes/ppa 
sudo apt update 
sudo apt install python3.11 
python3.11-venv python3.11-dev

Then set it as default:
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.11 1






🔧 Project Setup Steps
1. Clone the Repository
git clone https://github.com/browser-use/web-ui.git
cd web-ui

2. Create and Activate Virtual Environment (if not using uv)
python3.11 -m venv .venv
source .venv/bin/activate

If using uv (recommended) :- 
curl -LsSf https://astral.sh/uv/install.sh | sh
uv venv --python 3.11
source .venv/bin/activate


3. Install Python Dependencies
uv pip install -r requirements.txt

If you see missing packages, install manually:
pip install gradio python-dotenv browser-use

4. Install Playwright Browsers
playwright install

Or just install Chromium:
playwright install chromium

5. No Need to Create or setup .env File


🧪 Run the Web UI
python webui.py --ip 127.0.0.1 --port 7788

Then open your browser and go to: http://127.0.0.1:7788

After Opening the Web UI application in the browser :- 
 
In the LLM Provider Select :- gemini/google
Model Name :- gemini-2.0-flash



Then For the API Key go to Browser and Search For Gemini API Key :-
 Go for Google AI Studio > Get API Key > Create API key > Gemini API 
Then Select the generated API key and paste in the Web UI API key Section



Now in the Web-Ui application > Browser Settings > Use Own Browser 

Now then Go to Run Agent :- 
 
Write your desired prompt that you want it to be done by the AI  and then Click Submit Task button.

You have successfully Integrated the AI in your Browser      





📝 Final Notes
Use Python 3.11 as tested for compatibility.


Activate .venv every session.


Use only supported models for browser agents.


Playwright must have browsers installed (playwright install).




