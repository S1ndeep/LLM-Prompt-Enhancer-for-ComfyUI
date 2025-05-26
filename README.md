🔮 LLM Prompt Enhancer for ComfyUI
A custom node for ComfyUI that utilizes local language models (LLMs) to refine, expand, and enhance your text-to-image prompts—resulting in higher quality generations with minimal manual effort.

🚀 Setup Instructions
Step 1: Download the Required Model
Model Name: Mistral-7B-Instruct-v0.3.Q4_K_M.gguf

Size: 4.37 GB

Source: HuggingFace – MaziyarPanahi/Mistral-7B-Instruct-v0.3-GGUF

Step 2: Install the Model in ComfyUI
Navigate to your ComfyUI installation directory.

Create a new folder:

plaintext
Copy
Edit
ComfyUI/models/llm_models/
Place the downloaded .gguf model file inside that folder.

✅ Only .gguf models compatible with llama-cpp-python are supported.

⚙️ Node Configuration
Parameter	Description	Default
Input Text	Your initial prompt or concept for enhancement.	(Required)
Model Selection	Select a GGUF model from llm_models/.	—
Max Tokens	Maximum number of tokens in the output prompt.	128
Instruction Template	Template for how the LLM interprets the prompt. E.g.: Improve this prompt: {prompt}	—
Temperature	Controls randomness (range: 0.1–2.0).	1.0
Top-P	Filters to top cumulative probability tokens.	0.9
Top-K	Limits token selection to top-K candidates per generation step.	50
Repetition Penalty	Penalizes repetitive phrases.	1.2

🧩 Compatibility & Requirements
✅ Works with llama-cpp-python and GGUF models

💻 Requires a system with sufficient RAM/VRAM (minimum 8 GB recommended)

🧠 Supports both CPU and GPU inference (GPU requires CUDA/cuBLAS compatibility)

🛠️ Troubleshooting
🔧 Common Issue: Missing llama-cpp-python
If using ComfyUI Windows Portable, follow these steps:

Open a terminal in:


ComfyUI_windows_portable/python_embeded/
Run:

python -m pip install llama-cpp-python --prefer-binary
python -m pip install https://github.com/oobabooga/llama-cpp-python-cuBLAS-wheels/releases/download/textgen-webui/llama_cpp_python_cuda-0.2.89+cu121-cp311-cp311-win_amd64.whl
🔁 Still Not Working?
Try a clean reinstall:


pip uninstall llama-cpp-python -y
pip install llama-cpp-python
✅ Ensure CUDA/cuBLAS versions match your GPU driver for acceleration.

📬 Support & Contributions
💡 Feature Requests: Open an issue on GitHub

🐞 Bug Reports: Include error logs and detailed steps to reproduce

🤝 Pull requests welcome for new features, bug fixes, or improvements

📜 License
MIT License – Free to use, modify, and distribute for both personal and commercial projects.

✔️ Rewritten for clarity, accessibility, and structure.
✔️ Headings and technical descriptions have been reorganized for better UX.
