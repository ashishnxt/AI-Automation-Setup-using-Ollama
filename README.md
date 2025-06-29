## 🧠 Local AI Automation Setup using Ollama + Browser-Use
---

### 📌 Overview
This document outlines the step-by-step process to:

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
ollama run llama3
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
### 📥 Clone Repository
```bash
git clone https://github.com/browser-use/browser-use.git
cd browser-use
```
### 🔧 Create Python Virtual Environment
```bash
python3 -m venv .venv
source .venv/bin/activate
```
### 🧪 Install Dependencies
```bash
pip install -r requirements.txt
```
---

## 🤖 Step 5: Link Browser-Use with Local Ollama Models
Edit `config.py` or within scripts to connect with local Ollama:

```python
OLLAMA_API = "http://localhost:11434"
MODEL = "llama3"
```
## 🔄 Step 5: Enjoy the web-ui
1. **Run the WebUI:** python webui.py --ip 127.0.0.1 --port 7788
2. **Access the WebUI:** Open your web browser and navigate to `http://127.0.0.1:7788` 


---

## 🛒 Step 6: Amazon Automation Task
**Automation Flow:**

- Open browser
- Go to [﻿amazon.in](https://www.amazon.in/) 
- Search: “LAPTOP”
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



