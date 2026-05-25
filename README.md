# 🔒 Portable Uncensored AI - Runs Entirely from a USB Drive

A **fully private, portable, uncensored AI assistant** that runs 100% from a USB flash drive. No internet needed after setup. No data leaves the USB. Works on **Windows**, **Mac**, and **Linux**.

**Now with multi-model support!** Choose from 6 curated AI models or bring your own.

## ⚡ Available Models

During installation, you'll choose which model(s) to download:

| #   | Model                        | Size    | Label         | Best For                                 |
| --- | ---------------------------- | ------- | ------------- | ---------------------------------------- |
| 1   | **NemoMix Unleashed 12B**    | ~7.0 GB | 🔓 UNCENSORED | ⭐ Recommended — best quality uncensored |
| 2   | **Dolphin 3.0 Llama 3.1 8B** | ~4.9 GB | 🔓 UNCENSORED | Classic uncensored all-rounder           |
| 3   | **Mistral 7B Instruct v0.3** | ~4.1 GB | 🔒 STANDARD   | Strong reasoning & coding                |
| 4   | **Qwen 2.5 7B Instruct**     | ~4.7 GB | 🔒 STANDARD   | Great multilingual support               |
| 5   | **Llama 3.2 3B Instruct**    | ~2.0 GB | 🔒 STANDARD   | Lightweight — fast on old PCs            |
| 6   | **Phi-3.5 Mini 3.8B**        | ~2.2 GB | 🔒 STANDARD   | Lightweight — good reasoning             |
| C   | **Custom GGUF**              | Varies  | 🎨 CUSTOM     | Bring your own HuggingFace model         |

> **🔓 UNCENSORED** = No content filters, answers everything  
> **🔒 STANDARD** = Normal safety guidelines apply

## 🚀 Setup (One Time Only)

### What You Need

- A USB flash drive with **at least 16 GB** of free space (32 GB recommended for multiple models)
- Format the USB as **exFAT** (works on Windows, Mac, and Linux)
- An internet connection for the initial download

### Steps

1. **Download this repo** and copy ALL files to your USB drive
2. **Double-click `install.bat`** on the USB drive
3. **Choose your model(s)** from the interactive menu
4. **Interactive AnythingLLM Setup**:
   - The AnythingLLM installer will open automatically.
   - **IMPORTANT**: When asked for the "Install Location", click **Browse** and select the `anythingllm` folder on your USB drive.
   - Wait for it to finish, then close the installer window.
5. **Done!** Your portable AI is ready to use.

### ⚠️ If a Model Download Fails

The installer automatically retries failed downloads. If it still fails:

1. **Download the model manually** from the HuggingFace resolved link shown in the console error.
2. **Place the .gguf file** into the `models\` folder on your USB.
3. **Re-run `install.bat`** — it will detect the file and skip the download.

### 🔄 Adding More Models Later

Just **re-run `install.bat`** and select additional models. Already-downloaded models are automatically skipped.

### 🎨 Custom Models

Want a model not on the list? During install, choose option **C** and paste any direct `.gguf` download link from HuggingFace. The installer handles the rest!

### 🗄️ Configuring Ollama Token Limit / Context Size

By default, the installer configures Ollama with a 4K token limit for optimal performance on most PCs. If you want to adjust this, follow these steps after install script has finished running:

1. Open this folder on your USB drive. `anythingllm_data/storage`
2. Open the `.env` file in a text editor.
3. Find the line that says `OLLAMA_MODEL_TOKEN_LIMIT=4096` and change `4096` to your desired token limit (e.g., `8192` for 8K tokens).
4. Save the file and restart the AI using the launcher script `start-windows.bat` or `start-mac.command` or `start-linux.sh`.
5. Incase if you re-run the installer script `install.bat` or `install.sh` it will reset the token limit back to 4096, so you will need to change it again in the `.env` file.
6. For mac, you may re-run the `start-mac.command` script and it will not overwrite the token limit in the `.env` file, so you can just restart the AI using this script after changing the token limit in the `.env` file.

## ▶️ How to Use

### On Windows

- Double-click **`start-windows.bat`** on the USB drive.
- **Improved Portability**: The launcher now automatically clears old path caches. This allows you to move between different computers without "JavaScript errors."
- The AnythingLLM chat window will open automatically.
- **Switch between models** in AnythingLLM: Settings → LLM → select your model.
- Keep the black terminal window open while chatting.
- Press any key in the terminal to safely shut down.

### On Mac

- Double-click **`start-mac.command`** on the USB drive.
- First time: It will automatically download the Mac engine (~2 min).
- The AnythingLLM window will open automatically.
- Press ENTER in the terminal to safely shut down.

### 🐧 On Linux

1. Open a terminal on your USB drive.
2. Run the launcher:
   make it executable first:
   ```bash
   chmod +x start-linux.sh preflight-check.sh install.sh install-core.sh
   ```
