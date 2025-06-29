## 🧠 Local AI Automation Setup using Ollama + Browser-Use
---

### 📌 Overview
In this project, I created a **fully local AI-powered automation environment** using my **Ubuntu machine** and **NVIDIA Ada 2000 GPU**. The setup replicates OpenAI Operator's functionality, but runs entirely offline and privately on my system. Here's what I did:

1. Install and run **Ollama** on Ubuntu
2. Download and use local AI models like **LLaMA 3** and **DeepSeek**
3. Set up **Browser-Use** to automate web tasks locally
4. Run everything using your **GPU (NVIDIA Ada 2000)**
5. Automate Amazon task: **Search for NVIDIA GPU → Add to Cart → Checkout**
---

## 🧰 Prerequisites
- ✅ Ubuntu 20.04 or 22.04
- ✅ NVIDIA Ada 2000 GPU (CUDA support)
- ✅ Python ≥ 3.10
- ✅ Git
- ✅ GPU drivers installed
---

## ⚙️ Step 1: Installing Ollama on Ubuntu
```bash
curl -fsSL https://ollama.com/install.sh | sh
```
### ✅ Verify Installation
```bash
ollama --version
```
---

## 🧠 Step 2: Running AI Models Locally
### 🔹 Install LLaMA 3 Model
```bash
llama run llama3
```
### 🔹 Install DeepSeek Model
```bash
ollama pull deepseek-coder
ollama run deepseek-coder
```
>  Use `ollama list` to confirm installed models. 

---

## 🧮 Step 3: Use NVIDIA Ada 2000 GPU
Ensure Ollama is using GPU:

```bash
nvidia-smi
```
>  GPU usage increases when a model is running. 

---

## 🌐 Step 4: Setup Browser-Use (Operator-like Automation)
## Installation Guide
#### Step 1: Clone the Repository
```
git clone https://github.com/browser-use/web-ui.git
cd web-ui
```
#### Step 2: Set Up Python Environment
We recommend using [﻿uv](https://docs.astral.sh/uv/) for managing the Python environment.

Using uv (recommended):

```
uv venv --python 3.11
```
Activate the virtual environment:

- Windows (Command Prompt):
```
.venv\Scripts\activate
```
- Windows (PowerShell):
```
.\.venv\Scripts\Activate.ps1
```
- macOS/Linux:
```
source .venv/bin/activate
```
#### Step 3: Install Dependencies
Install Python packages:

```
uv pip install -r requirements.txt
```
Install Browsers in playwright.

```
playwright install --with-deps
```
Or you can install specific browsers by running:

```
playwright install chromium --with-deps
```
#### Step 4: Configure Environment
1. Create a copy of the example environment file:
- Windows (Command Prompt):
```
copy .env.example .env
```
- macOS/Linux/Windows (PowerShell):
```
cp .env.example .env
```
1. Open `.env`  in your preferred text editor and add your API keys and other settings
#### Step 5: Enjoy the web-ui
1. **Run the WebUI:**python webui.py --ip 127.0.0.1 --port 7788
2. **Access the WebUI:** Open your web browser and navigate to `http://127.0.0.1:7788` 




## 🛒 Step 6: Amazon Automation Task
**Automation Flow:**

- Open browser
- Go to [﻿amazon.in](https://www.amazon.in/) 
- Search: “LAPTOPS”
- Select first result
- Add to Cart
- Proceed to Checkout
---

## 🧠 Benefits of This Local Stack
| Feature | Status |
| ----- | ----- |
| Fully Offline AI | ✅ Yes |
| Browser Automation | ✅ Yes |
| OpenAI Operator Clone | ✅ With  |
| GPU Acceleration | ✅ Ada 2000 Enabled |
| No Cloud/API Needed | ✅ Fully Local |
| Real Task Executed | ✅ Amazon checkout |
---



