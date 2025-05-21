✅ Enhanced GitHub-Friendly Markdown Version (README.md)
md
Copy
Edit
# Web UI Setup Guide (Browser-Use Project)

This document provides a complete, step-by-step guide to setting up and running the `browser-use/web-ui` project locally.

---

## ✅ Prerequisites

**OS:** Linux (tested on Ubuntu-based system)  
**Python Version:** 3.11 (recommended)

### Install Python 3.11

sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.11 python3.11-venv python3.11-dev


🔧 Project Setup Steps
1. Clone the Repository
git clone https://github.com/browser-use/web-ui.git
cd web-ui
2. Create and Activate Virtual Environment
Option A: Traditional venv

python3.11 -m venv .venv
source .venv/bin/activate
Option B: Using uv (recommended)

curl -LsSf https://astral.sh/uv/install.sh | sh
uv venv --python 3.11
source .venv/bin/activate
3. Install Python Dependencies

uv pip install -r requirements.txt
If you face missing packages:


pip install gradio python-dotenv browser-use
4. Install Playwright Browsers
Install all:


playwright install
Or only Chromium:


playwright install chromium
5. Skip .env File Setup
No .env setup is needed for this project.

🧪 Run the Web UI
python webui.py --ip 127.0.0.1 --port 7788
Open your browser at:
http://127.0.0.1:7788

⚙️ Configuring the Web UI
In the LLM Provider dropdown, select: gemini/google

Set Model Name to: gemini-2.0-flash

For the API Key:

Go to Google → Search “Gemini API Key”

Open Google AI Studio

Click Get API Key > Create API Key > Gemini API

Copy and paste the key into the Web UI

🧠 Using Your Own Browser
In the Web UI:

Navigate to Browser Settings

Enable Use Own Browser

Then:

Go to Run Agent

Enter your prompt

Click Submit Task

🎉 You’ve successfully integrated Gemini AI into your browser!

📝 Final Notes
Use Python 3.11 for compatibility

Activate .venv every session

Stick to supported models

Don’t forget playwright install

---

