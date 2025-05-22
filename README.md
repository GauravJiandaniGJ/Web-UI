# Web UI Setup Guide (Browser-Use Project)

This document provides a complete, step-by-step guide to setting up and running the `browser-use/web-ui` project locally.

---

## ✅ Prerequisites

**OS:** Linux (tested on Ubuntu-based system)  
**Python Version:** 3.11 (recommended)

### 🔹 Install Python 3.11

```bash
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.11 python3.11-venv python3.11-dev

🔹 Set Python 3.11 as Default
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.11 1

🔧 Project Setup Steps

1. Clone the Repository
git clone https://github.com/browser-use/web-ui.git
cd web-ui

2. Create and Activate Virtual Environment
Option A: Traditional venv
python3.11 -m venv .venv
source .venv/bin/activate

Option B: Using uv (Recommended)

curl -LsSf https://astral.sh/uv/install.sh | sh
uv venv --python 3.11
source .venv/bin/activate

3. Install Python Dependencies
uv pip install -r requirements.txt
If you see missing packages, install manually:
pip install gradio python-dotenv browser-use

4. Install Playwright Browsers
Install all browsers:
playwright install

If any error :- 

sudo $(python -m playwright install-deps)


Or just install Chromium:
playwright install chromium

5. No Need to Create or Configure .env File
🧪 Run the Web UI
python webui.py --ip 127.0.0.1 --port 7788
Open your browser and go to:

http://127.0.0.1:7788

⚙️ Configuring the Web UI

In the LLM Provider dropdown, select: gemini/google

Set Model Name to: gemini-2.0-flash-exp

For the API Key:

Go to Google and search for: Gemini API Key

Open Google AI Studio

Click Get API Key > Create API Key > Gemini API

Copy and paste the key into the Web UI

🧠 Using Your Own Browser
In the Web UI:

Go to Browser Settings

Enable Use Own Browser

Then:

Navigate to Run Agent

Enter your prompt

Click Submit Task

🎉 You’ve successfully integrated Gemini AI into your browser!

📝 Final Notes
Use Python 3.11 for compatibility

Always activate .venv in every session

Stick to supported models for stability

Ensure playwright install is run before using browser automation
